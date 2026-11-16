# Where call transcripts live

Read this when you write a scheduled check's prompt (where to look) and when you run one (how to find this call).

Start from the tools you actually have: a connector or MCP server for the user's meeting app or notetaker beats anything below. Find the call by its time (a meeting that started within 30 minutes of the booked time) and by the other person (in the title, the attendees or the speaker names). If 2 transcripts could fit, don't pick one; ask.

## Meeting apps

- **Google Meet.** When transcription is turned on, Meet saves the transcript as a Google Doc in the organizer's Google Drive, in a folder called "Meet Recordings", and usually attaches it to the calendar event. Reach it with a Google Drive or Calendar connector. If the user wasn't the organizer, it sits in the organizer's Drive and may only be shared with them.
- **Zoom.** Only cloud recordings get a transcript, and only when audio transcripts are turned on for the account. It's saved with the recording as a VTT file. Reach it with a Zoom connector or Zoom's cloud recordings API, or the user can download it from the Zoom web portal under Recordings. Local recordings have no transcript.
- **Microsoft Teams.** When transcription was on, the transcript is attached to the meeting, in its chat and its recap, and can be downloaded from there. Reach it with a Microsoft 365 connector.

## Notetaker apps

Granola, Otter, Fireflies, Fathom, Grain, tl;dv, Read.ai and similar apps keep transcripts in their own app, and many offer an MCP server, an API or an integration. Use it if it's connected. Some also email a recap after each call with a link to the transcript; with an email connector, search for that email.

## Files on the computer

Some notetakers keep transcripts on the computer, and some people save transcript files (VTT, SRT or TXT) to a folder. A scheduled check that runs on the same computer can read them; one that runs in the cloud can't. Ask once which folder, and put its full path in the prompt.

## When nothing is reachable

Schedule the check to suggest the review instead (step 4 of the template), and name where the user will find the transcript to share: Zoom's web portal under Recordings, the Google Doc in Drive's "Meet Recordings" folder, or the Teams meeting's chat.
