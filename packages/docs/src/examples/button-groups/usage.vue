<template>
  <v-card flat class="py-12">
    <v-card-text>
      <v-container fluid class="pa-0">
        <v-layout wrap>
          <v-flex xs12 sm6 class="py-2">
            <p>Exclusive</p>
            <v-btn-toggle v-model="toggle_exclusive">
              <v-btn text>
                <v-icon>format_align_left</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_align_center</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_align_right</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_align_justify</v-icon>
              </v-btn>
            </v-btn-toggle>
          </v-flex>
          <v-flex xs12 sm6 class="py-2">
            <p>Multiple</p>
            <v-btn-toggle v-model="toggle_multiple" multiple>
              <v-btn text>
                <v-icon>format_bold</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_italic</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_underlined</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_color_fill</v-icon>
              </v-btn>
            </v-btn-toggle>
          </v-flex>
          <v-flex xs12 sm6 class="py-2">
            <p>No Options Selected</p>
            <v-btn-toggle v-model="toggle_none">
              <v-btn text>
                <v-icon>format_align_left</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_align_center</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_align_right</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_align_justify</v-icon>
              </v-btn>
            </v-btn-toggle>
          </v-flex>
          <v-flex xs12 sm6 class="py-2">
            <p>Mandatory</p>
            <v-btn-toggle v-model="toggle_one" mandatory>
              <v-btn text>
                <v-icon>format_align_left</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_align_center</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_align_right</v-icon>
              </v-btn>
              <v-btn text>
                <v-icon>format_align_justify</v-icon>
              </v-btn>
            </v-btn-toggle>
          </v-flex>
          <v-flex xs12 sm6 class="py-2">
            <p>Text Options</p>
            <v-btn-toggle v-model="text">
              <v-btn text value="left">
                Left
              </v-btn>
              <v-btn text value="center">
                Center
              </v-btn>
              <v-btn text value="right">
                Right
              </v-btn>
              <v-btn text value="justify">
                Justify
              </v-btn>
            </v-btn-toggle>
          </v-flex>
          <v-flex xs12 sm6 class="py-2">
            <p>Text &amp; Icon Options</p>
            <v-btn-toggle v-model="icon">
              <v-btn text value="left">
                <span class="hidden-sm-and-down">Left</span>
                <v-icon>format_align_left</v-icon>
              </v-btn>
              <v-btn text value="center">
                <span class="hidden-sm-and-down">Center</span>
                <v-icon>format_align_center</v-icon>
              </v-btn>
              <v-btn text value="right">
                <span class="hidden-sm-and-down">Right</span>
                <v-icon>format_align_right</v-icon>
              </v-btn>
              <v-btn text value="justify">
                <span class="hidden-sm-and-down">Justify</span>
                <v-icon>format_align_justify</v-icon>
              </v-btn>
            </v-btn-toggle>
          </v-flex>
        </v-layout>
      </v-container>
    </v-card-text>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        text: 'center',
        icon: 'justify',
        toggle_none: null,
        toggle_one: 0,
        toggle_exclusive: 2,
        toggle_multiple: [0, 1, 2],
      }
    },
  }

</script>
