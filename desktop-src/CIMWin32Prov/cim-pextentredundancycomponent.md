---
description: La \_ clase CIM PExtentRedundancyComponent representa las extensiones físicas que participan en un grupo de redundancia de almacenamiento.
ms.assetid: 5a4bb1e8-7b99-410a-bba5-2c63beabd00e
ms.tgt_platform: multiple
title: CIM_PExtentRedundancyComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PExtentRedundancyComponent
- CIM_PExtentRedundancyComponent.PartComponent
- CIM_PExtentRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb2b6a88a789e93ca45f8469e0e67449e3473ddc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495953"
---
# <a name="cim_pextentredundancycomponent-class"></a><span data-ttu-id="cd93f-103">\_Clase PExtentRedundancyComponent de CIM</span><span class="sxs-lookup"><span data-stu-id="cd93f-103">CIM\_PExtentRedundancyComponent class</span></span>

<span data-ttu-id="cd93f-104">La clase **CIM \_ PExtentRedundancyComponent** representa las extensiones físicas que participan en un grupo de redundancia de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="cd93f-104">The **CIM\_PExtentRedundancyComponent** class represents the physical extents that participate in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd93f-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="cd93f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cd93f-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cd93f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cd93f-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cd93f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cd93f-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="cd93f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd93f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd93f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{AD3C1FA2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_PExtentRedundancyComponent : CIM_RedundancyComponent
{
  CIM_PhysicalExtent         REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="cd93f-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd93f-110">Members</span></span>

<span data-ttu-id="cd93f-111">La clase **CIM \_ PExtentRedundancyComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cd93f-111">The **CIM\_PExtentRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="cd93f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd93f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd93f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd93f-113">Properties</span></span>

<span data-ttu-id="cd93f-114">La clase **CIM \_ PExtentRedundancyComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd93f-114">The **CIM\_PExtentRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd93f-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="cd93f-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd93f-116">Tipo de datos: **CIM \_ StorageRedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="cd93f-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="cd93f-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd93f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd93f-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="cd93f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="cd93f-119">Un [**\_ StorageRedundancyGroup de CIM**](cim-storageredundancygroup.md) que describe el grupo de redundancia de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="cd93f-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that describes the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="cd93f-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cd93f-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd93f-121">Tipo de datos: **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="cd93f-121">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="cd93f-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd93f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd93f-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="cd93f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="cd93f-124">[**\_ PhysicalExtent CIM**](cim-physicalextent.md) que describe la extensión física que participa en el grupo de redundancia.</span><span class="sxs-lookup"><span data-stu-id="cd93f-124">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd93f-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd93f-125">Remarks</span></span>

<span data-ttu-id="cd93f-126">La clase **CIM \_ PExtentRedundancyComponent** se deriva de [**\_ RedundancyComponent de CIM**](cim-redundancycomponent.md).</span><span class="sxs-lookup"><span data-stu-id="cd93f-126">The **CIM\_PExtentRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="cd93f-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="cd93f-127">WMI does not implement this class.</span></span>

<span data-ttu-id="cd93f-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="cd93f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cd93f-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="cd93f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd93f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd93f-130">Requirements</span></span>



| <span data-ttu-id="cd93f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd93f-131">Requirement</span></span> | <span data-ttu-id="cd93f-132">Value</span><span class="sxs-lookup"><span data-stu-id="cd93f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd93f-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd93f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cd93f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd93f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd93f-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd93f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cd93f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd93f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd93f-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cd93f-137">Namespace</span></span><br/>                | <span data-ttu-id="cd93f-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cd93f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd93f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="cd93f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd93f-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd93f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd93f-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd93f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd93f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd93f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd93f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd93f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd93f-144">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="cd93f-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

