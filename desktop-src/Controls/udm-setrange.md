---
title: Mensaje de UDM_SETRANGE (commctrl. h)
description: Establece las posiciones mínima y máxima (intervalo) de un control de flechas.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- UDM_SETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079551"
---
# <a name="udm_setrange-message"></a><span data-ttu-id="1b2d9-104">Error de UDM \_ SetRange</span><span class="sxs-lookup"><span data-stu-id="1b2d9-104">UDM\_SETRANGE message</span></span>

<span data-ttu-id="1b2d9-105">Establece las posiciones mínima y máxima (intervalo) de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-105">Sets the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b2d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b2d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b2d9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b2d9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1b2d9-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1b2d9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b2d9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b2d9-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor **breve** que especifica la posición máxima del control de flechas y el valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es un valor **Short** que especifica la posición mínima.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **short** that specifies the maximum position for the up-down control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **short** that specifies the minimum position.</span></span> <span data-ttu-id="1b2d9-111">Ninguna posición puede ser mayor que el valor de MAXVAL de UD \_ o menor que el valor de MINVAL de Ud \_ .</span><span class="sxs-lookup"><span data-stu-id="1b2d9-111">Neither position can be greater than the UD\_MAXVAL value or less than the UD\_MINVAL value.</span></span> <span data-ttu-id="1b2d9-112">Además, la diferencia entre las dos posiciones no puede superar el \_ MAXVAL de Ud.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-112">In addition, the difference between the two positions cannot exceed UD\_MAXVAL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b2d9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b2d9-113">Return value</span></span>

<span data-ttu-id="1b2d9-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b2d9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b2d9-115">Remarks</span></span>

<span data-ttu-id="1b2d9-116">La posición máxima puede ser menor que la posición mínima.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-116">The maximum position can be less than the minimum position.</span></span> <span data-ttu-id="1b2d9-117">Al hacer clic en el botón de flecha arriba, se mueve la posición actual más cerca de la posición máxima y al hacer clic en el botón de flecha abajo se desplaza hacia la posición mínima.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-117">Clicking the up arrow button moves the current position closer to the maximum position, and clicking the down arrow button moves toward the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b2d9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b2d9-118">Requirements</span></span>



| <span data-ttu-id="1b2d9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b2d9-119">Requirement</span></span> | <span data-ttu-id="1b2d9-120">Value</span><span class="sxs-lookup"><span data-stu-id="1b2d9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b2d9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b2d9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1b2d9-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1b2d9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b2d9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b2d9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1b2d9-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b2d9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b2d9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b2d9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b2d9-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b2d9-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b2d9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b2d9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b2d9-128">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="1b2d9-128">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="1b2d9-129">**UDM \_ SetRange**</span><span class="sxs-lookup"><span data-stu-id="1b2d9-129">**UDM\_SETRANGE**</span></span>](udm-setrange.md)
</dt> </dl>

 

