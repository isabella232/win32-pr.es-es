---
title: Clic en IAgentNotifySink
description: Clic en IAgentNotifySink
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0e63244a89467225a7bfd045af6dc112431d12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120908"
---
# <a name="iagentnotifysinkclick"></a><span data-ttu-id="63949-103">IAgentNotifySink::Click</span><span class="sxs-lookup"><span data-stu-id="63949-103">IAgentNotifySink::Click</span></span>

<span data-ttu-id="63949-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="63949-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="63949-105">Notifica a una aplicación cliente cuando el usuario hace clic en el icono de la barra de tareas de un carácter o carácter.</span><span class="sxs-lookup"><span data-stu-id="63949-105">Notifies a client application when the user clicks a character or character's taskbar icon.</span></span>

-   <span data-ttu-id="63949-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="63949-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="63949-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="63949-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="63949-108">Identificador del carácter en el que se ha hecho clic.</span><span class="sxs-lookup"><span data-stu-id="63949-108">Identifier of the clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="63949-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="63949-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="63949-110">Parámetro que indica el botón del mouse y el estado de la tecla modificadora.</span><span class="sxs-lookup"><span data-stu-id="63949-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="63949-111">El parámetro puede devolver cualquier combinación de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="63949-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="63949-112">Valor</span><span class="sxs-lookup"><span data-stu-id="63949-112">Value</span></span>  | <span data-ttu-id="63949-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="63949-113">Description</span></span>                                    |
|--------|------------------------------------------------|
| <span data-ttu-id="63949-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="63949-114">0x0001</span></span> | <span data-ttu-id="63949-115">Botón izquierdo</span><span class="sxs-lookup"><span data-stu-id="63949-115">Left Button</span></span>                                    |
| <span data-ttu-id="63949-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="63949-116">0x0010</span></span> | <span data-ttu-id="63949-117">Botón Central</span><span class="sxs-lookup"><span data-stu-id="63949-117">Middle Button</span></span>                                  |
| <span data-ttu-id="63949-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="63949-118">0x0002</span></span> | <span data-ttu-id="63949-119">Botón derecho</span><span class="sxs-lookup"><span data-stu-id="63949-119">Right Button</span></span>                                   |
| <span data-ttu-id="63949-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="63949-120">0x0004</span></span> | <span data-ttu-id="63949-121">Mayús Key Down</span><span class="sxs-lookup"><span data-stu-id="63949-121">Shift Key Down</span></span>                                 |
| <span data-ttu-id="63949-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="63949-122">0x0008</span></span> | <span data-ttu-id="63949-123">Control de la tecla Abajo</span><span class="sxs-lookup"><span data-stu-id="63949-123">Control Key Down</span></span>                               |
| <span data-ttu-id="63949-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="63949-124">0x0020</span></span> | <span data-ttu-id="63949-125">Alt tecla abajo</span><span class="sxs-lookup"><span data-stu-id="63949-125">Alt Key Down</span></span>                                   |
| <span data-ttu-id="63949-126">0x1000</span><span class="sxs-lookup"><span data-stu-id="63949-126">0x1000</span></span> | <span data-ttu-id="63949-127">Evento en el icono de la barra de tareas del carácter</span><span class="sxs-lookup"><span data-stu-id="63949-127">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="63949-128"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="63949-128"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="63949-129">Coordenada x del puntero del mouse en píxeles, en relación con el origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="63949-129">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="63949-130"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="63949-130"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="63949-131">Coordenada y del puntero del mouse en píxeles, en relación con el origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="63949-131">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="63949-132">Este evento se envía al cliente activo de entrada del carácter.</span><span class="sxs-lookup"><span data-stu-id="63949-132">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="63949-133">Si ninguno de los clientes del carácter está activo de entrada, el servidor notifica al cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="63949-133">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="63949-134">Si el carácter está visible, el servidor también activa esa entrada de cliente y envía [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="63949-134">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="63949-135">Si el carácter está oculto, el carácter también se muestra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="63949-135">If the character hidden, the character is also automatically shown.</span></span>

 

 




