---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077674"
---
# <a name="iagentnotifysink"></a><span data-ttu-id="51c36-103">IAgentNotifySink</span><span class="sxs-lookup"><span data-stu-id="51c36-103">IAgentNotifySink</span></span>

<span data-ttu-id="51c36-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51c36-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="51c36-105">IAgentNotifySink notifica a los clientes cuando se producen determinados cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="51c36-105">IAgentNotifySink notifies clients when certain state changes occur.</span></span> <span data-ttu-id="51c36-106">Estas funciones también están disponibles en [IAgentNotifySinkEx](iagentnotifysinkex.md).</span><span class="sxs-lookup"><span data-stu-id="51c36-106">These functions are also available from [IAgentNotifySinkEx](iagentnotifysinkex.md).</span></span>

<span data-ttu-id="51c36-107">**Métodos en orden de Vtable**</span><span class="sxs-lookup"><span data-stu-id="51c36-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="51c36-108">IAgentNotifySink</span><span class="sxs-lookup"><span data-stu-id="51c36-108">IAgentNotifySink</span></span>                                                      | <span data-ttu-id="51c36-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="51c36-109">Description</span></span>                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51c36-110">**Command**</span><span class="sxs-lookup"><span data-stu-id="51c36-110">**Command**</span></span>](command-method.md)                                     | <span data-ttu-id="51c36-111">Se produce cuando el servidor procesa un comando definido por el cliente.</span><span class="sxs-lookup"><span data-stu-id="51c36-111">Occurs when the server processes a client-defined command.</span></span>                               |
| [<span data-ttu-id="51c36-112">**ActivateInputState**</span><span class="sxs-lookup"><span data-stu-id="51c36-112">**ActivateInputState**</span></span>](iagentnotifysink--activateinputstate.md)    | <span data-ttu-id="51c36-113">Se produce cuando un carácter entra o deja de ser de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="51c36-113">Occurs when a character becomes or ceases to be input-active.</span></span>                            |
| [<span data-ttu-id="51c36-114">**BalloonVisibleState**</span><span class="sxs-lookup"><span data-stu-id="51c36-114">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="51c36-115">Se produce cuando cambia el estado **visible** del carácter.</span><span class="sxs-lookup"><span data-stu-id="51c36-115">Occurs when the character's **Visible** state changes.</span></span>                                   |
| [<span data-ttu-id="51c36-116">**Evento de clic**</span><span class="sxs-lookup"><span data-stu-id="51c36-116">**Click Event**</span></span>](click-event.md)                                    | <span data-ttu-id="51c36-117">Se produce cuando se hace clic en un carácter.</span><span class="sxs-lookup"><span data-stu-id="51c36-117">Occurs when a character is clicked.</span></span>                                                      |
| [<span data-ttu-id="51c36-118">**Evento DblClick**</span><span class="sxs-lookup"><span data-stu-id="51c36-118">**DblClick Event**</span></span>](dblclick-event.md)                              | <span data-ttu-id="51c36-119">Se produce cuando se hace doble clic en un carácter.</span><span class="sxs-lookup"><span data-stu-id="51c36-119">Occurs when a character is double-clicked.</span></span>                                               |
| [<span data-ttu-id="51c36-120">**DragStart**</span><span class="sxs-lookup"><span data-stu-id="51c36-120">**DragStart**</span></span>](/windows/desktop/lwef/dragstart-event)                                | <span data-ttu-id="51c36-121">Se produce cuando un usuario comienza a arrastrar un carácter.</span><span class="sxs-lookup"><span data-stu-id="51c36-121">Occurs when a user starts dragging a character.</span></span>                                          |
| [<span data-ttu-id="51c36-122">**DragComplete**</span><span class="sxs-lookup"><span data-stu-id="51c36-122">**DragComplete**</span></span>](https://www.bing.com/search?q=**DragComplete**)                          | <span data-ttu-id="51c36-123">Se produce cuando un usuario deja de arrastrar un carácter.</span><span class="sxs-lookup"><span data-stu-id="51c36-123">Occurs when a user stops dragging a character.</span></span>                                           |
| [<span data-ttu-id="51c36-124">**RequestStart**</span><span class="sxs-lookup"><span data-stu-id="51c36-124">**RequestStart**</span></span>](iagentnotifysink--requeststart.md)                | <span data-ttu-id="51c36-125">Se produce cuando el servidor comienza a procesar un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="51c36-125">Occurs when the server begins processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>    |
| [<span data-ttu-id="51c36-126">**RequestComplete**</span><span class="sxs-lookup"><span data-stu-id="51c36-126">**RequestComplete**</span></span>](iagentnotifysink--requestcomplete.md)          | <span data-ttu-id="51c36-127">Se produce cuando el servidor finaliza el procesamiento de un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="51c36-127">Occurs when the server completes processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> |
| [<span data-ttu-id="51c36-128">**Marcador**</span><span class="sxs-lookup"><span data-stu-id="51c36-128">**Bookmark**</span></span>](iagentnotifysink--bookmark.md)                        | <span data-ttu-id="51c36-129">Se produce cuando el servidor procesa un marcador.</span><span class="sxs-lookup"><span data-stu-id="51c36-129">Occurs when the server processes a bookmark.</span></span>                                             |
| [<span data-ttu-id="51c36-130">**Activos**</span><span class="sxs-lookup"><span data-stu-id="51c36-130">**Idle**</span></span>](iagentnotifysink--idle.md)                                | <span data-ttu-id="51c36-131">Se produce cuando el servidor inicia o finaliza el procesamiento inactivo.</span><span class="sxs-lookup"><span data-stu-id="51c36-131">Occurs when the server starts or ends idle processing.</span></span>                                   |
| [<span data-ttu-id="51c36-132">**Move**</span><span class="sxs-lookup"><span data-stu-id="51c36-132">**Move**</span></span>](iagentnotifysink--move.md)                                | <span data-ttu-id="51c36-133">Se produce cuando se mueve un carácter.</span><span class="sxs-lookup"><span data-stu-id="51c36-133">Occurs when a character has been moved.</span></span>                                                  |
| [<span data-ttu-id="51c36-134">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="51c36-134">**Size**</span></span>](iagentnotifysink---size.md)                               | <span data-ttu-id="51c36-135">Se produce cuando se ha cambiado el tamaño de un carácter.</span><span class="sxs-lookup"><span data-stu-id="51c36-135">Occurs when a character has been resized.</span></span>                                                |
| [<span data-ttu-id="51c36-136">**BalloonVisibleState**</span><span class="sxs-lookup"><span data-stu-id="51c36-136">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="51c36-137">Se produce cuando cambia el estado de visibilidad del globo de palabras de un carácter.</span><span class="sxs-lookup"><span data-stu-id="51c36-137">Occurs when the visibility state of a character's word balloon changes.</span></span>                  |



 

<span data-ttu-id="51c36-138">Los eventos IAgentNotifySink:: restart y IAgentNotifySink:: shutdown, que se admiten en versiones anteriores de Microsoft Agent, ahora están obsoletos.</span><span class="sxs-lookup"><span data-stu-id="51c36-138">The IAgentNotifySink::Restart and IAgentNotifySink::Shutdown events, supported in earlier versions of Microsoft Agent, are now obsolete.</span></span> <span data-ttu-id="51c36-139">Aunque se admite por compatibilidad con versiones anteriores, el servidor ya no envía estos eventos.</span><span class="sxs-lookup"><span data-stu-id="51c36-139">While supported for backward compatibility, the server no longer sends these events.</span></span>

 

 