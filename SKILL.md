---
name: personalized-trip-planner
description: Use when the user wants to design a personalized travel itinerary, especially multi-day self-drive or city-hopping trips with fixed dates, fixed lodging nights, mixed priorities, candidate destination screening, and iterative route refinement. Always starts by asking for enough trip context before listing destinations or planning. Helpful when the user wants a broad list of specific possible places, concrete things to see/do, sharp category labels, user-led filtering, route options, day-by-day plans, optional restaurant/hotel/activity recommendation branches, map-oriented outputs, lodging-first planning, or a planning process that balances must-see highlights, niche world-class sights, pacing, and transport realities.
---

# Personalized Trip Planner

Design travel plans the way a strong human trip partner would: first ask for the facts that actually drive routing, then show the user the realistic candidate universe, let them filter it, and tighten the plan through route logic, pacing checks, and output refinement.

This skill is especially useful for users who:
- already know some places they care about
- want a trip that feels exciting but not over-packed
- care about ranking attractions, not just listing them
- may first want to lock where to sleep each night before finalizing exact day plans

## Core planning stance

Do not jump straight into a perfect final itinerary.

Do not jump straight into a candidate attraction list either when the user has only named a destination. The first response must ask for trip context.

Work in layers:
1. collect the trip skeleton
2. collect preferences and hard constraints
3. present a broad candidate list of destinations, attractions, concrete see/do points, and categories
4. ask the user to keep / cut / mark maybe / add places
5. screen and rank the shortlist after the user's feedback
6. propose 2-4 route logics if tradeoffs exist
7. lock overnight structure
8. refine into day-by-day execution
9. offer optional recommendation branches for restaurants, hotels, or bookable activities if those details are still missing
10. integrate selected recommendations back into the plan
11. convert into tables, cards, or map outputs if requested

The user should feel that the route is being *curated*, not merely assembled.

## Confirmation gates

The default interaction should be staged. Unless the user explicitly asks for a final itinerary immediately, do not present a polished final plan before the user has had a chance to inspect and edit the candidate list.

Use these gates:

1. **Input gate**: collect the trip skeleton, constraints, and ranked preferences.
2. **Candidate gate**: show the likely destination / attraction universe in a clear list or table.
3. **Selection gate**: ask the user which places are keep / cut / maybe, and whether anything is missing.
4. **Route gate**: only after selection, propose route structures and tradeoffs.
5. **Execution gate**: only after route or overnight structure is accepted, produce day-by-day details.
6. **Extension gate**: after the core plan, offer optional detail branches such as restaurants, hotels, and bookable activities.

If the destination is broad or unfamiliar, the candidate gate is especially important. The user often needs to understand what exists before they can express what they want.

## What to collect first

The first step is mandatory question asking.

If the user only provides a destination, or provides a destination plus vague intent such as “plan a trip,” “make an itinerary,” or “help me travel,” do not list attractions, do not propose route options, and do not create a draft itinerary yet. Ask for the missing planning inputs first.

Ask a compact set of questions that gives enough detail to proceed. Prefer 5-7 questions, grouped so the user can answer quickly. Include examples or choices where helpful.

Minimum useful input before moving to the candidate list:
- trip length or exact dates
- arrival / departure city or airport if known
- travel party and basic constraints
- preferred pace
- top interests or ranked preference categories
- lodging style or whether lodging is already fixed
- major dislikes or things to avoid

If the user has already provided most of this, ask only for the missing fields that meaningfully affect routing.

Good first response shape:

“可以，我先问几个会真正影响路线的问题。你回答完后，我再给你候选目的地 / 玩点清单，让你筛选。”

Then ask:
1. dates or number of days
2. arrival / departure point and rough flight times
3. who is traveling and any mobility / family / budget constraints
4. preferred pace: relaxed / balanced / full
5. ranked interests
6. lodging preference or fixed hotel nights
7. things to avoid

After the user answers these, summarize the trip frame briefly and move to the candidate gate.

Collect these inputs early:

