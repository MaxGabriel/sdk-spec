# Requesting /start

1. The SDK should pull /start from disk, if it exists.
2. The SDK hits the med.heyzap.com/start endpoint to get the latest /start data.
3. The SDK will keep retrying until it succeeds, with some sort of exponential falloff. Once it succeeds, it should cache the /start response to disk.
    * The SDK should update the following things from cached version: 
        * New enabled networks
        * Any configuration
            * IAP disable time, disabled tags, etc.


The SDK should send the default mediation parameters to /start.

## Rationale / Reason for existence

* Our mediation will work even when med.heyzap.com is down
* Allows faster startup

## Points of contact

* iOS: Max
* Android: Thomas
* mediation-service: Micah
