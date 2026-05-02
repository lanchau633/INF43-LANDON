# 43
### Title: MapMates: 
Team Members: Anna Chen (annac26), Daniel Han (hand12), Daniel Cho (djcho5@uci.edu), Burhan Shahid (shahidb@uci.edu), Landon Chau (landonc2@uci.edu)

#### Executive Summary:
MapMates is an iPhone application that allows people to find others with similar interests in their area. 

The audience of MapMates is any person who is looking for other people with similar interests. 

The goal of MapMates is to help connect people together through finding similar interests and proximity. 

The first main feature is pre-made tags, where users are able to describe their interests so that others can identify similar users. 

Our second main feature is a user biography, where users can write a small blurb introducing themselves to other users. They are also able to add contact information in the biography to connect with other users outside of the app, such as phone number or Instagram. 

The third feature is interest pins. People can pin a location on a map showing where an event will be held, and other users will be able to view it and participate in the event if they are interested. Along with that, we have a directory of interest pins. People are able to search through upcoming interest pins to find nearby events they may want to attend.

Our fourth feature is an interactive map where users can view the location of other users and events. Along with that people can add extra information to their location, such as a picture or description giving location context.

Additionally, our fifth feature provides user verification through facial recognition and age verification. When creating an account, people must go through user verification in order to prevent bots and scams on the application and strengthen our community.

Our sixth feature is that users can specific distance ranges for finding people and events. People can set their search radius from 2 miles to 50 miles near them so they can find events and people they can meet in person.

The seventh feature is current status, where users can broadcast what they are currently doing, such as “studying in the library”, as a more spontaneous way of meeting new people. 

Our last feature is friend requests. If users really enjoyed getting to know each other, they can add each other as friends, which allows their status and events to pop up before other users’ activity. Additionally, people can use this feature to monitor their real life friends.


#### Application Context/Environmental Constraints:
The app will run on IOS and is for mobile usage. It'll depend on the user's location settings (allow/disallow), as well as access to a photo camera in order to do facial recognition.


#### Functional Requirements:

#### Five given features:
- **Users are able to add multiple pre-made tags**: Users can add multiple descriptive tags to their profile, such as “#Basketball”, “#Piano”, and so on describing their hobbies and interests. These tags will be visible to other users, helping people find others who share similar passions and making it easier to form meaningful connections.

- **Users can create their own bio with interests**: Several areas to add contact information (phone number, instagram, etc). Each user maintains a profile with a short bio and optional contact details such as Instagram or other forms of social media, making it easy to connect beyond the app. 

- **Interest pins at a time/place for large groups to meet up / events**: Users can drop a pin on the map at a specific time and location to invite others to a planned activity or event. Pins are matched to relevant interest tags so that users with shared hobbies are notified of opportunities nearby.

- **Directory of interests for users in an area to discover**: The app provides a browsable directory of active interests, groups, and users in a given area, allowing people to discover what's happening around them. This gives users an alternative to the map view and makes it easy to explore communities, trending activities, or niche interest groups they may not have encountered otherwise.

- **Interactive map**: Map will show a tailored map of groups and meeting points set by the user tags, the interest pins are able to be specified for a specific location, such as what floor and room allows pictures to be taken of the meeting location for a better understanding.

- **Users are able to specify distance ranges**: Users are able to go into settings and change the distance they are able to start, see, or join a group meeting on a map. For specific people, the user can define the exact location the closest friends can see. For other distant friends (not best friends), a custom range (options should be given) could be defined depending on the trust level (5 mi, 10 mi, 50 mi)


#### Two unique features:
- **Account Verification**: During account creation, users complete a short facial scan and age verification step to confirm they are a real person who meets the minimum age requirement. This prevents fake profiles, bots, and underage accounts from accessing the app, creating a safer environment where users can confidently meet up knowing everyone has been verified. Verified status is displayed on each profile so users can quickly see that the people they're connecting with are legitimate.

- **Current Status**: Users can broadcast a real-time status describing what they're currently doing, such as "shooting hoops at the park," "studying at the library," or "grabbing coffee downtown." Friends and nearby users with matching interest tags can see these statuses and choose to join in spontaneously, turning everyday activities into opportunities for connection. Statuses are temporary and expire automatically after a set period, supporting casual in-the-moment hangouts alongside the pre-planned events created through interest pins.

