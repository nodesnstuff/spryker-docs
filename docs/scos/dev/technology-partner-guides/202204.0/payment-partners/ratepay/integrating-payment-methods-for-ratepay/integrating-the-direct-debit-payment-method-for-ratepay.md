---
title: Integrating the Direct Debit payment method for RatePay
description: Integrate direct debit payment through Ratepay into the Spryker-based shop.
last_updated: Jun 16, 2021
template: concept-topic-template
originalLink: https://documentation.spryker.com/2021080/docs/ratepay-direct-debit
originalArticleId: 5b1a8407-02f1-418e-9f69-98643224753c
redirect_from:
  - /2021080/docs/ratepay-direct-debit
  - /2021080/docs/en/ratepay-direct-debit
  - /docs/ratepay-direct-debit
  - /docs/en/ratepay-direct-debit
  - /docs/scos/dev/technology-partner-guides/202200.0/payment-partners/ratepay/integrating-payment-methods-for-ratepay/integrating-the-direct-debit-payment-method-for-ratepay.html
  - /docs/scos/user/technology-partners/202204.0/payment-partners/ratepay/integrating-payment-methods-for-ratepay/integrating-the-direct-debit-payment-method-for-ratepay.html
related:
  - title: RatePay
    link: docs/scos/user/technology-partners/page.version/payment-partners/ratepay.html
  - title: RatePay - Payment Workflow
    link: docs/scos/dev/technology-partner-guides/page.version/payment-partners/ratepay/ratepay-payment-workflow.html
  - title: RatePay facade methods
    link: docs/scos/dev/technology-partner-guides/page.version/payment-partners/ratepay/ratepay-facade-methods.html
  - title: Disabling address updates from the backend application for RatePay
    link: docs/scos/dev/technology-partner-guides/page.version/payment-partners/ratepay/disabling-address-updates-from-the-backend-application-for-ratepay.html
  - title: Integrating the Invoice payment method for RatePay
    link: docs/scos/dev/technology-partner-guides/page.version/payment-partners/ratepay/integrating-payment-methods-for-ratepay//integrating-the-invoice-payment-method-for-ratepay.html
  - title: RatePay- Core Module Structure Diagram
    link: docs/scos/dev/technology-partner-guides/page.version/payment-partners/ratepay/ratepay-core-module-structure-diagram.html
  - title: Integrating the Installment payment method for RatePay
    link: docs/scos/dev/technology-partner-guides/page.version/payment-partners/ratepay/integrating-payment-methods-for-ratepay//integrating-the-installment-payment-method-for-ratepay.html
  - title: Integrating the Prepayment payment method for RatePay
    link: docs/scos/dev/technology-partner-guides/page.version/payment-partners/ratepay/integrating-payment-methods-for-ratepay//integrating-the-prepayment-payment-method-for-ratepay.html
  - title: RatePay - State Machine Commands and Conditions
    link: docs/scos/dev/technology-partner-guides/page.version/payment-partners/ratepay/ratepay-state-machine-commands-and-conditions.html
---

## Workflow Scenarios


### Payment Flow

![Click Me](https://spryker.s3.eu-central-1.amazonaws.com/docs/Technology+Partners/Payment+Partners/Ratepay/ratepay-ddelv-payment-flow.png)

### Cancellation Flow

![Click Me](https://spryker.s3.eu-central-1.amazonaws.com/docs/Technology+Partners/Payment+Partners/Ratepay/ratepay-ddelv-payment-flow.png)

### Partial Cancellation Flow

![Click Me](https://spryker.s3.eu-central-1.amazonaws.com/docs/Technology+Partners/Payment+Partners/Ratepay/ratepay-ddelv-partial-cancellation-flow.png)

### Refund Flow

![Click Me](https://spryker.s3.eu-central-1.amazonaws.com/docs/Technology+Partners/Payment+Partners/Ratepay/ratepay-ddelv-refund-flow.png)

## Integrating Direct Debit

**Direct Debit Payment**—in order to integrate direct debit payment, two simple steps are needed: set RatePAY Direct Debit payment configuration and call the facade functions.

### Set RatePay Direct Debit Configuration

The configuration to integrate Direct Debit payments using RatePAY is:
* `PROFILE_ID`: merchant's login (required).
* `SECURITY_CODE`: merchant's password (required).
* `SHOP_ID`: shop identifier (required).
* `SYSTEM_ID`: system identifier (required).
* `CLIENT_VERSION`: client system version.
* `CLIENT_NAME`: client name.
* `RATEPAY_REQUEST_VERSION`: request version.
* `RATEPAY_REQUEST_XMLNS_URN`: request XMLNS urn.
* `MODE`: the mode of the transaction, either test or live (required).
* `API_TEST_URL`: test mode API url.
* `API_LIVE_URL`: live mode API url.
* `DEBIT_PAY_TYPES`: debit pay types, can be DIRECT-DEBIT or BANK-TRANSFER.

## Performing Requests

In order to perform the needed requests, you can easily use the implemented state machine commands and conditions. The [RatePAY State Machine Commands and Conditions](/docs/scos/dev/technology-partner-guides/{{page.version}}/payment-partners/ratepay/ratepay-state-machine-commands-and-conditions.html) section gives a summary of them. You can also use the facade methods directly which, however, are invoked by the state machine.
