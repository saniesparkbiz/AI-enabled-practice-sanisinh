# Implementation Outline

I would divide this work into three parts

**Part 1 - Frontend Work**

- On the Google Calendar invite detail page, add a small indicator box that shows how busy or free the user is on that day. The invite detail page component should be somewhere around the invite view folder in the frontend codebase.
- The indicator should sit near the top of the page, above the accept and decline buttons so the user sees it before making a decision.
- When the user hovers or taps on this indicator, show a small popup that lists all the existing events for that day with their time slots so the user can see exactly what is already booked.
- The popup should close when the user clicks or taps outside of it.
- Make sure the design of this indicator and popup matches the existing Google Calendar styling.
- Make sure both the indicator and the popup look clean on mobile view as well since many users open invites on their phone.

**Part 2 - Backend Work**

- Add a new GET route in the calendar backend controller that accepts the invite date and the user id and returns the availability summary for that day.
- In this route write the business logic to fetch all confirmed events for that day from the user's primary calendar and calculate the total free time within working hours.
- Make sure the route handles the case where the invite date is far in the future and the calendar has no events yet.

**Part 3 - Integration and Verification**

- Connect the frontend indicator box and the popup to the new backend route so both show real data when the invite page loads.
- Write end to end test cases to verify that the indicator shows correct data for a busy day, a free day and a day with a direct conflict.
- Also write a test case to verify that the popup opens correctly and shows the right list of events for that day.
- Write unit test cases on the backend to verify the free time calculation logic covers all edge cases like all day events, tentative events and missing working hours.
