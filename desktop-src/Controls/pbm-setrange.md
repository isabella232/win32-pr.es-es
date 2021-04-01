---
title: Mensaje de PBM_SETRANGE (commctrl. h)
description: Establece los valores mínimo y máximo de una barra de progreso y vuelve a dibujar la barra para reflejar el nuevo intervalo.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- PBM_SETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905422"
---
# <a name="pbm_setrange-message"></a><span data-ttu-id="88803-104">\_Mensaje de SetRange de PBM</span><span class="sxs-lookup"><span data-stu-id="88803-104">PBM\_SETRANGE message</span></span>

<span data-ttu-id="88803-105">Establece los valores mínimo y máximo de una barra de progreso y vuelve a dibujar la barra para reflejar el nuevo intervalo.</span><span class="sxs-lookup"><span data-stu-id="88803-105">Sets the minimum and maximum values for a progress bar and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="88803-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88803-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88803-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88803-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88803-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="88803-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="88803-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88803-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88803-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el valor de intervalo mínimo y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el valor de intervalo máximo.</span><span class="sxs-lookup"><span data-stu-id="88803-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum range value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum range value.</span></span> <span data-ttu-id="88803-111">El valor de intervalo mínimo no debe ser negativo.</span><span class="sxs-lookup"><span data-stu-id="88803-111">The minimum range value must not be negative.</span></span> <span data-ttu-id="88803-112">De forma predeterminada, el valor mínimo es cero.</span><span class="sxs-lookup"><span data-stu-id="88803-112">By default, the minimum value is zero.</span></span> <span data-ttu-id="88803-113">El valor de intervalo máximo debe ser mayor que el valor de intervalo mínimo.</span><span class="sxs-lookup"><span data-stu-id="88803-113">The maximum range value must be greater than the minimum range value.</span></span> <span data-ttu-id="88803-114">De forma predeterminada, el valor de intervalo máximo es 100.</span><span class="sxs-lookup"><span data-stu-id="88803-114">By default, the maximum range value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88803-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88803-115">Return value</span></span>

<span data-ttu-id="88803-116">Devuelve los valores de intervalo anteriores si se realiza correctamente, o bien cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="88803-116">Returns the previous range values if successful, or zero otherwise.</span></span> <span data-ttu-id="88803-117">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el valor mínimo anterior y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el valor máximo anterior.</span><span class="sxs-lookup"><span data-stu-id="88803-117">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the previous minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the previous maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88803-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88803-118">Remarks</span></span>

<span data-ttu-id="88803-119">Si no establece los valores del intervalo, el sistema establece el valor mínimo en 0 y el valor máximo en 100.</span><span class="sxs-lookup"><span data-stu-id="88803-119">If you do not set the range values, the system sets the minimum value to 0 and the maximum value to 100.</span></span> <span data-ttu-id="88803-120">Dado que este mensaje expresa el intervalo como un entero sin signo de 16 bits, puede extenderse de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="88803-120">Because this message expresses the range as a 16-bit unsigned integer, it can extend from 0 to 65,535.</span></span> <span data-ttu-id="88803-121">El valor mínimo del intervalo puede ser de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="88803-121">The minimum value in the range can be from 0 to 65,535.</span></span> <span data-ttu-id="88803-122">Del mismo modo, el valor máximo puede ser de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="88803-122">Likewise, the maximum value can be from 0 to 65,535.</span></span>

<span data-ttu-id="88803-123">Para establecer un intervalo mayor, llame a [**PBM \_ SETRANGE32**](pbm-setrange32.md).</span><span class="sxs-lookup"><span data-stu-id="88803-123">To set a larger range, call [**PBM\_SETRANGE32**](pbm-setrange32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88803-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88803-124">Requirements</span></span>



| <span data-ttu-id="88803-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="88803-125">Requirement</span></span> | <span data-ttu-id="88803-126">Value</span><span class="sxs-lookup"><span data-stu-id="88803-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88803-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88803-127">Minimum supported client</span></span><br/> | <span data-ttu-id="88803-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="88803-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88803-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88803-129">Minimum supported server</span></span><br/> | <span data-ttu-id="88803-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="88803-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88803-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88803-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="88803-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="88803-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88803-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="88803-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="88803-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="88803-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="88803-135">**GETRANGE de PBM \_**</span><span class="sxs-lookup"><span data-stu-id="88803-135">**PBM\_GETRANGE**</span></span>](pbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="88803-136">**SETRANGE32 de PBM \_**</span><span class="sxs-lookup"><span data-stu-id="88803-136">**PBM\_SETRANGE32**</span></span>](pbm-setrange32.md)
</dt> </dl>

 

