<script lang="ts" setup>
import Link from '@tiptap/extension-link'
import Table from '@tiptap/extension-table'
import TableCell from '@tiptap/extension-table-cell'
import TableHeader from '@tiptap/extension-table-header'
import TableRow from '@tiptap/extension-table-row'
import TaskItem from '@tiptap/extension-task-item'
import TaskList from '@tiptap/extension-task-list'
import StarterKit from '@tiptap/starter-kit'
import { EditorContent, useEditor } from '@tiptap/vue-3'

defineOptions({
  name: 'MaskyEditor',
})

const editor = useEditor({
  content: '<p>Masky editor 🎉</p>',
  extensions: [
    StarterKit,

    // node
    Table,
    TableRow,
    TableHeader,
    TableCell,
    TaskList,
    TaskItem,

    // mark
    Link,
  ],
  editorProps: {
    attributes: {
      class: 'py-4 px-6 focus:outline-none',
    },
  },
})
</script>

<template>
  <EditorContent :editor="editor" />
</template>
