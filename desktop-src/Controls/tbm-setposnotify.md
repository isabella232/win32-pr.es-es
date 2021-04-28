---
title: TBM_SETPOSNOTIFY mensaje (Commctrl.h)
description: 'TBM_SETPOSNOTIFY mensaje: establece la posición lógica actual del control deslizante en una barra de seguimiento.'
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY de mensajes controles de Windows
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
ms.openlocfilehash: 7201f3056ed05e6321ab9d9bd726edc3b4470f0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104083"
---
# <a name="tbm_setposnotify-message"></a><span data-ttu-id="b0f68-104">Mensaje \_ TBM SETPOSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="b0f68-104">TBM\_SETPOSNOTIFY message</span></span>

<span data-ttu-id="b0f68-105">Establece la posición lógica actual del control deslizante en una barra de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="b0f68-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0f68-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0f68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f68-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0f68-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f68-108">wParam no se usa.</span><span class="sxs-lookup"><span data-stu-id="b0f68-108">wParam is unused.</span></span>

</dd> <dt>

<span data-ttu-id="b0f68-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0f68-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f68-110">Nueva posición lógica del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="b0f68-110">New logical position of the slider.</span></span> <span data-ttu-id="b0f68-111">Las posiciones lógicas válidas son los valores enteros del intervalo de posiciones del control deslizante mínimo al máximo de la barra de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="b0f68-111">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="b0f68-112">Si este valor está fuera del intervalo máximo y mínimo del control, la posición se establece en el valor máximo o mínimo.</span><span class="sxs-lookup"><span data-stu-id="b0f68-112">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0f68-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0f68-113">Return value</span></span>

<span data-ttu-id="b0f68-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b0f68-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0f68-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0f68-115">Remarks</span></span>

<span data-ttu-id="b0f68-116">Al llamar a **TBM \_ SETPOSNOTIFY,** se establecerá la ubicación del control deslizante de la barra de seguimiento como lo haría [**TBM \_ SETPOS,**](tbm-setpos.md) pero también hará que la barra de seguimiento notifique a su elemento primario de un movimiento a través de un mensaje WM [**\_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL.**](wm-vscroll.md)</span><span class="sxs-lookup"><span data-stu-id="b0f68-116">Calling **TBM\_SETPOSNOTIFY** will set the trackbar slider location like [**TBM\_SETPOS**](tbm-setpos.md) would, but it will also cause the trackbar to notify its parent of a move via a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f68-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0f68-117">Requirements</span></span>



| <span data-ttu-id="b0f68-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0f68-118">Requirement</span></span> | <span data-ttu-id="b0f68-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b0f68-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f68-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0f68-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b0f68-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0f68-121">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b0f68-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0f68-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b0f68-123">Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="b0f68-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b0f68-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0f68-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0f68-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="b0f68-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





