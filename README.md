
# 拖拽指令引用

```vue

<child v-directives-drag />

<template>
  <span
    class="line-drag-point"
    :style="`left: ${currentPosition.x}px;top: ${currentPosition.y}px`"
  ></span>
</template>

<script lang="ts">
import { H3Draggable } from '@/drag';

@Component({
  name: "child"
  })
export default class child extends Vue implements H3Draggable {
  onDragstart(evt: DragEvent) {
    // console.log('开始拖拽', evt);
  }
}
</script>
```

```ts
<child v-directives-drop />

onDragenter(evt: DragEvent) {
  // console.log("拖拽进入到绘图区：", evt);
}
onDrop(evt: DragEvent) {
  // console.log("放置了节点到绘图区：", evt);
}

```

```ts
//活动节点

<child v-directives-activity-drag />

onDragstart(evt: DragEvent) {
    /* 开始操作节点 */
}

onDragend(evt: DragEvent) {
    /* 结束操作节点 */
}
```


