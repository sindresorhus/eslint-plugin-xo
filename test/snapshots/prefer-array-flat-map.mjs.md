# Snapshot report for `test/prefer-array-flat-map.mjs`

The actual snapshot is saved in `prefer-array-flat-map.mjs.snap`.

Generated by [AVA](https://avajs.dev).

## Invalid #1
      1 | const bar = [[1],[2],[3]].map(i => [i]).flat()

> Output

    `␊
      1 | const bar = [[1],[2],[3]].flatMap(i => [i])␊
    `

> Error 1/1

    `␊
    > 1 | const bar = [[1],[2],[3]].map(i => [i]).flat()␊
        |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Prefer `.flatMap(…)` over `.map(…).flat()`.␊
    `

## Invalid #2
      1 | const bar = [[1],[2],[3]].map(i => [i]).flat(1.00)

> Output

    `␊
      1 | const bar = [[1],[2],[3]].flatMap(i => [i])␊
    `

> Error 1/1

    `␊
    > 1 | const bar = [[1],[2],[3]].map(i => [i]).flat(1.00)␊
        |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Prefer `.flatMap(…)` over `.map(…).flat()`.␊
    `

## Invalid #3
      1 | const bar = [[1],[2],[3]].map(i => [i]).flat(1,)

> Output

    `␊
      1 | const bar = [[1],[2],[3]].flatMap(i => [i])␊
    `

> Error 1/1

    `␊
    > 1 | const bar = [[1],[2],[3]].map(i => [i]).flat(1,)␊
        |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Prefer `.flatMap(…)` over `.map(…).flat()`.␊
    `

## Invalid #4
      1 | const foo = [].concat(...bar.map((i) => i));

> Error 1/1

    `␊
    > 1 | const foo = [].concat(...bar.map((i) => i));␊
        |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Prefer `.flatMap(…)` over `[].concat(...foo.map(…))`.␊
    `