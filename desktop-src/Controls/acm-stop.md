---
title: Mensaje de ACM_STOP (commctrl. h)
description: Detiene la reproducción de un clip AVI en un control Animation. Puede enviar este mensaje explícitamente o mediante la macro Animate \_ Stop.
ms.assetid: ba39a579-665e-4d45-8f1f-f190acd76db7
keywords:
- ACM_STOP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- ACM_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81cfc92ac2778ae559fcd9fb8db2b0cd7bb866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150022"
---
# <a name="acm_stop-message"></a><span data-ttu-id="394de-105">Mensaje de detención de ACM \_</span><span class="sxs-lookup"><span data-stu-id="394de-105">ACM\_STOP message</span></span>

<span data-ttu-id="394de-106">Detiene la reproducción de un clip AVI en un control Animation.</span><span class="sxs-lookup"><span data-stu-id="394de-106">Stops playing an AVI clip in an animation control.</span></span> <span data-ttu-id="394de-107">Puede enviar este mensaje explícitamente o mediante la macro [**Animate \_ Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .</span><span class="sxs-lookup"><span data-stu-id="394de-107">You can send this message explicitly or by using the [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="394de-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="394de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="394de-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="394de-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="394de-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="394de-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="394de-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="394de-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="394de-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="394de-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="394de-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="394de-113">Return value</span></span>

<span data-ttu-id="394de-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="394de-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="394de-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="394de-115">Requirements</span></span>



| <span data-ttu-id="394de-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="394de-116">Requirement</span></span> | <span data-ttu-id="394de-117">Value</span><span class="sxs-lookup"><span data-stu-id="394de-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="394de-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="394de-118">Minimum supported client</span></span><br/> | <span data-ttu-id="394de-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="394de-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="394de-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="394de-120">Minimum supported server</span></span><br/> | <span data-ttu-id="394de-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="394de-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="394de-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="394de-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="394de-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="394de-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





