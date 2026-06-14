# wiki-quartz-template

Publish a [Wiki CLI](https://github.com/wazootech/wiki)-compatible vault with [Quartz](https://quartz.jzhao.xyz/). Edit in Obsidian or any editor; validate with `wiki check`; publish with Quartz.

Registry: [Wiki CLI templates](https://github.com/wazootech/wiki/blob/main/docs/wiki/Wiki_CLI.md#ecosystem-templates).

## Quick start

```bash
pip install wazootech-wiki
wiki check --strict
npm install
npx quartz build --serve
```

## Layout

| Path | Role |
| ---- | ---- |
| `content/` | Markdown vault (Quartz content root) |
| `wiki.yaml` | Wiki CLI config (`wiki.inputs: [content]`) |
| `quartz.config.ts` | Quartz site configuration |

## CI

GitHub Actions runs `wiki check --strict` and `wiki lint --strict` on every push. Wire Quartz build/deploy in your fork (see [Quartz hosting](https://quartz.jzhao.xyz/hosting/)).

## Obsidian

Point your vault at `content/` or symlink it. Keep Wikipedia-style filenames; use Markdown links when `link.style` is `markdown`.

## Related

- [#16](https://github.com/wazootech/wiki/issues/16)
- [Obsidian integration](https://github.com/wazootech/wiki/blob/main/docs/wiki/Obsidian_Integration.md)
