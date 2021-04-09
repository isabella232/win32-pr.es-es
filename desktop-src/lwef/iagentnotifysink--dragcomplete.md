---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53215591e3d2797c5b57e5586ccb13fc91f5902
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076240"
---
# <a name="iagentnotifysinkdragcomplete"></a><span data-ttu-id="a98f0-103">IAgentNotifySink::D ragComplete</span><span class="sxs-lookup"><span data-stu-id="a98f0-103">IAgentNotifySink::DragComplete</span></span>

<span data-ttu-id="a98f0-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a98f0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="a98f0-105">Notifica a una aplicación cliente cuando el usuario deja de arrastrar un carácter.</span><span class="sxs-lookup"><span data-stu-id="a98f0-105">Notifies a client application when the user stops dragging a character.</span></span>

-   <span data-ttu-id="a98f0-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a98f0-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="a98f0-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="a98f0-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="a98f0-108">Identificador del carácter arrastrado.</span><span class="sxs-lookup"><span data-stu-id="a98f0-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="a98f0-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="a98f0-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="a98f0-110">Un parámetro que indica el botón del mouse y el estado de la tecla modificadora.</span><span class="sxs-lookup"><span data-stu-id="a98f0-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="a98f0-111">El parámetro puede devolver cualquier combinación de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a98f0-111">The parameter can return any combination of the following:</span></span>



|        |                  |
|--------|------------------|
| <span data-ttu-id="a98f0-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="a98f0-112">0x0001</span></span> | <span data-ttu-id="a98f0-113">Botón izquierdo</span><span class="sxs-lookup"><span data-stu-id="a98f0-113">Left Button</span></span>      |
| <span data-ttu-id="a98f0-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="a98f0-114">0x0010</span></span> | <span data-ttu-id="a98f0-115">Botón central</span><span class="sxs-lookup"><span data-stu-id="a98f0-115">Middle Button</span></span>    |
| <span data-ttu-id="a98f0-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="a98f0-116">0x0002</span></span> | <span data-ttu-id="a98f0-117">Botón derecho</span><span class="sxs-lookup"><span data-stu-id="a98f0-117">Right Button</span></span>     |
| <span data-ttu-id="a98f0-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="a98f0-118">0x0004</span></span> | <span data-ttu-id="a98f0-119">Tecla Mayús abajo</span><span class="sxs-lookup"><span data-stu-id="a98f0-119">Shift Key Down</span></span>   |
| <span data-ttu-id="a98f0-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="a98f0-120">0x0008</span></span> | <span data-ttu-id="a98f0-121">Tecla control abajo</span><span class="sxs-lookup"><span data-stu-id="a98f0-121">Control Key Down</span></span> |
| <span data-ttu-id="a98f0-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="a98f0-122">0x0020</span></span> | <span data-ttu-id="a98f0-123">Tecla Alt abajo</span><span class="sxs-lookup"><span data-stu-id="a98f0-123">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="a98f0-124"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="a98f0-124"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="a98f0-125">Coordenada x del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="a98f0-125">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="a98f0-126"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="a98f0-126"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="a98f0-127">Coordenada y del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="a98f0-127">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




