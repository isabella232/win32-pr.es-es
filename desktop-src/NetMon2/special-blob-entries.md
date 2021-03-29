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
# <a name="special-blob-entries"></a><span data-ttu-id="f6f35-103">Entradas de BLOB especiales</span><span class="sxs-lookup"><span data-stu-id="f6f35-103">Special BLOB Entries</span></span>

<span data-ttu-id="f6f35-104">En los ejemplos siguientes se usa la función [**SetStringInBlob**](setstringinblob.md) para crear entradas de BLOB especiales.</span><span class="sxs-lookup"><span data-stu-id="f6f35-104">The following examples use the [**SetStringInBlob**](setstringinblob.md) function to create special BLOB entries.</span></span>

## <a name="npp-name"></a><span data-ttu-id="f6f35-105">Nombre de NPP</span><span class="sxs-lookup"><span data-stu-id="f6f35-105">NPP Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a><span data-ttu-id="f6f35-106">NPP (identificador de clase)</span><span class="sxs-lookup"><span data-stu-id="f6f35-106">NPP Class Identifier</span></span>

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a><span data-ttu-id="f6f35-107">Nombre del procedimiento CFGPROC</span><span class="sxs-lookup"><span data-stu-id="f6f35-107">CFGPROC Procedure Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a><span data-ttu-id="f6f35-108">Nombre de raíz de árbol para la interfaz de usuario del Finder</span><span class="sxs-lookup"><span data-stu-id="f6f35-108">Tree Root Name for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a><span data-ttu-id="f6f35-109">Mostrar cadena para la interfaz de usuario del Finder</span><span class="sxs-lookup"><span data-stu-id="f6f35-109">Display String for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a><span data-ttu-id="f6f35-110">Etiquetas de interfaz</span><span class="sxs-lookup"><span data-stu-id="f6f35-110">Interface Tags</span></span>

<span data-ttu-id="f6f35-111">En este ejemplo se incluyen todas las interfaces admitidas por NPP.</span><span class="sxs-lookup"><span data-stu-id="f6f35-111">This example includes every interface supported by the NPP.</span></span>

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



