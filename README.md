React+Browserify+Mocha Rig
==========================

A project template demonstrating an isomorphic UI testing workflow using `browserify`, `mochify`, and `react`.

Project Layout
--------------

The `app` is kept inside `node_modules` to allow for root-namespacing of application code. Each `react` component includes a
`spec` and `fixture` suite that sits alongside the component definition.  The example `renderSpec` uses the `fixture/index.js` definition to automatically verify that the fixture props+state properly renders the correct component HTML output. Tests can run 
in phantomjs, node, and any Saucelabs supported browser thanks to mochify's selenium webdriver support.

Naming Rules
------------

- All tests must match `*Spec.js`
- All components should export an `id`. Example: `module.exports.id = 'ComponentName'`

Available Commands
------------------

- `npm run test-dev`: Run your test suite with `watchify` enabled.  Tests will be rerun whenever a change is made to a test or test dependency.

- `npm run test`: Run the full test suite in node, phantom and wd.

- `npm run dev`: Run your app with `watchify`.

- `npm run build`: Build app for deploy.


