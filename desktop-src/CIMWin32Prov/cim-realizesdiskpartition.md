---
description: La \_ clase CIM RealizesDiskPartition representa una partición de disco en un medio físico que modela la creación de particiones en una unidad SCSI o IDE sin procesar.
ms.assetid: cc317f7d-06cd-4126-8123-6a3eb32f792e
ms.tgt_platform: multiple
title: CIM_RealizesDiskPartition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesDiskPartition
- CIM_RealizesDiskPartition.Dependent
- CIM_RealizesDiskPartition.Antecedent
- CIM_RealizesDiskPartition.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d138aafd179f5fefa40896fe4b9e6a0426b34422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153052"
---
# <a name="cim_realizesdiskpartition-class"></a><span data-ttu-id="5969d-103">\_Clase RealizesDiskPartition de CIM</span><span class="sxs-lookup"><span data-stu-id="5969d-103">CIM\_RealizesDiskPartition class</span></span>

<span data-ttu-id="5969d-104">La clase **CIM \_ RealizesDiskPartition** representa una partición de disco en un medio físico que modela la creación de particiones en una unidad SCSI o IDE sin procesar.</span><span class="sxs-lookup"><span data-stu-id="5969d-104">The **CIM\_RealizesDiskPartition** class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5969d-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="5969d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5969d-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5969d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5969d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5969d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5969d-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5969d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5969d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5969d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B80-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesDiskPartition : CIM_Realizes
{
  CIM_DiskPartition REF Dependent;
  CIM_PhysicalMedia REF Antecedent;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="5969d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="5969d-110">Members</span></span>

<span data-ttu-id="5969d-111">La clase **CIM \_ RealizesDiskPartition** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5969d-111">The **CIM\_RealizesDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="5969d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5969d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5969d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5969d-113">Properties</span></span>

<span data-ttu-id="5969d-114">La clase **CIM \_ RealizesDiskPartition** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5969d-114">The **CIM\_RealizesDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5969d-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5969d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5969d-116">Tipo de datos: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="5969d-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="5969d-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5969d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5969d-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="5969d-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="5969d-119">[**\_ PhysicalMedia CIM**](cim-physicalmedia.md) que describe el medio físico en el que se realiza la extensión.</span><span class="sxs-lookup"><span data-stu-id="5969d-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="5969d-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="5969d-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5969d-121">Tipo de datos: **CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="5969d-121">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="5969d-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5969d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5969d-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="5969d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5969d-124">Un [**\_ DiskPartition de CIM**](cim-diskpartition.md) que describe la partición de disco que se encuentra en el medio.</span><span class="sxs-lookup"><span data-stu-id="5969d-124">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="5969d-125">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="5969d-125">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5969d-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5969d-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5969d-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5969d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5969d-128">Dirección inicial del medio físico en el que comienza la partición de disco.</span><span class="sxs-lookup"><span data-stu-id="5969d-128">Starting address on the physical media where the disk partition begins.</span></span> <span data-ttu-id="5969d-129">La dirección final de la partición se determina mediante las propiedades **NumberOfBlocks** y **blocksize** del objeto [**\_ DiskPartition de CIM**](cim-diskpartition.md) .</span><span class="sxs-lookup"><span data-stu-id="5969d-129">The partition's ending address is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_DiskPartition**](cim-diskpartition.md) object.</span></span>

<span data-ttu-id="5969d-130">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5969d-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5969d-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5969d-131">Remarks</span></span>

<span data-ttu-id="5969d-132">La clase **CIM \_ RealizesDiskPartition** se deriva de las contrataciones de [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="5969d-132">The **CIM\_RealizesDiskPartition** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="5969d-133">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="5969d-133">WMI does not implement this class.</span></span>

<span data-ttu-id="5969d-134">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="5969d-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5969d-135">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="5969d-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5969d-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5969d-136">Requirements</span></span>



| <span data-ttu-id="5969d-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="5969d-137">Requirement</span></span> | <span data-ttu-id="5969d-138">Value</span><span class="sxs-lookup"><span data-stu-id="5969d-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5969d-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5969d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5969d-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5969d-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5969d-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5969d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5969d-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5969d-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5969d-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5969d-143">Namespace</span></span><br/>                | <span data-ttu-id="5969d-144">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5969d-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5969d-145">MOF</span><span class="sxs-lookup"><span data-stu-id="5969d-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5969d-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5969d-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5969d-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5969d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5969d-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5969d-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5969d-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="5969d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5969d-150">**Contrataciones \_ de CIM**</span><span class="sxs-lookup"><span data-stu-id="5969d-150">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

