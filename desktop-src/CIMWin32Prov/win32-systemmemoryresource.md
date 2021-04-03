---
description: La \_ clase WMI abstracta SystemMemoryResource de Win32 representa un recurso de memoria del sistema en un equipo que ejecuta Windows.
ms.assetid: a834a1e4-f3e4-4b57-9521-98520c301016
ms.tgt_platform: multiple
title: Win32_SystemMemoryResource (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemMemoryResource
- Win32_SystemMemoryResource.Caption
- Win32_SystemMemoryResource.Description
- Win32_SystemMemoryResource.InstallDate
- Win32_SystemMemoryResource.Name
- Win32_SystemMemoryResource.Status
- Win32_SystemMemoryResource.CreationClassName
- Win32_SystemMemoryResource.CSCreationClassName
- Win32_SystemMemoryResource.CSName
- Win32_SystemMemoryResource.EndingAddress
- Win32_SystemMemoryResource.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6064f2d983978998c47518ee50b93c3a7fedfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907497"
---
# <a name="win32_systemmemoryresource-class"></a><span data-ttu-id="89b90-103">\_Clase Win32 SystemMemoryResource</span><span class="sxs-lookup"><span data-stu-id="89b90-103">Win32\_SystemMemoryResource class</span></span>

<span data-ttu-id="89b90-104">La [clase WMI](../wmisdk/retrieving-a-class.md) abstracta **\_ SystemMemoryResource de Win32** representa un recurso de memoria del sistema en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="89b90-104">The **Win32\_SystemMemoryResource** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a system memory resource on a computer system running Windows.</span></span>

<span data-ttu-id="89b90-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="89b90-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="89b90-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="89b90-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89b90-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89b90-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4CE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemMemoryResource : CIM_MemoryMappedIO
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint64   EndingAddress;
  uint64   StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="89b90-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="89b90-108">Members</span></span>

<span data-ttu-id="89b90-109">La **clase \_ SystemMemoryResource de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="89b90-109">The **Win32\_SystemMemoryResource** class has these types of members:</span></span>

-   [<span data-ttu-id="89b90-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="89b90-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89b90-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="89b90-111">Properties</span></span>

<span data-ttu-id="89b90-112">La **clase \_ SystemMemoryResource de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="89b90-112">The **Win32\_SystemMemoryResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89b90-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="89b90-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b90-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="89b90-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89b90-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89b90-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b90-116">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="89b90-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="89b90-117">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="89b90-117">A short textual description of the object.</span></span>

<span data-ttu-id="89b90-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89b90-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="89b90-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b90-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="89b90-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89b90-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89b90-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b90-122">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="89b90-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="89b90-123">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="89b90-123">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="89b90-124">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="89b90-124">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="89b90-125">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="89b90-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="89b90-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b90-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="89b90-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89b90-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89b90-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b90-129">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="89b90-129">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="89b90-130">Propiedad **CreationClassName** del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="89b90-130">Scoping computer system's **CreationClassName** property.</span></span>

<span data-ttu-id="89b90-131">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="89b90-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="89b90-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b90-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="89b90-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89b90-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89b90-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b90-135">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="89b90-135">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="89b90-136">Propiedad **nombre** del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="89b90-136">Scoping computer system's **Name** property.</span></span>

<span data-ttu-id="89b90-137">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="89b90-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89b90-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b90-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="89b90-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89b90-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89b90-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b90-141">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="89b90-141">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="89b90-142">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="89b90-142">A textual description of the object.</span></span>

<span data-ttu-id="89b90-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89b90-144">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="89b90-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b90-145">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89b90-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89b90-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89b90-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b90-147">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s asignada de memoria DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="89b90-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="89b90-148">Dirección final de e/s asignada a la memoria.</span><span class="sxs-lookup"><span data-stu-id="89b90-148">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="89b90-149">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="89b90-150">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-150">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="89b90-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="89b90-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b90-152">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="89b90-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="89b90-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89b90-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b90-154">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="89b90-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="89b90-155">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="89b90-155">Indicates when the object was installed.</span></span> <span data-ttu-id="89b90-156">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="89b90-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="89b90-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89b90-158">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="89b90-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b90-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="89b90-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89b90-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89b90-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b90-161">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="89b90-161">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="89b90-162">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="89b90-162">Label by which the object is known.</span></span> <span data-ttu-id="89b90-163">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="89b90-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="89b90-164">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89b90-165">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="89b90-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b90-166">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89b90-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89b90-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89b90-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b90-168">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s asignada de memoria DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="89b90-168">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="89b90-169">Dirección inicial de e/s asignada a la memoria.</span><span class="sxs-lookup"><span data-stu-id="89b90-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="89b90-170">La propiedad de identificador de recursos de hardware debe establecerse en este valor para construir la clave de recurso de e/s asignada.</span><span class="sxs-lookup"><span data-stu-id="89b90-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="89b90-171">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="89b90-172">Esta propiedad se hereda de [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-172">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="89b90-173">**Estado**</span><span class="sxs-lookup"><span data-stu-id="89b90-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b90-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="89b90-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89b90-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89b90-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b90-176">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="89b90-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="89b90-177">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="89b90-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="89b90-178">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="89b90-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="89b90-179">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="89b90-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="89b90-180">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="89b90-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="89b90-181">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="89b90-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="89b90-182">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="89b90-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="89b90-183">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="89b90-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="89b90-184">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="89b90-185">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="89b90-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="89b90-186">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="89b90-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="89b90-187">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="89b90-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="89b90-188">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="89b90-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89b90-189">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="89b90-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="89b90-190">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="89b90-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="89b90-191">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="89b90-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="89b90-192">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="89b90-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="89b90-193">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="89b90-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="89b90-194">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="89b90-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="89b90-195">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="89b90-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="89b90-196">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="89b90-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="89b90-197">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="89b90-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="89b90-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="89b90-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="89b90-199">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89b90-199">Remarks</span></span>

<span data-ttu-id="89b90-200">La **clase \_ SystemMemoryResource de Win32** se deriva de [**\_ MemoryMappedIO de CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="89b90-200">The **Win32\_SystemMemoryResource** class is derived from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89b90-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89b90-201">Requirements</span></span>



| <span data-ttu-id="89b90-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="89b90-202">Requirement</span></span> | <span data-ttu-id="89b90-203">Value</span><span class="sxs-lookup"><span data-stu-id="89b90-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89b90-204">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89b90-204">Minimum supported client</span></span><br/> | <span data-ttu-id="89b90-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89b90-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89b90-206">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89b90-206">Minimum supported server</span></span><br/> | <span data-ttu-id="89b90-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89b90-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89b90-208">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="89b90-208">Namespace</span></span><br/>                | <span data-ttu-id="89b90-209">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="89b90-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89b90-210">MOF</span><span class="sxs-lookup"><span data-stu-id="89b90-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89b90-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89b90-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89b90-212">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89b90-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89b90-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89b90-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b90-214">Vea también</span><span class="sxs-lookup"><span data-stu-id="89b90-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b90-215">**\_MEMORYMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="89b90-215">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dt>

[<span data-ttu-id="89b90-216">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="89b90-216">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
