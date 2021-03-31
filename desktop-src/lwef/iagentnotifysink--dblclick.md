---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ec7372d524027588dae5a0a3aafaf07146556e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418706"
---
# <a name="iagentnotifysinkdblclick"></a><span data-ttu-id="8adbc-103">IAgentNotifySink::D blClick</span><span class="sxs-lookup"><span data-stu-id="8adbc-103">IAgentNotifySink::DblClick</span></span>

<span data-ttu-id="8adbc-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8adbc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="8adbc-105">Notifica a una aplicación cliente cuando el usuario hace doble clic en un carácter.</span><span class="sxs-lookup"><span data-stu-id="8adbc-105">Notifies a client application when the user double-clicks a character.</span></span>

-   <span data-ttu-id="8adbc-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8adbc-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="8adbc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="8adbc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="8adbc-108">Identificador del carácter doble clic.</span><span class="sxs-lookup"><span data-stu-id="8adbc-108">Identifier of the double-clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="8adbc-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="8adbc-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="8adbc-110">Un parámetro que indica el botón del mouse y el estado de la tecla modificadora.</span><span class="sxs-lookup"><span data-stu-id="8adbc-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="8adbc-111">El parámetro puede devolver cualquier combinación de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8adbc-111">The parameter can return any combination of the following:</span></span>



|        |                                                |
|--------|------------------------------------------------|
| <span data-ttu-id="8adbc-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="8adbc-112">0x0001</span></span> | <span data-ttu-id="8adbc-113">Botón izquierdo</span><span class="sxs-lookup"><span data-stu-id="8adbc-113">Left Button</span></span>                                    |
| <span data-ttu-id="8adbc-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="8adbc-114">0x0010</span></span> | <span data-ttu-id="8adbc-115">Botón central</span><span class="sxs-lookup"><span data-stu-id="8adbc-115">Middle Button</span></span>                                  |
| <span data-ttu-id="8adbc-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="8adbc-116">0x0002</span></span> | <span data-ttu-id="8adbc-117">Botón derecho</span><span class="sxs-lookup"><span data-stu-id="8adbc-117">Right Button</span></span>                                   |
| <span data-ttu-id="8adbc-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="8adbc-118">0x0004</span></span> | <span data-ttu-id="8adbc-119">Tecla Mayús abajo</span><span class="sxs-lookup"><span data-stu-id="8adbc-119">Shift Key Down</span></span>                                 |
| <span data-ttu-id="8adbc-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="8adbc-120">0x0008</span></span> | <span data-ttu-id="8adbc-121">Tecla control abajo</span><span class="sxs-lookup"><span data-stu-id="8adbc-121">Control Key Down</span></span>                               |
| <span data-ttu-id="8adbc-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="8adbc-122">0x0020</span></span> | <span data-ttu-id="8adbc-123">Tecla Alt abajo</span><span class="sxs-lookup"><span data-stu-id="8adbc-123">Alt Key Down</span></span>                                   |
| <span data-ttu-id="8adbc-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="8adbc-124">0x1000</span></span> | <span data-ttu-id="8adbc-125">Evento producido en el icono de la barra de tareas del carácter</span><span class="sxs-lookup"><span data-stu-id="8adbc-125">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="8adbc-126"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="8adbc-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="8adbc-127">Coordenada x del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="8adbc-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="8adbc-128"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="8adbc-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="8adbc-129">Coordenada y del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="8adbc-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="8adbc-130">Este evento se envía al cliente de entrada-activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="8adbc-130">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="8adbc-131">Si ninguno de los clientes del carácter es de entrada-activo, el servidor notifica al cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="8adbc-131">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="8adbc-132">Si el carácter está visible, el servidor también hace que la entrada del cliente esté activa y envía [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="8adbc-132">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="8adbc-133">Si el carácter está oculto, el carácter también se muestra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8adbc-133">If the character is hidden, the character is also automatically shown.</span></span>

 

 




