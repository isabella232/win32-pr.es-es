---
title: Enumeración BG_JOB_PRIORITY (Deliveryoptimization. h)
description: La enumeración BG_JOB_PRIORITY define los valores constantes que especifican el nivel de prioridad de un trabajo.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- Enumeración BG_JOB_PRIORITY
- Enumeración BG_JOB_PRIORITY
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079237"
---
# <a name="bg_job_priority-enumeration"></a><span data-ttu-id="6606e-105">Enumeración BG_JOB_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="6606e-105">BG_JOB_PRIORITY enumeration</span></span>

<span data-ttu-id="6606e-106">La enumeración **BG_JOB_PRIORITY** define los valores constantes que especifican el nivel de prioridad de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="6606e-106">The **BG_JOB_PRIORITY** enumeration defines the constant values that specify the priority level of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="6606e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6606e-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a><span data-ttu-id="6606e-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="6606e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6606e-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span><span class="sxs-lookup"><span data-stu-id="6606e-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span></span>
</dt> <dd>

<span data-ttu-id="6606e-110">Transfiere el trabajo en primer plano.</span><span class="sxs-lookup"><span data-stu-id="6606e-110">Transfers the job in the foreground.</span></span> <span data-ttu-id="6606e-111">Las transferencias en primer plano compiten por el ancho de banda de red con otras aplicaciones, lo que puede impedir la experiencia de red del usuario.</span><span class="sxs-lookup"><span data-stu-id="6606e-111">Foreground transfers compete for network bandwidth with other applications, which can impede the user's network experience.</span></span> <span data-ttu-id="6606e-112">Este es el nivel de prioridad más alto.</span><span class="sxs-lookup"><span data-stu-id="6606e-112">This is the highest priority level.</span></span>

</dd> <dt>

<span data-ttu-id="6606e-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span><span class="sxs-lookup"><span data-stu-id="6606e-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="6606e-114">Transfiere el trabajo en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="6606e-114">Transfers the job in the background.</span></span> <span data-ttu-id="6606e-115">Las transferencias en segundo plano usan un pequeño porcentaje de ancho de banda de red.</span><span class="sxs-lookup"><span data-stu-id="6606e-115">Background transfers use a small percentage of network bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="6606e-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span><span class="sxs-lookup"><span data-stu-id="6606e-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="6606e-117">El comportamiento es el mismo para todos los trabajos que no están en primer plano.</span><span class="sxs-lookup"><span data-stu-id="6606e-117">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="6606e-118">Vea los comentarios en BG_JOB_PRIORITY_HIGH para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6606e-118">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> <dt>

<span data-ttu-id="6606e-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span><span class="sxs-lookup"><span data-stu-id="6606e-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="6606e-120">El comportamiento es el mismo para todos los trabajos que no están en primer plano.</span><span class="sxs-lookup"><span data-stu-id="6606e-120">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="6606e-121">Vea los comentarios en BG_JOB_PRIORITY_HIGH para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6606e-121">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6606e-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6606e-122">Remarks</span></span>

<span data-ttu-id="6606e-123">Se pueden realizar varias transferencias en primer plano y en segundo plano simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="6606e-123">Multiple foreground and background transfers can take place simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="6606e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6606e-124">Requirements</span></span>



| <span data-ttu-id="6606e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6606e-125">Requirement</span></span> | <span data-ttu-id="6606e-126">Value</span><span class="sxs-lookup"><span data-stu-id="6606e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6606e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6606e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6606e-128">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="6606e-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6606e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6606e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6606e-130">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="6606e-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6606e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6606e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6606e-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6606e-132"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6606e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6606e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6606e-134">**IBackgroundCopyJob:: GetPriority (**</span><span class="sxs-lookup"><span data-stu-id="6606e-134">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[<span data-ttu-id="6606e-135">**IBackgroundCopyJob:: SetPriority**</span><span class="sxs-lookup"><span data-stu-id="6606e-135">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





