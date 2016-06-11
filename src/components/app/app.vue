<script>
  import template from './template.html';
  import Subscription from 'components/subscription/subscription.vue';

  export default {
    template,
    components: {
      Subscription,
    },
    data() {
      return {
        newSearchTerm: '',
        channels: [],
      };
    },
    methods: {
      newSubscription() {
        this.channels.push({
          term: this.newSearchTerm,
          active: true,
        });
        this.newSearchTerm = '';
      },
      toggleSearch(toggledChannel) {
        for (const channel of this.channels) {
          if (toggledChannel.term === channel.term) {
            channel.active = !channel.active;
            // break;
          }
        }
      },
    },
  };
</script>
