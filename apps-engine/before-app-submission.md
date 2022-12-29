---
description: Make sure to check these before submitting the app, it will fail otherwise
---

# Before app submission

#### Check your package.json

Make sure your `package.json` looks like this

```json
{
    "devDependencies": {
        "@rocket.chat/apps-engine": "^1.36.0",
        "@types/node": "^18.11.18",
        "tslint": "^5.20.1",
        "typescript": "^4.9.4"
    }
}
```

Everything should be in `devDependencies` and there should be no regular dependencies&#x20;

#### check/update apps engine version

If you need to update the apps engine version simply change\
`"@rocket.chat/apps-engine": "^1.36.0"`\
``in the package.json to \
`"@rocket.chat/apps-engine": "*"` \
and run

```bash
npm update --save
```

this will install the latest version, if you need a specific version.
