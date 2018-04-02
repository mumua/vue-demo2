<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <!--<ul>
       <li>
        <a
          href="https://vuejs.org"
          target="_blank"
        >
          Core Docs
        </a>
      </li>
      <li>
        <a
          href="https://forum.vuejs.org"
          target="_blank"
        >
          Forum
        </a>
      </li>
      <li>
        <a
          href="https://chat.vuejs.org"
          target="_blank"
        >
          Community Chat
        </a>
      </li>
      <li>
        <a
          href="https://twitter.com/vuejs"
          target="_blank"
        >
          Twitter
        </a>
      </li>
      <br>
      <li>
        <a
          href="http://vuejs-templates.github.io/webpack/"
          target="_blank"
        >
          Docs for This Template
        </a>
      </li>
    </ul> -->
    <!-- <h2>Ecosystem</h2>
    <ul>
      <li>
        <a
          href="http://router.vuejs.org/"
          target="_blank"
        >
          vue-router
        </a>
      </li>
      <li>
        <a
          href="http://vuex.vuejs.org/"
          target="_blank"
        >
          vuex
        </a>
      </li>
      <li>
        <a
          href="http://vue-loader.vuejs.org/"
          target="_blank"
        >
          vue-loader
        </a>
      </li>
      <li>
        <a
          href="https://github.com/vuejs/awesome-vue"
          target="_blank"
        >
          awesome-vue
        </a>
      </li>
    </ul> -->
    <div @click='testevent' >
      {{data1| cap}}
    </div>
    <a v-bind:href="url" v-bind:target="target">连接</a>
    <div  v-if="stylename" v-bind:class="{'stylename':stylename}" v-html="data">11</div>
      <input type="text" v-model="data1"/>
   </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to my Vue.js App',
      data1: 'heloworld',
      url: 'https://www.baidu.com',
      target: '_blank',
      testevent () {
        alert('dianji')
      },
      stylename: true,
      sitess: [{ name: 'Runoob' }, { name: 'Google' }, { name: 'Taobao' }],
      boj: {
        2: '学的不仅是技术，更是梦想！',
        1: '菜鸟教程',
        0: 'http://www.runoob.com'
      }
    }
  },
  computed: {
    sited: {
      get: function () {
        return this.name + '' + this.url
      },
      set: function (newValue) {
        let names = newValue.split('')
        this.name = name[0]
        this.url = name[names.length - 1]
      }
    }
  },
  filters: {
    cap: function (data) {
      if (!data) return ''
      data = data.toString()
      return data.charAt(0).toUpperCase() + data.slice(1)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.stylename {
  color: #42b983;
}
</style>
