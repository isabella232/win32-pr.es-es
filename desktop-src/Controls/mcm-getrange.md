---
title: Mensaje de MCM_GETRANGE (commctrl. h)
description: Recupera las fechas mínimas y máximas permitidas establecidas para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetRange.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- MCM_GETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905601"
---
# <a name="mcm_getrange-message"></a><span data-ttu-id="4364f-105">Mensaje de MCM \_ GETRANGE</span><span class="sxs-lookup"><span data-stu-id="4364f-105">MCM\_GETRANGE message</span></span>

<span data-ttu-id="4364f-106">Recupera las fechas mínimas y máximas permitidas establecidas para un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="4364f-106">Retrieves the minimum and maximum allowable dates set for a month calendar control.</span></span> <span data-ttu-id="4364f-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) .</span><span class="sxs-lookup"><span data-stu-id="4364f-107">You can send this message explicitly or by using the [**MonthCal\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4364f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4364f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4364f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4364f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4364f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4364f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4364f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4364f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4364f-112">Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá la información de límite de fecha.</span><span class="sxs-lookup"><span data-stu-id="4364f-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the date limit information.</span></span> <span data-ttu-id="4364f-113">El límite mínimo se establece en *lprgSysTimeArray* \[ 0 \] y *lprgSysTimeArray* \[ 1 \] recibe el límite máximo.</span><span class="sxs-lookup"><span data-stu-id="4364f-113">The minimum limit is set in *lprgSysTimeArray*\[0\], and *lprgSysTimeArray*\[1\] receives the maximum limit.</span></span> <span data-ttu-id="4364f-114">Si alguno de los elementos se establece en ceros, no se establece ningún límite correspondiente para el control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="4364f-114">If either element is set to all zeros, then no corresponding limit is set for the month calendar control.</span></span> <span data-ttu-id="4364f-115">Este parámetro debe ser una dirección válida y no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="4364f-115">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4364f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4364f-116">Return value</span></span>

<span data-ttu-id="4364f-117">Devuelve un **valor DWORD** que puede ser cero (no se establece ningún límite) o una combinación de los siguientes valores que especifican la información de límite:</span><span class="sxs-lookup"><span data-stu-id="4364f-117">Returns a **DWORD** that can be zero (no limits are set) or a combination of the following values that specify limit information:</span></span>



| <span data-ttu-id="4364f-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4364f-118">Return code</span></span>                                                                              | <span data-ttu-id="4364f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4364f-119">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4364f-120"><dt>**GDTR \_ máx.**</dt></span><span class="sxs-lookup"><span data-stu-id="4364f-120"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="4364f-121">Se establece un límite máximo para el control; *lprgSysTimeArray* \[ 0 \] es válido y contiene la información de fecha aplicable.</span><span class="sxs-lookup"><span data-stu-id="4364f-121">A maximum limit is set for the control; *lprgSysTimeArray*\[0\] is valid and contains the applicable date information.</span></span> <br/> |
| <dl> <span data-ttu-id="4364f-122"><dt>**GDTR \_ mín.**</dt></span><span class="sxs-lookup"><span data-stu-id="4364f-122"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="4364f-123">Se establece un límite mínimo para el control. *lprgSysTimeArray* \[ 1 \] es válido y contiene la información de fecha aplicable.</span><span class="sxs-lookup"><span data-stu-id="4364f-123">A minimum limit is set for the control; *lprgSysTimeArray*\[1\] is valid and contains the applicable date information.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="4364f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4364f-124">Requirements</span></span>



| <span data-ttu-id="4364f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4364f-125">Requirement</span></span> | <span data-ttu-id="4364f-126">Value</span><span class="sxs-lookup"><span data-stu-id="4364f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4364f-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4364f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4364f-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4364f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4364f-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4364f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4364f-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4364f-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4364f-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4364f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4364f-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4364f-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4364f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4364f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4364f-134">Horas en el control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="4364f-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

