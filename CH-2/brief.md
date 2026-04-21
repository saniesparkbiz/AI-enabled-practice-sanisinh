# Brief

When a user receives a meeting invite and clicks to view it, they land on the Google Calendar invite detail page. This page shows the meeting details and accept or decline buttons but gives the user no sense of how their day already looks. We want to add a small indicator on this page that shows how busy or free the user is on the day of the invite — so they can make an informed decision without having to go back and scan their calendar manually.

# Assumptions

- This feature will available to everyone
- We will show the indicator on the Google Calendar invite detail page only
- We will calculate availability for the full day of the invite, not just the time around the meeting
- Only confirmed events will be counted as busy
- We will only look at the user's primary calendar
- Free time will be calculated within the user's set working hours
- The user cannot take any action on their existing events from this indicator
- This feature has nothing to do with the meeting description written by the organiser
