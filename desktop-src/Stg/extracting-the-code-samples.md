---
title: Extraer los ejemplos de código
description: Aunque los ejemplos de código están divididos en una serie de lecciones del tutorial, las agrupaciones de ejemplo adecuadas se pueden extraer fácilmente de la colección.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418569"
---
# <a name="extracting-the-code-samples"></a><span data-ttu-id="14792-103">Extraer los ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="14792-103">Extracting the Code Samples</span></span>

<span data-ttu-id="14792-104">Aunque los ejemplos de código están divididos en una serie de lecciones del tutorial, las agrupaciones de ejemplo adecuadas se pueden extraer fácilmente de la colección.</span><span class="sxs-lookup"><span data-stu-id="14792-104">Though the code samples are divided into a series of tutorial lessons, the appropriate sample groupings can easily be extracted from the collection.</span></span> <span data-ttu-id="14792-105">La mayoría de los directorios de ejemplo individuales están diseñados para funcionar junto con al menos otro directorio de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="14792-105">Most of the individual sample directories are meant to work in conjunction with at least one other sample directory.</span></span> <span data-ttu-id="14792-106">Los ejemplos relacionados con los componentes se componen de un par de cliente y servidor, con el servidor que requiere el uso de la utilidad de ejemplo REGISTER.</span><span class="sxs-lookup"><span data-stu-id="14792-106">The component-related samples consist of a client and server pair, with the server requiring the use of the REGISTER sample utility.</span></span> <span data-ttu-id="14792-107">A continuación se muestra un resumen de las agrupaciones de ejemplo y cómo extraer cada grupo como una unidad que se pueda compilar.</span><span class="sxs-lookup"><span data-stu-id="14792-107">Here is a summary of the sample groupings and how to extract each group as a buildable unit.</span></span> <span data-ttu-id="14792-108">Para cada agrupación de ejemplo, copie el contenido de los directorios mostrados.</span><span class="sxs-lookup"><span data-stu-id="14792-108">For each sample grouping, copy the content of the directories shown.</span></span> <span data-ttu-id="14792-109">El \[ \] Directorio de destino primario que se muestra no requiere contenido de la rama samples.</span><span class="sxs-lookup"><span data-stu-id="14792-109">The parent \[destination\] directory shown requires no content from the samples branch.</span></span> <span data-ttu-id="14792-110">Sin embargo, los menús de ayuda de los ejemplos en ejecución suponen que se trata del tutorial adecuado. Los archivos de ayuda HTM se encuentran en este \[ Directorio de destino primario \] .</span><span class="sxs-lookup"><span data-stu-id="14792-110">However, the help menus in the running samples do assume that the appropriate tutorial .HTM help files are located in this parent \[destination\] directory.</span></span>

<span data-ttu-id="14792-111">Para la aplicación READTUT de Win32:</span><span class="sxs-lookup"><span data-stu-id="14792-111">For the Win32 READTUT application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

<span data-ttu-id="14792-112">Para la aplicación esqueleto de Win32 EXE:</span><span class="sxs-lookup"><span data-stu-id="14792-112">For the Win32 EXE skeleton application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

<span data-ttu-id="14792-113">Para el esqueleto del archivo DLL de Win32:</span><span class="sxs-lookup"><span data-stu-id="14792-113">For the Win32 DLL skeleton:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

<span data-ttu-id="14792-114">Para los ejemplos de objetos COM básicos:</span><span class="sxs-lookup"><span data-stu-id="14792-114">For the basic COM object samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

<span data-ttu-id="14792-115">Para los ejemplos de cliente/servidor de componentes DLL básicos en proceso:</span><span class="sxs-lookup"><span data-stu-id="14792-115">For the basic in-process DLL component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

<span data-ttu-id="14792-116">Para los ejemplos de cliente/servidor de componente con licencia:</span><span class="sxs-lookup"><span data-stu-id="14792-116">For the licensed component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

<span data-ttu-id="14792-117">Para los ejemplos de serialización estándar:</span><span class="sxs-lookup"><span data-stu-id="14792-117">For the standard marshaling samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

<span data-ttu-id="14792-118">Para los ejemplos de cliente/servidor locales fuera de proceso:</span><span class="sxs-lookup"><span data-stu-id="14792-118">For the out-of-process local client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

<span data-ttu-id="14792-119">Para los ejemplos de cliente/servidor de modelo de apartamento:</span><span class="sxs-lookup"><span data-stu-id="14792-119">For the apartment model client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

<span data-ttu-id="14792-120">Para los ejemplos de cliente/servidor DCOM (COM distribuido):</span><span class="sxs-lookup"><span data-stu-id="14792-120">For the DCOM (Distributed COM) client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

<span data-ttu-id="14792-121">Para los ejemplos de cliente/servidor de subprocesamiento libre:</span><span class="sxs-lookup"><span data-stu-id="14792-121">For the free threading client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

<span data-ttu-id="14792-122">Para los ejemplos de cliente/servidor de objetos COM conectables:</span><span class="sxs-lookup"><span data-stu-id="14792-122">For the connectable COM object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

<span data-ttu-id="14792-123">Para los ejemplos de cliente/servidor de almacenamiento estructurado:</span><span class="sxs-lookup"><span data-stu-id="14792-123">For the structured storage client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

<span data-ttu-id="14792-124">Para los ejemplos de cliente/servidor de objeto persistente:</span><span class="sxs-lookup"><span data-stu-id="14792-124">For the persistent object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

<span data-ttu-id="14792-125">Para los ejemplos de cliente/servidor de seguridad de DCOM:</span><span class="sxs-lookup"><span data-stu-id="14792-125">For the DCOM security client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




