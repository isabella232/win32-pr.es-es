---
description: La \_ clase CIM OperatingSystem representa un sistema operativo del equipo, que se compone de software y firmware que hace que el hardware del equipo sea utilizable.
ms.assetid: 014d2553-e1ac-4394-84ae-307af3658f6e
ms.tgt_platform: multiple
title: CIM_OperatingSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem
- CIM_OperatingSystem.Caption
- CIM_OperatingSystem.CreationClassName
- CIM_OperatingSystem.CSCreationClassName
- CIM_OperatingSystem.CSName
- CIM_OperatingSystem.CurrentTimeZone
- CIM_OperatingSystem.Description
- CIM_OperatingSystem.Distributed
- CIM_OperatingSystem.FreePhysicalMemory
- CIM_OperatingSystem.FreeSpaceInPagingFiles
- CIM_OperatingSystem.FreeVirtualMemory
- CIM_OperatingSystem.InstallDate
- CIM_OperatingSystem.LastBootUpTime
- CIM_OperatingSystem.LocalDateTime
- CIM_OperatingSystem.MaxNumberOfProcesses
- CIM_OperatingSystem.MaxProcessMemorySize
- CIM_OperatingSystem.Name
- CIM_OperatingSystem.NumberOfLicensedUsers
- CIM_OperatingSystem.NumberOfProcesses
- CIM_OperatingSystem.NumberOfUsers
- CIM_OperatingSystem.OSType
- CIM_OperatingSystem.OtherTypeDescription
- CIM_OperatingSystem.SizeStoredInPagingFiles
- CIM_OperatingSystem.Status
- CIM_OperatingSystem.TotalSwapSpaceSize
- CIM_OperatingSystem.TotalVirtualMemorySize
- CIM_OperatingSystem.TotalVisibleMemorySize
- CIM_OperatingSystem.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b4af54a0f086bee4b743b083c27a67777786bc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538961"
---
# <a name="cim_operatingsystem-class"></a><span data-ttu-id="339f2-103">CIM \_ OperatingSystem (clase)</span><span class="sxs-lookup"><span data-stu-id="339f2-103">CIM\_OperatingSystem class</span></span>

<span data-ttu-id="339f2-104">La clase **CIM \_ OperatingSystem** representa un sistema operativo del equipo, que se compone de software y firmware que hace que el hardware del equipo sea utilizable.</span><span class="sxs-lookup"><span data-stu-id="339f2-104">The **CIM\_OperatingSystem** class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="339f2-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="339f2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="339f2-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="339f2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="339f2-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="339f2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="339f2-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="339f2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="339f2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="339f2-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C565-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_OperatingSystem : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  sint16   CurrentTimeZone;
  string   Description;
  boolean  Distributed;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint16   OSType;
  string   OtherTypeDescription;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="339f2-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="339f2-110">Members</span></span>

<span data-ttu-id="339f2-111">La clase **CIM \_ OperatingSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="339f2-111">The **CIM\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="339f2-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="339f2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="339f2-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="339f2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="339f2-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="339f2-114">Methods</span></span>

<span data-ttu-id="339f2-115">La clase **CIM \_ OperatingSystem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="339f2-115">The **CIM\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="339f2-116">Método</span><span class="sxs-lookup"><span data-stu-id="339f2-116">Method</span></span>                                                           | <span data-ttu-id="339f2-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="339f2-117">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="339f2-118">**Reboot**</span><span class="sxs-lookup"><span data-stu-id="339f2-118">**Reboot**</span></span>](reboot-method-in-class-cim-operatingsystem.md)     | <span data-ttu-id="339f2-119">Método de clase que cierra el sistema del equipo y, a continuación, lo reinicia.</span><span class="sxs-lookup"><span data-stu-id="339f2-119">Class method that shuts down the computer system, then restarts it.</span></span> <span data-ttu-id="339f2-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="339f2-120">Not implemented by WMI.</span></span><br/>                                 |
| [<span data-ttu-id="339f2-121">**Apagado**</span><span class="sxs-lookup"><span data-stu-id="339f2-121">**Shutdown**</span></span>](shutdown-method-in-class-cim-operatingsystem.md) | <span data-ttu-id="339f2-122">Método de clase que descarga programas y archivos dll hasta el punto en el que es seguro apagar el equipo.</span><span class="sxs-lookup"><span data-stu-id="339f2-122">Class method that unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span> <span data-ttu-id="339f2-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="339f2-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="339f2-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="339f2-124">Properties</span></span>

