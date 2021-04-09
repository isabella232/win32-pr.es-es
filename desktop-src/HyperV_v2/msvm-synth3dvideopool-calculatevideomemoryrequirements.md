---
description: Calcula la cantidad de memoria de vídeo necesaria para una máquina virtual de RemoteFX.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Método CalculateVideoMemoryRequirements de la clase Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154592"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a><span data-ttu-id="56cb0-103">Método CalculateVideoMemoryRequirements de la \_ clase Synth3dVideoPool de MSVM</span><span class="sxs-lookup"><span data-stu-id="56cb0-103">CalculateVideoMemoryRequirements method of the Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="56cb0-104">Calcula la cantidad de memoria de vídeo necesaria para una máquina virtual de RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="56cb0-104">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="56cb0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56cb0-105">Syntax</span></span>


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a><span data-ttu-id="56cb0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56cb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56cb0-107">*monitorResolution* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="56cb0-107">*monitorResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56cb0-108">La resolución máxima del monitor de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="56cb0-108">The maximum monitor resolution for the virtual machine.</span></span> <span data-ttu-id="56cb0-109">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="56cb0-109">This must be one of the following values.</span></span>



| <span data-ttu-id="56cb0-110">Value</span><span class="sxs-lookup"><span data-stu-id="56cb0-110">Value</span></span>                                                                        | <span data-ttu-id="56cb0-111">Significado</span><span class="sxs-lookup"><span data-stu-id="56cb0-111">Meaning</span></span>                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="56cb0-112"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-112"><dt>0</dt></span></span> </dl> | <span data-ttu-id="56cb0-113">La resolución máxima es 1024 768.</span><span class="sxs-lookup"><span data-stu-id="56cb0-113">The maximum resolution is 1024   768.</span></span><br/>  |
| <dl> <span data-ttu-id="56cb0-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-114"><dt>1</dt></span></span> </dl> | <span data-ttu-id="56cb0-115">La resolución máxima es 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="56cb0-115">The maximum resolution is 1280   1024.</span></span><br/> |
| <dl> <span data-ttu-id="56cb0-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-116"><dt>2</dt></span></span> </dl> | <span data-ttu-id="56cb0-117">La resolución máxima es 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="56cb0-117">The maximum resolution is 1600   1200.</span></span><br/> |
| <dl> <span data-ttu-id="56cb0-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="56cb0-119">La resolución máxima es 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="56cb0-119">The maximum resolution is 1920   1200.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="56cb0-120">*numberOfMonitors* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="56cb0-120">*numberOfMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56cb0-121">Número máximo de monitores para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="56cb0-121">The maximum number of monitors for the virtual machine.</span></span> <span data-ttu-id="56cb0-122">El número mínimo de monitores es uno y el máximo depende de la resolución de pantalla máxima.</span><span class="sxs-lookup"><span data-stu-id="56cb0-122">The minimum number of monitors is one and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="56cb0-123">En la tabla siguiente se define el número máximo de monitores permitido para diferentes resoluciones.</span><span class="sxs-lookup"><span data-stu-id="56cb0-123">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="56cb0-124">Solución</span><span class="sxs-lookup"><span data-stu-id="56cb0-124">Resolution</span></span>             | <span data-ttu-id="56cb0-125">Monitores máximos</span><span class="sxs-lookup"><span data-stu-id="56cb0-125">Maximum monitors</span></span> |
|------------------------|------------------|
| <span data-ttu-id="56cb0-126">1024 768</span><span class="sxs-lookup"><span data-stu-id="56cb0-126">1024   768</span></span><br/>  | <span data-ttu-id="56cb0-127">4</span><span class="sxs-lookup"><span data-stu-id="56cb0-127">4</span></span><br/>     |
| <span data-ttu-id="56cb0-128">1280 1024</span><span class="sxs-lookup"><span data-stu-id="56cb0-128">1280   1024</span></span><br/> | <span data-ttu-id="56cb0-129">4</span><span class="sxs-lookup"><span data-stu-id="56cb0-129">4</span></span><br/>     |
| <span data-ttu-id="56cb0-130">1600 1200</span><span class="sxs-lookup"><span data-stu-id="56cb0-130">1600   1200</span></span><br/> | <span data-ttu-id="56cb0-131">3</span><span class="sxs-lookup"><span data-stu-id="56cb0-131">3</span></span><br/>     |
| <span data-ttu-id="56cb0-132">1920 1200</span><span class="sxs-lookup"><span data-stu-id="56cb0-132">1920   1200</span></span><br/> | <span data-ttu-id="56cb0-133">2</span><span class="sxs-lookup"><span data-stu-id="56cb0-133">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="56cb0-134">*requiredVideoMemory* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="56cb0-134">*requiredVideoMemory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56cb0-135">Recibe la cantidad necesaria de memoria de vídeo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="56cb0-135">Receives the required amount of video memory, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56cb0-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56cb0-136">Return value</span></span>

<span data-ttu-id="56cb0-137">Devuelve un código de estado, que puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="56cb0-137">Returns a status code, which can be one of the following values.</span></span>



