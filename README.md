# Daniel Kindl

```csharp
public record Whoami
{
    public string[] Principles => new[]
    {
        "Test-Driven Development",
        "SOLID",
        "Clean Architecture",
        "Delivery Discipline"
    };

    // Implementation details. Swappable.
    public string[] Languages => new[] { "C#", ".NET", "TypeScript", "Astro", "Svelte", "Python" };

    public string Method => "I design the system. AI does a lot of the typing. I own the result.";
}
```

## What that looks like in practice

- **Test-Driven Development** — the test describes the behaviour before the
  implementation exists. A change not covered by a test isn't finished.
- **SOLID / Clean Architecture** — dependencies point inward. Domain logic
  doesn't reference a specific framework, database driver, or UI layer, so
  any of those can be replaced without touching the core.
- **Delivery discipline** — small commits, one concern each, CI green
  before merge. No batching unrelated changes into a PR that's already open.

## How I like to work

- **Design first.** Architecture and interfaces are settled before
  implementation exists — AI writes a lot of what follows, but not the
  shape it follows.
- **Tests as spec.** Behaviour not covered by a test isn't done, it's a
  guess.
- **Patterns over frameworks.** Reusing a shape — a repository, a pipeline,
  a strategy — survives a framework swap; framework-specific code doesn't.

## Currently

[TangoByteLens](https://github.com/daniel-kindl/TangoByteLens) — a
client-side binary file inspector. Byte ranges render as a navigable
schema tree linked to a hex view, file formats load through a plugin
architecture, and large files stream via `Blob.slice` so nothing has to
fit in memory. Nothing leaves the browser. It's the same design-first /
tests-as-spec approach, run against TypeScript and Svelte instead of
C#/.NET.
