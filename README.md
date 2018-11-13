# Kiwi Irc as a vue component -

This module is to be used in Vuejs projects, and imports the Kiwi Irc app as a component.


First you will need a working Vuejs project. See [here](https://github.com/vuejs-templates/webpack) for help.

### Usage:
using npm:

    npm i kiwi-vue-component

using yarn:

    yarn add kiwi-vue-component

Then, in your Vuejs project...

    import KiwiIrc from 'kiwi-vue-component'
    import 'kiwi-vue-component/style.css'

You will need to provide a Kiwi config object, as shown in the example below:

    <template>
        <div id="myapp">
            <KiwiIrc :kiwi-config="kiwiConfig"></KiwiIrc>
        </div>
    </template>

    <script>
    import KiwiIrc from 'kiwi-vue-component'
    import 'kiwi-vue-component/style.css'

    export default {
      components: {
        KiwiIrc
      },
      data () {
        return {
          kiwiConfig: {
            'windowTitle': 'Kiwi IRC - The web IRC client',
            'startupScreen': 'welcome',
            'kiwiServer': 'https://localdev.clients.kiwiirc.com/webirc/kiwiirc/',
            'restricted': false,
            'theme': 'Nightswatch',
            'themes': [
              { 'name': 'Default', 'url': 'static/themes/default' },
              { 'name': 'Dark', 'url': 'static/themes/dark' },
              { 'name': 'Coffee', 'url': 'static/themes/coffee' },
              { 'name': 'GrayFox', 'url': 'static/themes/grayfox' },
              { 'name': 'Nightswatch', 'url': 'static/themes/nightswatch' },
              { 'name': 'Osprey', 'url': 'static/themes/osprey' },
              { 'name': 'Radioactive', 'url': 'static/themes/radioactive' },
              { 'name': 'Sky', 'url': 'static/themes/sky' }
            ],
            'startupOptions': {
              'server': 'irc.freenode.net',
              'port': 6667,
              'tls': false,
              'direct': false,
              'channel': '#kiwiirc-default',
              'nick': 'kiwi-n?'
            },
            'embedly': {
              'key': ''
            },
            'plugins': [
            ]
          }
        }
      }
    }
    </script>

    <style>
    #myapp {
        margin-left: auto;
        margin-right: auto;
        margin-top: 12.5vh;
        height: 75vh;
        width: 75%;
        border: 1px solid black;
    }
    </style>

