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