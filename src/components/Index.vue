<template>
  <div class="index">
    <div class="index-left">
      <ul>
        <li>
          <router-link to="/discover"
            ><span class="iconfont icon-yinle"></span>发现音乐</router-link
          >
        </li>
        <li>
          <router-link to="/recommend"
            ><span class="iconfont icon-yinleliebiao-"></span>推荐歌单</router-link
          >
        </li>
        <li>
          <router-link to="/newsongs"
            ><span class="iconfont icon-music"></span>最新音乐</router-link
          >
        </li>
        <li>
          <router-link to="/mvs"
            ><span class="iconfont icon-bofangMV"></span>最新MV</router-link
          >
        </li>
      </ul>
    </div>
    <main>
      <el-scrollbar style="height: 100%">
        <!-- <router-view></router-view> -->
        <slot></slot>
      </el-scrollbar>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style>
.index {
  /* height: 800px; */
  display: flex;
}

.index-left {
  width: 200px;
  min-width: 200px;
  /* background-color: #ededed; */
  text-align: center;
  border-right: 1px solid #ededed;
}

.index-left ul {
  list-style: none;
}

.index-left li {
  cursor: pointer;
  letter-spacing: 0.3rem;
  height: 60px;
  line-height: 60px;
  display: flex;
  transition: all 0.5s ease-out;
}

.index-left li:hover {
  background-color: #ffffff6b;
}

.index-left a {
  text-decoration: none;
  color: #ebebeb;
  display: block;
  width: 100%;
  height: 100%;
  font-size: 1rem;
  padding-left: 30px;
  text-align: left;
}

.index-left a::before {
  margin-right: 10px;
}

.router-link-active {
  color: #ffffff !important;
  font-weight: bold;
}

main {
  flex: 1;
  min-width: 750px;
  /* height: 800px; */
  /* overflow-y: scroll; */
  /* background-color: skyblue; */
}
</style>
