<template>
  <index-md>
    <template v-slot:default>
      <demo-block>
        <p>
          通过<code>slot</code>你可以传入自定义的上传按钮类型和文字提示。可通过设置<code>limitt</code>和<code>on-exceedt</code>来限制上传文件的个数和定义超出限制时的行为。可通过设置<code>before-removet</code>来阻止文件移除操作。
        </p>
        <template v-slot:source>
          <demo-default></demo-default>
        </template>
        <template v-slot:highlight>
          <default-md></default-md>
        </template>
      </demo-block>
    </template>
    <template v-slot:demo1>
      <demo-block>
        <template v-slot:source>
          <demo1></demo1>
        </template>
        <template v-slot:highlight>
          <demo1-md></demo1-md>
        </template>
      </demo-block>
    </template>
    <template v-slot:demo2>
      <demo-block>
        <template v-slot:source>
          <demo2></demo2>
        </template>
        <template v-slot:highlight>
          <demo2-md></demo2-md>
        </template>
      </demo-block>
    </template>
    <template v-slot:demo3>
      <demo-block>
        <template v-slot:source>
          <demo3></demo3>
        </template>
        <template v-slot:highlight>
          <demo3-md></demo3-md>
        </template>
      </demo-block>
    </template>
    <template v-slot:demo4>
      <demo-block>
        <template v-slot:source>
          <demo4></demo4>
        </template>
        <template v-slot:highlight>
          <demo4-md></demo4-md>
        </template>
      </demo-block>
    </template>
    <template v-slot:demo5>
      <demo-block>
        <template v-slot:source>
          <demo5></demo5>
        </template>
        <template v-slot:highlight>
          <demo5-md></demo5-md>
        </template>
      </demo-block>
    </template>
    <template v-slot:demo6>
      <demo-block>
        <template v-slot:source>
          <demo6></demo6>
        </template>
        <template v-slot:highlight>
          <demo6-md></demo6-md>
        </template>
      </demo-block>
    </template>
    <template v-slot:table>
      <document-table title="属性" :data="attributes"></document-table>
      <document-table title="插槽" :data="slot"></document-table>
      <document-table
        title="方法"
        type="Events"
        :data="events"
      ></document-table>
    </template>
  </index-md>
</template>
<script>
import indexMd from './index.md'
import defaultMd from './default.md'
import attributes from './attributes'
import slot from './slot'
import events from './events'

import demoDefault from './default'

import demo1 from './demo1'
import demo2 from './demo2'
import demo3 from './demo3'
import demo4 from './demo4'
import demo5 from './demo5'
import demo6 from './demo6'

import demo1Md from './demo1.md'
import demo2Md from './demo2.md'
import demo3Md from './demo3.md'
import demo4Md from './demo4.md'
import demo5Md from './demo5.md'
import demo6Md from './demo6.md'

export default {
  name: 'upload',
  components: {
    defaultMd,
    indexMd,
    'demo-default': demoDefault,
    demo1,
    demo2,
    demo3,
    demo4,
    demo5,
    demo6,
    demo1Md,
    demo2Md,
    demo3Md,
    demo4Md,
    demo5Md,
    demo6Md
  },
  data () {
    return {
      attributes,
      slot,
      events
    }
  }
}
</script>
