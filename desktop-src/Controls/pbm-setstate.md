---
title: Mensaje de PBM_SETSTATE (commctrl. h)
description: Establece el estado de la barra de progreso.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- PBM_SETSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c91e94bcc909957264eff776e56d3580b2c36ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491800"
---
# <a name="pbm_setstate-message"></a><span data-ttu-id="86111-104">Mensaje de PBM \_ SETSTATE</span><span class="sxs-lookup"><span data-stu-id="86111-104">PBM\_SETSTATE message</span></span>

<span data-ttu-id="86111-105">Establece el estado de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="86111-105">Sets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="86111-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86111-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86111-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86111-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86111-108">Estado de la barra de progreso que se está configurando.</span><span class="sxs-lookup"><span data-stu-id="86111-108">State of the progress bar that is being set.</span></span> <span data-ttu-id="86111-109">Uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="86111-109">One of the following values.</span></span>



| <span data-ttu-id="86111-110">Valor</span><span class="sxs-lookup"><span data-stu-id="86111-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="86111-111">Significado</span><span class="sxs-lookup"><span data-stu-id="86111-111">Meaning</span></span>                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="86111-112"><dt>**PBST \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="86111-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="86111-113">En curso.</span><span class="sxs-lookup"><span data-stu-id="86111-113">In progress.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="86111-114"><dt>**\_error PBST**</dt></span><span class="sxs-lookup"><span data-stu-id="86111-114"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="86111-115">Error.</span><span class="sxs-lookup"><span data-stu-id="86111-115">Error.</span></span><br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="86111-116"><dt>**PBST en \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="86111-116"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="86111-117">En pausa.</span><span class="sxs-lookup"><span data-stu-id="86111-117">Paused.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="86111-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86111-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="86111-119">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="86111-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86111-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86111-120">Return value</span></span>

<span data-ttu-id="86111-121">Devuelve el estado anterior.</span><span class="sxs-lookup"><span data-stu-id="86111-121">Returns the previous state.</span></span>

## <a name="requirements"></a><span data-ttu-id="86111-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86111-122">Requirements</span></span>



| <span data-ttu-id="86111-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="86111-123">Requirement</span></span> | <span data-ttu-id="86111-124">Value</span><span class="sxs-lookup"><span data-stu-id="86111-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86111-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86111-125">Minimum supported client</span></span><br/> | <span data-ttu-id="86111-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="86111-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86111-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86111-127">Minimum supported server</span></span><br/> | <span data-ttu-id="86111-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="86111-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86111-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86111-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="86111-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="86111-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





