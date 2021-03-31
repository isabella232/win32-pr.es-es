---
title: Mensaje de MCM_GETCURSEL (commctrl. h)
description: Recupera la fecha seleccionada actualmente. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetCurSel.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- MCM_GETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491447"
---
# <a name="mcm_getcursel-message"></a><span data-ttu-id="2e10f-105">Mensaje de MCM \_ GETCURSEL</span><span class="sxs-lookup"><span data-stu-id="2e10f-105">MCM\_GETCURSEL message</span></span>

<span data-ttu-id="2e10f-106">Recupera la fecha seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="2e10f-106">Retrieves the currently selected date.</span></span> <span data-ttu-id="2e10f-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="2e10f-107">You can send this message explicitly or by using the [**MonthCal\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e10f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e10f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e10f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e10f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2e10f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2e10f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2e10f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e10f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e10f-112">Puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá la información de fecha seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="2e10f-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the currently selected date information.</span></span> <span data-ttu-id="2e10f-113">Este parámetro debe ser una dirección válida y no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="2e10f-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e10f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e10f-114">Return value</span></span>

<span data-ttu-id="2e10f-115">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="2e10f-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="2e10f-116">Este mensaje siempre producirá un error cuando se aplique a los controles de calendario mensual establecidos en el estilo [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2e10f-116">This message will always fail when applied to month calendar controls set to the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e10f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e10f-117">Requirements</span></span>



| <span data-ttu-id="2e10f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e10f-118">Requirement</span></span> | <span data-ttu-id="2e10f-119">Value</span><span class="sxs-lookup"><span data-stu-id="2e10f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e10f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e10f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e10f-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2e10f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e10f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e10f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e10f-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e10f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e10f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e10f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e10f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e10f-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e10f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e10f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e10f-127">Horas en el control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="2e10f-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

