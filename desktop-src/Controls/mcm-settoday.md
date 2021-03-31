---
title: Mensaje de MCM_SETTODAY (commctrl. h)
description: Establece el 0034; actualmente \ 0034; selección de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetToday.
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- MCM_SETTODAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b725e5f61e3c08170a323b063616434acb857e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804010"
---
# <a name="mcm_settoday-message"></a><span data-ttu-id="66193-105">Mensaje de MCM \_ SETTODAY</span><span class="sxs-lookup"><span data-stu-id="66193-105">MCM\_SETTODAY message</span></span>

<span data-ttu-id="66193-106">Establece la selección "hoy" para un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="66193-106">Sets the "today" selection for a month calendar control.</span></span> <span data-ttu-id="66193-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) .</span><span class="sxs-lookup"><span data-stu-id="66193-107">You can send this message explicitly or by using the [**MonthCal\_SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="66193-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66193-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66193-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66193-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="66193-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="66193-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="66193-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66193-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66193-112">Puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contiene la fecha que se va a establecer como la selección "hoy" del control.</span><span class="sxs-lookup"><span data-stu-id="66193-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the "today" selection for the control.</span></span> <span data-ttu-id="66193-113">Si este parámetro se establece en **null**, el control vuelve a la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="66193-113">If this parameter is set to **NULL**, the control returns to the default setting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66193-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66193-114">Return value</span></span>

<span data-ttu-id="66193-115">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="66193-115">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="66193-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66193-116">Remarks</span></span>

<span data-ttu-id="66193-117">Si la selección "hoy" está establecida en cualquier fecha distinta de la predeterminada, se aplican las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="66193-117">If the "today" selection is set to any date other than the default, the following conditions apply:</span></span>

-   <span data-ttu-id="66193-118">El control no actualizará automáticamente la selección "hoy" cuando la hora pase la medianoche del día actual.</span><span class="sxs-lookup"><span data-stu-id="66193-118">The control will not automatically update the "today" selection when the time passes midnight for the current day.</span></span>
-   <span data-ttu-id="66193-119">El control no actualizará automáticamente su presentación en función de los cambios de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="66193-119">The control will not automatically update its display based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="66193-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66193-120">Requirements</span></span>



| <span data-ttu-id="66193-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="66193-121">Requirement</span></span> | <span data-ttu-id="66193-122">Value</span><span class="sxs-lookup"><span data-stu-id="66193-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66193-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66193-123">Minimum supported client</span></span><br/> | <span data-ttu-id="66193-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="66193-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66193-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66193-125">Minimum supported server</span></span><br/> | <span data-ttu-id="66193-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="66193-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66193-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66193-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="66193-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66193-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66193-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="66193-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66193-130">Horas en el control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="66193-130">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

