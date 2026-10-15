# Nafath Discovery Mission Brief

Version: NAFATH-V2

Track: Cybersecurity 

## Overview
A reliable 5G service for emergency responders needs different IT fields to work together. Software should handle repeated requests correctly to avoid creating duplicate incident records. AI can help predict network congestion, but its results need to be tested to make sure they work well with new data. Mobile apps should allow responders to access saved information and record updates when there is no internet connection. Networking, such as 5G network slicing, can help provide the resources needed for emergency services during busy periods. Cybersecurity is also important because the operator needs to detect attacks, protect important systems, and restore services safely. Data systems help organize network usage by region and day, making it easier to find problems and compare performance. All six fields help make the service more reliable during emergencies. **Incident response is an important cybersecurity topic because it helps the operator manage attacks and restore services.**

## Software
HTTP methods are used to send requests between an app and a server. Some methods, such as GET, are safe because they should not change data on the server. Other methods, such as PUT and DELETE, are idempotent, which means repeating the same request should have the same intended effect. This is important when an emergency responder's app loses connection and retries a request. Repeating a request that is not idempotent may cause duplicate incident records if the system has no protection against duplicates.

Resource: RFC 9110: HTTP Semantics - https://www.rfc-editor.org/rfc/rfc9110.html
## AI
Overfitting happens when an AI model learns the training data too well but does not perform well with new data. Cross-validation helps test how well a model works using different parts of the available data. For example, a telecom company could use AI to predict when its 5G network may become crowded. Testing the model with different data groups can help identify overfitting before the company uses its predictions to support network operations.

Resource: 3.1. Cross-validation: evaluating estimator performance - https://scikit-learn.org/stable/modules/cross_validation.html
## Mobile
An offline-first mobile app can still perform important tasks when the internet connection is weak or unavailable. For example, emergency responders should be able to view saved incident details and record updates when the 5G network is down. The app can save changes on the device and synchronize them when the connection returns. It should also handle conflicting updates carefully so important information is not accidentally lost.

Resource: Build an offline-first app - https://developer.android.com/topic/architecture/data-layer/offline-first
## Networking

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
