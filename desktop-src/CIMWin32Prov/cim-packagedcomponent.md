---
description: La \_ Asociación PackagedComponent de CIM representa una relación explícita en la que un componente normalmente está contenido en un paquete físico, como un chasis o una tarjeta.
ms.assetid: ef0cdbc4-41ee-4517-92ca-61cfcbe64c36
ms.tgt_platform: multiple
title: CIM_PackagedComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackagedComponent
- CIM_PackagedComponent.LocationWithinContainer
- CIM_PackagedComponent.PartComponent
- CIM_PackagedComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b95cbbea60bfbd6bb352e53cfecb8819d99ec24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907040"
---
# <a name="cim_packagedcomponent-class"></a><span data-ttu-id="804c5-103">\_Clase PackagedComponent de CIM</span><span class="sxs-lookup"><span data-stu-id="804c5-103">CIM\_PackagedComponent class</span></span>

<span data-ttu-id="804c5-104">La **Asociación \_ PackagedComponent de CIM** representa una relación explícita en la que un componente normalmente está contenido en un paquete físico, como un chasis o una tarjeta.</span><span class="sxs-lookup"><span data-stu-id="804c5-104">The **CIM\_PackagedComponent** association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

<span data-ttu-id="804c5-105">**Nota:**  Es posible que un componente se quite de, o que todavía no se haya insertado en, su paquete contenedor (es decir, la propiedad booleana **extraíble** sea **true**).</span><span class="sxs-lookup"><span data-stu-id="804c5-105">**Note**  A component may be removed from, or not yet inserted into, its containing package (that is, the **Removable** Boolean property is **TRUE**).</span></span> <span data-ttu-id="804c5-106">Por lo tanto, un componente no siempre se puede asociar a un contenedor.</span><span class="sxs-lookup"><span data-stu-id="804c5-106">Therefore, a component may not always be associated with a container.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="804c5-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="804c5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="804c5-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="804c5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="804c5-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="804c5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="804c5-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="804c5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="804c5-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="804c5-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B79-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackagedComponent : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalComponent REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="804c5-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="804c5-112">Members</span></span>

<span data-ttu-id="804c5-113">La clase **CIM \_ PackagedComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="804c5-113">The **CIM\_PackagedComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="804c5-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="804c5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="804c5-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="804c5-115">Properties</span></span>

<span data-ttu-id="804c5-116">La clase **CIM \_ PackagedComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="804c5-116">The **CIM\_PackagedComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="804c5-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="804c5-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="804c5-118">Tipo de datos: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="804c5-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="804c5-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="804c5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="804c5-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="804c5-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="804c5-121">Un [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md) que describe el paquete físico que contiene los componentes.</span><span class="sxs-lookup"><span data-stu-id="804c5-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that contains component(s).</span></span>

</dd> <dt>

<span data-ttu-id="804c5-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="804c5-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="804c5-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="804c5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="804c5-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="804c5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="804c5-125">Cadena de forma libre que representa la posición del elemento físico en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="804c5-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="804c5-126">La información relativa a los elementos estacionarios del contenedor (por ejemplo, "segunda Bahía de unidad de la parte superior"), ángulos, altitudes y otros datos se puede grabar en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="804c5-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="804c5-127">Esta cadena se puede complementar o utilizar en lugar de crear una instancia del objeto de [**\_ Ubicación CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="804c5-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="804c5-128">Esta propiedad se hereda del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="804c5-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="804c5-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="804c5-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="804c5-130">Tipo de datos: **CIM \_ PhysicalComponent**</span><span class="sxs-lookup"><span data-stu-id="804c5-130">Data type: **CIM\_PhysicalComponent**</span></span>
</dt> <dt>

<span data-ttu-id="804c5-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="804c5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="804c5-132">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="804c5-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="804c5-133">Un [**\_ PhysicalComponent de CIM**](cim-physicalcomponent.md) que describe el componente físico que se encuentra en el paquete.</span><span class="sxs-lookup"><span data-stu-id="804c5-133">A [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) describing the physical component which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="804c5-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="804c5-134">Remarks</span></span>

<span data-ttu-id="804c5-135">La clase **CIM \_ PackagedComponent** se deriva del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="804c5-135">The **CIM\_PackagedComponent** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="804c5-136">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="804c5-136">WMI does not implement this class.</span></span>

<span data-ttu-id="804c5-137">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="804c5-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="804c5-138">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="804c5-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="804c5-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="804c5-139">Requirements</span></span>



| <span data-ttu-id="804c5-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="804c5-140">Requirement</span></span> | <span data-ttu-id="804c5-141">Value</span><span class="sxs-lookup"><span data-stu-id="804c5-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="804c5-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="804c5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="804c5-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="804c5-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="804c5-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="804c5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="804c5-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="804c5-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="804c5-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="804c5-146">Namespace</span></span><br/>                | <span data-ttu-id="804c5-147">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="804c5-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="804c5-148">MOF</span><span class="sxs-lookup"><span data-stu-id="804c5-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="804c5-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="804c5-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="804c5-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="804c5-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="804c5-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="804c5-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="804c5-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="804c5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804c5-153">**\_Contenedor CIM**</span><span class="sxs-lookup"><span data-stu-id="804c5-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

