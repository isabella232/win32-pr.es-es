---
title: Código de notificación de NM_CUSTOMDRAW (commctrl. h)
description: Notifica a la ventana primaria de un control sobre las operaciones de dibujo personalizadas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- NM_CUSTOMDRAW controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489047"
---
# <a name="nm_customdraw-notification-code"></a><span data-ttu-id="9da2e-105">Código de notificación de NM \_ CUSTOMDRAW</span><span class="sxs-lookup"><span data-stu-id="9da2e-105">NM\_CUSTOMDRAW notification code</span></span>

<span data-ttu-id="9da2e-106">Notifica a la ventana primaria de un control sobre las operaciones de dibujo personalizadas.</span><span class="sxs-lookup"><span data-stu-id="9da2e-106">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="9da2e-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9da2e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a><span data-ttu-id="9da2e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9da2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9da2e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9da2e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9da2e-110">Puntero a una estructura personalizada relacionada con Draw que contiene información sobre la operación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="9da2e-110">A pointer to a custom draw-related structure that contains information about the drawing operation.</span></span> <span data-ttu-id="9da2e-111">En la lista siguiente se especifican los controles y sus estructuras asociadas.</span><span class="sxs-lookup"><span data-stu-id="9da2e-111">The following list specifies the controls and their associated structures.</span></span>



