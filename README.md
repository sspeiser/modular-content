<!--
author:   Sebastian Speiser
email:    sebastian.speiser@hft-stuttgart
version:  0.1.0
language: en
narrator: US English Female

comment:  This template composes LiaScript courses from individual files.
          After using the preprocessor this template is removed.
          

@include
Test
<script style="width: 100%; display: block" run-once="true" modify="false">
console.log('whe')
    // Get the URL of the course
    const importingDoc = window.location.search.slice(1);
    const modularUrl = 'https://sspeiser.github.io/modular-content/index.html?' + encodeURIComponent(importingDoc)
    send.liascript(`
        This is a LiaScript course using the modular-content extension.
        To properly load this course, please use https://sspeiser.github.io/modular-content/ or directly [click here](${modularUrl}).
    `)
</script>
@end
-->

# Creating modular LiaScript Courses

With this template you gain the `@include` macro that imports another LiaScript file into your course.
If you open a course using this directly in LiaScript, it will show warnings that you have to open it using the modular-content preprocessor: https://sspeiser.github.io/modular-content/

The preprocessor downloads files that are included and then passes it to the regular LiaScript interpreter.
Currently there is a limit on course size depending on the browser you are using - roughly 8 kB.
There is a plan to use an anonymous file hosting service for larger files.

This is a first proof of concept.
