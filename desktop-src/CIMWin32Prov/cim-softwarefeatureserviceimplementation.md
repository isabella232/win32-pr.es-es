---
description: La \_ clase CIM SoftwareFeatureServiceImplementation representa una asociación entre un servicio y cómo se implementa en el software.
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureServiceImplementation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc521de933a4567c0760495880baf9251a774938
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152834"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a><span data-ttu-id="04b98-103">\_Clase SoftwareFeatureServiceImplementation de CIM</span><span class="sxs-lookup"><span data-stu-id="04b98-103">CIM\_SoftwareFeatureServiceImplementation class</span></span>

<span data-ttu-id="04b98-104">La clase **CIM \_ SoftwareFeatureServiceImplementation** representa una asociación entre un servicio y cómo se implementa en el software.</span><span class="sxs-lookup"><span data-stu-id="04b98-104">The **CIM\_SoftwareFeatureServiceImplementation** class represents an association between a service and how it is implemented in software.</span></span> <span data-ttu-id="04b98-105">Un servicio puede ser proporcionado por más de una característica de software, que funciona conjuntamente entre sí.</span><span class="sxs-lookup"><span data-stu-id="04b98-105">A service can be provided by more than one software feature, operating in conjunction with one another.</span></span> <span data-ttu-id="04b98-106">Además, una característica de software puede proporcionar más de un servicio.</span><span class="sxs-lookup"><span data-stu-id="04b98-106">Additionally, a software feature can provide more than one service.</span></span> <span data-ttu-id="04b98-107">Cuando hay varias características de software asociadas a un único servicio, se supone que los elementos funcionan conjuntamente para proporcionar el servicio.</span><span class="sxs-lookup"><span data-stu-id="04b98-107">When multiple software features are associated with a single service, it is assumed that the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="04b98-108">Si existen implementaciones diferentes de un servicio, cada implementación produciría instancias individuales del objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="04b98-108">If different implementations of a service exist, each implementation would result in individual instantiations of the service object.</span></span> <span data-ttu-id="04b98-109">Las instancias individuales tendrían asociaciones con las implementaciones únicas.</span><span class="sxs-lookup"><span data-stu-id="04b98-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04b98-110">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="04b98-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="04b98-111">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="04b98-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="04b98-112">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="04b98-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="04b98-113">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="04b98-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b98-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04b98-114">Syntax</span></span>

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="04b98-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="04b98-115">Members</span></span>

<span data-ttu-id="04b98-116">La clase **CIM \_ SoftwareFeatureServiceImplementation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="04b98-116">The **CIM\_SoftwareFeatureServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="04b98-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="04b98-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04b98-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="04b98-118">Properties</span></span>

<span data-ttu-id="04b98-119">La clase **CIM \_ SoftwareFeatureServiceImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="04b98-119">The **CIM\_SoftwareFeatureServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04b98-120">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="04b98-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b98-121">Tipo de datos: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="04b98-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="04b98-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="04b98-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04b98-123">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="04b98-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="04b98-124">Un [**\_ SoftwareFeature de CIM**](cim-softwarefeature.md) que describe la característica de software antecedente.</span><span class="sxs-lookup"><span data-stu-id="04b98-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="04b98-125">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="04b98-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b98-126">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="04b98-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="04b98-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="04b98-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04b98-128">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="04b98-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="04b98-129">Un [**\_ servicio CIM**](cim-service.md) que describe el servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="04b98-129">A [**CIM\_Service**](cim-service.md) that describes the dependent service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04b98-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04b98-130">Remarks</span></span>

<span data-ttu-id="04b98-131">La clase **CIM \_ SoftwareFeatureServiceImplementation** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="04b98-131">The **CIM\_SoftwareFeatureServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="04b98-132">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="04b98-132">WMI does not implement this class.</span></span>

<span data-ttu-id="04b98-133">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="04b98-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="04b98-134">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="04b98-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b98-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04b98-135">Requirements</span></span>



| <span data-ttu-id="04b98-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="04b98-136">Requirement</span></span> | <span data-ttu-id="04b98-137">Value</span><span class="sxs-lookup"><span data-stu-id="04b98-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04b98-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04b98-138">Minimum supported client</span></span><br/> | <span data-ttu-id="04b98-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04b98-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="04b98-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04b98-140">Minimum supported server</span></span><br/> | <span data-ttu-id="04b98-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04b98-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="04b98-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="04b98-142">Namespace</span></span><br/>                | <span data-ttu-id="04b98-143">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="04b98-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="04b98-144">MOF</span><span class="sxs-lookup"><span data-stu-id="04b98-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04b98-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04b98-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="04b98-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04b98-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04b98-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04b98-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b98-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="04b98-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b98-149">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="04b98-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

