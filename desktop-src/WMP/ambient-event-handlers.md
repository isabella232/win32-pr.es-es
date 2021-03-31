---
title: Controladores de eventos de ambiente
description: Controladores de eventos de ambiente
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Aspectos de Windows Media Player, controladores de eventos de ambiente
- máscaras, controladores de eventos de ambiente
- referencia para máscaras, controladores de eventos de ambiente
- Controladores de eventos de ambiente
- eventos, ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418479"
---
# <a name="ambient-event-handlers"></a><span data-ttu-id="6ab85-108">Controladores de eventos de ambiente</span><span class="sxs-lookup"><span data-stu-id="6ab85-108">Ambient Event Handlers</span></span>

<span data-ttu-id="6ab85-109">Los controladores de eventos siguientes se pueden implementar para la mayoría de los elementos de máscara.</span><span class="sxs-lookup"><span data-stu-id="6ab85-109">The following event handlers can be implemented for most skin elements.</span></span> <span data-ttu-id="6ab85-110">Los atributos de evento de ambiente a los que se tiene acceso con la palabra clave **Event** se pueden usar dentro de un controlador de eventos para determinar el estado del teclado y del mouse en el momento del evento.</span><span class="sxs-lookup"><span data-stu-id="6ab85-110">The ambient event attributes accessed with the **event** keyword can be used within an event handler to determine the state of the keyboard and mouse at the time of the event.</span></span>



