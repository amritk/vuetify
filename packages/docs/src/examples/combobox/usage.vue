<template>
  <v-container fluid>
    <v-layout wrap>
      <v-flex xs12>
        <v-combobox
          v-model="select"
          :items="items"
          label="Select a favorite activity or create a new one"
        ></v-combobox>
      </v-flex>
      <v-flex xs12>
        <v-combobox
          v-model="select"
          :items="items"
          chips
          label="I use chips"
        ></v-combobox>
      </v-flex>
      <v-flex xs12>
        <v-combobox
          v-model="select"
          :items="items"
          chips
          label="I use a scoped slot"
        >
          <template v-slot:selection="data">
            <v-chip
              :key="JSON.stringify(data.item)"
              v-bind="data.attrs"
              :input-value="data.selected"
              :disabled="data.disabled"
              @click.stop="data.parent.selectedIndex = data.index"
              @click:close="data.parent.selectItem(data.item)"
            >
              <v-avatar class="accent white--text" left>
                {{ data.item.slice(0, 1).toUpperCase() }}
              </v-avatar>
              {{ data.item }}
            </v-chip>
          </template>
        </v-combobox>
      </v-flex>
      <v-flex xs12>
        <v-combobox
          v-model="select"
          chips
          label="I'm readonly"
          readonly
        ></v-combobox>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        select: 'Programming',
        items: [
          'Programming',
          'Design',
          'Vue',
          'Vuetify',
        ],
      }
    },
  }
</script>
