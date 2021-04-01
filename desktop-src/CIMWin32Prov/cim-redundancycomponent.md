---
description: La \_ clase CIM RedundancyComponent asocia un grupo de redundancia compuesto por elementos del sistema administrados e indica que, juntos, los elementos proporcionan redundancia.
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: CIM_RedundancyComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bcd1c16417ba0c02e13579f9e471076d4c61818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906989"
---
# <a name="cim_redundancycomponent-class"></a><span data-ttu-id="707d3-103">\_Clase RedundancyComponent de CIM</span><span class="sxs-lookup"><span data-stu-id="707d3-103">CIM\_RedundancyComponent class</span></span>

<span data-ttu-id="707d3-104">La clase **CIM \_ RedundancyComponent** asocia un grupo de redundancia compuesto por elementos del sistema administrados e indica que, juntos, los elementos proporcionan redundancia.</span><span class="sxs-lookup"><span data-stu-id="707d3-104">The **CIM\_RedundancyComponent** class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="707d3-105">Todos los elementos agregados en un grupo de redundancia deben ser instancias de la misma clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="707d3-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="707d3-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="707d3-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="707d3-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="707d3-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="707d3-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="707d3-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="707d3-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="707d3-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="707d3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="707d3-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="707d3-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="707d3-111">Members</span></span>

<span data-ttu-id="707d3-112">La clase **CIM \_ RedundancyComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="707d3-112">The **CIM\_RedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="707d3-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="707d3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="707d3-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="707d3-114">Properties</span></span>

<span data-ttu-id="707d3-115">La clase **CIM \_ RedundancyComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="707d3-115">The **CIM\_RedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="707d3-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="707d3-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="707d3-117">Tipo de datos: **CIM \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="707d3-117">Data type: **CIM\_RedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="707d3-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="707d3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="707d3-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="707d3-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="707d3-120">La **Asociación \_ RedundancyComponent de CIM** indica que "este conjunto de aficionados" o "estas extensiones físicas" participan en un solo grupo de redundancia.</span><span class="sxs-lookup"><span data-stu-id="707d3-120">The **CIM\_RedundancyComponent** association indicates that 'this set of fans' or 'these physical extents' participate in a single redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="707d3-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="707d3-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="707d3-122">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="707d3-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="707d3-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="707d3-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="707d3-124">Un [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) que describe el elemento secundario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="707d3-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

<span data-ttu-id="707d3-125">Esta propiedad se hereda del [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="707d3-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="707d3-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="707d3-126">Remarks</span></span>

<span data-ttu-id="707d3-127">**CIM \_ RedundancyComponent** se deriva del [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="707d3-127">**CIM\_RedundancyComponent** is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="707d3-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="707d3-128">WMI does not implement this class.</span></span>

<span data-ttu-id="707d3-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="707d3-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="707d3-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="707d3-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="707d3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="707d3-131">Requirements</span></span>



| <span data-ttu-id="707d3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="707d3-132">Requirement</span></span> | <span data-ttu-id="707d3-133">Value</span><span class="sxs-lookup"><span data-stu-id="707d3-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="707d3-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="707d3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="707d3-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="707d3-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="707d3-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="707d3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="707d3-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="707d3-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="707d3-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="707d3-138">Namespace</span></span><br/>                | <span data-ttu-id="707d3-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="707d3-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="707d3-140">MOF</span><span class="sxs-lookup"><span data-stu-id="707d3-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="707d3-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="707d3-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="707d3-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="707d3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="707d3-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="707d3-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="707d3-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="707d3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="707d3-145">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="707d3-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