| <span data-ttu-id="56cb0-138">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56cb0-138">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="56cb0-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="56cb0-139">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="56cb0-140"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-140"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="56cb0-141">Ejecutado.</span><span class="sxs-lookup"><span data-stu-id="56cb0-141">Successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="56cb0-142"><dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="56cb0-143">Trabajo iniciado.</span><span class="sxs-lookup"><span data-stu-id="56cb0-143">Job started.</span></span><br/>                               |
| <dl> <span data-ttu-id="56cb0-144"><dt>**Error**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-144"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="56cb0-145">Failed.</span><span class="sxs-lookup"><span data-stu-id="56cb0-145">Failed.</span></span><br/>                                    |
| <dl> <span data-ttu-id="56cb0-146"><dt>**Acceso Denegado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-146"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="56cb0-147">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="56cb0-147">Access denied.</span></span><br/>                             |
| <dl> <span data-ttu-id="56cb0-148"><dt>**No compatible**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-148"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="56cb0-149">No se admite.</span><span class="sxs-lookup"><span data-stu-id="56cb0-149">Not supported.</span></span><br/>                             |
| <dl> <span data-ttu-id="56cb0-150">El <dt>**Estado es desconocido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-150"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="56cb0-151">Se desconoce el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="56cb0-151">Status is unknown.</span></span><br/>                         |
| <dl> <span data-ttu-id="56cb0-152"><dt>**Tiempo de espera**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-152"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="56cb0-153">Tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="56cb0-153">Timeout.</span></span><br/>                                   |
| <dl> <span data-ttu-id="56cb0-154"><dt>**Parámetro no válido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-154"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="56cb0-155">Un parámetro no es válido.</span><span class="sxs-lookup"><span data-stu-id="56cb0-155">A parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="56cb0-156">El <dt>**sistema está en uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-156"><dt>**System is in used**</dt> <dt>32774</dt></span></span> </dl>                      | <span data-ttu-id="56cb0-157">El sistema está en uso.</span><span class="sxs-lookup"><span data-stu-id="56cb0-157">System is in use.</span></span><br/>                          |
| <dl> <span data-ttu-id="56cb0-158"><dt>**Estado no válido para esta operación**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-158"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="56cb0-159">El estado no es válido para esta operación.</span><span class="sxs-lookup"><span data-stu-id="56cb0-159">The state is not valid for this operation.</span></span><br/> |
| <dl> <span data-ttu-id="56cb0-160"><dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-160"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="56cb0-161">Tipo de datos incorrecto.</span><span class="sxs-lookup"><span data-stu-id="56cb0-161">Incorrect data type.</span></span><br/>                       |
| <dl> <span data-ttu-id="56cb0-162">El <dt>**sistema no está disponible**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-162"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="56cb0-163">El sistema no está disponible.</span><span class="sxs-lookup"><span data-stu-id="56cb0-163">System is not available.</span></span><br/>                   |
| <dl> <span data-ttu-id="56cb0-164"><dt>**Memoria**</dt> insuficiente <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-164"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="56cb0-165">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="56cb0-165">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="56cb0-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56cb0-166">Remarks</span></span>

<span data-ttu-id="56cb0-167">Normalmente, se llama a este método en el sistema host para determinar si el host tiene suficiente memoria de vídeo disponible para hospedar una máquina virtual de RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="56cb0-167">This method is typically called on the host system to determine if the host has enough available video memory to host a RemoteFX virtual machine.</span></span> <span data-ttu-id="56cb0-168">Para ello, compare la cantidad de memoria de vídeo calculada por este método con la propiedad [**MSVM \_ PhysicalGPUInfo. AvailableVideoMemory**](msvm-physicalgpuinfo.md) para determinar si el equipo host tiene suficiente memoria de vídeo disponible.</span><span class="sxs-lookup"><span data-stu-id="56cb0-168">To do this, you compare the amount of video memory calculated by this method with the [**Msvm\_PhysicalGPUInfo.AvailableVideoMemory**](msvm-physicalgpuinfo.md) property to determine if the host machine has enough available video memory.</span></span> <span data-ttu-id="56cb0-169">Puede usar esta información para determinar si una máquina virtual se puede migrar al sistema host.</span><span class="sxs-lookup"><span data-stu-id="56cb0-169">You can use this information to determine if a virtual machine can be moved to the host system.</span></span>

## <a name="requirements"></a><span data-ttu-id="56cb0-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56cb0-170">Requirements</span></span>



| <span data-ttu-id="56cb0-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="56cb0-171">Requirement</span></span> | <span data-ttu-id="56cb0-172">Value</span><span class="sxs-lookup"><span data-stu-id="56cb0-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56cb0-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56cb0-173">Minimum supported client</span></span><br/> | <span data-ttu-id="56cb0-174">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="56cb0-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="56cb0-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56cb0-175">Minimum supported server</span></span><br/> | <span data-ttu-id="56cb0-176">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="56cb0-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56cb0-177">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="56cb0-177">Namespace</span></span><br/>                | <span data-ttu-id="56cb0-178">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="56cb0-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="56cb0-179">MOF</span><span class="sxs-lookup"><span data-stu-id="56cb0-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56cb0-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="56cb0-181">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56cb0-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56cb0-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="56cb0-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="56cb0-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="56cb0-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56cb0-184">**MSVM \_ PhysicalGPUInfo**</span><span class="sxs-lookup"><span data-stu-id="56cb0-184">**Msvm\_PhysicalGPUInfo**</span></span>](msvm-physicalgpuinfo.md)
</dt> <dt>

[<span data-ttu-id="56cb0-185">**MSVM \_ Synth3dVideoPool**</span><span class="sxs-lookup"><span data-stu-id="56cb0-185">**Msvm\_Synth3dVideoPool**</span></span>](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




