---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 031e78319beb0f62ddb0ea340fca0cd7ed88c0a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357122"
---
# <a name="iagentnotifysinkdragstart"></a><span data-ttu-id="d81e7-103">IAgentNotifySink::D ragStart</span><span class="sxs-lookup"><span data-stu-id="d81e7-103">IAgentNotifySink::DragStart</span></span>

<span data-ttu-id="d81e7-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d81e7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="d81e7-105">Notifica a una aplicación cliente cuando el usuario comienza a arrastrar un carácter.</span><span class="sxs-lookup"><span data-stu-id="d81e7-105">Notifies a client application when the user starts dragging a character.</span></span>

-   <span data-ttu-id="d81e7-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d81e7-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="d81e7-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="d81e7-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="d81e7-108">Identificador del carácter arrastrado.</span><span class="sxs-lookup"><span data-stu-id="d81e7-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="d81e7-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="d81e7-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="d81e7-110">Un parámetro que indica el botón del mouse y el estado de la tecla modificadora.</span><span class="sxs-lookup"><span data-stu-id="d81e7-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="d81e7-111">El parámetro puede devolver cualquier combinación de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d81e7-111">The parameter can return any combination of the following:</span></span>



|        |                  |
|--------|------------------|
| <span data-ttu-id="d81e7-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="d81e7-112">0x0001</span></span> | <span data-ttu-id="d81e7-113">Botón izquierdo</span><span class="sxs-lookup"><span data-stu-id="d81e7-113">Left Button</span></span>      |
| <span data-ttu-id="d81e7-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="d81e7-114">0x0010</span></span> | <span data-ttu-id="d81e7-115">Botón central</span><span class="sxs-lookup"><span data-stu-id="d81e7-115">Middle Button</span></span>    |
| <span data-ttu-id="d81e7-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="d81e7-116">0x0002</span></span> | <span data-ttu-id="d81e7-117">Botón derecho</span><span class="sxs-lookup"><span data-stu-id="d81e7-117">Right Button</span></span>     |
| <span data-ttu-id="d81e7-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="d81e7-118">0x0004</span></span> | <span data-ttu-id="d81e7-119">Tecla Mayús abajo</span><span class="sxs-lookup"><span data-stu-id="d81e7-119">Shift Key Down</span></span>   |
| <span data-ttu-id="d81e7-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="d81e7-120">0x0008</span></span> | <span data-ttu-id="d81e7-121">Tecla control abajo</span><span class="sxs-lookup"><span data-stu-id="d81e7-121">Control Key Down</span></span> |
| <span data-ttu-id="d81e7-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="d81e7-122">0x0020</span></span> | <span data-ttu-id="d81e7-123">Tecla Alt abajo</span><span class="sxs-lookup"><span data-stu-id="d81e7-123">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="d81e7-124"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="d81e7-124"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="d81e7-125">Coordenada x del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="d81e7-125">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="d81e7-126"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="d81e7-126"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="d81e7-127">Coordenada y del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="d81e7-127">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




