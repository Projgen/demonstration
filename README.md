# demonstration

Contains a step by step guide for demonstration and mass testing purposes

## installations

### remote template execution

```bash
mkdir projgen-test
cd projgen-test
npx @projgen/cli create https://raw.githubusercontent.com/Projgen/demonstration/refs/heads/main/demo-template.json -y
```

- press 'y' and `ENTER`
- press `ENTER` to select `npm`

After [confirming](#checks) everything is correct, you can delete the `projgen-test` folder again

### local template execution

```bash
mkdir projgen-test
cd projgen-test
npx @projgen/cli add https://raw.githubusercontent.com/Projgen/demonstration/refs/heads/main/demo-template.json
```

- press 'y' and `ENTER`

```bash
npx @projgen/cli cr demo-template -y
```

- press `ENTER` to select `npm`

After [confirming](#checks) everything is correct, you can delete the `projgen-test` folder again

## Checks

- Check for:
  - Folder ./{{project-name}} was created and contains the regular vite react boilerplate code
  - `package.json` contains `@tailwindcss/vite` in `dependencies`
  - `vite.config.ts` has an import from `@tailwindcss/vite` and lists `tailwindcss()` in plugins
  - `src/index.css` contains only `@import 'tailwindcss';`
  - `package.json` has `version` set to `1.0.0`