- **Friend Requests**: Users can view other profiles and send friend requests to stay connected with people they meet through the app. Location sharing is privacy-first: only confirmed friends can see a user's general location range (not a precise pin), and non-friends cannot see location information at all unless the user explicitly enables broader visibility in settings.

#### Functional Requirements Analyses
**Feature 1: Pre-Made Interest Tags**

Description: Users select from a curated tag library that controls who they see on the map and who sees them.

Pros:
- Creates a consistent, searchable vocabulary — no fragmentation from misspellings or synonyms.
Simplifies onboarding: users immediately understand what tags are available and what to pick.

Cons:
- A fixed library cannot cover every niche hobby, making some users feel the app does not represent their interests.
- The library requires ongoing maintenance; stale or unused tags accumulate over time.
- 
Ethical Concerns:
- Certain tag categories (e.g., religious groups, political activism) could expose users to discrimination or targeting if - location data were compromised. Tag categories warrant careful design review.
- Implicitly defining "legitimate" interests through a closed list may marginalize communities not represented at launch.

#### Feature 2: User Bio & Contact Information
Description: Each user has a profile with a free-text bio and optional contact fields visible to matched users.

Pros:
- Enables genuine off-app connection; users are not locked into messaging within MapMates.
- Optional fields reduce friction — privacy-conscious users are not forced to share contact info.
- Profiles give users something meaningful to read before deciding to approach someone in person.
  
Cons:
- Displaying real contact details (phone number, Instagram) on a geolocation app creates a potential vector for harassment - if the contact-visibility gate is bypassed.
- No content moderation on bios in the initial release means offensive bios persist until reported.
- Users may enter fake or outdated contact info, frustrating others who attempt to reach out.

Ethical Concerns:
- A live location app that surfaces a phone number or social handle is a potential stalking vector. The friend-gated default is a key mitigation.
- Profiles displaying gender, age, or physical appearance combined with real-time location may enable targeting of vulnerable users, particularly women and minors.
- A future release should include content moderation and a minimum age display constraint.

#### Feature 3: Interest Pins & Directory
Description: Users create geo-tagged event pins at a specific time and place; the directory surfaces pins and communities to browsing users.

Pros:
- Transforms MapMates from a passive discovery tool into an active community-organizing platform.
- Location photos and floor/room details reduce the friction of finding the right meeting spot in complex venues.
- The directory provides an alternative entry point for users who prefer browsing to map exploration.
  
Cons:
- Public pins tied to a specific location and time could attract bad actors who wish to disrupt gatherings, particularly for minority or vulnerable groups.
- No-show culture (RSVPing without attending) may discourage organizers from continuing to post events.
  
Ethical Concerns:
- Events for sensitive groups (e.g., LGBTQ+ meetups, religious communities) listed on a public map could expose attendees to harm. A private/invite-only pin mode should be prioritized in a near-future release.
- If a pin description includes a personal home address, this constitutes a doxxing risk. The system should display a warning if a pin description appears to contain a residential address.

#### Feature 4: Interactive Map
Description: The core map view renders live user pins and event pins filtered by the viewer's tags and range settings.

Pros:
- A visual, spatial interface is the most intuitive way to understand "who is near me right now."
- Combining user pins and event pins in a single view reduces the need to switch between screens.
- Location photos and floor/room details attached to pins solve a real usability problem for large buildings or complex venues.
  
Cons:
- A densely populated map (urban area, popular tag) can become visually cluttered, degrading usability.
- Real-time location updates are battery-intensive; frequent polling may cause user complaints.
  
Ethical Concerns:
- A single map pin may effectively de-anonymize a user. The system should consider reducing precision automatically when user density is low.
- Screen recording of the map by a malicious user could enable tracking of others even if the app implements access controls. This risk is inherent to any live-map product and should be disclosed in the privacy policy.

#### Feature 5: Distance Range Settings
Description: Each user sets a global proximity range and per-friend tier ranges governing who appears on their map and who can see their location.

Pros:
- Accommodates both urban users (who may prefer 0.5–2 miles) and rural users (who may need 25–50 miles).
- Per-friend tier control gives users trust management without requiring technical knowledge.

Cons:
- Users with a very large global range (50 miles) will see many pins and may receive overwhelming notifications.
  
