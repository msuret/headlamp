---
title: "Class: default"
linkTitle: "default"
slug: "lib_k8s_pod.default"
---

[lib/k8s/pod](../modules/lib_k8s_pod.md).default

## Hierarchy

- `any`

  ↳ **`default`**

## Constructors

### constructor

• **new default**(`json`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `json` | [`KubePod`](../interfaces/lib_k8s_pod.KubePod.md) |

#### Inherited from

makeKubeObject<KubePod\>('Pod').constructor

#### Defined in

[lib/k8s/cluster.ts:70](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/cluster.ts#L70)

## Properties

### apiEndpoint

▪ `Static` **apiEndpoint**: `Object`

#### Index signature

▪ [other: `string`]: `any`

#### Defined in

[lib/k8s/pod.ts:35](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/pod.ts#L35)

___

### className

▪ `Static` **className**: `string`

#### Inherited from

makeKubeObject<KubePod\>('Pod').className

#### Defined in

[lib/k8s/cluster.ts:71](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/cluster.ts#L71)

## Accessors

### spec

• `get` **spec**(): `Object`

#### Returns

`Object`

| Name | Type |
| :------ | :------ |
| `containers` | [`KubeContainer`](../interfaces/lib_k8s_cluster.KubeContainer.md)[] |
| `nodeName` | `string` |

#### Defined in

[lib/k8s/pod.ts:37](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/pod.ts#L37)

___

### status

• `get` **status**(): `Object`

#### Returns

`Object`

| Name | Type |
| :------ | :------ |
| `conditions` | [`KubeCondition`](../interfaces/lib_k8s_cluster.KubeCondition.md)[] |
| `containerStatuses` | [`KubeContainerStatus`](../interfaces/lib_k8s_cluster.KubeContainerStatus.md)[] |
| `hostIP` | `string` |
| `message` | `string` |
| `phase` | `string` |
| `qosClass` | `string` |
| `reason` | `string` |
| `startTime` | `number` |

#### Defined in

[lib/k8s/pod.ts:41](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/pod.ts#L41)

## Methods

### exec

▸ **exec**(`container`, `onExec`, `options?`): `Object`

#### Parameters

| Name | Type |
| :------ | :------ |
| `container` | `string` |
| `onExec` | [`StreamResultsCb`](../modules/lib_k8s_apiProxy.md#streamresultscb) |
| `options` | [`ExecOptions`](../interfaces/lib_k8s_pod.ExecOptions.md) |

#### Returns

`Object`

| Name | Type |
| :------ | :------ |
| `cancel` | () => `void` |
| `getSocket` | () => ``null`` \| `WebSocket` |

#### Defined in

[lib/k8s/pod.ts:68](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/pod.ts#L68)

___

### getLogs

▸ **getLogs**(`container`, `tailLines`, `showPrevious`, `onLogs`): () => `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `container` | `string` |
| `tailLines` | `number` |
| `showPrevious` | `boolean` |
| `onLogs` | [`StreamResultsCb`](../modules/lib_k8s_apiProxy.md#streamresultscb) |

#### Returns

`fn`

▸ (): `void`

##### Returns

`void`

#### Defined in

[lib/k8s/pod.ts:45](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/pod.ts#L45)

___

### apiList

▸ `Static` **apiList**(`onList`): `any`

#### Parameters

| Name | Type |
| :------ | :------ |
| `onList` | (`arg`: `any`[]) => `void` |

#### Returns

`any`

#### Inherited from

makeKubeObject<KubePod\>('Pod').apiList

#### Defined in

[lib/k8s/cluster.ts:55](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/cluster.ts#L55)

___

### getErrorMessage

▸ `Static` **getErrorMessage**(`err?`): ``null`` \| `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `err?` | ``null`` \| [`ApiError`](../interfaces/lib_k8s_apiProxy.ApiError.md) |

#### Returns

``null`` \| `string`

#### Inherited from

makeKubeObject<KubePod\>('Pod').getErrorMessage

#### Defined in

[lib/k8s/cluster.ts:69](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/cluster.ts#L69)

___

### useApiGet

▸ `Static` **useApiGet**(`onGet`, `name`, `namespace?`, `onError?`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `onGet` | (...`args`: `any`) => `void` |
| `name` | `string` |
| `namespace?` | `string` |
| `onError?` | (`err`: [`ApiError`](../interfaces/lib_k8s_apiProxy.ApiError.md)) => `void` |

#### Returns

`void`

#### Inherited from

makeKubeObject<KubePod\>('Pod').useApiGet

#### Defined in

[lib/k8s/cluster.ts:60](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/cluster.ts#L60)

___

### useApiList

▸ `Static` **useApiList**(`onList`, `onError?`): `any`

#### Parameters

| Name | Type |
| :------ | :------ |
| `onList` | (`arg`: `any`[]) => `void` |
| `onError?` | (`err`: [`ApiError`](../interfaces/lib_k8s_apiProxy.ApiError.md)) => `void` |

#### Returns

`any`

#### Inherited from

makeKubeObject<KubePod\>('Pod').useApiList

#### Defined in

[lib/k8s/cluster.ts:56](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/cluster.ts#L56)

___

### useList

▸ `Static` **useList**(`onList?`): [`any`[], ``null`` \| [`ApiError`](../interfaces/lib_k8s_apiProxy.ApiError.md), (`items`: `any`[]) => `void`, (`err`: ``null`` \| [`ApiError`](../interfaces/lib_k8s_apiProxy.ApiError.md)) => `void`]

#### Parameters

| Name | Type |
| :------ | :------ |
| `onList?` | (...`arg`: `any`[]) => `any` |

#### Returns

[`any`[], ``null`` \| [`ApiError`](../interfaces/lib_k8s_apiProxy.ApiError.md), (`items`: `any`[]) => `void`, (`err`: ``null`` \| [`ApiError`](../interfaces/lib_k8s_apiProxy.ApiError.md)) => `void`]

#### Inherited from

makeKubeObject<KubePod\>('Pod').useList

#### Defined in

[lib/k8s/cluster.ts:66](https://github.com/kinvolk/headlamp/blob/168f394/frontend/src/lib/k8s/cluster.ts#L66)