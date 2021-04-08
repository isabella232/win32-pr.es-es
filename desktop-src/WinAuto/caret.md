---
title: Símbolo de intercalación (referencia de elementos de interfaz de usuario de MSAA)
description: El símbolo de intercalación es una línea, un bloque o un mapa de bits intermitentes en el área cliente de una ventana o en un control que acepta la entrada del teclado.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "103904373"
---
# <a name="caret-msaa-ui-element-reference"></a><span data-ttu-id="04413-103">Símbolo de intercalación (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="04413-103">Caret (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="04413-104">En este tema se describen los acentos para la referencia de elementos de la interfaz de usuario de MSAA.</span><span class="sxs-lookup"><span data-stu-id="04413-104">This topic describes carets for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="04413-105">El uso de las intercalaciones en varios marcos de interfaz de usuario no se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="04413-105">How to use carets in various UI frameworks is not described here.</span></span> <span data-ttu-id="04413-106">Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.</span><span class="sxs-lookup"><span data-stu-id="04413-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="04413-107">El símbolo de intercalación es una línea, un bloque o un mapa de bits intermitentes en el área cliente de una ventana o en un control que acepta la entrada del teclado.</span><span class="sxs-lookup"><span data-stu-id="04413-107">The caret is a flashing line, block, or bitmap in the client area of a window or in a control that accepts keyboard input.</span></span> <span data-ttu-id="04413-108">Indica el lugar en el que se insertan texto o gráficos.</span><span class="sxs-lookup"><span data-stu-id="04413-108">It indicates the place at which text or graphics are inserted.</span></span> <span data-ttu-id="04413-109">Dado que solo una ventana a la vez tiene el foco de teclado, solo hay un símbolo de intercalación en el sistema.</span><span class="sxs-lookup"><span data-stu-id="04413-109">Because only one window at a time has the keyboard focus, there is only one caret in the system.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="04413-110">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="04413-110">IAccessible Methods</span></span>

<span data-ttu-id="04413-111">El símbolo de intercalación admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="04413-111">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="04413-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="04413-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="04413-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="04413-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="04413-114">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="04413-114">IAccessible Properties</span></span>

<span data-ttu-id="04413-115">El símbolo de intercalación admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="04413-115">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04413-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04413-116">Property</span></span></th>
<th><span data-ttu-id="04413-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04413-117">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04413-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="04413-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="04413-119">La propiedad <strong>ChildCount</strong> es cero.</span><span class="sxs-lookup"><span data-stu-id="04413-119">The <strong>ChildCount</strong> property is zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04413-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span><span class="sxs-lookup"><span data-stu-id="04413-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span></span></td>
<td><span data-ttu-id="04413-121">La propiedad <strong>Name</strong> es &quot; Edit &quot; .</span><span class="sxs-lookup"><span data-stu-id="04413-121">The <strong>Name</strong> property is &quot;Edit&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04413-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span><span class="sxs-lookup"><span data-stu-id="04413-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span></span></td>
<td><span data-ttu-id="04413-123">La propiedad de <strong>rol</strong> es <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span><span class="sxs-lookup"><span data-stu-id="04413-123">The <strong>Role</strong> property is <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04413-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span><span class="sxs-lookup"><span data-stu-id="04413-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span></span></td>
<td><span data-ttu-id="04413-125">Los valores posibles para la propiedad <strong>State</strong> incluyen:</span><span class="sxs-lookup"><span data-stu-id="04413-125">Possible values for the <strong>State</strong> property include:</span></span>
<ul>
<li><span data-ttu-id="04413-126">Cero, lo que significa que el símbolo de intercalación es visible</span><span class="sxs-lookup"><span data-stu-id="04413-126">Zero, which means the caret is visible</span></span></li>
<li><span data-ttu-id="04413-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span><span class="sxs-lookup"><span data-stu-id="04413-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="04413-128">Notas</span><span class="sxs-lookup"><span data-stu-id="04413-128">Notes</span></span>

-   <span data-ttu-id="04413-129">A diferencia de otros elementos de la interfaz de usuario, el objeto de símbolo de intercalación no tiene un identificador de ventana asociado.</span><span class="sxs-lookup"><span data-stu-id="04413-129">Unlike other UI elements, the caret object does not have an associated window handle.</span></span> <span data-ttu-id="04413-130">Para obtener acceso al objeto de símbolo de intercalación, los clientes deben establecer [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y esperar a que el objeto de símbolo de intercalación genere eventos.</span><span class="sxs-lookup"><span data-stu-id="04413-130">To obtain access to the caret object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the caret object to generate events.</span></span>
-   <span data-ttu-id="04413-131">El objeto de símbolo de intercalación en el control Rich Edit proporcionado por Riched20.dll (que se usa en los editores de texto como Microsoft WordPad en Windows 98) no envía ningún [WinEvents](winevents-infrastructure.md) cuando se cambia su posición durante la selección de texto.</span><span class="sxs-lookup"><span data-stu-id="04413-131">The caret object in the rich edit control provided by Riched20.dll (which is used in text editors such as Microsoft WordPad in Windows 98) does not send any [WinEvents](winevents-infrastructure.md) when its position is changed during text selection.</span></span> <span data-ttu-id="04413-132">Cuando los usuarios presionan Mayús y las teclas de dirección para seleccionar texto, el objeto de símbolo de intercalación no desencadena el [**objeto de evento \_ \_ LOCATIONCHANGE**](event-constants.md) WinEvent.</span><span class="sxs-lookup"><span data-stu-id="04413-132">When users press SHIFT and arrow keys to select text, the caret object does not trigger the [**EVENT\_OBJECT\_LOCATIONCHANGE**](event-constants.md) WinEvent.</span></span> <span data-ttu-id="04413-133">Del mismo modo, cuando la selección se establece mediante programación a través de mensajes Rich Edit, el objeto de símbolo de intercalación no envía ningún evento para indicar su nueva posición.</span><span class="sxs-lookup"><span data-stu-id="04413-133">Similarly, when the selection is set programmatically through rich edit messages, the caret object does not send any events to indicate its new position.</span></span>

    <span data-ttu-id="04413-134">Todas las aplicaciones que usan Riched20.dll muestran este problema.</span><span class="sxs-lookup"><span data-stu-id="04413-134">All applications that use Riched20.dll exhibit this problem.</span></span> <span data-ttu-id="04413-135">Las aplicaciones que usan versiones anteriores del control Rich Edit envían correctamente los eventos en función de la selección.</span><span class="sxs-lookup"><span data-stu-id="04413-135">Applications using earlier versions of the rich edit control correctly send events based on the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04413-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04413-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04413-137">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="04413-137">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




