---
description: La \_ clase CIM MemoryCapacity representa la memoria que se puede instalar en un elemento físico y sus configuraciones mínima y máxima.
ms.assetid: a962ee38-9281-4a7a-b9d7-b321edb5670d
ms.tgt_platform: multiple
title: CIM_MemoryCapacity (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCapacity
- CIM_MemoryCapacity.Caption
- CIM_MemoryCapacity.Description
- CIM_MemoryCapacity.Name
- CIM_MemoryCapacity.MaximumMemoryCapacity
- CIM_MemoryCapacity.MemoryType
- CIM_MemoryCapacity.MinimumMemoryCapacity
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa63d06187c76c5add433502d012cdb63905795a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274871"
---
# <a name="cim_memorycapacity-class"></a><span data-ttu-id="2fe8e-103">\_Clase MemoryCapacity de CIM</span><span class="sxs-lookup"><span data-stu-id="2fe8e-103">CIM\_MemoryCapacity class</span></span>

<span data-ttu-id="2fe8e-104">La clase **CIM \_ MemoryCapacity** representa la memoria que se puede instalar en un elemento físico y sus configuraciones mínima y máxima.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-104">The **CIM\_MemoryCapacity** class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="2fe8e-105">La información sobre la memoria que está instalada actualmente y los requisitos mínimos y máximos de un elemento se encuentra en las instancias de la clase [**\_ PhysicalMemory de CIM**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="2fe8e-105">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fe8e-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2fe8e-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2fe8e-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2fe8e-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2fe8e-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fe8e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fe8e-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryCapacity : CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
  uint64 MaximumMemoryCapacity;
  uint16 MemoryType;
  uint64 MinimumMemoryCapacity;
};
```

## <a name="members"></a><span data-ttu-id="2fe8e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2fe8e-111">Members</span></span>

<span data-ttu-id="2fe8e-112">La clase **CIM \_ MemoryCapacity** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2fe8e-112">The **CIM\_MemoryCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="2fe8e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fe8e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fe8e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fe8e-114">Properties</span></span>

<span data-ttu-id="2fe8e-115">La clase **CIM \_ MemoryCapacity** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-115">The **CIM\_MemoryCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2fe8e-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fe8e-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fe8e-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fe8e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fe8e-119">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2fe8e-120">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-120">Short textual description of the object.</span></span>

<span data-ttu-id="2fe8e-121">Esta propiedad se hereda de [**\_ PhysicalCapacity CIM**](cim-physicalcapacity.md).</span><span class="sxs-lookup"><span data-stu-id="2fe8e-121">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fe8e-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fe8e-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fe8e-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fe8e-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fe8e-125">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-125">Textual description of the object.</span></span>

<span data-ttu-id="2fe8e-126">Esta propiedad se hereda de [**\_ PhysicalCapacity CIM**](cim-physicalcapacity.md).</span><span class="sxs-lookup"><span data-stu-id="2fe8e-126">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fe8e-127">**MaximumMemoryCapacity**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-127">**MaximumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fe8e-128">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2fe8e-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fe8e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fe8e-130">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="2fe8e-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2fe8e-131">Cantidad máxima de memoria, en kilobytes, que puede admitir el elemento físico asociado.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-131">Maximum amount of memory, in kilobytes, that can be supported by the associated physical element.</span></span>

<span data-ttu-id="2fe8e-132">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2fe8e-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2fe8e-133">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-133">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fe8e-134">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2fe8e-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fe8e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fe8e-136">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalMemory**](cim-physicalmemory.md).**MemoryType**")</span><span class="sxs-lookup"><span data-stu-id="2fe8e-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalMemory**](cim-physicalmemory.md).**MemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="2fe8e-137">Tipo de memoria, que forma parte de la clave de objeto.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-137">Type of memory, which is part of the object key.</span></span> <span data-ttu-id="2fe8e-138">Los valores corresponden a la lista de posibles tipos de memoria de la clase [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="2fe8e-138">Values correspond to the list of possible memory types in the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2fe8e-139">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2fe8e-140">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="2fe8e-141">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-141">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="2fe8e-142">**DRAM sincrónica** (3)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-142">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="2fe8e-143">**DRAM de caché** (4)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-143">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="2fe8e-144">**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-144">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="2fe8e-145">**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-145">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="2fe8e-146">**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-146">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="2fe8e-147">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-147">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="2fe8e-148">**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-148">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="2fe8e-149">**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-149">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="2fe8e-150">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-150">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="2fe8e-151">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-151">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="2fe8e-152">**Feprom** (13)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-152">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="2fe8e-153">**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-153">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="2fe8e-154">**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-154">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="2fe8e-155">**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-155">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="2fe8e-156">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-156">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="2fe8e-157">**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-157">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="2fe8e-158">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-158">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="2fe8e-159">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-159">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR-2"></span><span id="ddr-2"></span>

<span data-ttu-id="2fe8e-160">**DDR-2** (21)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-160">**DDR-2** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2fe8e-161">**MinimumMemoryCapacity**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-161">**MinimumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fe8e-162">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2fe8e-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fe8e-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fe8e-164">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="2fe8e-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2fe8e-165">Cantidad mínima de memoria, en kilobytes, que se necesita para que el elemento físico asociado funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-165">Minimum amount of memory, in kilobytes, that is needed for the associated physical element to operate correctly.</span></span>

<span data-ttu-id="2fe8e-166">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2fe8e-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2fe8e-167">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fe8e-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fe8e-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fe8e-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fe8e-170">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2fe8e-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2fe8e-171">Nombre del objeto; sirve como parte de la clave de objeto.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-171">The name of the object; serves as a part of the object key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fe8e-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fe8e-172">Remarks</span></span>

<span data-ttu-id="2fe8e-173">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-173">WMI does not implement this class.</span></span>

<span data-ttu-id="2fe8e-174">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-174">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2fe8e-175">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2fe8e-175">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fe8e-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fe8e-176">Requirements</span></span>



| <span data-ttu-id="2fe8e-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fe8e-177">Requirement</span></span> | <span data-ttu-id="2fe8e-178">Value</span><span class="sxs-lookup"><span data-stu-id="2fe8e-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fe8e-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fe8e-179">Minimum supported client</span></span><br/> | <span data-ttu-id="2fe8e-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fe8e-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2fe8e-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fe8e-181">Minimum supported server</span></span><br/> | <span data-ttu-id="2fe8e-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fe8e-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2fe8e-183">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2fe8e-183">Namespace</span></span><br/>                | <span data-ttu-id="2fe8e-184">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2fe8e-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2fe8e-185">MOF</span><span class="sxs-lookup"><span data-stu-id="2fe8e-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fe8e-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fe8e-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fe8e-187">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2fe8e-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fe8e-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fe8e-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fe8e-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fe8e-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fe8e-190">**\_PHYSICALCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="2fe8e-190">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> </dl>

 

