---
description: Representa el estado configurado de un dispositivo de partición GPU.
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Msvm_GpuPartitionSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d8c9809b3a062654eaf0fb7a73b75b0188f7284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001254"
---
# <a name="msvm_gpupartitionsettingdata-class"></a><span data-ttu-id="433de-103">MSVM \_ GpuPartitionSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="433de-103">Msvm\_GpuPartitionSettingData class</span></span>

<span data-ttu-id="433de-104">Representa el estado configurado de un dispositivo de partición GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-104">Represents the configured state of a GPU partition device.</span></span>

<span data-ttu-id="433de-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="433de-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="433de-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="433de-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="433de-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="433de-107">Members</span></span>

<span data-ttu-id="433de-108">La clase **MSVM \_ GpuPartitionSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="433de-108">The **Msvm\_GpuPartitionSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="433de-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="433de-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="433de-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="433de-110">Properties</span></span>

<span data-ttu-id="433de-111">La clase **MSVM \_ GpuPartitionSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="433de-111">The **Msvm\_GpuPartitionSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="433de-112">**MaxPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="433de-112">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-113">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-115">La cantidad máxima de motores de proceso que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-115">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="433de-116">**MaxPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="433de-116">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-117">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-117">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-119">La cantidad máxima de motores de descodificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-119">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="433de-120">**MaxPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="433de-120">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-121">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-123">La cantidad máxima de motores de codificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-123">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="433de-124">**MaxPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="433de-124">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-125">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-127">Cantidad máxima de VRAM que aparecerá en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-127">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="433de-128">**MinPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="433de-128">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-129">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-131">La cantidad mínima de motores de proceso que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-131">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="433de-132">**MinPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="433de-132">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-133">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-135">La cantidad mínima de motores de descodificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-135">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="433de-136">**MinPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="433de-136">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-137">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-139">La cantidad mínima de motores de codificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-139">The minimum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="433de-140">**MinPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="433de-140">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-141">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-143">La cantidad mínima de VRAM que aparecerá en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-143">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="433de-144">**OptimalPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="433de-144">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-145">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-146">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-147">La cantidad óptima de motores de proceso que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-147">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="433de-148">**OptimalPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="433de-148">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-149">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-151">La cantidad óptima de motores de descodificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-151">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="433de-152">**OptimalPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="433de-152">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-153">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-155">La cantidad óptima de motores de codificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-155">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="433de-156">**OptimalPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="433de-156">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433de-157">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="433de-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="433de-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="433de-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="433de-159">Cantidad óptima de VRAM que aparecerá en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="433de-159">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="433de-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="433de-160">Requirements</span></span>



| <span data-ttu-id="433de-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="433de-161">Requirement</span></span> | <span data-ttu-id="433de-162">Value</span><span class="sxs-lookup"><span data-stu-id="433de-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="433de-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="433de-163">Minimum supported client</span></span><br/> | <span data-ttu-id="433de-164">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="433de-164">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="433de-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="433de-165">Minimum supported server</span></span><br/> | <span data-ttu-id="433de-166">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="433de-166">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="433de-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="433de-167">Namespace</span></span><br/>                | <span data-ttu-id="433de-168">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="433de-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="433de-169">MOF</span><span class="sxs-lookup"><span data-stu-id="433de-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="433de-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="433de-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="433de-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="433de-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="433de-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="433de-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="433de-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="433de-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433de-174">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="433de-174">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




