---
description: El evento ShowMenu se envía cuando el disco habilita o deshabilita el modo en que se muestra un menú.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997885"
---
# <a name="showmenu"></a><span data-ttu-id="6c345-103">ShowMenu</span><span class="sxs-lookup"><span data-stu-id="6c345-103">ShowMenu</span></span>

> [!Note]  
> <span data-ttu-id="6c345-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6c345-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6c345-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="6c345-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6c345-106">El `ShowMenu` evento se envía cuando el disco habilita o deshabilita el modo en que se muestra un menú.</span><span class="sxs-lookup"><span data-stu-id="6c345-106">The `ShowMenu` event is sent when the disc enables or disables the showing of a menu.</span></span>

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a><span data-ttu-id="6c345-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c345-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c345-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span><span class="sxs-lookup"><span data-stu-id="6c345-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span></span>
</dt> <dd>

<span data-ttu-id="6c345-109">Especifica el menú que se ha habilitado o deshabilitado como valor numérico.</span><span class="sxs-lookup"><span data-stu-id="6c345-109">Specifies which menu has been enabled or disabled as a Number value.</span></span>



| <span data-ttu-id="6c345-110">Value</span><span class="sxs-lookup"><span data-stu-id="6c345-110">Value</span></span> | <span data-ttu-id="6c345-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c345-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="6c345-112">2</span><span class="sxs-lookup"><span data-stu-id="6c345-112">2</span></span>     | <span data-ttu-id="6c345-113">Título</span><span class="sxs-lookup"><span data-stu-id="6c345-113">Title</span></span>       |
| <span data-ttu-id="6c345-114">3</span><span class="sxs-lookup"><span data-stu-id="6c345-114">3</span></span>     | <span data-ttu-id="6c345-115">Root</span><span class="sxs-lookup"><span data-stu-id="6c345-115">Root</span></span>        |
| <span data-ttu-id="6c345-116">4</span><span class="sxs-lookup"><span data-stu-id="6c345-116">4</span></span>     | <span data-ttu-id="6c345-117">Subimagen</span><span class="sxs-lookup"><span data-stu-id="6c345-117">Subpicture</span></span>  |
| <span data-ttu-id="6c345-118">5</span><span class="sxs-lookup"><span data-stu-id="6c345-118">5</span></span>     | <span data-ttu-id="6c345-119">Audio</span><span class="sxs-lookup"><span data-stu-id="6c345-119">Audio</span></span>       |
| <span data-ttu-id="6c345-120">6</span><span class="sxs-lookup"><span data-stu-id="6c345-120">6</span></span>     | <span data-ttu-id="6c345-121">Ángulo</span><span class="sxs-lookup"><span data-stu-id="6c345-121">Angle</span></span>       |
| <span data-ttu-id="6c345-122">7</span><span class="sxs-lookup"><span data-stu-id="6c345-122">7</span></span>     | <span data-ttu-id="6c345-123">Capítulo</span><span class="sxs-lookup"><span data-stu-id="6c345-123">Chapter</span></span>     |



 

</dd> <dt>

<span data-ttu-id="6c345-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="6c345-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="6c345-125">Especifica si la operación está habilitada o deshabilitada como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="6c345-125">Specifies whether the operation is enabled or disabled as a Boolean.</span></span>

</dd> </dl>

 

 



