<p align="center">
  <img alt="cmless" src="https://raw.githubusercontent.com/cmless/cmless/master/logo.png" />
</p>

<p align="center">
  A seamless build tool for dazzling front end projects
</p>

<hr />

# Installation
## Local
To install the package as a development dependency of your project:
```
npm install cmless -D
```

Then modify your `package.json` file:
```json
{
  "scripts": {
    "start": "cmless start",
    "build": "cmless build"
  },
  "cmless": {
  }
}
```

You can then execute `npm start` or `npm run build` in the command line.

## Global
Alternatively, install the package globally:
```
npm install cmless -g
```

Then run the commands from any compatible project.

# Commands
### `cmless start`
Start a new development server

### `cmless build`
Build your application for production.

# Options
Modify the `cmless` object in your project's `package.json` to change build options. For the default configuration, see this project's [`package.json`](./package.json).

- `browserslist` - a list of target browsers to autoprefix CSS for. See [Browserslist](https://github.com/browserslist/browserslist) documentation
- `cmless`
  - `port` - the port on which to run the development server
  - `input` - the main input folder
  - `template` - the main HTML template file
  - `script` - the main JavaScript / TypeScript file
  - `style` - a JavaScript / TypeScript file exporting variables that can be used in CSS, HTML, and JavaScript
  - `pwa` - see available options in the [webpack PWA manifest](https://github.com/arthurbergmz/webpack-pwa-manifest#webpackpwamanifestoptions) documentation
  - `env` - environment variables, for example the `NODE_ENV` variable can be used with `process.env.NODE_ENV`
  - `assets` - a list of file extensions supported by the file loader
  - `output` - the folder output files will be saved to after building for production
  - `clean` - a list of folders to clean before each production build
  - `serviceWorker` - see available options in the [Workbox webpack plugin](https://developers.google.com/web/tools/workbox/modules/workbox-webpack-plugin) documentation
