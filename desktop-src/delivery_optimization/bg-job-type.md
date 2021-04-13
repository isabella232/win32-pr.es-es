---
title: Enumeración BG_JOB_TYPE (Deliveryoptimization. h)
description: La enumeración BG_JOB_TYPE define valores constantes que especifican el tipo de trabajo de transferencia, como la descarga.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- Enumeración BG_JOB_TYPE
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490066"
---
# <a name="bg_job_type-enumeration"></a><span data-ttu-id="94236-104">Enumeración BG_JOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="94236-104">BG_JOB_TYPE enumeration</span></span>

<span data-ttu-id="94236-105">La enumeración **BG_JOB_TYPE** define valores constantes que especifican el tipo de trabajo de transferencia, como la descarga.</span><span class="sxs-lookup"><span data-stu-id="94236-105">The **BG_JOB_TYPE** enumeration defines constant values that specify the type of transfer job, such as download.</span></span>

## <a name="syntax"></a><span data-ttu-id="94236-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94236-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a><span data-ttu-id="94236-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="94236-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="94236-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span><span class="sxs-lookup"><span data-stu-id="94236-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="94236-109">Especifica que el trabajo descarga archivos en el cliente.</span><span class="sxs-lookup"><span data-stu-id="94236-109">Specifies that the job downloads files to the client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94236-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94236-110">Requirements</span></span>



| <span data-ttu-id="94236-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="94236-111">Requirement</span></span> | <span data-ttu-id="94236-112">Value</span><span class="sxs-lookup"><span data-stu-id="94236-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94236-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94236-113">Minimum supported client</span></span><br/> | <span data-ttu-id="94236-114">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="94236-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="94236-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94236-115">Minimum supported server</span></span><br/> | <span data-ttu-id="94236-116">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="94236-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="94236-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94236-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="94236-118"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="94236-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94236-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="94236-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94236-120">**IBackgroundCopyJob:: GetType**</span><span class="sxs-lookup"><span data-stu-id="94236-120">**IBackgroundCopyJob::GetType**</span></span>](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[<span data-ttu-id="94236-121">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="94236-121">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





