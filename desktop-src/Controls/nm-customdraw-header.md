---
title: Código de notificación de NM_CUSTOMDRAW (encabezado) (commctrl. h)
description: Lo envía un control de encabezado para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 44dab54b-45ef-4fba-93b8-2a3e35cda23f
keywords:
- Controles de Windows de código de notificación de NM_CUSTOMDRAW (encabezado)
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
ms.openlocfilehash: 89d6b35503aebed221da6cec212c6dbf614061f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658411"
---
# <a name="nm_customdraw-header-notification-code"></a><span data-ttu-id="7fd25-105">NM \_ código de notificación de CUSTOMDRAW (encabezado)</span><span class="sxs-lookup"><span data-stu-id="7fd25-105">NM\_CUSTOMDRAW (header) notification code</span></span>

<span data-ttu-id="7fd25-106">Lo envía un control de encabezado para notificar a su ventana primaria sobre las operaciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="7fd25-106">Sent by a header control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="7fd25-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7fd25-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7fd25-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fd25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fd25-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fd25-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fd25-110">Puntero a una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="7fd25-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="7fd25-111">El miembro **dwItemSpec** de esta estructura contiene el índice del elemento que se está dibujando y el miembro **lItemlParam** de esta estructura contiene el *lParam* del elemento.</span><span class="sxs-lookup"><span data-stu-id="7fd25-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fd25-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fd25-112">Return value</span></span>

<span data-ttu-id="7fd25-113">El valor que la aplicación puede devolver depende de la fase de dibujo actual.</span><span class="sxs-lookup"><span data-stu-id="7fd25-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="7fd25-114">El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo.</span><span class="sxs-lookup"><span data-stu-id="7fd25-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="7fd25-115">Debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7fd25-115">You must return one of the following values.</span></span>



| <span data-ttu-id="7fd25-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7fd25-116">Return code</span></span>                                                                                            | <span data-ttu-id="7fd25-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fd25-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fd25-118"><dt>**CDRF \_ predeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd25-118"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="7fd25-119">El control se dibujará por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="7fd25-119">The control will draw itself.</span></span> <span data-ttu-id="7fd25-120">No enviará ningún mensaje de [ \_ CUSTOMDRAW nm](nm-customdraw.md) adicional para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="7fd25-120">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) messages for this paint cycle.</span></span> <span data-ttu-id="7fd25-121">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="7fd25-121">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="7fd25-122"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd25-122"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="7fd25-123">El control notificará al elemento primario de cualquier operación de dibujo relacionada con los elementos.</span><span class="sxs-lookup"><span data-stu-id="7fd25-123">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="7fd25-124">Enviará \_ los códigos de notificación de nm CUSTOMDRAW antes y después de dibujar los elementos.</span><span class="sxs-lookup"><span data-stu-id="7fd25-124">It will send NM\_CUSTOMDRAW notification codes before and after drawing items.</span></span> <span data-ttu-id="7fd25-125">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="7fd25-125">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="7fd25-126"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd25-126"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="7fd25-127">El control notificará al elemento primario después de borrar un elemento.</span><span class="sxs-lookup"><span data-stu-id="7fd25-127">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="7fd25-128">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="7fd25-128">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="7fd25-129"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd25-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="7fd25-130">El control notificará al elemento primario después de que se dibuje un elemento.</span><span class="sxs-lookup"><span data-stu-id="7fd25-130">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="7fd25-131">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="7fd25-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="7fd25-132"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd25-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="7fd25-133">[Versiones de control comunes](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="7fd25-133">[Common Control Versions](common-control-versions.md).</span></span> <span data-ttu-id="7fd25-134">El control notificará al elemento primario cuando se dibuje un subelemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="7fd25-134">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="7fd25-135">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="7fd25-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="7fd25-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd25-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="7fd25-137">La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente.</span><span class="sxs-lookup"><span data-stu-id="7fd25-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="7fd25-138">Para obtener más información sobre cómo cambiar las fuentes, consulte [cambiar fuentes y colores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="7fd25-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="7fd25-139">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="7fd25-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="7fd25-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd25-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="7fd25-141">La aplicación dibujó el elemento manualmente.</span><span class="sxs-lookup"><span data-stu-id="7fd25-141">Your application drew the item manually.</span></span> <span data-ttu-id="7fd25-142">El control no dibujará el elemento.</span><span class="sxs-lookup"><span data-stu-id="7fd25-142">The control will not draw the item.</span></span> <span data-ttu-id="7fd25-143">Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="7fd25-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7fd25-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fd25-144">Remarks</span></span>

<span data-ttu-id="7fd25-145">Consulte [uso de Draw personalizado](custom-draw.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7fd25-145">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd25-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fd25-146">Requirements</span></span>



| <span data-ttu-id="7fd25-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fd25-147">Requirement</span></span> | <span data-ttu-id="7fd25-148">Value</span><span class="sxs-lookup"><span data-stu-id="7fd25-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd25-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fd25-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd25-150">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7fd25-150">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fd25-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fd25-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd25-152">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7fd25-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fd25-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fd25-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fd25-154"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fd25-154"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





