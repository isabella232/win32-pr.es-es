---
description: La \_ clase MemoryOnCard de CIM asocia la memoria física que se encuentra en los paneles de hospedaje, las tarjetas de adaptador, etc. Esta asociación define explícitamente la relación de memoria con las tarjetas.
ms.assetid: 0d094cad-c542-4794-b6e1-87cdc8067668
ms.tgt_platform: multiple
title: CIM_MemoryOnCard (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryOnCard
- CIM_MemoryOnCard.LocationWithinContainer
- CIM_MemoryOnCard.PartComponent
- CIM_MemoryOnCard.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2094101ab0cbbbc769194793273bf080cfe52818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659618"
---
# <a name="cim_memoryoncard-class"></a><span data-ttu-id="aac66-104">\_Clase MemoryOnCard de CIM</span><span class="sxs-lookup"><span data-stu-id="aac66-104">CIM\_MemoryOnCard class</span></span>

<span data-ttu-id="aac66-105">La **clase \_ MemoryOnCard de CIM** asocia la memoria física que se encuentra en los paneles de hospedaje, las tarjetas de adaptador, etc.</span><span class="sxs-lookup"><span data-stu-id="aac66-105">The **CIM\_MemoryOnCard** class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="aac66-106">Esta asociación define explícitamente la relación de memoria con las tarjetas.</span><span class="sxs-lookup"><span data-stu-id="aac66-106">This association explicitly defines the relationship of memory to cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aac66-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="aac66-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aac66-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aac66-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aac66-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="aac66-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aac66-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="aac66-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aac66-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aac66-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryOnCard : CIM_PackagedComponent
{
  string                 LocationWithinContainer;
  CIM_PhysicalMemory REF PartComponent;
  CIM_Card           REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="aac66-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="aac66-112">Members</span></span>

<span data-ttu-id="aac66-113">La clase **CIM \_ MemoryOnCard** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aac66-113">The **CIM\_MemoryOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="aac66-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aac66-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aac66-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aac66-115">Properties</span></span>

<span data-ttu-id="aac66-116">La clase **CIM \_ MemoryOnCard** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="aac66-116">The **CIM\_MemoryOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aac66-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="aac66-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac66-118">Tipo de datos **: \_ tarjeta CIM**</span><span class="sxs-lookup"><span data-stu-id="aac66-118">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="aac66-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aac66-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aac66-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="aac66-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="aac66-121">Una [**\_ tarjeta CIM**](cim-card.md) que describe la tarjeta que incluye o "contiene" memoria.</span><span class="sxs-lookup"><span data-stu-id="aac66-121">A [**CIM\_Card**](cim-card.md) describing the card that includes or 'contains' memory.</span></span>

</dd> <dt>

<span data-ttu-id="aac66-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="aac66-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac66-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aac66-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aac66-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aac66-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aac66-125">Cadena de forma libre que representa la posición del elemento físico en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="aac66-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="aac66-126">La información relativa a los elementos estacionarios del contenedor (por ejemplo, "segunda Bahía de unidad de la parte superior"), ángulos, altitudes y otros datos se puede grabar en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="aac66-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="aac66-127">Esta cadena se puede complementar o utilizar en lugar de crear una instancia del objeto de [**\_ Ubicación CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="aac66-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="aac66-128">Esta propiedad se hereda del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="aac66-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="aac66-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="aac66-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac66-130">Tipo de datos: **CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="aac66-130">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="aac66-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aac66-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aac66-132">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="aac66-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="aac66-133">Un [**\_ PhysicalMemory de CIM**](cim-physicalmemory.md) que describe la memoria física que se encuentra en la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="aac66-133">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) describing the physical memory which is located on the card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aac66-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aac66-134">Remarks</span></span>

<span data-ttu-id="aac66-135">La clase **CIM \_ MemoryOnCard** se deriva de [**\_ PackagedComponent de CIM**](cim-packagedcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="aac66-135">The **CIM\_MemoryOnCard** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

<span data-ttu-id="aac66-136">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="aac66-136">WMI does not implement this class.</span></span>

<span data-ttu-id="aac66-137">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="aac66-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aac66-138">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="aac66-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aac66-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aac66-139">Requirements</span></span>



| <span data-ttu-id="aac66-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="aac66-140">Requirement</span></span> | <span data-ttu-id="aac66-141">Value</span><span class="sxs-lookup"><span data-stu-id="aac66-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aac66-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aac66-142">Minimum supported client</span></span><br/> | <span data-ttu-id="aac66-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aac66-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aac66-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aac66-144">Minimum supported server</span></span><br/> | <span data-ttu-id="aac66-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aac66-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aac66-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aac66-146">Namespace</span></span><br/>                | <span data-ttu-id="aac66-147">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aac66-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aac66-148">MOF</span><span class="sxs-lookup"><span data-stu-id="aac66-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aac66-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aac66-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aac66-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aac66-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aac66-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aac66-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aac66-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="aac66-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aac66-153">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="aac66-153">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> </dl>

 

