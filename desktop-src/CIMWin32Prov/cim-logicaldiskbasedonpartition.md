---
description: La \_ clase LogicalDiskBasedOnPartition de CIM asocia un disco lógico a la partición de disco en la que reside.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: CIM_LogicalDiskBasedOnPartition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67aac7ae8d295bd6d98e06e0ebb8135d3330f52f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538505"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a><span data-ttu-id="1e2e0-103">\_Clase LogicalDiskBasedOnPartition de CIM</span><span class="sxs-lookup"><span data-stu-id="1e2e0-103">CIM\_LogicalDiskBasedOnPartition class</span></span>

<span data-ttu-id="1e2e0-104">La **clase \_ LogicalDiskBasedOnPartition de CIM** asocia un disco lógico a la partición de disco en la que reside.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-104">The **CIM\_LogicalDiskBasedOnPartition** class associates a logical disk with the disk partition on which it resides.</span></span>

<span data-ttu-id="1e2e0-105">Por ejemplo, la unidad C de un equipo puede encontrarse en una partición en un medio físico local, lo que indica que un disco lógico no puede abarcar más de una partición.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-105">For example, a computer's drive C can be located on a partition on local physical media, which dictates that a logical disk cannot span more than one partition.</span></span> <span data-ttu-id="1e2e0-106">Sin embargo, cuando un disco lógico puede abarcar más de una partición, el disco lógico se basa en la configuración de RAID (por ejemplo, un conjunto de espejos o de bandas).</span><span class="sxs-lookup"><span data-stu-id="1e2e0-106">When a logical disk can span more than one partition, however, the logical disk is based on RAID configuration (for example, a mirror or stripe set).</span></span> <span data-ttu-id="1e2e0-107">En ese caso, el disco lógico se basa en el volumen de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-107">In which case, the logical disk is based on storage volume.</span></span> <span data-ttu-id="1e2e0-108">Para evitar el uso incorrecto de la Asociación **\_ LogicalDiskBasedOnPartition de CIM** , se colocó el calificador **Max (1)** en la referencia **antecedente** a la partición de disco.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-108">To prevent using the **CIM\_LogicalDiskBasedOnPartition** association incorrectly, the **Max(1)** qualifier was put on the **Antecedent** reference to the disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e2e0-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1e2e0-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1e2e0-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1e2e0-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1e2e0-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2e0-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e2e0-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="1e2e0-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e2e0-114">Members</span></span>

<span data-ttu-id="1e2e0-115">La clase **CIM \_ LogicalDiskBasedOnPartition** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1e2e0-115">The **CIM\_LogicalDiskBasedOnPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="1e2e0-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e2e0-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e2e0-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e2e0-117">Properties</span></span>

<span data-ttu-id="1e2e0-118">La clase **CIM \_ LogicalDiskBasedOnPartition** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-118">The **CIM\_LogicalDiskBasedOnPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e2e0-119">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="1e2e0-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2e0-120">Tipo de datos: **CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="1e2e0-120">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="1e2e0-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e2e0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e2e0-122">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="1e2e0-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1e2e0-123">Un [**\_ DiskPartition de CIM**](cim-diskpartition.md) que describe la partición del disco.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-123">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition.</span></span>

</dd> <dt>

<span data-ttu-id="1e2e0-124">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="1e2e0-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2e0-125">Tipo de datos: **CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="1e2e0-125">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="1e2e0-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e2e0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e2e0-127">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="1e2e0-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1e2e0-128">Un [**\_ LogicalDisk de CIM**](cim-logicaldisk.md) que describe el disco lógico que se basa en la partición.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-128">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="1e2e0-129">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="1e2e0-129">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2e0-130">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e2e0-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e2e0-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e2e0-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e2e0-132">Indica el final de la extensión de alto nivel en el almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-132">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="1e2e0-133">Esta propiedad es útil cuando se asignan extensiones no contiguas a una agrupación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-133">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="1e2e0-134">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1e2e0-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="1e2e0-135">Esta propiedad se hereda de [**\_ BasedOn CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="1e2e0-135">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e2e0-136">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="1e2e0-136">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2e0-137">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e2e0-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e2e0-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e2e0-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e2e0-139">Indica el principio de la extensión de alto nivel en el almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-139">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="1e2e0-140">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1e2e0-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="1e2e0-141">Esta propiedad se hereda de [**\_ BasedOn CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="1e2e0-141">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e2e0-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e2e0-142">Remarks</span></span>

<span data-ttu-id="1e2e0-143">La clase **CIM \_ LogicalDiskBasedOnPartition** se deriva de [**la \_ BasedOn CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="1e2e0-143">The **CIM\_LogicalDiskBasedOnPartition** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="1e2e0-144">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-144">WMI does not implement this class.</span></span> <span data-ttu-id="1e2e0-145">Para las clases derivadas de **CIM \_ LogicalDiskBasedOnPartition**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1e2e0-145">For classes derived from **CIM\_LogicalDiskBasedOnPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1e2e0-146">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1e2e0-147">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e2e0-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e2e0-148">Requirements</span></span>



| <span data-ttu-id="1e2e0-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e2e0-149">Requirement</span></span> | <span data-ttu-id="1e2e0-150">Value</span><span class="sxs-lookup"><span data-stu-id="1e2e0-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2e0-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e2e0-151">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2e0-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e2e0-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e2e0-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e2e0-153">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2e0-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e2e0-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e2e0-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1e2e0-155">Namespace</span></span><br/>                | <span data-ttu-id="1e2e0-156">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1e2e0-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1e2e0-157">MOF</span><span class="sxs-lookup"><span data-stu-id="1e2e0-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e2e0-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e2e0-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e2e0-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e2e0-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e2e0-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e2e0-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e2e0-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e2e0-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e2e0-162">**\_BasedOn CIM**</span><span class="sxs-lookup"><span data-stu-id="1e2e0-162">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

