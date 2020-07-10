<template>
  <div>
    <b-tabs v-model="activeTab">
      <b-tab-item label="General">
        <General />
      </b-tab-item>
      <b-tab-item label="Metadata">
        <Metadata />
      </b-tab-item>
    </b-tabs>
  </div>
</template>
<script lang="ts" >
import { Component, Prop, Vue, Watch } from 'vue-property-decorator';
import General from '@/components/settings/General.vue';
import Metadata from '@/components/metadata/Metadata.vue';

@Component({
  components: {
    General,
    Metadata
  },
})
export default class Settings extends Vue {
  private activeTab: number = 0;

  // @Watch('$route.params.tab')
  // private async reflect() {
  //   if (typeof this.$route.params.tab === 'number') {
  //     this.activeTab = Number(this.$route.params.tab);
  //   }
  // }

  // private async tabClick(): Promise<void> {
  //   this.$router.replace(`/accounts/${this.activeTab}`)
  // }

  // private async mounted(): Promise<void> {
  //   this.reflect()
  // }
}
</script>

