---
layout: default
title: Health Component
nav_order: 3
---

# Health Component

The Health Component is a component that can be added to an entity to give it health. It can be used to represent the health of a player, an enemy, a destructible object, etc.

## Properties

| Property               | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| **Debug**              | Whether to show debug information in the editor.                            |
| **Max Health**         | The maximum health of the entity.                                           |
| **Current Health**     | The current health of the entity.                                           |
| **Start Health**       | The starting health of the entity.                                          |
| **Is Alive**           | Whether the entity is alive.                                                |
| **Low Health Threshold** | The threshold at which the entity's health is considered low.              |
| **Can Regenerate**     | Whether the entity can regenerate health.                                   |
| **Regeneration Rate**  | The rate at which the entity's health regenerates. If set to 0, the entity will not regenerate health. |
| **Regeneration Delay** | The delay before the entity starts regenerating health after taking damage. |
| **Max Regeneration Cap** | The maximum health the entity can regenerate to.                          |
| **Can Invincible**     | Whether the entity can become invincible after taking damage.               |
| **Invincibility Duration** | The duration of invincibility after taking damage.                      |
| **Low Health Threshold** | The health percentage at which OnLowHealth is triggered.                  |

## Methods

| Method                  | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| **Current Health**      | Returns the entity's current health.                                        |
| **Current Max Health**  | Returns the entity's max health.                                            |
| **Set Max Health**      | Sets the entity's max health.                                               |
| **Set Current Health**  | Sets the entity's current health.                                           |
| **Reset Health**        | Resets the entity's health to its starting health.                          |
| **Take Damage**         | Takes damage from the entity's health.                                      |
| **Heal**                | Heals the entity's health.                                                  |
| **Start Regeneration**  | Starts regenerating the entity's health.                                    |
| **Stop Regeneration**   | Stops regenerating the entity's health.                                     |
| **Start Invincibility** | Starts invincibility.                                                       |
| **Stop Invincibility**  | Stops invincibility.                                                        |
| **Is Alive**            | Returns whether the entity is alive.                                        |

## Events

| Event                        | Description                                                                 |
|------------------------------|-----------------------------------------------------------------------------|
| **On Health Changed**        | Called when the entity's health changes.                                    |
| **On Health Regenerated**    | Called when the entity's health regenerates.                                |
| **On Health Regeneration Started** | Called when the entity starts regenerating health.                   |
| **On Health Regeneration Stopped** | Called when the entity stops regenerating health.                    |
| **On Health Fully Regenerated** | Called when the entity's health is fully regenerated.                   |
| **On Invincibility Started** | Called when the entity starts invincibility.                               |
| **On Invincibility Stopped** | Called when the entity stops invincibility.                                |
| **On Damage Taken**          | Called when the entity takes damage.                                        |
| **On Low Health**            | Called when the entity's health is low.                                     |
| **On Death**                 | Called when the entity dies.                                                |

## Examples

### Basic Usage

// Example of adding a Health Component to an entity Entity entity = new Entity(); HealthComponent healthComponent = new HealthComponent(); entity.AddComponent(healthComponent);
// Setting initial health values healthComponent.MaxHealth = 100; healthComponent.CurrentHealth = 100; healthComponent.StartHealth = 100;

### Taking Damage

// Example of taking damage healthComponent.TakeDamage(20); Console.WriteLine(healthComponent.CurrentHealth); // Output: 80

### Healing

// Example of healing healthComponent.Heal(10); Console.WriteLine(healthComponent.CurrentHealth); // Output: 90

### Regeneration

// Example of starting health regeneration healthComponent.CanRegenerate = true; healthComponent.RegenerationRate = 5; healthComponent.StartRegeneration();

## Tips and Tricks

- **Debugging**: Enable the `Debug` property to see detailed information about the health component in the editor.
- **Balancing**: Adjust the `Regeneration Rate` and `Regeneration Delay` to balance the gameplay experience.
- **Invincibility**: Use the `Can Invincible` and `Invincibility Duration` properties to create temporary invincibility after taking damage, which can be useful for creating more forgiving gameplay mechanics.

<!-- Add images here to illustrate the properties, methods, and events. For example:
![Health Component Properties](path/to/health-component-properties.png)
*Image showing the properties of the Health Component in the editor.*

![Health Component Methods](path/to/health-component-methods.png)
*Image showing the methods of the Health Component being used in code.*

![Health Component Events](path/to/health-component-events.png)
*Image showing the events of the Health Component being triggered.*
-->