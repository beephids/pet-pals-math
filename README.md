# Pet Pals Math

A math practice game for kids. Every animal is hungry. Solve problems to fill a treat bowl, and that animal becomes a friend who moves into the Pet Meadow.

Play it at https://beephids.github.io/pet-pals-math/

## What's inside

- **Pet Shop** (Chapter 2, adding within 1,000): adding in your head, then adding 3 or 4 numbers in columns with carrying.
- **Berry Woods** (Chapter 3, subtracting within 1,000): number tracks, number bonds, the number diamond, and column subtraction with regrouping and across zeros.
- **Help that steps in gradually**: the first wrong try gets a hint, the second shows a helper such as a number bond or ten frame, and the third fills in the answer and brings a similar problem back later in the round.
- **Pet Meadow**: every friend earned so far roams the meadow and can be petted.
- **Parents page** (behind a multiplication question): set stars, see recent practice with the problems that needed help, and copy a progress code to move stars to another device.

## How it works

The whole game is one self-contained `index.html` with no build step. Progress is saved in the browser's `localStorage`, so it stays on the device it was played on unless you move it with a progress code. The only outside request is to Google Fonts.

To run it locally, open `index.html` in a browser.

## Adding a chapter

Each chapter is a world registered with `PetPals.world({...})`, and its problems come from generators registered with `PetPals.gen(key, {...})`. The input styles (typed equation, column addition, number track, guided steps, column subtraction, number diamond) live in the engine and can be reused by any world. See the comment at the top of the engine script for the details.
