---
description: Describe las capacidades y la administración de los medios que almacenan datos y permite la recuperación de los datos. Esta superclase se utiliza para representar componentes RAID de software y hardware, o una extensión lógica sin procesar de medios físicos.
ms.assetid: 29d105fb-8c34-4824-8679-883aef02a0c9
title: CIM_StorageExtent (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent
- CIM_StorageExtent.DataOrganization
- CIM_StorageExtent.Purpose
- CIM_StorageExtent.Access
- CIM_StorageExtent.ErrorMethodology
- CIM_StorageExtent.BlockSize
- CIM_StorageExtent.NumberOfBlocks
- CIM_StorageExtent.ConsumableBlocks
- CIM_StorageExtent.IsBasedOnUnderlyingRedundancy
- CIM_StorageExtent.SequentialAccess
- CIM_StorageExtent.ExtentStatus
- CIM_StorageExtent.NoSinglePointOfFailure
- CIM_StorageExtent.DataRedundancy
- CIM_StorageExtent.PackageRedundancy
- CIM_StorageExtent.DeltaReservation
- CIM_StorageExtent.Primordial
- CIM_StorageExtent.Name
- CIM_StorageExtent.NameFormat
- CIM_StorageExtent.NameNamespace
- CIM_StorageExtent.OtherNameNamespace
- CIM_StorageExtent.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a3dc1b58dd97582e229497e754d10c3f307eab76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687522"
---
# <a name="cim_storageextent-class-hyper-v-management"></a><span data-ttu-id="03e0d-104">CIM_StorageExtent (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="03e0d-104">CIM_StorageExtent class (Hyper-V management)</span></span>

<span data-ttu-id="03e0d-105">Describe las capacidades y la administración de los medios que almacenan datos y permite la recuperación de los datos.</span><span class="sxs-lookup"><span data-stu-id="03e0d-105">Describes the capabilities and management of media that stores data and allows retrieval of the data.</span></span> <span data-ttu-id="03e0d-106">Esta superclase se utiliza para representar componentes RAID de software y hardware, o una extensión lógica sin procesar de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="03e0d-106">This super class is used to represent software and hardware RAID components, or a raw logical extent of physical media.</span></span>

## <a name="syntax"></a><span data-ttu-id="03e0d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03e0d-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.13.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_StorageExtent : CIM_LogicalDevice
{
  uint16  DataOrganization;
  string  Purpose;
  uint16  Access;
  string  ErrorMethodology;
  uint64  BlockSize;
  uint64  NumberOfBlocks;
  uint64  ConsumableBlocks;
  boolean IsBasedOnUnderlyingRedundancy;
  boolean SequentialAccess;
  uint16  ExtentStatus[];
  boolean NoSinglePointOfFailure;
  uint16  DataRedundancy;
  uint16  PackageRedundancy;
  uint8   DeltaReservation;
  boolean Primordial = FALSE;
  string  Name;
  uint16  NameFormat;
  uint16  NameNamespace;
  string  OtherNameNamespace;
  string  OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="03e0d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="03e0d-108">Members</span></span>

<span data-ttu-id="03e0d-109">La clase **CIM \_ StorageExtent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="03e0d-109">The **CIM\_StorageExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="03e0d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03e0d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03e0d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03e0d-111">Properties</span></span>

<span data-ttu-id="03e0d-112">La clase **CIM \_ StorageExtent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="03e0d-112">The **CIM\_StorageExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03e0d-113">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="03e0d-113">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03e0d-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-116">Una descripción de la compatibilidad de lectura y escritura de los medios.</span><span class="sxs-lookup"><span data-stu-id="03e0d-116">A description of the read/write support of the media.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03e0d-117">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="03e0d-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="03e0d-118">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="03e0d-118">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="03e0d-119">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="03e0d-119">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="03e0d-120">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="03e0d-120">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="03e0d-121">**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="03e0d-121">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03e0d-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="03e0d-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-123">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03e0d-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-125">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Almacenamiento de host DMTF \| 001,4 "," MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="03e0d-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.4", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits", "MIF.DMTF\|Storage Devices\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-126">Tamaño, en bytes, de los bloques que forman la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="03e0d-126">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="03e0d-127">Si se usan tamaños de bloque variable, esta propiedad debe especificar el tamaño máximo del bloque.</span><span class="sxs-lookup"><span data-stu-id="03e0d-127">If variable block sizes are used, then this property should specify the maximum block size.</span></span> <span data-ttu-id="03e0d-128">Si el tamaño de bloque es desconocido o si un concepto de bloque no es válido (por ejemplo, para **\_ AggregateExtent de CIM**, [**\_ memoria de CIM**](cim-memory.md) o [**\_ LogicalDisk de CIM**](cim-logicaldisk.md)), esta propiedad debe establecerse en "1" (desconocido).</span><span class="sxs-lookup"><span data-stu-id="03e0d-128">If the block size is unknown or if a block concept is not valid (for example, for **CIM\_AggregateExtent**, [**CIM\_Memory**](cim-memory.md) or [**CIM\_LogicalDisk**](cim-logicaldisk.md)), then this property should be set to "1" (unknow).</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-129">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="03e0d-129">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-130">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03e0d-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-132">Número máximo de bloques que están disponibles para su uso al encapar **\_ StorageExtent CIM** mediante la Asociación de clase [**\_ basada en CIM**](cim-basedon.md) .</span><span class="sxs-lookup"><span data-stu-id="03e0d-132">The maximum number of blocks, that are available for use when layering **CIM\_StorageExtent** using the [**CIM\_BasedOn**](cim-basedon.md) class association.</span></span> <span data-ttu-id="03e0d-133">Esta propiedad solo tiene significado cuando se hace referencia a la extensión de almacenamiento en la propiedad **antecedente** de un objeto **\_ basado en CIM** .</span><span class="sxs-lookup"><span data-stu-id="03e0d-133">This property only has meaning when the storage extent is referenced in the **Antecedent** property in a **CIM\_BasedOn** object.</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-134">**Organización de los mismos**</span><span class="sxs-lookup"><span data-stu-id="03e0d-134">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03e0d-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-137">Tipo de organización de datos utilizada por los medios.</span><span class="sxs-lookup"><span data-stu-id="03e0d-137">The type of data organization used by the media.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03e0d-138">**Otro** (0)</span><span class="sxs-lookup"><span data-stu-id="03e0d-138">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03e0d-139">**Desconocido** (1)</span><span class="sxs-lookup"><span data-stu-id="03e0d-139">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Block"></span><span id="fixed_block"></span><span id="FIXED_BLOCK"></span>

<span data-ttu-id="03e0d-140">**Bloque fijo** (2)</span><span class="sxs-lookup"><span data-stu-id="03e0d-140">**Fixed Block** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable_Block"></span><span id="variable_block"></span><span id="VARIABLE_BLOCK"></span>

<span data-ttu-id="03e0d-141">**Bloque de variables** (3)</span><span class="sxs-lookup"><span data-stu-id="03e0d-141">**Variable Block** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Count_Key_Data"></span><span id="count_key_data"></span><span id="COUNT_KEY_DATA"></span>

<span data-ttu-id="03e0d-142">**Datos de clave de recuento** (4)</span><span class="sxs-lookup"><span data-stu-id="03e0d-142">**Count Key Data** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03e0d-143">**Redundancia de los mismos**</span><span class="sxs-lookup"><span data-stu-id="03e0d-143">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03e0d-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-146">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**","**\_ StorageSetting CIM**.**DataRedundancyMax**","**\_ StorageSetting CIM**.**DataRedundancyMin**")</span><span class="sxs-lookup"><span data-stu-id="03e0d-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**", "**CIM\_StorageSetting**.**DataRedundancyMax**", "**CIM\_StorageSetting**.**DataRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-147">El número de copias completas de los datos que se mantienen actualmente.</span><span class="sxs-lookup"><span data-stu-id="03e0d-147">The number of complete copies of data that are currently maintained.</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-148">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="03e0d-148">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-149">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="03e0d-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-151">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percentage"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ StorageSetting CIM**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**","**\_ StorageSetting CIM**.**DeltaReservationMax**","**\_ StorageSetting CIM**.**DeltaReservationMin**")</span><span class="sxs-lookup"><span data-stu-id="03e0d-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percentage"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**", "**CIM\_StorageSetting**.**DeltaReservationMax**", "**CIM\_StorageSetting**.**DeltaReservationMin**")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-152">Valor actual para la reserva Delta.</span><span class="sxs-lookup"><span data-stu-id="03e0d-152">The current value for delta reservation.</span></span> <span data-ttu-id="03e0d-153">Se trata de un porcentaje que especifica la cantidad de espacio que se debe reservar en una réplica para almacenar en caché los cambios.</span><span class="sxs-lookup"><span data-stu-id="03e0d-153">This is a percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-154">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="03e0d-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03e0d-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-157">El tipo de detección y corrección de errores admitidos por la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="03e0d-157">The type of error detection and correction supported by the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-158">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="03e0d-158">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-159">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03e0d-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-161">Información de estado adicional.</span><span class="sxs-lookup"><span data-stu-id="03e0d-161">Additional status information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03e0d-162">**Otro** (0)</span><span class="sxs-lookup"><span data-stu-id="03e0d-162">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03e0d-163">**Desconocido** (1)</span><span class="sxs-lookup"><span data-stu-id="03e0d-163">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None_Not_Applicable"></span><span id="none_not_applicable"></span><span id="NONE_NOT_APPLICABLE"></span>

<span data-ttu-id="03e0d-164">**Ninguno/no aplicable** (2)</span><span class="sxs-lookup"><span data-stu-id="03e0d-164">**None/Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broken"></span><span id="broken"></span><span id="BROKEN"></span>

<span data-ttu-id="03e0d-165">**Roto** (3)</span><span class="sxs-lookup"><span data-stu-id="03e0d-165">**Broken** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Lost"></span><span id="data_lost"></span><span id="DATA_LOST"></span>

<span data-ttu-id="03e0d-166">**Datos perdidos** (4)</span><span class="sxs-lookup"><span data-stu-id="03e0d-166">**Data Lost** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Reconfig"></span><span id="dynamic_reconfig"></span><span id="DYNAMIC_RECONFIG"></span>

<span data-ttu-id="03e0d-167">**Reconfiguración dinámica** (5)</span><span class="sxs-lookup"><span data-stu-id="03e0d-167">**Dynamic Reconfig** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Exposed"></span><span id="exposed"></span><span id="EXPOSED"></span>

<span data-ttu-id="03e0d-168">**Expuesto** (6)</span><span class="sxs-lookup"><span data-stu-id="03e0d-168">**Exposed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Fractionally_Exposed"></span><span id="fractionally_exposed"></span><span id="FRACTIONALLY_EXPOSED"></span>

<span data-ttu-id="03e0d-169">De **exposición fraccionada** (7)</span><span class="sxs-lookup"><span data-stu-id="03e0d-169">**Fractionally Exposed** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Exposed"></span><span id="partially_exposed"></span><span id="PARTIALLY_EXPOSED"></span>

<span data-ttu-id="03e0d-170">**Parcialmente expuesto** (8)</span><span class="sxs-lookup"><span data-stu-id="03e0d-170">**Partially Exposed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Disabled"></span><span id="protection_disabled"></span><span id="PROTECTION_DISABLED"></span>

<span data-ttu-id="03e0d-171">**Protección deshabilitada** (9)</span><span class="sxs-lookup"><span data-stu-id="03e0d-171">**Protection Disabled** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Readying"></span><span id="readying"></span><span id="READYING"></span>

<span data-ttu-id="03e0d-172">**Preparado** (10)</span><span class="sxs-lookup"><span data-stu-id="03e0d-172">**Readying** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Rebuild"></span><span id="rebuild"></span><span id="REBUILD"></span>

<span data-ttu-id="03e0d-173">**Volver a generar** (11)</span><span class="sxs-lookup"><span data-stu-id="03e0d-173">**Rebuild** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Recalculate"></span><span id="recalculate"></span><span id="RECALCULATE"></span>

<span data-ttu-id="03e0d-174">**Recalcular** (12)</span><span class="sxs-lookup"><span data-stu-id="03e0d-174">**Recalculate** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Spare_in_Use"></span><span id="spare_in_use"></span><span id="SPARE_IN_USE"></span>

<span data-ttu-id="03e0d-175">**Repuesto en uso** (13)</span><span class="sxs-lookup"><span data-stu-id="03e0d-175">**Spare in Use** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Verify_In_Progress"></span><span id="verify_in_progress"></span><span id="VERIFY_IN_PROGRESS"></span>

<span data-ttu-id="03e0d-176">**Comprobar en curso** (14)</span><span class="sxs-lookup"><span data-stu-id="03e0d-176">**Verify In Progress** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="In-Band_Access_Granted"></span><span id="in-band_access_granted"></span><span id="IN-BAND_ACCESS_GRANTED"></span>

<span data-ttu-id="03e0d-177">**Acceso en banda concedido** (15)</span><span class="sxs-lookup"><span data-stu-id="03e0d-177">**In-Band Access Granted** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Imported"></span><span id="imported"></span><span id="IMPORTED"></span>

<span data-ttu-id="03e0d-178">**Importado** (16)</span><span class="sxs-lookup"><span data-stu-id="03e0d-178">**Imported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Exported"></span><span id="exported"></span><span id="EXPORTED"></span>

<span data-ttu-id="03e0d-179">**Exportado** (17)</span><span class="sxs-lookup"><span data-stu-id="03e0d-179">**Exported** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="03e0d-180">**DMTF reservado** (18.. 32767)</span><span class="sxs-lookup"><span data-stu-id="03e0d-180">**DMTF Reserved** (18..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="03e0d-181">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="03e0d-181">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03e0d-182">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="03e0d-182">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-183">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03e0d-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-185">**true** si las extensiones de almacenamiento subyacentes son miembros de [**un \_ StorageRedundancyGroup CIM**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="03e0d-185">**true** if the underlying storage extents are members of a [**CIM\_StorageRedundancyGroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-186">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="03e0d-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03e0d-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-189">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCITS-T10 \| VPD 83, identificador 0 de asociación \| "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**","**CIM \_ StorageExtent**.**NameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="03e0d-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**", "**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-190">Identificador único para la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="03e0d-190">A unique identifier for the storage extent.</span></span> <span data-ttu-id="03e0d-191">La propiedad **NameFormat** especifica el formato de nombre que se va a usar en la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="03e0d-191">The **NameFormat** property specifies the naming format to use in the **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-192">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="03e0d-192">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-193">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03e0d-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-195">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Name**","**CIM \_ StorageExtent**.**NameNamespace**","**\_ StorageExtent CIM**.**OtherNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="03e0d-195">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**NameNamespace**", "**CIM\_StorageExtent**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-196">El formato de nombre de la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="03e0d-196">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03e0d-197">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="03e0d-197">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03e0d-198">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="03e0d-198">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA6"></span><span id="vpd83naa6"></span>

<span data-ttu-id="03e0d-199">**VPD83NAA6** (2)</span><span class="sxs-lookup"><span data-stu-id="03e0d-199">**VPD83NAA6** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA5"></span><span id="vpd83naa5"></span>

<span data-ttu-id="03e0d-200">**VPD83NAA5** (3)</span><span class="sxs-lookup"><span data-stu-id="03e0d-200">**VPD83NAA5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="03e0d-201">**VPD83Type2** (4)</span><span class="sxs-lookup"><span data-stu-id="03e0d-201">**VPD83Type2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="03e0d-202">**VPD83Type1** (5)</span><span class="sxs-lookup"><span data-stu-id="03e0d-202">**VPD83Type1** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type0"></span><span id="vpd83type0"></span><span id="VPD83TYPE0"></span>

<span data-ttu-id="03e0d-203">**VPD83Type0** (6)</span><span class="sxs-lookup"><span data-stu-id="03e0d-203">**VPD83Type0** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="03e0d-204">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="03e0d-204">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="03e0d-205">**NodeWWN** (8)</span><span class="sxs-lookup"><span data-stu-id="03e0d-205">**NodeWWN** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="03e0d-206">**NAA** (9)</span><span class="sxs-lookup"><span data-stu-id="03e0d-206">**NAA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="03e0d-207">**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="03e0d-207">**EUI64** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="03e0d-208">**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="03e0d-208">**T10VID** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="03e0d-209">**Nombre del dispositivo de SO** (12)</span><span class="sxs-lookup"><span data-stu-id="03e0d-209">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03e0d-210">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="03e0d-210">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-211">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03e0d-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-213">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCITS-T10 \| VPD 83, identificador 0 de asociación \| "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Name**","**CIM \_ StorageExtent**.**OtherNameNamespace**","**\_ StorageExtent CIM**.**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="03e0d-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**OtherNameNamespace**", "**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-214">Espacio de nombres de la propiedad Name.</span><span class="sxs-lookup"><span data-stu-id="03e0d-214">The namespace of the name property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03e0d-215">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="03e0d-215">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03e0d-216">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="03e0d-216">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="03e0d-217">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="03e0d-217">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="03e0d-218">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="03e0d-218">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="03e0d-219">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="03e0d-219">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="03e0d-220">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="03e0d-220">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="03e0d-221">**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="03e0d-221">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="03e0d-222">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="03e0d-222">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="03e0d-223">**Espacio de nombres de dispositivo de SO** (8)</span><span class="sxs-lookup"><span data-stu-id="03e0d-223">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03e0d-224">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="03e0d-224">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-225">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03e0d-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-227">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")</span><span class="sxs-lookup"><span data-stu-id="03e0d-227">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-228">**true** si no hay ningún punto único de error; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="03e0d-228">**true** if there are not any single points of failure; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-229">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="03e0d-229">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-230">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03e0d-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-232">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Almacenamiento de host DMTF \| 001,5 "," MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="03e0d-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-233">El número total de bloques contiguos lógicamente que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="03e0d-233">The total number of logically contiguous blocks that form the storage extent.</span></span> <span data-ttu-id="03e0d-234">El tamaño total de la extensión de almacenamiento se calcula multiplicando **blocksize** por **NumberOfBlocks**.</span><span class="sxs-lookup"><span data-stu-id="03e0d-234">The total size of the storage extent is calculated by multiplying **BlockSize** by **NumberOfBlocks**.</span></span> <span data-ttu-id="03e0d-235">Si el **blocksize** es "1", esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="03e0d-235">If the **BlockSize** is "1", this property is the total size of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-236">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="03e0d-236">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03e0d-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-239">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="03e0d-239">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-240">El formato de la propiedad **Name** cuando la propiedad **NameFormat** está establecida en "1" (otra).</span><span class="sxs-lookup"><span data-stu-id="03e0d-240">The format of the **Name** property when the **NameFormat** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-241">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="03e0d-241">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03e0d-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-244">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="03e0d-244">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-245">Descripción del espacio de nombres de la propiedad **Name** cuando la propiedad **NameNamespace** se establece en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="03e0d-245">A description of the namespace of the **Name** property when the **NameNamespace** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-246">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="03e0d-246">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-247">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03e0d-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-249">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**","**\_ StorageSetting CIM**.**PackageRedundancyMax**","**\_ StorageSetting CIM**.**PackageRedundancyMin**")</span><span class="sxs-lookup"><span data-stu-id="03e0d-249">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**", "**CIM\_StorageSetting**.**PackageRedundancyMax**", "**CIM\_StorageSetting**.**PackageRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-250">Número actual de paquetes físicos que pueden fallar sin pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="03e0d-250">The current number of physical packages that can fail without data loss.</span></span> <span data-ttu-id="03e0d-251">Por ejemplo, en un dominio de almacenamiento, este podría ser el número de ejes de disco.</span><span class="sxs-lookup"><span data-stu-id="03e0d-251">For example, in a storage domain, this might be the number of disk spindles.</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-252">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="03e0d-252">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-253">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03e0d-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-255">**true** si la extensión de almacenamiento es primordial; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="03e0d-255">**true** if the storage extent is primordial; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-256">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="03e0d-256">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03e0d-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-259">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageDescr ")</span><span class="sxs-lookup"><span data-stu-id="03e0d-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageDescr")</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-260">Descripción del uso de medios.</span><span class="sxs-lookup"><span data-stu-id="03e0d-260">A description of the media usage.</span></span>

