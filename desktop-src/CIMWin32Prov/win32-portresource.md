---
description: La \_ clase WMI PortResource de Win32 representa un puerto de e/s en un equipo que ejecuta Windows.
ms.assetid: 820f4f49-571c-4044-aefc-69bac5d59e6f
ms.tgt_platform: multiple
title: Win32_PortResource (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortResource
- Win32_PortResource.Alias
- Win32_PortResource.Caption
- Win32_PortResource.CreationClassName
- Win32_PortResource.CSCreationClassName
- Win32_PortResource.CSName
- Win32_PortResource.Description
- Win32_PortResource.EndingAddress
- Win32_PortResource.InstallDate
- Win32_PortResource.Name
- Win32_PortResource.StartingAddress
- Win32_PortResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3c08424dd1aee555068c78a9308afe732634c61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998151"
---
# <a name="win32_portresource-class"></a><span data-ttu-id="741c8-103">\_Clase Win32 PortResource</span><span class="sxs-lookup"><span data-stu-id="741c8-103">Win32\_PortResource class</span></span>

<span data-ttu-id="741c8-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PortResource de Win32** representa un puerto de e/s en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="741c8-104">The **Win32\_PortResource** [WMI class](../wmisdk/retrieving-a-class.md) represents an I/O port on a computer system running Windows.</span></span>

<span data-ttu-id="741c8-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="741c8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="741c8-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="741c8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="741c8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="741c8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PortResource : Win32_SystemMemoryResource
{
  boolean  Alias;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="741c8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="741c8-108">Members</span></span>

<span data-ttu-id="741c8-109">La **clase \_ PortResource de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="741c8-109">The **Win32\_PortResource** class has these types of members:</span></span>

-   [<span data-ttu-id="741c8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="741c8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="741c8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="741c8-111">Properties</span></span>

<span data-ttu-id="741c8-112">La **clase \_ PortResource de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="741c8-112">The **Win32\_PortResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="741c8-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="741c8-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="741c8-114">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="741c8-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="741c8-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="741c8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="741c8-116">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| información de e/s de estructuras de inesperados win32api Configuration Manager \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="741c8-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Configuration Manager Structures\|IO\_INFO")</span></span>
</dt> </dl>

<span data-ttu-id="741c8-117">Si **es true**, esta instancia representa uno de los intervalos con un alias.</span><span class="sxs-lookup"><span data-stu-id="741c8-117">If **TRUE**, this instance represents one of the ranges with an alias.</span></span> <span data-ttu-id="741c8-118">Si **es false**, la instancia representa una dirección de puerto base.</span><span class="sxs-lookup"><span data-stu-id="741c8-118">If **FALSE**, the instance represents a base port address.</span></span> <span data-ttu-id="741c8-119">Una dirección de puerto base es una dirección de Puerto predeterminada dedicada a un servicio o un dispositivo específicos.</span><span class="sxs-lookup"><span data-stu-id="741c8-119">A base port address is a predetermined port address dedicated to a specific service or device.</span></span> <span data-ttu-id="741c8-120">Una dirección de alias de puerto es aquella a la que responde un dispositivo como si fuera la dirección real de un puerto de e/s.</span><span class="sxs-lookup"><span data-stu-id="741c8-120">A port alias address is one that a device responds to as if it were the actual address of an I/O port.</span></span>

</dd> <dt>

<span data-ttu-id="741c8-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="741c8-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="741c8-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="741c8-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="741c8-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="741c8-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="741c8-124">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="741c8-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="741c8-125">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="741c8-125">Short description of the object.</span></span>

<span data-ttu-id="741c8-126">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="741c8-127">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="741c8-127">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="741c8-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="741c8-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="741c8-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="741c8-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="741c8-130">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="741c8-130">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="741c8-131">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="741c8-131">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="741c8-132">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="741c8-132">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="741c8-133">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-133">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="741c8-134">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="741c8-134">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="741c8-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="741c8-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="741c8-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="741c8-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="741c8-137">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="741c8-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="741c8-138">Nombre de la clase de creación del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="741c8-138">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="741c8-139">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-139">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="741c8-140">**CSName**</span><span class="sxs-lookup"><span data-stu-id="741c8-140">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="741c8-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="741c8-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="741c8-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="741c8-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="741c8-143">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="741c8-143">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="741c8-144">Nombre del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="741c8-144">Name of the scoping computer system.</span></span>

<span data-ttu-id="741c8-145">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-145">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="741c8-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="741c8-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="741c8-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="741c8-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="741c8-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="741c8-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="741c8-149">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="741c8-149">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="741c8-150">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="741c8-150">Description of the object.</span></span>

<span data-ttu-id="741c8-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="741c8-152">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="741c8-152">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="741c8-153">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="741c8-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="741c8-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="741c8-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="741c8-155">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s asignada de memoria DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="741c8-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="741c8-156">Dirección final de e/s asignada a la memoria.</span><span class="sxs-lookup"><span data-stu-id="741c8-156">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="741c8-157">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-157">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="741c8-158">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="741c8-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="741c8-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="741c8-160">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="741c8-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="741c8-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="741c8-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="741c8-162">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="741c8-162">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="741c8-163">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="741c8-163">Date and time the object was installed.</span></span> <span data-ttu-id="741c8-164">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="741c8-164">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="741c8-165">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="741c8-166">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="741c8-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="741c8-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="741c8-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="741c8-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="741c8-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="741c8-169">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="741c8-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="741c8-170">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="741c8-170">Label by which the object is known.</span></span> <span data-ttu-id="741c8-171">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="741c8-171">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="741c8-172">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="741c8-173">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="741c8-173">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="741c8-174">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="741c8-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="741c8-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="741c8-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="741c8-176">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("StartingAddress"), [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s asignada de memoria DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="741c8-176">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartingAddress"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="741c8-177">Dirección inicial de e/s asignada a la memoria.</span><span class="sxs-lookup"><span data-stu-id="741c8-177">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="741c8-178">La propiedad de identificador de recursos de hardware debe establecerse en este valor para construir la clave de recurso de e/s asignada.</span><span class="sxs-lookup"><span data-stu-id="741c8-178">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="741c8-179">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-179">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="741c8-180">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="741c8-181">**Estado**</span><span class="sxs-lookup"><span data-stu-id="741c8-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="741c8-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="741c8-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="741c8-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="741c8-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="741c8-184">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="741c8-184">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="741c8-185">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="741c8-185">Current status of the object.</span></span> <span data-ttu-id="741c8-186">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="741c8-186">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="741c8-187">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="741c8-187">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="741c8-188">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="741c8-188">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="741c8-189">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="741c8-189">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="741c8-190">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="741c8-190">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="741c8-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="741c8-192">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="741c8-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="741c8-193">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="741c8-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="741c8-194">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="741c8-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="741c8-195">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="741c8-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="741c8-196">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="741c8-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="741c8-197">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="741c8-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="741c8-198">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="741c8-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="741c8-199">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="741c8-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="741c8-200">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="741c8-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="741c8-201">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="741c8-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="741c8-202">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="741c8-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="741c8-203">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="741c8-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="741c8-204">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="741c8-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="741c8-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="741c8-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="741c8-206">Observaciones</span><span class="sxs-lookup"><span data-stu-id="741c8-206">Remarks</span></span>

<span data-ttu-id="741c8-207">La **clase \_ PortResource de Win32** se deriva de [**\_ SystemMemoryResource de Win32**](win32-systemmemoryresource.md).</span><span class="sxs-lookup"><span data-stu-id="741c8-207">The **Win32\_PortResource** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="741c8-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="741c8-208">Requirements</span></span>



| <span data-ttu-id="741c8-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="741c8-209">Requirement</span></span> | <span data-ttu-id="741c8-210">Value</span><span class="sxs-lookup"><span data-stu-id="741c8-210">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="741c8-211">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="741c8-211">Minimum supported client</span></span><br/> | <span data-ttu-id="741c8-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="741c8-212">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="741c8-213">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="741c8-213">Minimum supported server</span></span><br/> | <span data-ttu-id="741c8-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="741c8-214">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="741c8-215">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="741c8-215">Namespace</span></span><br/>                | <span data-ttu-id="741c8-216">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="741c8-216">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="741c8-217">MOF</span><span class="sxs-lookup"><span data-stu-id="741c8-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="741c8-218"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="741c8-218"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="741c8-219">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="741c8-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="741c8-220"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="741c8-220"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="741c8-221">Vea también</span><span class="sxs-lookup"><span data-stu-id="741c8-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="741c8-222">**Win32 \_ SystemMemoryResource**</span><span class="sxs-lookup"><span data-stu-id="741c8-222">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="741c8-223">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="741c8-223">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
