# Concept: a heat check-in service for solo elderly farmers

Built from [the problem statement](problem-statement.md): elderly people doing outdoor farm work in South Korea, often alone, during the hours the government's own advisory already flags as most dangerous.

## Who it's for

The elderly farmer is the one enrolled and who uses the service day to day. A family member (typically an adult child) is the one who signs up and pays.

## What it does

A subscription SMS check-in service:

- On any day with an **active extreme-heat advisory**, the farmer receives a single check-in text.
- If they don't reply within a set window, the service texts/calls a **pre-designated neighbor**, who physically checks on them.

This targets the government's own noon–5 p.m. advisory window directly — the same window the KDCA already recommends avoiding for outdoor work ([Korea heat deaths, elderly](../sources/korea-heat-deaths-elderly.md)).

## How it works in the real world

- **Business model:** a startup, not a government or nonprofit program. Family members pay the recurring subscription; the farmer isn't the one billed.
- **Enrollment requirement:** signing up requires naming at least one reachable neighbor as the escalation contact. **Farmers with no reachable neighbor cannot enroll** — that's a deliberate scope limit, not an oversight (see below).
- **Trigger source:** the service depends on a reliable feed of extreme-heat-advisory days to know when to send a check-in at all; it assumes such a feed exists and is accurate.
- **Mechanism:** basic SMS, not an app or wearable — the target user is an elderly farmer, so the service is built for a basic phone, not a smartphone.

## What we're deliberately leaving out

- **Deaths at home or near roads.** Of South Korea's 238 recorded heat deaths since 2011, **15% happened at home** and roughly **14% near roads** ([Korea heat deaths, elderly](../sources/korea-heat-deaths-elderly.md)). This service is scoped to farm work specifically; it does nothing for those settings.
- **Farmers with no reachable neighbor.** Both named cases in our source — a woman in her 80s near a greenhouse in Jinju, another on Jeju Island — were found only after they'd already collapsed, with no one nearby ([Korea heat deaths, elderly](../sources/korea-heat-deaths-elderly.md)). A service that requires a neighbor to enroll does not reach farmers in that exact situation. We're choosing to scope around this rather than solve for it yet.

## Open question

Whether "no neighbor on file" should eventually fall back to emergency services automatically was raised and deliberately deferred — for now, a reachable neighbor is a hard requirement to enroll at all.
