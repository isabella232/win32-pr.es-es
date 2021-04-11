---
description: La \_ clase CIM MemoryMappedIO representa la arquitectura de equipo de e/s asignada a la memoria. Esta clase trata los recursos de memoria y de e/s de puerto.
ms.assetid: cf418cd0-1ace-4d86-a878-65e81771787e
ms.tgt_platform: multiple
title: CIM_MemoryMappedIO (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryMappedIO
- CIM_MemoryMappedIO.Caption
- CIM_MemoryMappedIO.Description
- CIM_MemoryMappedIO.InstallDate
- CIM_MemoryMappedIO.Name
- CIM_MemoryMappedIO.Status
- CIM_MemoryMappedIO.CreationClassName
- CIM_MemoryMappedIO.CSCreationClassName
- CIM_MemoryMappedIO.CSName
- CIM_MemoryMappedIO.EndingAddress
- CIM_MemoryMappedIO.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28ce4d60a6bba10e857afae7cc93d2e94c69b29f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080238"
---
# <a name="cim_memorymappedio-class"></a><span data-ttu-id="b3c6c-104">\_Clase MemoryMappedIO de CIM</span><span class="sxs-lookup"><span data-stu-id="b3c6c-104">CIM\_MemoryMappedIO class</span></span>

<span data-ttu-id="b3c6c-105">La clase **CIM \_ MemoryMappedIO** representa la arquitectura de equipo de e/s asignada a la memoria.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-105">The **CIM\_MemoryMappedIO** class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="b3c6c-106">Esta clase trata los recursos de memoria y de e/s de puerto.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-106">This class addresses memory and port I/O resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3c6c-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b3c6c-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b3c6c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b3c6c-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b3c6c-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c6c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3c6c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryMappedIO : CIM_SystemResource
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

## <a name="members"></a><span data-ttu-id="b3c6c-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="b3c6c-112">Members</span></span>

<span data-ttu-id="b3c6c-113">La clase **CIM \_ MemoryMappedIO** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b3c6c-113">The **CIM\_MemoryMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="b3c6c-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b3c6c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3c6c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b3c6c-115">Properties</span></span>

<span data-ttu-id="b3c6c-116">La clase **CIM \_ MemoryMappedIO** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-116">The **CIM\_MemoryMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3c6c-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c6c-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c6c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-120">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b3c6c-121">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-121">A short textual description of the object.</span></span>

<span data-ttu-id="b3c6c-122">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3c6c-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3c6c-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c6c-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c6c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-126">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b3c6c-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b3c6c-127">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b3c6c-128">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="b3c6c-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c6c-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c6c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-132">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b3c6c-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b3c6c-133">Propiedad **CreationClassName** del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-133">Scoping computer system's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="b3c6c-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c6c-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c6c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-137">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b3c6c-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b3c6c-138">Propiedad **nombre** del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-138">Scoping computer system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="b3c6c-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c6c-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c6c-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-142">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b3c6c-143">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-143">A textual description of the object.</span></span>

<span data-ttu-id="b3c6c-144">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3c6c-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3c6c-145">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-145">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c6c-146">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-146">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c6c-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s asignada de memoria DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="b3c6c-149">Dirección final de e/s asignada a la memoria.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-149">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="b3c6c-150">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b3c6c-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b3c6c-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c6c-152">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c6c-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-154">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b3c6c-155">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-155">Indicates when the object was installed.</span></span> <span data-ttu-id="b3c6c-156">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b3c6c-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3c6c-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3c6c-158">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c6c-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c6c-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-161">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b3c6c-162">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-162">Label by which the object is known.</span></span> <span data-ttu-id="b3c6c-163">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b3c6c-164">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3c6c-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3c6c-165">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c6c-166">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c6c-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-168">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s asignada de memoria DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-168">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="b3c6c-169">Dirección inicial de e/s asignada a la memoria.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="b3c6c-170">La propiedad de identificador de recursos de hardware debe establecerse en este valor para construir la clave de recurso de e/s asignada.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="b3c6c-171">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b3c6c-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b3c6c-172">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-172">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c6c-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c6c-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c6c-175">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b3c6c-176">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-176">String that indicates the current status of the object.</span></span> <span data-ttu-id="b3c6c-177">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-177">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b3c6c-178">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="b3c6c-178">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b3c6c-179">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="b3c6c-179">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b3c6c-180">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="b3c6c-180">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b3c6c-181">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-181">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b3c6c-182">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-182">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b3c6c-183">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3c6c-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b3c6c-184">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b3c6c-184">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b3c6c-185">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-185">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b3c6c-186">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-186">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b3c6c-187">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-187">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b3c6c-188">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-188">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b3c6c-189">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-189">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b3c6c-190">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-190">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b3c6c-191">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-191">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b3c6c-192">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-192">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b3c6c-193">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-193">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b3c6c-194">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-194">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b3c6c-195">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-195">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b3c6c-196">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="b3c6c-196">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b3c6c-197"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b3c6c-197"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b3c6c-198">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3c6c-198">Remarks</span></span>

<span data-ttu-id="b3c6c-199">La clase **CIM \_ MemoryMappedIO** se deriva de [**\_ SystemResource de CIM**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="b3c6c-199">The **CIM\_MemoryMappedIO** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="b3c6c-200">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-200">WMI does not implement this class.</span></span> <span data-ttu-id="b3c6c-201">Para las clases derivadas de **CIM \_ MemoryMappedIO**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b3c6c-201">For classes derived from **CIM\_MemoryMappedIO**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b3c6c-202">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b3c6c-203">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c6c-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3c6c-204">Requirements</span></span>



| <span data-ttu-id="b3c6c-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c6c-205">Requirement</span></span> | <span data-ttu-id="b3c6c-206">Value</span><span class="sxs-lookup"><span data-stu-id="b3c6c-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c6c-207">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3c6c-207">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c6c-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3c6c-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3c6c-209">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3c6c-209">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c6c-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3c6c-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3c6c-211">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b3c6c-211">Namespace</span></span><br/>                | <span data-ttu-id="b3c6c-212">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b3c6c-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b3c6c-213">MOF</span><span class="sxs-lookup"><span data-stu-id="b3c6c-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3c6c-214"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3c6c-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3c6c-215">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3c6c-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3c6c-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3c6c-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c6c-217">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3c6c-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c6c-218">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-218">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

