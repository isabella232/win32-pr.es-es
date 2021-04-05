---
title: Código de notificación de NM_CUSTOMDRAW (información sobre herramientas) (commctrl. h)
description: Lo envía un control ToolTip para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- Código de notificación de NM_CUSTOMDRAW (información sobre herramientas), controles de Windows
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
ms.openlocfilehash: 9ce1047f63c8580051f7d57abf3308bde37238a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804135"
---
# <a name="nm_customdraw-tooltip-notification-code"></a><span data-ttu-id="42e2d-105">Código de notificación de NM \_ CUSTOMDRAW (ToolTip)</span><span class="sxs-lookup"><span data-stu-id="42e2d-105">NM\_CUSTOMDRAW (tooltip) notification code</span></span>

<span data-ttu-id="42e2d-106">Lo envía un control ToolTip para notificar a su ventana primaria sobre las operaciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="42e2d-106">Sent by a tooltip control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="42e2d-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="42e2d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="42e2d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42e2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42e2d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42e2d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42e2d-110">Puntero a una estructura [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) que contiene información sobre la operación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="42e2d-110">Pointer to an [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) structure that contains information about the drawing operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42e2d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42e2d-111">Return value</span></span>

<span data-ttu-id="42e2d-112">El valor que la aplicación puede devolver depende de la fase de dibujo actual.</span><span class="sxs-lookup"><span data-stu-id="42e2d-112">The value that your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="42e2d-113">El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo.</span><span class="sxs-lookup"><span data-stu-id="42e2d-113">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="42e2d-114">Debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="42e2d-114">You must return one of the following values.</span></span>



| <span data-ttu-id="42e2d-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="42e2d-115">Return code</span></span>                                                                                            | <span data-ttu-id="42e2d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="42e2d-116">Description</span></span>                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42e2d-117"><dt>**CDRF \_ predeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="42e2d-117"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="42e2d-118">El control se dibujará por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="42e2d-118">The control will draw itself.</span></span> <span data-ttu-id="42e2d-119">No enviará ningún código de notificación [nm \_ CUSTOMDRAW](nm-customdraw.md) adicional para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="42e2d-119">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="42e2d-120">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="42e2d-120">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="42e2d-121"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="42e2d-121"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="42e2d-122">El control notificará al elemento primario de cualquier operación de dibujo relacionada con los elementos.</span><span class="sxs-lookup"><span data-stu-id="42e2d-122">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="42e2d-123">Enviará los códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar los elementos.</span><span class="sxs-lookup"><span data-stu-id="42e2d-123">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="42e2d-124">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="42e2d-124">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                            |
| <dl> <span data-ttu-id="42e2d-125"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="42e2d-125"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="42e2d-126">El control notificará al elemento primario después de borrar un elemento.</span><span class="sxs-lookup"><span data-stu-id="42e2d-126">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="42e2d-127">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="42e2d-127">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="42e2d-128"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="42e2d-128"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="42e2d-129">El control notificará al elemento primario después de que se dibuje un elemento.</span><span class="sxs-lookup"><span data-stu-id="42e2d-129">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="42e2d-130">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="42e2d-130">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="42e2d-131"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="42e2d-131"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="42e2d-132">[Versión 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="42e2d-132">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="42e2d-133">El control notificará al elemento primario cuando se dibuje un subelemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="42e2d-133">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="42e2d-134">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="42e2d-134">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="42e2d-135"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="42e2d-135"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="42e2d-136">La aplicación especificó una nueva fuente para el elemento.</span><span class="sxs-lookup"><span data-stu-id="42e2d-136">Your application specified a new font for the item.</span></span> <span data-ttu-id="42e2d-137">El control usará la nueva fuente.</span><span class="sxs-lookup"><span data-stu-id="42e2d-137">The control will use the new font.</span></span> <span data-ttu-id="42e2d-138">Para obtener más información acerca de cómo cambiar las fuentes, consulte [cambiar fuentes y colores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="42e2d-138">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="42e2d-139">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="42e2d-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="42e2d-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="42e2d-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="42e2d-141">La aplicación dibujó el elemento manualmente.</span><span class="sxs-lookup"><span data-stu-id="42e2d-141">Your application drew the item manually.</span></span> <span data-ttu-id="42e2d-142">El control no dibujará el elemento.</span><span class="sxs-lookup"><span data-stu-id="42e2d-142">The control will not draw the item.</span></span> <span data-ttu-id="42e2d-143">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="42e2d-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="42e2d-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42e2d-144">Requirements</span></span>



| <span data-ttu-id="42e2d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="42e2d-145">Requirement</span></span> | <span data-ttu-id="42e2d-146">Value</span><span class="sxs-lookup"><span data-stu-id="42e2d-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42e2d-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42e2d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="42e2d-148">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="42e2d-148">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42e2d-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42e2d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="42e2d-150">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="42e2d-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42e2d-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42e2d-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="42e2d-152"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42e2d-152"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42e2d-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="42e2d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e2d-154">Usar Draw personalizado</span><span class="sxs-lookup"><span data-stu-id="42e2d-154">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





