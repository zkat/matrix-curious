# matrix-curious

FAQ and resources for those curious about joining the Matrix network!

## General FAQ

### What is Matrix?

You know how you can send and receive email from any number of services and clients, and email servers are able to talk to each other and figure out who gets what, and no one specifically "owns" email so there's a lot of room for different clients to do things better in different ways?

You can think of Matrix as that, but for chat platforms. The "siloed" counterparts to Matrix would be Discord, Slack, Teams, etc. Matrix might seem like it's behind these in comparison, but it's a more forward-looking and fast-growing alternative that's... better for the environment. :)

### How do I sign up? What are all these "servers"?

You can sign up on any server, and still chat with anyone on (mostly) any other server! So, for the most part, it doesn't matter where you sign up.

If you want to go the _easy_ way, that's probably to sign up on [matrix.org itself](https://app.element.io/?pk_vid=d4b162e0e6c511851631808451ab93fb#/register), but you can also talk to a friend, or [pay to host your own, using your own domain name](#hosting-faq)

### What do all these terms mean?

Most concepts for folks coming from Slack/Discord/etc map fairly easily. Here's a short glossary/thesaurus of terms and how they map between services.

Discord |Slack | Matrix | Notes
--------|------|--------|-------
channel | channel | room | n.b. Slack servers are sometimes called "channels" but I don't think this is official.
server | server/channel | space | Spaces are a bit fancier in some ways, such as rooms being able to exist in multiple Spaces, and Spaces being able to contain other Spaces themselves.
instance (usually the _service_ itself) | instance (usually the _service_ itself) | server or homeserver | Matrix is [federated](https://matrix.org/faq/#what-does-federated-mean%3F). Many "servers" can talk to each other to form a network, and everyone can talk to each other across these servers, regardless of where their "homeserver" is.


### Help! I tried to join the Matrix Curious link but I can't join the room?

The [Matrix Curious link](https://matrix.to/#/#matrix-curious:matrix.org) is actually a link to something called a "Space", roughly equivalent to a Discord or Slack server. They're a very new feature, so many clients don't yet fully support them. Some of the confusion comes from the fact that they are _technically_ rooms, so clients who aren't fully Space-aware might get confused and try to treat it as one.

If you try first joining the space from something like Element or FluffyChat, you'll be able to join the rooms, and then other clients should work just fine for those individual rooms.

### The UX for this is really painful!

There's a lot of sharp corners in pretty much all the main clients right now, but they're still good enough to be usable for the day-to-day. UX and perf improvements are the highest priority right now for Element and a lot of other developers, so you should see marked improvements in the coming months (as of Nov 2021).

If you have specific pain points, feel free to ask about them on Matrix Curious! That's exactly what it's for! We'll do our best to either sort you out, or point you at a tracking issue for the fix!

### I see a lot of cryptocurrency/blockchain stuff on the matrix.org registry. Is this a blockchain thing?

Absolutely not! Matrix is its own, non-blockchain, protocol, and the developers aren't super supportive of blockchain stuff. It just so happens that Matrix is a pretty useful platform, and some early adopters have pretty technolibertarian tendencies, which often overlap with blockchain stuff.

If this is not something you're into, there's plenty of comfortable spaces away from that bullshit, such as Matrix Curious! :)

## Features FAQ

### How do I enable Labs features on Element?

Go to Settings and go to the Labs tab on the sidebar. There's lots of good stuff there to try!

### Does Matrix support threads/threading?

Threading is [actively being worked on](https://github.com/vector-im/roadmap/projects/1#card-48804707). Some clients, such as Element, already support threading. On Element, you'll have to enable the Labs feature. (As of nov 2021)

### Does Matrix support custom emoji?

Not in the protocol right now, and it's not a priority, but some clients such as FluffyChat (TODO: link) already support custom emoji packs!

However, Element is planning on supporting it in the future, see [their roadmap](https://github.com/vector-im/roadmap/projects/1#card-48806230).

### Does Matrix support stickers?

Not yet, some proposals exist (see [here](https://github.com/matrix-org/matrix-doc/pull/1951) and [here](https://github.com/matrix-org/matrix-doc/pull/2545)), and Fluffychat, Nheko-reborn, and Element (with an integration manager) technically support it, it's not as polished or straight-forward as, for example, Telegram.

### The notification defaults are really noisy. How do I fix it?

You can change your default ("global") settings by going to the settings menu of your favorite app. On Element Desktop, this is the area you usually want to edit:

![Global notification settins on Element Desktop](media/notifications.png)

"Noisy" means you'll get a big notification badge and an audio notification.

## Hosting FAQ

### I want my own account/@ on my own domain. How can I do that?

You can use [these hosting services](https://matrix.org/hosting/)! Some of them support bringing your own domain name.

Note that, right now, there's no real identity migration path, so if you lose access to your server/domain, it's possible that you'll lose your entire matrix identity/history, so pick a provider you trust. The account migration story is currently being worked on, so this is not going to be true in the longer term.

