---
id: 587d824e367417b2b2512c58
title: Run Functional Tests on API Endpoints using Chai-HTTP
challengeType: 2
isHidden: false
forumTopicId: 301593
---

## Description
<section id='description'>
As a reminder, this project is being built upon the following starter project on <a href='https://glitch.com/edit/#!/remix/clone-from-repo?REPO_URL=https://github.com/freeCodeCamp/boilerplate-mochachai/'>Glitch</a>, or cloned from <a href='https://github.com/freeCodeCamp/boilerplate-mochachai/'>GitHub</a>.

</section>

## Instructions
<section id='instructions'>
Replace <code>assert.fail()</code>. Test the status and the <code>text.response</code>. Make the test pass.
Don't send a name in the query, the endpoint responds with "hello Guest".
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: All tests should pass
    testString: getUserInput => $.get(getUserInput('url') + '/_api/get-tests?type=functional&n=0').then(data => { assert.equal(data.state,'passed'); }, xhr => { throw new Error(xhr.responseText); })
  - text: You should test for 'res.status' == 200
    testString: getUserInput => $.get(getUserInput('url') + '/_api/get-tests?type=functional&n=0').then(data => { assert.equal(data.assertions[0].method, 'equal'); assert.equal(data.assertions[0].args[0], 'res.status'); assert.equal(data.assertions[0].args[1], '200');}, xhr => { throw new Error(xhr.responseText); })
  - text: You should test for 'res.text' == 'hello Guest'
    testString: getUserInput => $.get(getUserInput('url') + '/_api/get-tests?type=functional&n=0').then(data => { assert.equal(data.assertions[1].method, 'equal'); assert.equal(data.assertions[1].args[0], 'res.text'); assert.equal(data.assertions[1].args[1], '\'hello Guest\'');}, xhr => { throw new Error(xhr.responseText); })

```

</section>

## Challenge Seed
<section id='challengeSeed'>

</section>

## Solution
<section id='solution'>

```js
/**
  Backend challenges don't need solutions, 
  because they would need to be tested against a full working project. 
  Please check our contributing guidelines to learn more.
*/
```

</section>
