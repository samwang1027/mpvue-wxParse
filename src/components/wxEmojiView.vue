<template>
  <view class="WxEmojiView wxParse-inline" :style="node.styleStr">
    <block v-for="node of node.textArray" :key="node.index">
      <block v-if="node.node == 'text'">{{node.text}}</block>
      <block v-else-if="node.node == 'element'">
        <image :class="wxEmoji" :src="node.baseSrcnode.text" />
      </block>
    </block>
  </view>
</template>

<script>
export default {
  name: 'WxEmojiView',
  props: {
    node: {}
  }
}
</script>
