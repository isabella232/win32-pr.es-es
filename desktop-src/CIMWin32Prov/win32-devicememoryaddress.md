---
description: La \_ clase WMI DeviceMemoryAddress de Win32 representa una dirección de memoria del dispositivo en un equipo que ejecuta Windows.
ms.assetid: f0a70724-5ced-47fe-b17e-e153e65b80df
ms.tgt_platform: multiple
title: Win32_DeviceMemoryAddress (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aa7472e3c20808ff52f6f45b0dca57fd19f9dd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000727"
---
# <a name="win32_devicememoryaddress-class"></a><span data-ttu-id="7cc56-103">\_Clase Win32 DeviceMemoryAddress</span><span class="sxs-lookup"><span data-stu-id="7cc56-103">Win32\_DeviceMemoryAddress class</span></span>

<span data-ttu-id="7cc56-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DeviceMemoryAddress de Win32** representa una dirección de memoria del dispositivo en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="7cc56-104">The **Win32\_DeviceMemoryAddress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a device memory address on a computer system running Windows.</span></span>

<span data-ttu-id="7cc56-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7cc56-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7cc56-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7cc56-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cc56-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cc56-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceMemoryAddress : Win32_SystemMemoryResource
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   MemoryType;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="7cc56-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7cc56-108">Members</span></span>

<span data-ttu-id="7cc56-109">La **clase \_ DeviceMemoryAddress de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7cc56-109">The **Win32\_DeviceMemoryAddress** class has these types of members:</span></span>

-   [<span data-ttu-id="7cc56-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7cc56-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7cc56-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7cc56-111">Properties</span></span>

<span data-ttu-id="7cc56-112">La **clase \_ DeviceMemoryAddress de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7cc56-112">The **Win32\_DeviceMemoryAddress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7cc56-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7cc56-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cc56-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7cc56-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cc56-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-116">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7cc56-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7cc56-117">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="7cc56-117">Short description of the object a one-line string.</span></span>

<span data-ttu-id="7cc56-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cc56-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7cc56-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cc56-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7cc56-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cc56-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-122">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7cc56-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7cc56-123">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="7cc56-123">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="7cc56-124">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="7cc56-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="7cc56-125">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cc56-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7cc56-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cc56-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7cc56-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cc56-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-129">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7cc56-129">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7cc56-130">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7cc56-130">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="7cc56-131">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cc56-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="7cc56-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cc56-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7cc56-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cc56-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-135">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7cc56-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7cc56-136">Nombre del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="7cc56-136">Name of the scoping computer system.</span></span>

<span data-ttu-id="7cc56-137">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cc56-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7cc56-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cc56-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7cc56-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cc56-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-141">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7cc56-141">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7cc56-142">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="7cc56-142">Description of the object.</span></span>

<span data-ttu-id="7cc56-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cc56-144">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="7cc56-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cc56-145">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7cc56-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cc56-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-147">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s asignada de memoria DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="7cc56-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="7cc56-148">Dirección final de e/s asignada a la memoria.</span><span class="sxs-lookup"><span data-stu-id="7cc56-148">Ending address of memory-mapped I/O.</span></span>

<span data-ttu-id="7cc56-149">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-149">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="7cc56-150">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7cc56-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="7cc56-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7cc56-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cc56-152">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7cc56-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cc56-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-154">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7cc56-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7cc56-155">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="7cc56-155">Date and time the object was installed.</span></span> <span data-ttu-id="7cc56-156">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="7cc56-156">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7cc56-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cc56-158">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="7cc56-158">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cc56-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7cc56-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cc56-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-161">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| marcas de \| \_ descriptor de recursos parciales de inesperados win32api SystemStructures cm \_ \_ \| ")</span><span class="sxs-lookup"><span data-stu-id="7cc56-161">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SystemStructures\|CM\_PARTIAL\_RESOURCE\_DESCRIPTOR\|Flags")</span></span>
</dt> </dl>

<span data-ttu-id="7cc56-162">Características del recurso de memoria en el equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="7cc56-162">Characteristics of the memory resource on the computer system running Windows.</span></span> <span data-ttu-id="7cc56-163">Los valores son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="7cc56-163">Values are the following.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="7cc56-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span><span class="sxs-lookup"><span data-stu-id="7cc56-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span></span>


</dt> <dd>

<span data-ttu-id="7cc56-165">La memoria se puede leer y escribir.</span><span class="sxs-lookup"><span data-stu-id="7cc56-165">The memory can be both read and written.</span></span>

</dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="7cc56-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("readonly")</span><span class="sxs-lookup"><span data-stu-id="7cc56-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")</span></span>


</dt> <dd>

<span data-ttu-id="7cc56-167">La memoria es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7cc56-167">The memory is read-only.</span></span>

</dd> <dt>

<span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>

<span data-ttu-id="7cc56-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span><span class="sxs-lookup"><span data-stu-id="7cc56-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span></span>


</dt> <dd>

<span data-ttu-id="7cc56-169">La memoria solo se puede escribir.</span><span class="sxs-lookup"><span data-stu-id="7cc56-169">The memory can only be written.</span></span>

</dd> <dt>

<span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>

<span data-ttu-id="7cc56-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Captura previa** ("captura previa")</span><span class="sxs-lookup"><span data-stu-id="7cc56-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetchable** ("Prefetchable")</span></span>


</dt> <dd>

<span data-ttu-id="7cc56-171">Un bloque de memoria se copia de la memoria principal en un búfer pequeño administrado por el chipset de memoria.</span><span class="sxs-lookup"><span data-stu-id="7cc56-171">A block of memory is copied from main memory into a small buffer managed by the memory chipset.</span></span> <span data-ttu-id="7cc56-172">Las operaciones de lectura repetidas de la misma parte de la memoria son más rápidas con la memoria que se captura previamente.</span><span class="sxs-lookup"><span data-stu-id="7cc56-172">Repeated read operations from the same part of memory are faster with prefetchable memory.</span></span>

</dd> <dt>

<span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>

<span data-ttu-id="7cc56-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")</span><span class="sxs-lookup"><span data-stu-id="7cc56-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")</span></span>


