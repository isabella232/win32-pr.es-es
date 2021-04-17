---
title: Mensaje de TCM_ADJUSTRECT (commctrl. h)
description: Calcula el área de presentación de un control de ficha dado un rectángulo de ventana o calcula el rectángulo de ventana que se correspondería con un área de presentación especificada. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ AdjustRect.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- TCM_ADJUSTRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658359"
---
# <a name="tcm_adjustrect-message"></a><span data-ttu-id="641a1-105">\_Mensaje ADJUSTRECT de TCM</span><span class="sxs-lookup"><span data-stu-id="641a1-105">TCM\_ADJUSTRECT message</span></span>

<span data-ttu-id="641a1-106">Calcula el área de presentación de un control de ficha dado un rectángulo de ventana o calcula el rectángulo de ventana que se correspondería con un área de presentación especificada.</span><span class="sxs-lookup"><span data-stu-id="641a1-106">Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a specified display area.</span></span> <span data-ttu-id="641a1-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) .</span><span class="sxs-lookup"><span data-stu-id="641a1-107">You can send this message explicitly or by using the [**TabCtrl\_AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="641a1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="641a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="641a1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="641a1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="641a1-110">Operación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="641a1-110">Operation to perform.</span></span> <span data-ttu-id="641a1-111">Si este parámetro es **true**, *lParam* especifica un rectángulo de presentación y recibe el rectángulo de ventana correspondiente.</span><span class="sxs-lookup"><span data-stu-id="641a1-111">If this parameter is **TRUE**, *lParam* specifies a display rectangle and receives the corresponding window rectangle.</span></span> <span data-ttu-id="641a1-112">Si este parámetro es **false**, *lParam* especifica un rectángulo de ventana y recibe el área de presentación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="641a1-112">If this parameter is **FALSE**, *lParam* specifies a window rectangle and receives the corresponding display area.</span></span>

</dd> <dt>

<span data-ttu-id="641a1-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="641a1-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="641a1-114">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica el rectángulo dado y recibe el rectángulo calculado.</span><span class="sxs-lookup"><span data-stu-id="641a1-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the given rectangle and receives the calculated rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="641a1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="641a1-115">Return value</span></span>

<span data-ttu-id="641a1-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="641a1-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="641a1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="641a1-117">Remarks</span></span>

<span data-ttu-id="641a1-118">Este mensaje solo se aplica a los controles de ficha que se encuentran en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="641a1-118">This message applies only to tab controls that are at the top.</span></span> <span data-ttu-id="641a1-119">No se aplica a los controles de ficha que se encuentran en los lados o en la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="641a1-119">It does not apply to tab controls that are on the sides or bottom.</span></span>

## <a name="requirements"></a><span data-ttu-id="641a1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="641a1-120">Requirements</span></span>



| <span data-ttu-id="641a1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="641a1-121">Requirement</span></span> | <span data-ttu-id="641a1-122">Value</span><span class="sxs-lookup"><span data-stu-id="641a1-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="641a1-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="641a1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="641a1-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="641a1-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="641a1-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="641a1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="641a1-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="641a1-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="641a1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="641a1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="641a1-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="641a1-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

