---
title: Instalar el componente de proveedor de ejemplo
description: Después de instalar el SDK de ADSI, en el directorio de instalación, cambie los directorios por el \\ \\ \\ \\ \\ subdirectorio de configuración del proveedor de ejemplos de ADSI NetDs. Ejecute Install.bat tal y como se describe en el archivo de README.TXT.
ms.assetid: 7bf4bf22-38ac-4b0d-946e-5f60c7693707
ms.tgt_platform: multiple
keywords:
- Instalar el componente de proveedor de ejemplo ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0df567aa08b03ce9c043d345380f05cd6d1c20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418353"
---
# <a name="installing-the-example-provider-component"></a><span data-ttu-id="ad1c1-105">Instalar el componente de proveedor de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad1c1-105">Installing the Example Provider Component</span></span>

<span data-ttu-id="ad1c1-106">Después de instalar el SDK de ADSI, en el directorio de instalación, cambie los directorios por el \\ \\ \\ \\ \\ subdirectorio de configuración del proveedor de ejemplos de ADSI NetDs.</span><span class="sxs-lookup"><span data-stu-id="ad1c1-106">After installing the ADSI SDK, from the installation directory, change directories to the Samples\\NetDs\\ADSI\\Samples\\Provider\\Setup subdirectory.</span></span> <span data-ttu-id="ad1c1-107">Ejecute Install.bat tal y como se describe en el archivo de README.TXT.</span><span class="sxs-lookup"><span data-stu-id="ad1c1-107">Run Install.bat as described in the README.TXT file.</span></span>

<span data-ttu-id="ad1c1-108">El proveedor ADSI de ejemplo agregará las siguientes subclaves y valores al registro cuando se ejecute Install.bat archivo:</span><span class="sxs-lookup"><span data-stu-id="ad1c1-108">The sample ADSI provider will add the following subkeys and values to the registry when Install.bat file is run:</span></span>

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

<span data-ttu-id="ad1c1-109">Existen otras entradas del registro para el componente de proveedor de ejemplo porque el componente de proveedor de ejemplo implementó su jerarquía de directorios en el registro.</span><span class="sxs-lookup"><span data-stu-id="ad1c1-109">Other registry entries for the example provider component exist because the example provider component implemented its directory hierarchy in the registry.</span></span> <span data-ttu-id="ad1c1-110">Esto no significa que otros proveedores quieran o deben hacer lo mismo.</span><span class="sxs-lookup"><span data-stu-id="ad1c1-110">This in no way implies other providers would want to or should do the same.</span></span>

 

 




