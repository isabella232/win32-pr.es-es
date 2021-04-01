---
title: IAgentNotifySink clic
description: IAgentNotifySink clic
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d1dccd838152503c603d158f043a0279d4b5c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075916"
---
# <a name="iagentnotifysinkclick"></a><span data-ttu-id="519a5-103">IAgentNotifySink:: click</span><span class="sxs-lookup"><span data-stu-id="519a5-103">IAgentNotifySink::Click</span></span>

<span data-ttu-id="519a5-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="519a5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="519a5-105">Notifica a una aplicación cliente cuando el usuario hace clic en el icono de la barra de tareas de un carácter o un carácter.</span><span class="sxs-lookup"><span data-stu-id="519a5-105">Notifies a client application when the user clicks a character or character's taskbar icon.</span></span>

-   <span data-ttu-id="519a5-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="519a5-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="519a5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="519a5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="519a5-108">Identificador del carácter en el que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="519a5-108">Identifier of the clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="519a5-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="519a5-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="519a5-110">Un parámetro que indica el botón del mouse y el estado de la tecla modificadora.</span><span class="sxs-lookup"><span data-stu-id="519a5-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="519a5-111">El parámetro puede devolver cualquier combinación de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="519a5-111">The parameter can return any combination of the following:</span></span>



|        |                                                |
|--------|------------------------------------------------|
| <span data-ttu-id="519a5-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="519a5-112">0x0001</span></span> | <span data-ttu-id="519a5-113">Botón izquierdo</span><span class="sxs-lookup"><span data-stu-id="519a5-113">Left Button</span></span>                                    |
| <span data-ttu-id="519a5-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="519a5-114">0x0010</span></span> | <span data-ttu-id="519a5-115">Botón central</span><span class="sxs-lookup"><span data-stu-id="519a5-115">Middle Button</span></span>                                  |
| <span data-ttu-id="519a5-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="519a5-116">0x0002</span></span> | <span data-ttu-id="519a5-117">Botón derecho</span><span class="sxs-lookup"><span data-stu-id="519a5-117">Right Button</span></span>                                   |
| <span data-ttu-id="519a5-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="519a5-118">0x0004</span></span> | <span data-ttu-id="519a5-119">Tecla Mayús abajo</span><span class="sxs-lookup"><span data-stu-id="519a5-119">Shift Key Down</span></span>                                 |
| <span data-ttu-id="519a5-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="519a5-120">0x0008</span></span> | <span data-ttu-id="519a5-121">Tecla control abajo</span><span class="sxs-lookup"><span data-stu-id="519a5-121">Control Key Down</span></span>                               |
| <span data-ttu-id="519a5-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="519a5-122">0x0020</span></span> | <span data-ttu-id="519a5-123">Tecla Alt abajo</span><span class="sxs-lookup"><span data-stu-id="519a5-123">Alt Key Down</span></span>                                   |
| <span data-ttu-id="519a5-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="519a5-124">0x1000</span></span> | <span data-ttu-id="519a5-125">Evento producido en el icono de la barra de tareas del carácter</span><span class="sxs-lookup"><span data-stu-id="519a5-125">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="519a5-126"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="519a5-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="519a5-127">Coordenada x del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="519a5-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="519a5-128"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="519a5-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="519a5-129">Coordenada y del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="519a5-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="519a5-130">Este evento se envía al cliente de entrada-activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="519a5-130">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="519a5-131">Si ninguno de los clientes del carácter es de entrada-activo, el servidor notifica al cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="519a5-131">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="519a5-132">Si el carácter está visible, el servidor también hace que la entrada del cliente esté activa y envía [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="519a5-132">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="519a5-133">Si el carácter está oculto, el carácter también se muestra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="519a5-133">If the character hidden, the character is also automatically shown.</span></span>

 

 




