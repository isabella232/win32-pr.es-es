---
title: Información del registro del proveedor
description: En este tema se muestran las claves y los valores que se deben establecer al agregar un proveedor ADSI.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790a80964bdcc6111a4c167056a0b85bda23e147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418349"
---
# <a name="provider-registry-information"></a>Información del registro del proveedor

El proveedor se registra con ADSI con las claves y los valores siguientes:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

El proveedor se registra con Windows con las claves y los valores siguientes:

```
HKEY_CLASSES_ROOT
   provider
      Clsid
         (Default) = <provider CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider DLL filename>
            ThreadingModel = Both
         ProgID = <provider object name>
         TypeLib = <provider TypeLib CLSID>
         Version = <provider version number>
```

El espacio de nombres del proveedor se registra con Windows con las claves y los valores siguientes:

```
HKEY_CLASSES_ROOT
   provider namespace
      Clsid
         (Default) = <provider namespace CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider namespace CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider namespace DLL filename>
            ThreadingModel = Both
         ProgID = <provider namespace object name>
         TypeLib = <provider namespace TypeLib CLSID>
         Version = <provider namespace version number>
```

En los párrafos anteriores, el *proveedor* es el identificador del objeto de nivel superior del proveedor. El *espacio de nombres del proveedor* es el identificador del objeto que implementa el espacio de nombres del proveedor.

Para ver un ejemplo concreto, consulte [instalar el componente de proveedor de ejemplo](installing-the-example-provider-component.md).

 

 




