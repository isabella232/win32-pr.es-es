---
title: Código de notificación de DTN_CLOSEUP (commctrl. h)
description: Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario cierra el calendario del mes desplegable.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- DTN_CLOSEUP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfcfb23215aeffe15bec576075fd4d930790e47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803272"
---
# <a name="dtn_closeup-notification-code"></a><span data-ttu-id="76ec6-104">Código de notificación de primer plano de DTN \_</span><span class="sxs-lookup"><span data-stu-id="76ec6-104">DTN\_CLOSEUP notification code</span></span>

<span data-ttu-id="76ec6-105">Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario cierra el calendario del mes desplegable.</span><span class="sxs-lookup"><span data-stu-id="76ec6-105">Sent by a date and time picker (DTP) control when the user closes the drop-down month calendar.</span></span> <span data-ttu-id="76ec6-106">El calendario mensual se cierra cuando el usuario elige una fecha en el calendario mensual o hace clic en la flecha desplegable mientras el calendario está abierto.</span><span class="sxs-lookup"><span data-stu-id="76ec6-106">The month calendar is closed when the user chooses a date from the month calendar or clicks the drop-down arrow while the calendar is open.</span></span> <span data-ttu-id="76ec6-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="76ec6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="76ec6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76ec6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76ec6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76ec6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76ec6-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre la notificación.</span><span class="sxs-lookup"><span data-stu-id="76ec6-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76ec6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76ec6-111">Return value</span></span>

<span data-ttu-id="76ec6-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="76ec6-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="76ec6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76ec6-113">Remarks</span></span>

<span data-ttu-id="76ec6-114">Los controles de DTP no mantienen un control de calendario mensual secundario estático.</span><span class="sxs-lookup"><span data-stu-id="76ec6-114">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="76ec6-115">El control de DTP destruye el control de calendario mensual secundario antes de enviar este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="76ec6-115">The DTP control destroys the child month calendar control prior to sending this notification code.</span></span> <span data-ttu-id="76ec6-116">Por lo tanto, la aplicación no debe basarse en un identificador de ventana estático para el calendario mensual del control.</span><span class="sxs-lookup"><span data-stu-id="76ec6-116">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="76ec6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76ec6-117">Requirements</span></span>



| <span data-ttu-id="76ec6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="76ec6-118">Requirement</span></span> | <span data-ttu-id="76ec6-119">Value</span><span class="sxs-lookup"><span data-stu-id="76ec6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76ec6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76ec6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76ec6-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="76ec6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76ec6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76ec6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76ec6-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="76ec6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76ec6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76ec6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="76ec6-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="76ec6-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76ec6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="76ec6-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="76ec6-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="76ec6-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="76ec6-128">\_lista desplegable DTN</span><span class="sxs-lookup"><span data-stu-id="76ec6-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="76ec6-129">**DTM \_ GETMONTHCAL**</span><span class="sxs-lookup"><span data-stu-id="76ec6-129">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

 





