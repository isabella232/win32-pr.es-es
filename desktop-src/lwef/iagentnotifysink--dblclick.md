---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88193f228f94d24384e6bf2b874e9208d67f3e9c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120928"
---
# <a name="iagentnotifysinkdblclick"></a><span data-ttu-id="76d04-103">IAgentNotifySink::D blClick</span><span class="sxs-lookup"><span data-stu-id="76d04-103">IAgentNotifySink::DblClick</span></span>

<span data-ttu-id="76d04-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="76d04-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="76d04-105">Notifica a una aplicación cliente cuando el usuario hace doble clic en un carácter.</span><span class="sxs-lookup"><span data-stu-id="76d04-105">Notifies a client application when the user double-clicks a character.</span></span>

-   <span data-ttu-id="76d04-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="76d04-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="76d04-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="76d04-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="76d04-108">Identificador del carácter con doble clic.</span><span class="sxs-lookup"><span data-stu-id="76d04-108">Identifier of the double-clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="76d04-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="76d04-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="76d04-110">Parámetro que indica el botón del mouse y el estado de la tecla modificadora.</span><span class="sxs-lookup"><span data-stu-id="76d04-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="76d04-111">El parámetro puede devolver cualquier combinación de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="76d04-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="76d04-112">Valor</span><span class="sxs-lookup"><span data-stu-id="76d04-112">Value</span></span>  | <span data-ttu-id="76d04-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="76d04-113">Description</span></span>                               |
|--------|------------------------------------------------|
| <span data-ttu-id="76d04-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="76d04-114">0x0001</span></span> | <span data-ttu-id="76d04-115">Botón izquierdo</span><span class="sxs-lookup"><span data-stu-id="76d04-115">Left Button</span></span>                                    |
| <span data-ttu-id="76d04-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="76d04-116">0x0010</span></span> | <span data-ttu-id="76d04-117">Botón Central</span><span class="sxs-lookup"><span data-stu-id="76d04-117">Middle Button</span></span>                                  |
| <span data-ttu-id="76d04-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="76d04-118">0x0002</span></span> | <span data-ttu-id="76d04-119">Botón derecho</span><span class="sxs-lookup"><span data-stu-id="76d04-119">Right Button</span></span>                                   |
| <span data-ttu-id="76d04-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="76d04-120">0x0004</span></span> | <span data-ttu-id="76d04-121">Mayús Key Down</span><span class="sxs-lookup"><span data-stu-id="76d04-121">Shift Key Down</span></span>                                 |
| <span data-ttu-id="76d04-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="76d04-122">0x0008</span></span> | <span data-ttu-id="76d04-123">Control de la tecla Abajo</span><span class="sxs-lookup"><span data-stu-id="76d04-123">Control Key Down</span></span>                               |
| <span data-ttu-id="76d04-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="76d04-124">0x0020</span></span> | <span data-ttu-id="76d04-125">Alt tecla abajo</span><span class="sxs-lookup"><span data-stu-id="76d04-125">Alt Key Down</span></span>                                   |
| <span data-ttu-id="76d04-126">0x1000</span><span class="sxs-lookup"><span data-stu-id="76d04-126">0x1000</span></span> | <span data-ttu-id="76d04-127">Evento en el icono de la barra de tareas del carácter</span><span class="sxs-lookup"><span data-stu-id="76d04-127">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="76d04-128"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="76d04-128"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="76d04-129">Coordenada x del puntero del mouse en píxeles, en relación con el origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="76d04-129">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="76d04-130"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="76d04-130"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="76d04-131">Coordenada y del puntero del mouse en píxeles, en relación con el origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="76d04-131">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="76d04-132">Este evento se envía al cliente activo de entrada del carácter.</span><span class="sxs-lookup"><span data-stu-id="76d04-132">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="76d04-133">Si ninguno de los clientes del carácter está activo de entrada, el servidor notifica al cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="76d04-133">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="76d04-134">Si el carácter está visible, el servidor también activa esa entrada de cliente y envía [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="76d04-134">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="76d04-135">Si el carácter está oculto, el carácter también se muestra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="76d04-135">If the character is hidden, the character is also automatically shown.</span></span>

 

 




