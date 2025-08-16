<script>
import { ref, h } from 'vue'

export default {
  setup(props) {
    const someVar = ref(false)
    window.someVar = someVar;

    return function () {
      var arr = [
        h("div", { key: "uno" }, "ahh 1")
      ]

      if (someVar.value) {
        arr.push(h("div", { key: "dos" }, "ahh 2"))
      }

      arr.push(h("div", { key: "tres", id: "someID" }, "ahh 3"))

      return arr
    }
  }
}
</script>