<span data-ttu-id="339f2-125">La clase **CIM \_ OperatingSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="339f2-125">The **CIM\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="339f2-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="339f2-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="339f2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-129">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="339f2-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-130">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="339f2-130">Short textual description of the object.</span></span>

<span data-ttu-id="339f2-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="339f2-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="339f2-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="339f2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-135">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="339f2-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="339f2-136">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="339f2-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="339f2-137">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="339f2-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="339f2-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="339f2-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="339f2-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-141">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="339f2-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="339f2-142">Ámbito del nombre de la clase de creación del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="339f2-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="339f2-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="339f2-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="339f2-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-146">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="339f2-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="339f2-147">Ámbito del nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="339f2-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="339f2-148">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="339f2-148">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-149">Tipo de datos: **sint16**</span><span class="sxs-lookup"><span data-stu-id="339f2-149">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-151">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="339f2-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-152">Número de minutos que el sistema operativo se desvía de la hora del meridiano de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="339f2-152">Number of minutes the operating system is offset from Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="339f2-153">El número es positivo, negativo o cero.</span><span class="sxs-lookup"><span data-stu-id="339f2-153">The number is positive, negative, or zero.</span></span>

</dd> <dt>

<span data-ttu-id="339f2-154">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="339f2-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="339f2-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-157">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="339f2-157">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-158">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="339f2-158">Textual description of the object.</span></span>

<span data-ttu-id="339f2-159">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="339f2-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-160">**Distribuya**</span><span class="sxs-lookup"><span data-stu-id="339f2-160">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-161">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="339f2-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339f2-163">Si es **true**, el sistema operativo se distribuye entre varios nodos de sistema de equipo, que se deben agrupar como un clúster.</span><span class="sxs-lookup"><span data-stu-id="339f2-163">If **TRUE**, the operating system is distributed across several computer system nodes, which should be grouped as a cluster.</span></span>

</dd> <dt>

<span data-ttu-id="339f2-164">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="339f2-164">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-165">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="339f2-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-167">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="339f2-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-168">Número de kilobytes de memoria física actualmente sin usar y disponibles.</span><span class="sxs-lookup"><span data-stu-id="339f2-168">Number of kilobytes of physical memory currently unused and available.</span></span>

<span data-ttu-id="339f2-169">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="339f2-169">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-170">**FreeSpaceInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="339f2-170">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-171">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="339f2-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-173">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Configuración de la memoria del sistema DMTF \| 001,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="339f2-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-174">Número de kilobytes que se pueden asignar a los archivos de paginación del sistema operativo sin que se produzca el intercambio de otras páginas. Un valor de 0 indica que no hay ningún archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="339f2-174">Number of kilobytes that can be mapped into the operating system's paging files without causing other pages to be swapped out. A value of 0 indicates that there are no paging files.</span></span>

<span data-ttu-id="339f2-175">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="339f2-175">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-176">**Freevirtualmemory (**</span><span class="sxs-lookup"><span data-stu-id="339f2-176">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-177">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="339f2-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-179">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="339f2-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-180">Número de kilobytes de memoria virtual actualmente sin usar y disponibles.</span><span class="sxs-lookup"><span data-stu-id="339f2-180">Number of kilobytes of virtual memory currently unused and available.</span></span> <span data-ttu-id="339f2-181">Por ejemplo, esto puede calcularse agregando la cantidad de RAM disponible a la cantidad de espacio de paginación libre (es decir, agregando las propiedades **FreePhysicalMemory** y **FreeSpaceInPagingFiles** ).</span><span class="sxs-lookup"><span data-stu-id="339f2-181">For example, this can be calculated by adding the amount of free RAM to the amount of free paging space (that is, adding the **FreePhysicalMemory** and **FreeSpaceInPagingFiles** properties).</span></span>

