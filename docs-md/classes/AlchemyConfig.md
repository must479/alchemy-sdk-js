[alchemy-sdk](../README.md) / [Exports](../modules.md) / AlchemyConfig

# Class: AlchemyConfig

This class holds the config information for the SDK client instance and
exposes the underlying providers for more advanced use cases.

## Table of contents

### Constructors

- [constructor](AlchemyConfig.md#constructor)

### Properties

- [apiKey](AlchemyConfig.md#apikey)
- [authToken](AlchemyConfig.md#authtoken)
- [batchRequests](AlchemyConfig.md#batchrequests)
- [maxRetries](AlchemyConfig.md#maxretries)
- [network](AlchemyConfig.md#network)
- [url](AlchemyConfig.md#url)

### Methods

- [getProvider](AlchemyConfig.md#getprovider)
- [getWebSocketProvider](AlchemyConfig.md#getwebsocketprovider)

## Constructors

### constructor

• **new AlchemyConfig**(`config?`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `config?` | [`AlchemySettings`](../interfaces/AlchemySettings.md) |

#### Defined in

[src/api/alchemy-config.ts:58](https://github.com/alchemyplatform/alchemy-sdk-js/blob/8b1ae5c/src/api/alchemy-config.ts#L58)

## Properties

### apiKey

• `Readonly` **apiKey**: `string`

The Alchemy API key.

#### Defined in

[src/api/alchemy-config.ts:22](https://github.com/alchemyplatform/alchemy-sdk-js/blob/8b1ae5c/src/api/alchemy-config.ts#L22)

___

### authToken

• `Optional` `Readonly` **authToken**: `string`

The optional Alchemy auth token to use when sending requests with the Notify API.

#### Defined in

[src/api/alchemy-config.ts:40](https://github.com/alchemyplatform/alchemy-sdk-js/blob/8b1ae5c/src/api/alchemy-config.ts#L40)

___

### batchRequests

• `Readonly` **batchRequests**: `boolean`

Setting to enable automatic batching on json-rpc requests. Defaults to false.

#### Defined in

[src/api/alchemy-config.ts:31](https://github.com/alchemyplatform/alchemy-sdk-js/blob/8b1ae5c/src/api/alchemy-config.ts#L31)

___

### maxRetries

• `Readonly` **maxRetries**: `number`

The maximum number of retries to perform.

#### Defined in

[src/api/alchemy-config.ts:28](https://github.com/alchemyplatform/alchemy-sdk-js/blob/8b1ae5c/src/api/alchemy-config.ts#L28)

___

### network

• `Readonly` **network**: [`Network`](../enums/Network.md)

The Network that this SDK is associated with.

#### Defined in

[src/api/alchemy-config.ts:25](https://github.com/alchemyplatform/alchemy-sdk-js/blob/8b1ae5c/src/api/alchemy-config.ts#L25)

___

### url

• `Optional` `Readonly` **url**: `string`

The optional hardcoded URL to send requests to instead of using the network
and apiKey.

#### Defined in

[src/api/alchemy-config.ts:37](https://github.com/alchemyplatform/alchemy-sdk-js/blob/8b1ae5c/src/api/alchemy-config.ts#L37)

## Methods

### getProvider

▸ **getProvider**(): `Promise`<[`AlchemyProvider`](AlchemyProvider.md)\>

Returns an AlchemyProvider instance. Only one provider is created per
Alchemy instance.

The AlchemyProvider is a wrapper around ether's `AlchemyProvider` class and
has been expanded to support Alchemy's Enhanced APIs.

Most common methods on the provider are available as top-level methods on
the [Alchemy](Alchemy.md) instance, but the provider is exposed here to access
other less-common methods.

#### Returns

`Promise`<[`AlchemyProvider`](AlchemyProvider.md)\>

#### Defined in

[src/api/alchemy-config.ts:100](https://github.com/alchemyplatform/alchemy-sdk-js/blob/8b1ae5c/src/api/alchemy-config.ts#L100)

___

### getWebSocketProvider

▸ **getWebSocketProvider**(): `Promise`<[`AlchemyWebSocketProvider`](AlchemyWebSocketProvider.md)\>

Returns an AlchemyWebsocketProvider instance. Only one provider is created
per Alchemy instance.

The AlchemyWebSocketProvider is a wrapper around ether's
`AlchemyWebSocketProvider` class and has been expanded to support Alchemy's
Subscription APIs, automatic backfilling, and other performance improvements.

Most common methods on the provider are available as top-level methods on
the [Alchemy](Alchemy.md) instance, but the provider is exposed here to access
other less-common methods.

#### Returns

`Promise`<[`AlchemyWebSocketProvider`](AlchemyWebSocketProvider.md)\>

#### Defined in

[src/api/alchemy-config.ts:122](https://github.com/alchemyplatform/alchemy-sdk-js/blob/8b1ae5c/src/api/alchemy-config.ts#L122)
