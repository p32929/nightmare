# nightmare

A copy of [Nightmare](https://www.npmjs.com/package/nightmare) 3.0.2, the high-level browser automation library by Segment, with only one change: it uses **Electron 6.1.12** instead of the older Electron the original ships with. I made it in 2021 so old Nightmare scripts could run on a newer Electron.

All the code is Segment's. If you are starting something new, a maintained tool such as Playwright or Puppeteer is a better choice. Use this only to keep an old Nightmare script running.

## What changed

1. `package.json`: `electron` moved from `^3.1.12` to `^6.1.12`.
2. Nothing else. The library code in `lib/` is the original Nightmare 3.0.2.

## Use it

Install it straight from this repository:

```bash
npm install p32929/nightmare
```

Then use it like normal Nightmare:

```js
const Nightmare = require('nightmare')
const nightmare = Nightmare({ show: true })

nightmare
  .goto('https://duckduckgo.com')
  .type('#search_form_input_homepage', 'github nightmare')
  .click('#search_button_homepage')
  .wait('#r1-0 a.result__a')
  .evaluate(() => document.querySelector('#r1-0 a.result__a').href)
  .end()
  .then(console.log)
  .catch(console.error)
```

For the full list of actions, see the [original Nightmare documentation on npm](https://www.npmjs.com/package/nightmare).

## License

MIT, as in the original Nightmare by Segment. The version history is in [History.md](History.md).

## Contributing

Contributions are very welcome, thank you! Before you start on a pull request, please open an issue and tell me what you would like to add or change. That way we can agree on it first, and your time is not spent on something that might not fit.

## You might also like

<p><a href="https://openstore.pfay.workers.dev/more/p32929/nightmare/0"><picture><source media="(prefers-color-scheme: dark)" srcset="https://openstore.pfay.workers.dev/more/p32929/nightmare/0-dark.svg"><img src="https://openstore.pfay.workers.dev/more/p32929/nightmare/0-light.svg" width="50%" align="top" alt="More apps by p32929 on OpenStore (1)"></picture></a><a href="https://openstore.pfay.workers.dev/more/p32929/nightmare/1"><picture><source media="(prefers-color-scheme: dark)" srcset="https://openstore.pfay.workers.dev/more/p32929/nightmare/1-dark.svg"><img src="https://openstore.pfay.workers.dev/more/p32929/nightmare/1-light.svg" width="50%" align="top" alt="More apps by p32929 on OpenStore (2)"></picture></a><br><a href="https://openstore.pfay.workers.dev/more/p32929/nightmare/2"><picture><source media="(prefers-color-scheme: dark)" srcset="https://openstore.pfay.workers.dev/more/p32929/nightmare/2-dark.svg"><img src="https://openstore.pfay.workers.dev/more/p32929/nightmare/2-light.svg" width="50%" align="top" alt="More apps by p32929 on OpenStore (3)"></picture></a><a href="https://openstore.pfay.workers.dev/more/p32929/nightmare/3"><picture><source media="(prefers-color-scheme: dark)" srcset="https://openstore.pfay.workers.dev/more/p32929/nightmare/3-dark.svg"><img src="https://openstore.pfay.workers.dev/more/p32929/nightmare/3-light.svg" width="50%" align="top" alt="More apps by p32929 on OpenStore (4)"></picture></a></p>

<p><a href="https://p32929.github.io/share/?repo=nightmare"><picture><source media="(prefers-color-scheme: dark)" srcset="https://p32929.github.io/readme/footer-share-dark.svg"><img src="https://p32929.github.io/readme/footer-share-light.svg" width="50%" align="top" alt="Share this project with your friends in one click"></picture></a><a href="https://p32929.github.io/support/"><picture><source media="(prefers-color-scheme: dark)" srcset="https://p32929.github.io/readme/footer-support-dark.svg"><img src="https://p32929.github.io/readme/footer-support-light.svg" width="50%" align="top" alt="If you like my work and want to support me, feel free to support"></picture></a><br><a href="https://openstore.pfay.workers.dev/add"><picture><source media="(prefers-color-scheme: dark)" srcset="https://p32929.github.io/readme/footer-join-dark.svg"><img src="https://p32929.github.io/readme/footer-join-light.svg" width="100%" align="top" alt="Put your own apps on OpenStore: free, your listing lives in your own repo"></picture></a></p>
