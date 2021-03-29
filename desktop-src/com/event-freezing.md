---
title: Congelación de eventos
description: Congelación de eventos
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903424"
---
# <a name="event-freezing"></a><span data-ttu-id="f3def-103">Congelación de eventos</span><span class="sxs-lookup"><span data-stu-id="f3def-103">Event Freezing</span></span>

<span data-ttu-id="f3def-104">Un contenedor puede notificar a un control que no está listo para responder a eventos mediante una llamada a [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **true**.</span><span class="sxs-lookup"><span data-stu-id="f3def-104">A container can notify a control that it is not ready to respond to events by calling [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE**.</span></span> <span data-ttu-id="f3def-105">Puede liberar los eventos llamando a **FreezeEvents** con **false**.</span><span class="sxs-lookup"><span data-stu-id="f3def-105">It can unfreeze the events by calling **FreezeEvents** with **FALSE**.</span></span> <span data-ttu-id="f3def-106">Cuando un contenedor inmoviliza eventos, está inmovilizando el procesamiento de eventos, no la recepción de eventos; es decir, un contenedor todavía puede recibir eventos mientras los eventos se inmovilizan.</span><span class="sxs-lookup"><span data-stu-id="f3def-106">When a container freezes events, it is freezing event processing, not event receiving; that is, a container can still receive events while events are frozen.</span></span> <span data-ttu-id="f3def-107">Si un contenedor recibe una notificación de eventos mientras sus eventos están inmovilizados, el contenedor debe omitir el evento.</span><span class="sxs-lookup"><span data-stu-id="f3def-107">If a container receives an event notification while its events are frozen, the container should ignore the event.</span></span> <span data-ttu-id="f3def-108">No es adecuado ninguna otra acción.</span><span class="sxs-lookup"><span data-stu-id="f3def-108">No other action is appropriate.</span></span>

<span data-ttu-id="f3def-109">Un control debe tomar nota de la llamada de un contenedor a [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **true** si es importante para el control que no se ha perdido un evento.</span><span class="sxs-lookup"><span data-stu-id="f3def-109">A control should take note of a container's call to [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE** if it is important to the control that an event is not missed.</span></span> <span data-ttu-id="f3def-110">Mientras el procesamiento de eventos de un contenedor está inmovilizado, un control debe implementar una de las técnicas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f3def-110">While a container's event processing is frozen, a control should implement one of the following techniques:</span></span>

-   <span data-ttu-id="f3def-111">Active los eventos en el conocimiento completo de que el contenedor no realizará ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="f3def-111">Fire the events in the full knowledge that the container will take no action.</span></span>
-   <span data-ttu-id="f3def-112">Descartar todos los eventos que el control habría desencadenado.</span><span class="sxs-lookup"><span data-stu-id="f3def-112">Discard all events that the control would have fired.</span></span>
-   <span data-ttu-id="f3def-113">Poner en cola todos los eventos pendientes y activarlos después de que el contenedor haya llamado a [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **false**.</span><span class="sxs-lookup"><span data-stu-id="f3def-113">Queue up all pending events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>
-   <span data-ttu-id="f3def-114">Poner en cola solo eventos relevantes o importantes y activarlos después de que el contenedor haya llamado a [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **false**.</span><span class="sxs-lookup"><span data-stu-id="f3def-114">Queue up only relevant or important events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>

<span data-ttu-id="f3def-115">Cada técnica es aceptable y adecuada en diferentes circunstancias.</span><span class="sxs-lookup"><span data-stu-id="f3def-115">Each technique is acceptable and appropriate in different circumstances.</span></span> <span data-ttu-id="f3def-116">El desarrollador del control es responsable de determinar e implementar la técnica adecuada para la funcionalidad del control.</span><span class="sxs-lookup"><span data-stu-id="f3def-116">The control developer is responsible for determining and implementing the appropriate technique for the control's functionality.</span></span>

 

 




