---
title: Mensaje de ACM_PLAY (commctrl. h)
description: Reproduce un clip AVI en un control Animation. El control reproduce el clip en segundo plano mientras se sigue ejecutando el subproceso. Puede enviar este mensaje explícitamente o mediante el uso de la macro Animate \_ Play.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- ACM_PLAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489652"
---
# <a name="acm_play-message"></a><span data-ttu-id="490fc-106">Mensaje de reproducción de ACM \_</span><span class="sxs-lookup"><span data-stu-id="490fc-106">ACM\_PLAY message</span></span>

<span data-ttu-id="490fc-107">Reproduce un clip AVI en un control Animation.</span><span class="sxs-lookup"><span data-stu-id="490fc-107">Plays an AVI clip in an animation control.</span></span> <span data-ttu-id="490fc-108">El control reproduce el clip en segundo plano mientras se sigue ejecutando el subproceso.</span><span class="sxs-lookup"><span data-stu-id="490fc-108">The control plays the clip in the background while the thread continues executing.</span></span> <span data-ttu-id="490fc-109">Puede enviar este mensaje explícitamente o mediante el uso de la macro [**Animate \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .</span><span class="sxs-lookup"><span data-stu-id="490fc-109">You can send this message explicitly or by using the [**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="490fc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="490fc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="490fc-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="490fc-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="490fc-112">Un valor **uint** que especifica el número de veces que se va a reproducir el clip AVI.</span><span class="sxs-lookup"><span data-stu-id="490fc-112">A **UINT** that specifies the number of times to replay the AVI clip.</span></span> <span data-ttu-id="490fc-113">Un valor de-1 significa que se reproduce el clip indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="490fc-113">A value of -1 means replay the clip indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="490fc-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="490fc-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="490fc-115">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es el índice de base cero del marco en el que comienza la reproducción.</span><span class="sxs-lookup"><span data-stu-id="490fc-115">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the zero-based index of the frame where playing begins.</span></span> <span data-ttu-id="490fc-116">El valor debe ser menor que 65.536.</span><span class="sxs-lookup"><span data-stu-id="490fc-116">The value must be less than 65,536.</span></span> <span data-ttu-id="490fc-117">Un valor de cero significa que comienza con el primer fotograma del clip AVI.</span><span class="sxs-lookup"><span data-stu-id="490fc-117">A value of zero means begin with the first frame in the AVI clip.</span></span>

<span data-ttu-id="490fc-118">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es el índice de base cero del marco en el que finaliza la reproducción.</span><span class="sxs-lookup"><span data-stu-id="490fc-118">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the zero-based index of the frame where playing ends.</span></span> <span data-ttu-id="490fc-119">El valor debe ser menor que 65.536.</span><span class="sxs-lookup"><span data-stu-id="490fc-119">The value must be less than 65,536.</span></span> <span data-ttu-id="490fc-120">Un valor de-1 significa terminar con el último fotograma del clip AVI.</span><span class="sxs-lookup"><span data-stu-id="490fc-120">A value of -1 means end with the last frame in the AVI clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="490fc-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="490fc-121">Return value</span></span>

<span data-ttu-id="490fc-122">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="490fc-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="490fc-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="490fc-123">Remarks</span></span>

<span data-ttu-id="490fc-124">Puede usar [**Animate \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) para dirigir el control de animación y mostrar un fotograma determinado del clip AVI.</span><span class="sxs-lookup"><span data-stu-id="490fc-124">You can use [**Animate\_Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) to direct the animation control to display a particular frame of the AVI clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="490fc-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="490fc-125">Requirements</span></span>



| <span data-ttu-id="490fc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="490fc-126">Requirement</span></span> | <span data-ttu-id="490fc-127">Value</span><span class="sxs-lookup"><span data-stu-id="490fc-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="490fc-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="490fc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="490fc-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="490fc-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="490fc-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="490fc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="490fc-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="490fc-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="490fc-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="490fc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="490fc-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="490fc-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

