<a id="asyncChatGPT"></a>

# asyncChatGPT

<a id="asyncChatGPT.asyncChatGPT"></a>

# asyncChatGPT.asyncChatGPT

<a id="asyncChatGPT.asyncChatGPT.generate_uuid"></a>

#### generate\_uuid

```python
def generate_uuid() -> str
```

Generates a UUID for the session -- Internal use only

**Returns**:

str

<a id="asyncChatGPT.asyncChatGPT.Chatbot"></a>

## Chatbot Objects

```python
class Chatbot()
```

Initializes the chatbot

See wiki for the configuration json:
https://github.com/acheong08/ChatGPT/wiki/Setup

**Arguments**:

- `config` (`:obj:`json``): The configuration json
- `conversation_id` (`:obj:`str`, optional`): The conversation ID
- `parent_id` (`:obj:`str`, optional`): The parent ID
- `debug` (`:obj:`bool`, optional`): Whether to enable debug mode
- `refresh` (`:obj:`bool`, optional`): Whether to refresh the session

**Returns**:

None or Exception

<a id="asyncChatGPT.asyncChatGPT.Chatbot.reset_chat"></a>

#### reset\_chat

```python
def reset_chat() -> None
```

Resets the conversation ID and parent ID

**Returns**:

None

<a id="asyncChatGPT.asyncChatGPT.Chatbot.refresh_headers"></a>

#### refresh\_headers

```python
def refresh_headers() -> None
```

Refreshes the headers -- Internal use only

**Returns**:

None

<a id="asyncChatGPT.asyncChatGPT.Chatbot.get_chat_stream"></a>

#### get\_chat\_stream

```python
async def get_chat_stream(data) -> None
```

Generator for chat stream -- Internal use only

**Arguments**:

- `data`: The data to send

**Returns**:

None

<a id="asyncChatGPT.asyncChatGPT.Chatbot.get_chat_text"></a>

#### get\_chat\_text

```python
async def get_chat_text(data) -> dict
```

Gets the chat response as text -- Internal use only

**Arguments**:

- `data`: The data to send

**Returns**:

The chat response

<a id="asyncChatGPT.asyncChatGPT.Chatbot.get_chat_response"></a>

#### get\_chat\_response

```python
async def get_chat_response(prompt, output="text") -> dict or None
```

Gets the chat response

**Arguments**:

- `prompt` (`:obj:`str``): The message sent to the chatbot
- `output` (`:obj:`str`, optional`): The output type `text` or `stream`

**Returns**:

`:obj:`dict` or :obj:`None` or :obj:`Exception``: The chat response `{"message": "Returned messages", "conversation_id": "conversation ID", "parent_id": "parent ID"}`

<a id="asyncChatGPT.asyncChatGPT.Chatbot.rollback_conversation"></a>

#### rollback\_conversation

```python
def rollback_conversation() -> None
```

Rollbacks the conversation

**Returns**:

None

<a id="asyncChatGPT.asyncChatGPT.Chatbot.refresh_session"></a>

#### refresh\_session

```python
def refresh_session() -> Exception
```

Refreshes the session

**Returns**:

None or Exception

<a id="asyncChatGPT.asyncChatGPT.Chatbot.login"></a>

#### login

```python
def login(email, password) -> None
```

Logs in to OpenAI

**Arguments**:

- `email` (`:obj:`str``): The email
- `password` (`:obj:`str``): The password

**Returns**:

None
