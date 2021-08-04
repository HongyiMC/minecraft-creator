---
# DO NOT TOUCH — This file was automatically generated. See https://github.com/Mojang/MinecraftScriptingApiDocsGenerator to modify descriptions, examples, etc.
author: jakeshirley
ms.author: jashir
ms.prod: gaming
title: mojang-minecraft.Player Class
description: Contents of the mojang-minecraft.Player class.
---
# Player Class
>[!IMPORTANT]
>These APIs are experimental as part of GameTest Framework. As with all experiments, you may see changes in functionality in updated Minecraft versions. Check the Minecraft Changelog for details on any changes to GameTest Framework APIs. Where possible, this documentation reflects the latest updates to APIs in Minecraft beta versions.


Represents a player within the world.

## Properties
### **id**
`read-only id: string;`

Identifier for the player.

Type: *string*


### **isSneaking**
`isSneaking: boolean;`

True if the player is currently using a sneaking movement.

Type: *boolean*


### **location**
`read-only location: Location;`

Current location of the player.

Type: [*Location*](Location.md)


### **name**
`read-only name: string;`

Name of the player.

Type: *string*


### **nameTag**
`nameTag: string;`

Optional name tag of the player.

Type: *string*


### **velocity**
`read-only velocity: Location;`

Current speed of the player across X, Y, and Z dimensions.

Type: [*Location*](Location.md)



## Methods
- [addEffect](#addeffect)
- [getComponent](#getcomponent)
- [getComponents](#getcomponents)
- [getEffect](#geteffect)
- [hasComponent](#hascomponent)
- [kill](#kill)
- [triggerEvent](#triggerevent)
  
### **addEffect**
`
addEffect(effectType: EffectType, duration: number, amplifier: number): void
`

Adds an effect, like poison, to the entity.
#### Arguments
| Parameter | Type | Default Value | Description |
| :--- | :--- | :--- | :---: |
| **effectType** | [*EffectType*](EffectType.md) | n/a | Type of effect to add to the entity. |
| **duration** | *number* | n/a | Amount of time, in seconds, for the effect to apply. |
| **amplifier** | *number* | n/a | Optional amplification of the effect to apply. |


> [!WARNING]
> This function can throw errors.

### **getComponent**
`
getComponent(componentId: string): any
`

Gets a component (that represents additional capabilities) for an entity.
#### Arguments
| Parameter | Type | Default Value | Description |
| :--- | :--- | :--- | :---: |
| **componentId** | *string* | n/a | The identifier of the component (e.g., 'minecraft:rideable') to retrieve. If no namespace prefix is specified, 'minecraft:' is assumed. If the component is not present on the entity, undefined is returned. |

Returns *any*


### **getComponents**
`
getComponents(): any[]
`

Returns all components that are both present on this entity and supported by the API.

Returns *any*[]


### **getEffect**
`
getEffect(effectType: EffectType): Effect
`

Returns the effect for the specified EffectType on the entity, or undefined if the effect is not present.
#### Arguments
| Parameter | Type | Default Value | Description |
| :--- | :--- | :--- | :---: |
| **effectType** | [*EffectType*](EffectType.md) | n/a | - |

Returns [*Effect*](Effect.md) - Effect object for the specified effect, or undefined if the effect is not present.

> [!WARNING]
> This function can throw errors.

### **hasComponent**
`
hasComponent(componentId: string): boolean
`

Returns true if the specified component is present on this entity.
#### Arguments
| Parameter | Type | Default Value | Description |
| :--- | :--- | :--- | :---: |
| **componentId** | *string* | n/a | The identifier of the component (e.g., 'minecraft:rideable') to retrieve. If no namespace prefix is specified, 'minecraft:' is assumed. |

Returns *boolean*


### **kill**
`
kill(): void
`

Kills this entity. The entity will drop loot as normal.


> [!WARNING]
> This function can throw errors.

### **triggerEvent**
`
triggerEvent(eventName: string): void
`

Triggers an entity type event. For every entity, a number of events are defined in an entities' definition for key entity behaviors; for example, creepers have a minecraft:start_exploding type event.
#### Arguments
| Parameter | Type | Default Value | Description |
| :--- | :--- | :--- | :---: |
| **eventName** | *string* | n/a | Name of the entity type event to trigger. If a namespace is not specified, minecraft: is assumed. |


> [!WARNING]
> This function can throw errors.