| <span data-ttu-id="9da2e-112">Control</span><span class="sxs-lookup"><span data-stu-id="9da2e-112">Control</span></span>                     | <span data-ttu-id="9da2e-113">Estructura de dibujo personalizada</span><span class="sxs-lookup"><span data-stu-id="9da2e-113">Custom Draw Structure</span></span>                    |
|-----------------------------|------------------------------------------|
| <span data-ttu-id="9da2e-114">Rebar, TrackBar y header</span><span class="sxs-lookup"><span data-stu-id="9da2e-114">Rebar, trackbar, and header</span></span> | [<span data-ttu-id="9da2e-115">**NMCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="9da2e-115">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| <span data-ttu-id="9da2e-116">Vista de lista</span><span class="sxs-lookup"><span data-stu-id="9da2e-116">List view</span></span>                   | [<span data-ttu-id="9da2e-117">**NMLVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="9da2e-117">**NMLVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| <span data-ttu-id="9da2e-118">Información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="9da2e-118">Tooltip</span></span>                     | [<span data-ttu-id="9da2e-119">**NMTTCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="9da2e-119">**NMTTCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| <span data-ttu-id="9da2e-120">Vista de árbol</span><span class="sxs-lookup"><span data-stu-id="9da2e-120">Tree view</span></span>                   | [<span data-ttu-id="9da2e-121">**NMTVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="9da2e-121">**NMTVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| <span data-ttu-id="9da2e-122">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="9da2e-122">Toolbar</span></span>                     | [<span data-ttu-id="9da2e-123">**NMTBCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="9da2e-123">**NMTBCUSTOMDRAW**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9da2e-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9da2e-124">Return value</span></span>

<span data-ttu-id="9da2e-125">El valor que la aplicación puede devolver depende de la fase de dibujo actual.</span><span class="sxs-lookup"><span data-stu-id="9da2e-125">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="9da2e-126">El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo.</span><span class="sxs-lookup"><span data-stu-id="9da2e-126">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="9da2e-127">Debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9da2e-127">You must return one of the following values.</span></span>



| <span data-ttu-id="9da2e-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9da2e-128">Return code</span></span>                                                                                            | <span data-ttu-id="9da2e-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="9da2e-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9da2e-130"><dt>**CDRF \_ predeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="9da2e-130"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="9da2e-131">El control se dibujará por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="9da2e-131">The control will draw itself.</span></span> <span data-ttu-id="9da2e-132">No enviará códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) adicionales para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="9da2e-132">It will not send additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="9da2e-133">Esta marca no se puede usar con ningún otro marcador.</span><span class="sxs-lookup"><span data-stu-id="9da2e-133">This flag cannot be used with any other flag.</span></span> <br/>                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="9da2e-134"><dt>**CDRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9da2e-134"><dt>**CDRF\_DOERASE**</dt></span></span> </dl>           | <span data-ttu-id="9da2e-135">El control solo dibujará el fondo.</span><span class="sxs-lookup"><span data-stu-id="9da2e-135">The control will only draw the background.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="9da2e-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="9da2e-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="9da2e-137">La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente.</span><span class="sxs-lookup"><span data-stu-id="9da2e-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="9da2e-138">Para obtener más información sobre cómo cambiar las fuentes, consulte [cambiar fuentes y colores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="9da2e-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="9da2e-139">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="9da2e-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="9da2e-140"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="9da2e-140"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="9da2e-141">El control notificará al elemento primario de cualquier operación de dibujo relacionada con los elementos.</span><span class="sxs-lookup"><span data-stu-id="9da2e-141">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="9da2e-142">Enviará los códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar los elementos.</span><span class="sxs-lookup"><span data-stu-id="9da2e-142">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="9da2e-143">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="9da2e-143">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="9da2e-144"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="9da2e-144"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="9da2e-145">El control notificará al elemento primario después de borrar un elemento.</span><span class="sxs-lookup"><span data-stu-id="9da2e-145">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="9da2e-146">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="9da2e-146">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="9da2e-147"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="9da2e-147"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="9da2e-148">El control enviará un código de notificación [nm \_ CUSTOMDRAW](nm-customdraw.md) cuando se complete el ciclo de dibujo para todo el control.</span><span class="sxs-lookup"><span data-stu-id="9da2e-148">The control will send an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code when the painting cycle for the entire control is complete.</span></span> <span data-ttu-id="9da2e-149">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="9da2e-149">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="9da2e-150"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="9da2e-150"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="9da2e-151">La aplicación recibirá un código de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** establecido en CDDS \_ ITEMPREPAINT \| CDDS \_ SubItem antes de que se dibuje cada subelemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="9da2e-151">Your application will receive an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code with **dwDrawStage** set to CDDS\_ITEMPREPAINT \| CDDS\_SUBITEM before each list-view subitem is drawn.</span></span> <span data-ttu-id="9da2e-152">Después, puede especificar la fuente y el color de cada subelemento por separado o devolver [**CDRF de \_ forma predeterminada**](cdrf-constants.md) para el procesamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9da2e-152">You can then specify font and color for each subitem separately or return [**CDRF\_DODEFAULT**](cdrf-constants.md) for default processing.</span></span> <span data-ttu-id="9da2e-153">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="9da2e-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="9da2e-154"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="9da2e-154"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="9da2e-155">La aplicación dibujó el elemento manualmente.</span><span class="sxs-lookup"><span data-stu-id="9da2e-155">Your application drew the item manually.</span></span> <span data-ttu-id="9da2e-156">El control no dibujará el elemento.</span><span class="sxs-lookup"><span data-stu-id="9da2e-156">The control will not draw the item.</span></span> <span data-ttu-id="9da2e-157">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="9da2e-157">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="9da2e-158"><dt>**CDRF \_ SKIPPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="9da2e-158"><dt>**CDRF\_SKIPPOSTPAINT**</dt></span></span> </dl>     | <span data-ttu-id="9da2e-159">El control no dibujará el rectángulo de foco alrededor de un elemento.</span><span class="sxs-lookup"><span data-stu-id="9da2e-159">The control will not draw the focus rectangle around an item.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="9da2e-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9da2e-160">Remarks</span></span>

<span data-ttu-id="9da2e-161">Actualmente, los siguientes controles admiten la funcionalidad de dibujo personalizada: encabezado, vista de lista, Rebar, barra de herramientas, información sobre herramientas, TrackBar y vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="9da2e-161">Currently, the following controls support custom draw functionality: header, list view, rebar, toolbar, tooltip, trackbar, and tree view.</span></span> <span data-ttu-id="9da2e-162">El dibujo personalizado también se admite para los controles de botón si tiene un manifiesto de aplicación para asegurarse de que Comctl32.dll versión 6 esté disponible.</span><span class="sxs-lookup"><span data-stu-id="9da2e-162">Custom draw is also supported for button controls if you have an application manifest to ensure that Comctl32.dll version 6 is available.</span></span>

<span data-ttu-id="9da2e-163">Si este mensaje se trata en un procedimiento de cuadro de diálogo, debe establecer el valor devuelto como parte de los datos de la ventana antes de devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="9da2e-163">If this message is handled in a dialog procedure, you must set the return value as part of the window data before returning **TRUE**.</span></span> <span data-ttu-id="9da2e-164">Para obtener más información, vea [**función dialogproc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span><span class="sxs-lookup"><span data-stu-id="9da2e-164">For more information, see [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span></span>

## <a name="requirements"></a><span data-ttu-id="9da2e-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9da2e-165">Requirements</span></span>



| <span data-ttu-id="9da2e-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="9da2e-166">Requirement</span></span> | <span data-ttu-id="9da2e-167">Value</span><span class="sxs-lookup"><span data-stu-id="9da2e-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9da2e-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9da2e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="9da2e-169">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9da2e-169">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9da2e-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9da2e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="9da2e-171">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9da2e-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9da2e-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9da2e-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="9da2e-173"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9da2e-173"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9da2e-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="9da2e-174">See also</span></span>

<dl> <dt>

<span data-ttu-id="9da2e-175">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9da2e-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9da2e-176">Dibujo personalizado</span><span class="sxs-lookup"><span data-stu-id="9da2e-176">Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

