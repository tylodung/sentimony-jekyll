<template>
  <div class="events">
    <h1>Events</h1>
    <div class="events__list">
      <p v-for="i in events.data" class="events__item">
        <a :href="i.url" class="events__link" v-if="i.date" v-html="i.date + ' @ ' + i.title"></a>
      </p>
    </div>
  </div>
</template>

<script>
  module.exports = {
    data: function () {
      return {
        events: {
          data: [
            {
              title: '',
              date: '',
              url: ''
            }
          ]
        }
      }
    },
    created: function () {
      var self = this;
      this.axios.get('/assets/data/events.json').then(function (response) {
        self.events = response.data.events;
      }).catch(function (error) {
        console.log(error);
      });
    }
  };
</script>

<style lang="scss?outputStyle=compressed">
  .events {
  }
</style>
