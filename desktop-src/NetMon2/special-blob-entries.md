---
description: En los ejemplos siguientes se usa la función SetStringInBlob para crear entradas de BLOB especiales.
ms.assetid: 4a921b0d-9934-48e2-8837-be0bd7b7fa7a
title: Entradas de BLOB especiales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfc40029e0a0f88c2f7bd242881b0d750a5dfa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810280"
---
# <a name="special-blob-entries"></a>Entradas de BLOB especiales

En los ejemplos siguientes se usa la función [**SetStringInBlob**](setstringinblob.md) para crear entradas de BLOB especiales.

## <a name="npp-name"></a>Nombre de NPP

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a>NPP (identificador de clase)

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a>Nombre del procedimiento CFGPROC

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a>Nombre de raíz de árbol para la interfaz de usuario del Finder

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a>Mostrar cadena para la interfaz de usuario del Finder

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a>Etiquetas de interfaz

En este ejemplo se incluyen todas las interfaces admitidas por NPP.

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



