---
description: Representa una GPU particionable. Cada GPU se puede segmentar en varias particiones de GPU, que se pueden asignar a una máquina virtual como vGPU.
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Msvm_PartitionableGpu (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f82904608a8e2ee4dfa13942066d57d35d511f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913113"
---
# <a name="msvm_partitionablegpu-class"></a><span data-ttu-id="f4382-104">MSVM \_ PartitionableGpu (clase)</span><span class="sxs-lookup"><span data-stu-id="f4382-104">Msvm\_PartitionableGpu class</span></span>

<span data-ttu-id="f4382-105">Representa una GPU particionable.</span><span class="sxs-lookup"><span data-stu-id="f4382-105">Represents a partitionable GPU.</span></span> <span data-ttu-id="f4382-106">Cada GPU se puede segmentar en varias particiones de GPU, que se pueden asignar a una máquina virtual como vGPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-106">Each GPU can be sliced into a number of GPU partitions, which can be assigned to a virtual machine as a vGPU.</span></span>

<span data-ttu-id="f4382-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f4382-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4382-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4382-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="f4382-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f4382-109">Members</span></span>

<span data-ttu-id="f4382-110">La clase **MSVM \_ PartitionableGpu** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f4382-110">The **Msvm\_PartitionableGpu** class has these types of members:</span></span>

-   [<span data-ttu-id="f4382-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4382-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4382-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4382-112">Properties</span></span>

<span data-ttu-id="f4382-113">La clase **MSVM \_ PartitionableGpu** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f4382-113">The **Msvm\_PartitionableGpu** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4382-114">**AvailableCompute**</span><span class="sxs-lookup"><span data-stu-id="f4382-114">**AvailableCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-115">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-117">La cantidad disponible de motores de proceso que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-117">The available amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-118">**AvailableDecode**</span><span class="sxs-lookup"><span data-stu-id="f4382-118">**AvailableDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-119">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-121">La cantidad disponible de motores de descodificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-121">The available amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-122">**AvailableEncode**</span><span class="sxs-lookup"><span data-stu-id="f4382-122">**AvailableEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-123">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-125">La cantidad disponible de motores de codificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-125">The available amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-126">**AvailableVRAM**</span><span class="sxs-lookup"><span data-stu-id="f4382-126">**AvailableVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-127">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-127">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-129">Cantidad de VRAM disponible que aparecerá en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-129">The available amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-130">**MaxPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="f4382-130">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-131">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-133">La cantidad máxima de motores de proceso que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-133">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-134">**MaxPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="f4382-134">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-135">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-137">La cantidad máxima de motores de descodificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-137">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-138">**MaxPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="f4382-138">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-139">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-139">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-141">La cantidad máxima de motores de codificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-141">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-142">**MaxPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="f4382-142">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-143">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-145">Cantidad máxima de VRAM que aparecerá en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-145">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-146">**MinPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="f4382-146">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-147">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-149">La cantidad mínima de motores de proceso que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-149">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-150">**MinPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="f4382-150">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-151">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-153">La cantidad mínima de motores de descodificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-153">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-154">**MinPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="f4382-154">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-155">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-157">La cantidad mínima de motores de codificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-157">The minumum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-158">**MinPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="f4382-158">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-159">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-161">La cantidad mínima de VRAM que aparecerá en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-161">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-162">**OptimalPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="f4382-162">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-163">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-165">La cantidad óptima de motores de proceso que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-165">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-166">**OptimalPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="f4382-166">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-167">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-169">La cantidad óptima de motores de descodificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-169">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-170">**OptimalPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="f4382-170">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-171">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-173">La cantidad óptima de motores de codificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-173">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-174">**OptimalPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="f4382-174">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-175">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-177">Cantidad óptima de VRAM que aparecerá en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-177">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-178">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="f4382-178">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-179">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4382-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-180">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f4382-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f4382-181">La cantidad de particiones de GPU en la que se segmenta la GPU física.</span><span class="sxs-lookup"><span data-stu-id="f4382-181">The amount of GPU partitions the physical GPU is sliced into.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-182">**TotalCompute**</span><span class="sxs-lookup"><span data-stu-id="f4382-182">**TotalCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-183">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-185">La cantidad total de motores de proceso que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-185">The total amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-186">**TotalDecode**</span><span class="sxs-lookup"><span data-stu-id="f4382-186">**TotalDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-187">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-189">La cantidad total de motores de descodificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-189">The total amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-190">**TotalEncode**</span><span class="sxs-lookup"><span data-stu-id="f4382-190">**TotalEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-191">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-193">La cantidad total de motores de codificación que aparecerán en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-193">The total amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-194">**TotalVRAM**</span><span class="sxs-lookup"><span data-stu-id="f4382-194">**TotalVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-195">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4382-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4382-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4382-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4382-197">La cantidad total de VRAM que aparecerá en la partición de GPU.</span><span class="sxs-lookup"><span data-stu-id="f4382-197">The total amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f4382-198">**ValidPartitionCounts**</span><span class="sxs-lookup"><span data-stu-id="f4382-198">**ValidPartitionCounts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4382-199">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4382-199">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f4382-200">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f4382-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f4382-201">Una matriz de opciones de partición GPU válida en la que se puede segmentar la GPU física.</span><span class="sxs-lookup"><span data-stu-id="f4382-201">An array of valid GPU partition options the physical GPU can be sliced into.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4382-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4382-202">Requirements</span></span>



| <span data-ttu-id="f4382-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4382-203">Requirement</span></span> | <span data-ttu-id="f4382-204">Value</span><span class="sxs-lookup"><span data-stu-id="f4382-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4382-205">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4382-205">Minimum supported client</span></span><br/> | <span data-ttu-id="f4382-206">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4382-206">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f4382-207">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4382-207">Minimum supported server</span></span><br/> | <span data-ttu-id="f4382-208">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f4382-208">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f4382-209">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f4382-209">Namespace</span></span><br/>                | <span data-ttu-id="f4382-210">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f4382-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f4382-211">MOF</span><span class="sxs-lookup"><span data-stu-id="f4382-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4382-212"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4382-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4382-213">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f4382-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4382-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f4382-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f4382-215">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4382-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4382-216">**ComputerSystem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f4382-216">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




