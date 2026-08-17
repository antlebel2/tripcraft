# TripCraft MVP

## MVP Goal

TripCraft V1 should prove that a traveler can provide the essential shape of a trip, answer relevant planning questions, and receive a realistic daily itinerary that gives them a credible starting point rather than something they must reconstruct.

The primary outcome is:

> Turn a traveler’s destinations, approximate duration, preferences, constraints, and existing plans into a saved, realistic daily itinerary that they can refine.

## Smallest Coherent User Journey

1. The traveler begins a new trip with at least one destination in mind.
2. Before generating the first itinerary, TripCraft gathers:
   - One or more destinations.
   - An approximate trip duration.
3. TripCraft asks an adaptive set of questions based on what the traveler has already provided.
4. The traveler supplies whichever additional information they know, such as:
   - Approximate or exact travel dates.
   - Interests and dislikes.
   - Must-do experiences.
   - Number and types of travelers.
   - Preferred pace.
   - Fitness level.
   - Mobility or accessibility constraints.
   - Transportation preferences.
   - Budget guidance.
   - Fixed commitments.
   - Reservations.
   - Existing itinerary items.
5. TripCraft determines whether it has enough information to create a responsible first draft. If it needs more information, it explains why.
6. Once the minimum trip information is present, the traveler may request an early draft before completing every suggested question.
7. TripCraft creates and saves a multi-day itinerary.
8. The traveler reviews the itinerary and refines it by adding, removing, replacing, moving, locking, or regenerating itinerary content.
9. The traveler can leave TripCraft and return later without losing the trip or its itinerary.

## Information Required Before First Generation

The traveler does not need to have all trip details when beginning the planning process. TripCraft should prompt for missing information as needed.

Before generating the first itinerary, TripCraft must know:

- At least one destination.
- An approximate duration.

Exact or approximate travel dates are not required. A duration range is acceptable when its minimum and maximum are no more than three days apart. For example, seven to ten days is sufficiently specific, while seven to fourteen days is not.

No other individual answer is universally required. TripCraft should evaluate the information as a whole and request additional context when generating an itinerary without it would likely produce a poor result.

A traveler may request an early draft after providing the required information. When relevant details remain unknown, TripCraft should clearly identify its assumptions and the resulting limitations.

Destination discovery is not part of V1. “I want to travel somewhere” is not enough to begin itinerary generation.

## Required for V1

### Adaptive Trip Intake

V1 must:

- Gather information through an adaptive questionnaire.
- Avoid asking for information already supplied in the traveler’s answers or existing plan.
- Explain why an additional answer is needed before generation when the available information is insufficient.
- Allow travelers to skip information that is not required.
- Allow an early draft after the minimum generation requirements have been met.
- Distinguish user-provided facts from assumptions made because information is missing.

### Multiple Destinations

V1 must:

- Support trips containing multiple destinations.
- Allow TripCraft to suggest the order of destinations.
- Allow travelers to reorder destinations during refinement.

Detailed optimization of travel between destinations is not required for V1.

### Initial Itinerary Generation

V1 must produce a complete first draft organized by day and broad periods such as:

- Morning.
- Afternoon.
- Evening.

The itinerary must:

- Incorporate the traveler’s must-do experiences.
- Preserve and account for fixed commitments and reservations.
- Account for expected activity duration.
- Reflect the traveler’s requested pace.
- Respect stated fitness, mobility, and accessibility constraints.
- Include reasonable meal periods.
- Avoid adding explicit rest periods unless the traveler requests them or their stated needs make them appropriate.
- Account for an existing partial itinerary.
- Surface important assumptions and missing information.

V1 does not need to recommend named businesses. It may use contextual placeholders such as:

- “Casual dinner near the evening activity.”
- “Choose a moderate trail appropriate for the group.”
- “Explore a museum matching the traveler’s interests.”

Placeholders should be specific enough to communicate the purpose, pacing, and intended context of an itinerary item.

### Existing Plans

V1 must allow travelers to manually enter:

- Existing itinerary items.
- Must-do activities.
- Fixed commitments.
- Reservations.

TripCraft must incorporate those items into its questions and recommendations rather than ignoring them, asking for the same information again, or proposing conflicting plans.

