---
title: Mensaje de MCM_SETRANGE (commctrl. h)
description: Establece las fechas mínima y máxima permitida para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetRange.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- MCM_SETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380e599da8cd4a054c02135bc64f57f29d2c81d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658326"
---
# <a name="mcm_setrange-message"></a><span data-ttu-id="6ae0f-105">\_Mensaje de SetRange de MCM</span><span class="sxs-lookup"><span data-stu-id="6ae0f-105">MCM\_SETRANGE message</span></span>

<span data-ttu-id="6ae0f-106">Establece las fechas mínima y máxima permitida para un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-106">Sets the minimum and maximum allowable dates for a month calendar control.</span></span> <span data-ttu-id="6ae0f-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) .</span><span class="sxs-lookup"><span data-stu-id="6ae0f-107">You can send this message explicitly or by using the [**MonthCal\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ae0f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ae0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae0f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ae0f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae0f-110">Valores de marca que especifican los límites de fecha que se establecen.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-110">Flag values that specify which date limits are being set.</span></span> <span data-ttu-id="6ae0f-111">Este valor debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6ae0f-111">This value must be one or both of the following:</span></span>



| <span data-ttu-id="6ae0f-112">Value</span><span class="sxs-lookup"><span data-stu-id="6ae0f-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="6ae0f-113">Significado</span><span class="sxs-lookup"><span data-stu-id="6ae0f-113">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="6ae0f-114"><dt>**GDTR \_ máx.**</dt></span><span class="sxs-lookup"><span data-stu-id="6ae0f-114"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="6ae0f-115">Se está configurando la fecha máxima permitida.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-115">The maximum allowable date is being set.</span></span> <span data-ttu-id="6ae0f-116">La estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en *lpSysTimeArray* \[ 1 \] debe contener información de fecha.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-116">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[1\] must contain date information.</span></span> <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="6ae0f-117"><dt>**GDTR \_ mín.**</dt></span><span class="sxs-lookup"><span data-stu-id="6ae0f-117"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="6ae0f-118">Se está configurando la fecha mínima permitida.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-118">The minimum allowable date is being set.</span></span> <span data-ttu-id="6ae0f-119">La estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en *lpSysTimeArray* \[ 0 \] debe contener información de fecha.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-119">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[0\] must contain date information.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="6ae0f-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ae0f-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae0f-121">Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contiene los límites de fecha.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-121">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain the date limits.</span></span> <span data-ttu-id="6ae0f-122">El límite máximo debe estar en *lpSysTimeArray* \[ 1 \] si \_ se especifica GDTR Max y *lpSysTimeArray* \[ 0 \] debe contener el límite mínimo si \_ se especifica GDTR min.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-122">The maximum limit must be in *lpSysTimeArray*\[1\] if GDTR\_MAX is specified, and *lpSysTimeArray*\[0\] must contain the minimum limit if GDTR\_MIN is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae0f-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ae0f-123">Return value</span></span>

<span data-ttu-id="6ae0f-124">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae0f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ae0f-125">Requirements</span></span>



| <span data-ttu-id="6ae0f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ae0f-126">Requirement</span></span> | <span data-ttu-id="6ae0f-127">Value</span><span class="sxs-lookup"><span data-stu-id="6ae0f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae0f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ae0f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae0f-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6ae0f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ae0f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ae0f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae0f-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ae0f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ae0f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ae0f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ae0f-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ae0f-133"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ae0f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ae0f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae0f-135">Horas en el control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="6ae0f-135">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

