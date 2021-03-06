# GeoFire — Realtime location queries with Firebase

GeoFire is set of open-source libraries for JavaScript, Objective-C, and Java that allow you
to store and query a set of keys based on their geographic location. At its heart, GeoFire
simply stores locations with string keys. Its main benefit, however, is the possibility of
retrieving only those keys within a given geographic area - all in realtime.

GeoFire uses [Firebase](https://www.firebase.com/?utm_source=geofire) for data storage,
allowing query results to be updated in realtime as they change. GeoFire *selectively
loads only the data near certain locations, keeping your applications light and responsive*,
even with extremely large datasets.

## GeoFire Clients

The GeoFire library is available in three different languages:

* [GeoFire for JavaScript](https://github.com/firebase/geofire-js)
* [GeoFire for Objective-C](https://github.com/firebase/geofire-objc)
* [GeoFire for Java](https://github.com/firebase/geofire-java)

All of the clients work on the same underlying data structure and have similar APIs, making
it easy to create a cross-platform app on top of GeoFire.

### Integrating GeoFire with your data

GeoFire is designed as a lightweight add-on to Firebase. To keep things simple, GeoFire stores data
in its own format and its own location within your Firebase. This allows your existing data format
and security rules to remain unchanged while still providing you with an easy solution for geo
queries.

#### Example Usage

Assume you are building an app to rate bars and you store all information for a bar, e.g. name,
business hours and price range, at `/bars/<bar-id>`. Later, you want to add the possibility for
users to search for bars in their vicinity. This is where GeoFire comes in. You can store the
location for each bar using GeoFire, using the bar IDs as GeoFire keys. GeoFire then allows you to
easily query which bar IDs (the keys) are nearby. To display any additional information about the
bars, you can load the information for each bar returned by the query at `/bars/<bar-id>`.

## Live Demo

To see GeoFire in action, you can [play around with our fully-featured JavaScript demo](https://geofire.firebaseapp.com/sfVehicles/index.html).
(Drag the purple circle!) This demo maps all of the San Francisco MUNI vehicles within a certain
search radius. You can drag around the search radius and see the vehicles update in realtime.

[![SF MUNI Demo Image](./sf-vehicles.png)](https://geofire.firebaseapp.com/sfVehicles/index.html)

We wrote the same demo for the Objective-C and Java clients as well. The code for the demos
is available in each client's respective repository.

## Getting Started with Firebase

GeoFire requires Firebase in order to store location data. You can
[sign up here](https://www.firebase.com/signup/?utm_source=geofire) for a free account.
