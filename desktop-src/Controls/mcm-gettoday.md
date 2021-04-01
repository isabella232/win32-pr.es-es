---
title: Mensaje de MCM_GETTODAY (commctrl. h)
description: Recupera la información de fecha de la fecha especificada como \ 0034; hoy \ 0034; para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetToday.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- MCM_GETTODAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996463"
---
# <a name="mcm_gettoday-message"></a><span data-ttu-id="42fe6-105">Mensaje de MCM \_ GETTODAY</span><span class="sxs-lookup"><span data-stu-id="42fe6-105">MCM\_GETTODAY message</span></span>

<span data-ttu-id="42fe6-106">Recupera la información de fecha de la fecha especificada como "hoy" para un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="42fe6-106">Retrieves the date information for the date specified as "today" for a month calendar control.</span></span> <span data-ttu-id="42fe6-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) .</span><span class="sxs-lookup"><span data-stu-id="42fe6-107">You can send this message explicitly or by using the [**MonthCal\_GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="42fe6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42fe6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42fe6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42fe6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="42fe6-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="42fe6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="42fe6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42fe6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42fe6-112">Puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá la información de fecha.</span><span class="sxs-lookup"><span data-stu-id="42fe6-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the date information.</span></span> <span data-ttu-id="42fe6-113">Este parámetro debe ser una dirección válida y no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="42fe6-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42fe6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42fe6-114">Return value</span></span>

<span data-ttu-id="42fe6-115">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="42fe6-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="42fe6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42fe6-116">Requirements</span></span>



| <span data-ttu-id="42fe6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="42fe6-117">Requirement</span></span> | <span data-ttu-id="42fe6-118">Value</span><span class="sxs-lookup"><span data-stu-id="42fe6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42fe6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42fe6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="42fe6-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="42fe6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42fe6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42fe6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="42fe6-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="42fe6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42fe6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42fe6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="42fe6-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42fe6-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42fe6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="42fe6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42fe6-126">Horas en el control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="42fe6-126">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

