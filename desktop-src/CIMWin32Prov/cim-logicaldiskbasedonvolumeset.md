---
description: La \_ Asociación LogicalDiskBasedOnVolumeSet de CIM relaciona los discos lógicos con el volumen en el que se encuentran. Los discos lógicos pueden basarse en un único volumen (por ejemplo, expuesto por un administrador de volumen de software) o una partición de disco.
ms.assetid: 15a588c9-a6b0-4393-927f-8e8818315542
ms.tgt_platform: multiple
title: CIM_LogicalDiskBasedOnVolumeSet (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnVolumeSet
- CIM_LogicalDiskBasedOnVolumeSet.EndingAddress
- CIM_LogicalDiskBasedOnVolumeSet.StartingAddress
- CIM_LogicalDiskBasedOnVolumeSet.Dependent
- CIM_LogicalDiskBasedOnVolumeSet.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2af4c141fe0b64979c6fb6e5b7b0e6068d018d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152880"
---
# <a name="cim_logicaldiskbasedonvolumeset-class"></a><span data-ttu-id="aeafc-104">\_Clase LogicalDiskBasedOnVolumeSet de CIM</span><span class="sxs-lookup"><span data-stu-id="aeafc-104">CIM\_LogicalDiskBasedOnVolumeSet class</span></span>

<span data-ttu-id="aeafc-105">La **Asociación \_ LogicalDiskBasedOnVolumeSet de CIM** relaciona los discos lógicos con el volumen en el que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="aeafc-105">The **CIM\_LogicalDiskBasedOnVolumeSet** association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="aeafc-106">Los discos lógicos pueden basarse en un único volumen (por ejemplo, expuesto por un administrador de volumen de software) o una partición de disco.</span><span class="sxs-lookup"><span data-stu-id="aeafc-106">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aeafc-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="aeafc-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aeafc-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aeafc-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aeafc-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="aeafc-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aeafc-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="aeafc-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeafc-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aeafc-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3A608798-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LogicalDiskBasedOnVolumeSet : CIM_BasedOn
{
  uint64              EndingAddress;
  uint64              StartingAddress;
  CIM_LogicalDisk REF Dependent;
  CIM_VolumeSet   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="aeafc-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="aeafc-112">Members</span></span>

<span data-ttu-id="aeafc-113">La clase **CIM \_ LogicalDiskBasedOnVolumeSet** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aeafc-113">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="aeafc-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aeafc-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aeafc-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aeafc-115">Properties</span></span>

<span data-ttu-id="aeafc-116">La clase **CIM \_ LogicalDiskBasedOnVolumeSet** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="aeafc-116">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aeafc-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="aeafc-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeafc-118">Tipo de datos: **CIM \_ VolumeSet**</span><span class="sxs-lookup"><span data-stu-id="aeafc-118">Data type: **CIM\_VolumeSet**</span></span>
</dt> <dt>

<span data-ttu-id="aeafc-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeafc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeafc-120">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="aeafc-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="aeafc-121">Un [**\_ VolumeSet de CIM**](cim-volumeset.md) que describe el conjunto de volúmenes.</span><span class="sxs-lookup"><span data-stu-id="aeafc-121">A [**CIM\_VolumeSet**](cim-volumeset.md) that describes the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="aeafc-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="aeafc-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeafc-123">Tipo de datos: **CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="aeafc-123">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="aeafc-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeafc-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeafc-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="aeafc-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="aeafc-126">Un [**\_ LogicalDisk de CIM**](cim-logicaldisk.md) que describe el disco lógico que se basa en el conjunto de volúmenes.</span><span class="sxs-lookup"><span data-stu-id="aeafc-126">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="aeafc-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="aeafc-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeafc-128">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aeafc-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aeafc-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeafc-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aeafc-130">Indica el final de la extensión de alto nivel en el almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="aeafc-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="aeafc-131">Esta propiedad es útil cuando se asignan extensiones no contiguas a una agrupación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="aeafc-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="aeafc-132">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aeafc-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="aeafc-133">Esta propiedad se hereda de [**\_ BasedOn CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="aeafc-133">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeafc-134">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="aeafc-134">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeafc-135">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aeafc-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aeafc-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeafc-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aeafc-137">Indica el principio de la extensión de alto nivel en el almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="aeafc-137">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="aeafc-138">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aeafc-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="aeafc-139">Esta propiedad se hereda de [**\_ BasedOn CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="aeafc-139">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aeafc-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aeafc-140">Remarks</span></span>

<span data-ttu-id="aeafc-141">La clase **CIM \_ LogicalDiskBasedOnVolumeSet** se deriva de [**la \_ BasedOn CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="aeafc-141">The **CIM\_LogicalDiskBasedOnVolumeSet** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="aeafc-142">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="aeafc-142">WMI does not implement this class.</span></span>

<span data-ttu-id="aeafc-143">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="aeafc-143">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aeafc-144">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="aeafc-144">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeafc-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeafc-145">Requirements</span></span>



| <span data-ttu-id="aeafc-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeafc-146">Requirement</span></span> | <span data-ttu-id="aeafc-147">Value</span><span class="sxs-lookup"><span data-stu-id="aeafc-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeafc-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aeafc-148">Minimum supported client</span></span><br/> | <span data-ttu-id="aeafc-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aeafc-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aeafc-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aeafc-150">Minimum supported server</span></span><br/> | <span data-ttu-id="aeafc-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aeafc-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aeafc-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aeafc-152">Namespace</span></span><br/>                | <span data-ttu-id="aeafc-153">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aeafc-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aeafc-154">MOF</span><span class="sxs-lookup"><span data-stu-id="aeafc-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aeafc-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aeafc-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aeafc-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aeafc-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeafc-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeafc-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeafc-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="aeafc-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeafc-159">**\_BasedOn CIM**</span><span class="sxs-lookup"><span data-stu-id="aeafc-159">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