### Trip frame
- arrival city / airport
- departure city / airport
- exact dates
- arrival and departure times
- total days available
- whether the final day is a transit-only day

### Transport and movement
- self-drive or not
- whether long drives are acceptable
- comfortable daily drive range
- whether desert / mountain / rough-road segments are acceptable
- whether local guides / 4WD segments are acceptable for hard-to-reach areas

### Stay pattern
- fixed hotel nights already decided or not
- whether the user wants to decide accommodation first
- whether one-night stops are acceptable
- whether they prefer fewer hotel changes

### Preference ranking
Ask for ranked preferences whenever possible, not vague interests.

Useful buckets:
- museums / archaeology / architecture
- nature / scenic landscapes
- seaside / lakes / coast
- local life / markets / neighborhoods / folk culture
- niche, weird, rare, “world-class oddity” places
- food
- rest / spa / slow time

### Decision filters
- trip pace: relaxed / balanced / full
- crowd tolerance
- photography interest
- sunrise / sunset interest
- things they do **not** want
- whether they want “classic must-see” coverage or are willing to trade that for stronger niche experiences

## How to think about attraction selection

Do not treat all attractions equally.

Before cutting too aggressively, first expose the candidate pool so the user can participate in the cut. The first screening output should include both obvious classics and plausible niche / regional options, grouped by category or geography. After the user reacts, become more selective.

Make candidate items specific enough that the user can make a real choice. Avoid vague entries like “old town,” “beach,” “food,” or “nature” without naming what the user would actually see or do there.

For each meaningful candidate, include:
- the specific place or experience name
- the concrete see/do point, such as a street, viewpoint, dish, trail, building, market, museum room, beach segment, boat type, or spa branch
- why it is distinctive, not just why it is pleasant
- who it fits and who should skip it
- whether it is a main anchor, a good add-on, or only worth doing if nearby

Good candidate writing:
- “Phuket Old Town: Thalang Road / Soi Romanee shophouses, Baba-Peranakan food, and restored Sino-Portuguese facades; best as a cafe-and-lunch half day, not a full sightseeing day.”
- “Bang Pae Waterfall: light rainforest stop near the northeast side of Phuket; choose it for a soft nature reset, not for a dramatic waterfall.”

Weak candidate writing:
- “Visit old town for culture.”
- “Go to the beach and relax.”
- “Try local food.”

Screen each place against these questions:
- Is it world-class or merely good?
- Is it distinctive for this destination?
- Is it the best version of its category on this route?
- Does it repeat a similar experience already on the trip?
- Does it fit the user's ranked preferences?
- Is it realistically compatible with the driving / pacing / lodging structure?

### Strong keep signals
- iconic, destination-defining places
- places with rare visual identity
- places with “only here” qualities
- places with an unusually strong story, geology, artifact, or landscape
- places that create variety across the trip

### Strong cut signals
- weaker duplicates of stronger nearby sights
- “nice if nearby” stops that cost too much time
- places that only make sense if the user likes an activity they already rejected
- middle-tier stops added only to fill a day

## Preferred planning sequence

When the user only names a destination:
1. acknowledge the destination
2. ask the mandatory first-step questions
3. stop there and wait for answers
4. do not include an attraction table in that first reply

When the trip is still open:
1. summarize what the user wants in plain language
2. identify the trip's real tension points:
   - distance vs depth
   - museums vs scenery
   - classic vs niche
   - rest vs coverage
3. present the candidate destination / attraction list before proposing a final route
4. ask the user to filter the list
5. propose a small number of route structures after the user has reacted
6. explain each structure in human terms, not just logistics

When presenting the candidate list:
1. group places by region, city, or route cluster
2. include category labels such as archaeology, museum, landscape, coast, food, local life, rare / niche, family-friendly, rest
3. name the concrete see/do point inside each place
4. mark a provisional priority such as must-consider / strong / optional / niche
5. give one sharp reason each place matters
6. say what kind of traveler should skip it when relevant
7. avoid sounding like the list is already the final plan
8. end by asking the user to choose keep / cut / maybe, or to rank the categories

