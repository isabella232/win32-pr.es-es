---
title: Mensaje de PBM_GETSTATE (commctrl. h)
description: Obtiene el estado de la barra de progreso.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- PBM_GETSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996737"
---
# <a name="pbm_getstate-message"></a><span data-ttu-id="5cc8a-104">Mensaje de GETSTATE de PBM \_</span><span class="sxs-lookup"><span data-stu-id="5cc8a-104">PBM\_GETSTATE message</span></span>

<span data-ttu-id="5cc8a-105">Obtiene el estado de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="5cc8a-105">Gets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5cc8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5cc8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cc8a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5cc8a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5cc8a-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5cc8a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5cc8a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5cc8a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5cc8a-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5cc8a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cc8a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5cc8a-111">Return value</span></span>

<span data-ttu-id="5cc8a-112">Devuelve el estado actual de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="5cc8a-112">Returns the current state of the progress bar.</span></span> <span data-ttu-id="5cc8a-113">Uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="5cc8a-113">One of the following values.</span></span>



| <span data-ttu-id="5cc8a-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5cc8a-114">Return code</span></span>                                                                                 | <span data-ttu-id="5cc8a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cc8a-115">Description</span></span>             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="5cc8a-116"><dt>**PBST \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="5cc8a-116"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="5cc8a-117">En curso.</span><span class="sxs-lookup"><span data-stu-id="5cc8a-117">In progress.</span></span><br/> |
| <dl> <span data-ttu-id="5cc8a-118"><dt>**\_error PBST**</dt></span><span class="sxs-lookup"><span data-stu-id="5cc8a-118"><dt>**PBST\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="5cc8a-119">Error.</span><span class="sxs-lookup"><span data-stu-id="5cc8a-119">Error.</span></span><br/>       |
| <dl> <span data-ttu-id="5cc8a-120"><dt>**PBST en \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="5cc8a-120"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="5cc8a-121">En pausa.</span><span class="sxs-lookup"><span data-stu-id="5cc8a-121">Paused.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="5cc8a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cc8a-122">Requirements</span></span>



| <span data-ttu-id="5cc8a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cc8a-123">Requirement</span></span> | <span data-ttu-id="5cc8a-124">Value</span><span class="sxs-lookup"><span data-stu-id="5cc8a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cc8a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cc8a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5cc8a-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5cc8a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5cc8a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cc8a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5cc8a-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5cc8a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cc8a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cc8a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cc8a-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cc8a-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





