---
description: Descripción de las técnicas de subestándar para exponer controles personalizados.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Técnicas subestándars para exponer controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678189"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a><span data-ttu-id="155a8-103">Técnicas subestándars para exponer controles personalizados</span><span class="sxs-lookup"><span data-stu-id="155a8-103">Substandard Techniques for Exposing Custom Controls</span></span>

<span data-ttu-id="155a8-104">Si una aplicación no admite Microsoft Active Accessibility, puede que no sea totalmente accesible.</span><span class="sxs-lookup"><span data-stu-id="155a8-104">If an application does not support Microsoft Active Accessibility, it may not be fully accessible.</span></span> <span data-ttu-id="155a8-105">Las técnicas siguientes presentan controles parcialmente compatibles:</span><span class="sxs-lookup"><span data-stu-id="155a8-105">The following techniques render controls partially compatible:</span></span>

-   <span data-ttu-id="155a8-106">Devuelve una cadena descriptiva cuando el control se consulta mediante el mensaje de \_ GETTEXT de WM.</span><span class="sxs-lookup"><span data-stu-id="155a8-106">Return a descriptive string when the control is queried by using the WM\_GETTEXT message.</span></span> <span data-ttu-id="155a8-107">Por ejemplo, permitir un equivalente personalizado de un control de botón con la etiqueta "Imprimir" para que se devuelva la cadena "botón Imprimir".</span><span class="sxs-lookup"><span data-stu-id="155a8-107">For example, allow a custom equivalent of a button control labeled "Print" to return the string "Print button."</span></span> <span data-ttu-id="155a8-108">Esto identifica el tipo de control y la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="155a8-108">This identifies both control type and label.</span></span> <span data-ttu-id="155a8-109">La misma cadena es adecuada para un botón con una etiqueta que no sea texto, como un gráfico de una impresora.</span><span class="sxs-lookup"><span data-stu-id="155a8-109">The same string is appropriate for a button with a label that is something other than text, such as a graphic of a printer.</span></span> <span data-ttu-id="155a8-110">Del mismo modo, permitir un control personalizado que se comporta como una casilla para devolver la cadena de título "marca de impresión habilitada".</span><span class="sxs-lookup"><span data-stu-id="155a8-110">Similarly, allow a custom control that behaves like a check box to return the caption string "Printing Enabled check box, checked."</span></span>
-   <span data-ttu-id="155a8-111">Admitir el mensaje de GETDLGCODE de WM \_ , que identifica la entrada del teclado que se admite.</span><span class="sxs-lookup"><span data-stu-id="155a8-111">Support the WM\_GETDLGCODE message, identifying the keyboard input that is supported.</span></span> <span data-ttu-id="155a8-112">Por ejemplo, permitir un equivalente personalizado de un control de edición para administrar WM \_ GETDLGCODE devolviendo DLGC \_ HASSETSEL si controla los mensajes para establecer la selección, DLGC \_ WANTARROWS si usa las teclas de dirección y DLGC \_ WANTCHARS para indicar que utiliza la entrada de caracteres.</span><span class="sxs-lookup"><span data-stu-id="155a8-112">For example, allow a custom equivalent of an edit control to handle WM\_GETDLGCODE by returning DLGC\_HASSETSEL if it handles messages to set the selection, DLGC\_WANTARROWS if it uses arrow keys, and DLGC\_WANTCHARS to indicate that it uses character input.</span></span>
    > [!Note]  
    > <span data-ttu-id="155a8-113">Solo los controles que tienen sus propios identificadores de ventana pueden responder a los \_ mensajes de GETDLGCODE GETTEXT y WM \_ .</span><span class="sxs-lookup"><span data-stu-id="155a8-113">Only controls that have their own window handles can respond to the WM\_GETTEXT and WM\_GETDLGCODE messages.</span></span>

     

<span data-ttu-id="155a8-114">Para evitar problemas de compatibilidad con las ayudas de accesibilidad, debe seguir Active Accessibility instrucciones detalladas al diseñar controles personalizados.</span><span class="sxs-lookup"><span data-stu-id="155a8-114">To avoid compatibility problems with accessibility aids, you should follow Active Accessibility guidelines closely when designing custom controls.</span></span> <span data-ttu-id="155a8-115">Para obtener más información sobre cómo evitar problemas de compatibilidad con las ayudas de accesibilidad, consulte la sección [accesibilidad](../accessibility/accessibility.md) .</span><span class="sxs-lookup"><span data-stu-id="155a8-115">For more information about how to avoid compatibility problems with accessibility aids, see the [Accessibility](../accessibility/accessibility.md) section.</span></span>

 

 
