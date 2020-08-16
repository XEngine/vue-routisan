<img src="https://rockett.pw/git-assets/vue-routisan/logo.svg" alt="Vue Routisan" width="250">

Elegant, fluent route definitions for [Vue Router](https://router.vuejs.org/), inspired by [Laravel](https://laravel.com).</p>

![Release 3.x](https://rockett.pw/git-assets/vue-routisan/release-3x.badge.svg)
![Made with JavaScript](https://rockett.pw/git-assets/badges/javascript.badge.svg)
![Gluten Free](https://rockett.pw/git-assets/badges/gluten-free.badge.svg)
![Built with ♥](https://rockett.pw/git-assets/badges/with-love.badge.svg)

![`npm i vue-routisan // yarn add vue-routisan`](https://rockett.pw/git-assets/vue-routisan/install.badge.svg)

---

Routisan provides you with a friendlier way to declare route definitions for Vue Router. Inspired by Laravel, it uses chained calls to build up your routes, allowing you to group and nest as deeply as you like.

```js
Route.view('blog', 'Blog').name('blog').children(() => {
  // All Posts
  Route.view('/', 'Blog/Posts').name('posts')

  // Single Post
  Route.view('{post}', 'Blog/Post').name('single-post').children(() => {
    Route.view('edit', 'Blog/Post/Edit').name('edit')
    Route.view('stats', 'Blog/Post/Stats').name('stats')
  })
})
```

This produces an array of routes in the format Vue Router expects to see, and follows a behaviour somewhat similar to Laravel’s router, such as:

- Using callbacks to iteratively collect routes
- Correctly joining nested routes together, regardles of prefixed slashes
- Correctly joining the names of nested routes, using a separator of your choice

## Documentation

You can read the docs on the [Vue Routisan 3 site](https://vue-routisan.rockett.pw/).

## License

Vue Routisan is licensed under the ISC license, which is more permissive variant of the MIT license. You can read the license [here](license.md).

## Contributing

If you would like to contribute code to Vue Routisan, simply open a Pull Request containing the changes you would like to see. Please provide a proper description of the changes, whether they fix a bug, enhance an existing feature, or add a new feature.

If you spot a bug and don’t know how to fix it (or just don’t have the time), simply [open an issue](https://github.com/mikerockett/vue-routisan/issues/new). Please ensure the issue is descriptive, and contains a link to a reproduction of the issue. Additionally, please prefix the title with the applicable version of Routisan, such as `[3.0]`.

Feature requests may also be submitted by opening an issue – please prefix the title with "Feature Request"