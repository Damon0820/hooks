---
title: Ready
nav: Hooks
group: useRequest
order: 5
---

# Ready

useRequest provides an `options.ready`, when its value is `false`, the request will never be sent.

The specific behavior is as follows:

1. In the automatic mode of `manual=false`, every time `ready` changes from `false` to `true`, a request will be automatically executed with the parameter `options.defaultParams`.
2. When `manual=true` manual request mode, as long as `ready=false`, the request triggered by `run/runAsync` will not be executed.

## Automatic mode

The following example demonstrates the behavior of `ready` in automatic mode. Every time `ready` changes from `false` to `true`, the request will be executed.

<code src="./demo/ready.tsx"></code>

## Manual mode

The following example demonstrates the behavior of `ready` in manual mode. Only when `ready` is equal to `true`, `run` will be executed.

<code src="./demo/manualReady.tsx"></code>

## API

### Options

| Property | Description                  | Type      | Default |
| -------- | ---------------------------- | --------- | ------- |
| ready    | Is the current request ready | `boolean` | `true`  |