<span data-ttu-id="339f2-182">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="339f2-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-183">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="339f2-183">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-184">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="339f2-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-186">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="339f2-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-187">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="339f2-187">Date and time the object was installed.</span></span> <span data-ttu-id="339f2-188">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="339f2-188">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="339f2-189">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="339f2-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-190">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="339f2-190">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-191">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="339f2-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339f2-193">Hora en que el sistema operativo se arrancó por última vez.</span><span class="sxs-lookup"><span data-stu-id="339f2-193">Time when the operating system was last booted.</span></span>

</dd> <dt>

<span data-ttu-id="339f2-194">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="339f2-194">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-195">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="339f2-195">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-197">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrSystemDate "," MIF. \|Información general de DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="339f2-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-198">Noción del sistema operativo de la fecha y hora locales del día.</span><span class="sxs-lookup"><span data-stu-id="339f2-198">Operating system's notion of the local date and time of day.</span></span>

</dd> <dt>

<span data-ttu-id="339f2-199">**MaxNumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="339f2-199">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-200">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="339f2-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-202">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrSystemMaxProcesses ")</span><span class="sxs-lookup"><span data-stu-id="339f2-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-203">Número máximo de contextos de proceso que el sistema operativo puede admitir.</span><span class="sxs-lookup"><span data-stu-id="339f2-203">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="339f2-204">Si no hay ningún máximo fijo, el valor debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="339f2-204">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="339f2-205">En los sistemas que tienen un máximo fijo, este objeto puede ayudar a diagnosticar los errores que se producen cuando se alcanza el máximo.</span><span class="sxs-lookup"><span data-stu-id="339f2-205">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached.</span></span> <span data-ttu-id="339f2-206">Si es desconocido, escriba-1.</span><span class="sxs-lookup"><span data-stu-id="339f2-206">If unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="339f2-207">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="339f2-207">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-208">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="339f2-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-210">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="339f2-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-211">Número máximo de kilobytes de memoria que se pueden asignar a un proceso.</span><span class="sxs-lookup"><span data-stu-id="339f2-211">Maximum number of kilobytes of memory that can be allocated to a process.</span></span> <span data-ttu-id="339f2-212">En el caso de los sistemas operativos sin memoria virtual, este valor suele ser igual a la cantidad total de memoria física, menos la memoria usada por el BIOS y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="339f2-212">For operating systems with no virtual memory, this value is typically equal to the total amount of physical memory, minus memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="339f2-213">En algunos sistemas operativos, este valor puede ser infinito, en cuyo caso se debe especificar 0.</span><span class="sxs-lookup"><span data-stu-id="339f2-213">For some operating systems, this value can be infinity, in which case 0 should be entered.</span></span> <span data-ttu-id="339f2-214">En otros casos, este valor puede ser una constante, por ejemplo, 2 GB o 4 GB.</span><span class="sxs-lookup"><span data-stu-id="339f2-214">In other cases, this value can be a constant, for example, 2 GB or 4 GB.</span></span>

<span data-ttu-id="339f2-215">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="339f2-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-216">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="339f2-216">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="339f2-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-219">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="339f2-219">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-220">Clave de una instancia del sistema operativo dentro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="339f2-220">Key of an operating system instance within a computer system.</span></span>

