# BirdIdentifier Backend

An ASP.NET Web API that uses machine learning (ML.NET) to identify bird species from images.

## Features

- **Bird Classification** - Identify bird species from uploaded images with confidence scores
- **Bird Persona** - Match people or objects to bird species for fun personality insights

## Main Endpoints
`POST /birds/identification/classify?version=X`

Identifies bird species in uploaded images. Returns the species name, confidence score, and a link to learn more. Rejects the request if the image is determined to not be a bird.

`POST /birds/identification/persona?version=X`

Matches any image (person, object, etc.) to the bird species it most closely resembles.

Both endpoints accept JPG/PNG images and support optional version parameter (1 or 2) to select the ML model.
### Example Response:
``` json
{
  "Name": "northern-cardinal",
  "Timestamp": "2025-12-18T10:30:00",
  "Score": 95.43,
  "LearnMoreLink": "https://www.google.com/search?q=northern+cardinal+bird"
}
```
## API Documentation

Complete API documentation with code samples in multiple languages:
- **[Interactive Docs](BirdIdentifierBackend.md)** - Full endpoint reference
- **[OpenAPI Spec](BirdIdentifierBackend/BirdIdentifierBackend.json)** - Machine-readable specification

## Getting Started

### Prerequisites
- .NET 10.0 SDK

### Running Locally

```bash
git clone https://github.com/adamgate/BirdIdentifierBackend.git
cd BirdIdentifierBackend
dotnet run --project BirdIdentifierBackend
```
