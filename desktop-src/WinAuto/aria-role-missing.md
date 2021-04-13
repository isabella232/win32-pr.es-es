---
title: Error de rol de ARIA para elementos con controladores de eventos
description: Error de rol de ARIA para elementos con controladores de eventos
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- AriaContainerRoleErrorMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eede416392e8b4cb644938242a9975238118ff07
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421553"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a><span data-ttu-id="86e33-104">Error de rol de ARIA para elementos con controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="86e33-104">ARIA Role Error for elements with event handlers</span></span>

## <a name="text"></a><span data-ttu-id="86e33-105">Texto</span><span class="sxs-lookup"><span data-stu-id="86e33-105">Text</span></span>

<span data-ttu-id="86e33-106">El elemento tiene un controlador de eventos pero no se ha definido un rol WAI-ARIA válido.</span><span class="sxs-lookup"><span data-stu-id="86e33-106">Element has an event handler but valid WAI-ARIA role is not defined.</span></span>

## <a name="type"></a><span data-ttu-id="86e33-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="86e33-107">Type</span></span>

<span data-ttu-id="86e33-108">Error</span><span class="sxs-lookup"><span data-stu-id="86e33-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="86e33-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="86e33-109">Description</span></span>

<span data-ttu-id="86e33-110">Este error se aplica a los elementos que no tienen un rol de aplicaciones de Internet enriquecidas con acceso a la iniciativa de accesibilidad web (WAI-ARIA).</span><span class="sxs-lookup"><span data-stu-id="86e33-110">This error applies to elements that do not have an implicit Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role.</span></span>

<span data-ttu-id="86e33-111">Este error indica que un elemento tiene un mouse o un controlador de eventos de teclado (**click**, **MouseDown**, **MouseUp**, **MouseMove**, **mouseout**, **mouseover**, **KeyUp**, **KeyDown** o **KEYPRESS**), pero no tiene establecido el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) y no es una de las etiquetas HTML que tiene un rol WAI-ARIA implícito (por ejemplo, **a**, **Button**, **IMG**, **Input**, **Select** , etc.).</span><span class="sxs-lookup"><span data-stu-id="86e33-111">This error indicates that an element has a mouse or keyboard event handler (**click**, **mousedown**, **mouseup**, **mousemove**, **mouseout**, **mouseover**, **keyup**, **keydown**, or **keypress**), but doesn’t have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set, and is not one of the HTML tags that has an implicit WAI-ARIA role (for example, **a**, **button**, **img**, **input**, **select** and so on).</span></span>

<span data-ttu-id="86e33-112">Es necesario establecer el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) para los elementos interactivos que no tienen ningún rol implícito (como una etiqueta **div** ) para exponer los patrones de comportamiento del elemento a los lectores de pantalla y otras tecnologías de asistencia.</span><span class="sxs-lookup"><span data-stu-id="86e33-112">Setting the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute for interactive elements that have no implicit role (such as a **div** tag) is necessary to expose the element's behavior patterns to screen readers and other assistive technologies.</span></span>

<span data-ttu-id="86e33-113">Para corregir este error, establezca el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) en un rol WAI-ARIA válido que se ajuste mejor a los patrones de comportamiento de este elemento y los atributos requeridos.</span><span class="sxs-lookup"><span data-stu-id="86e33-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role that best fits this element's behavior patterns and required attributes.</span></span> <span data-ttu-id="86e33-114">Por ejemplo, si una etiqueta **div** funciona como un botón, establezca el atributo role en "Button".</span><span class="sxs-lookup"><span data-stu-id="86e33-114">For example, if a **div** tag functions as a button, set the role attribute to "button".</span></span>

## <a name="example"></a><span data-ttu-id="86e33-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86e33-115">Example</span></span>


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




