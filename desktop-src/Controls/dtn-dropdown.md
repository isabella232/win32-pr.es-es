---
title: Código de notificación de DTN_DROPDOWN (commctrl. h)
description: Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario activa el calendario del mes desplegable. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- DTN_DROPDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905426"
---
# <a name="dtn_dropdown-notification-code"></a><span data-ttu-id="6d006-105">\_Código de notificación de desplegable DTN</span><span class="sxs-lookup"><span data-stu-id="6d006-105">DTN\_DROPDOWN notification code</span></span>

<span data-ttu-id="6d006-106">Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario activa el calendario del mes desplegable.</span><span class="sxs-lookup"><span data-stu-id="6d006-106">Sent by a date and time picker (DTP) control when the user activates the drop-down month calendar.</span></span> <span data-ttu-id="6d006-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6d006-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="6d006-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d006-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d006-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d006-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d006-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre la notificación.</span><span class="sxs-lookup"><span data-stu-id="6d006-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d006-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d006-111">Return value</span></span>

<span data-ttu-id="6d006-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="6d006-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d006-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d006-113">Remarks</span></span>

<span data-ttu-id="6d006-114">Una tarea que el controlador de notificación puede tener que realizar es personalizar el control de calendario mensual de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="6d006-114">One task that your notification handler may need to perform is to customize the dropdown month-calendar control.</span></span> <span data-ttu-id="6d006-115">Por ejemplo, si no desea "ir a hoy", debe establecer el estilo [**MCS \_ noactual**](month-calendar-control-styles.md)  del control.</span><span class="sxs-lookup"><span data-stu-id="6d006-115">For instance, if you do not want "Go To Today," you need to set the control's [**MCS\_NOTODAY**](month-calendar-control-styles.md)  style.</span></span> <span data-ttu-id="6d006-116">Para recuperar un identificador del control de calendario mensual, envíe el control de DTP a un mensaje [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md) .</span><span class="sxs-lookup"><span data-stu-id="6d006-116">To retrieve a handle to the month-calendar control, send the DTP control a [**DTM\_GETMONTHCAL**](dtm-getmonthcal.md) message.</span></span> <span data-ttu-id="6d006-117">Después, puede usar este identificador y [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer el estilo de calendario mensual deseado.</span><span class="sxs-lookup"><span data-stu-id="6d006-117">You can then use this handle and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) to set the desired month-calendar style.</span></span>

<span data-ttu-id="6d006-118">Los controles de DTP no mantienen un control de calendario mensual secundario estático.</span><span class="sxs-lookup"><span data-stu-id="6d006-118">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="6d006-119">El control de DTP crea un nuevo control de calendario mensual antes de enviar este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="6d006-119">The DTP control creates a new month calendar control before sending this notification code.</span></span> <span data-ttu-id="6d006-120">Además, el control de DTP destruye el control secundario cuando no está activo (visible).</span><span class="sxs-lookup"><span data-stu-id="6d006-120">Additionally, the DTP control destroys the child control when it is not active (visible).</span></span> <span data-ttu-id="6d006-121">Por lo tanto, la aplicación no debe basarse en un identificador de ventana estático para el calendario mensual del control.</span><span class="sxs-lookup"><span data-stu-id="6d006-121">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d006-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d006-122">Requirements</span></span>



| <span data-ttu-id="6d006-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d006-123">Requirement</span></span> | <span data-ttu-id="6d006-124">Value</span><span class="sxs-lookup"><span data-stu-id="6d006-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d006-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d006-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6d006-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6d006-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d006-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d006-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6d006-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d006-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d006-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d006-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d006-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d006-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d006-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d006-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d006-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6d006-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6d006-133">DTN \_ primer plano</span><span class="sxs-lookup"><span data-stu-id="6d006-133">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="6d006-134">**DTM \_ GETMONTHCAL**</span><span class="sxs-lookup"><span data-stu-id="6d006-134">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

