---
title: Eventos secundarios
description: Eventos secundarios
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Aspectos de Windows Media Player, eventos secundarios
- máscaras, eventos secundarios
- eventos, secundarios
- escribir código para máscaras, eventos secundarios
- eventos secundarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486959"
---
# <a name="secondary-events"></a><span data-ttu-id="e16e7-108">Eventos secundarios</span><span class="sxs-lookup"><span data-stu-id="e16e7-108">Secondary Events</span></span>

<span data-ttu-id="e16e7-109">Puede determinar qué otros eventos están teniendo lugar cuando se desencadena un evento específico.</span><span class="sxs-lookup"><span data-stu-id="e16e7-109">You can determine what other events are taking place when a specific event is triggered.</span></span> <span data-ttu-id="e16e7-110">Por ejemplo, cuando se hace clic en un botón del mouse, es posible que desee saber si la tecla ALT estaba presionada al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e16e7-110">For example, when a mouse button is clicked, you may want to know whether the ALT key was down at the same time.</span></span>

## <a name="event-attributes"></a><span data-ttu-id="e16e7-111">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="e16e7-111">Event Attributes</span></span>

<span data-ttu-id="e16e7-112">Se admiten los siguientes atributos de evento para las máscaras:</span><span class="sxs-lookup"><span data-stu-id="e16e7-112">The following event attributes are supported for skins:</span></span>

-   <span data-ttu-id="e16e7-113">**altKey**</span><span class="sxs-lookup"><span data-stu-id="e16e7-113">**altKey**</span></span>
-   <span data-ttu-id="e16e7-114">**botón**</span><span class="sxs-lookup"><span data-stu-id="e16e7-114">**button**</span></span>
-   <span data-ttu-id="e16e7-115">**clientX**</span><span class="sxs-lookup"><span data-stu-id="e16e7-115">**clientX**</span></span>
-   <span data-ttu-id="e16e7-116">**cliente de**</span><span class="sxs-lookup"><span data-stu-id="e16e7-116">**clientY**</span></span>
-   <span data-ttu-id="e16e7-117">**ctrlKey**</span><span class="sxs-lookup"><span data-stu-id="e16e7-117">**ctrlKey**</span></span>
-   <span data-ttu-id="e16e7-118">**fromElement**</span><span class="sxs-lookup"><span data-stu-id="e16e7-118">**fromElement**</span></span>
-   <span data-ttu-id="e16e7-119">**offsetX**</span><span class="sxs-lookup"><span data-stu-id="e16e7-119">**offsetX**</span></span>
-   <span data-ttu-id="e16e7-120">**desplazamiento**</span><span class="sxs-lookup"><span data-stu-id="e16e7-120">**offsetY**</span></span>
-   <span data-ttu-id="e16e7-121">**screenX**</span><span class="sxs-lookup"><span data-stu-id="e16e7-121">**screenX**</span></span>
-   <span data-ttu-id="e16e7-122">**pantalla**</span><span class="sxs-lookup"><span data-stu-id="e16e7-122">**screenY**</span></span>
-   <span data-ttu-id="e16e7-123">**shiftKey**</span><span class="sxs-lookup"><span data-stu-id="e16e7-123">**shiftKey**</span></span>
-   <span data-ttu-id="e16e7-124">**srcElement**</span><span class="sxs-lookup"><span data-stu-id="e16e7-124">**srcElement**</span></span>
-   <span data-ttu-id="e16e7-125">**toElement**</span><span class="sxs-lookup"><span data-stu-id="e16e7-125">**toElement**</span></span>
-   <span data-ttu-id="e16e7-126">**x**</span><span class="sxs-lookup"><span data-stu-id="e16e7-126">**x**</span></span>
-   <span data-ttu-id="e16e7-127">**y**</span><span class="sxs-lookup"><span data-stu-id="e16e7-127">**y**</span></span>
-   <span data-ttu-id="e16e7-128">**keyCode**</span><span class="sxs-lookup"><span data-stu-id="e16e7-128">**keyCode**</span></span>

<span data-ttu-id="e16e7-129">Para obtener más información sobre estos atributos, vea la [referencia de programación](skin-programming-reference.md)de la máscara.</span><span class="sxs-lookup"><span data-stu-id="e16e7-129">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="using-secondary-events"></a><span data-ttu-id="e16e7-130">Usar eventos secundarios</span><span class="sxs-lookup"><span data-stu-id="e16e7-130">Using Secondary Events</span></span>

<span data-ttu-id="e16e7-131">Solo se pueden procesar atributos de evento en el código JScript.</span><span class="sxs-lookup"><span data-stu-id="e16e7-131">You can only process event attributes in JScript code.</span></span> <span data-ttu-id="e16e7-132">Debe usar la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="e16e7-132">You must use the following syntax:</span></span>


```C++
event.eventattributename
```



<span data-ttu-id="e16e7-133">*eventattributename* es el nombre del atributo de evento.</span><span class="sxs-lookup"><span data-stu-id="e16e7-133">*eventattributename* is the name of the event attribute.</span></span> <span data-ttu-id="e16e7-134">Por ejemplo, para determinar si se presionó la tecla ALT durante un evento de clic, podría usar las líneas siguientes en el código JScript:</span><span class="sxs-lookup"><span data-stu-id="e16e7-134">For example, to determine whether the ALT key was pressed during a click event, you could use the following lines in your JScript code:</span></span>


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a><span data-ttu-id="e16e7-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e16e7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e16e7-136">**Controlar eventos**</span><span class="sxs-lookup"><span data-stu-id="e16e7-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




