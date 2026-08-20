{
  "$schema": "https://schemas.botframework.com/schemas/skills/v2.1/skill-manifest.json",
  "$id": "SampleEchoSkill",
  "name": "Echo Skill",
  "version": "1.0.0",
  "description": "A skill that echoes back whatever the user says, useful for testing Copilot connectivity.",
  "publisherName": "Contoso Dev Team",
  "msaAppId": "00000000-0000-0000-0000-000000000000",
  "endpoint": "https://azurewebsites.net",
  "activities": {
    "message": {
      "type": "message",
      "description": "Receives text from the user and replies with an exact echo."
    }
  },
  "definitions": {
    "echoUtterances": {
      "type": "object",
      "properties": {
        "text": {
          "type": "string",
          "description": "The message text to echo back."
        }
      }
    }
  },
  "dispatchModels": {
    "intents": [
      {
        "id": "EchoIntent",
        "description": "Triggers when the user asks to repeat, echo, or mimic text.",
        "utterances": [
          "echo this please",
          "repeat after me",
          "say hello world",
          "test the connection"
        ]
      }
    ]
  }
}
