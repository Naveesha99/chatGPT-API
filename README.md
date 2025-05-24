# AI Content Generator - Backend

This is the backend for the **AI Content Generator** tool, responsible for handling requests from the frontend and interacting with the OpenAI API to generate text content.

## ⚙️ Tech Stack

- Java 17+
- Spring Boot 3.x
- Spring Web
- OpenAI API (via HTTP requests)
- CORS enabled using `@CrossOrigin("*")` for development

## 🚀 Getting Started

### Prerequisites

- JDK 17+
- Maven

### Installation

```bash
# Clone the repository
git clone https://github.com/Naveesha99/chatGPT-API.git
cd chatGPT-API

# Build the application
./mvnw clean install

# Run the application
./mvnw spring-boot:run
```

### 🔐 Environment Variables

Set your OpenAI API key in an environment variable or application.properties:

```properties
openapi.api.url=https://api.openai.com/v1/chat/completions
openapi.api.model=openai_api_model
openapi.api.key=your_openai_api_key
```

### 📡 API Endpoint

- `POST /api/generate`
  - **Request body:**
    ```json
    {
      "prompt": "Write a formal apology email."
    }
    ```
  - **Response:**
    ```json
    {
      "result": "Dear Sir, I sincerely apologize for..."
    }
    ```

## 🔐 CORS Configuration

CORS is enabled using the `@CrossOrigin("*")` annotation at the controller level:

```java
@CrossOrigin("*") // Allow all origins
@RestController
@RequestMapping("/api/chat")
public class ContentController {
    // ...
}
```

This allows requests from any frontend origin during development.

## 📂 Backend Structure

```
src/main/java/
└── com/example/aicontent/
    ├── config/
    ├── controller/
    ├── dto/
    ├── service/
    └── AiContentApplication.java
```

## 🧠 Powered by

- [OpenAI API](https://platform.openai.com/)

---

Made with ❤️ by [Naveesha](https://github.com/Naveesha99)
