---
description: La \_ Asociación RealizesPExtent de CIM representa la relación en la que se realizan las extensiones físicas en un medio físico. Además, se especifica la dirección inicial de la extensión física en el medio físico.
ms.assetid: 9abe1a7d-8463-4d48-8cec-52bf934ad08b
ms.tgt_platform: multiple
title: CIM_RealizesPExtent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesPExtent
- CIM_RealizesPExtent.Dependent
- CIM_RealizesPExtent.Antecedent
- CIM_RealizesPExtent.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 906861c7bc7a7e09d40d3457d069cdb9dd3a6b11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659517"
---
# <a name="cim_realizespextent-class"></a><span data-ttu-id="f017d-104">\_Clase RealizesPExtent de CIM</span><span class="sxs-lookup"><span data-stu-id="f017d-104">CIM\_RealizesPExtent class</span></span>

<span data-ttu-id="f017d-105">La **Asociación \_ RealizesPExtent de CIM** representa la relación en la que se realizan las extensiones físicas en un medio físico.</span><span class="sxs-lookup"><span data-stu-id="f017d-105">The **CIM\_RealizesPExtent** association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="f017d-106">Además, se especifica la dirección inicial de la extensión física en el medio físico.</span><span class="sxs-lookup"><span data-stu-id="f017d-106">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f017d-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f017d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f017d-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f017d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f017d-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f017d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f017d-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f017d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f017d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f017d-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesPExtent : CIM_Realizes
{
  CIM_PhysicalExtent REF Dependent;
  CIM_PhysicalMedia  REF Antecedent;
  uint64                 StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="f017d-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="f017d-112">Members</span></span>

<span data-ttu-id="f017d-113">La clase **CIM \_ RealizesPExtent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f017d-113">The **CIM\_RealizesPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="f017d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f017d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f017d-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f017d-115">Properties</span></span>

<span data-ttu-id="f017d-116">La clase **CIM \_ RealizesPExtent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f017d-116">The **CIM\_RealizesPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f017d-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f017d-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f017d-118">Tipo de datos: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="f017d-118">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="f017d-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f017d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f017d-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f017d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f017d-121">[**\_ PhysicalMedia CIM**](cim-physicalmedia.md) que describe el medio físico en el que se realiza la extensión.</span><span class="sxs-lookup"><span data-stu-id="f017d-121">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="f017d-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="f017d-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f017d-123">Tipo de datos: **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="f017d-123">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="f017d-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f017d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f017d-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="f017d-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f017d-126">[**\_ PhysicalExtent CIM**](cim-physicalextent.md) que describe la extensión física que se encuentra en el medio.</span><span class="sxs-lookup"><span data-stu-id="f017d-126">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="f017d-127">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="f017d-127">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f017d-128">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f017d-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f017d-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f017d-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f017d-130">Dirección inicial en el medio físico en el que comienza la extensión física.</span><span class="sxs-lookup"><span data-stu-id="f017d-130">Starting address on the physical media where the physical extent begins.</span></span> <span data-ttu-id="f017d-131">La dirección final de la extensión física se determina mediante las propiedades **NumberOfBlocks** y **blocksize** del objeto [**\_ PhysicalExtent de CIM**](cim-physicalextent.md) .</span><span class="sxs-lookup"><span data-stu-id="f017d-131">The ending address of the physical extent is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_PhysicalExtent**](cim-physicalextent.md) object.</span></span>

<span data-ttu-id="f017d-132">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f017d-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f017d-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f017d-133">Remarks</span></span>

<span data-ttu-id="f017d-134">La clase **CIM \_ RealizesPExtent** se deriva de las contrataciones de [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="f017d-134">The **CIM\_RealizesPExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="f017d-135">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="f017d-135">WMI does not implement this class.</span></span>

<span data-ttu-id="f017d-136">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f017d-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f017d-137">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f017d-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f017d-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f017d-138">Requirements</span></span>



| <span data-ttu-id="f017d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f017d-139">Requirement</span></span> | <span data-ttu-id="f017d-140">Value</span><span class="sxs-lookup"><span data-stu-id="f017d-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f017d-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f017d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f017d-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f017d-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f017d-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f017d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f017d-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f017d-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f017d-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f017d-145">Namespace</span></span><br/>                | <span data-ttu-id="f017d-146">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f017d-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f017d-147">MOF</span><span class="sxs-lookup"><span data-stu-id="f017d-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f017d-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f017d-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f017d-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f017d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f017d-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f017d-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f017d-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="f017d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f017d-152">**Contrataciones \_ de CIM**</span><span class="sxs-lookup"><span data-stu-id="f017d-152">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

