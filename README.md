# Address Comparison API with Gemini

This Next.js application provides an API and user interface for comparing two addresses to determine if they refer to the same physical location. It uses Google's Gemini AI model to analyze the addresses and provide a match result with confidence level.

## Features

- API endpoint for address comparison
- User-friendly interface for entering and comparing addresses
- Detailed results including match status, confidence level, and explanation
- Input validation and error handling

## Setup

1. Clone the repository
2. Install dependencies:
   ```
   npm install
   ```
3. Create a `.env.local` file in the root directory with your Gemini API key:
   ```
   GEMINI_API_KEY=your_gemini_api_key_here
   ```
4. Run the development server:
   ```
   npm run dev
   ```

## API Usage

### Endpoint

```
POST /api/compare-addresses
```

### Request Body

```json
{
  "address1": "123 Main St, Anytown, CA 12345",
  "address2": "123 Main Street, Anytown, California 12345"
}
```

### Response

```json
{
  "match": true,
  "confidence": 0.95,
  "explanation": "Both addresses refer to the same location. The only difference is the abbreviation of 'Street' to 'St' and spelling out 'California' vs using the abbreviation 'CA'."
}
```

## How It Works

The application uses Google's Gemini AI model to analyze and compare the addresses. The model considers various factors such as:

- Variations in formatting
- Abbreviations
- Missing apartment/unit numbers
- Typos and other common differences in address notation

The result includes:
- `match`: Boolean indicating if the addresses likely refer to the same location
- `confidence`: Number between 0 and 1 indicating the confidence level
- `explanation`: Brief explanation of the reasoning behind the result

## Technologies Used

- Next.js
- React
- Google Generative AI (Gemini)
- Tailwind CSS
- shadcn/ui components#   A d d r e s s C o m p a r a t o r G e m i n i  
 