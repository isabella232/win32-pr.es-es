---
description: La \_ Asociación PackageInChassis de CIM representa la relación en la que un chasis puede contener otros paquetes, como otros chasis y tarjetas.
ms.assetid: 3243bc0f-ce20-4108-b6e3-838bcb8f2fec
ms.tgt_platform: multiple
title: CIM_PackageInChassis (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInChassis
- CIM_PackageInChassis.LocationWithinContainer
- CIM_PackageInChassis.PartComponent
- CIM_PackageInChassis.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 26b65f983970c91d36e8d0a301277c67a2cc5639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496271"
---
# <a name="cim_packageinchassis-class"></a><span data-ttu-id="94cc5-103">\_Clase PackageInChassis de CIM</span><span class="sxs-lookup"><span data-stu-id="94cc5-103">CIM\_PackageInChassis class</span></span>

<span data-ttu-id="94cc5-104">La **Asociación \_ PackageInChassis de CIM** representa la relación en la que un chasis puede contener otros paquetes, como otros chasis y tarjetas.</span><span class="sxs-lookup"><span data-stu-id="94cc5-104">The **CIM\_PackageInChassis** association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94cc5-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="94cc5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="94cc5-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="94cc5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="94cc5-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="94cc5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="94cc5-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="94cc5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="94cc5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94cc5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B74-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInChassis : CIM_Container
{
  string                  LocationWithinContainer;
  CIM_PhysicalPackage REF PartComponent;
  CIM_Chassis         REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="94cc5-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="94cc5-110">Members</span></span>

<span data-ttu-id="94cc5-111">La clase **CIM \_ PackageInChassis** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="94cc5-111">The **CIM\_PackageInChassis** class has these types of members:</span></span>

-   [<span data-ttu-id="94cc5-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94cc5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94cc5-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94cc5-113">Properties</span></span>

<span data-ttu-id="94cc5-114">La clase **CIM \_ PackageInChassis** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="94cc5-114">The **CIM\_PackageInChassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94cc5-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="94cc5-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94cc5-116">Tipo de datos **: \_ chasis CIM**</span><span class="sxs-lookup"><span data-stu-id="94cc5-116">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="94cc5-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94cc5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94cc5-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="94cc5-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="94cc5-119">Un [**\_ chasis CIM**](cim-chassis.md) que describe el chasis que contiene otros paquetes físicos.</span><span class="sxs-lookup"><span data-stu-id="94cc5-119">A [**CIM\_Chassis**](cim-chassis.md) describing the chassis that contains other physical packages.</span></span>

</dd> <dt>

<span data-ttu-id="94cc5-120">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="94cc5-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94cc5-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="94cc5-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94cc5-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94cc5-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94cc5-123">Cadena de forma libre que representa la posición del elemento físico en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="94cc5-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="94cc5-124">La información relativa a los elementos estacionarios del contenedor (por ejemplo, "segunda Bahía de unidad de la parte superior"), ángulos, altitudes y otros datos se puede grabar en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="94cc5-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="94cc5-125">Esta cadena se puede complementar o utilizar en lugar de crear una instancia del objeto de [**\_ Ubicación CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="94cc5-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="94cc5-126">Esta propiedad se hereda del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="94cc5-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="94cc5-127">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="94cc5-127">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94cc5-128">Tipo de datos: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="94cc5-128">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="94cc5-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94cc5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94cc5-130">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="94cc5-130">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="94cc5-131">Un [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md) que describe el paquete físico que se encuentra en el chasis.</span><span class="sxs-lookup"><span data-stu-id="94cc5-131">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package which is contained in the chassis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94cc5-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94cc5-132">Remarks</span></span>

<span data-ttu-id="94cc5-133">La clase **CIM \_ PackageInChassis** se deriva del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="94cc5-133">The **CIM\_PackageInChassis** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="94cc5-134">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="94cc5-134">WMI does not implement this class.</span></span>

<span data-ttu-id="94cc5-135">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="94cc5-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="94cc5-136">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="94cc5-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="94cc5-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94cc5-137">Requirements</span></span>



| <span data-ttu-id="94cc5-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="94cc5-138">Requirement</span></span> | <span data-ttu-id="94cc5-139">Value</span><span class="sxs-lookup"><span data-stu-id="94cc5-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94cc5-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94cc5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="94cc5-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94cc5-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94cc5-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94cc5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="94cc5-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94cc5-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94cc5-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94cc5-144">Namespace</span></span><br/>                | <span data-ttu-id="94cc5-145">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="94cc5-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94cc5-146">MOF</span><span class="sxs-lookup"><span data-stu-id="94cc5-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94cc5-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94cc5-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94cc5-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94cc5-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94cc5-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94cc5-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94cc5-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="94cc5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94cc5-151">**\_Contenedor CIM**</span><span class="sxs-lookup"><span data-stu-id="94cc5-151">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

