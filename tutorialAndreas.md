# Trekk på kode for å få motoren til å spinne

## Åpne motorblokken
Bruk ulik kode for å gjøre dette
Bruk blokken ``||basic:pause||`` og blokken ``||servos:setAngle||`` og plasser dem i ``||basic:forever|| blokken``.
```blocks
basic.forever(function () {
servos.P0.setAngle(90)
basic.pause(100)
```
## Endre på verdiene for vinkel og pause
Prøv å få motoren til å gå fra 0 til 180
```blocks
servos.P0.setAngle(0)
servos.P0.setAngle(180)
```
## Ferdig kode
```blocks
basic.forever(function () {
        servos.P0.setAngle(30)
        basic.pause(1000)
        servos.P0.setAngle(150)
        basic.pause(1000)
```
/**
* Bruk denne fila for å definere egne funksjoner og blokker.
* Les mer i https://makecode.microbit.org/blocks/custom
*/

enum MyEnum {
    //% block="one"
    One,
    //% block="two"
    Two
}

/**
 * Custom blocks
 */
//% weight=100 color=#0fbc11 icon=""
namespace custom {
    /**
     * TODO: describe your function here
     * @param n describe parameter here, eg: 5
     * @param s describe parameter here, eg: "Hello"
     * @param e describe parameter here
     */
    //% block
    export function foo(n: number, s: string, e: MyEnum): void {
        // Add code here
    }

    /**
     * TODO: describe your function here
     * @param value describe value here, eg: 5
     */
    //% block
    export function fib(value: number): number {
        return value <= 1 ? value : fib(value -1) + fib(value - 2);
    }
}
