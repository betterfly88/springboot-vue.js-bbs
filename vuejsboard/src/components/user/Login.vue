<template>
  <div class="container">
    <div class="row center-align">
      <h1>로그인</h1>
    </div>
    <div class="row center-align">
      <p th:if="${param.error != null}">
        잘못된 정보를 입력하였습니다
      </p>
    </div>
    <form method="post" action="/login">
    <input type="hidden" th:name="${_csrf.parameterName}" th:value="${_csrf.token}" />
      <div class="row">
        <div class="col s3"></div>
        <div class="col s6">
          <div class="row">
            <div class="input-field col s12">
              <input id="userId" name="userId" type="text" class="validate" autofocus="autofocus">
              <label for="userId">사용자 아이디</label>
            </div>
          </div>
          <div class="row">
            <div class="input-field col s12">
              <input id="password" name="password" type="password" class="validate">
              <label for="password">비밀번호</label>
            </div>
          </div>
          <div class="row">
            <div class="col s12 right-align">
              <input type="checkbox" class="filled-in" id="rememberMe" name="REMEMBER_ME" />
              <label for="rememberMe">자동 로그인</label>
            </div>
          </div>
          <button class="btn waves-effect waves-light" type="submit" name="action">로그인
            <i class="material-icons right">send</i>
          </button>
        </div>
        <div class="col s3"></div>
      </div>
    </form>
  </div>
</template>
