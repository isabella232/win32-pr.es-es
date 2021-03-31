---
description: La \_ Asociación ChassisInRack de CIM representa el &\# 0034; que contiene&\# 0034; relación entre un bastidor y un chasis que contiene.
ms.assetid: 1c8a5058-58fe-42e0-b337-7e1a05120789
ms.tgt_platform: multiple
title: CIM_ChassisInRack (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ChassisInRack
- CIM_ChassisInRack.LocationWithinContainer
- CIM_ChassisInRack.PartComponent
- CIM_ChassisInRack.GroupComponent
- CIM_ChassisInRack.BottomU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fd582991df30bc36cd71c4c3fa08d9a5a5153819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153244"
---
# <a name="cim_chassisinrack-class"></a><span data-ttu-id="d2822-103">\_Clase ChassisInRack de CIM</span><span class="sxs-lookup"><span data-stu-id="d2822-103">CIM\_ChassisInRack class</span></span>

<span data-ttu-id="d2822-104">La **Asociación \_ ChassisInRack de CIM** representa la relación "que contiene" entre un bastidor y un chasis que contiene.</span><span class="sxs-lookup"><span data-stu-id="d2822-104">The **CIM\_ChassisInRack** association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2822-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="d2822-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d2822-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d2822-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d2822-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d2822-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d2822-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d2822-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2822-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2822-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B73-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ChassisInRack : CIM_Container
{
  string          LocationWithinContainer;
  CIM_Chassis REF PartComponent;
  CIM_Rack    REF GroupComponent;
  uint16          BottomU;
};
```

## <a name="members"></a><span data-ttu-id="d2822-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d2822-110">Members</span></span>

<span data-ttu-id="d2822-111">La clase **CIM \_ ChassisInRack** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d2822-111">The **CIM\_ChassisInRack** class has these types of members:</span></span>

-   [<span data-ttu-id="d2822-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2822-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2822-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2822-113">Properties</span></span>

<span data-ttu-id="d2822-114">La clase **CIM \_ ChassisInRack** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d2822-114">The **CIM\_ChassisInRack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2822-115">**BottomU**</span><span class="sxs-lookup"><span data-stu-id="d2822-115">**BottomU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2822-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2822-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2822-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2822-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2822-118">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("EE. UU.")</span><span class="sxs-lookup"><span data-stu-id="d2822-118">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="d2822-119">Entero que indica la "U" más baja o inferior en la que se monta el chasis.</span><span class="sxs-lookup"><span data-stu-id="d2822-119">Integer that indicates the lowest or bottom "U" in which the chassis is mounted.</span></span> <span data-ttu-id="d2822-120">Una "U" es una unidad de medida estándar para el alto de un bastidor, o componente montable en bastidor, y es igual a 1,75 pulgadas o 4,445 centímetros.</span><span class="sxs-lookup"><span data-stu-id="d2822-120">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="d2822-121">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d2822-121">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2822-122">Tipo de datos **: \_ bastidor CIM**</span><span class="sxs-lookup"><span data-stu-id="d2822-122">Data type: **CIM\_Rack**</span></span>
</dt> <dt>

<span data-ttu-id="d2822-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2822-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2822-124">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="d2822-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d2822-125">Un [**\_ bastidor CIM**](cim-rack.md) que describe el bastidor que contiene el chasis.</span><span class="sxs-lookup"><span data-stu-id="d2822-125">A [**CIM\_Rack**](cim-rack.md) that describes the rack that contains the chassis.</span></span>

</dd> <dt>

<span data-ttu-id="d2822-126">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="d2822-126">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2822-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2822-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2822-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2822-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2822-129">Cadena de forma libre que representa la posición del elemento físico en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="d2822-129">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="d2822-130">La información relativa a los elementos estacionarios del contenedor (por ejemplo, "segunda Bahía de unidad de la parte superior"), ángulos, altitudes y otros datos se puede grabar en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d2822-130">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="d2822-131">Esta cadena se puede complementar o utilizar en lugar de crear una instancia del objeto de [**\_ Ubicación CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="d2822-131">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="d2822-132">Esta propiedad se hereda del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="d2822-132">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2822-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d2822-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2822-134">Tipo de datos **: \_ chasis CIM**</span><span class="sxs-lookup"><span data-stu-id="d2822-134">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="d2822-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2822-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2822-136">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="d2822-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d2822-137">Un [**\_ chasis CIM**](cim-chassis.md) que describe el chasis que se monta en el bastidor.</span><span class="sxs-lookup"><span data-stu-id="d2822-137">A [**CIM\_Chassis**](cim-chassis.md) that describes the chassis which is mounted in the rack.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2822-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2822-138">Remarks</span></span>

<span data-ttu-id="d2822-139">La clase **CIM \_ ChassisInRack** se deriva del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="d2822-139">The **CIM\_ChassisInRack** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="d2822-140">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="d2822-140">WMI does not implement this class.</span></span>

<span data-ttu-id="d2822-141">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="d2822-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d2822-142">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="d2822-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2822-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2822-143">Requirements</span></span>



| <span data-ttu-id="d2822-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2822-144">Requirement</span></span> | <span data-ttu-id="d2822-145">Value</span><span class="sxs-lookup"><span data-stu-id="d2822-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2822-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2822-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d2822-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2822-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2822-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2822-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d2822-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2822-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2822-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d2822-150">Namespace</span></span><br/>                | <span data-ttu-id="d2822-151">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d2822-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d2822-152">MOF</span><span class="sxs-lookup"><span data-stu-id="d2822-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2822-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2822-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2822-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2822-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2822-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2822-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2822-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2822-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2822-157">**\_Contenedor CIM**</span><span class="sxs-lookup"><span data-stu-id="d2822-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

