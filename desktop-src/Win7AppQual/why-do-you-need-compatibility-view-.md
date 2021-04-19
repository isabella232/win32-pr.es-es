---
description: .
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: ¿Por qué necesita la vista de compatibilidad?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fd1902ad77af863e61be36800a8c4f9eabf227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688584"
---
# <a name="why-do-you-need-compatibility-view"></a><span data-ttu-id="c68f2-103">¿Por qué necesita la vista de compatibilidad?</span><span class="sxs-lookup"><span data-stu-id="c68f2-103">Why Do You Need Compatibility View?</span></span>

<span data-ttu-id="c68f2-104">La característica vista de compatibilidad sigue un conjunto de reglas para mostrar el contenido correctamente, sin que se necesiten acciones de usuario (o administrador de TI) siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="c68f2-104">The Compatibility View feature follows a set of rules to display content correctly, without any user (or IT administrator) action needed whenever possible.</span></span> <span data-ttu-id="c68f2-105">La vista de compatibilidad permite a los desarrolladores indicar al explorador qué motor de representación usar y permite a los usuarios invalidar los modos de elección y cambio del explorador.</span><span class="sxs-lookup"><span data-stu-id="c68f2-105">Compatibility View enables developers to instruct the browser which rendering engine to use and enables users to override the browser’s choice and switch modes.</span></span> <span data-ttu-id="c68f2-106">Si el desarrollador y el profesional de ti no especifican el modo de representación que se va a usar, el usuario verá el icono de "página rota" en el extremo derecho de la barra de direcciones, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="c68f2-106">If the developer and IT professional do not specify which rendering mode to use, user sees the "broken page" icon at the right end of the address bar, as the following illustration shows.</span></span>

![Ilustración del icono de página rota junto a la barra de direcciones](images/iecompatview.png)

<span data-ttu-id="c68f2-108">Si un usuario hace clic en el icono, Windows Internet Explorer 8 cambia los modos de representación y la página se recarga al instante.</span><span class="sxs-lookup"><span data-stu-id="c68f2-108">If a user clicks the icon, Windows Internet Explorer 8 switches rendering modes, and the page reloads instantly.</span></span>

<span data-ttu-id="c68f2-109">Los usuarios no siempre ven este icono.</span><span class="sxs-lookup"><span data-stu-id="c68f2-109">Users do not always see this icon.</span></span> <span data-ttu-id="c68f2-110">Es una solución secundaria en lugar del mecanismo de compatibilidad de aplicaciones principal.</span><span class="sxs-lookup"><span data-stu-id="c68f2-110">It is a secondary solution instead of the primary application compatibility mechanism.</span></span> <span data-ttu-id="c68f2-111">Windows Internet Explorer muestra este icono solo cuando tiene sentido un cambio en la vista de compatibilidad, como cuando un usuario ve las páginas del modo estándar.</span><span class="sxs-lookup"><span data-stu-id="c68f2-111">Windows Internet Explorer displays this icon only when a change into Compatibility View makes sense, such as when a user views standards mode pages.</span></span> <span data-ttu-id="c68f2-112">En todos los demás casos, como cuando un usuario ve las páginas del modo no estándar o las vistas sitios de la zona de intranet, el icono no aparece.</span><span class="sxs-lookup"><span data-stu-id="c68f2-112">In all other cases, such as when a user views quirks mode pages or views Intranet Zone sites, the icon does not appear.</span></span> <span data-ttu-id="c68f2-113">Para obtener más información acerca de la vista de compatibilidad y el momento en el que aparece el icono, vea Introducción a la [vista de compatibilidad](/archive/blogs/ie/).</span><span class="sxs-lookup"><span data-stu-id="c68f2-113">For more information about Compatibility View and when the icon appears, see [Introducing Compatibility View](/archive/blogs/ie/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c68f2-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c68f2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c68f2-115">Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="c68f2-115">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
