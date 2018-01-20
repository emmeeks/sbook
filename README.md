# sbook

instructions on how to run the speech to text api on gcloud

in iterm
  gcloud init
  follow the prompts to log-in to your project
  export API_KEY=<YOUR_API_KEY>
    
  curl -s -X POST -H "Content-Type: application/json" --data-binary @request.json \
"https://speech.googleapis.com/v1/speech:longrunningrecognize?key=${API_KEY}"

this returns your name #

now all you do is GET it

curl -s -k -H "Content-Type: application/json" \
    -H "Authorization: Bearer {access_token}" \
    https://speech.googleapis.com/v1/operations/{name}
    
reference: https://cloud.google.com/speech/docs/auth

