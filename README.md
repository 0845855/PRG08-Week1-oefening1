# PRG08-Week1-oefening1

## Herhaling OOP concepten
classes, encapsulation, composition, inheritance, interface, static, abstract

## Opdracht 1
- Maak een **abstract gameobject** class waar **kart** en **driver** van overerven
- Het gameobject krijgt via de constructor de juiste afbeelding
- Het gameobject plaatst een div in de body
- Maak de **message** class **static** en corrigeer alle aanroepen
- De kart **heeft** een driver

## Opdracht 2
- Voeg een game loop toe aan game.ts. Geef de kart een speed property. De game loop update de kart. 
- Laat de kart van links naar rechts rijden.
- Hoe wordt de driver geupdate?

## Voorbeeldcode

### Inheritance

```
class Vehicle {
    constructor() {
        console.log("vroom!");
    );
}
class Car extends Vehicle {
    constructor() {
        super();
    }
}
```

### Interface

```
interface Vehicle {
    private fuel: number;
    public drive();
}
class Car implements Vehicle {
    private fuel: number = 4;
    public drive(){
    }
}
```

### Static

```
public static class Calculator { 
    public static add(a :number, b :number) : number { 
       return a + b;
    } 
} 
let n : number = Calculator.add(3,4);
```

### Game Loop

```
class Game {

    private fish:Fish;

    constructor() {
        this.fish = new Fish();     
        requestAnimationFrame(() => this.gameLoop());
    }

    gameLoop(){
        this.fish.move();
        requestAnimationFrame(() => this.gameLoop());
    }
}
```

## Links
- [Instellen werkomgeving](https://github.com/HR-CMGT/PRG04-Week0)
- [Typescript Classes](https://www.typescriptlang.org/docs/handbook/classes.html)
- [Game Loop](https://developer.mozilla.org/en-US/docs/Web/API/window/requestAnimationFrame)