Ethical Concerns:
- A large range in a low-density area can effectively de-anonymize users even with location noise applied. The system should consider capping precision relative to range.
- Proximity-entry notifications could theoretically be used to track a target's movements if an adversary continuously adjusts their own position.

#### Feature 6 (Unique): Account Verification
Description: A one-time facial liveness check plus government ID age verification during onboarding.

Pros:
- Significantly reduces bot accounts, catfishing, and fake profiles, increasing user trust and safety for in-person meetups.
- Age gating protects minors
- Verified badge signals legitimacy to other users before any physical meeting.
  
Cons:
- Biometric data collection introduces regulatory obligations.
- Facial liveness APIs have documented higher error rates for users with darker skin tones, which may systematically exclude users of color.
- Government ID upload is a significant privacy ask; users with no ID or expired ID cannot be age-verified.
  
Ethical Concerns:
- ID verification may disproportionately exclude undocumented individuals or those from countries with non-standard government IDs.

#### Feature 7 (Unique): Current Status
Description: Users broadcast a short real-time text status that appears on their map pin and profile, with an timer of 24 hours.

Pros:
- Converts passive map presence into an active, low-friction social signal.
- Enables spontaneous IRL meetups that complement the pre-planned event system (Interest Pins).
- Pulsing visual indicator draws attention to "active" users without requiring notification spam.
  
Cons:
- Free-text statuses with no moderation in the initial release can surface offensive content to nearby matching users.
- If many users in a dense area all have active statuses, the map may become visually noisy.
- Users may forget to clear statuses, leading to stale or misleading information persisting beyond the intended duration.
  
Ethical Concerns:
- A specific status like "At Starbucks on Central Ave — come find me!" combined with live location significantly reduces a user's anonymity relative to the default ± 100 m baseline. The system should display a nudge warning when a status appears to contain a precise address.

#### Feature 8: Friend Requests & Friend Activity
Description: Users can add each other as friends to gain location visibility and see prioritized friend activity in a feed.

Pros:
- Provides a natural path from a one-off map encounter to an ongoing social connection.
- Privacy-first: location is off by default to non-friends, aligning with user expectations.
- The Friend Activity feed creates a lightweight social layer on top of the map experience without requiring a full social network.
  
Cons:
- A friend request system can be abused to send unsolicited requests at scale (spam).
- The tiered friend system (Close Friends vs. Friends) adds UI complexity that may confuse users.
  
Ethical Concerns:
- Users should be able to remove friends and revoke location access instantly and this should be prominently communicated.
- The Friend Activity feed aggregates behavioral data (RSVPs, statuses, pins) about friends. Users should have clear controls over what they broadcast to their own feed.

## **Use Cases**

### **Use Case 1: Discovering Nearby Users by Interest Tag (FR-TAGS + FR-MAP)**

**Actor:** Registered, verified user Kenji. Active tags: `#Basketball`.

**Preconditions:** Kenji is logged in, location sharing is enabled, proximity range is set to 5 miles.

**Basic Flow:**

1. Kenji opens MapMates. The map loads centered on his GPS location.

2. The system queries for all verified users with `#Basketball` active within 5 miles who are confirmed friends of Kenji or have enabled broader visibility.

3. Two avatar pins appear on the map.

4. Kenji taps one pin. A profile card appears: "Marcus — #Basketball, #Fitness — Currently: 'Shooting around at Aldrich Park.'"

5. Kenji taps "View Full Profile." Marcus's bio and Instagram handle are visible because they are confirmed friends.

6. Kenji taps the Instagram handle and messages Marcus to join him.

**Alternative Flow (No Matches in Range):**

1. No pins appear within 5 miles.

2. Kenji navigates to Settings → Distance Range and increases his range to 15 miles.

3. One new pin appears. Kenji taps it and views the profile.

**Exceptional Flow (Location Permission Denied):**

1. On first launch, the system requests location permission. Kenji denies it.

2. The map displays a locked state with an overlay: "MapMates needs your location to show nearby users. Enable it in iPhone Settings → Privacy → Location Services."

3. No pins are rendered until permission is granted.

***


### **Use Case 2: Setting Up a Bio and Contact Info (FR-PROFILE)**

**Actor:** New user Maya, who has just passed account verification.

**Preconditions:** Maya's account is verified. She has not yet completed her profile.

