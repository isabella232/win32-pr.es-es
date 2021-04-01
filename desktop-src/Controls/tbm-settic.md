---
title: Mensaje de TBM_SETTIC (commctrl. h)
description: Establece una marca de graduación en una barra de aumento en la posición lógica especificada.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- TBM_SETTIC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150064"
---
# <a name="tbm_settic-message"></a><span data-ttu-id="2ecbd-104">TBM \_ SETTIC</span><span class="sxs-lookup"><span data-stu-id="2ecbd-104">TBM\_SETTIC message</span></span>

<span data-ttu-id="2ecbd-105">Establece una marca de graduación en una barra de aumento en la posición lógica especificada.</span><span class="sxs-lookup"><span data-stu-id="2ecbd-105">Sets a tick mark in a trackbar at the specified logical position.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ecbd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ecbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ecbd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ecbd-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2ecbd-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2ecbd-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2ecbd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ecbd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ecbd-110">Posición de la marca de graduación.</span><span class="sxs-lookup"><span data-stu-id="2ecbd-110">Position of the tick mark.</span></span> <span data-ttu-id="2ecbd-111">Este parámetro puede ser cualquiera de los valores enteros en el intervalo de la barra de desplazamiento mínimo y máximo de posiciones de control deslizante.</span><span class="sxs-lookup"><span data-stu-id="2ecbd-111">This parameter can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ecbd-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ecbd-112">Return value</span></span>

<span data-ttu-id="2ecbd-113">Devuelve **true** si la marca de graduación está establecida o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2ecbd-113">Returns **TRUE** if the tick mark is set, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ecbd-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ecbd-114">Remarks</span></span>

<span data-ttu-id="2ecbd-115">Una barra de aumento crea sus propias marcas de graduación primero y último.</span><span class="sxs-lookup"><span data-stu-id="2ecbd-115">A trackbar creates its own first and last tick marks.</span></span> <span data-ttu-id="2ecbd-116">No utilice este mensaje para establecer la primera y la última marca de graduación.</span><span class="sxs-lookup"><span data-stu-id="2ecbd-116">Do not use this message to set the first and last tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ecbd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ecbd-117">Requirements</span></span>



| <span data-ttu-id="2ecbd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ecbd-118">Requirement</span></span> | <span data-ttu-id="2ecbd-119">Value</span><span class="sxs-lookup"><span data-stu-id="2ecbd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ecbd-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ecbd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2ecbd-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2ecbd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ecbd-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ecbd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2ecbd-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ecbd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ecbd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ecbd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ecbd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ecbd-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ecbd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ecbd-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ecbd-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2ecbd-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2ecbd-128">**TBM \_ GETPTICS**</span><span class="sxs-lookup"><span data-stu-id="2ecbd-128">**TBM\_GETPTICS**</span></span>](tbm-getptics.md)
</dt> <dt>

[<span data-ttu-id="2ecbd-129">**TBM \_ GETTIC**</span><span class="sxs-lookup"><span data-stu-id="2ecbd-129">**TBM\_GETTIC**</span></span>](tbm-gettic.md)
</dt> </dl>

 

 





