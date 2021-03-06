# JSON_Schema--Project

# What is a JSON schema
JSON Schema is a vocabulary that allows you to annotate and validate JSON documents.
it defines the structure of a JSON message, can be used to validate a JSON message or API request and response in JSON format.

# Benefits
1. Describes your existing data format(s).
2. Provides clear human- and machine- readable documentation.
3. Validates data which is useful for:
         1. Automated testing.
         2. Ensuring quality of client submitted data.

# Briefing 
This is a generic program that:
- Reads a JSON file similar to what's present in this location (./data/)
- Sniffs the schema of the JSON file 
- Dumps the output in (./schema/)
# Additional informations for test cases
- - Padding: All attributes in the JSON schema should be padded with "tag" and "description" keys
- The schema output must capture ONLY the attributes within the "message" key of the input JSON source data (see line 8 in the input JSON files). All attributes withn the key "attributes" should be excluded
- The JSON schema should set all properties "required": false
- For data types of the JSON schema:
STRING: program should identify what is a string and map accordingly in JSON schema output
INTEGER: program should identify what is an integer and map accordingly in JSON schema output
ENUM: When the value in an array is a string, the program should map the data type as an ENUM 
ARRAY: When the value in an array is another JSON object, the program should map the data type as an ARRAY 

# Coding Environment
 Visual Studio Code

# Dependencies
json, 
collections, 
unittest, 
sys, 
os

# Example
From the json data in data_2.json, the data structure is shown.
```json
{
    "attributes": {
      "appName": "ABCDEFGHIJKLMNOPQRSTUVW",
      "eventType": "ABCDEFGHIJKLMNOPQRSTUVWXYZ",
      "subEventType": "ABCDEFGHIJKLMNO",
      "sensitive": false
    },
    "message": {
      "user": {
        "id": "ABCDEFGHIJKLMNOP",
        "nickname": "ABCD",
        "title": "ABCDEFGHIJKLMNOPQRSTUVWXYZABC",
        "accountType": "ABCDEFGHIJKLMNOPQRSTUVWX",
        "countryCode": "ABCDEFGHIJKLMNOPQRSTUVWX",
        "orientation": "ABCDEFGHIJKLMNOPQRSTU"
      },
      "time": 890,
      "acl": [],
      "publicFeed": false,
      "internationalCountries":
      [
        "ABCDEFGHIJKLMNOPQRSTUVWXYZA",
        "ABCDEFGHIJKLMNOPQ",
        "ABCDEFGHIJKLMNOPQRSTUVW",
        "ABCDEFGHIJKLMNOPQRSTUVWXY",
        "ABCDEFGHIJK",
        "ABCDEFGHIJKLMNOPQRSTUVWXYZ",
        "ABCDEFGHIJKLMNOPQR",
        "ABCDEFG",
        "ABCDEFGHIJKLM"
      ],
      "topTraderFeed": true
    }
  }
  
  
  
{
  "Id": 1,
  "_comment": "Expected output, generates a json schema as shown below:"
}
  
  
  
      {
    "battle": {
        "id": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "name": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "orientation": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "settings": {
            "minParticipants": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "integer"
            },
            "maxParticipants": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "integer"
            },
            "battleType": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "string"
            },
            "wagerType": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "string"
            },
            "countdown": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "integer"
            },
            "duration": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "integer"
            },
            "archetype": {
                "name": {
                    "tag": "",
                    "description": "",
                    "required": false,
                    "type": "string"
                },
                "iconId": {
                    "tag": "",
                    "description": "",
                    "required": false,
                    "type": "string"
                }
            }
        },
        "status": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "creationTime": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "integer"
        },
        "startTime": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "integer"
        },
        "endTime": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "integer"
        },
        "creator": {
            "id": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "string"
            },
            "nickname": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "string"
            },
            "title": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "string"
            },
            "accountType": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "string"
            },
            "countryCode": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "string"
            },
            "orientation": {
                "tag": "",
                "description": "",
                "required": false,
                "type": "string"
            }
        },
        "participants": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "array"
        }
    },
    "joiner": {
        "id": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "nickname": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "title": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "accountType": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "countryCode": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "orientation": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        }
    },
    "participantIds": {
        "tag": "",
        "description": "",
        "required": false,
        "type": "enum"
    },
    "user": {
        "id": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "nickname": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "title": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "accountType": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "countryCode": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        },
        "orientation": {
            "tag": "",
            "description": "",
            "required": false,
            "type": "string"
        }
    },
    "time": {
        "tag": "",
        "description": "",
        "required": false,
        "type": "integer"
    },
    "acl": {
        "tag": "",
        "description": "",
        "required": false,
        "type": "enum"
    },
    "publicFeed": {
        "tag": "",
        "description": "",
        "required": false,
        "type": "integer"
    },
    "internationalCountries": {
        "tag": "",
        "description": "",
        "required": false,
        "type": "enum"
    },
    "topTraderFeed": {
        "tag": "",
        "description": "",
        "required": false,
        "type": "integer"
    }
}
