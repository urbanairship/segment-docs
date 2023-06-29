## Airship (Actions) Destination

{% include content/plan-grid.md name="actions" %}


[Airship](https://app.segment.com/airship/destinations/catalog/actions-airship) provides an end-to-end solution for capturing value across the entire customer app lifecycle — from acquisition and activation to engagement and loyalty. It starts with Airship’s market-leading app store optimization (ASO) solutions promoting app discovery and downloads. Then our unified journey orchestration, content creation and experimentation solutions kick in. App teams can quickly design, deploy and iterate no-code native app experiences and cross-channel campaigns — bridging inside-the-app experiences with outside-the-app messaging.

This destination is maintained by Airship. For any issues with the destination, [contact their Support team](mailto:support@airship.com).

> success ""
> **Good to know**: This page is about the [Actions-framework](/docs/connections/destinations/actions/) Airship Segment destination. There's also a page about the [non-Actions Airship destination](/docs/connections/destinations/catalog/airship/). Both of these destinations receive data from Segment.

## Benefits of Airship (Actions) vs Airship Classic

Airship (Actions) provides the following benefits over the classic Airship destination:

- **Flexibility**. Complete flexibility for mapping your data from any Segment event type to one of three Airship endpoints. Make optimal use of data from Segment to trigger Automations, for audience segmentation, or to personalize end-users in-app experiences and messages.
- **Reporting**. Better and more meaningful feedback from the Airship API. This integration calls the Airship API directly, so the endpoint response shows precisely how the integration is performing.


## Getting started

1. From the Segment web app, click **Catalog**, then click **Destinations**.
2. Find the Destinations Actions item in the left navigation, and click it.
3. Click **Configure Airship (Actions)**.
4. Select an existing Source to connect to Airship (Actions).
5. Name the destination and choose between filling in the settings manually or copying from an existing instance.
6. Click Create Destination
7. Enter your Access Token and App Key - these can be optained by going to your Airship project and navigating to Settings->Partner Integrations and selecting Segment. Following the instructions there will create a Tag Group, Attributes, and provide the Access Token and App Key.
8. Select the appropriate data center. 

## Additional Information
Out of the box functionality, including some default mappings (all overridable):
1. Custom Events
    * Send signals to Airship to trigger messages or segment audiences
    * Default Event Type is `Track`
    * Custom Event `name` defaults to the `Event` property
    * Airship Named User ID defaults to `userId`
    * Event Occurred defaults to `timestamp`
    * Custom Event `properties` defaults to `properties`
2. Set Attributes
    * Associate properties with a user for personalization or segmentation
    * Default Event Type is `Identify`
    * Airship Named User ID defaults to `userId`
    * Attribute Occurred defaults to `timestamp`
    * There is a long list of mappings for attributes that are common between the platforms
3. Manage Tags
    * Segment audiences based on behavior or traits
    * Airship Named User ID defaults to `userId`
    * Airship Tag Group defaults to `segment-integration` (Don't change this unless you really intend to!)
    * Airship Tag Names defaults to a placeholder object called `traits.airship_tags`. This likely doesn't exist, so either create it or point it to the relevant Tag Name(s) to be set/removed.
    * Tag names must be boolean. True will set the tag for the Named User, False will remove it.

## Named User ID
Named User is an Airship concept for identifying users and associating them with devices and delivery addresses. It's explained in detail (here)[https://docs.airship.com/guides/messaging/user-guide/audience/segmentation/named-users/]. It's important to note that this integration will not perform the association of a Named User to a delivery address - that should be set up in either the mobile/web SDK or through some custom workflow out of band from this integration.

{% include components/actions-fields.html %}