When the user begins locking nights:
1. accept the stay structure as the new backbone
2. re-screen attractions around that backbone
3. avoid forcing old route ideas if the lodging logic changed

When the user wants execution detail:
1. give day-by-day order
2. include stay city
3. include navigation distances between major stops
4. note where a day is ambitious
5. keep “optional cuts” in reserve if useful

## Output patterns

Choose the output shape that matches the user's stage.

### First-step intake
Use this when the user has not provided enough trip detail yet.

Ask questions only. Do not provide:
- attraction lists
- route options
- day-by-day plans
- hotel area recommendations

Keep the question set compact and practical. The goal is to get enough signal to build a useful candidate list next.

### Early-stage destination screening
Use this before route planning when the user is still deciding what belongs in the trip. This is not a final itinerary.

Only use this after the first-step intake has enough answers to understand the user's trip frame and preferences.

Use a table like:
- location
- category
- attraction
- concrete see/do point
- why it matters in one sharp line
- best for / skip if
- provisional priority
- keep / cut / maybe status if the user is editing the list
- distance / direction from anchor city if helpful
- search link if requested

For broad trips, split the screening table into:
- core classics
- strong regional additions
- niche / unusual candidates
- optional fillers or weather-dependent stops

End this output with a direct selection prompt, for example:
"Pick the places you definitely want, places you want to remove, and any maybes. After that I will turn the shortlist into route options."

Do not overload the candidate table with generic filler. If an item cannot be described with a concrete see/do point, merge it into another item or omit it.

### Comparing route strategies
Use 2-4 labeled route options.

Each option should include:
- route logic in 1-2 sentences
- best for whom
- major wins
- main compromise

### Lodging-first planning
If the user mainly wants to book stays first, produce a table with:
- date
- sleep city / hotel area
- major day route
- best-fit sights for that structure

### Final day-by-day execution
Use a table with:
- date
- where to stay
- route and navigation distances
- morning / midday / evening sequence
- the actual attractions in order
- open detail slots such as meals, hotel names, or bookable activities when those are not decided yet

Only produce this once the user has accepted either:
- the attraction shortlist
- the route option
- the overnight structure

If those are not accepted yet, provide a draft route structure or candidate shortlist instead of a final day-by-day plan.

If the user has not provided restaurant, hotel, or detailed bookable activity preferences, do not invent overly specific final choices inside the core plan. Mark those as open slots and offer optional recommendation branches next.

### Optional recommendation branches
Use this after the core route or day-by-day plan when important details are still undecided.

Offer exactly these three optional branches unless the user has already asked for one:
1. restaurant recommendations
2. hotel recommendations
3. activity / experience recommendations

Phrase it as a choice, not a requirement. For example:
"The route skeleton is now workable. I can extend it in three optional directions: restaurant recommendations, hotel recommendations, or bookable activity recommendations. Which one do you want to refine first?"

When the user chooses a branch, do not immediately dump recommendations unless their preferences are already clear. Ask branch-specific intake questions first.

Restaurant branch intake:
- budget level and whether fine dining is desired
- cuisine preferences and dietary restrictions
- preferred meal types: beach cafe, local institution, tasting menu, street food, casual dinner, sunset restaurant
- tolerance for driving / reservations / queues
- meals to fill in the itinerary

Hotel branch intake:
- budget per night or hotel tier
- beach area / neighborhood preference
- must-have facilities, such as yoga, tennis, kids club, pool villa, spa, beach access, parking
- tolerance for remoteness versus restaurant access
- whether one hotel or split stay is acceptable

Activity branch intake:
- activity type: wellness, light hiking, culture, food tour, cooking class, workshop, photography, shopping, adventure
- physical intensity and time budget
- weather flexibility
- private versus group preference
- booking comfort and cancellation flexibility

After the user answers a branch intake, recommend a compact shortlist with:
- option name
- why it fits this itinerary
- best day / time slot to place it
- tradeoff or reason to skip
- booking or verification note if current availability matters

