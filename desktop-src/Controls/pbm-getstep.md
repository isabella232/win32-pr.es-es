---
title: Mensaje de PBM_GETSTEP (commctrl. h)
description: Recupera el incremento de paso de una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un mensaje de STEPIT de PBM \_ . De forma predeterminada, el incremento de paso se establece en 10.
ms.assetid: 0cf3052a-cf86-4c0e-ad59-ddab7c6e3602
keywords:
- PBM_GETSTEP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_GETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dcc4adb18d2b60d2936c2cdc7ab79d00389b3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996736"
---
# <a name="pbm_getstep-message"></a><span data-ttu-id="9dd5e-106">Mensaje de GETSTEP de PBM \_</span><span class="sxs-lookup"><span data-stu-id="9dd5e-106">PBM\_GETSTEP message</span></span>

<span data-ttu-id="9dd5e-107">Recupera el incremento de paso de una barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="9dd5e-107">Retrieves the step increment from a progress bar.</span></span> <span data-ttu-id="9dd5e-108">El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un mensaje de [**\_ STEPIT de PBM**](pbm-stepit.md) .</span><span class="sxs-lookup"><span data-stu-id="9dd5e-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="9dd5e-109">De forma predeterminada, el incremento de paso se establece en 10.</span><span class="sxs-lookup"><span data-stu-id="9dd5e-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="9dd5e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9dd5e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd5e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9dd5e-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9dd5e-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9dd5e-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9dd5e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9dd5e-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9dd5e-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9dd5e-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dd5e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9dd5e-115">Return value</span></span>

<span data-ttu-id="9dd5e-116">Devuelve el incremento de paso actual.</span><span class="sxs-lookup"><span data-stu-id="9dd5e-116">Returns the current step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd5e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dd5e-117">Requirements</span></span>



| <span data-ttu-id="9dd5e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dd5e-118">Requirement</span></span> | <span data-ttu-id="9dd5e-119">Value</span><span class="sxs-lookup"><span data-stu-id="9dd5e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd5e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dd5e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd5e-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9dd5e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9dd5e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dd5e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd5e-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9dd5e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9dd5e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9dd5e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dd5e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dd5e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





