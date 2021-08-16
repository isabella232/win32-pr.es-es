---
title: Información del Registro del proveedor
description: En este tema se muestra qué claves y valores deben establecerse al agregar un proveedor ADSI.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813ad37d77d532e3c9bec91bcc3eda1f0aaf703f09dd3cf1b61ac059d7d7493b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838871"
---
# <a name="provider-registry-information"></a>Información del Registro del proveedor

El proveedor se registra con ADSI con las siguientes claves y valores:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

El proveedor se registra con Windows con las siguientes claves y valores:

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

El espacio de nombres del proveedor se registra Windows con las siguientes claves y valores:

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

En los párrafos anteriores, *el proveedor* es el identificador del objeto de nivel superior del proveedor. El *espacio de nombres* del proveedor es el identificador del objeto que implementa el espacio de nombres del proveedor.

Para obtener un ejemplo específico, vea [Instalación del componente de proveedor de ejemplo](installing-the-example-provider-component.md).

 

 




