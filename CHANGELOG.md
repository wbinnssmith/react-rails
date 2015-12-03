# react-rails

#### Breaking Changes

#### New Features

#### Deprecation

#### Bug Fixes

## 1.5.0 (November 25, 2015)

#### Breaking Changes

#### New Features

- Update to React 0.14.3 #412
- `config.react.camelize_props = true` will camelize `react_component` prop keys #409

#### Deprecation

#### Bug Fixes

- Fix chained `.es6` file names with JSX processor #411
- Don't insert `// =require`s multiple times #398

## 1.4.2 (November 5, 2015)

#### Breaking Changes

#### New Features

- Component generator `--coffee` option #387
- Support Sprockets 4 with a JSX processor #385

#### Deprecation

#### Bug Fixes

- Support custom attributes when rendering from controller #384

## 1.4.1 (October 23, 2015)

#### Breaking Changes

#### New Features

#### Deprecation

#### Bug Fixes

- Minify & optimize the production build of React.js #380

## 1.4.0 (October 22, 2015)

#### Breaking Changes

#### New Features

- Include React.js 0.14

#### Deprecation

#### Bug Fixes

## 1.3.3 (October 21, 2015)

#### Breaking Changes

#### New Features

#### Deprecation

#### Bug Fixes

- Also support React 0.14 in `unmountComponents` #372
- Use a fallback view helper in case a Rails controller wasn't used #375

## 1.3.2 (October 13, 2015)

#### Breaking Changes

#### New Features

- The UJS can mount and unmount components within a given DOM node #358
- Support dropped-in React 0.14 in UJS #366

#### Deprecation

#### Bug Fixes

## 1.3.1 (September 18, 2015)

#### Breaking Changes

#### New Features

#### Deprecation

#### Bug Fixes

- Use controller lifecycle hooks for view helper (tests don't run middlewares) #356

## 1.3.0 (September 15, 2015)

#### Breaking Changes

#### New Features

- Render components directly from the controller with `render component: ...` #329
- Provide a custom view helper with `config.react.view_helper_implementation` #346

#### Deprecation

#### Bug Fixes

- Allow `react-rails` configs to be set in initializers #347

## 1.2.0 (August 19, 2015)

#### Breaking Changes

#### New Features

- Support `--es6` option in component generator #332
- Support Sprockets 3 #322

#### Deprecation

#### Bug Fixes

- Don't bother unmounting components `onBeforeUnload` #318
- Include `React::Rails::VERSION` in the gem #335

## 1.1.0 (July 9, 2015)

#### Breaking Changes

- Changed server rendering configuration names #253

  |  Old | New  |
  | ---- | ---- |
  | `config.react.timeout` | `config.react.server_renderer_timeout` |
  | `config.react.max_renderers` | `config.react.server_renderer_pool_size` |
  | `config.react.react_js` | `config.react.server_renderer_options[:files]` |
  | `config.react.component_filenames` | `config.react.server_renderer_options[:files]` |
  | `config.react.replay_console` | `config.react.server_renderer_options[:replay_console]` |
  | (none) | `config.react.server_renderer` |

- JSX is transformed by Babel, not JSTransform #295

#### New Features

- Allow custom renderers for server rendering #253
- Server render with `renderToStaticMarkup` via `prerender: :static` #253
- Accept `config.react.jsx_transform_options = {asset_path: "path/to/JSXTransformer.js"}` #273
- Added `BabelTransformer` for transforming JSX #295
- Added `ExecJSRenderer` to server rendering tools
- Accept `config.react.jsx_transformer_class` #302

#### Deprecations

- `JSXTransformer` won't be updated

#### Bug Fixes

- Fix gem versions in tests #270
- Expire the Sprockets cache if you change React.js builds #257
- Instead of copying builds into local directires, add different React.js builds to the asset pipeline #254
- Camelize attribute names in the component generator #262
- Add `tilt` dependency #248
- Default prerender pool size to 1 #302


## 1.0.0 (April 7, 2015)

#### New Features

- Vendor versions of React.js with `config.variant`, `config.addons` and `//= require react`
- Component generator
- View helper and UJS for mounting components
- Server rendering with `prerender: true`
- Transform `.jsx` in the asset pipeline
