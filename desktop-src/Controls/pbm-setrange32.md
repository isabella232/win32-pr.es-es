---
title: Mensaje de PBM_SETRANGE32 (commctrl. h)
description: Establece los valores mínimo y máximo de una barra de progreso en valores de 32 bits y vuelve a dibujar la barra para reflejar el nuevo intervalo.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- PBM_SETRANGE32 controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803049"
---
# <a name="pbm_setrange32-message"></a><span data-ttu-id="af2db-104">Mensaje de SETRANGE32 de PBM \_</span><span class="sxs-lookup"><span data-stu-id="af2db-104">PBM\_SETRANGE32 message</span></span>

<span data-ttu-id="af2db-105">Establece los valores mínimo y máximo de una barra de progreso en valores de 32 bits y vuelve a dibujar la barra para reflejar el nuevo intervalo.</span><span class="sxs-lookup"><span data-stu-id="af2db-105">Sets the minimum and maximum values for a progress bar to 32-bit values, and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="af2db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af2db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af2db-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af2db-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af2db-108">Valor de intervalo mínimo.</span><span class="sxs-lookup"><span data-stu-id="af2db-108">Minimum range value.</span></span> <span data-ttu-id="af2db-109">De forma predeterminada, el valor mínimo es cero.</span><span class="sxs-lookup"><span data-stu-id="af2db-109">By default, the minimum value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="af2db-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af2db-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af2db-111">Valor de intervalo máximo.</span><span class="sxs-lookup"><span data-stu-id="af2db-111">Maximum range value.</span></span> <span data-ttu-id="af2db-112">Este valor debe ser mayor que *wParam*.</span><span class="sxs-lookup"><span data-stu-id="af2db-112">This value must be greater than *wParam*.</span></span> <span data-ttu-id="af2db-113">De forma predeterminada, el valor máximo es 100.</span><span class="sxs-lookup"><span data-stu-id="af2db-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af2db-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af2db-114">Return value</span></span>

<span data-ttu-id="af2db-115">Devuelve un valor **DWORD** que contiene el límite inferior de 16 bits anterior en su [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y el límite superior de 16 bits anterior en su [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="af2db-115">Returns a **DWORD** value that holds the previous 16-bit low limit in its [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous 16-bit high limit in its [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="af2db-116">Si los intervalos anteriores eran valores de 32 bits, el valor devuelto consta de los **LOWORD** s de ambos límites de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="af2db-116">If the previous ranges were 32-bit values, the return value consists of the **LOWORD** s of both 32-bit limits.</span></span>

## <a name="remarks"></a><span data-ttu-id="af2db-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af2db-117">Remarks</span></span>

<span data-ttu-id="af2db-118">Para recuperar los valores de 32 bits altos y bajos completos, use el [**mensaje \_ GETRANGE de PBM**](pbm-getrange.md) .</span><span class="sxs-lookup"><span data-stu-id="af2db-118">To retrieve the entire high and low 32-bit values, use the [**PBM\_GETRANGE**](pbm-getrange.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="af2db-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af2db-119">Requirements</span></span>



| <span data-ttu-id="af2db-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="af2db-120">Requirement</span></span> | <span data-ttu-id="af2db-121">Value</span><span class="sxs-lookup"><span data-stu-id="af2db-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af2db-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af2db-122">Minimum supported client</span></span><br/> | <span data-ttu-id="af2db-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="af2db-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af2db-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af2db-124">Minimum supported server</span></span><br/> | <span data-ttu-id="af2db-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="af2db-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af2db-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af2db-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="af2db-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="af2db-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

