---
title: Enumeración BITS_JOB_PROPERTY_ID (Deliveryoptimization. h)
description: La enumeración BITS_JOB_PROPERTY_ID especifica el identificador de la propiedad para el trabajo DO. Esta enumeración se utiliza en la Unión BITS_JOB_PROPERTY_VALUE para determinar el tipo de valor contenido en la Unión.
ms.assetid: B0F3C6C2-474F-4FD8-990A-770FAA993550
keywords:
- Enumeración BITS_JOB_PROPERTY_ID
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1d00d4dc12b27c1c80b0e18bb095641a56e322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801388"
---
# <a name="bits_job_property_id-enumeration"></a><span data-ttu-id="ee2d9-105">Enumeración BITS_JOB_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="ee2d9-105">BITS_JOB_PROPERTY_ID enumeration</span></span>

<span data-ttu-id="ee2d9-106">La enumeración **BITS_JOB_PROPERTY_ID** especifica el identificador de la propiedad para el trabajo do.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-106">The **BITS_JOB_PROPERTY_ID** enumeration specifies the ID of the property for the DO job.</span></span> <span data-ttu-id="ee2d9-107">Esta enumeración se utiliza en la Unión [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) para determinar el tipo de valor contenido en la Unión.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-107">This enumeration is used in the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union to determine the type of value contained in the union.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee2d9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee2d9-108">Syntax</span></span>


```C++
typedef enum  { 
  BITS_JOB_PROPERTY_ID_COST_FLAGS                     = 1,
  BITS_JOB_PROPERTY_NOTIFICATION_CLSID                = 2,
  BITS_JOB_PROPERTY_DYNAMIC_CONTENT                   = 3,
  BITS_JOB_PROPERTY_HIGH_PERFORMANCE                  = 4,
  BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE                 = 5,
  BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS            = 7,
  BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS  = 9,
  BITS_JOB_PROPERTY_ON_DEMAND_MODE                    = 10
} BITS_JOB_PROPERTY_ID;
```



## <a name="constants"></a><span data-ttu-id="ee2d9-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="ee2d9-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ee2d9-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="ee2d9-111">IDENTIFICADOR que se usa para [controlar el comportamiento](https://www.bing.com/search?q=control+transfer+behavior) de la transferencia en redes móviles o similares.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-111">The ID that is used to [control transfer behavior](https://www.bing.com/search?q=control+transfer+behavior) over cellular and/or similar networks.</span></span> <span data-ttu-id="ee2d9-112">Esta propiedad se puede cambiar mientras se realiza una transferencia. las nuevas marcas de costo surtirán efecto inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-112">This property may be changed while a transfer is ongoing   the new cost flags will take effect immediately.</span></span>

<span data-ttu-id="ee2d9-113">Esta propiedad usa el campo **Dword** **BITS_JOB_PROPERTY_VALUE** s.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-113">This property uses the **BITS_JOB_PROPERTY_VALUE** s **Dword** field.</span></span>

</dd> <dt>

<span data-ttu-id="ee2d9-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="ee2d9-115">IDENTIFICADOR que se usa para [registrar una devolución de llamada com](https://www.bing.com/search?q=register+a+COM+callback) por CLSID para recibir notificaciones sobre el progreso y la finalización de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-115">The ID that is used to [register a COM callback](https://www.bing.com/search?q=register+a+COM+callback) by CLSID to receive notifications about the progress and completion of a DO job.</span></span> <span data-ttu-id="ee2d9-116">El CLSID debe hacer referencia a una clase asociada a un servidor COM fuera de proceso registrado.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-116">The CLSID must refer to a class associated with a registered out-of-process COM server.</span></span> <span data-ttu-id="ee2d9-117">También puede establecerse en **GUID_NULL** para borrar un CLSID de notificación establecido previamente.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-117">It may also be set to **GUID_NULL** to clear a previously set notification CLSID.</span></span>

<span data-ttu-id="ee2d9-118">Esta propiedad usa el campo **CLsID** **BITS_JOB_PROPERTY_VALUE** s.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-118">This property uses the **BITS_JOB_PROPERTY_VALUE** s **CLsID** field.</span></span>

</dd> <dt>

<span data-ttu-id="ee2d9-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="ee2d9-120">No se admite.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-120">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ee2d9-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span></span>
</dt> <dd>

<span data-ttu-id="ee2d9-122">No se admite.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ee2d9-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span></span>
</dt> <dd>

<span data-ttu-id="ee2d9-124">No se admite.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-124">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ee2d9-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="ee2d9-126">No se admite.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-126">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ee2d9-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span></span>
</dt> <dd>

<span data-ttu-id="ee2d9-128">No se admite.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-128">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ee2d9-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="ee2d9-130">No se admite.</span><span class="sxs-lookup"><span data-stu-id="ee2d9-130">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee2d9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee2d9-131">Requirements</span></span>



| <span data-ttu-id="ee2d9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee2d9-132">Requirement</span></span> | <span data-ttu-id="ee2d9-133">Value</span><span class="sxs-lookup"><span data-stu-id="ee2d9-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee2d9-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee2d9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ee2d9-135">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee2d9-135">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ee2d9-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee2d9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ee2d9-137">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="ee2d9-137">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ee2d9-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee2d9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee2d9-139"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee2d9-139"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee2d9-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee2d9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee2d9-141">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-141">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="ee2d9-142">**BITS_JOB_PROPERTY_VALUE**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-142">**BITS_JOB_PROPERTY_VALUE**</span></span>](bits-job-property-value-.md)
</dt> <dt>

[<span data-ttu-id="ee2d9-143">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-143">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> <dt>

[<span data-ttu-id="ee2d9-144">**IBackgroundCopyJob5:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-144">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> <dt>

[<span data-ttu-id="ee2d9-145">**IBackgroundCopyJob5:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="ee2d9-145">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





