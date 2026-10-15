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
5G network slicing allows a telecom operator to create separate virtual networks on shared physical infrastructure. Each slice can be designed for different service needs. For example, a slice for emergency responders could be configured to support their communication needs during busy periods. This can help manage network traffic, but it does not guarantee that the service will never fail. The operator still needs to monitor network performance and prepare for outages.

Resource: 5G System Overview - https://www.3gpp.org/technologies/5g-system-overview
## Cybersecurity
When a cyberattack threatens a 5G service, the operator needs to detect the incident, assess its impact, and contain the threat. The security team should follow an incident response plan and inform the appropriate people. After controlling the attack, the team should restore affected services safely and investigate what happened. Reviewing the incident can help the operator improve its security measures and reduce the chance of similar problems in the future.

Resource: Incident Response Recommendations and Considerations for Cybersecurity Risk Management: A CSF 2.0 Community Profile - https://csrc.nist.gov/pubs/sp/800/61/r3/final
## Data
A telecom operator can use a star schema to organize network usage data. The fact table can store measurements, such as data usage and dropped calls. Dimension tables can describe details such as the date, region, and service type. This structure helps the operator compare network performance across different regions and days. By analyzing the data, the operator can identify usage patterns and find areas where service quality may need improvement.

Resource: Dimensional modeling in Microsoft Fabric Warehouse - https://learn.microsoft.com/en-us/fabric/data-warehouse/dimensional-modeling-overview
## Misconception in My Track
A common misconception is that cybersecurity only means using antivirus software and strong passwords. In reality, cybersecurity also includes monitoring systems, controlling access, preparing for attacks, and responding to security incidents. For example, a 5G operator may have security tools, but an attacker could still find a weakness in the network. The operator needs to detect suspicious activity, contain the threat, and restore services safely. This shows that cybersecurity is not only about preventing attacks. It also involves preparing for incidents and reducing their impact when they happen.

Resource: Incident Response Recommendations and Considerations for Cybersecurity Risk Management: A CSF 2.0 Community Profile - https://csrc.nist.gov/pubs/sp/800/61/r3/final
## Open Question
How can a telecom operator make sure its 5G service stays available for emergency responders during a serious cyberattack, especially if the attack affects the network systems used to detect and stop it?
