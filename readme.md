# Concept
1. User identifies object (e.g. with picture or description).
2. Agent adopts identity of that object.
3. User can then have a speech conversation with agent.

Easy-peasy!

### Design parameters
* Character
* Voice

### Performance measures
* Transcription accuracy and latency
* Character quality, voice quality, voice latency
* Ability to interrupt character mid-sentence
* Application portability (e.g. can it only run on my laptop, can I use it on mobile)

### System design

Streams:
* All streams permanently exist in parallel (no creation/destruction)
1. Input audio stream
2. This is transcribed to input text stream
3. Input text stream is mapped to character output text stream
4. Output text stream is mapped to output audio stream

v0.1 (fixed character, no voice)
* Pre-defined object, an granny's china teapot.
* Text interaction with object (i.e. no character voice stream).
* Python script running inside container.

v0.11 (fixed character, fixed voice)
* Still the granny's china teapot.
* Speech interaction with object using Coqui's streaming models (no voice tuning).
* Still a Python script running inside a container.

v0.111 (custom character, fixed voice)
* User can describe the object via text or speech input.
* Still a fixed voice.