Automatic interpretation or import of arbitrary documents, emails, confirmations, and booking-service data is not required.

### Itinerary Refinement

After generating an itinerary, travelers must be able to:

- Add a suggested activity.
- Add a custom activity.
- Remove an activity.
- Replace an activity.
- Move an activity within a day.
- Move an activity to another day.
- Reorder destinations.
- Change preferences or constraints and request corresponding revisions.
- Lock accepted items so later revisions preserve them.
- Regenerate an individual day.
- Regenerate the entire trip.

TripCraft must not silently make meaningful planning changes. The traveler remains the final decision-maker.

### Saved Trips

V1 must persist trips and itineraries so travelers can:

- Save their progress.
- Leave the product.
- Return later.
- Continue reviewing and refining the same trip.

Persistent saved trips are part of the core MVP journey, not an optional enhancement.

### Budget Input

Budget is an optional planning input in V1.

TripCraft may use broad budget guidance to influence the general character of its suggestions. V1 does not promise:

- Exact prices.
- Cost estimates.
- A calculated itinerary total.
- Comprehensive trip budgeting.
- A guarantee that the itinerary fits a precise monetary limit.

## Explicitly Not Required for V1

V1 does not require:

- Destination discovery or destination selection.
- Booking or purchasing flights, accommodations, activities, restaurants, or tickets.
- Group collaboration, invitations, shared editing, or voting.
- Named restaurant, hotel, tour-provider, or other business recommendations.
- Accommodation search or booking.
- Planning transportation to and from the overall trip.
- Detailed local navigation.
- Geographic route optimization.
- Travel-time validation between itinerary items.
- Opening-day or opening-hour validation.
- Detailed planning or optimization of travel between destinations.
- Exact hour-by-hour scheduling.
- Exact or comprehensive budgeting.
- Live or guaranteed weather information.
- Local event discovery.
- A complete trip-readiness system.
- Packing guidance.
- Travel-document or entry-requirement guidance.
- Automatic imports from email, documents, booking services, or external accounts.
- Long-term preference learning across multiple trips.

## Possible Future Features

Potential post-MVP capabilities include:

- Destination inspiration and recommendations.
- Named places, restaurants, accommodations, attractions, tours, and businesses.
- Opening-hours and closure validation.
- Geographic clustering and route optimization.
- Estimated travel time between activities.
- Detailed transportation planning.
- Travel planning between destinations.
- Exact timed schedules.
- User-selectable planning precision, including hour-by-hour control.
- Current or historical weather guidance.
- Seasonal suitability checks.
- Local event discovery and recommendations.
- Approximate costs and complete trip-budget estimates.
- Accommodation, flight, and transportation research.
- Booking links and deeper integrations with specialized booking services.
- Importing reservations and confirmations from external sources.
- Group invitations, shared viewing, collaborative editing, and voting.
- Full trip-readiness tracking.
- Packing, documentation, entry-requirement, and preparation guidance.
- Long-term preference learning with the traveler’s permission.

## MVP Success Criteria

The MVP succeeds when:

- A traveler can start with a destination and approximate duration rather than needing a fully researched trip.
- TripCraft gathers enough pertinent information to avoid producing a generic or obviously unsuitable itinerary.
- The traveler can request an earlier draft once the minimum generation requirements are satisfied.
- The resulting itinerary includes the traveler’s must-dos, fixed commitments, reservations, and existing plans.
- The plan is organized into understandable days and broad periods.
- Activity duration, meals, pace, fitness, mobility, and accessibility needs are reflected appropriately.
- Important assumptions and limitations are understandable.
- The traveler can revise the plan without losing accepted or locked items.
- A multi-destination trip can be created and reordered.
- The trip remains available when the traveler leaves and returns.
- The resulting itinerary is a credible planning foundation that needs refinement rather than reconstruction.

## MVP Boundaries

V1 proves itinerary creation and iterative refinement. It does not attempt to complete the traveler’s entire planning journey.

TripCraft may provide a useful plan without identifying every exact venue, validating every external fact, optimizing every route, or managing every trip preparation. Those limitations should be visible rather than hidden.

The traveler owns all meaningful decisions. TripCraft proposes, organizes, explains, and revises, but does not silently finalize decisions or claim certainty it does not have.
