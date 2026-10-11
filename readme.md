# Awesome Chrome DevTools [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Awesome tooling and resources in the Chrome DevTools ecosystem

Tools, protocol drivers, trace viewers, and standalone frontends built around Chrome DevTools and the Chrome DevTools Protocol (CDP). Following the [Awesome Manifesto](https://github.com/sindresorhus/awesome/blob/main/awesome.md), we keep this list focused on what's genuinely useful rather than indexing everything in the space.

## Contents

- [Learning](#learning)
- [Tracing & Profiling](#tracing--profiling)
- [Chrome DevTools Protocol](#chrome-devtools-protocol)
- [Using DevTools frontend with other platforms](#using-devtools-frontend-with-other-platforms)
- [DevTools Extensions](#devtools-extensions)
- [Alumni](#alumni)

---

## Learning
- [Dev Tips](https://umaar.com/dev-tips/) - Large collection of tips as animated gifs.
- [DevTools Tips](https://devtoolstips.org/) - Collection of illustrated tips as mini tutorials.
- [Web cheatcodes](https://codepo8.github.io/web-cheatcodes/) - Browser developer tools for non-developers.
- [Dear Console](https://codepo8.github.io/dearconsole) - A collection of snippets to use in the browser console.
- [Chrome Secret Menus](https://github.com/sparkyrider/chrome-secret-menus) - Guide to Chrome's internal `chrome://` pages and diagnostic tools.
- [Front-end Debugging Tools Handbook](https://github.com/lala-hakobyan/front-end-debugging-handbook) - Practical guide to front-end debugging across DevTools, framework extensions, and IDEs.

---

## Tracing & Profiling

DevTools Performance traces and V8 `.cpuprofile` logs are plain JSON under the hood, and a few standalone viewers do great things with them:

- [trace.cafe](https://trace.cafe/) - Share and view web performance traces directly in the DevTools Performance panel ([source](https://github.com/paulirish/trace.cafe)).
- [speedscope](https://github.com/jlfwong/speedscope) - Fast, interactive flamegraph viewer that imports Chrome `.cpuprofile` and timeline traces.
- [cpupro](https://github.com/discoveryjs/cpupro) - Deep V8/Chrome `.cpuprofile` analyzer with flamegraphs, call trees, and hot-spot diagnostics.
- [Perfetto](https://github.com/google/perfetto) - System profiling and trace analysis suite ([ui.perfetto.dev](https://ui.perfetto.dev/)) with Chromium trace support and SQL trace querying.

---

## Chrome DevTools Protocol

Pro-tip: flip on Chrome's built-in [Protocol Monitor](https://developer.chrome.com/docs/devtools/protocol-monitor) (`More tools > Protocol monitor`) to watch live CDP traffic and fire off raw commands right in the browser.

- [ChromeDevTools/devtools-protocol](https://github.com/chromedevtools/devtools-protocol) - **Canonical location of the protocol JSON**, TypeScript types, and issue tracker for protocol bugs.
- [DevTools Protocol API Docs](https://chromedevtools.github.io/devtools-protocol/) - Browsable UI for exploring the protocol's domains, methods, and events.

### Developing with the protocol
- [chrome-remote-interface Wiki](https://github.com/cyrus-and/chrome-remote-interface/wiki) - Handy recipes for common raw-CDP tasks.
- [Chrome Protocol Proxy](https://github.com/wendigo/chrome-protocol-proxy) - Proxy for inspecting and debugging CDP client traffic.

### The big two automation libraries
- [Puppeteer](https://github.com/puppeteer/puppeteer) - High-level Node.js API for controlling Chrome over CDP and WebDriver BiDi. See also [awesome-puppeteer](https://github.com/transitive-bullshit/awesome-puppeteer).
- [Playwright](https://github.com/microsoft/playwright) - Cross-browser automation for Chromium, Firefox, and WebKit across Node.js, Python, .NET, and Java. See also [awesome-playwright](https://github.com/mxschmitt/awesome-playwright).

### Libraries for driving the protocol (or a layer above)

- JavaScript/Node.js: [chrome-remote-interface](https://github.com/cyrus-and/chrome-remote-interface) - Low-level CDP client
- Rust: [chromiumoxide](https://github.com/mattsse/chromiumoxide) - Async/tokio library with generated types
- Rust: [Rust Headless Chrome](https://github.com/rust-headless-chrome/rust-headless-chrome) - High-level headless Chrome client
- Java: [chrome-devtools-java-client](https://github.com/kklisura/chrome-devtools-java-client) - Low-level protocol client
- Java: [jvppeteer](https://github.com/fanyong920/jvppeteer) - Headless Chrome for Java
- Python: [Zendriver](https://github.com/cdpdriver/zendriver) - Async CDP browser automation
- Python: [PyCDP](https://github.com/hyperiongray/python-chrome-devtools-protocol) - Sans-IO wrappers (see also [Trio driver](https://github.com/hyperiongray/trio-chrome-devtools-protocol))
- Python: [ChromeController](https://github.com/fake-name/ChromeController) - High-level browser mgmt
- Go: [chromedp](https://github.com/chromedp/chromedp) - High-level actions and tasks
- Go: [Rod](https://github.com/go-rod/rod) - High-level automation and scraping
- Go: [cdp](https://github.com/mafredri/cdp) - Type-safe bindings for CDP
- C#/.NET: [Puppeteer Sharp](https://github.com/hardkoded/puppeteer-sharp) - Puppeteer port
- C#/.NET: [dotnet-chrome-protocol](https://github.com/seclerp/dotnet-chrome-protocol) - Runtime library and schema codegen
- Ruby: [Ferrum](https://github.com/rubycdp/ferrum) - High-level API to control Chrome
- Ruby: [Cuprite](https://github.com/rubycdp/cuprite) - Capybara driver
- Kotlin: [chrome-devtools-kotlin](https://github.com/joffrey-bion/chrome-devtools-kotlin) - Coroutine-based client library
- Kotlin: [kdriver](https://github.com/cdpdriver/kdriver) - High-level coroutine-based automation
- Clojure: [clj-chrome-devtools](https://github.com/tatut/clj-chrome-devtools) - Autogenerated CDP wrapper
- Clojure: [cuic](https://github.com/milankinen/cuic) - High-level UI test automation
- PHP: [chrome-devtools-protocol](https://github.com/jakubkulhan/chrome-devtools-protocol) - Client library

### Agentic Browser Automation

> We're *extremely* picky with this section. Everyone is wrapping a browser for agents right now—expect any PR adding another MCP server or agent CLI to be closed unless it has real traction and does something novel with CDP under the hood.

- [chrome-devtools-mcp](https://github.com/ChromeDevTools/chrome-devtools-mcp) - Official MCP server for Chrome DevTools, which also includes a [CLI](https://github.com/ChromeDevTools/chrome-devtools-mcp/blob/main/skills/chrome-devtools-cli/SKILL.md).
- [Webcmd](https://github.com/agentrhq/webcmd) - Compiles site navigation into deterministic per-site CLI commands for AI agents.
- [Lumen](https://github.com/omxyz/lumen) - Vision-first browser agent with self-healing deterministic replay over CDP.
- [bdg](https://github.com/szymdzum/browser-debugger-cli) - Persistent background CDP session exposing DOM, network, console, and raw protocol methods as shell commands.
- [jshookmcp](https://github.com/vmoranv/jshookmcp) - MCP workspace that hooks your real signed-in Chrome over CDP (not a scripted browser): live DOM/network interception, TLS keylog, and script injection as agent-callable tools, so the agent verifies end-state against real responses instead of a UI "success" label.


### Browser Adapters
- [devtools-remote-debugger](https://github.com/Nice-PLQ/devtools-remote-debugger) - Debug a webpage remotely via a CDP agent implemented in client-side JS.
- [Inspect](https://inspect.dev/) - Use DevTools against iOS and Android browsers and WebViews. **(closed source)**


## Using DevTools frontend with other platforms

The DevTools UI is a web app speaking CDP over a WebSocket, so you can embed it or point it at Node, Ruby, mobile webviews, or custom runtimes (see `chrome://inspect` for built-in targets).

- [ChromeDevTools/devtools-frontend](https://github.com/ChromeDevTools/devtools-frontend) - Canonical source repo for the Chrome DevTools UI (published to npm as [chrome-devtools-frontend](https://www.npmjs.com/package/chrome-devtools-frontend)).
- [Chii](https://github.com/liriliri/chii) & [Eruda](https://github.com/liriliri/eruda) - Remote debugging server using the real `devtools-frontend` UI (`Chii`, a modern Weinre replacement) and in-page mobile DevTools console (`Eruda`).
- [vscode-js-debug](https://github.com/microsoft/vscode-js-debug) - Official DAP-compliant JavaScript and Chrome CDP debugger powering VS Code.
- [VS Code - Elements for Microsoft Edge](https://github.com/microsoft/vscode-edge-devtools) - Elements and Network panels embedded inside VS Code.
- [Debugging Node.js with Chrome DevTools](https://medium.com/@paul_irish/debugging-node-js-nightlies-with-chrome-devtools-7c4a1b95ae27) - Guide on debugging and profiling Node.js with `node --inspect`.
- [ruby/debug](https://github.com/ruby/debug) - Ruby's official debugger, which supports connecting Chrome DevTools over CDP (`rdbg --open=chrome`).

---

## DevTools Extensions

- [React Developer Tools](https://chromewebstore.google.com/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi) - Inspect React component hierarchies, props, and profiler flamegraphs.
- [Vue.js Developer Tools](https://github.com/vuejs/devtools) - Inspect Vue.js components, state, and routing.
- [Angular DevTools](https://chromewebstore.google.com/detail/angular-devtools/ienfalfjdbdpebioblfackkekamfmbnh) - Component tree inspection and change-detection profiling for Angular.
- [Redux Devtools](https://chromewebstore.google.com/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd) - Time-travel debugging and action history for Redux.
- [Ember.js Inspector](https://chromewebstore.google.com/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi) - Inspect Ember.js objects, routes, and data.
- [Web Component DevTools](https://chromewebstore.google.com/detail/web-component-devtools/gdniinfdlmmmjpnhgnkmfpffipenjljo) - Inspect, modify, and observe custom elements and shadow DOM on the page.
- [Clockwork](https://chromewebstore.google.com/detail/clockwork/dmggabnehkmmfmdffgajcflpdjlnoemp?hl=en) - PHP application profiling and request inspection in DevTools.
- [RailsPanel](https://chromewebstore.google.com/detail/railspanel/gjpfobpafnhjhbajcjgccbbdofdckggg?hl=en-US) - Ruby on Rails request and SQL profiling panel.

## Alumni
Old projects, likely not maintained any longer… But still cool.

- [ndb](https://github.com/GoogleChromeLabs/ndb) - Improved Node.js debugging experience built on the DevTools frontend.
- [thetool](https://github.com/sfninja/thetool) - CPU, memory, coverage, and type profiling for Node.js.
- [Facebook Stetho](https://github.com/facebook/stetho) - Native Android debugging with Chrome DevTools.
- [PonyDebugger](https://github.com/square/PonyDebugger) - Remote network and Core Data debugging for iOS apps via Chrome DevTools.
- [betwixt](https://github.com/kdzwinel/betwixt) - System-level network proxy inspected through a standalone DevTools Network panel.
- [Dirac](https://github.com/binaryage/dirac) - ClojureScript debugging with a custom DevTools fork.
- [VS Code - Debugger for Chrome](https://github.com/Microsoft/vscode-chrome-debug/) - Original Chrome debugger for VS Code (superseded by built-in [vscode-js-debug](https://github.com/microsoft/vscode-js-debug), which has a rich CDP/DAP implementation).
- [noice-json-rpc](https://github.com/nojvek/noice-json-rpc) - Proxy-based TypeScript/JS library exposing CDP domains directly as an API.
- [PuPHPeteer](https://github.com/rialto-php/puphpeteer) - PHP bridge to Node Puppeteer.
- [Insight](https://github.com/3Dparallax/insight/) - WebGL debugging toolkit for Chrome DevTools.
- [Remote Debug Gateway](https://github.com/RemoteDebug/remotedebug-gateway) - Connect a debugging client to multiple browsers at once.
  - Multiuser DevTools: [DevTools Remote](https://github.com/auchenberg/devtools-remote) - Remotely debug someone else's browser.
- [DevTools Backend](https://github.com/christian-bromann/devtools-backend) - Standalone implementation of the Chrome DevTools backend to debug arbitrary web environments.
- Python CDP driver: [pychrome](https://github.com/fate0/pychrome) - Low-level CDP transport handler.
- [ios-webkit-debug-proxy](https://github.com/google/ios-webkit-debug-proxy) - Exposes Mobile Safari & UIWebView instances via CDP.
  - [Remote Debug iOS WebKit adapter](https://github.com/RemoteDebug/remotedebug-ios-webkit-adapter) - Builds on `ios-webkit-debug-proxy` and translates WebKit's Remote Debugging Protocol to CDP.
- [IE Diagnostics Adapter](https://github.com/Microsoft/IEDiagnosticsAdapter) - Protocol adapter translating IE 11 to CDP.

