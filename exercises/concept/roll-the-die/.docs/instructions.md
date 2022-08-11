# Instructions

Continuing the theme of the wizards and warriors game, it is time to add an all purpose die rolling method. This will be the traditional 18 sided die with numbers 1 to 18. Players also generate a spell strength.

# How to generate a random number.
Random is a pseudorandom number generator that we can initialize using the `new` keyword.
```csharp
var random = new Random();
```
Once initialized we can retrieve a random number from the `Random` class:
```csharp
var rNum = random.Next();
```
The who code goes like this:
```csharp
Random dice = new Random(); // Initialize
int roll = dice.Next(1, 7); // Set roll to random number between 1 and 6

return new Random().Next(1, 7); // Or just resturn rundom number
```

## 1. Enable a _wizards and warriors_ player to roll a die.

Implement a `RollDie()` method on the `Player` class.

```csharp
var player = new Player();
player.RollDie();
// => >= 1 <= 18
```

## 2. Players need their strength. Provide a means to generate spell strength

Implement a `GenerateSpellStrength()` method on the player class. The spell strength is between 0.0 and up to but not including 100.0.

Note that spell strength must be a real number (not an integer) to reduce the possibility of a tie when the strengths of two adversaries are compared.

```csharp
var player = new Player();
player.GenerateSpellStrength();
// => >= 0.0 < 100.0
```
