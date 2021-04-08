---
description: La \_ clase de contenedor CIM representa una asociación entre un elemento contenido y un elemento físico contenedor. Un objeto contenedor debe ser un paquete físico.
ms.assetid: 9b119163-3c56-44e2-ba66-d8add3c375fa
ms.tgt_platform: multiple
title: CIM_Container (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Container
- CIM_Container.PartComponent
- CIM_Container.GroupComponent
- CIM_Container.LocationWithinContainer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70aca54c80a954deed88d1ec740f0057753bf5e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000661"
---
# <a name="cim_container-class"></a><span data-ttu-id="e5a12-104">\_Clase de contenedor CIM</span><span class="sxs-lookup"><span data-stu-id="e5a12-104">CIM\_Container class</span></span>

<span data-ttu-id="e5a12-105">La clase de **\_ contenedor CIM** representa una asociación entre un elemento contenido y un elemento físico contenedor.</span><span class="sxs-lookup"><span data-stu-id="e5a12-105">The **CIM\_Container** class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="e5a12-106">Un objeto contenedor debe ser un paquete físico.</span><span class="sxs-lookup"><span data-stu-id="e5a12-106">A containing object must be a physical package.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5a12-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="e5a12-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e5a12-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e5a12-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e5a12-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e5a12-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e5a12-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e5a12-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a12-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5a12-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Container : CIM_Component
{
  CIM_PhysicalElement REF PartComponent;
  CIM_PhysicalPackage REF GroupComponent;
  string                  LocationWithinContainer;
};
```

## <a name="members"></a><span data-ttu-id="e5a12-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="e5a12-112">Members</span></span>

<span data-ttu-id="e5a12-113">La clase de **\_ contenedor CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e5a12-113">The **CIM\_Container** class has these types of members:</span></span>

-   [<span data-ttu-id="e5a12-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e5a12-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5a12-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e5a12-115">Properties</span></span>

<span data-ttu-id="e5a12-116">La **clase \_ contenedora CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e5a12-116">The **CIM\_Container** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5a12-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e5a12-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5a12-118">Tipo de datos: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="e5a12-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="e5a12-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e5a12-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5a12-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e5a12-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e5a12-121">Un [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md) que representa el paquete físico que contiene otros elementos físicos, incluidos otros paquetes.</span><span class="sxs-lookup"><span data-stu-id="e5a12-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that represents the physical package that contains other physical elements, including other packages.</span></span>

</dd> <dt>

<span data-ttu-id="e5a12-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="e5a12-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5a12-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e5a12-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5a12-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e5a12-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5a12-125">Cadena de forma libre que representa la posición del elemento físico en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="e5a12-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="e5a12-126">La información relativa a los elementos estacionarios del contenedor (por ejemplo, "segunda Bahía de unidad de la parte superior"), ángulos, altitudes y otros datos se puede grabar en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e5a12-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="e5a12-127">Esta cadena se puede complementar o utilizar en lugar de crear una instancia del objeto de [**\_ Ubicación CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a12-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="e5a12-128">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e5a12-128">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5a12-129">Tipo de datos: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="e5a12-129">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="e5a12-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e5a12-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5a12-131">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e5a12-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e5a12-132">[**\_ PhysicalElement CIM**](cim-physicalelement.md) que describe el elemento físico que se encuentra en el paquete.</span><span class="sxs-lookup"><span data-stu-id="e5a12-132">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5a12-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5a12-133">Remarks</span></span>

<span data-ttu-id="e5a12-134">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="e5a12-134">WMI does not implement this class.</span></span> <span data-ttu-id="e5a12-135">Para obtener más información sobre las clases derivadas del **\_ contenedor CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e5a12-135">For more information about classes derived from **CIM\_Container**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e5a12-136">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="e5a12-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e5a12-137">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="e5a12-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a12-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5a12-138">Requirements</span></span>



| <span data-ttu-id="e5a12-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5a12-139">Requirement</span></span> | <span data-ttu-id="e5a12-140">Value</span><span class="sxs-lookup"><span data-stu-id="e5a12-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a12-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5a12-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a12-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5a12-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5a12-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5a12-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a12-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5a12-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5a12-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e5a12-145">Namespace</span></span><br/>                | <span data-ttu-id="e5a12-146">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e5a12-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e5a12-147">MOF</span><span class="sxs-lookup"><span data-stu-id="e5a12-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5a12-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5a12-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5a12-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e5a12-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5a12-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5a12-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5a12-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5a12-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a12-152">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="e5a12-152">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

