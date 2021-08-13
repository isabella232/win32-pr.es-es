---
title: Instalación del componente de proveedor de ejemplo
description: Después de instalar el SDK de ADSI, desde el directorio de instalación, cambie los directorios al subdirectorio Samples NetDs ADSI Samples Provider Setup (Configuración del proveedor de ejemplos de ADSI de Samples \\ \\ \\ \\ \\ NetDs). Ejecute Install.bat como se describe en el README.TXT archivo.
ms.assetid: 7bf4bf22-38ac-4b0d-946e-5f60c7693707
ms.tgt_platform: multiple
keywords:
- Instalación del adsi del componente de proveedor de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e58fb471385b862982904e69a432bec1a94e3b9aff0248fdacd9f5e9c7a3e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333245"
---
# <a name="installing-the-example-provider-component"></a>Instalación del componente de proveedor de ejemplo

Después de instalar el SDK de ADSI, desde el directorio de instalación, cambie los directorios al subdirectorio Samples NetDs ADSI Samples Provider Setup (Configuración del proveedor de ejemplos de ADSI de Samples \\ \\ \\ \\ \\ NetDs). Ejecute Install.bat como se describe en el README.TXT archivo.

El proveedor ADSI de ejemplo agregará las siguientes subclaves y valores al Registro cuando Install.bat se ejecute el archivo :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               Sample = SampleNamespace
```

```
HKEY_CLASSES_ROOT
   SampleNamespace
      Clsid = {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   Sample
      Clsid = {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Namespace Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = SampleNamespace
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Provider Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = Sample
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

Existen otras entradas del Registro para el componente de proveedor de ejemplo porque el componente de proveedor de ejemplo implementó su jerarquía de directorios en el Registro. Esto de ninguna manera implica que otros proveedores quieran o deberían hacer lo mismo.

 

 