<span data-ttu-id="339f2-221">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="339f2-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-222">**NumberOfLicensedUsers**</span><span class="sxs-lookup"><span data-stu-id="339f2-222">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-223">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="339f2-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339f2-225">Número de licencias de usuario para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="339f2-225">Number of user licenses for the operating system.</span></span> <span data-ttu-id="339f2-226">Si es ilimitado, escriba 0, si es desconocido, escriba-1.</span><span class="sxs-lookup"><span data-stu-id="339f2-226">If unlimited, enter 0, if unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="339f2-227">**NumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="339f2-227">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-228">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="339f2-228">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-230">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrSystemProcesses ")</span><span class="sxs-lookup"><span data-stu-id="339f2-230">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-231">Número de contextos de proceso cargados o en ejecución actualmente en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="339f2-231">Number of process contexts currently loaded or running on the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="339f2-232">**NumberOfUsers**</span><span class="sxs-lookup"><span data-stu-id="339f2-232">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-233">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="339f2-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-235">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrSystemNumUsers ")</span><span class="sxs-lookup"><span data-stu-id="339f2-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-236">Número de sesiones de usuario para las que el sistema operativo está almacenando actualmente información de estado.</span><span class="sxs-lookup"><span data-stu-id="339f2-236">Number of user sessions for which the operating system is currently storing state information.</span></span>

</dd> <dt>

<span data-ttu-id="339f2-237">**OSType**</span><span class="sxs-lookup"><span data-stu-id="339f2-237">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-238">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="339f2-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-240">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ OperatingSystem**.**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="339f2-240">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-241">Tipo de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="339f2-241">Type of operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="339f2-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="339f2-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="339f2-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="339f2-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="339f2-244"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="339f2-244"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-245">Mac OS</span><span class="sxs-lookup"><span data-stu-id="339f2-245">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="339f2-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="339f2-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-247">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="339f2-247">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="339f2-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="339f2-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="339f2-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="339f2-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="339f2-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="339f2-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="339f2-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="339f2-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-252">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="339f2-252">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="339f2-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="339f2-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-254">HP-UX</span><span class="sxs-lookup"><span data-stu-id="339f2-254">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="339f2-255"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="339f2-255"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="339f2-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="339f2-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="339f2-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="339f2-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="339f2-258"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="339f2-258"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="339f2-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="339f2-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-260">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="339f2-260">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="339f2-261"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="339f2-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="339f2-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="339f2-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-263">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="339f2-263">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="339f2-264"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="339f2-264"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-265">Windows 95</span><span class="sxs-lookup"><span data-stu-id="339f2-265">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="339f2-266"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="339f2-266"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-267">Windows 98</span><span class="sxs-lookup"><span data-stu-id="339f2-267">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="339f2-268"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="339f2-268"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-269">Windows NT</span><span class="sxs-lookup"><span data-stu-id="339f2-269">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="339f2-270"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="339f2-270"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-271">Windows CE</span><span class="sxs-lookup"><span data-stu-id="339f2-271">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="339f2-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="339f2-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-273">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="339f2-273">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="339f2-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="339f2-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="339f2-275"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="339f2-275"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="339f2-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="339f2-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="339f2-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="339f2-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="339f2-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="339f2-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="339f2-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="339f2-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="339f2-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="339f2-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="339f2-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="339f2-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="339f2-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="339f2-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="339f2-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="339f2-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="339f2-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="339f2-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="339f2-285"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="339f2-285"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-286">Una serie</span><span class="sxs-lookup"><span data-stu-id="339f2-286">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="339f2-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="339f2-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-288">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="339f2-288">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="339f2-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="339f2-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-290">Tándem</span><span class="sxs-lookup"><span data-stu-id="339f2-290">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="339f2-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="339f2-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-292">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="339f2-292">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="339f2-293"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="339f2-293"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="339f2-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="339f2-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="339f2-295"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="339f2-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="339f2-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="339f2-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="339f2-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="339f2-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="339f2-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="339f2-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-299">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="339f2-299">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="339f2-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="339f2-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="339f2-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="339f2-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="339f2-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="339f2-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="339f2-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="339f2-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-304">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="339f2-304">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="339f2-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="339f2-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="339f2-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="339f2-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="339f2-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="339f2-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="339f2-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="339f2-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="339f2-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="339f2-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="339f2-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="339f2-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="339f2-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="339f2-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="339f2-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="339f2-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="339f2-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="339f2-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="339f2-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="339f2-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="339f2-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="339f2-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="339f2-316">Palm OS</span><span class="sxs-lookup"><span data-stu-id="339f2-316">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="339f2-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="339f2-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="339f2-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="339f2-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="339f2-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="339f2-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="339f2-320"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span><span class="sxs-lookup"><span data-stu-id="339f2-320"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="339f2-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="339f2-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="339f2-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="339f2-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="339f2-323">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="339f2-323">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="339f2-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-326">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ OperatingSystem**.**OSType**")</span><span class="sxs-lookup"><span data-stu-id="339f2-326">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-327">Describe el tipo de fabricante y sistema operativo cuando la propiedad **OSType** se establece en 1 ("Other").</span><span class="sxs-lookup"><span data-stu-id="339f2-327">Describes the manufacturer and operating system type when the **OSType** property is set to 1 ("Other").</span></span> <span data-ttu-id="339f2-328">El formato de la cadena insertada en **OtherTypeDescription** debe ser similar a las cadenas de **valores** definidas para **OSType**.</span><span class="sxs-lookup"><span data-stu-id="339f2-328">The format of the string inserted in **OtherTypeDescription** should be similar to the **Values** strings defined for **OSType**.</span></span> <span data-ttu-id="339f2-329">Esta propiedad debe establecerse en NULL cuando **OSType** es un valor distinto de 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="339f2-329">This property should be set to null when **OSType** is a value other than 1 (one).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-330">**SizeStoredInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="339f2-330">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-331">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="339f2-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-333">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Configuración de la memoria del sistema DMTF \| 001,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="339f2-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-334">Número de kilobytes que se pueden almacenar en los archivos de paginación del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="339f2-334">Number of kilobytes that can be stored in the operating system's paging files.</span></span> <span data-ttu-id="339f2-335">Este número no representa el tamaño físico real del archivo de paginación en el disco.</span><span class="sxs-lookup"><span data-stu-id="339f2-335">This number does not represent the actual physical size of the paging file on disk.</span></span> <span data-ttu-id="339f2-336">Un valor de 0 (cero) indica que no hay ningún archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="339f2-336">A value of 0 (zero)indicates that there are no paging files.</span></span>