</dt> <dd>

<span data-ttu-id="7cc56-174">TBD</span><span class="sxs-lookup"><span data-stu-id="7cc56-174">TBD</span></span>

</dd> <dt>

<span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>

<span data-ttu-id="7cc56-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span><span class="sxs-lookup"><span data-stu-id="7cc56-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span></span>


</dt> <dd>

<span data-ttu-id="7cc56-176">TBD</span><span class="sxs-lookup"><span data-stu-id="7cc56-176">TBD</span></span>

</dd> <dt>

<span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>

<span data-ttu-id="7cc56-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Almacenable en caché** ("almacenable en caché")</span><span class="sxs-lookup"><span data-stu-id="7cc56-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Cacheable** ("Cacheable")</span></span>


</dt> <dd>

<span data-ttu-id="7cc56-178">TBD</span><span class="sxs-lookup"><span data-stu-id="7cc56-178">TBD</span></span>

</dd> <dt>

<span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>

<span data-ttu-id="7cc56-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")</span><span class="sxs-lookup"><span data-stu-id="7cc56-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")</span></span>


</dt> <dd>

<span data-ttu-id="7cc56-180">TBD</span><span class="sxs-lookup"><span data-stu-id="7cc56-180">TBD</span></span>

</dd> <dt>

<span id="Bar"></span><span id="bar"></span><span id="BAR"></span>

<span data-ttu-id="7cc56-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Barra** ("bar")</span><span class="sxs-lookup"><span data-stu-id="7cc56-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Bar** ("Bar")</span></span>


</dt> <dd>

<span data-ttu-id="7cc56-182">TBD</span><span class="sxs-lookup"><span data-stu-id="7cc56-182">TBD</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7cc56-183">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7cc56-183">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cc56-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7cc56-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cc56-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-186">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7cc56-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7cc56-187">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="7cc56-187">Label by which the object is known.</span></span> <span data-ttu-id="7cc56-188">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="7cc56-188">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="7cc56-189">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cc56-190">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="7cc56-190">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cc56-191">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7cc56-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cc56-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-193">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s asignada de memoria DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="7cc56-193">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="7cc56-194">Dirección inicial de e/s asignada a la memoria.</span><span class="sxs-lookup"><span data-stu-id="7cc56-194">Starting address of memory-mapped I/O.</span></span> <span data-ttu-id="7cc56-195">La propiedad de identificador de recursos de hardware debe establecerse en este valor para construir la clave de recurso de e/s asignada.</span><span class="sxs-lookup"><span data-stu-id="7cc56-195">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="7cc56-196">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-196">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="7cc56-197">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7cc56-197">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="7cc56-198">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7cc56-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cc56-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7cc56-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cc56-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cc56-201">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="7cc56-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7cc56-202">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7cc56-202">Current status of the object.</span></span> <span data-ttu-id="7cc56-203">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="7cc56-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7cc56-204">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="7cc56-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7cc56-205">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="7cc56-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7cc56-206">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="7cc56-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7cc56-207">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="7cc56-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7cc56-208">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7cc56-209">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7cc56-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7cc56-210">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7cc56-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7cc56-211">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7cc56-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7cc56-212">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7cc56-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7cc56-213">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7cc56-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7cc56-214">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7cc56-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7cc56-215">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7cc56-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7cc56-216">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7cc56-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7cc56-217">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7cc56-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7cc56-218">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7cc56-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7cc56-219">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7cc56-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7cc56-220">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7cc56-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7cc56-221">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7cc56-221">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="7cc56-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7cc56-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7cc56-223">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7cc56-223">Remarks</span></span>

<span data-ttu-id="7cc56-224">La **clase \_ DeviceMemoryAddress de Win32** se deriva de [**\_ SystemMemoryResource de Win32**](win32-systemmemoryresource.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-224">The **Win32\_DeviceMemoryAddress** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cc56-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cc56-225">Requirements</span></span>



| <span data-ttu-id="7cc56-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cc56-226">Requirement</span></span> | <span data-ttu-id="7cc56-227">Value</span><span class="sxs-lookup"><span data-stu-id="7cc56-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc56-228">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cc56-228">Minimum supported client</span></span><br/> | <span data-ttu-id="7cc56-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cc56-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7cc56-230">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cc56-230">Minimum supported server</span></span><br/> | <span data-ttu-id="7cc56-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cc56-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7cc56-232">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7cc56-232">Namespace</span></span><br/>                | <span data-ttu-id="7cc56-233">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7cc56-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7cc56-234">MOF</span><span class="sxs-lookup"><span data-stu-id="7cc56-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cc56-235"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7cc56-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cc56-236">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7cc56-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cc56-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cc56-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cc56-238">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cc56-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cc56-239">**Win32 \_ SystemMemoryResource**</span><span class="sxs-lookup"><span data-stu-id="7cc56-239">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="7cc56-240">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="7cc56-240">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

