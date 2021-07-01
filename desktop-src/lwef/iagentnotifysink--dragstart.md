---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33ae89f9e24c6c7b0ec69fba1a98b3a64a18620
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120830"
---
# <a name="iagentnotifysinkdragstart"></a><span data-ttu-id="51568-103">IAgentNotifySink::D ragStart</span><span class="sxs-lookup"><span data-stu-id="51568-103">IAgentNotifySink::DragStart</span></span>

<span data-ttu-id="51568-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51568-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="51568-105">Notifica a una aplicación cliente cuando el usuario comienza a arrastrar un carácter.</span><span class="sxs-lookup"><span data-stu-id="51568-105">Notifies a client application when the user starts dragging a character.</span></span>

-   <span data-ttu-id="51568-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="51568-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="51568-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="51568-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="51568-108">Identificador del carácter arrastrado.</span><span class="sxs-lookup"><span data-stu-id="51568-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="51568-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="51568-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="51568-110">Parámetro que indica el botón del mouse y el estado de la tecla modificadora.</span><span class="sxs-lookup"><span data-stu-id="51568-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="51568-111">El parámetro puede devolver cualquier combinación de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="51568-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="51568-112">Valor</span><span class="sxs-lookup"><span data-stu-id="51568-112">Value</span></span>  | <span data-ttu-id="51568-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="51568-113">Description</span></span>      |
|--------|------------------|
| <span data-ttu-id="51568-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="51568-114">0x0001</span></span> | <span data-ttu-id="51568-115">Botón izquierdo</span><span class="sxs-lookup"><span data-stu-id="51568-115">Left Button</span></span>      |
| <span data-ttu-id="51568-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="51568-116">0x0010</span></span> | <span data-ttu-id="51568-117">Botón Central</span><span class="sxs-lookup"><span data-stu-id="51568-117">Middle Button</span></span>    |
| <span data-ttu-id="51568-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="51568-118">0x0002</span></span> | <span data-ttu-id="51568-119">Botón derecho</span><span class="sxs-lookup"><span data-stu-id="51568-119">Right Button</span></span>     |
| <span data-ttu-id="51568-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="51568-120">0x0004</span></span> | <span data-ttu-id="51568-121">Mayús Key Down</span><span class="sxs-lookup"><span data-stu-id="51568-121">Shift Key Down</span></span>   |
| <span data-ttu-id="51568-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="51568-122">0x0008</span></span> | <span data-ttu-id="51568-123">Tecla De control hacia abajo</span><span class="sxs-lookup"><span data-stu-id="51568-123">Control Key Down</span></span> |
| <span data-ttu-id="51568-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="51568-124">0x0020</span></span> | <span data-ttu-id="51568-125">Tecla Alt hacia abajo</span><span class="sxs-lookup"><span data-stu-id="51568-125">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="51568-126"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="51568-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="51568-127">Coordenada x del puntero del mouse en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="51568-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="51568-128"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="51568-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="51568-129">Coordenada y del puntero del mouse en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="51568-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