<span data-ttu-id="339f2-337">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="339f2-337">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-338">**Estado**</span><span class="sxs-lookup"><span data-stu-id="339f2-338">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-339">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="339f2-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-341">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="339f2-341">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-342">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="339f2-342">Current status of the object.</span></span>

<span data-ttu-id="339f2-343">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="339f2-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="339f2-344">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="339f2-344">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="339f2-345">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="339f2-345">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="339f2-346">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="339f2-346">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="339f2-347">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="339f2-347">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="339f2-348">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="339f2-348">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="339f2-349">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="339f2-349">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="339f2-350">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="339f2-350">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="339f2-351">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="339f2-351">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="339f2-352">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="339f2-352">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="339f2-353">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="339f2-353">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="339f2-354">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="339f2-354">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="339f2-355">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="339f2-355">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="339f2-356">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="339f2-356">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="339f2-357">**TotalSwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="339f2-357">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-358">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="339f2-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-360">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="339f2-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-361">Espacio de intercambio total, en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="339f2-361">Total swap space, in kilobytes.</span></span> <span data-ttu-id="339f2-362">Este valor puede ser null (no especificado) si el espacio de intercambio no se distingue de los archivos de paginación.</span><span class="sxs-lookup"><span data-stu-id="339f2-362">This value can be null (unspecified) if swap space is not distinguished from page files.</span></span> <span data-ttu-id="339f2-363">Sin embargo, algunos sistemas operativos distinguen estos conceptos.</span><span class="sxs-lookup"><span data-stu-id="339f2-363">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="339f2-364">Por ejemplo, los procesos completos se pueden "intercambiar" en UNIX cuando la lista de páginas disponibles cae y permanece por debajo de una cantidad especificada.</span><span class="sxs-lookup"><span data-stu-id="339f2-364">For example, entire processes can be "swapped out" in UNIX when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="339f2-365">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="339f2-365">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-366">**TotalVirtualMemorySize**</span><span class="sxs-lookup"><span data-stu-id="339f2-366">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-367">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="339f2-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-369">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="339f2-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-370">Número de kilobytes de la memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="339f2-370">Number of kilobytes of virtual memory.</span></span> <span data-ttu-id="339f2-371">Por ejemplo, calcule esto agregando la cantidad de RAM total a la cantidad de espacio de paginación (es decir, agregue la cantidad de memoria en o agregada por el sistema del equipo a la propiedad **SizeStoredInPagingFiles** .</span><span class="sxs-lookup"><span data-stu-id="339f2-371">For example, calculate this by adding the amount of total RAM to the amount of paging space (that is, add the amount of memory in or aggregated by the computer system to the **SizeStoredInPagingFiles** property.</span></span>

<span data-ttu-id="339f2-372">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="339f2-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-373">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="339f2-373">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-374">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="339f2-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-376">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="339f2-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-377">Cantidad total de memoria física, en kilobytes, disponible para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="339f2-377">Total amount of physical memory, in kilobytes, available to the operating system.</span></span> <span data-ttu-id="339f2-378">Este valor no indica necesariamente la cantidad real de memoria física, sino lo que se notifica al sistema operativo como disponible para ella.</span><span class="sxs-lookup"><span data-stu-id="339f2-378">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="339f2-379">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="339f2-379">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="339f2-380">**Versión**</span><span class="sxs-lookup"><span data-stu-id="339f2-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339f2-381">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="339f2-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="339f2-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339f2-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339f2-383">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sistema operativo DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="339f2-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="339f2-384">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="339f2-384">Version of the operation.</span></span>

<span data-ttu-id="339f2-385">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="339f2-385">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="339f2-386"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="339f2-386"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="339f2-387"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="339f2-387"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="339f2-388">Observaciones</span><span class="sxs-lookup"><span data-stu-id="339f2-388">Remarks</span></span>

<span data-ttu-id="339f2-389">La clase **CIM \_ OperatingSystem** se deriva de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="339f2-389">The **CIM\_OperatingSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="339f2-390">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="339f2-390">WMI does not implement this class.</span></span> <span data-ttu-id="339f2-391">Para las clases WMI que se derivan de **CIM \_ OperatingSystem**, consulte [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="339f2-391">For WMI classes that are derived from **CIM\_OperatingSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="339f2-392">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="339f2-392">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="339f2-393">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="339f2-393">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="339f2-394">Requisitos</span><span class="sxs-lookup"><span data-stu-id="339f2-394">Requirements</span></span>



| <span data-ttu-id="339f2-395">Requisito</span><span class="sxs-lookup"><span data-stu-id="339f2-395">Requirement</span></span> | <span data-ttu-id="339f2-396">Value</span><span class="sxs-lookup"><span data-stu-id="339f2-396">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="339f2-397">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="339f2-397">Minimum supported client</span></span><br/> | <span data-ttu-id="339f2-398">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="339f2-398">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="339f2-399">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="339f2-399">Minimum supported server</span></span><br/> | <span data-ttu-id="339f2-400">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="339f2-400">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="339f2-401">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="339f2-401">Namespace</span></span><br/>                | <span data-ttu-id="339f2-402">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="339f2-402">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="339f2-403">MOF</span><span class="sxs-lookup"><span data-stu-id="339f2-403">MOF</span></span><br/>                      | <dl> <span data-ttu-id="339f2-404"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="339f2-404"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="339f2-405">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="339f2-405">DLL</span></span><br/>                      | <dl> <span data-ttu-id="339f2-406"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="339f2-406"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="339f2-407">Vea también</span><span class="sxs-lookup"><span data-stu-id="339f2-407">See also</span></span>

<dl> <dt>

[<span data-ttu-id="339f2-408">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="339f2-408">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