**Basic Flow:**

1. After verification, the system prompts: "Set up your profile to start meeting people."

2. Maya enters display name "Maya K," writes bio "Urban sketcher and cold brew enthusiast," and selects tags `#UrbanSketching` and `#Coffee`.

3. Maya adds her Instagram handle `@maya.sketches` and leaves all other contact fields blank.

4. Maya saves. Her pin becomes visible on the maps of friends and users with matching tags within their range.

5. A nearby confirmed friend with `#UrbanSketching` taps Maya's pin and can see her Instagram handle on the full profile.

**Alternative Flow (User Skips All Contact Fields):**

1. Maya completes the display name, bio, and tags, but leaves all contact fields blank.

2. Profile saves successfully. Other users see her name, tags, and bio only.

**Exceptional Flow (Bio Over Character Limit):**

1. Maya types 340 characters in the bio field.

2. A live character counter shows "340/300" in red. The Save button is disabled.

3. Maya shortens her bio to 295 characters. The counter turns green and Save becomes active.

***


### **Use Case 3: Creating an Interest Pin for a Group Skate Session (FR-PINS)**

**Actor:** Verified user DeShawn. Active tag: `#Skateboarding`.

**Preconditions:** DeShawn has fewer than 5 active Interest Pins.

**Basic Flow:**

1. DeShawn long-presses on the Culver Skate Park location on the map.

2. The "Create Pin" form opens pre-populated with the tapped coordinates.

3. DeShawn fills in: Title "Sunday Sesh @ Culver," tag `#Skateboarding`, date/time "Sunday 3:00 PM," description "All levels welcome. Bring water!" He uploads a photo of the skate park entrance.

4. DeShawn submits. The pin appears as an event marker on all `#Skateboarding` users' maps.

5. User Aaliyah sees the pin, taps it, reads the details, and RSVPs "Going."

6. DeShawn receives a push notification: "Aaliyah is going to Sunday Sesh @ Culver."

**Alternative Flow (Past Date Selected):**

1. DeShawn accidentally sets the date to yesterday.

2. The system shows an inline validation error: "Event time must be in the future." The Submit button is disabled until the date is corrected.

**Exceptional Flow (5-Pin Cap Reached):**

1. DeShawn tries to create a new pin but already has 5 active.

2. The system shows: "You've reached the 5-pin limit. Delete an existing pin to create a new one." DeShawn is navigated to his pin management screen.

***


### **Use Case 4: Browsing the Interest Directory (FR-PINS — Directory)**

**Actor:** Verified user Sofia, new to the city.

**Preconditions:** Sofia is logged in, location sharing enabled.

**Basic Flow:**

1. Sofia taps the "Directory" tab at the bottom of the screen.

2. The directory loads showing active Interest Pins and the "Active Interests Nearby" section within 5 miles. Top entries: `#Hiking` (9 active users), `#BoardGames` (6 active users).

3. Sofia taps `#BoardGames`. A detail screen shows two upcoming pins and 6 active users.

4. Sofia taps "Add to My Tags." `#BoardGames` is added to her active tag list.

5. Sofia's map now shows users and pins for `#BoardGames`.

**Alternative Flow (Keyword Search):**

1. Sofia types "music" into the directory search bar.

2. Results show: `#LiveMusic` (2 pins this week, 4 active users), `#JamSession` (1 active user).

3. Sofia adds `#LiveMusic` to her tags.

**Exceptional Flow (No Results in Range):**

1. Sofia is in a low-density area. The directory shows: "No active interests or events found within 5 miles. Try expanding your search area."

2. Sofia taps "Expand to 25 miles" and sees results populate.

***


### **Use Case 5: Adjusting Distance Range (FR-RANGE)**

**Actor:** Verified user Tomás.

**Preconditions:** Tomás is logged in. Current global range: 5 miles.

**Basic Flow:**

1. Tomás taps the settings icon → "Distance Range."

2. A range slider is displayed from 2 to 50 miles, currently at 5.

3. Tomás drags the slider to 12 miles and sees a visual map overlay of the new radius.

4. Tomás taps "Save." The map immediately re-queries and displays 3 additional pins.

5. Tomás receives a notification: "Priya (#Soccer) is within your range."

**Alternative Flow (Notifications Disabled):**

1. Tomás sets range to 12 miles but has disabled push notifications in iPhone settings.

