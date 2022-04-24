# Between JavaScript state

This project is intended to show main difference between JavaScript state-management libraries.

As we're trying to focus on a state-management, the most of other aspects of frontend-development are hidden under `@between-javascript-state/shared` library:

- Developing / building tools (`webpack`, etc.)
- UI components
- API layer
- The big part of routing routine

## Architecture

We use [Feature Sliced](https://feature-sliced.design) metodology.

The contents hidden under `@between-javascript-state/shared`:
- The most of `shared` layer contents
- The most of `app` layer contents
- The most of `lib` folders contents
- `components` folders contents

## Use Cases requirements

- Forms
  - _(not yet final)_ Dynamic form fields
- Filters synced with URL query params (filter, sort, pagination, etc.)
  - Should always do single request on load
  - Filters should reset when navigating to the same page without URL query parameters
- Debounced search

## Technical requirements

- Forms should be done using state-management library, without using any form-manager
- There should be at least one feature depending on the state of other feature / layer
  - There should be at least one feature depending on the **load status** of other feature / layer

## API

> :construction: **The API is not ready yet**

To show the real commertial use cases, we need to work closely with data. The simple CRUD's are not enough.

Most likely, it will be [Amplication](https://amplication.com) or [NestJS](https://nestjs.com) application.
