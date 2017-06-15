# jest-symlink-repro

To reproduce:

1. `npm install`.
2. Run `node index.js`. You should see

    $ node index.js
    a was required
    done
    
3. Run `npm test`. You should see


```
$ npm test

> @ test /private/tmp/test-project
> jest

 FAIL  ./index.test.js
  ● Test suite failed to run

    Your test suite must contain at least one test.

      at onResult (node_modules/jest/node_modules/jest-cli/build/TestRunner.js:110:20)
          at <anonymous>

Test Suites: 1 failed, 1 total
Tests:       0 total
Snapshots:   0 total
Time:        0.964s
Ran all test suites.
  console.log a.js:1
    a was required

  console.log b.js:1
    a was required

  console.log index.test.js:3
    done
```

Notice that `a was required` was printed twice above.
