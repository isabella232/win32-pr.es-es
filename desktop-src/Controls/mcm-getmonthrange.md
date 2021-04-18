---
title: Mensaje de MCM_GETMONTHRANGE (commctrl. h)
description: Recupera información de fecha (mediante estructuras SYSTEMTIME) que representa los límites máximo y mínimo de la presentación de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetMonthRange.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- MCM_GETMONTHRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022ca7e05cc0c69cd32f6ad92531420cdaed7c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658414"
---
# <a name="mcm_getmonthrange-message"></a><span data-ttu-id="a3111-105">Mensaje de MCM \_ GETMONTHRANGE</span><span class="sxs-lookup"><span data-stu-id="a3111-105">MCM\_GETMONTHRANGE message</span></span>

<span data-ttu-id="a3111-106">Recupera información de fecha (mediante estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) ) que representa los límites máximo y mínimo de la presentación de un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="a3111-106">Retrieves date information (using [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures) that represents the high and low limits of a month calendar control's display.</span></span> <span data-ttu-id="a3111-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) .</span><span class="sxs-lookup"><span data-stu-id="a3111-107">You can send this message explicitly or by using the [**MonthCal\_GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3111-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3111-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3111-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3111-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3111-110">Valor que especifica el ámbito de los límites de intervalo que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="a3111-110">Value specifying the scope of the range limits to be retrieved.</span></span> <span data-ttu-id="a3111-111">Este valor debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3111-111">This value must be one of the following:</span></span>



| <span data-ttu-id="a3111-112">Value</span><span class="sxs-lookup"><span data-stu-id="a3111-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="a3111-113">Significado</span><span class="sxs-lookup"><span data-stu-id="a3111-113">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <span data-ttu-id="a3111-114"><dt>**GMR \_ DAYSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="a3111-114"><dt>**GMR\_DAYSTATE**</dt></span></span> </dl> | <span data-ttu-id="a3111-115">Incluye los meses anteriores y finales del intervalo visible que solo se muestran parcialmente.</span><span class="sxs-lookup"><span data-stu-id="a3111-115">Include preceding and trailing months of visible range that are only partially displayed.</span></span> <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <span data-ttu-id="a3111-116"><dt>**GMR \_ visible**</dt></span><span class="sxs-lookup"><span data-stu-id="a3111-116"><dt>**GMR\_VISIBLE**</dt></span></span> </dl>    | <span data-ttu-id="a3111-117">Incluye solo los meses que se muestran por completo.</span><span class="sxs-lookup"><span data-stu-id="a3111-117">Include only those months that are entirely displayed.</span></span> <br/>                                    |



 

</dd> <dt>

<span data-ttu-id="a3111-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3111-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3111-119">Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá los límites inferior y superior del ámbito especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="a3111-119">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the scope specified by *wParam*.</span></span> <span data-ttu-id="a3111-120">Los límites inferior y superior se colocan en *lprgSysTimeArray* \[ 0 \] y *lprgSysTimeArray* \[ 1 \] , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a3111-120">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="a3111-121">Este parámetro debe ser una dirección válida y no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a3111-121">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3111-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3111-122">Return value</span></span>

<span data-ttu-id="a3111-123">Devuelve un valor INT que representa el intervalo, en meses, que abarcan los dos límites devueltos en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="a3111-123">Returns an INT value that represents the range, in months, spanned by the two limits returned at *lParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3111-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3111-124">Requirements</span></span>



| <span data-ttu-id="a3111-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3111-125">Requirement</span></span> | <span data-ttu-id="a3111-126">Value</span><span class="sxs-lookup"><span data-stu-id="a3111-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3111-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3111-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a3111-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a3111-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3111-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3111-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a3111-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a3111-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3111-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3111-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3111-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3111-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3111-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3111-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3111-134">Horas en el control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="a3111-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

