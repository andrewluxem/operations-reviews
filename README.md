# operations-reviews

Builds a recurring operations review packet with measures, exceptions, controls, and actions.

It produces:

- **Operations Review Packet:** a working artifact built from supplied facts, labeled inference, and visible missing fields.

It executes the [Operations Reviews playbook](https://www.andrewluxem.com/playbooks/operations-reviews). The playbook teaches the framework. This skill runs it and returns a working artifact.

**Static by construction: no dependencies, executable code, telemetry, network calls, remote instructions, auto-update, scheduled work, or background behavior.** It reads only the files in its own skill folder. Nothing happens until a user or agent invokes it.

## Install

Clone and copy the skill into Claude Code:

```bash
git clone https://github.com/andrewluxem/operations-reviews.git
cp -r operations-reviews/skills/operations-reviews ~/.claude/skills/
```

For Codex, copy the same complete folder to the Codex skills directory:

```bash
cp -r operations-reviews/skills/operations-reviews ~/.codex/skills/
```

Or install it as a Claude Code plugin:

```text
/plugin marketplace add andrewluxem/operations-reviews
/plugin install operations-reviews@operations-reviews
```

For clients that install from an archive, use the versioned [operations-reviews v1.0.0 ZIP](https://www.andrewluxem.com/downloads/operations-reviews-v1.0.0.zip).

## Invoke it

```text
Build the operations review packet from these measures and exceptions
Use the operations-reviews skill.
```

Naming the skill is always valid: `use the operations-reviews skill`.

## Files

```text
.claude-plugin/
  plugin.json
  marketplace.json
skills/operations-reviews/
  assets/operations-review-packet-template.md
  LICENSE.md
  meta.yaml
  references/operations-review-standard.md
  SKILL.md
README.md
LICENSE
```

The complete canonical package is copied under `skills/operations-reviews/`, including every asset, reference, test prompt, source note, changelog entry, and license file present in the source.

## Versioning

Plugin installation is version-pinned. When behavior changes, update the version consistently in `SKILL.md`, `meta.yaml`, `.claude-plugin/plugin.json`, and `.claude-plugin/marketplace.json`, then add a changelog entry. Reinstalling is an explicit update; this repository never auto-updates itself.

## License

MIT. See [LICENSE](LICENSE). The canonical skill folder carries the same authorization in [skills/operations-reviews/LICENSE.md](skills/operations-reviews/LICENSE.md).
