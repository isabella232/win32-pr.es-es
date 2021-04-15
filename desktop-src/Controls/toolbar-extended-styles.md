---
title: Estilos extendidos de barra de herramientas (CommCtrl. h)
description: En esta sección se enumeran los estilos extendidos admitidos por los controles de barra de herramientas.
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056e48753485364017f04f7b84e609b19473bf5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649686"
---
# <a name="toolbar-extended-styles"></a><span data-ttu-id="f7064-103">Estilos extendidos de barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="f7064-103">Toolbar Extended Styles</span></span>

<span data-ttu-id="f7064-104">En esta sección se enumeran los estilos extendidos admitidos por los controles de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f7064-104">This section lists the extended styles supported by toolbar controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f7064-105">Constante</span><span class="sxs-lookup"><span data-stu-id="f7064-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f7064-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7064-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <span data-ttu-id="f7064-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f7064-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f7064-108"><a href="common-control-versions.md">Versión 4,71</a>.</span><span class="sxs-lookup"><span data-stu-id="f7064-108"><a href="common-control-versions.md">Version 4.71</a>.</span></span> <span data-ttu-id="f7064-109">Este estilo permite que los botones tengan una flecha de lista desplegable independiente.</span><span class="sxs-lookup"><span data-stu-id="f7064-109">This style allows buttons to have a separate dropdown arrow.</span></span> <span data-ttu-id="f7064-110">Los botones que tienen el estilo de <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> se dibujarán con una flecha de lista desplegable en una sección independiente, a la derecha del botón.</span><span class="sxs-lookup"><span data-stu-id="f7064-110">Buttons that have the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> style will be drawn with a dropdown arrow in a separate section, to the right of the button.</span></span> <span data-ttu-id="f7064-111">Si se hace clic en la flecha, solo se detendrá la parte de la flecha del botón y el control de barra de herramientas enviará un <a href="tbn-dropdown.md">TBN_DROPDOWN</a> código de notificación para solicitar a la aplicación que muestre el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="f7064-111">If the arrow is clicked, only the arrow portion of the button will depress, and the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code to prompt the application to display the dropdown menu.</span></span> <span data-ttu-id="f7064-112">Si se hace clic en la parte principal del botón, el control de barra de herramientas envía un mensaje de WM_COMMAND con el identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="f7064-112">If the main part of the button is clicked, the toolbar control sends a WM_COMMAND message with the button's ID.</span></span> <span data-ttu-id="f7064-113">Normalmente, la aplicación responde iniciando el primer comando en el menú.</span><span class="sxs-lookup"><span data-stu-id="f7064-113">The application normally responds by launching the first command on the menu.</span></span><br/> <span data-ttu-id="f7064-114">Hay muchas situaciones en las que quizás desee tener solo algunos de los botones de lista desplegable en una barra de herramientas con flechas separadas.</span><span class="sxs-lookup"><span data-stu-id="f7064-114">There are many situations where you may want to have only some of the dropdown buttons on a toolbar with separated arrows.</span></span> <span data-ttu-id="f7064-115">Para ello, establezca el estilo extendido TBSTYLE_EX_DRAWDDARROWS.</span><span class="sxs-lookup"><span data-stu-id="f7064-115">To do so, set the TBSTYLE_EX_DRAWDDARROWS extended style.</span></span> <span data-ttu-id="f7064-116">Asigne a los botones que no tendrán flechas separadas el estilo de <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f7064-116">Give those buttons that will not have separated arrows the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> style.</span></span> <span data-ttu-id="f7064-117">Los botones con este estilo tendrán una flecha junto a la imagen.</span><span class="sxs-lookup"><span data-stu-id="f7064-117">Buttons with this style will have an arrow displayed next to the image.</span></span> <span data-ttu-id="f7064-118">Sin embargo, la flecha no será independiente y cuando se haga clic en cualquier parte del botón, el control de barra de herramientas enviará un código de notificación <a href="tbn-dropdown.md">TBN_DROPDOWN</a> .</span><span class="sxs-lookup"><span data-stu-id="f7064-118">However, the arrow will not be separate and when any part of the button is clicked, the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code.</span></span> <span data-ttu-id="f7064-119">Para evitar problemas de repintado, este estilo debe establecerse antes de que el control de barra de herramientas se vuelva visible.</span><span class="sxs-lookup"><span data-stu-id="f7064-119">To prevent repainting problems, this style should be set before the toolbar control becomes visible.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <span data-ttu-id="f7064-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f7064-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f7064-121"><a href="common-control-versions.md">Versión 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="f7064-121"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="f7064-122">Este estilo oculta los botones recortados parcialmente.</span><span class="sxs-lookup"><span data-stu-id="f7064-122">This style hides partially clipped buttons.</span></span> <span data-ttu-id="f7064-123">El uso más común de este estilo es para las barras de herramientas que forman parte de un control rebar.</span><span class="sxs-lookup"><span data-stu-id="f7064-123">The most common use of this style is for toolbars that are part of a rebar control.</span></span> <span data-ttu-id="f7064-124">Si una banda adyacente cubre parte de un botón, el botón no se mostrará.</span><span class="sxs-lookup"><span data-stu-id="f7064-124">If an adjacent band covers part of a button, the button will not be displayed.</span></span> <span data-ttu-id="f7064-125">Sin embargo, si la banda rebar tiene el estilo de <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> , el botón se mostrará en el menú desplegable del botón de contenido adicional.</span><span class="sxs-lookup"><span data-stu-id="f7064-125">However, if the rebar band has the <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> style, the button will be displayed on the chevron's dropdown menu.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <span data-ttu-id="f7064-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f7064-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f7064-127"><a href="common-control-versions.md">Versión 6</a>.</span><span class="sxs-lookup"><span data-stu-id="f7064-127"><a href="common-control-versions.md">Version 6</a>.</span></span> <span data-ttu-id="f7064-128">Este estilo requiere que la barra de herramientas tenga doble búfer.</span><span class="sxs-lookup"><span data-stu-id="f7064-128">This style requires the toolbar to be double buffered.</span></span> <span data-ttu-id="f7064-129">El doble búfer es un mecanismo que detecta cuándo ha cambiado la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f7064-129">Double buffering is a mechanism that detects when the toolbar has changed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f7064-130">Comctl32.dll versión 6 no es redistribuible, pero se incluye en Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="f7064-130">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="f7064-131">Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="f7064-131">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="f7064-132">Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.</span><span class="sxs-lookup"><span data-stu-id="f7064-132">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <span data-ttu-id="f7064-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f7064-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f7064-134"><a href="common-control-versions.md">Versión 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="f7064-134"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="f7064-135">Este estilo permite establecer el texto de todos los botones, pero solo se muestra para esos botones con el estilo de botón de <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f7064-135">This style allows you to set text for all buttons, but only display it for those buttons with the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> button style.</span></span> <span data-ttu-id="f7064-136">También se debe establecer el estilo <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f7064-136">The <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> style must also be set.</span></span> <span data-ttu-id="f7064-137">Normalmente, cuando un botón no muestra texto, la aplicación debe controlar <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> o <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> para mostrar una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="f7064-137">Normally, when a button does not display text, your application must handle <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> or <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> to display a tooltip.</span></span> <span data-ttu-id="f7064-138">Con el TBSTYLE_EX_MIXEDBUTTONS estilo extendido, el texto que se establece pero no se muestra en un botón se usará automáticamente como texto de la información sobre herramientas del botón.</span><span class="sxs-lookup"><span data-stu-id="f7064-138">With the TBSTYLE_EX_MIXEDBUTTONS extended style, text that is set but not displayed on a button will automatically be used as the button's tooltip text.</span></span> <span data-ttu-id="f7064-139">La aplicación solo necesita controlar TBN_GETINFOTIP o TTN_GETDISPINFO si necesita más flexibilidad para especificar el texto de la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="f7064-139">Your application only needs to handle TBN_GETINFOTIP or or TTN_GETDISPINFO if it needs more flexibility in specifying the tooltip text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <span data-ttu-id="f7064-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f7064-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f7064-141"><a href="common-control-versions.md">Versión 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="f7064-141"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="f7064-142"><strong>Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.</strong></span><span class="sxs-lookup"><span data-stu-id="f7064-142"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="f7064-143">Este estilo proporciona a la barra de herramientas una orientación vertical y organiza los botones de la barra de herramientas en columnas.</span><span class="sxs-lookup"><span data-stu-id="f7064-143">This style gives the toolbar a vertical orientation and organizes the toolbar buttons into columns.</span></span> <span data-ttu-id="f7064-144">Los botones fluyen verticalmente hasta que un botón supera el alto de límite de la barra de herramientas (vea <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>) y, a continuación, se crea una nueva columna.</span><span class="sxs-lookup"><span data-stu-id="f7064-144">The buttons flow down vertically until a button has exceeded the bounding height of the toolbar (see <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), and then a new column is created.</span></span> <span data-ttu-id="f7064-145">La barra de herramientas fluye los botones de esta manera hasta que se coloquen todos los botones.</span><span class="sxs-lookup"><span data-stu-id="f7064-145">The toolbar flows the buttons in this manner until all buttons are positioned.</span></span> <span data-ttu-id="f7064-146">Para usar este estilo, también se debe establecer el estilo TBSTYLE_EX_VERTICAL.</span><span class="sxs-lookup"><span data-stu-id="f7064-146">To use this style, the TBSTYLE_EX_VERTICAL style must also be set.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f7064-147">Es posible que este estilo no se admita en versiones futuras de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="f7064-147">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="f7064-148">Además, este estilo no se define en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="f7064-148">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="f7064-149">Agregue la siguiente definición a los archivos de origen de la aplicación para usar este estilo: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span><span class="sxs-lookup"><span data-stu-id="f7064-149">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <span data-ttu-id="f7064-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f7064-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f7064-151"><a href="common-control-versions.md">Versión 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="f7064-151"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="f7064-152"><strong>Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.</strong></span><span class="sxs-lookup"><span data-stu-id="f7064-152"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="f7064-153">Este estilo proporciona a la barra de herramientas una orientación vertical.</span><span class="sxs-lookup"><span data-stu-id="f7064-153">This style gives the toolbar a vertical orientation.</span></span> <span data-ttu-id="f7064-154">Los botones de la barra de herramientas fluyen de arriba abajo en lugar de horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="f7064-154">Toolbar buttons flow from top to bottom instead of horizontally.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f7064-155">Es posible que este estilo no se admita en versiones futuras de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="f7064-155">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="f7064-156">Además, este estilo no se define en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="f7064-156">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="f7064-157">Agregue la siguiente definición a los archivos de origen de la aplicación para usar este estilo: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span><span class="sxs-lookup"><span data-stu-id="f7064-157">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span></span></blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="f7064-158">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7064-158">Remarks</span></span>

<span data-ttu-id="f7064-159">Para establecer un estilo extendido, envíe el control de barra de herramientas a un mensaje [**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="f7064-159">To set an extended style, send the toolbar control a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span> <span data-ttu-id="f7064-160">Para determinar qué estilos extendidos están establecidos actualmente, envíe un mensaje de [**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="f7064-160">To determine what extended styles are currently set, send a [**TB\_GETEXTENDEDSTYLE**](tb-getextendedstyle.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7064-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7064-161">Requirements</span></span>



| <span data-ttu-id="f7064-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7064-162">Requirement</span></span> | <span data-ttu-id="f7064-163">Value</span><span class="sxs-lookup"><span data-stu-id="f7064-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7064-164">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7064-164">Header</span></span><br/> | <dl> <span data-ttu-id="f7064-165"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7064-165"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





