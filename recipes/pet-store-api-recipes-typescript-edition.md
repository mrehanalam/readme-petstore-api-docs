---
title: 🍲 Pet Store API Recipes – TypeScript Edition
description: Recipe Description
hidden: false
recipe:
  color: '#018FF4'
  icon: 🦉
---
```node Node
const axios = require('axios');

async function listAvailableDogs() {
  const response = await axios.get(`${BASE_URL}/pets?type=dog`, {
    headers: { Authorization: `Bearer ${API_TOKEN}` }
  });
  console.log(response.data);
}

listAvailableDogs();

```

```json Response Example
{"success":true}
```

# Prerequisites

<!-- node@ -->

Install a request library:

Or with node-fetch (v3+ requires ESM):


# API token 

<!-- node@ -->

Set up your API token (replace with your actual token)

# Get Available Dogs (with Axios)

<!-- node@ -->

