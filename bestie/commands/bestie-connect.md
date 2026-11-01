---
description: Connect this plugin to your Bestie App with your one-time connection code.
disable-model-invocation: false
---

Call `bestie.fetch_skill` with `{"slug":"bestie-connect"}`. Before you are connected it answers not_available. That is expected, so do not treat it as a failure.

Ask the member to paste their one-time connection code. They get it by signing in to their Bestie App, opening the Start here page and pressing Get a connection code. It starts with cwp_ and works once, for about ten minutes. Never repeat the code back and never write it anywhere.

Call `bestie.connect` with `{"pairing_code":"<the code>"}`. Tell the member which organisation it connected to, using the name exactly as returned.

When it connects, call `bestie.fetch_skill` with `{"slug":"bestie-onboard"}` and follow it exactly. It welcomes the member, lists what they can do, and offers to ask a few questions to fill in their brand and voice.

If connect answers not_available, say the code may have expired and ask them to press Get a connection code again.
