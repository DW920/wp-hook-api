# Instructions

- [ ] Fork this gist.
- [ ] Modify the code samples to complete the first 2 tasks.
- [ ] Answer the remaining 2 questions.
- [ ] Reply back to the email you were sent with the link to your completed gist by 5:00 pm EST on Wednesday, January 22.

___

1. Given an API route for retrieving a specific record, do the following:
   1. Get the `id` param
   2. Return a 404 if the record isn't found
   3. Return a response with the record if it is found
   
_Note: This task is conceptual and we understand you do not have the full code. Please imagine there is working code up to the point of the task. Please do not complete the imagined portion of the code, nor write a full plugin to complete this task._

Route format:

`/publishers/(?P<id>\d+)`

`/publishers/397`

Code that returns the response:
```php
<?php

function get_publisher( \WP_REST_Request $request ) {
    // Task 1-i: Replace `null` with the retreived `id` parameter
    $publisher_id = null;

    /*
     * Imagine code that gets the record from the database as `$publisher`
     */

    if ( empty( $publisher ) ) {
        // Task 1-ii: Return a 404 response
    }

    // Task 1-iii: Return a normal REST response with the `$publisher`
}
```

2. Do the following:
   1. Add a WordPress hook to determine the value of the `visible` property on some item.
   2. Then use that hook elsewhere to change the value to `false`;

```php
<?php

function modify_item( $item ) {
    /*
     * `$item` is an object
     */

    // Task 2-i: Set the `visible` property of `$item` to the value of a hook `item_visibility`, with a default value of `true`

    return $item;
}

/*
 * Elsewhere in the code
 */

function hide_item() {
    // Task 2-ii: Add the `item_visibility` hook to change the `visible property of `$item` to `false`
}

```

3. What is your favorite WordPress core function and why?
4. What frustrates you about WordPress, and what's something that you think needs to change?