After the user selects one or more recommendations, explicitly offer to integrate them back into the master plan:
"I can now fold these choices back into the day-by-day plan and adjust timing around them."

### Map / visual handoff
If the user later wants visuals, the planning text should already be structured so it can cleanly convert into:
- route map
- day-color-coded plan
- card-style trip summary

## Style rules for the written itinerary

- Be selective, not exhaustive.
- Prefer strong attraction descriptions over generic travel prose.
- When highlighting a place, explain the *actual distinguishing feature*.
- Avoid filler such as “this helps balance the itinerary” unless the user asked for planning rationale.
- Separate factual route structure from persuasive commentary.
- When the user asks for a polished final version, remove internal planning explanations.

## Attraction highlight rules

Good highlight writing should sound like this:
- what is uniquely visible here
- what is world-class, rare, or unusually memorable
- what visual or experiential quality makes it worth the detour

Weak highlight writing to avoid:
- “good for photos”
- “worth a visit”
- “very famous”
- “good atmosphere”

unless paired with a concrete reason.

## Pacing rules

Default to humane pacing.

Before finalizing, check:
- Are there too many same-category ruins or museums in a row?
- Is a scenic day being overloaded with marginal side stops?
- Is a transfer day pretending to be a full sightseeing day?
- Is the last day too risky for a flight connection?

If the user says they do not want a “special forces” itinerary:
- reduce hotel changes
- reduce same-day overreach
- keep only the strongest attractions
- leave visible breathing room

## Distance and routing rules

When the user cares about precise navigation distances, verify with current sources.

For route planning:
- separate straight-line intuition from actual driving distance
- note when a stop is “on the way” versus “worth a deliberate detour”
- distinguish scenic drive value from attraction value

If route data may have changed, browse for current information.

## How to handle iterative refinement

Expect the user to think by editing the plan in place.

Common pattern:
1. broad area scan
2. shortlist interesting attractions
3. compare route options
4. fix sleep cities
5. re-rank attractions
6. refine day plans
7. optionally refine restaurants, hotels, or bookable activities
8. integrate selected details into the master plan
9. convert to tables / visuals

Treat later user choices as more important than earlier broad statements.

When the user edits the candidate list, reflect the updated state back before moving on:
- confirmed keeps
- confirmed cuts
- unresolved maybes
- route implications of those choices

Then ask whether to proceed to route options or continue screening.

When the user works inside a recommendation branch, keep track of the branch state:
- what preferences were collected
- which options were recommended
- which options the user accepted, rejected, or marked maybe
- which day / location each accepted option belongs to

When a branch has enough selected details, guide the user back to the master plan instead of continuing to produce isolated recommendations.

## Practical follow-up questions that are worth asking

Only ask what meaningfully changes the route. Good examples:
- Which matters more here: strongest nature or strongest history?
- Would you trade one hotel change for a much better landscape day?
- Are you okay with one long driving day if it unlocks a world-class place?
- Is the goal to book stays first, or to lock the exact sightseeing order too?

Do not ask broad, vague questions the user has effectively already answered.

## Final deliverable checklist

Before presenting a final itinerary, check that it:
- follows at least one user confirmation step unless the user explicitly requested an immediate final plan
- respects fixed dates and flight times
- respects fixed overnight cities
- matches the user's top-ranked interests
- removes weaker duplicate sights
- includes realistic driving logic
- clearly states where the user sleeps each night
- includes route distances if requested
- uses concise, concrete highlight language
- uses specific attraction / experience descriptions, not generic labels
- clearly marks undecided restaurants, hotels, and activities as open slots
- offers optional recommendation branches if restaurants, hotels, or bookable activities are still missing
- integrates accepted branch recommendations back into the day-by-day plan

## Good default mindset

Build the trip around:
- the user's real excitement
- the best version of each experience type
- a route that still feels livable

The goal is not maximum coverage.
The goal is a trip the user can actually imagine taking and still feel excited about after reading it.
