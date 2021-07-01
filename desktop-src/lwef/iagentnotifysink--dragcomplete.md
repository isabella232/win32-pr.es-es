---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb93fbc7bae1ac43d534962659b850561bd50a6d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120810"
---
# <a name="iagentnotifysinkdragcomplete"></a><span data-ttu-id="b4ac9-103">IAgentNotifySink::D ragComplete</span><span class="sxs-lookup"><span data-stu-id="b4ac9-103">IAgentNotifySink::DragComplete</span></span>

<span data-ttu-id="b4ac9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b4ac9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="b4ac9-105">Notifica a una aplicación cliente cuando el usuario deja de arrastrar un carácter.</span><span class="sxs-lookup"><span data-stu-id="b4ac9-105">Notifies a client application when the user stops dragging a character.</span></span>

-   <span data-ttu-id="b4ac9-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b4ac9-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="b4ac9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="b4ac9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="b4ac9-108">Identificador del carácter arrastrado.</span><span class="sxs-lookup"><span data-stu-id="b4ac9-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="b4ac9-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="b4ac9-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="b4ac9-110">Parámetro que indica el botón del mouse y el estado de la tecla modificadora.</span><span class="sxs-lookup"><span data-stu-id="b4ac9-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="b4ac9-111">El parámetro puede devolver cualquier combinación de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b4ac9-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="b4ac9-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b4ac9-112">Value</span></span>  | <span data-ttu-id="b4ac9-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4ac9-113">Description</span></span>      |
|--------|------------------|
| <span data-ttu-id="b4ac9-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="b4ac9-114">0x0001</span></span> | <span data-ttu-id="b4ac9-115">Botón izquierdo</span><span class="sxs-lookup"><span data-stu-id="b4ac9-115">Left Button</span></span>      |
| <span data-ttu-id="b4ac9-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="b4ac9-116">0x0010</span></span> | <span data-ttu-id="b4ac9-117">Botón Central</span><span class="sxs-lookup"><span data-stu-id="b4ac9-117">Middle Button</span></span>    |
| <span data-ttu-id="b4ac9-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="b4ac9-118">0x0002</span></span> | <span data-ttu-id="b4ac9-119">Botón derecho</span><span class="sxs-lookup"><span data-stu-id="b4ac9-119">Right Button</span></span>     |
| <span data-ttu-id="b4ac9-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="b4ac9-120">0x0004</span></span> | <span data-ttu-id="b4ac9-121">Mayús Key Down</span><span class="sxs-lookup"><span data-stu-id="b4ac9-121">Shift Key Down</span></span>   |
| <span data-ttu-id="b4ac9-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="b4ac9-122">0x0008</span></span> | <span data-ttu-id="b4ac9-123">Tecla De control hacia abajo</span><span class="sxs-lookup"><span data-stu-id="b4ac9-123">Control Key Down</span></span> |
| <span data-ttu-id="b4ac9-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="b4ac9-124">0x0020</span></span> | <span data-ttu-id="b4ac9-125">Tecla Alt hacia abajo</span><span class="sxs-lookup"><span data-stu-id="b4ac9-125">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="b4ac9-126"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="b4ac9-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="b4ac9-127">Coordenada x del puntero del mouse en píxeles, en relación con el origen de la pantalla (esquina superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="b4ac9-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="b4ac9-128"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="b4ac9-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="b4ac9-129">Coordenada y del puntero del mouse en píxeles, en relación con el origen de la pantalla (esquina superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="b4ac9-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




