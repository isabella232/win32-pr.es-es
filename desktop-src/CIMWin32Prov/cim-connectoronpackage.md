---
description: La \_ clase CIM ConnectorOnPackage representa una asociación que hace explícita la relación de contención entre los conectores y los paquetes. Los paquetes físicos contienen conectores y otros elementos físicos.
ms.assetid: 67cfb8c7-b952-452c-aeb4-0f06b2b0570b
ms.tgt_platform: multiple
title: CIM_ConnectorOnPackage (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectorOnPackage
- CIM_ConnectorOnPackage.LocationWithinContainer
- CIM_ConnectorOnPackage.PartComponent
- CIM_ConnectorOnPackage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9dfac5cf2daa19f1d3c073ac65d30fa859d2523b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907332"
---
# <a name="cim_connectoronpackage-class"></a><span data-ttu-id="e11db-104">\_Clase ConnectorOnPackage de CIM</span><span class="sxs-lookup"><span data-stu-id="e11db-104">CIM\_ConnectorOnPackage class</span></span>

<span data-ttu-id="e11db-105">La clase **CIM \_ ConnectorOnPackage** representa una asociación que hace explícita la relación de contención entre los conectores y los paquetes.</span><span class="sxs-lookup"><span data-stu-id="e11db-105">The **CIM\_ConnectorOnPackage** class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="e11db-106">Los paquetes físicos contienen conectores y otros elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="e11db-106">Physical packages contain connectors as well as other physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e11db-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="e11db-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e11db-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e11db-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e11db-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e11db-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e11db-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e11db-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e11db-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e11db-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectorOnPackage : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e11db-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="e11db-112">Members</span></span>

<span data-ttu-id="e11db-113">La clase **CIM \_ ConnectorOnPackage** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e11db-113">The **CIM\_ConnectorOnPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="e11db-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e11db-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e11db-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e11db-115">Properties</span></span>

<span data-ttu-id="e11db-116">La clase **CIM \_ ConnectorOnPackage** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e11db-116">The **CIM\_ConnectorOnPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e11db-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e11db-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e11db-118">Tipo de datos: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="e11db-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="e11db-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e11db-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e11db-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e11db-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e11db-121">Un [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md) que describe el paquete físico que tiene un conector.</span><span class="sxs-lookup"><span data-stu-id="e11db-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="e11db-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="e11db-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e11db-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e11db-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e11db-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e11db-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e11db-125">Cadena de forma libre que representa la posición del elemento físico en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="e11db-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="e11db-126">La información relativa a los elementos estacionarios del contenedor (por ejemplo, "segunda Bahía de unidad de la parte superior"), ángulos, altitudes y otros datos se puede grabar en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e11db-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="e11db-127">Esta cadena se puede complementar o utilizar en lugar de crear una instancia del objeto de [**\_ Ubicación CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="e11db-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="e11db-128">Esta propiedad se hereda del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="e11db-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="e11db-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e11db-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e11db-130">Tipo de datos: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="e11db-130">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="e11db-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e11db-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e11db-132">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e11db-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e11db-133">Un [**\_ PhysicalConnector de CIM**](cim-physicalconnector.md) que describe el conector físico.</span><span class="sxs-lookup"><span data-stu-id="e11db-133">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e11db-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e11db-134">Remarks</span></span>

<span data-ttu-id="e11db-135">La clase **CIM \_ ConnectorOnPackage** se deriva del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="e11db-135">The **CIM\_ConnectorOnPackage** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="e11db-136">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="e11db-136">WMI does not implement this class.</span></span>

<span data-ttu-id="e11db-137">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="e11db-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e11db-138">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="e11db-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e11db-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e11db-139">Requirements</span></span>



| <span data-ttu-id="e11db-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e11db-140">Requirement</span></span> | <span data-ttu-id="e11db-141">Value</span><span class="sxs-lookup"><span data-stu-id="e11db-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e11db-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e11db-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e11db-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e11db-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e11db-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e11db-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e11db-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e11db-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e11db-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e11db-146">Namespace</span></span><br/>                | <span data-ttu-id="e11db-147">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e11db-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e11db-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e11db-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e11db-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e11db-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e11db-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e11db-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e11db-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e11db-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e11db-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="e11db-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e11db-153">**\_Contenedor CIM**</span><span class="sxs-lookup"><span data-stu-id="e11db-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

