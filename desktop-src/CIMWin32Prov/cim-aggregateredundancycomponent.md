---
description: La \_ clase CIM AggregateRedundancyComponent describe la extensión física agregada en un grupo de redundancia de almacenamiento.
ms.assetid: 3407e888-e17c-4f65-a33f-056002accbf7
ms.tgt_platform: multiple
title: CIM_AggregateRedundancyComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregateRedundancyComponent
- CIM_AggregateRedundancyComponent.PartComponent
- CIM_AggregateRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9a5e638730578bad8d64f35b29a5152898c23fd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807687"
---
# <a name="cim_aggregateredundancycomponent-class"></a><span data-ttu-id="552da-103">\_Clase AggregateRedundancyComponent de CIM</span><span class="sxs-lookup"><span data-stu-id="552da-103">CIM\_AggregateRedundancyComponent class</span></span>

<span data-ttu-id="552da-104">La clase **CIM \_ AggregateRedundancyComponent** describe la extensión física agregada en un grupo de redundancia de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="552da-104">The **CIM\_AggregateRedundancyComponent** class describes the aggregate physical extent in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="552da-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="552da-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="552da-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="552da-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="552da-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="552da-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="552da-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="552da-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="552da-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="552da-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{154E66D8-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AggregateRedundancyComponent : CIM_RedundancyComponent
{
  CIM_AggregatePExtent       REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="552da-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="552da-110">Members</span></span>

<span data-ttu-id="552da-111">La clase **CIM \_ AggregateRedundancyComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="552da-111">The **CIM\_AggregateRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="552da-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="552da-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="552da-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="552da-113">Properties</span></span>

<span data-ttu-id="552da-114">La clase **CIM \_ AggregateRedundancyComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="552da-114">The **CIM\_AggregateRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="552da-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="552da-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="552da-116">Tipo de datos: **CIM \_ StorageRedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="552da-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="552da-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="552da-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="552da-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="552da-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="552da-119">Un [**\_ StorageRedundancyGroup de CIM**](cim-storageredundancygroup.md) que contiene el grupo de redundancia de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="552da-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that contains the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="552da-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="552da-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="552da-121">Tipo de datos: **CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="552da-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="552da-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="552da-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="552da-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="552da-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="552da-124">Un [**\_ AggregatePExtent de CIM**](cim-aggregatepextent.md) que contiene la extensión física agregada que participa en el grupo de redundancia.</span><span class="sxs-lookup"><span data-stu-id="552da-124">A [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that contains the aggregate physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="552da-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="552da-125">Remarks</span></span>

<span data-ttu-id="552da-126">La clase **CIM \_ AggregateRedundancyComponent** se deriva de [**\_ RedundancyComponent de CIM**](cim-redundancycomponent.md).</span><span class="sxs-lookup"><span data-stu-id="552da-126">The **CIM\_AggregateRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="552da-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="552da-127">WMI does not implement this class.</span></span>

<span data-ttu-id="552da-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="552da-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="552da-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="552da-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="552da-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="552da-130">Requirements</span></span>



| <span data-ttu-id="552da-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="552da-131">Requirement</span></span> | <span data-ttu-id="552da-132">Value</span><span class="sxs-lookup"><span data-stu-id="552da-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="552da-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="552da-133">Minimum supported client</span></span><br/> | <span data-ttu-id="552da-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="552da-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="552da-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="552da-135">Minimum supported server</span></span><br/> | <span data-ttu-id="552da-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="552da-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="552da-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="552da-137">Namespace</span></span><br/>                | <span data-ttu-id="552da-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="552da-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="552da-139">MOF</span><span class="sxs-lookup"><span data-stu-id="552da-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="552da-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="552da-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="552da-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="552da-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="552da-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="552da-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="552da-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="552da-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="552da-144">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="552da-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

