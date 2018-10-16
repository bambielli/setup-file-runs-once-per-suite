## setupFiles only run once per test suite

I noticed today that the jest documentation states that setupFiles run once per test. However in actuality setupFiles seem to only run once per test suite.

https://github.com/facebook/jest/blob/master/docs/Configuration.md#setupfiles-array

To run this reproduction

1) Run npm install
2) Then run npm test

I wrote 4 tests spread between 2 test suites. setupJest.js has a console.log statement in it that will print when setupJest executes. You should see 2 log outputs (one for each test suite), even thought the documentation makes it seem like you would see 4 (one for each test).
