---
title: Mensaje de PBM_SETSTEP (commctrl. h)
description: Especifica el incremento de paso de una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un mensaje de STEPIT de PBM \_ . De forma predeterminada, el incremento de paso se establece en 10.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- PBM_SETSTEP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240d09aeadcd7994187704d0b5a4630ab1b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658263"
---
# <a name="pbm_setstep-message"></a><span data-ttu-id="3b5e1-106">Mensaje de SETSTEP de PBM \_</span><span class="sxs-lookup"><span data-stu-id="3b5e1-106">PBM\_SETSTEP message</span></span>

<span data-ttu-id="3b5e1-107">Especifica el incremento de paso de una barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="3b5e1-107">Specifies the step increment for a progress bar.</span></span> <span data-ttu-id="3b5e1-108">El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un mensaje de [**\_ STEPIT de PBM**](pbm-stepit.md) .</span><span class="sxs-lookup"><span data-stu-id="3b5e1-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="3b5e1-109">De forma predeterminada, el incremento de paso se establece en 10.</span><span class="sxs-lookup"><span data-stu-id="3b5e1-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b5e1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b5e1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b5e1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b5e1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b5e1-112">Nuevo incremento de paso.</span><span class="sxs-lookup"><span data-stu-id="3b5e1-112">New step increment.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e1-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b5e1-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3b5e1-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3b5e1-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b5e1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b5e1-115">Return value</span></span>

<span data-ttu-id="3b5e1-116">Devuelve el incremento del paso anterior.</span><span class="sxs-lookup"><span data-stu-id="3b5e1-116">Returns the previous step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b5e1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b5e1-117">Requirements</span></span>



| <span data-ttu-id="3b5e1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b5e1-118">Requirement</span></span> | <span data-ttu-id="3b5e1-119">Value</span><span class="sxs-lookup"><span data-stu-id="3b5e1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b5e1-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b5e1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b5e1-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3b5e1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b5e1-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b5e1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b5e1-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b5e1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b5e1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b5e1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b5e1-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b5e1-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





