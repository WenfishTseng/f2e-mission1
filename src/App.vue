<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
          <a class="navbar-brand" href="#">
            <img height="30" src="img/logo.png" alt="" />
          </a>
          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mx-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <RouterLink class="nav-link active" to="/">首頁</RouterLink>
                <!-- <a class="nav-link active" aria-current="page" href="#">首頁</a> -->
              </li>
              <li class="nav-item">
                <RouterLink class="nav-link" to="/about">產品目錄</RouterLink>
              </li>
              <li class="nav-item dropdown">
                <a
                  class="nav-link dropdown-toggle"
                  href="#"
                  id="navbarDropdown"
                  role="button"
                  data-bs-toggle="dropdown"
                  aria-expanded="false"
                >
                  關於我們
                </a>
                <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                  <li><a class="dropdown-item" href="#">公司理念</a></li>
                  <li><a class="dropdown-item" href="#">歷史沿革</a></li>
                  <li><a class="dropdown-item" href="#">團隊介紹</a></li>
                </ul>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">最新消息</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">聯絡我們</a>
              </li>
            </ul>
            <form class="d-flex">
              <a href="#" class="btn btn-outline-primary me-2">線上諮詢</a>
              <a href="#" class="btn btn-primary">產品資訊</a>
            </form>
          </div>
        </div>
      </nav>
      <!-- <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav> -->
    </div>
  </header>

  <RouterView />
</template>

<style lang="scss">
$primary: red;
@import './assets/all.scss'; // 載入樣式
$primary: red;
div {
  color: $primary;
}
</style>
