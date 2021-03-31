---
title: Código de notificación de NM_CUSTOMDRAW (vista de árbol) (commctrl. h)
description: Lo envía un control de vista de árbol para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- Código de notificación de NM_CUSTOMDRAW (vista de árbol) controles de Windows
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
ms.openlocfilehash: 2bb3f7b44748c2ac9c5b9651c079a8b90df0c508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905002"
---
# <a name="nm_customdraw-tree-view-notification-code"></a><span data-ttu-id="8815c-105">NM \_ CUSTOMDRAW (vista de árbol) código de notificación</span><span class="sxs-lookup"><span data-stu-id="8815c-105">NM\_CUSTOMDRAW (tree view) notification code</span></span>

<span data-ttu-id="8815c-106">Lo envía un control de vista de árbol para notificar a su ventana primaria sobre las operaciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="8815c-106">Sent by a tree-view control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="8815c-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8815c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8815c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8815c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8815c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8815c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8815c-110">Puntero a una estructura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) que contiene y recibe información sobre la operación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="8815c-110">Pointer to an [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure that contains and receives information about the drawing operation.</span></span> <span data-ttu-id="8815c-111">El miembro **dwItemSpec** del miembro **nmcd** de esta estructura contiene el identificador del elemento que se está dibujando.</span><span class="sxs-lookup"><span data-stu-id="8815c-111">The **dwItemSpec** member of the **nmcd** member of this structure contains the handle of the item being drawn.</span></span> <span data-ttu-id="8815c-112">El miembro **lItemlParam** del miembro **nmcd** de esta estructura contiene el *lParam* del elemento que se está dibujando.</span><span class="sxs-lookup"><span data-stu-id="8815c-112">The **lItemlParam** member of the **nmcd** member of this structure contains the *lParam* of the item being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8815c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8815c-113">Return value</span></span>

<span data-ttu-id="8815c-114">El valor que la aplicación puede devolver depende de la fase de dibujo actual.</span><span class="sxs-lookup"><span data-stu-id="8815c-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="8815c-115">El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo.</span><span class="sxs-lookup"><span data-stu-id="8815c-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="8815c-116">Debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8815c-116">You must return one of the following values.</span></span>



| <span data-ttu-id="8815c-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8815c-117">Return code</span></span>                                                                                            | <span data-ttu-id="8815c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8815c-118">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8815c-119"><dt>**CDRF \_ predeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="8815c-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="8815c-120">El control se dibuja a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="8815c-120">The control draws itself.</span></span> <span data-ttu-id="8815c-121">No envía ningún código [ \_ CUSTOMDRAW nm](nm-customdraw.md) adicional para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="8815c-121">It does not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) codes for this paint cycle.</span></span> <span data-ttu-id="8815c-122">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="8815c-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="8815c-123"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="8815c-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="8815c-124">El control notifica al elemento primario de cualquier operación de dibujo relacionada con los elementos.</span><span class="sxs-lookup"><span data-stu-id="8815c-124">The control notifies the parent of any item-related drawing operations.</span></span> <span data-ttu-id="8815c-125">Envía códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar los elementos.</span><span class="sxs-lookup"><span data-stu-id="8815c-125">It sends [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="8815c-126">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="8815c-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                |
| <dl> <span data-ttu-id="8815c-127"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="8815c-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="8815c-128">El control notifica al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="8815c-128">The control notifies the parent after erasing an item.This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="8815c-129"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="8815c-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="8815c-130">El control notifica al elemento primario después de dibujar un elemento.</span><span class="sxs-lookup"><span data-stu-id="8815c-130">The control notifies the parent after painting an item.</span></span> <span data-ttu-id="8815c-131">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="8815c-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="8815c-132"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="8815c-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | [<span data-ttu-id="8815c-133">Versión 4,71.</span><span class="sxs-lookup"><span data-stu-id="8815c-133">Version 4.71.</span></span>](common-control-versions.md) <span data-ttu-id="8815c-134">El control notifica al elemento primario cuando se dibuja un subelemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="8815c-134">The control notifies the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="8815c-135">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="8815c-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="8815c-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="8815c-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="8815c-137">La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente.</span><span class="sxs-lookup"><span data-stu-id="8815c-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="8815c-138">Para obtener más información sobre cómo cambiar las fuentes, consulte [cambiar fuentes y colores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="8815c-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="8815c-139">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="8815c-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="8815c-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="8815c-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="8815c-141">La aplicación dibujó el elemento manualmente.</span><span class="sxs-lookup"><span data-stu-id="8815c-141">Your application drew the item manually.</span></span> <span data-ttu-id="8815c-142">El control no dibujará el elemento.</span><span class="sxs-lookup"><span data-stu-id="8815c-142">The control will not draw the item.</span></span> <span data-ttu-id="8815c-143">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="8815c-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="8815c-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8815c-144">Remarks</span></span>

[<span data-ttu-id="8815c-145">Versión 5,80.</span><span class="sxs-lookup"><span data-stu-id="8815c-145">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="8815c-146">Si cambia la fuente devolviendo [**CDRF \_ NEWFONT**](cdrf-constants.md), el control de vista de árbol podría mostrar texto recortado.</span><span class="sxs-lookup"><span data-stu-id="8815c-146">If you change the font by returning [**CDRF\_NEWFONT**](cdrf-constants.md), the tree-view control might display clipped text.</span></span> <span data-ttu-id="8815c-147">Este comportamiento es necesario para la compatibilidad con versiones anteriores de los controles comunes.</span><span class="sxs-lookup"><span data-stu-id="8815c-147">This behavior is necessary for backward compatibility with earlier versions of the common controls.</span></span> <span data-ttu-id="8815c-148">Si desea cambiar la fuente de un control de vista de árbol, obtendrá mejores resultados si envía un mensaje [**\_ SETVERSION de CCM**](ccm-setversion.md) con el valor de *wParam* establecido en 5 antes de agregar elementos al control.</span><span class="sxs-lookup"><span data-stu-id="8815c-148">If you want to change the font of a tree-view control, you will get better results if you send a [**CCM\_SETVERSION**](ccm-setversion.md) message with the *wParam* value set to 5 before adding any items to the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="8815c-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8815c-149">Requirements</span></span>



| <span data-ttu-id="8815c-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="8815c-150">Requirement</span></span> | <span data-ttu-id="8815c-151">Value</span><span class="sxs-lookup"><span data-stu-id="8815c-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8815c-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8815c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="8815c-153">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8815c-153">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8815c-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8815c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="8815c-155">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8815c-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8815c-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8815c-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="8815c-157"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8815c-157"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8815c-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="8815c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8815c-159">Usar Draw personalizado</span><span class="sxs-lookup"><span data-stu-id="8815c-159">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





