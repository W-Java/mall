<template>
  <div class="tab-bar-item" @click="itemClick">
<!--    v-if来判断输出哪一张颜色的图片-->
    <div v-if="!isActive">
      <slot name="item-img"></slot>
    </div>
    <div v-else>
      <slot name="item-img-active"></slot>
    </div>
<!--    动态绑定style 可以设定文字的对应颜色-->
    <div :style="activeStyle">
      <slot name="item-text"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
    path: String,
    activeColor: {
      type: String,
      default: 'red'
    }
  },
  data() {
    return {
    }
  },
  computed: {
    // 用来判断此时谁处于活跃状态
    isActive() {
      // 判断当前活跃的组件和我的组件路径是不是一样的
      return this.$route.path.indexOf(this.path) != -1
    },
    // 用来设置style是否添加
    activeStyle() {
      return this.isActive ? {color: this.activeColor} : {}
    }
  },
  methods: {
    itemClick() {
      this.$router.replace(this.path)
    }
  }
}
</script>

<style>

.tab-bar-item {
  /*设置均匀分布*/
  flex: 1;
  /*高度*/
  height: 49px;
  /*设置居中*/
  text-align: center;
  /*字体大小*/
  font-size: 15px;
}

.tab-bar-item img {
  width: 24px;
  height: 24px;
  margin-top: 3px;
  margin-bottom: 2px;
  vertical-align: middle;
}


</style>
