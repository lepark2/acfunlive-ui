<template>
  <div>
    <el-button style="margin-left: 30px; margin-top: 30px;" @click="liveDialog = true">
      订阅主播
    </el-button>
    <LiveConfigDialog :show-dialog="liveDialog" @hideDialog="liveDialog = false" />
    <el-divider />
    <el-link
      type="primary"
      :href="href"
      target="_blank"
      style="margin-left: 50px"
    >
      显示日志
    </el-link>
  </div>
</template>

<script>
export default {
  data () {
    return {
      liveDialog: false,
      href: `http://${location.hostname}:51880/log`
    }
  }
}
</script>
