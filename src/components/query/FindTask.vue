<template>
  <Form :model="formItem" :label-width="80">
    <FormItem label="地名">
      <Input v-model="formItem.input" placeholder="请输入查询名称" />
    </FormItem>
    <FormItem>
      <Button type="primary" @click="query">查询</Button>
    </FormItem>
  </Form>
</template>

<script>
export default {
  name: 'findtask',
  data () {
    return {
      formItem: {
        input: ''
      }
    }
  },
  methods: {
    query () {
      this.$emit('click', this.formItem.input)
    }
  }

}
</script>

<style scoped>

</style>
