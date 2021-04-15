---
title: Código de notificación de NM_CUSTOMDRAW (Button) (commctrl. h)
description: Notifica a la ventana primaria de un control de botón sobre las operaciones de dibujo personalizadas en el botón. El control de botón envía este código de notificación en forma de mensaje de notificación de WM \_ .
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- Controles de Windows de código de notificación de NM_CUSTOMDRAW (botón)
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
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493318"
---
# <a name="nm_customdraw-button-notification-code"></a><span data-ttu-id="58000-105">Código de notificación de NM \_ CUSTOMDRAW (Button)</span><span class="sxs-lookup"><span data-stu-id="58000-105">NM\_CUSTOMDRAW (button) notification code</span></span>

<span data-ttu-id="58000-106">Notifica a la ventana primaria de un control de botón sobre las operaciones de dibujo personalizadas en el botón.</span><span class="sxs-lookup"><span data-stu-id="58000-106">Notifies the parent window of a button control about custom draw operations on the button.</span></span>

<span data-ttu-id="58000-107">El control de botón envía este código de notificación en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="58000-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="58000-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58000-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58000-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58000-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58000-110">Puntero a una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="58000-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="58000-111">El miembro **dwItemSpec** de esta estructura contiene el índice del elemento que se está dibujando y el miembro **lItemlParam** de esta estructura contiene el *lParam* del elemento.</span><span class="sxs-lookup"><span data-stu-id="58000-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58000-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58000-112">Return value</span></span>

<span data-ttu-id="58000-113">El valor que la aplicación puede devolver depende de la fase de dibujo actual.</span><span class="sxs-lookup"><span data-stu-id="58000-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="58000-114">El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo.</span><span class="sxs-lookup"><span data-stu-id="58000-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="58000-115">Debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="58000-115">You must return one of the following values.</span></span>



| <span data-ttu-id="58000-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="58000-116">Return code</span></span>                                                                                          | <span data-ttu-id="58000-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="58000-117">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58000-118"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="58000-118"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl> | <span data-ttu-id="58000-119">El control notificará al elemento primario después de borrar un elemento.</span><span class="sxs-lookup"><span data-stu-id="58000-119">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="58000-120">Solo se puede usar si **dwDrawStage** es igual a CDDS \_ preerase.</span><span class="sxs-lookup"><span data-stu-id="58000-120">This can be used only if **dwDrawStage** equals CDDS\_PREERASE.</span></span><br/>                                  |
| <dl> <span data-ttu-id="58000-121"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="58000-121"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl> | <span data-ttu-id="58000-122">El control notificará al elemento primario después de que se dibuje un elemento.</span><span class="sxs-lookup"><span data-stu-id="58000-122">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="58000-123">Solo se puede usar si **dwDrawStage** es igual a CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="58000-123">This can be used only if **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                 |
| <dl> <span data-ttu-id="58000-124"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="58000-124"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>     | <span data-ttu-id="58000-125">La aplicación dibujó el elemento manualmente.</span><span class="sxs-lookup"><span data-stu-id="58000-125">The application drew the item manually.</span></span> <span data-ttu-id="58000-126">El control no dibujará el elemento.</span><span class="sxs-lookup"><span data-stu-id="58000-126">The control will not draw the item.</span></span> <span data-ttu-id="58000-127">Se puede usar cuando **dwDrawStage** es igual a CDDS \_ preerase o CDDS \_ PREPAINT.</span><span class="sxs-lookup"><span data-stu-id="58000-127">This can be used when **dwDrawStage** equals CDDS\_PREERASE or CDDS\_PREPAINT.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="58000-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58000-128">Remarks</span></span>

<span data-ttu-id="58000-129">Si el control de botón está marcado como OwnerDraw (BS \_ OwnerDraw), el código de notificación de nm \_ CUSTOMDRAW no se envía.</span><span class="sxs-lookup"><span data-stu-id="58000-129">If the button control is marked ownerdraw (BS\_OWNERDRAW), the NM\_CUSTOMDRAW notification code is not sent.</span></span>

<span data-ttu-id="58000-130">Consulte [uso de Draw personalizado](custom-draw.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="58000-130">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

> [!Note]  
> <span data-ttu-id="58000-131">Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="58000-131">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="58000-132">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="58000-132">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58000-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58000-133">Requirements</span></span>



| <span data-ttu-id="58000-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="58000-134">Requirement</span></span> | <span data-ttu-id="58000-135">Value</span><span class="sxs-lookup"><span data-stu-id="58000-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58000-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58000-136">Minimum supported client</span></span><br/> | <span data-ttu-id="58000-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="58000-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="58000-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58000-138">Minimum supported server</span></span><br/> | <span data-ttu-id="58000-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="58000-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="58000-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58000-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="58000-141"><dt>Commctrl. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58000-141"><dt>Commctrl.h (include Windows.h)</dt></span></span> </dl> |



 

 





