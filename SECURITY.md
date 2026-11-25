# Security policy

This covers every kadr package: kadr, kadr-ui, kadr-captions, kadr-photos,
kadr-audio, kadr-persistence and Kadr Studio.

## Supported versions

Fixes go into the latest release of each package. For kadr, that is the latest
1.x. For the other packages, it is their latest minor version.

## Reporting a vulnerability

Please don't open a public issue. Report it privately instead: on the affected
repository, open the **Security** tab and choose **Report a vulnerability**.
Only the maintainer sees the report.

A useful report says:

- which package and version,
- what an attacker could do, and
- how to reproduce it, ideally with the file or code that triggers it.

kadr is maintained by one person, so allow a few days for a first reply. When
a fix ships, the advisory is published and credits you, unless you'd rather it
didn't.

## What counts

kadr reads files that apps hand it, so the likeliest problems are crafted
inputs. For example:

- a video, image, LUT (`.cube`) or caption file (SRT, WebVTT) that crashes the
  app, hangs it, or makes kadr read or write outside the paths it was given;
- a saved project that kadr-persistence decodes into something unsafe.

Bugs in AVFoundation or Core Image themselves belong with Apple, through
[Feedback Assistant](https://feedbackassistant.apple.com). If you're not sure
which side a problem is on, report it here and we'll work it out.
