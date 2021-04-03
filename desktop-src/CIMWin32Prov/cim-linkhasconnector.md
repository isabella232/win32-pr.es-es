---
description: La \_ clase LinkHasConnector de CIM asocia los cables y los vínculos usados como conectores físicos, que conectan los elementos físicos. Esta asociación define explícitamente la relación de los conectores para \_ PHYSICALLINK CIM.
ms.assetid: c8244b93-749a-424a-ab40-ce5ce79c8b02
ms.tgt_platform: multiple
title: CIM_LinkHasConnector (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LinkHasConnector
- CIM_LinkHasConnector.PartComponent
- CIM_LinkHasConnector.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daeb9d07fefc4c52c7b630dcc69099c1cae429a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907285"
---
# <a name="cim_linkhasconnector-class"></a><span data-ttu-id="9f035-104">\_Clase LinkHasConnector de CIM</span><span class="sxs-lookup"><span data-stu-id="9f035-104">CIM\_LinkHasConnector class</span></span>

<span data-ttu-id="9f035-105">La **clase \_ LinkHasConnector de CIM** asocia los cables y los vínculos usados como conectores físicos, que conectan los elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="9f035-105">The **CIM\_LinkHasConnector** class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="9f035-106">Esta asociación define explícitamente la relación de los conectores para [**\_ PhysicalLink CIM**](cim-physicallink.md).</span><span class="sxs-lookup"><span data-stu-id="9f035-106">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f035-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9f035-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9f035-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9f035-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9f035-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9f035-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9f035-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9f035-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f035-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f035-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_LinkHasConnector : CIM_Component
{
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalLink      REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="9f035-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="9f035-112">Members</span></span>

<span data-ttu-id="9f035-113">La clase **CIM \_ LinkHasConnector** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9f035-113">The **CIM\_LinkHasConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="9f035-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f035-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f035-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f035-115">Properties</span></span>

<span data-ttu-id="9f035-116">La clase **CIM \_ LinkHasConnector** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f035-116">The **CIM\_LinkHasConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f035-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9f035-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f035-118">Tipo de datos: **CIM \_ PhysicalLink**</span><span class="sxs-lookup"><span data-stu-id="9f035-118">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="9f035-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f035-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f035-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="9f035-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9f035-121">Un [**\_ PhysicalLink de CIM**](cim-physicallink.md) que describe el vínculo físico que tiene un conector.</span><span class="sxs-lookup"><span data-stu-id="9f035-121">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="9f035-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9f035-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f035-123">Tipo de datos: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="9f035-123">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="9f035-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f035-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f035-125">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="9f035-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9f035-126">Un [**\_ PhysicalConnector de CIM**](cim-physicalconnector.md) que describe el conector físico.</span><span class="sxs-lookup"><span data-stu-id="9f035-126">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f035-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f035-127">Remarks</span></span>

<span data-ttu-id="9f035-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="9f035-128">WMI does not implement this class.</span></span>

<span data-ttu-id="9f035-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9f035-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9f035-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9f035-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f035-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f035-131">Requirements</span></span>



| <span data-ttu-id="9f035-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f035-132">Requirement</span></span> | <span data-ttu-id="9f035-133">Value</span><span class="sxs-lookup"><span data-stu-id="9f035-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f035-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f035-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9f035-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f035-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f035-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f035-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9f035-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f035-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f035-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9f035-138">Namespace</span></span><br/>                | <span data-ttu-id="9f035-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9f035-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f035-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9f035-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f035-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f035-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f035-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f035-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f035-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f035-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f035-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f035-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f035-145">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="9f035-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

