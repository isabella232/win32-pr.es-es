---
title: Mensaje de MCM_SETFIRSTDAYOFWEEK (commctrl. h)
description: Establece el primer día de la semana para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetFirstDayOfWeek.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- MCM_SETFIRSTDAYOFWEEK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32452c9043bbd7c3bbcf96f9dc32e67714eacce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658374"
---
# <a name="mcm_setfirstdayofweek-message"></a><span data-ttu-id="6d8ad-105">Mensaje de MCM \_ SETFIRSTDAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="6d8ad-105">MCM\_SETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="6d8ad-106">Establece el primer día de la semana para un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="6d8ad-106">Sets the first day of the week for a month calendar control.</span></span> <span data-ttu-id="6d8ad-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) .</span><span class="sxs-lookup"><span data-stu-id="6d8ad-107">You can send this message explicitly or by using the [**MonthCal\_SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d8ad-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d8ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d8ad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d8ad-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6d8ad-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6d8ad-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6d8ad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d8ad-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d8ad-112">Valor de tipo **int** que representa el día que se va a establecer como primer día de la semana, donde 0 es el lunes, 1 es el martes, etc.</span><span class="sxs-lookup"><span data-stu-id="6d8ad-112">Value of type **int** representing which day is to be set as the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d8ad-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d8ad-113">Return value</span></span>

<span data-ttu-id="6d8ad-114">Devuelve un valor **DWORD** que contiene dos valores.</span><span class="sxs-lookup"><span data-stu-id="6d8ad-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="6d8ad-115">La palabra alta es un valor **booleano** que es distinto de cero si el primer día de la semana anterior no era igual a la configuración regional \_ IFIRSTDAYOFWEEK, o bien, cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6d8ad-115">The high word is a **BOOL** value that is nonzero if the previous first day of the week did not equal LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="6d8ad-116">La palabra baja es un valor INT que representa el primer día de la semana anterior.</span><span class="sxs-lookup"><span data-stu-id="6d8ad-116">The low word is an INT value that represents the previous first day of the week.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d8ad-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d8ad-117">Remarks</span></span>

<span data-ttu-id="6d8ad-118">Si el primer día de la semana se establece en un valor distinto del predeterminado (configuración regional \_ IFIRSTDAYOFWEEK), el control no actualizará automáticamente los cambios del primer día de la semana en función de los cambios de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="6d8ad-118">If the first day of the week is set to anything other than the default (LOCALE\_IFIRSTDAYOFWEEK), the control will not automatically update first-day-of-the-week changes based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d8ad-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d8ad-119">Requirements</span></span>



| <span data-ttu-id="6d8ad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d8ad-120">Requirement</span></span> | <span data-ttu-id="6d8ad-121">Value</span><span class="sxs-lookup"><span data-stu-id="6d8ad-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d8ad-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d8ad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6d8ad-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6d8ad-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d8ad-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d8ad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6d8ad-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d8ad-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d8ad-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d8ad-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d8ad-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d8ad-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





