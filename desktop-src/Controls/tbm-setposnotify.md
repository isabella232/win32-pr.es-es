---
title: Mensaje de TBM_SETPOSNOTIFY (commctrl. h)
description: Establece la posición lógica actual del control deslizante en una barra de desplazamiento.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636a2add9f13470a89b312450f1a3dcbc185be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489803"
---
# <a name="tbm_setposnotify-message"></a><span data-ttu-id="91d98-104">TBM \_ SETPOSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="91d98-104">TBM\_SETPOSNOTIFY message</span></span>

<span data-ttu-id="91d98-105">Establece la posición lógica actual del control deslizante en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="91d98-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="91d98-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91d98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91d98-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91d98-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91d98-108">wParam no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="91d98-108">wParam is unused.</span></span>

</dd> <dt>

<span data-ttu-id="91d98-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91d98-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91d98-110">Nueva posición lógica del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="91d98-110">New logical position of the slider.</span></span> <span data-ttu-id="91d98-111">Las posiciones lógicas válidas son los valores enteros en el intervalo de la barra de desplazamiento mínimo al máximo.</span><span class="sxs-lookup"><span data-stu-id="91d98-111">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="91d98-112">Si este valor está fuera del intervalo máximo y mínimo del control, la posición se establece en el valor máximo o mínimo.</span><span class="sxs-lookup"><span data-stu-id="91d98-112">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91d98-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91d98-113">Return value</span></span>

<span data-ttu-id="91d98-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="91d98-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91d98-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91d98-115">Remarks</span></span>

<span data-ttu-id="91d98-116">Si se llama a **TBM \_ SETPOSNOTIFY** , se establecerá la ubicación del control deslizante de TrackBar como [**TBM \_ SETPOS**](tbm-setpos.md) , pero también hará que la barra de desplazamiento notifique a su elemento primario de un movimiento a través de un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="91d98-116">Calling **TBM\_SETPOSNOTIFY** will set the trackbar slider location like [**TBM\_SETPOS**](tbm-setpos.md) would, but it will also cause the trackbar to notify its parent of a move via a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="91d98-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91d98-117">Requirements</span></span>



| <span data-ttu-id="91d98-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="91d98-118">Requirement</span></span> | <span data-ttu-id="91d98-119">Value</span><span class="sxs-lookup"><span data-stu-id="91d98-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91d98-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91d98-120">Minimum supported client</span></span><br/> | <span data-ttu-id="91d98-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="91d98-121">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="91d98-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91d98-122">Minimum supported server</span></span><br/> | <span data-ttu-id="91d98-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="91d98-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="91d98-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91d98-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="91d98-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91d98-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





