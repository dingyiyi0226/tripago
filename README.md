# TripAgo

Trip-Ago, an album platform to record and share your trips.

## Environment

+ Frontend: ReactJS
+ Backend: NodeJS
+ Database: Cloud Firestore

## Development

### Prerequisites

Make sure the prerequisites are installed

+ yarn

### Backend

Install and run backend server
```bash
> cd Tripago/backend
> yarn
> yarn server
```
To connect to Firestore database and access Google APIs, ```.env``` is needed at ```Tripago/backend```:

``` bash
### Tripago/backend/.env

## Required for local server to access cloud storage.
## The cloud_storage_key.json is generated by Google when client applies for an access to cloud storage
GOOGLE_APPLICATION_CREDENTIALS=cloud_storage_key.json

## Name of the project on Google Cloud Platform
GOOGLE_CLOUD_PROJECT=[PROJECT_NAME]

## Name of the storage bucket on Google Cloud Platform
GCLOUD_STORAGE_BUCKET=[STORAGE_BUCKET_NAME]

## Google API key (for Google Maps)
GOOGLE_API_KEY=[API_KEY]
```

### Frontend

Install dependency and start web service

```bash
> cd Tripago/frontend
> yarn # or npm install
> yarn start
```

To connect to server, ```.env.production```(local website) or ```.env.development```(deployed website) are needed at ```Tripago/frontend```:

``` bash
### Tripago/backend/.env.production or Tripago/backend/.env.development
## Un-comment one of the following configurations for local/cloud server.

## Cloud server
# REACT_APP_BACKEND_URL=[SERVER_PATH] 

## Local server
# REACT_APP_BACKEND_URL=''
```
## Product
The website is deployed online [here](https://dingyiyi0226.github.io/tripago).

For Safari users, the website may not function normally due to cookie policies. Please go to Preference (⌘,) -> Privacy, and uncheck "prevent cross-site tracking" to allow cookies to work normally. Cookies are only used to record users' login status.


