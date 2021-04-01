---
description: La \_ clase CIM ApplicationSystemSoftwareFeature representa una asociación que identifica las características de software que componen un sistema de aplicación determinado. Las características de software se pueden incluir en diferentes productos.
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: CIM_ApplicationSystemSoftwareFeature (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b13a15370b19583eef61fb36fda2d63fcb61989
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907378"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a><span data-ttu-id="b0ecd-104">\_Clase ApplicationSystemSoftwareFeature de CIM</span><span class="sxs-lookup"><span data-stu-id="b0ecd-104">CIM\_ApplicationSystemSoftwareFeature class</span></span>

<span data-ttu-id="b0ecd-105">La clase **CIM \_ ApplicationSystemSoftwareFeature** representa una asociación que identifica las características de software que componen un sistema de aplicación determinado.</span><span class="sxs-lookup"><span data-stu-id="b0ecd-105">The **CIM\_ApplicationSystemSoftwareFeature** class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="b0ecd-106">Las características de software se pueden incluir en diferentes productos.</span><span class="sxs-lookup"><span data-stu-id="b0ecd-106">The software features can be included in different products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0ecd-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="b0ecd-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b0ecd-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b0ecd-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b0ecd-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b0ecd-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b0ecd-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b0ecd-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0ecd-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0ecd-111">Syntax</span></span>

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="b0ecd-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="b0ecd-112">Members</span></span>

<span data-ttu-id="b0ecd-113">La clase **CIM \_ ApplicationSystemSoftwareFeature** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b0ecd-113">The **CIM\_ApplicationSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="b0ecd-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b0ecd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0ecd-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b0ecd-115">Properties</span></span>

<span data-ttu-id="b0ecd-116">La clase **CIM \_ ApplicationSystemSoftwareFeature** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b0ecd-116">The **CIM\_ApplicationSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0ecd-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b0ecd-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0ecd-118">Tipo de datos: **CIM \_ ApplicationSystem**</span><span class="sxs-lookup"><span data-stu-id="b0ecd-118">Data type: **CIM\_ApplicationSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b0ecd-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b0ecd-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0ecd-120">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="b0ecd-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b0ecd-121">[**\_ ApplicationSystem CIM**](cim-applicationsystem.md) que contiene el sistema primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="b0ecd-121">A [**CIM\_ApplicationSystem**](cim-applicationsystem.md) that contains the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="b0ecd-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b0ecd-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0ecd-123">Tipo de datos: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="b0ecd-123">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="b0ecd-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b0ecd-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0ecd-125">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="b0ecd-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b0ecd-126">Un [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) que contiene el elemento secundario que es un componente de un sistema.</span><span class="sxs-lookup"><span data-stu-id="b0ecd-126">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that contain the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0ecd-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0ecd-127">Remarks</span></span>

<span data-ttu-id="b0ecd-128">La clase **CIM \_ ApplicationSystemSoftwareFeature** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="b0ecd-128">The **CIM\_ApplicationSystemSoftwareFeature** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="b0ecd-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="b0ecd-129">WMI does not implement this class.</span></span>

<span data-ttu-id="b0ecd-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="b0ecd-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b0ecd-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="b0ecd-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0ecd-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0ecd-132">Requirements</span></span>



| <span data-ttu-id="b0ecd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0ecd-133">Requirement</span></span> | <span data-ttu-id="b0ecd-134">Value</span><span class="sxs-lookup"><span data-stu-id="b0ecd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ecd-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0ecd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b0ecd-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0ecd-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0ecd-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0ecd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b0ecd-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0ecd-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0ecd-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b0ecd-139">Namespace</span></span><br/>                | <span data-ttu-id="b0ecd-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b0ecd-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b0ecd-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b0ecd-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0ecd-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0ecd-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0ecd-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0ecd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0ecd-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0ecd-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0ecd-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0ecd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0ecd-146">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b0ecd-146">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