</dd> <dt>

<span data-ttu-id="03e0d-261">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="03e0d-261">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03e0d-262">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03e0d-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03e0d-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03e0d-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03e0d-264">**true** si un objeto [**\_ MediaAccessDevice de CIM**](cim-mediaaccessdevice.md) tiene acceso de forma secuencial al almacenamiento; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="03e0d-264">**true** if storage is sequentially accessed by a [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) object; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03e0d-265">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03e0d-265">Requirements</span></span>



| <span data-ttu-id="03e0d-266">Requisito</span><span class="sxs-lookup"><span data-stu-id="03e0d-266">Requirement</span></span> | <span data-ttu-id="03e0d-267">Value</span><span class="sxs-lookup"><span data-stu-id="03e0d-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03e0d-268">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03e0d-268">Minimum supported client</span></span><br/> | <span data-ttu-id="03e0d-269">Windows 8</span><span class="sxs-lookup"><span data-stu-id="03e0d-269">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="03e0d-270">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03e0d-270">Minimum supported server</span></span><br/> | <span data-ttu-id="03e0d-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03e0d-271">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="03e0d-272">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="03e0d-272">Namespace</span></span><br/>                | <span data-ttu-id="03e0d-273">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="03e0d-273">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="03e0d-274">MOF</span><span class="sxs-lookup"><span data-stu-id="03e0d-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03e0d-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03e0d-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03e0d-276">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03e0d-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03e0d-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03e0d-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="03e0d-278">Vea también</span><span class="sxs-lookup"><span data-stu-id="03e0d-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e0d-279">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="03e0d-279">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

