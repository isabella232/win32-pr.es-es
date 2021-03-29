---
title: Mensaje de MCM_SETDAYSTATE (commctrl. h)
description: Establece los Estados de día para todos los meses que están visibles actualmente dentro de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetDayState.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- MCM_SETDAYSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492850"
---
# <a name="mcm_setdaystate-message"></a><span data-ttu-id="df202-105">Mensaje de MCM \_ SETDAYSTATE</span><span class="sxs-lookup"><span data-stu-id="df202-105">MCM\_SETDAYSTATE message</span></span>

<span data-ttu-id="df202-106">Establece los Estados de día para todos los meses que están visibles actualmente dentro de un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="df202-106">Sets the day states for all months that are currently visible within a month calendar control.</span></span> <span data-ttu-id="df202-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) .</span><span class="sxs-lookup"><span data-stu-id="df202-107">You can send this message explicitly or by using the [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="df202-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df202-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df202-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df202-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df202-110">Valor que indica el número de elementos que hay en la matriz a la que se dirige *lParam* .</span><span class="sxs-lookup"><span data-stu-id="df202-110">Value indicating how many elements are in the array that *lParam* points to.</span></span>

</dd> <dt>

<span data-ttu-id="df202-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df202-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df202-112">Puntero a una matriz de valores [**MONTHDAYSTATE**](monthdaystate.md) que definen cómo se dibujará el control de calendario mensual cada día en su pantalla.</span><span class="sxs-lookup"><span data-stu-id="df202-112">Pointer to an array of [**MONTHDAYSTATE**](monthdaystate.md) values that define how the month calendar control will draw each day in its display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df202-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df202-113">Return value</span></span>

<span data-ttu-id="df202-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="df202-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="df202-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df202-115">Remarks</span></span>

<span data-ttu-id="df202-116">Una aplicación puede establecer explícitamente la información de estado de los días mediante el envío de este mensaje, pero el estado no se conservará cuando se desplace una parte diferente del calendario en la vista.</span><span class="sxs-lookup"><span data-stu-id="df202-116">An application can explicitly set day state information by sending this message, but the state will not persist when a different part of the calendar is scrolled into view.</span></span> <span data-ttu-id="df202-117">Normalmente, la información de estado de los días se establece como respuesta al código de notificación de [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , que se envía cada vez que es necesario actualizar el control.</span><span class="sxs-lookup"><span data-stu-id="df202-117">Day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed.</span></span>

<span data-ttu-id="df202-118">La matriz de *lParam* debe contener tantos elementos como el valor devuelto por la siguiente macro:</span><span class="sxs-lookup"><span data-stu-id="df202-118">The array at *lParam* must contain as many elements as the value returned by the following macro:</span></span>

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

<span data-ttu-id="df202-119">Tenga en cuenta que la matriz de *lParam* debe contener valores [**MONTHDAYSTATE**](monthdaystate.md) que se correspondan con todos los meses que se encuentran actualmente en la pantalla del control, en orden cronológico.</span><span class="sxs-lookup"><span data-stu-id="df202-119">Keep in mind that the array at *lParam* must contain [**MONTHDAYSTATE**](monthdaystate.md) values that correspond with all months currently in the control's display, in chronological order.</span></span> <span data-ttu-id="df202-120">Esto incluye los dos meses que se pueden mostrar parcialmente antes del primer mes y después del último mes.</span><span class="sxs-lookup"><span data-stu-id="df202-120">This includes the two months that may be partially displayed before the first month and after the last month.</span></span>

## <a name="requirements"></a><span data-ttu-id="df202-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df202-121">Requirements</span></span>



| <span data-ttu-id="df202-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="df202-122">Requirement</span></span> | <span data-ttu-id="df202-123">Value</span><span class="sxs-lookup"><span data-stu-id="df202-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df202-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df202-124">Minimum supported client</span></span><br/> | <span data-ttu-id="df202-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="df202-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df202-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df202-126">Minimum supported server</span></span><br/> | <span data-ttu-id="df202-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="df202-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df202-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df202-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="df202-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="df202-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df202-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="df202-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df202-131">Usar controles de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="df202-131">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 





