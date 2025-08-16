<script>
import { ref, h } from 'vue'

export default {
  setup(props) {
    const someVar = ref(false)
    window.someVar = someVar;

    return function () {
      var arr = [
        h("div", "ahh 1")
      ]

      if (someVar.value) {
        arr.push(h("div", "ahh 2"))
      }

      arr.push(h("div", { id: "someID" }, "ahh 3"))

      return arr
    }
  }
}
</script>