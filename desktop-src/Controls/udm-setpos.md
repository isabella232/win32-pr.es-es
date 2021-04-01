---
title: Mensaje de UDM_SETPOS (commctrl. h)
description: Establece la posición actual de un control de flechas con una precisión de 16 bits.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- UDM_SETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150646"
---
# <a name="udm_setpos-message"></a><span data-ttu-id="353a1-104">\_Mensaje SETPOS UDM</span><span class="sxs-lookup"><span data-stu-id="353a1-104">UDM\_SETPOS message</span></span>

<span data-ttu-id="353a1-105">Establece la posición actual de un control de flechas con una precisión de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="353a1-105">Sets the current position for an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="353a1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="353a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="353a1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="353a1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="353a1-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="353a1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="353a1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="353a1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="353a1-110">Nueva posición del control de flechas.</span><span class="sxs-lookup"><span data-stu-id="353a1-110">New position for the up-down control.</span></span> <span data-ttu-id="353a1-111">Si el parámetro está fuera del intervalo especificado del control, *lParam* se establecerá en el valor válido más próximo.</span><span class="sxs-lookup"><span data-stu-id="353a1-111">If the parameter is outside the control's specified range, *lParam* will be set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="353a1-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="353a1-112">Return value</span></span>

<span data-ttu-id="353a1-113">El valor devuelto es la posición anterior.</span><span class="sxs-lookup"><span data-stu-id="353a1-113">The return value is the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="353a1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="353a1-114">Remarks</span></span>

<span data-ttu-id="353a1-115">Este mensaje solo admite posiciones de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="353a1-115">This message only supports 16-bit positions.</span></span> <span data-ttu-id="353a1-116">Si se han habilitado valores de 32 bits para un control de flechas con [**UDM \_ SETRANGE32**](udm-setrange32.md), use [**UDM \_ SETPOS32**](udm-setpos32.md).</span><span class="sxs-lookup"><span data-stu-id="353a1-116">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), use [**UDM\_SETPOS32**](udm-setpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="353a1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="353a1-117">Requirements</span></span>



| <span data-ttu-id="353a1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="353a1-118">Requirement</span></span> | <span data-ttu-id="353a1-119">Value</span><span class="sxs-lookup"><span data-stu-id="353a1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="353a1-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="353a1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="353a1-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="353a1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="353a1-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="353a1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="353a1-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="353a1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="353a1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="353a1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="353a1-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="353a1-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="353a1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="353a1-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="353a1-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="353a1-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="353a1-128">**UDM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="353a1-128">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="353a1-129">**UDM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="353a1-129">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> </dl>

 

 





