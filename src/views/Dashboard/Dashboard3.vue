<template>
  <es-codemirror :code="code"></es-codemirror>
</template>

<script>

  import esCodemirror from '@/components/es-codemirror-vue'
  export default {
    name: "Dashboar3",
    components:{
      esCodemirror
    },
    data(){
      return{
        code: `<template>
            <h1>Hello World!</h1>
            <codemirror v-model="code" :options="cmOption" />
          </template>
          <script>
            // import 'some-codemirror-resource'
            export default {
              data() {
                return {
                  code: 'const A = 10',
                  cmOption: {
                    tabSize: 4,
                    styleActiveLine: true,
                    lineNumbers: true,
                    line: true,
                    foldGutter: true,
                    styleSelectedText: true,
                    mode: 'text/javascript',
                    keyMap: "sublime",
                    matchBrackets: true,
                    showCursorWhenSelecting: true,
                    theme: "monokai",
                    extraKeys: { "Ctrl": "autocomplete" },
                    hintOptions:{
                      completeSingle: false
                    }
                  }
                }
              }
            }
          ${'<\/script>'}
          <style lang="scss">
            @import './sass/mixins';
            @import './sass/variables';
            main {
              position: relative;
            }
          </style>`
      }
    }
  }
</script>

<style scoped>

</style>
