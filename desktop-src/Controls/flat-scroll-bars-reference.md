---
title: Barra de desplazamiento plana
description: Esta sección contiene información sobre los elementos de programación usados para controlar las barras de desplazamiento sin formato.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e611e8d5755d119a8c24bdbccb9f10408d3d7d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903259"
---
# <a name="flat-scroll-bar"></a><span data-ttu-id="df2f8-103">Barra de desplazamiento plana</span><span class="sxs-lookup"><span data-stu-id="df2f8-103">Flat Scroll Bar</span></span>

<span data-ttu-id="df2f8-104">Esta sección contiene información sobre los elementos de programación usados para controlar las barras de desplazamiento sin formato.</span><span class="sxs-lookup"><span data-stu-id="df2f8-104">This section contains information about the programming elements used to control flat scroll bars.</span></span>

### <a name="overviews"></a><span data-ttu-id="df2f8-105">Temas de introducción</span><span class="sxs-lookup"><span data-stu-id="df2f8-105">Overviews</span></span>



| <span data-ttu-id="df2f8-106">Tema</span><span class="sxs-lookup"><span data-stu-id="df2f8-106">Topic</span></span>                                    | <span data-ttu-id="df2f8-107">Contenido</span><span class="sxs-lookup"><span data-stu-id="df2f8-107">Contents</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df2f8-108">Barras de desplazamiento plana</span><span class="sxs-lookup"><span data-stu-id="df2f8-108">Flat Scroll Bars</span></span>](flat-scroll-bars.md) | <span data-ttu-id="df2f8-109">Microsoft Internet Explorer 4,0 presentó una nueva tecnología visual denominada barras de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-109">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="df2f8-110">Funcionalmente, las barras de desplazamiento sin formato se comportan igual que las barras de desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="df2f8-110">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="df2f8-111">La diferencia es que puede personalizar su apariencia en una extensión mayor que las barras de desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="df2f8-111">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="df2f8-112">Functions</span><span class="sxs-lookup"><span data-stu-id="df2f8-112">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df2f8-113">Tema</span><span class="sxs-lookup"><span data-stu-id="df2f8-113">Topic</span></span></th>
<th><span data-ttu-id="df2f8-114">Contenido</span><span class="sxs-lookup"><span data-stu-id="df2f8-114">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df2f8-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-116">Habilita o deshabilita uno o ambos botones de dirección de la barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-116">Enables or disables one or both flat scroll bar direction buttons.</span></span> <span data-ttu-id="df2f8-117">Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> estándar.</span><span class="sxs-lookup"><span data-stu-id="df2f8-117">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df2f8-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-119">Obtiene la información de una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-119">Gets the information for a flat scroll bar.</span></span> <span data-ttu-id="df2f8-120">Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> estándar.</span><span class="sxs-lookup"><span data-stu-id="df2f8-120">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df2f8-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-122">Obtiene la posición del control en una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-122">Gets the thumb position in a flat scroll bar.</span></span> <span data-ttu-id="df2f8-123">Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> estándar.</span><span class="sxs-lookup"><span data-stu-id="df2f8-123">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df2f8-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-125">Obtiene las propiedades de una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-125">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="df2f8-126">Esta función también se puede usar para determinar si se ha llamado a <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> para esta ventana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-126">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df2f8-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-128">Obtiene las propiedades de una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-128">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="df2f8-129">Esta función también se puede usar para determinar si se ha llamado a <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> para esta ventana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-129">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="df2f8-130">Es idéntico a <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="df2f8-130">This is identical to <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df2f8-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-132">Obtiene el intervalo de desplazamiento de una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-132">Gets the scroll range for a flat scroll bar.</span></span> <span data-ttu-id="df2f8-133">Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> estándar.</span><span class="sxs-lookup"><span data-stu-id="df2f8-133">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df2f8-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-135">Establece la información de una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-135">Sets the information for a flat scroll bar.</span></span> <span data-ttu-id="df2f8-136">Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> estándar.</span><span class="sxs-lookup"><span data-stu-id="df2f8-136">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df2f8-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-138">Establece la posición actual del control Thumb en una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-138">Sets the current position of the thumb in a flat scroll bar.</span></span> <span data-ttu-id="df2f8-139">Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> estándar.</span><span class="sxs-lookup"><span data-stu-id="df2f8-139">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df2f8-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-141">Establece las propiedades de una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-141">Sets the properties for a flat scroll bar.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df2f8-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-143">Establece el intervalo de desplazamiento de una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-143">Sets the scroll range of a flat scroll bar.</span></span> <span data-ttu-id="df2f8-144">Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> estándar.</span><span class="sxs-lookup"><span data-stu-id="df2f8-144">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df2f8-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-146">Muestra u oculta una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="df2f8-146">Shows or hides a flat scroll bar.</span></span> <span data-ttu-id="df2f8-147">Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> estándar.</span><span class="sxs-lookup"><span data-stu-id="df2f8-147">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df2f8-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-149">Inicializa barras de desplazamiento plana para una ventana determinada.</span><span class="sxs-lookup"><span data-stu-id="df2f8-149">Initializes flat scroll bars for a particular window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df2f8-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span><span class="sxs-lookup"><span data-stu-id="df2f8-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="df2f8-151">Desinicializa las barras de desplazamiento plana para una ventana determinada.</span><span class="sxs-lookup"><span data-stu-id="df2f8-151">Uninitializes flat scroll bars for a particular window.</span></span> <span data-ttu-id="df2f8-152">La ventana especificada se revertirá a las barras de desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="df2f8-152">The specified window will revert to standard scroll bars.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

 





