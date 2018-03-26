# Billing Library with developerPayload support

It's a fork of the Play Billing Library: https://developer.android.com/google/play/billing/billing_library.html

Original: com.android.billingclient:billing:1.0

Original version lacks of the developerPayload support:
   
   https://github.com/googlesamples/android-play-billing/issues/78
   
   https://issuetracker.google.com/issues/63381481
   
   https://stackoverflow.com/questions/46562806/play-billing-library-is-missing-developerpayload
 
In this fork the developerPayload are supported.

```groovy
implementation 'me.drakeet.billing:billing:1.0.1'
```

```java
BillingFlowParams flowParams = BillingFlowParams.newBuilder()
                        .setSku("inapp_1")
                        .setType(SkuType.INAPP)
                        .setDeveloperPayload("your_custom_developer_payload")
                        .build();
int responseCode = billingClient.launchBillingFlow(MainActivity.this, flowParams);
```
