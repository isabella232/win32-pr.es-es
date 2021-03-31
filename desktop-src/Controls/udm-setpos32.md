---
title: Mensaje de UDM_SETPOS32 (commctrl. h)
description: Establece la posición de un control de flechas con una precisión de 32 bits.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- UDM_SETPOS32 controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0153305bb535a79dbed59e8d42a7c25157c30cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996715"
---
# <a name="udm_setpos32-message"></a><span data-ttu-id="cbec5-104">\_Mensaje SETPOS32 UDM</span><span class="sxs-lookup"><span data-stu-id="cbec5-104">UDM\_SETPOS32 message</span></span>

<span data-ttu-id="cbec5-105">Establece la posición de un control de flechas con una precisión de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cbec5-105">Sets the position of an up-down control with 32-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="cbec5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbec5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbec5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cbec5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cbec5-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cbec5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cbec5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cbec5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbec5-110">Variable de tipo Integer que especifica la nueva posición del control de flechas.</span><span class="sxs-lookup"><span data-stu-id="cbec5-110">Variable of type integer that specifies the new position for the up-down control.</span></span> <span data-ttu-id="cbec5-111">Si el parámetro está fuera del intervalo especificado del control, *lParam* se establece en el valor válido más próximo.</span><span class="sxs-lookup"><span data-stu-id="cbec5-111">If the parameter is outside the control's specified range, *lParam* is set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbec5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbec5-112">Return value</span></span>

<span data-ttu-id="cbec5-113">Devuelve la posición anterior.</span><span class="sxs-lookup"><span data-stu-id="cbec5-113">Returns the previous position.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbec5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbec5-114">Requirements</span></span>



| <span data-ttu-id="cbec5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbec5-115">Requirement</span></span> | <span data-ttu-id="cbec5-116">Value</span><span class="sxs-lookup"><span data-stu-id="cbec5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cbec5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbec5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cbec5-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cbec5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cbec5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbec5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cbec5-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cbec5-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cbec5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbec5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbec5-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbec5-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbec5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbec5-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="cbec5-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="cbec5-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cbec5-125">**UDM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="cbec5-125">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="cbec5-126">**UDM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="cbec5-126">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="cbec5-127">**UDM \_ GETPOS32**</span><span class="sxs-lookup"><span data-stu-id="cbec5-127">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)
</dt> </dl>

 

 





