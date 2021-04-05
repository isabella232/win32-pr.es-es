---
description: La \_ clase WMI PhysicalMemoryLocation Association de Win32 relaciona una matriz de memoria física y su memoria física.
ms.assetid: 40252428-77ca-4dfb-8048-c05096a114d8
ms.tgt_platform: multiple
title: Win32_PhysicalMemoryLocation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryLocation
- Win32_PhysicalMemoryLocation.LocationWithinContainer
- Win32_PhysicalMemoryLocation.PartComponent
- Win32_PhysicalMemoryLocation.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daa6d47b13cb5caa74a10f28ab5fcd6e66e1524f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000821"
---
# <a name="win32_physicalmemorylocation-class"></a><span data-ttu-id="72788-103">\_Clase Win32 PhysicalMemoryLocation</span><span class="sxs-lookup"><span data-stu-id="72788-103">Win32\_PhysicalMemoryLocation class</span></span>

<span data-ttu-id="72788-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PhysicalMemoryLocation** Association de Win32 relaciona una matriz de memoria física y su memoria física.</span><span class="sxs-lookup"><span data-stu-id="72788-104">The **Win32\_PhysicalMemoryLocation** association [WMI class](../wmisdk/retrieving-a-class.md) relates an array of physical memory and its physical memory.</span></span>

<span data-ttu-id="72788-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="72788-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="72788-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="72788-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="72788-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72788-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="72788-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="72788-108">Members</span></span>

<span data-ttu-id="72788-109">La **clase \_ PhysicalMemoryLocation de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="72788-109">The **Win32\_PhysicalMemoryLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="72788-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72788-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72788-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72788-111">Properties</span></span>

<span data-ttu-id="72788-112">La **clase \_ PhysicalMemoryLocation de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="72788-112">The **Win32\_PhysicalMemoryLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72788-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="72788-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72788-114">Tipo de datos: **Win32 \_ PhysicalMemoryArray**</span><span class="sxs-lookup"><span data-stu-id="72788-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="72788-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72788-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72788-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemoryArray")</span><span class="sxs-lookup"><span data-stu-id="72788-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="72788-117">[**\_ PhysicalMemoryArray de Win32**](win32-physicalmemoryarray.md) que representa la matriz de memoria física que contiene la memoria física.</span><span class="sxs-lookup"><span data-stu-id="72788-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that represents the physical memory array that contains the physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="72788-118">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="72788-118">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72788-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72788-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72788-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72788-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72788-121">Cadena de forma libre que representa la posición del elemento físico en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="72788-121">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="72788-122">La información relativa a los elementos estacionarios del contenedor (por ejemplo, "segunda Bahía de unidad de la parte superior"), ángulos, altitudes y otros datos se puede grabar en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="72788-122">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="72788-123">Esta cadena se puede complementar o utilizar en lugar de crear una instancia del objeto de [**\_ Ubicación CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="72788-123">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="72788-124">Esta propiedad se hereda del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="72788-124">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="72788-125">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="72788-125">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72788-126">Tipo de datos: **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="72788-126">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="72788-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72788-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72788-128">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemory")</span><span class="sxs-lookup"><span data-stu-id="72788-128">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="72788-129">[**\_ PhysicalMemory de Win32**](win32-physicalmemory.md) que representa la memoria física incluida en la matriz de memoria física.</span><span class="sxs-lookup"><span data-stu-id="72788-129">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory contained in the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72788-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72788-130">Remarks</span></span>

<span data-ttu-id="72788-131">La **clase \_ PhysicalMemoryLocation de Win32** se deriva de [**\_ PackagedComponent de CIM**](cim-packagedcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="72788-131">The **Win32\_PhysicalMemoryLocation** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72788-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72788-132">Requirements</span></span>



| <span data-ttu-id="72788-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="72788-133">Requirement</span></span> | <span data-ttu-id="72788-134">Value</span><span class="sxs-lookup"><span data-stu-id="72788-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72788-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72788-135">Minimum supported client</span></span><br/> | <span data-ttu-id="72788-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72788-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72788-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72788-137">Minimum supported server</span></span><br/> | <span data-ttu-id="72788-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72788-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72788-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="72788-139">Namespace</span></span><br/>                | <span data-ttu-id="72788-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="72788-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72788-141">MOF</span><span class="sxs-lookup"><span data-stu-id="72788-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72788-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72788-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72788-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72788-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72788-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72788-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72788-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="72788-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72788-146">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="72788-146">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dt>

[<span data-ttu-id="72788-147">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="72788-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
