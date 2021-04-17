---
title: Mensaje de MCM_SETCURSEL (commctrl. h)
description: Establece la fecha seleccionada actualmente para un control de calendario mensual. Si la fecha especificada no está en la vista, el control actualiza la pantalla para que aparezca en la vista. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetCurSel.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- MCM_SETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658376"
---
# <a name="mcm_setcursel-message"></a><span data-ttu-id="a45d2-106">Mensaje de MCM \_ SETCURSEL</span><span class="sxs-lookup"><span data-stu-id="a45d2-106">MCM\_SETCURSEL message</span></span>

<span data-ttu-id="a45d2-107">Establece la fecha seleccionada actualmente para un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="a45d2-107">Sets the currently selected date for a month calendar control.</span></span> <span data-ttu-id="a45d2-108">Si la fecha especificada no está en la vista, el control actualiza la pantalla para que aparezca en la vista.</span><span class="sxs-lookup"><span data-stu-id="a45d2-108">If the specified date is not in view, the control updates the display to bring it into view.</span></span> <span data-ttu-id="a45d2-109">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="a45d2-109">You can send this message explicitly or by using the [**MonthCal\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a45d2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a45d2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a45d2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a45d2-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a45d2-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a45d2-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a45d2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a45d2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a45d2-114">Puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contiene la fecha que se va a establecer como la selección actual.</span><span class="sxs-lookup"><span data-stu-id="a45d2-114">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the current selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a45d2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a45d2-115">Return value</span></span>

<span data-ttu-id="a45d2-116">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="a45d2-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="a45d2-117">Se producirá un error en este mensaje si se aplica a un control de calendario mensual que use el estilo [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a45d2-117">This message will fail if applied to a month calendar control that uses the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="a45d2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a45d2-118">Requirements</span></span>



| <span data-ttu-id="a45d2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a45d2-119">Requirement</span></span> | <span data-ttu-id="a45d2-120">Value</span><span class="sxs-lookup"><span data-stu-id="a45d2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a45d2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a45d2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a45d2-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a45d2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a45d2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a45d2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a45d2-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a45d2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a45d2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a45d2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a45d2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a45d2-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a45d2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a45d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a45d2-128">Horas en el control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="a45d2-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

