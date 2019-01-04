# Continuous Deployment With Sparkle for macOS Apps

[@robenkleene](https://twitter.com/robenkleene)
[robenkleene.com](https://robenkleene.com)
[thepotionlab.com](https://thepotionlab.com)

---

## What's Continuous Deployment?

Agile + Continuous Integration + Deployment

---

## Why Continuous Deployment?

[The Continuous Culture by Kim van Wilgen](https://www.youtube.com/watch?v=x47pgeWxXHY)

### Unused features

- **Large Deliveries**: 64% 
- **Small Deliveries**: 14%

### Chance of Success

- **Large Project**: 10%
- **Small Projects**: 74%

---

- **Slow**: 1 release every 100 days
- **Fast**: 7448 releases a day (Amazon)

### 2017 State of DevOps Report

Focus on high value work.

"High performers are doing significantly less manual work"

"HP LaserJet was able to increase time spent on developing new features by 700 percent.""

---

## Uh, Native Apps?

All this is only tangentially related to native app development where releases are more costly, and harder to rollback.

But managing releases are still tedious.

---

## System

1. Continuous integration with Bitrise
2. `rsync` it to the server
3. Manual create the Appcast
4. Deploy build for each tag

---

## Build Steps

	xcodebuild archive \
		-scheme $(SCHEME) \
		-archivePath $(ARCHIVE_PATH)

---

## Signing

---

## Continuous Integration Services

Bitrise $36/month (200 free builds a month)
Travis $69/month (Free for open source)
CirtcleCI $39/month (Nothing from for macOS)
App Center $40/month (250 free build minutes per month)