| <span data-ttu-id="6ab85-111">Controlador de eventos</span><span class="sxs-lookup"><span data-stu-id="6ab85-111">Event handler</span></span>                                   | <span data-ttu-id="6ab85-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ab85-112">Description</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ab85-113">*atributo* \_ de onchange</span><span class="sxs-lookup"><span data-stu-id="6ab85-113">*attribute*\_onchange</span></span>](attribute-onchange.md) | <span data-ttu-id="6ab85-114">Cuando un atributo de máscara cambia de valor, se produce un evento que se puede controlar mediante un controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="6ab85-114">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="6ab85-115">El nombre del controlador de eventos es el nombre del atributo seguido por un carácter de subrayado y "onchange", como "valor onchange \_ ".</span><span class="sxs-lookup"><span data-stu-id="6ab85-115">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span> |
| [<span data-ttu-id="6ab85-116">onblur</span><span class="sxs-lookup"><span data-stu-id="6ab85-116">onblur</span></span>](onblur.md)                            | <span data-ttu-id="6ab85-117">Controla un evento que se produce cuando el elemento pierde el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="6ab85-117">Handles an event that occurs when the element loses the keyboard focus.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="6ab85-118">AlHacerClic</span><span class="sxs-lookup"><span data-stu-id="6ab85-118">onclick</span></span>](onclick.md)                          | <span data-ttu-id="6ab85-119">Controla un evento que se produce cuando el usuario hace clic en el elemento.</span><span class="sxs-lookup"><span data-stu-id="6ab85-119">Handles an event that occurs when the user clicks the element.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="6ab85-120">ondblclick</span><span class="sxs-lookup"><span data-stu-id="6ab85-120">ondblclick</span></span>](ondblclick.md)                    | <span data-ttu-id="6ab85-121">Controla un evento que se produce cuando el usuario hace doble clic en el elemento.</span><span class="sxs-lookup"><span data-stu-id="6ab85-121">Handles an event that occurs when the user double-clicks the element.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="6ab85-122">onendalphablend</span><span class="sxs-lookup"><span data-stu-id="6ab85-122">onendalphablend</span></span>](onendalphablend.md)          | <span data-ttu-id="6ab85-123">Controla un evento que se produce cuando un elemento completa una operación **alphaBlendTo** .</span><span class="sxs-lookup"><span data-stu-id="6ab85-123">Handles an event that occurs when an element completes an **alphaBlendTo** operation.</span></span>                                                                                                                                         |
| [<span data-ttu-id="6ab85-124">onendmove</span><span class="sxs-lookup"><span data-stu-id="6ab85-124">onendmove</span></span>](onendmove.md)                      | <span data-ttu-id="6ab85-125">Controla un evento que se produce cuando un elemento completa una operación **moveTo** .</span><span class="sxs-lookup"><span data-stu-id="6ab85-125">Handles an event that occurs when an element completes a **moveTo** operation.</span></span>                                                                                                                                                |
| [<span data-ttu-id="6ab85-126">onfocus</span><span class="sxs-lookup"><span data-stu-id="6ab85-126">onfocus</span></span>](onfocus.md)                          | <span data-ttu-id="6ab85-127">Controla un evento que se produce cuando el elemento recibe el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="6ab85-127">Handles an event that occurs when the element receives the keyboard focus.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="6ab85-128">onkeydown</span><span class="sxs-lookup"><span data-stu-id="6ab85-128">onkeydown</span></span>](onkeydown.md)                      | <span data-ttu-id="6ab85-129">Controla un evento que se produce cuando se presiona una tecla.</span><span class="sxs-lookup"><span data-stu-id="6ab85-129">Handles an event that occurs when a key is pressed.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="6ab85-130">onkeypress</span><span class="sxs-lookup"><span data-stu-id="6ab85-130">onkeypress</span></span>](onkeypress.md)                    | <span data-ttu-id="6ab85-131">Controla un evento que se produce cuando el usuario presiona una clave alfanumérica.</span><span class="sxs-lookup"><span data-stu-id="6ab85-131">Handles an event that occurs when the user presses an alphanumeric key.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="6ab85-132">AlSubirTecla</span><span class="sxs-lookup"><span data-stu-id="6ab85-132">onkeyup</span></span>](onkeyup.md)                          | <span data-ttu-id="6ab85-133">Controla un evento que se produce cuando se suelta una tecla.</span><span class="sxs-lookup"><span data-stu-id="6ab85-133">Handles an event that occurs when a key is released.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="6ab85-134">alsubirmouse</span><span class="sxs-lookup"><span data-stu-id="6ab85-134">onmousedown</span></span>](onmousedown.md)                  | <span data-ttu-id="6ab85-135">Controla un evento que se produce cuando el usuario hace clic en un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="6ab85-135">Handles an event that occurs when the user clicks a mouse button.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="6ab85-136">almovermouse</span><span class="sxs-lookup"><span data-stu-id="6ab85-136">onmousemove</span></span>](onmousemove.md)                  | <span data-ttu-id="6ab85-137">Controla un evento que se produce cuando el usuario mueve el puntero del mouse mientras se encuentra sobre un elemento.</span><span class="sxs-lookup"><span data-stu-id="6ab85-137">Handles an event that occurs when the user moves the mouse pointer while it is over an element.</span></span>                                                                                                                               |
| [<span data-ttu-id="6ab85-138">onmouseout</span><span class="sxs-lookup"><span data-stu-id="6ab85-138">onmouseout</span></span>](onmouseout.md)                    | <span data-ttu-id="6ab85-139">Controla un evento que se produce cuando el usuario mueve el puntero fuera del elemento.</span><span class="sxs-lookup"><span data-stu-id="6ab85-139">Handles an event that occurs when the user moves the pointer off the element.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="6ab85-140">onmouseover</span><span class="sxs-lookup"><span data-stu-id="6ab85-140">onmouseover</span></span>](onmouseover.md)                  | <span data-ttu-id="6ab85-141">Controla un evento que se produce cuando el usuario coloca por primera vez el puntero sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="6ab85-141">Handles an event that occurs when the user first places the pointer over the element.</span></span>                                                                                                                                         |
| [<span data-ttu-id="6ab85-142">OnMouseUp</span><span class="sxs-lookup"><span data-stu-id="6ab85-142">onmouseup</span></span>](onmouseup.md)                      | <span data-ttu-id="6ab85-143">Controla un evento que se produce cuando el usuario suelta un botón del mouse mientras el puntero está sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="6ab85-143">Handles an event that occurs when the user releases a mouse button while the pointer is over the element.</span></span>                                                                                                                     |
| [<span data-ttu-id="6ab85-144">OnResize</span><span class="sxs-lookup"><span data-stu-id="6ab85-144">onresize</span></span>](onresize.md)                        | <span data-ttu-id="6ab85-145">Controla un evento que se produce cuando se cambia el tamaño de un control.</span><span class="sxs-lookup"><span data-stu-id="6ab85-145">Handles an event that occurs when a control resizes.</span></span>                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="6ab85-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ab85-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab85-147">**Atributos de evento de ambiente**</span><span class="sxs-lookup"><span data-stu-id="6ab85-147">**Ambient Event Attributes**</span></span>](ambient-event-attributes.md)
</dt> <dt>

[<span data-ttu-id="6ab85-148">**Referencia de programación de máscara**</span><span class="sxs-lookup"><span data-stu-id="6ab85-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




