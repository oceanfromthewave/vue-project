<script>
/* computed/Computed.vue 계산된 속성 예제 작성 */
export default {
  data() {
    return {
      author: {
        name: 'John Doe',
        books: [
          'Vue 2 - Advanced Guide',
          'Vue 3 - Basic Guide',
          'Vue 4 - The Mystery'
        ]
      }
    }
  },
  computed: {
    // 계산된 값을 반환하는 속성
    publishedBooksMessage() {
      // `this`는 컴포넌트 인스턴스를 가리킵니다.
      return this.author.books.length > 0 ? 'Yes' : 'No'
    }
  }
}
</script>

<template>
    <p>책을 가지고 있다.</p>
    <span>{{ publishedBooksMessage }}</span>
</template>