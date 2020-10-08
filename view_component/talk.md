
### View Components in Rails

*with the view_component gem*

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
.right[by Dany Marcoux from the Build Solutions team at SUSE]

---

### Agenda

- What are components?
- Why should you use components?
- How can you use view_component?
- Short demo in OBS
- Q&A

---

### What are components?

Components are Ruby objects that output HTML.

Inspired by frontend frameworks like React and Vue. Unlike them, view_component is a server-side approach.

Components are most effective in cases where view code is reused or benefits from being tested directly.

---

### Why should you use components?

#### Testing

\+ Components can be unit-tested.

\- Views are only tested through slow integration tests.

#### Data Flow

\+ Components have an explicit interface. They use the standard Ruby `initializer`
method.

\- Views have an implicit interface, making it hard to know what information is
needed to render them.

#### Standards

\+ Components are Ruby objects, making it easy to follow and enforce code quality
standards.

\- Views often fail basic Ruby code quality standards: huge files, deep conditional
nesting, and more.

---

### How can you use view_component?

`view_component` is supported natively in Rails 6.1, and compatible with Rails 5.0+ via an included monkey patch.

*From the [Layouts and Rendering guide](https://edgeguides.rubyonrails.org/layouts_and_rendering.html#rendering-objects):*

> Rails can render objects responding to `:render_in.`
```ruby
render MyComponent.new
```
>This calls render_in on the provided object with the current view context.

---

### Short demo in OBS

Code: https://github.com/openSUSE/open-build-service/compare/master...dmarcoux:introduce-view_component

Then live in the development environment of OBS!

---

### Q&A

Upstream: https://github.com/github/view_component

Slides in markdown format: https://github.com/dmarcoux/talks
