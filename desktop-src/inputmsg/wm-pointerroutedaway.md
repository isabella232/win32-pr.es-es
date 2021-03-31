---
title: Mensaje WM_POINTERROUTEDAWAY
description: Se produce en el proceso que recibe la entrada cuando la entrada del puntero se enruta a otro proceso. AddContentWithCrossProcessChaining).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERROUTEDAWAY
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3c099c02338aa70817d75717064e0b99ac13c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079539"
---
# <a name="wm_pointerroutedaway-message"></a><span data-ttu-id="2c585-104">Mensaje WM_POINTERROUTEDAWAY</span><span class="sxs-lookup"><span data-stu-id="2c585-104">WM_POINTERROUTEDAWAY message</span></span>

<span data-ttu-id="2c585-105">Se produce en el proceso que recibe la entrada cuando la entrada del puntero se enruta a otro proceso.</span><span class="sxs-lookup"><span data-stu-id="2c585-105">Occurs on the process receiving input when the pointer input is routed to another process.</span></span>

<span data-ttu-id="2c585-106">Se envía cuando la entrada de puntero pasa de un proceso a otro en el contenido configurado para el encadenamiento entre procesos ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span><span class="sxs-lookup"><span data-stu-id="2c585-106">Sent when pointer input transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="2c585-107">Este mensaje se envía al proceso que recibe actualmente la entrada de puntero.</span><span class="sxs-lookup"><span data-stu-id="2c585-107">This message is sent to the process currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDAWAY       0x0252
```



## <a name="parameters"></a><span data-ttu-id="2c585-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c585-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c585-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c585-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c585-110">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="2c585-110">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="2c585-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c585-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c585-112">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="2c585-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c585-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c585-113">Return value</span></span>

<span data-ttu-id="2c585-114">NULL</span><span class="sxs-lookup"><span data-stu-id="2c585-114">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="2c585-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c585-115">Remarks</span></span>

<span data-ttu-id="2c585-116">Este mensaje no se envía con un mensaje [**WM_POINTERUP**](wm-pointerup.md) o un mensaje [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="2c585-116">This message is not sent with either a [**WM_POINTERUP**](wm-pointerup.md) message or a [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c585-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c585-117">Requirements</span></span>



| <span data-ttu-id="2c585-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c585-118">Requirement</span></span> | <span data-ttu-id="2c585-119">Value</span><span class="sxs-lookup"><span data-stu-id="2c585-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c585-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c585-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c585-121">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c585-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2c585-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c585-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c585-123">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c585-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c585-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c585-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c585-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c585-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c585-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c585-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c585-127">Mensajes</span><span class="sxs-lookup"><span data-stu-id="2c585-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="2c585-128">**WM_POINTERROUTEDTO**</span><span class="sxs-lookup"><span data-stu-id="2c585-128">**WM_POINTERROUTEDTO**</span></span>](wm-pointerroutedto.md)
</dt> </dl>

 

