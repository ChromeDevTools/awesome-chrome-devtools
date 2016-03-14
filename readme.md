# Awesome chrome-devtools [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

> Awesome tooling and resources in the Chrome DevTools ecosystem

## Learning
* [Dev Tips](https://umaar.com/dev-tips/) - Large collection of tips as animated gifs.

### DevTools as an IDE
* [Chrome DevTools App](https://github.com/auchenberg/chrome-devtools-app) - Standalone devtools app which can inspect various targets.
* [DevTools Remote](https://devtoolsremote.com/) - Remotely debug someone else's browser via Chrome DevTools.
* [DevTools Snippets](https://github.com/bahmutov/code-snippets) - Collection of DevTools snippets.

### Node.js + DevTools
* [chrome-remote-interface](https://github.com/cyrus-and/chrome-remote-interface) - The recommended Node.js API for the protocol. There are also [TypeScript-friendly alternatives](https://github.com/DickvdBrink/chrome-debug-protocol).
* [chrome-devtools-frontend](https://www.npmjs.com/package/chrome-devtools-frontend) - Mirror of the frontend shipping in Chrome.
* [chrome-timeline-model](https://www.npmjs.com/package/devtools-timeline-model) - Uses frontend as lib to process profiling data.
* [crmux](https://github.com/sidorares/crmux) - Multiplexes protocol connections.
* [crconsole](https://github.com/sidorares/crconsole) - Terminal based chrome console and debugger.
* [buggerJS](https://github.com/buggerjs/bugger) - Provides Chrome DevTools bindings for node.

### Chrome Debugging Protocol
* [Debugging Protocol Viewer](https://chromedevtools.github.io/debugger-protocol-viewer/) - Easy browsable UI for exploring the protocol's domains, methods and events
* [Remote Debug Gateway](https://github.com/RemoteDebug/remotedebug-gateway) - Allows you to connect a client to multiple browsers at once.
* [Remote Debug Firefox adapter](https://github.com/RemoteDebug/remotedebug-firefox-adapter) - Translates Firefox's devtools protocol to the CDP
* [ios-webkit-debug-proxy](https://github.com/google/ios-webkit-debug-proxy) - Exposes Mobile Safari & UIWebView instances via the CDP.
* [IE Diagnostics Adapter](https://github.com/Microsoft/IEDiagnosticsAdapter) - Protocol adaptor for Microsoft IE 10/11 to CDP.
* [devtools-compat-proxy](https://github.com/artygus/devtools-compat-proxy) - Young effort to translate modern Safari debugging protocol to modern CDP.
* [crmux](https://github.com/sidorares/crmux) - Multiplexer to handle multiple clients.
* [PonyDebugger](https://github.com/square/PonyDebugger) - Remote network and data debugging iOS apps with Chrome DevTools
* [Facebook Stetho](https://github.com/facebook/stetho) - Native Android debugging with Chrome DevTools

### Network Inspection
* [betwixt](https://github.com/kdzwinel/betwixt) - System level network proxy, providing inspection via Network panel

### CPU profile
* [JSCLegacyProfiler/json2trace](https://github.com/facebook/react-native/blob/master/JSCLegacyProfiler/json2trace) - Converts Safari's JavaScriptCore profiler output into `.cpuprofile`
* [call-trace](https://github.com/brendankenny/call-trace) - Can instrument your JS with hooks, and then generate a `.cpuprofile`  of the of the complete (non-sampled) execution. View either time or call counts.
* [cpuprofilify](https://github.com/thlorenz/cpuprofilify) - Converts output of various profiling/sampling tools to the `.cpuprofile` format.
* [Wishbone python framework](http://wishbone.readthedocs.org/en/develop/miscellaneous.html#profiling) - Profiling data can export as `.cpuprofile`.

### Chrome Debugger integration with Editors
* [Showcase Protocol Clients](https://developer.chrome.com/devtools/docs/debugging-clients) - Lists many, like Brackets, Vim, LightTable, Sublime, etc.
* [VS Code - Debugger for Chrome](https://github.com/Microsoft/vscode-chrome-debug/) - Chrome Debugger for Visual Studio Code

## Extensions
### Workflow
* [Clockwork](https://chrome.google.com/webstore/detail/clockwork/dmggabnehkmmfmdffgajcflpdjlnoemp?hl=en)  View PHP application profiling data.
* [Emulated Device Lab](https://chrome.google.com/webstore/detail/emulated-device-lab/oaonfodocibcdobdeelbbfggjombamff) - Experiment with multiple devices being emulated at the same time.
* [RailsPanel](https://chrome.google.com/webstore/detail/railspanel/gjpfobpafnhjhbajcjgccbbdofdckggg?hl=en-US) - View Ruby on Rails application profiling data.
* [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi) - Inspect the React component hierarchies.
* [EmberJS Inspector](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi) - Allows you to inspect EmberJS objects in your application.
* [VueJS Developer Tools](https://github.com/vuejs/vue-devtools) - Chrome devtools extension for debugging Vue.js applications
* [Angular Batarang](https://chrome.google.com/webstore/detail/angularjs-batarang/ighdmehidhipcmcojjgiloacoafjmpfk) - Inspect an Angular application's scope and profile its data.
* [Marionette Inspector](https://chrome.google.com/webstore/detail/marionette-inspector/fbgfjlockdhidoaempmjcddibjklhpka) - Inspect a Marionette application's views, events or live data.
* [Backbone Debugger](https://chrome.google.com/webstore/detail/backbone-debugger/bhljhndlimiafopmmhjlgfpnnchjjbhd) - Inspect a Backbone application's views, models, events and routes.
* [App Inspector for Sencha](https://chrome.google.com/webstore/detail/app-inspector-for-sencha/pbeapidedgdpniokbedbfbaacglkceae) - Inspect a Sencha ExtJS/Touch application's component tree, data stores, events, and layouts.
* [Redux Devtools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd) - DevTools for Redux with actions history, undo and replay.
* [Three.js](https://chrome.google.com/webstore/detail/threejs-editor-extension/fbgbekpggeldiacgjkacbkkcbjhmakea/) - A Chrome DevTools extension to edit any three.js project.

### UX
* [DevTools Author](https://chrome.google.com/webstore/detail/devtools-author/egfhcfdfnajldliefpdoaojgahefjhhi) - A selection of author settings for Chrome Developer Tools.
* [Zero Dark Matrix](https://chrome.google.com/webstore/detail/devtools-theme-zero-dark/bomhdjeadceaggdgfoefmpeafkjhegbo) - Dark theme for Chrome Developer Tools.
