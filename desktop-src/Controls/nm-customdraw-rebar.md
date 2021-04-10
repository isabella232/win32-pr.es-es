---
title: Código de notificación de NM_CUSTOMDRAW (rebar) (commctrl. h)
description: Lo envía el control rebar para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3ba9bb59-f297-4af1-a9a9-d8789def5bde
keywords:
- Código de notificación NM_CUSTOMDRAW (rebar) controles de Windows
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
ms.openlocfilehash: 329f3e9abfb20dbca8cebd3a6bf02673ad00f904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151267"
---
# <a name="nm_customdraw-rebar-notification-code"></a><span data-ttu-id="78bf1-105">Código de notificación de NM \_ CUSTOMDRAW (rebar)</span><span class="sxs-lookup"><span data-stu-id="78bf1-105">NM\_CUSTOMDRAW (rebar) notification code</span></span>

<span data-ttu-id="78bf1-106">Lo envía el control rebar para notificar a su ventana primaria sobre las operaciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="78bf1-106">Sent by the rebar control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="78bf1-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="78bf1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="78bf1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78bf1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78bf1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78bf1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78bf1-110">Puntero a una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="78bf1-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="78bf1-111">El miembro **dwItemSpec** de esta estructura contiene el identificador de la banda que se está dibujando.</span><span class="sxs-lookup"><span data-stu-id="78bf1-111">The **dwItemSpec** member of this structure contains the identifier of the band being drawn.</span></span> <span data-ttu-id="78bf1-112">El miembro **lItemlParam** de esta estructura contiene el *lParam* de la banda que se está dibujando.</span><span class="sxs-lookup"><span data-stu-id="78bf1-112">The **lItemlParam** member of this structure contains the *lParam* of the band being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78bf1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78bf1-113">Return value</span></span>

<span data-ttu-id="78bf1-114">El valor que la aplicación puede devolver depende de la fase de dibujo actual.</span><span class="sxs-lookup"><span data-stu-id="78bf1-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="78bf1-115">El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo.</span><span class="sxs-lookup"><span data-stu-id="78bf1-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="78bf1-116">Debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="78bf1-116">You must return one of the following values.</span></span>



| <span data-ttu-id="78bf1-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="78bf1-117">Return code</span></span>                                                                                            | <span data-ttu-id="78bf1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="78bf1-118">Description</span></span>                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="78bf1-119"><dt>**CDRF \_ predeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="78bf1-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="78bf1-120">El control se dibujará por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="78bf1-120">The control will draw itself.</span></span> <span data-ttu-id="78bf1-121">No enviará ninguna notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) adicional para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="78bf1-121">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notifications for this paint cycle.</span></span> <span data-ttu-id="78bf1-122">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="78bf1-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="78bf1-123"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="78bf1-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="78bf1-124">El control notificará al elemento primario de cualquier operación de dibujo relacionada con los elementos.</span><span class="sxs-lookup"><span data-stu-id="78bf1-124">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="78bf1-125">Enviará los códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar los elementos.</span><span class="sxs-lookup"><span data-stu-id="78bf1-125">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="78bf1-126">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="78bf1-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="78bf1-127"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="78bf1-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="78bf1-128">El control notificará al elemento primario después de borrar un elemento.</span><span class="sxs-lookup"><span data-stu-id="78bf1-128">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="78bf1-129">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="78bf1-129">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="78bf1-130"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="78bf1-130"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="78bf1-131">El control notificará al elemento primario después de que se dibuje un elemento.</span><span class="sxs-lookup"><span data-stu-id="78bf1-131">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="78bf1-132">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="78bf1-132">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="78bf1-133"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="78bf1-133"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="78bf1-134">El control notificará al elemento primario de cualquier operación de dibujo relacionada con los elementos.</span><span class="sxs-lookup"><span data-stu-id="78bf1-134">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="78bf1-135">Enviará los códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar los elementos.</span><span class="sxs-lookup"><span data-stu-id="78bf1-135">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="78bf1-136">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="78bf1-136">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="78bf1-137"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="78bf1-137"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="78bf1-138">La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente.</span><span class="sxs-lookup"><span data-stu-id="78bf1-138">The application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="78bf1-139">Para obtener más información acerca de cómo cambiar las fuentes, consulte [cambiar fuentes y colores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="78bf1-139">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="78bf1-140">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="78bf1-140">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="78bf1-141"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="78bf1-141"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="78bf1-142">La aplicación dibujó el elemento manualmente.</span><span class="sxs-lookup"><span data-stu-id="78bf1-142">The application drew the item manually.</span></span> <span data-ttu-id="78bf1-143">El control no dibujará el elemento.</span><span class="sxs-lookup"><span data-stu-id="78bf1-143">The control will not draw the item.</span></span> <span data-ttu-id="78bf1-144">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="78bf1-144">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="78bf1-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78bf1-145">Requirements</span></span>



| <span data-ttu-id="78bf1-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="78bf1-146">Requirement</span></span> | <span data-ttu-id="78bf1-147">Value</span><span class="sxs-lookup"><span data-stu-id="78bf1-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78bf1-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78bf1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="78bf1-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="78bf1-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78bf1-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78bf1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="78bf1-151">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="78bf1-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78bf1-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78bf1-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="78bf1-153"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="78bf1-153"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78bf1-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="78bf1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78bf1-155">Usar Draw personalizado</span><span class="sxs-lookup"><span data-stu-id="78bf1-155">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





