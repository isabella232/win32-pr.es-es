---
title: Enumeración BITS_JOB_TRANSFER_POLICY (Deliveryoptimization. h)
description: La enumeración BITS_JOB_TRANSFER_POLICY define los valores de identificador correspondientes a las propiedades de DO.
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- Enumeración BITS_JOB_TRANSFER_POLICY
- Enumeración BITS_JOB_TRANSFER_POLICY
topic_type:
- apiref
api_name:
- BITS_JOB_TRANSFER_POLICY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 455752375b76e574923ccdd96d1d05fc9142c16c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150075"
---
# <a name="bits_job_transfer_policy-enumeration"></a><span data-ttu-id="fd3a8-105">Enumeración BITS_JOB_TRANSFER_POLICY</span><span class="sxs-lookup"><span data-stu-id="fd3a8-105">BITS_JOB_TRANSFER_POLICY enumeration</span></span>

<span data-ttu-id="fd3a8-106">La enumeración **BITS_JOB_TRANSFER_POLICY** define los valores de identificador correspondientes a las propiedades de do.</span><span class="sxs-lookup"><span data-stu-id="fd3a8-106">The **BITS_JOB_TRANSFER_POLICY** enumeration defines ID values corresponding to DO properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd3a8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd3a8-107">Syntax</span></span>


```C++
typedef enum _BITS_JOB_TRANSFER_POLICY { 
  BITS_JOB_TRANSFER_POLICY_ALWAYS        = 0x800000ff,
  BITS_JOB_TRANSFER_POLICY_NOT_ROAMING   = 0x8000007f,
  BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE  = 0x8000006f,
  BITS_JOB_TRANSFER_POLICY_STANDARD      = 0x80000067,
  BITS_JOB_TRANSFER_POLICY_UNRESTRICTED  = 0x80000021
} BITS_JOB_TRANSFER_POLICY;
```



## <a name="constants"></a><span data-ttu-id="fd3a8-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="fd3a8-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd3a8-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span><span class="sxs-lookup"><span data-stu-id="fd3a8-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="fd3a8-110">Especifica que el trabajo se transferirá cuando la conectividad esté disponible, independientemente del costo.</span><span class="sxs-lookup"><span data-stu-id="fd3a8-110">Specifies that the job will be transferred when connectivity is available, regardless of the cost.</span></span>

</dd> <dt>

<span data-ttu-id="fd3a8-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span><span class="sxs-lookup"><span data-stu-id="fd3a8-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span></span>
</dt> <dd>

<span data-ttu-id="fd3a8-112">Especifica que el trabajo se transferirá cuando la conectividad esté disponible, a menos que la conectividad esté sujeta a suplementos móviles.</span><span class="sxs-lookup"><span data-stu-id="fd3a8-112">Specifies that the job will be transferred when connectivity is available, unless that connectivity is subject to roaming surcharges.</span></span>

</dd> <dt>

<span data-ttu-id="fd3a8-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span><span class="sxs-lookup"><span data-stu-id="fd3a8-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span></span>
</dt> <dd>

<span data-ttu-id="fd3a8-114">Especifica que el trabajo se transferirá solo cuando la conectividad esté disponible, lo que no está sujeto a un suplemento.</span><span class="sxs-lookup"><span data-stu-id="fd3a8-114">Specifies that the job will be transferred only when connectivity is available which is not subject to a surcharge.</span></span>

</dd> <dt>

<span data-ttu-id="fd3a8-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span><span class="sxs-lookup"><span data-stu-id="fd3a8-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="fd3a8-116">Especifica que el trabajo se transferirá solo cuando la conectividad esté disponible, lo que no está sujeto a un suplemento ni a un agotamiento cercano.</span><span class="sxs-lookup"><span data-stu-id="fd3a8-116">Specifies that the job will be transferred only when connectivity is available which is neither subject to a surcharge nor near exhaustion.</span></span>

</dd> <dt>

<span data-ttu-id="fd3a8-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span><span class="sxs-lookup"><span data-stu-id="fd3a8-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span></span>
</dt> <dd>

<span data-ttu-id="fd3a8-118">Especifica que el trabajo se transferirá solo cuando esté disponible la conectividad que no imponga costos ni límites de tráfico.</span><span class="sxs-lookup"><span data-stu-id="fd3a8-118">Specifies that the job will be transferred only when connectivity is available which does not impose costs or traffic limits.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd3a8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd3a8-119">Requirements</span></span>



| <span data-ttu-id="fd3a8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd3a8-120">Requirement</span></span> | <span data-ttu-id="fd3a8-121">Value</span><span class="sxs-lookup"><span data-stu-id="fd3a8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3a8-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd3a8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fd3a8-123">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd3a8-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fd3a8-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd3a8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fd3a8-125">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="fd3a8-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fd3a8-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd3a8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd3a8-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd3a8-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





