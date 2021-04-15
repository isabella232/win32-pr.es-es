---
title: Eventos externos
description: Eventos externos
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Aspectos de Windows Media Player, eventos externos
- máscaras, eventos externos
- eventos, externos
- escribir código para máscaras, eventos externos
- eventos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695448"
---
# <a name="external-events"></a><span data-ttu-id="e5629-108">Eventos externos</span><span class="sxs-lookup"><span data-stu-id="e5629-108">External Events</span></span>

<span data-ttu-id="e5629-109">Cuando los usuarios hacen clic en un botón o presionan una tecla, puede responder a su entrada con los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="e5629-109">When users click a button or press a key, you can respond to their input with event handlers.</span></span> <span data-ttu-id="e5629-110">Un controlador de eventos es una sección de código que se ejecuta cada vez que se desencadena el evento.</span><span class="sxs-lookup"><span data-stu-id="e5629-110">An event handler is a section of code that runs whenever the event is triggered.</span></span>

<span data-ttu-id="e5629-111">Los elementos de máscara admiten los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="e5629-111">The following events are supported by skin elements:</span></span>

-   <span data-ttu-id="e5629-112">**carga**</span><span class="sxs-lookup"><span data-stu-id="e5629-112">**load**</span></span>
-   <span data-ttu-id="e5629-113">**close**</span><span class="sxs-lookup"><span data-stu-id="e5629-113">**close**</span></span>
-   <span data-ttu-id="e5629-114">**cambiar el tamaño**</span><span class="sxs-lookup"><span data-stu-id="e5629-114">**resize**</span></span>
-   <span data-ttu-id="e5629-115">**temporizador**</span><span class="sxs-lookup"><span data-stu-id="e5629-115">**timer**</span></span>
-   <span data-ttu-id="e5629-116">**hizo**</span><span class="sxs-lookup"><span data-stu-id="e5629-116">**click**</span></span>
-   <span data-ttu-id="e5629-117">**dblclick**</span><span class="sxs-lookup"><span data-stu-id="e5629-117">**dblclick**</span></span>
-   <span data-ttu-id="e5629-118">**error**</span><span class="sxs-lookup"><span data-stu-id="e5629-118">**error**</span></span>
-   <span data-ttu-id="e5629-119">**mousedown**</span><span class="sxs-lookup"><span data-stu-id="e5629-119">**mousedown**</span></span>
-   <span data-ttu-id="e5629-120">**mouseup**</span><span class="sxs-lookup"><span data-stu-id="e5629-120">**mouseup**</span></span>
-   <span data-ttu-id="e5629-121">**mousemove**</span><span class="sxs-lookup"><span data-stu-id="e5629-121">**mousemove**</span></span>
-   <span data-ttu-id="e5629-122">**mouseover**</span><span class="sxs-lookup"><span data-stu-id="e5629-122">**mouseover**</span></span>
-   <span data-ttu-id="e5629-123">**mouseout**</span><span class="sxs-lookup"><span data-stu-id="e5629-123">**mouseout**</span></span>
-   <span data-ttu-id="e5629-124">**keypress**</span><span class="sxs-lookup"><span data-stu-id="e5629-124">**keypress**</span></span>
-   <span data-ttu-id="e5629-125">**keydown**</span><span class="sxs-lookup"><span data-stu-id="e5629-125">**keydown**</span></span>
-   <span data-ttu-id="e5629-126">**keyup**</span><span class="sxs-lookup"><span data-stu-id="e5629-126">**keyup**</span></span>

<span data-ttu-id="e5629-127">Vea la [referencia de programación](skin-programming-reference.md) de la máscara para obtener más detalles sobre eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="e5629-127">See the [Skin Programming Reference](skin-programming-reference.md) for more details about specific events.</span></span>

<span data-ttu-id="e5629-128">Un controlador de eventos externo típico asignaría un nombre al evento y definiría el código que se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="e5629-128">A typical external event handler would name the event and define the code that will run.</span></span> <span data-ttu-id="e5629-129">Por ejemplo, si desea crear código para iniciar Windows Media Player cuando el usuario hace clic en un botón, colocaría la siguiente línea en el código del botón.</span><span class="sxs-lookup"><span data-stu-id="e5629-129">For example, if you want to create code to start Windows Media Player when the user clicks on a button, you would put the following line in your button code.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



<span data-ttu-id="e5629-130">Se reproducirá el archivo denominado Laure. WMA.</span><span class="sxs-lookup"><span data-stu-id="e5629-130">This will play the file named laure.wma.</span></span> <span data-ttu-id="e5629-131">Tenga en cuenta que agrega la palabra "ON" a eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="e5629-131">Note that you add the word "on" to specific events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5629-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5629-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5629-133">**Controlar eventos**</span><span class="sxs-lookup"><span data-stu-id="e5629-133">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




