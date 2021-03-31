---
title: Mensaje de DTM_GETMONTHCAL (commctrl. h)
description: Obtiene el identificador del control de calendario mensual de un selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la macro GetMonthCal de fecha y hora \_ .
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- DTM_GETMONTHCAL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996755"
---
# <a name="dtm_getmonthcal-message"></a><span data-ttu-id="ef0ae-105">DTM \_ GETMONTHCAL</span><span class="sxs-lookup"><span data-stu-id="ef0ae-105">DTM\_GETMONTHCAL message</span></span>

<span data-ttu-id="ef0ae-106">Obtiene el identificador del control de calendario mensual de un selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="ef0ae-106">Gets the handle to a date and time picker's (DTP) child month calendar control.</span></span> <span data-ttu-id="ef0ae-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetMonthCal de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) .</span><span class="sxs-lookup"><span data-stu-id="ef0ae-107">You can send this message explicitly or use the [**DateTime\_GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef0ae-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef0ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef0ae-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef0ae-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ef0ae-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ef0ae-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef0ae-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ef0ae-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef0ae-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef0ae-113">Return value</span></span>

<span data-ttu-id="ef0ae-114">Devuelve el identificador del control de calendario mensual del control de DTP si se realiza correctamente, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-114">Returns the handle to a DTP control's child month calendar control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef0ae-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef0ae-115">Remarks</span></span>

<span data-ttu-id="ef0ae-116">Los controles de DTP crean un control de calendario mensual secundario cuando el usuario hace clic en la flecha desplegable (notificación de desplegable[DTN \_ ](dtn-dropdown.md) ).</span><span class="sxs-lookup"><span data-stu-id="ef0ae-116">DTP controls create a child month calendar control when the user clicks the drop-down arrow ([DTN\_DROPDOWN](dtn-dropdown.md) notification).</span></span> <span data-ttu-id="ef0ae-117">Cuando el calendario mensual ya no es necesario, se destruye (se envía una notificación [DTN \_ primer plano](dtn-closeup.md) en la destrucción).</span><span class="sxs-lookup"><span data-stu-id="ef0ae-117">When the month calendar is no longer needed, it is destroyed (a [DTN\_CLOSEUP](dtn-closeup.md) notification is sent on destruction).</span></span> <span data-ttu-id="ef0ae-118">Por lo tanto, la aplicación no debe basarse en un identificador estático para el calendario mensual del control de DTP.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-118">So your application must not rely on a static handle to the DTP control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef0ae-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef0ae-119">Requirements</span></span>



| <span data-ttu-id="ef0ae-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef0ae-120">Requirement</span></span> | <span data-ttu-id="ef0ae-121">Value</span><span class="sxs-lookup"><span data-stu-id="ef0ae-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0ae-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef0ae-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0ae-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ef0ae-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef0ae-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef0ae-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0ae-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef0ae-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef0ae-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef0ae-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef0ae-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef0ae-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef0ae-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef0ae-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef0ae-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ef0ae-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ef0ae-130">DTN \_ primer plano</span><span class="sxs-lookup"><span data-stu-id="ef0ae-130">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="ef0ae-131">\_lista desplegable DTN</span><span class="sxs-lookup"><span data-stu-id="ef0ae-131">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> </dl>

 

 





