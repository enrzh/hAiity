# Public screenshots

Captured October 7, 2026 from hAiity source revision `98241c1`, build 276, on
an isolated iPhone 18 Pro simulator running iOS 27. They are native app captures,
not reconstructed UI or photographs of personal data.

The launch uses the app's simulator-only `-design-fixture realistic` mode. It
creates its own temporary HabitStore, disables native/cloud integrations and
uses example reading, water and walking habits. `-pro on` demonstrates Pro
statistics without a purchase. No real Apple account or habit data is used.

| File | Screen |
| --- | --- |
| `habits.png` | Habits, light |
| `habits-dark-new.png` | Habits, dark |
| `statistics.png` | Stats, light, Pro preview |
| `more.png` | More, light |

To refresh, build the current Debug simulator app in the private source
repository, install it into a dedicated screenshot simulator, and launch with:

```
xcrun simctl launch <screenshot-simulator-id> com.aiity.haiity \
  -design-fixture realistic -screen habits -pro on \
  -AppleLanguages '(en)' -AppleLocale en_GB -design-appearance light
```

Use `stats` or `more` for the other screens and `dark` for dark appearance.
Set a consistent status bar with `simctl status_bar`, then photograph the
settled screen with `simctl io <id> screenshot <path>`. Inspect every image
before publishing. Retain the original PNG pixels and aspect ratio. Older,
unreferenced screenshots remain for historical links; they are not current UI.
