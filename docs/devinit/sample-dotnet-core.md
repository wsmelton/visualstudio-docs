---
title: .NET Core app
description: Example repository that uses devinit to install a specific .NET Core SDK.
ms.date: 11/02/2020
ms.topic: reference
author: andysterland
ms.author: andster
manager: jillfra
ms.workload:
- multiple
monikerRange: ">= vs-2019"
ms.prod: visual-studio-windows
ms.technology: devinit
---

# .NET Core app

See the [DotnetCoreDevinitExample](https://github.com/microsoft/DotnetCoreDevinitExample) repository for a full example of using devinit to install the required .NET Core SDK version in Codespaces.

## .devinit.json

```json
{
  "$schema": "https://json.schemastore.org/devinit.schema-2.0",
  "run": [
    {
      "comments": "Installs the .NET Core SDK specified in the global.json file.",
      "tool": "require-dotnetcoresdk"
    }
  ]
}
```

## .devcontainer.json

Contents of the _.devcontainer.json_ file in the repo root.

```json
{
  "postCreateCommand": "devinit init"
}
```

## global.json

Contents of the _global.json_ file in the repo root.

```json
{
  "sdk": {
    "version": "3.1.302"
  }
}
```