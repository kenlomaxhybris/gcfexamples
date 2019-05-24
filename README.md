# Material for a Google Cloud Functions Workshop

terminal> git clone https://github.com/kenlomaxhybris/gcfexamples.git


## node101

terminal> cd gcfexamples/node101

node js0
node js1
node js2
node js3
node js4
node js5
node eventloopexample
node promise1

debugging helloWorld locally:
  node --inspect index.js
  chrome://inspect
  curl "http://localhost:8080?name=TheresaMay"
  

## Google Cloud Functions example
terminal> cd gcfexamples/gcfexample
terminal> npm install express @google-cloud/debug-agent @google-cloud/storage @google-cloud/vision @google-cloud/speech @google-cloud/translate @google-cloud/text-to-speech

To execute google APIs you need to have "permission", which means a serviceaccount key.
Chrome> https://console.cloud.google.com/iam-admin/serviceaccounts

Download the json file and set your GOOGLE_APPLICATION_CREDENTIALS to it:

terminal> export GOOGLE_APPLICATION_CREDENTIALS=pathToJSONAPIKey 

You can now run google api from your laptop:

terminal> node debugging.js
or
terminal> node --inspect debugging.js
chrome://inspect

curl "http://localhost:8080/helloWorld?file=TheresaMay"

curl "http://localhost:8080/gcfs?bucketin=gcfinput&bucketout=gcfoutput&targetLocale=fr&file=input.txt&gender=MALE&sourceLocale=en-US"

To test in GC: {"bucketin":"gcfinput", "bucketout":"gcfoutput","targetLocale":"fr", "file":"input.txt"}

StackDriver
  Checkin code
  Set snapshot points
  Invoke from Testing tab 
  
