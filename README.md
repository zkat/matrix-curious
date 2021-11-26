# matrix-curious

FAQ and resources for those curious about joining the Matrix network!

To ask more questions, or just try things out in a space meant for newbies to do just that, join the [Matrix Curious Space](https://matrix.to/#/#matrix-curious:matrix.org)!

Don't know how to join? Keep reading below!

## General FAQ

### What is Matrix?

You know how you can send and receive email from any number of services and clients, and email servers are able to talk to each other and figure out who gets what, and no one specifically "owns" email so there's a lot of room for different clients to do things better in different ways?

You can think of Matrix as that, but for chat platforms. The "siloed" counterparts to Matrix would be Discord, Slack, Teams, etc. Matrix might seem like it's behind these in comparison, but it's a more forward-looking and fast-growing alternative that's... better for the environment. :)

### How do I sign up? What are all these "servers"?

You can sign up on any server, and still chat with anyone on (mostly) any other server! So, for the most part, it doesn't matter where you sign up.

If you want to go the _easy_ way, that's probably to sign up on [matrix.org itself](https://app.element.io/?pk_vid=d4b162e0e6c511851631808451ab93fb#/register), but you can also talk to a friend, or [pay to host your own, using your own domain name](#hosting-faq)

### Is there a client? Which one should I pick?

There's [a bunch of clients](https://matrix.org/clients/), with different levels of support and features. In general, it seems Element and FluffyChat are the more feature-complete ones, but the others are worth trying out, too, and some of them even do things in interesting ways. Element and FluffyChat both also have iOS and Android clients.

### What do all these terms mean?

Most concepts for folks coming from Slack/Discord/etc map fairly easily. Here's a short glossary/thesaurus of terms and how they map between services.

Discord |Slack | Matrix | Notes
--------|------|--------|-------
channel | channel | room | n.b. Slack servers are sometimes called "channels" but I don't think this is official.
server | workspace (sometimes people refer to them as "channels" anyway) | space | Spaces are a bit fancier in some ways, such as rooms being able to exist in multiple Spaces, and Spaces being able to contain other Spaces themselves.
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

### How do I do spoilers/CW/sensitive messages?

For messages, this varies by client. In Element, you can usually just use the `/spoiler` slash command. Other clients might vary. Feel free to PR your client's method here.

For media, there's currently no support for spoilers/CW. ([Tracking issue](https://github.com/vector-im/element-web/issues/10882))

### Can I add alt text to images?

Not in a portable way right now. There's a text field but some clients use it for filename, some for alt text. That's something that currently needs fixing in the protocol. If this is important to you, please push for it [here](https://github.com/matrix-org/matrix-doc/pull/2530). The current more generalized push for something that would allow alt-text (among other things) is [MSC1767](https://github.com/matrix-org/matrix-doc/pull/1767).

### Can I pin messages?

This is currently in progress, and is a Labs feature on Element (TODO: link?).

### Does Matrix support audio/video calling? What about screen sharing?

It does! Though, again, features available may depend on your client.

### The notification defaults are really noisy. How do I fix it?

You can change your default ("global") settings by going to the settings menu of your favorite app. On Element Desktop, this is the area you usually want to edit:

**All Settings** → **Notifications** → **Global**

| Option                            | Setting |
|-----------------------------------|---------|
| Messages in group chats           | Off     |
| Encrypted messages in group chats | Off     |

![Global notification settings on Element Desktop](media/notifications.png)

"Noisy" means you'll get a big notification badge and an audio notification.

### If Matrix supports end-to-end encryption (E2EE), why don't all channels use it?

E2EE is great, but it comes with some disadvantages when it comes to large community rooms, for example:

1. Most bots don't work
2. A lot of clients still don't support it
3. It stops some conveniences from being possible, such as the server resizing images for you, which leaves more work on the client side (slowing things down)

In general, there's not much/any benefit in E2EE for very large, public channels where anyone could be there, so the setting is turned off by default because of this.

### Can I have a different display name/nickname per room/space?

Yes! How you change it depends on the client but, for example, the `/myroomnick` slash command will let you do this on Element.

You can also set your display name globally in Settings.

Note that no clients currently let you change a nickname _space-wide_, and there's nothing in the protocol for doing this.

### Can I add profile information to my account?

There's a [proposal for that](https://github.com/matrix-org/matrix-doc/pull/1769) in discussion, which would allow arbitrary data, but no clients currently use it. It doesn't require any server-side changes so it can be contributed!

## Hosting FAQ

### I want my own account/@ on my own domain. How can I do that?

You can use [these hosting services](https://matrix.org/hosting/)! Some of them support bringing your own domain name.

Note that, right now, there's no real identity migration path, so if you lose access to your server/domain, it's possible that you'll lose your entire matrix identity/history, so pick a provider you trust. The account migration story is currently being worked on, so this is not going to be true in the longer term.

