---
title: Estilos de control de encabezado (CommCtrl. h)
description: Los controles de encabezado tienen varios estilos, que se describen en esta sección, que determinan la apariencia y el comportamiento del control. Los estilos iniciales se establecen al crear el control de encabezado.
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8450ad39cdb965e3e4be15f0093ec4737a87c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649717"
---
# <a name="header-control-styles"></a><span data-ttu-id="fa99f-104">Estilos de control de encabezado</span><span class="sxs-lookup"><span data-stu-id="fa99f-104">Header Control Styles</span></span>

<span data-ttu-id="fa99f-105">Los controles de encabezado tienen varios estilos, que se describen en esta sección, que determinan la apariencia y el comportamiento del control.</span><span class="sxs-lookup"><span data-stu-id="fa99f-105">Header controls have a number of styles, described in this section, that determine the control's appearance and behavior.</span></span> <span data-ttu-id="fa99f-106">Los estilos iniciales se establecen al crear el control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="fa99f-106">You set the initial styles when you create the header control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="fa99f-107">Constante</span><span class="sxs-lookup"><span data-stu-id="fa99f-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="fa99f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa99f-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <span data-ttu-id="fa99f-109"><dt><strong>HDS_BUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa99f-109"><dt><strong>HDS_BUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa99f-110">Cada elemento del control tiene el aspecto y se comporta como un botón de opción.</span><span class="sxs-lookup"><span data-stu-id="fa99f-110">Each item in the control looks and behaves like a push button.</span></span> <span data-ttu-id="fa99f-111">Este estilo es útil si una aplicación realiza una tarea cuando el usuario hace clic en un elemento del control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="fa99f-111">This style is useful if an application carries out a task when the user clicks an item in the header control.</span></span> <span data-ttu-id="fa99f-112">Por ejemplo, una aplicación podría ordenar la información de las columnas de manera diferente en función del elemento en el que el usuario haga clic.</span><span class="sxs-lookup"><span data-stu-id="fa99f-112">For example, an application could sort information in the columns differently depending on which item the user clicks.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <span data-ttu-id="fa99f-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa99f-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa99f-114">Permite la reordenación de elementos de encabezado de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="fa99f-114">Allows drag-and-drop reordering of header items.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <span data-ttu-id="fa99f-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa99f-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa99f-116">Incluye una barra de filtros como parte del control de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="fa99f-116">Include a filter bar as part of the standard header control.</span></span> <span data-ttu-id="fa99f-117">Esta barra permite a los usuarios aplicar de forma cómoda un filtro a la pantalla.</span><span class="sxs-lookup"><span data-stu-id="fa99f-117">This bar allows users to conveniently apply a filter to the display.</span></span> <span data-ttu-id="fa99f-118">Las llamadas a <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> producirán un nuevo tamaño para el control y harán que la vista de lista se actualice.</span><span class="sxs-lookup"><span data-stu-id="fa99f-118">Calls to <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> will yield a new size for the control and cause the list view to update.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <span data-ttu-id="fa99f-119"><dt><strong>HDS_FLAT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa99f-119"><dt><strong>HDS_FLAT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa99f-120"><a href="common-control-versions.md">Versión 6,0 y versiones posteriores</a>.</span><span class="sxs-lookup"><span data-stu-id="fa99f-120"><a href="common-control-versions.md">Version 6.0 and later</a>.</span></span> <span data-ttu-id="fa99f-121">Hace que el control de encabezado se dibuje plano cuando el sistema operativo se ejecuta en modo clásico.</span><span class="sxs-lookup"><span data-stu-id="fa99f-121">Causes the header control to be drawn flat when the operating system is running in classic mode.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fa99f-122">Comctl32.dll versión 6 no es redistribuible, pero se incluye en Windows.</span><span class="sxs-lookup"><span data-stu-id="fa99f-122">Comctl32.dll version 6 is not redistributable but it is included in Windows.</span></span> <span data-ttu-id="fa99f-123">Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="fa99f-123">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="fa99f-124">Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.</span><span class="sxs-lookup"><span data-stu-id="fa99f-124">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <span data-ttu-id="fa99f-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa99f-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa99f-126">Hace que el control de encabezado muestre el contenido de la columna incluso mientras el usuario cambia el tamaño de una columna.</span><span class="sxs-lookup"><span data-stu-id="fa99f-126">Causes the header control to display column contents even while the user resizes a column.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <span data-ttu-id="fa99f-127"><dt><strong>HDS_HIDDEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa99f-127"><dt><strong>HDS_HIDDEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa99f-128">Indica un control de encabezado que se va a ocultar.</span><span class="sxs-lookup"><span data-stu-id="fa99f-128">Indicates a header control that is intended to be hidden.</span></span> <span data-ttu-id="fa99f-129">Este estilo no oculta el control.</span><span class="sxs-lookup"><span data-stu-id="fa99f-129">This style does not hide the control.</span></span> <span data-ttu-id="fa99f-130">En su lugar, cuando se envía el mensaje de <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> a un control de encabezado con el estilo de HDS_HIDDEN, el control devuelve cero en el miembro <strong>CY</strong> de la estructura <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>windowpos (</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fa99f-130">Instead, when you send the <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> message to a header control with the HDS_HIDDEN style, the control returns zero in the <strong>cy</strong> member of the <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> structure.</span></span> <span data-ttu-id="fa99f-131">A continuación, ocultaría el control estableciendo su alto en cero.</span><span class="sxs-lookup"><span data-stu-id="fa99f-131">You would then hide the control by setting its height to zero.</span></span> <span data-ttu-id="fa99f-132">Esto puede ser útil si desea usar el control como contenedor de información en lugar de como un control visual.</span><span class="sxs-lookup"><span data-stu-id="fa99f-132">This can be useful when you want to use the control as an information container instead of a visual control.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <span data-ttu-id="fa99f-133"><dt><strong>HDS_HORZ</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa99f-133"><dt><strong>HDS_HORZ</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa99f-134">Crea un control de encabezado con una orientación horizontal.</span><span class="sxs-lookup"><span data-stu-id="fa99f-134">Creates a header control with a horizontal orientation.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <span data-ttu-id="fa99f-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa99f-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa99f-136">Habilita el seguimiento activo.</span><span class="sxs-lookup"><span data-stu-id="fa99f-136">Enables hot tracking.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <span data-ttu-id="fa99f-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa99f-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa99f-138"><a href="common-control-versions.md">Versión 6,00 y versiones posteriores</a>.</span><span class="sxs-lookup"><span data-stu-id="fa99f-138"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="fa99f-139">Permite colocar casillas en los elementos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="fa99f-139">Allows the placing of checkboxes on header items.</span></span> <span data-ttu-id="fa99f-140">Para obtener más información, vea el miembro <strong>FMT</strong> de <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="fa99f-140">For more information, see the <strong>fmt</strong> member of <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <span data-ttu-id="fa99f-141"><dt><strong>HDS_NOSIZING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa99f-141"><dt><strong>HDS_NOSIZING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa99f-142"><a href="common-control-versions.md">Versión 6,00 y versiones posteriores</a>.</span><span class="sxs-lookup"><span data-stu-id="fa99f-142"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="fa99f-143">El usuario no puede arrastrar el divisor en el control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="fa99f-143">The user cannot drag the divider on the header control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <span data-ttu-id="fa99f-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa99f-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa99f-145"><a href="common-control-versions.md">Versión 6,00 y versiones posteriores</a>.</span><span class="sxs-lookup"><span data-stu-id="fa99f-145"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="fa99f-146">Se muestra un botón cuando no se pueden mostrar todos los elementos dentro del rectángulo del control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="fa99f-146">A button is displayed when not all items can be displayed within the header control's rectangle.</span></span> <span data-ttu-id="fa99f-147">Al hacer clic en este botón, se envía una notificación <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> .</span><span class="sxs-lookup"><span data-stu-id="fa99f-147">When clicked, this button sends an <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> notification.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="fa99f-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa99f-148">Remarks</span></span>

<span data-ttu-id="fa99f-149">Para recuperar y cambiar los estilos después de crear el control, use las funciones [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) y [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="fa99f-149">To retrieve and change the styles after creating the control, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa99f-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa99f-150">Requirements</span></span>



| <span data-ttu-id="fa99f-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa99f-151">Requirement</span></span> | <span data-ttu-id="fa99f-152">Value</span><span class="sxs-lookup"><span data-stu-id="fa99f-152">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa99f-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa99f-153">Header</span></span><br/> | <dl> <span data-ttu-id="fa99f-154"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa99f-154"><dt>CommCtrl.h</dt></span></span> </dl> |



