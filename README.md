# Athena Plugin - Factions Paychecks

A paycheck system for factions for the Athena Framework compatible with `3.9.0` of the [Athena Framework](https://athenaframework.com/).

## Installation

1. Open a command prompt in your main Athena Directory.
2. Navigate to the plugins folder.

```ts
cd src/core/plugins
```

3. Copy the command below.

**SSH**

```
git clone git@github.com:Stuyk/athena-plugin-factions-paychecks.git
```

**HTTPS**
```
git clone https://github.com/Stuyk/athena-plugin-factions-paychecks
```

4. Append the following code to the [Factions Plugin](https://github.com/Stuyk/athena-plugin-factions).

File: `factions/webview/coreInjections.ts`

```ts
export const FactionCorePageInjections = {
    actions: {},
    bank: {
        BankPaychecks: defineAsyncComponent(() => import('../../athena-plugin-factions-paychecks/components/BankPaychecks.vue')),
    },
    members: {},
    rankings: {},
    settings: {
        Paychecks: defineAsyncComponent(() => import('../../athena-plugin-factions-paychecks/components/Paychecks.vue')),
    },
};
```
