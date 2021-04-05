---
description: La \_ clase CIM SoftwareFeatureSAPImplementation representa una asociación entre un punto de acceso al servicio (SAP) y cómo se implementa en el software.
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureSAPImplementation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4130163ce90aea7a72b4d76a5c6c20b0631edf3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906986"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a><span data-ttu-id="32e3d-103">\_Clase SoftwareFeatureSAPImplementation de CIM</span><span class="sxs-lookup"><span data-stu-id="32e3d-103">CIM\_SoftwareFeatureSAPImplementation class</span></span>

<span data-ttu-id="32e3d-104">La clase **CIM \_ SoftwareFeatureSAPImplementation** representa una asociación entre un punto de acceso al servicio (SAP) y cómo se implementa en el software.</span><span class="sxs-lookup"><span data-stu-id="32e3d-104">The **CIM\_SoftwareFeatureSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented in software.</span></span> <span data-ttu-id="32e3d-105">Un SAP puede ser proporcionado por más de una característica de software para funcionar conjuntamente entre sí.</span><span class="sxs-lookup"><span data-stu-id="32e3d-105">A SAP can be provided by more than one software feature to operate in conjunction with one another.</span></span> <span data-ttu-id="32e3d-106">Además, una característica de software puede proporcionar más de un SAP.</span><span class="sxs-lookup"><span data-stu-id="32e3d-106">Additionally, a software feature can provide more than one SAP.</span></span> <span data-ttu-id="32e3d-107">Cuando hay muchas características de software asociadas a un único SAP, se supone que los elementos funcionan conjuntamente para proporcionar el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="32e3d-107">When many software features are associated with a single SAP, it is assumed that the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="32e3d-108">Si existen implementaciones diferentes de un SAP, cada implementación produciría instancias individuales del objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="32e3d-108">If different implementations of a SAP exist, each implementation would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="32e3d-109">Las instancias individuales tendrían asociaciones con las implementaciones únicas.</span><span class="sxs-lookup"><span data-stu-id="32e3d-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32e3d-110">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="32e3d-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="32e3d-111">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="32e3d-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="32e3d-112">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="32e3d-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="32e3d-113">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="32e3d-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e3d-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32e3d-114">Syntax</span></span>

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="32e3d-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="32e3d-115">Members</span></span>

<span data-ttu-id="32e3d-116">La clase **CIM \_ SoftwareFeatureSAPImplementation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="32e3d-116">The **CIM\_SoftwareFeatureSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="32e3d-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32e3d-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32e3d-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32e3d-118">Properties</span></span>

<span data-ttu-id="32e3d-119">La clase **CIM \_ SoftwareFeatureSAPImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="32e3d-119">The **CIM\_SoftwareFeatureSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32e3d-120">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="32e3d-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3d-121">Tipo de datos: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="32e3d-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="32e3d-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32e3d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32e3d-123">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="32e3d-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="32e3d-124">Un [**\_ SoftwareFeature de CIM**](cim-softwarefeature.md) que describe la característica de software antecedente.</span><span class="sxs-lookup"><span data-stu-id="32e3d-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="32e3d-125">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="32e3d-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e3d-126">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="32e3d-126">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="32e3d-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32e3d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32e3d-128">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="32e3d-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="32e3d-129">Un [**\_ punto de CIM**](cim-serviceaccesspoint.md) que describe el punto de acceso al servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="32e3d-129">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the dependent service access point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32e3d-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32e3d-130">Remarks</span></span>

<span data-ttu-id="32e3d-131">La clase **CIM \_ SoftwareFeatureSAPImplementation** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="32e3d-131">The **CIM\_SoftwareFeatureSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="32e3d-132">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="32e3d-132">WMI does not implement this class.</span></span>

<span data-ttu-id="32e3d-133">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="32e3d-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="32e3d-134">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="32e3d-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="32e3d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32e3d-135">Requirements</span></span>



| <span data-ttu-id="32e3d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="32e3d-136">Requirement</span></span> | <span data-ttu-id="32e3d-137">Value</span><span class="sxs-lookup"><span data-stu-id="32e3d-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32e3d-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e3d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="32e3d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32e3d-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32e3d-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e3d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="32e3d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32e3d-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32e3d-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32e3d-142">Namespace</span></span><br/>                | <span data-ttu-id="32e3d-143">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="32e3d-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="32e3d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="32e3d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32e3d-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32e3d-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="32e3d-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32e3d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32e3d-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32e3d-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e3d-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="32e3d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e3d-149">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="32e3d-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

