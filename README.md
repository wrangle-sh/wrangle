# Wrangle

Static analysis tool with a powerful rule- and LLM-based engine for identifying technical debt. We operate **both** low-level (linting line-by-line) as well as high-level (architectural considerations).

## Prerequisites

Wrangle uses LLMs for a large portion of the "higher-level" analysis that we do. More providers are on the roadmap, but OpenAI is the only one for now.

> **Planned:** More providers.

## To Install

Installation is supported on all prominent package managers.

- npm: `npm i -D @wrangle/cli`
- yarn: `yarn i -D @wrangle/cli`
- pnpm: `pnpm i -D @wrangle/cli`

We recommend against a global installation, as that can make it difficult for other collaborators to run the tool.

## To Run

`wrangle run` is the main entrypoint. By default, anything LLM-powered is skipped, so no environment variables are necessary.

```shell
wrangle run
```

To include LLM-powered rules, supply `OPENAI_API_KEY` to the command and add the `--llm` flag.

```shell
OPENAI_API_KEY=<key> wrangle run --llm
```

> **Planned:** Wrangle will also be available at a shorter `wr` alias.

## Configuration

We use a `wrangle.json` file and a published JSON Schema.

> **Planned:** Support for `.js`, `.ts`, `.mjs`, `.mts`, `.cjs`, `.cts`, and as a `package.json` key.

## License

Wrangle is permissively licensed under the [Functional Source License](https://fsl.software/), following in the footsteps of [Sentry](https://open.sentry.io/licensing/). Code releases revert to the MIT License after two years.

A FSL license is all-permissive with the notable exclusion that you can't turn around, throw a thin UI around it, and sell it as a code inspection service. This permits almost all developer usage while protecting the creators of the tool from the [Free-rider Problem](https://en.wikipedia.org/wiki/Free-rider_problem).