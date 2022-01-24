<template>
  <v-app>
    <v-card
      id="memo"
      rounded="xl"
      class="mx-4 my-2 "
    >
      <v-card-title
        id="memo-title"
        style="font-size: 32px;"
        class="overflow-x-hidden text-no-wrap text-truncate"
      >
        {{ memo.title }}
      </v-card-title>
      <v-card-text
        id="memo-text"
        style="font-size: 16px;"
      >
        {{ memo.text }}
      </v-card-text>
      <div id="btn-group">
        <v-btn
          large
          icon
        >
          <v-icon>mdi-pencil</v-icon>
        </v-btn>
        <v-btn
          large
          icon
        >
          <v-icon>mdi-delete</v-icon>
        </v-btn>
      </div>
    </v-card>
  </v-app>
</template>
<script>
export default {
  props: {
    memo: {
      type: Object,
      default: null
    }
  }
}
</script>
<style lang="scss">
.v-application--wrap{
  min-height: 0;
}
#memo {
  position: relative;
  background-color: aquamarine;
}
#memo-title {
  display: block;
  padding-right: 0;
}
#btn-group {
  text-align: right;
  margin: 4px 16px 8px 16px;
}
#memo-text {
  padding: 0 16px;
  overflow: hidden;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 6;
}
</style>