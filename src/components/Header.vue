<template>
  <div class="wrapper">

    <a-row class="grid-demo">
      <a-col :span="6">
        <div class="logoBar"> <!-- #region logo -->
          <img class="logo" height="32px" src="@/assets/logo.svg" alt="Vue logo" />ColleagueRate
          <!-- #endregion -->
        </div>
      </a-col>
      <a-col :span="6">
      </a-col>
      <a-col :span="10">
        <div>
          <!-- #region nav -->
          <nav class="nav">
            <router-link to="/" exact>主页</router-link>
            <router-link to="/list" exact>排名</router-link>
            <router-link to="/about">关于</router-link>
          </nav>
          <!-- #endregion -->
        </div>
      </a-col>
      <a-col :span="2">
        <div>
          <!-- #region user -->
          <a-avatar>
            <IconUser />
          </a-avatar>
          <!-- #endregion -->
        </div>
      </a-col>
    </a-row>

  </div>
</template>

<script>
export default {
  name: 'Header',
  // Your component's logic goes here
}
</script>

<style scoped>
.grid-demo .arco-col {
  /* 水平居中 */
  display: flex;
  justify-content: center;
  align-items: center;
  /* 垂直居中 */
  height: 64px;
  background-color: var(--color-white);


  color: var(--color-white);
  text-align: center;
}

.wrapper1 {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  color: var(--color-white);
}

.nav {
  display: flex;
  gap: 5px;
  /* margin-right: 20px; */
}

.nav a {
  color: black;
  text-decoration: none;
  margin-left: 10px;
}

.logoBar {
  display: flex;
  align-items: center;
  gap: 10px;
  /* 字体 */
  font-size: 20px;
  font-weight: bold;
  color: var(--color-black);
}
</style>
