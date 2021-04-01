---
title: Código de notificación de NM_CUSTOMDRAW (TrackBar) (commctrl. h)
description: Enviado por un control TrackBar para notificar a sus ventanas principales las operaciones de dibujo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- Controles de Windows de código de notificación de NM_CUSTOMDRAW (TrackBar)
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
ms.openlocfilehash: 68ebbffd531fb44e2491d72954ce111db208f2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151266"
---
# <a name="nm_customdraw-trackbar-notification-code"></a><span data-ttu-id="01b75-105">Código de notificación de NM \_ CUSTOMDRAW (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="01b75-105">NM\_CUSTOMDRAW (trackbar) notification code</span></span>

<span data-ttu-id="01b75-106">Enviado por un control TrackBar para notificar a sus ventanas principales las operaciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="01b75-106">Sent by a trackbar control to notify its parent windows about drawing operations.</span></span> <span data-ttu-id="01b75-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="01b75-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="01b75-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01b75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01b75-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01b75-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01b75-110">Puntero a una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="01b75-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="01b75-111">El miembro **dwItemSpec** de esta estructura contendrá uno de los [valores de dibujo personalizados](custom-draw-values.md) que indica qué parte del control se está dibujando.</span><span class="sxs-lookup"><span data-stu-id="01b75-111">The **dwItemSpec** member of this structure will contain one of the [Custom Draw Values](custom-draw-values.md) that indicates which part of the control is being drawn.</span></span> <span data-ttu-id="01b75-112">Los controles TrackBar insertan los valores siguientes en el miembro **dwItemSpec** de esta estructura para identificar la parte del control que se está dibujando:</span><span class="sxs-lookup"><span data-stu-id="01b75-112">Trackbar controls insert the following values into the **dwItemSpec** member of this structure to identify the portion of the control being drawn:</span></span>



| <span data-ttu-id="01b75-113">Value</span><span class="sxs-lookup"><span data-stu-id="01b75-113">Value</span></span>                                                                                                                                                      | <span data-ttu-id="01b75-114">Significado</span><span class="sxs-lookup"><span data-stu-id="01b75-114">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="01b75-115"><dt>**\_canal TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="01b75-115"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="01b75-116">Identifica el canal en el que se desplaza el marcador de control de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="01b75-116">Identifies the channel that the trackbar control's thumb marker slides along.</span></span> <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="01b75-117"><dt>**\_Thumb TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="01b75-117"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="01b75-118">Identifica el marcador de control de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="01b75-118">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="01b75-119">Esta es la parte del control que mueve el usuario.</span><span class="sxs-lookup"><span data-stu-id="01b75-119">This is the portion of the control that the user moves.</span></span> <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="01b75-120"><dt>**TBCD \_ las marcas**</dt></span><span class="sxs-lookup"><span data-stu-id="01b75-120"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="01b75-121">Identifica las marcas de graduación de incremento que aparecen a lo largo del borde del control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="01b75-121">Identifies the increment tick marks that appear along the edge of the trackbar control.</span></span> <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01b75-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01b75-122">Return value</span></span>

<span data-ttu-id="01b75-123">El valor que la aplicación puede devolver depende de la fase de dibujo actual.</span><span class="sxs-lookup"><span data-stu-id="01b75-123">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="01b75-124">El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo.</span><span class="sxs-lookup"><span data-stu-id="01b75-124">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="01b75-125">Debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="01b75-125">You must return one of the following values.</span></span>



| <span data-ttu-id="01b75-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="01b75-126">Return code</span></span>                                                                                            | <span data-ttu-id="01b75-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="01b75-127">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01b75-128"><dt>**CDRF \_ predeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="01b75-128"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="01b75-129">El control se dibujará por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="01b75-129">The control will draw itself.</span></span> <span data-ttu-id="01b75-130">No enviará ningún código de notificación [nm \_ CUSTOMDRAW](nm-customdraw.md) adicional para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="01b75-130">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="01b75-131">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="01b75-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="01b75-132"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="01b75-132"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="01b75-133">El control notificará al elemento primario de cualquier operación de dibujo relacionada con los elementos.</span><span class="sxs-lookup"><span data-stu-id="01b75-133">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="01b75-134">Enviará los códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar los elementos.</span><span class="sxs-lookup"><span data-stu-id="01b75-134">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="01b75-135">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="01b75-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                         |
| <dl> <span data-ttu-id="01b75-136"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="01b75-136"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="01b75-137">El control notificará al elemento primario después de borrar un elemento.</span><span class="sxs-lookup"><span data-stu-id="01b75-137">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="01b75-138">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="01b75-138">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="01b75-139"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="01b75-139"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="01b75-140">El control notificará al elemento primario después de que se dibuje un elemento.</span><span class="sxs-lookup"><span data-stu-id="01b75-140">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="01b75-141">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="01b75-141">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="01b75-142"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="01b75-142"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="01b75-143">[Versión 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="01b75-143">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="01b75-144">El control notificará al elemento primario cuando se dibuje un subelemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="01b75-144">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="01b75-145">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="01b75-145">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="01b75-146"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="01b75-146"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="01b75-147">La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente.</span><span class="sxs-lookup"><span data-stu-id="01b75-147">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="01b75-148">Para obtener más información sobre cómo cambiar las fuentes, consulte [cambiar fuentes y colores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="01b75-148">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="01b75-149">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="01b75-149">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="01b75-150"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="01b75-150"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="01b75-151">La aplicación dibujó el elemento manualmente.</span><span class="sxs-lookup"><span data-stu-id="01b75-151">Your application drew the item manually.</span></span> <span data-ttu-id="01b75-152">El control no dibujará el elemento.</span><span class="sxs-lookup"><span data-stu-id="01b75-152">The control will not draw the item.</span></span> <span data-ttu-id="01b75-153">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="01b75-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="01b75-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01b75-154">Requirements</span></span>



| <span data-ttu-id="01b75-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b75-155">Requirement</span></span> | <span data-ttu-id="01b75-156">Value</span><span class="sxs-lookup"><span data-stu-id="01b75-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01b75-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01b75-157">Minimum supported client</span></span><br/> | <span data-ttu-id="01b75-158">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="01b75-158">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01b75-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01b75-159">Minimum supported server</span></span><br/> | <span data-ttu-id="01b75-160">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="01b75-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01b75-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01b75-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="01b75-162"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="01b75-162"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01b75-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="01b75-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b75-164">Usar Draw personalizado</span><span class="sxs-lookup"><span data-stu-id="01b75-164">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





