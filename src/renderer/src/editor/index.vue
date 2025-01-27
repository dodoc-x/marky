<script lang="ts" setup>
import StarterKit from '@tiptap/starter-kit'
import { EditorContent, useEditor } from '@tiptap/vue-3'

defineOptions({
  name: 'MaskyEditor',
})

const editor = useEditor({
  content: '<p>Masky editor 🎉</p>',
  extensions: [StarterKit],
})
</script>

<template>
  <EditorContent :editor="editor" />
</template>