2. No notification fires. Tomás still sees new pins on the map when he opens the app.

**Exceptional Flow (Value Below Minimum):**

1. Tomás manually enters "1" into a text input for range.

2. The system shows: "Minimum range is 2 miles." The Save button remains disabled until a valid value is entered.

***


### **Use Case 6: Completing Account Verification (FR-VERIFY)**

**Actor:** New user Priya, just finished registration.

**Preconditions:** Priya has created an account with email and password.

**Basic Flow:**

1. The app displays: "Almost there — let's verify your account. This keeps MapMates safe for everyone."

2. **Step 1 — Liveness Check:** Priya grants camera permission. The front camera activates with an on-screen guide. Priya slowly turns her head as instructed. A 4-second clip is captured and sent to the verification API.

3. The API returns a passing liveness score.

4. **Step 2 — Age Verification:** Priya is prompted to photograph her driver's license. The ID-parsing API extracts her date of birth and confirms she is 18.

5. Both checks pass. Priya's account is marked Verified. A shield badge is added to her profile.

6. Priya is directed to complete her profile setup.

**Alternative Flow (Poor Lighting During Liveness Check):**

1. The liveness API returns a low-confidence score due to poor lighting.

2. The app prompts: "Verification unsuccessful. Try again in a well-lit area, facing forward."

3. Priya moves to better lighting and retries successfully.

**Exceptional Flow (Three Consecutive Failures):**

1. Priya fails the liveness check three times due to a faulty front camera.

2. The system displays: "We were unable to verify your account. Please contact support at support\@mapmates.app for help."

3. The account enters a locked state; Priya cannot appear on other users' maps until support resolves the issue.

***


### **Use Case 7: Setting a Current Status (FR-STATUS)**

**Actor:** Verified user Lena. Active tag: `#Yoga`.

**Preconditions:** Lena is logged in with location sharing enabled.

**Basic Flow:**

1. Lena taps the status icon on the main map screen. A prompt appears: "What are you up to right now?"

2. Lena types: "Morning flow at Aldrich Park — all levels welcome!" and selects a 4-hour expiry.

3. Lena taps "Set Status." Her map pin begins pulsing.

4. A nearby confirmed friend with `#Yoga` within their range taps Lena's pulsing pin, reads the status, and decides to head to the park.

5. After 4 hours, the system automatically clears the status and the pulsing animation stops.

**Alternative Flow (Linking Status to an Interest Pin):**

1. Lena has an existing Pin: "Saturday Sunrise Yoga @ Aldrich Park."

2. While setting her status, she taps "Link to a Pin" and selects that pin.

3. Her status card now includes a "View Event →" button that opens the pin detail.

**Exceptional Flow (Status Text Too Long):**

1. Lena types 115 characters into the status field.

2. The character counter shows "115/100" in red. The Set Status button is disabled.

3. Lena trims her message to 98 characters. The counter turns green and the button activates.

***


### **Use Case 8: Sending and Managing a Friend Request (FR-FRIENDS)**

**Actor:** Verified user Carlos, who met user Jess at a skate park event pin.

**Preconditions:** Both Carlos and Jess are verified users. They are not yet friends.

**Basic Flow:**

1. Carlos taps Jess's map pin → "View Full Profile."

2. On Jess's profile, Carlos taps "Add Friend." A friend request is sent.

3. Jess receives a push notification: "Carlos sent you a friend request."

4. Jess opens the Friends tab, reviews Carlos's profile, and taps "Accept."

5. Carlos receives a notification: "Jess accepted your friend request."

6. Carlos's map now shows Jess's location pin (within Jess's default friend range setting).

7. In the Friend Activity feed, Carlos sees Jess's latest status and upcoming RSVP.

**Alternative Flow (Request Declined):**

1. Jess taps "Decline" on Carlos's request.

2. No notification is sent to Carlos. The request disappears from both inboxes.

3. Carlos's map does not show Jess's location.

**Exceptional Flow (User Blocks Another):**

1. A different user repeatedly sends Carlos unwanted friend requests.

2. Carlos visits that user's profile and taps "Block."

3. The blocked user's pin disappears from Carlos's map immediately.

4. The blocked user can no longer view Carlos's profile or send requests.

5. The block is silent — the blocked user receives no notification.
