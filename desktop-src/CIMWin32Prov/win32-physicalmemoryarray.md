---
description: Win32 \_ PhysicalMemoryArray&\# 160; La clase WMI representa los detalles sobre la memoria física del sistema del equipo. Esto incluye el número de dispositivos de memoria, la capacidad de memoria disponible y el tipo de memoria&\# 8212; por ejemplo, memoria de sistema o de vídeo.
ms.assetid: 6b553230-e1fc-46e6-b13a-02fbbd34034d
ms.tgt_platform: multiple
title: Win32_PhysicalMemoryArray (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryArray
- Win32_PhysicalMemoryArray.IsCompatible
- Win32_PhysicalMemoryArray.Caption
- Win32_PhysicalMemoryArray.CreationClassName
- Win32_PhysicalMemoryArray.Depth
- Win32_PhysicalMemoryArray.Description
- Win32_PhysicalMemoryArray.Height
- Win32_PhysicalMemoryArray.HotSwappable
- Win32_PhysicalMemoryArray.InstallDate
- Win32_PhysicalMemoryArray.Location
- Win32_PhysicalMemoryArray.Manufacturer
- Win32_PhysicalMemoryArray.MaxCapacity
- Win32_PhysicalMemoryArray.MaxCapacityEx
- Win32_PhysicalMemoryArray.MemoryDevices
- Win32_PhysicalMemoryArray.MemoryErrorCorrection
- Win32_PhysicalMemoryArray.Model
- Win32_PhysicalMemoryArray.Name
- Win32_PhysicalMemoryArray.OtherIdentifyingInfo
- Win32_PhysicalMemoryArray.PartNumber
- Win32_PhysicalMemoryArray.PoweredOn
- Win32_PhysicalMemoryArray.Removable
- Win32_PhysicalMemoryArray.Replaceable
- Win32_PhysicalMemoryArray.SerialNumber
- Win32_PhysicalMemoryArray.SKU
- Win32_PhysicalMemoryArray.Status
- Win32_PhysicalMemoryArray.Tag
- Win32_PhysicalMemoryArray.Use
- Win32_PhysicalMemoryArray.Version
- Win32_PhysicalMemoryArray.Weight
- Win32_PhysicalMemoryArray.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8a585b0399f7015113b02ff48dbeb85956c9e62b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000822"
---
# <a name="win32_physicalmemoryarray-class"></a><span data-ttu-id="b1420-104">\_Clase Win32 PhysicalMemoryArray</span><span class="sxs-lookup"><span data-stu-id="b1420-104">Win32\_PhysicalMemoryArray class</span></span>

<span data-ttu-id="b1420-105">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PhysicalMemoryArray de Win32** representa los detalles sobre la memoria física del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="b1420-105">The **Win32\_PhysicalMemoryArray** [WMI class](../wmisdk/retrieving-a-class.md) represents details about the computer system physical memory.</span></span> <span data-ttu-id="b1420-106">Esto incluye el número de dispositivos de memoria, la capacidad de memoria disponible y el tipo de memoria, por ejemplo, memoria de sistema o de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b1420-106">This includes the number of memory devices, memory capacity available, and memory type—for example, system or video memory.</span></span>

<span data-ttu-id="b1420-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b1420-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b1420-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b1420-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1420-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1420-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B99-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemoryArray : CIM_PhysicalPackage
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   Location;
  string   Manufacturer;
  uint32   MaxCapacity;
  uint64   MaxCapacityEx;
  uint16   MemoryDevices;
  uint16   MemoryErrorCorrection;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  uint16   Use;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="b1420-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b1420-110">Members</span></span>

<span data-ttu-id="b1420-111">La **clase \_ PhysicalMemoryArray de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b1420-111">The **Win32\_PhysicalMemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="b1420-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1420-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b1420-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1420-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b1420-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1420-114">Methods</span></span>

<span data-ttu-id="b1420-115">La clase **Win32 \_ PhysicalMemoryArray** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b1420-115">The **Win32\_PhysicalMemoryArray** class has these methods.</span></span>



| <span data-ttu-id="b1420-116">Método</span><span class="sxs-lookup"><span data-stu-id="b1420-116">Method</span></span>           | <span data-ttu-id="b1420-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1420-117">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="b1420-118">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="b1420-118">**IsCompatible**</span></span> | <span data-ttu-id="b1420-119">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="b1420-119">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b1420-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1420-120">Properties</span></span>

<span data-ttu-id="b1420-121">La **clase \_ PhysicalMemoryArray de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b1420-121">The **Win32\_PhysicalMemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1420-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b1420-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-125">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b1420-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-126">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="b1420-126">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="b1420-127">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-128">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b1420-128">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-131">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="b1420-131">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b1420-132">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="b1420-132">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b1420-133">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="b1420-133">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="b1420-134">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-134">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-135">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="b1420-135">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-136">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="b1420-136">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-138">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="b1420-138">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-139">Profundidad del paquete físico: en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="b1420-139">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="b1420-140">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-140">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1420-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-144">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="b1420-144">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-145">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b1420-145">Description of the object.</span></span>

<span data-ttu-id="b1420-146">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-147">**Height**</span><span class="sxs-lookup"><span data-stu-id="b1420-147">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-148">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="b1420-148">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-150">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="b1420-150">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-151">Alto del paquete físico: en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="b1420-151">Height of the physical package—in inches.</span></span>

<span data-ttu-id="b1420-152">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-152">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-153">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="b1420-153">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-154">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b1420-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-156">Si es true, un paquete físico puede intercambiarse en caliente (si es posible reemplazar el elemento con un **valor** físicamente diferente pero equivalente mientras el paquete contenedor tiene energía aplicada a él, está "activado").</span><span class="sxs-lookup"><span data-stu-id="b1420-156">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it, is "on").</span></span> <span data-ttu-id="b1420-157">Por ejemplo, un paquete de unidad de disco insertado mediante conectores SCA es extraíble y puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="b1420-157">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="b1420-158">Todos los paquetes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="b1420-158">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="b1420-159">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-159">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-160">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b1420-160">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-161">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1420-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-163">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="b1420-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-164">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b1420-164">Date and time the object was installed.</span></span> <span data-ttu-id="b1420-165">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b1420-165">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b1420-166">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-167">**Ubicación**</span><span class="sxs-lookup"><span data-stu-id="b1420-167">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-168">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1420-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-170">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 16 \| Location")</span><span class="sxs-lookup"><span data-stu-id="b1420-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-171">Ubicación física de la matriz de memoria.</span><span class="sxs-lookup"><span data-stu-id="b1420-171">Physical location of the memory array.</span></span>

<span data-ttu-id="b1420-172">Este valor procede del miembro **Location** de la estructura de la **matriz de memoria física** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="b1420-172">This value comes from the **Location** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b1420-173">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="b1420-173">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1420-174">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b1420-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1420-175">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b1420-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_board_or_motherboard"></span><span id="system_board_or_motherboard"></span><span id="SYSTEM_BOARD_OR_MOTHERBOARD"></span>

<span data-ttu-id="b1420-176">**Placa de sistema o placa base** (3)</span><span class="sxs-lookup"><span data-stu-id="b1420-176">**System board or motherboard** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_add-on_card"></span><span id="isa_add-on_card"></span><span id="ISA_ADD-ON_CARD"></span>

<span data-ttu-id="b1420-177">**Tarjeta de complemento ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="b1420-177">**ISA add-on card** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_add-on_card"></span><span id="eisa_add-on_card"></span><span id="EISA_ADD-ON_CARD"></span>

<span data-ttu-id="b1420-178">**Tarjeta complementaria EISA** (5)</span><span class="sxs-lookup"><span data-stu-id="b1420-178">**EISA add-on card** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_add-on_card"></span><span id="pci_add-on_card"></span><span id="PCI_ADD-ON_CARD"></span>

<span data-ttu-id="b1420-179">**Tarjeta de complemento PCI** (6)</span><span class="sxs-lookup"><span data-stu-id="b1420-179">**PCI add-on card** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_add-on_card"></span><span id="mca_add-on_card"></span><span id="MCA_ADD-ON_CARD"></span>

<span data-ttu-id="b1420-180">**Tarjeta complementaria MCA** (7)</span><span class="sxs-lookup"><span data-stu-id="b1420-180">**MCA add-on card** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_add-on_card"></span><span id="pcmcia_add-on_card"></span><span id="PCMCIA_ADD-ON_CARD"></span>

<span data-ttu-id="b1420-181">**Tarjeta complementaria PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="b1420-181">**PCMCIA add-on card** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_add-on_card"></span><span id="proprietary_add-on_card"></span><span id="PROPRIETARY_ADD-ON_CARD"></span>

<span data-ttu-id="b1420-182">**Tarjeta complementaria de propiedad** (9)</span><span class="sxs-lookup"><span data-stu-id="b1420-182">**Proprietary add-on card** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="b1420-183">**Nubus** (10)</span><span class="sxs-lookup"><span data-stu-id="b1420-183">**NuBus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C20_add-on_card"></span><span id="pc-98_c20_add-on_card"></span><span id="PC-98_C20_ADD-ON_CARD"></span>

<span data-ttu-id="b1420-184">**Tarjeta de complemento de PC-98/C20** (11)</span><span class="sxs-lookup"><span data-stu-id="b1420-184">**PC-98/C20 add-on card** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C24_add-on_card"></span><span id="pc-98_c24_add-on_card"></span><span id="PC-98_C24_ADD-ON_CARD"></span>

<span data-ttu-id="b1420-185">**Tarjeta de complemento de PC-98/C24** (12)</span><span class="sxs-lookup"><span data-stu-id="b1420-185">**PC-98/C24 add-on card** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_E_add-on_card"></span><span id="pc-98_e_add-on_card"></span><span id="PC-98_E_ADD-ON_CARD"></span>

<span data-ttu-id="b1420-186">**Tarjeta de complemento de PC-98/E** (13)</span><span class="sxs-lookup"><span data-stu-id="b1420-186">**PC-98/E add-on card** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_Local_bus_add-on_card"></span><span id="pc-98_local_bus_add-on_card"></span><span id="PC-98_LOCAL_BUS_ADD-ON_CARD"></span>

<span data-ttu-id="b1420-187">**Tarjeta complementaria de bus PC-98/local** (14)</span><span class="sxs-lookup"><span data-stu-id="b1420-187">**PC-98/Local bus add-on card** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1420-188">**Le**</span><span class="sxs-lookup"><span data-stu-id="b1420-188">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-191">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="b1420-191">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b1420-192">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b1420-192">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="b1420-193">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-193">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-194">**MaxCapacity**</span><span class="sxs-lookup"><span data-stu-id="b1420-194">**MaxCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-195">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1420-195">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-197">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo de SMBIOS 16 de \| capacidad máxima")</span><span class="sxs-lookup"><span data-stu-id="b1420-197">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Maximum Capacity")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-198">En su lugar, use la propiedad **MaxCapacityEx** .</span><span class="sxs-lookup"><span data-stu-id="b1420-198">Use the **MaxCapacityEx** property instead.</span></span>

<span data-ttu-id="b1420-199">Este valor procede del miembro **capacidad máxima** de la estructura de la **matriz de memoria física** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="b1420-199">This value comes from the **Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="b1420-200">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Tamaño máximo de memoria (en bytes) que se instala para esta matriz de memoria concreta.</span><span class="sxs-lookup"><span data-stu-id="b1420-200">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** Maximum memory size (in bytes) installable for this particular memory array.</span></span> <span data-ttu-id="b1420-201">Si no se conoce el tamaño, se asigna a la propiedad un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="b1420-201">If the size is unknown, the property is given a value of 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-202">**MaxCapacityEx**</span><span class="sxs-lookup"><span data-stu-id="b1420-202">**MaxCapacityEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-203">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b1420-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-205">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 16 \| de capacidad máxima extendida"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="b1420-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Extended Maximum Capacity"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-206">Tamaño máximo de memoria (en kilobytes) que se instala para esta matriz de memoria concreta.</span><span class="sxs-lookup"><span data-stu-id="b1420-206">Maximum memory size (in kilobytes) installable for this particular memory array.</span></span> <span data-ttu-id="b1420-207">Si no se conoce el tamaño, se asigna a la propiedad un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="b1420-207">If the size is unknown, the property is given a value of 0 (zero).</span></span>

<span data-ttu-id="b1420-208">Este valor procede del miembro de **capacidad máxima extendida** de la estructura de la **matriz de memoria física** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="b1420-208">This value comes from the **Extended Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="b1420-209">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="b1420-209">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b1420-210">**MemoryDevices**</span><span class="sxs-lookup"><span data-stu-id="b1420-210">**MemoryDevices**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-211">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1420-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-213">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo de SMBIOS 16 \| número de dispositivos de memoria")</span><span class="sxs-lookup"><span data-stu-id="b1420-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Number of Memory Devices")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-214">Número de ranuras físicas o sockets disponibles en esta matriz de memoria.</span><span class="sxs-lookup"><span data-stu-id="b1420-214">Number of physical slots or sockets available in this memory array.</span></span>

<span data-ttu-id="b1420-215">Este valor procede del miembro **número de dispositivos de memoria** de la estructura de la **matriz de memoria física** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="b1420-215">This value comes from the **Number of Memory Devices** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="b1420-216">**MemoryErrorCorrection**</span><span class="sxs-lookup"><span data-stu-id="b1420-216">**MemoryErrorCorrection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-217">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1420-217">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-219">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("corrección de errores de memoria de tipo de SMBIOS \| 16 \| ")</span><span class="sxs-lookup"><span data-stu-id="b1420-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-220">Tipo de corrección de errores utilizada por la matriz de memoria.</span><span class="sxs-lookup"><span data-stu-id="b1420-220">Type of error correction used by the memory array.</span></span>

<span data-ttu-id="b1420-221">Este valor procede del miembro de **corrección de errores de memoria** de la estructura de la matriz de **memoria física** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="b1420-221">This value comes from the **Memory Error Correction** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b1420-222">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="b1420-222">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1420-223">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b1420-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1420-224">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b1420-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b1420-225">**Ninguno** (3)</span><span class="sxs-lookup"><span data-stu-id="b1420-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="b1420-226">**Paridad** (4)</span><span class="sxs-lookup"><span data-stu-id="b1420-226">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="b1420-227">**ECC de un bit** (5)</span><span class="sxs-lookup"><span data-stu-id="b1420-227">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="b1420-228">**ECC de varios bits** (6)</span><span class="sxs-lookup"><span data-stu-id="b1420-228">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="b1420-229">**CRC** (7)</span><span class="sxs-lookup"><span data-stu-id="b1420-229">**CRC** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1420-230">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="b1420-230">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-233">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="b1420-233">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b1420-234">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b1420-234">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="b1420-235">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-236">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b1420-236">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-239">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b1420-239">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-240">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="b1420-240">Label by which the object is known.</span></span> <span data-ttu-id="b1420-241">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="b1420-241">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b1420-242">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-243">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b1420-243">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-244">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-246">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b1420-246">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="b1420-247">Un ejemplo son los datos de código de barras asociados a un elemento que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="b1420-247">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="b1420-248">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único o se puede usar como una clave de elemento, esta propiedad sería **null** y los datos de código de barras usados como clave de clase en la propiedad de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="b1420-248">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="b1420-249">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-249">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-250">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="b1420-250">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-253">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="b1420-253">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b1420-254">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b1420-254">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="b1420-255">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-255">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-256">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="b1420-256">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-257">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b1420-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-259">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="b1420-259">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="b1420-260">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-260">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-261">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="b1420-261">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-262">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b1420-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-264">Si es **true**, un paquete físico es extraíble (si está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado general).</span><span class="sxs-lookup"><span data-stu-id="b1420-264">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="b1420-265">Un paquete todavía puede ser extraíble si la alimentación debe estar "desactivada" para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="b1420-265">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="b1420-266">Si la potencia puede ser "ON" y se ha quitado el paquete, el elemento es extraíble y puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="b1420-266">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="b1420-267">Por ejemplo, una batería adicional en un equipo portátil es extraíble, como un paquete de unidad de disco insertado mediante conectores SCA.</span><span class="sxs-lookup"><span data-stu-id="b1420-267">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="b1420-268">Sin embargo, el último puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="b1420-268">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="b1420-269">La pantalla de un portátil no es extraíble, ni tampoco es una fuente de alimentación que no sea redundante.</span><span class="sxs-lookup"><span data-stu-id="b1420-269">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="b1420-270">La eliminación de estos componentes afectaría a la función del empaquetado general o no es posible debido a la estrecha integración del paquete.</span><span class="sxs-lookup"><span data-stu-id="b1420-270">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="b1420-271">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-271">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-272">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="b1420-272">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-273">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b1420-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-275">Si **es true**, este componente de medio físico se puede reemplazar por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="b1420-275">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="b1420-276">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="b1420-276">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="b1420-277">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="b1420-277">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="b1420-278">Otro ejemplo es un paquete de fuente de alimentación montado en raíles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="b1420-278">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="b1420-279">Todos los paquetes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="b1420-279">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="b1420-280">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-280">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-281">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b1420-281">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-282">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-284">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="b1420-284">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b1420-285">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b1420-285">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="b1420-286">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-287">**SKU**</span><span class="sxs-lookup"><span data-stu-id="b1420-287">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-290">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="b1420-290">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b1420-291">Número de unidad de almacenamiento para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b1420-291">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="b1420-292">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-293">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b1420-293">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-294">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-296">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="b1420-296">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-297">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b1420-297">Current status of the object.</span></span> <span data-ttu-id="b1420-298">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="b1420-298">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b1420-299">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="b1420-299">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b1420-300">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="b1420-300">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b1420-301">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="b1420-301">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b1420-302">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b1420-302">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b1420-303">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b1420-304">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b1420-304">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b1420-305">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="b1420-305">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b1420-306">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="b1420-306">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b1420-307">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b1420-307">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1420-308">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b1420-308">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b1420-309">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b1420-309">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b1420-310">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="b1420-310">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b1420-311">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="b1420-311">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b1420-312">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="b1420-312">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b1420-313">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="b1420-313">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b1420-314">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b1420-314">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b1420-315">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="b1420-315">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b1420-316">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="b1420-316">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1420-317">**Tag**</span><span class="sxs-lookup"><span data-stu-id="b1420-317">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-318">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-320">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**invalidación**](../wmisdk/standard-qualifiers.md) ("etiqueta"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b1420-320">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-321">Identificador único de la matriz de memoria física.</span><span class="sxs-lookup"><span data-stu-id="b1420-321">Unique identifier of the physical memory array.</span></span>

<span data-ttu-id="b1420-322">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-322">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="b1420-323">Ejemplo: "matriz de memoria física 1"</span><span class="sxs-lookup"><span data-stu-id="b1420-323">Example: "Physical Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="b1420-324">**Uso**</span><span class="sxs-lookup"><span data-stu-id="b1420-324">**Use**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-325">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1420-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-327">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| uso del tipo de SMBIOS 16 \| ")</span><span class="sxs-lookup"><span data-stu-id="b1420-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Use")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-328">Cómo se utiliza la memoria en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="b1420-328">How memory is used in the computer system.</span></span>

<span data-ttu-id="b1420-329">Este valor procede del miembro **use** de la estructura de la **matriz de memoria física** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="b1420-329">This value comes from the **Use** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b1420-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="b1420-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1420-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b1420-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1420-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b1420-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>

<span data-ttu-id="b1420-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**Memoria del sistema** (3)</span><span class="sxs-lookup"><span data-stu-id="b1420-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**System memory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>

<span data-ttu-id="b1420-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Memoria de vídeo** (4)</span><span class="sxs-lookup"><span data-stu-id="b1420-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Video memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>

<span data-ttu-id="b1420-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Memoria Flash** (5)</span><span class="sxs-lookup"><span data-stu-id="b1420-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Flash memory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>

<span data-ttu-id="b1420-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**RAM no volátil** (6)</span><span class="sxs-lookup"><span data-stu-id="b1420-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**Non-volatile RAM** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b1420-337">RAM no volátil</span><span class="sxs-lookup"><span data-stu-id="b1420-337">Nonvolatile RAM</span></span>

</dd> <dt>

<span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>

<span data-ttu-id="b1420-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Memoria caché** (7)</span><span class="sxs-lookup"><span data-stu-id="b1420-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Cache memory** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1420-339">**Versión**</span><span class="sxs-lookup"><span data-stu-id="b1420-339">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-342">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="b1420-342">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b1420-343">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b1420-343">Version of the physical element.</span></span>

<span data-ttu-id="b1420-344">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-344">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-345">**Peso**</span><span class="sxs-lookup"><span data-stu-id="b1420-345">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-346">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="b1420-346">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-348">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("libras")</span><span class="sxs-lookup"><span data-stu-id="b1420-348">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-349">Peso del paquete físico en libras.</span><span class="sxs-lookup"><span data-stu-id="b1420-349">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="b1420-350">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-350">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-351">**Width**</span><span class="sxs-lookup"><span data-stu-id="b1420-351">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-352">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="b1420-352">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-354">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="b1420-354">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-355">Ancho del paquete físico en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="b1420-355">Width of the physical package in inches.</span></span>

<span data-ttu-id="b1420-356">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-356">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1420-357">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1420-357">Remarks</span></span>

<span data-ttu-id="b1420-358">La **clase \_ PhysicalMemoryArray de Win32** se deriva de [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b1420-358">The **Win32\_PhysicalMemoryArray** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b1420-359">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b1420-359">Examples</span></span>

<span data-ttu-id="b1420-360">En el siguiente ejemplo de PowerShell se recupera el número de ranuras de memoria y la cantidad de memoria instalada en un equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="b1420-360">The following PowerShell sample retrieves the number of memory slots and the amount of memory installed on a target computer.</span></span>


```PowerShell
$strComputer = Read-Host "Enter Computer Name"
 $colSlots = Get-WmiObject -Class "win32_PhysicalMemoryArray" -namespace "root\CIMV2" `
 -computerName $strComputer
 $colRAM = Get-WmiObject -Class "win32_PhysicalMemory" -namespace "root\CIMV2" `
 -computerName $strComputer

Foreach ($objSlot In $colSlots){
      "Total Number of DIMM Slots: " + $objSlot.MemoryDevices
 }
 Foreach ($objRAM In $colRAM) {
      "Memory Installed: " + $objRAM.DeviceLocator
      "Memory Size: " + ($objRAM.Capacity / 1GB) + " GB"
 }
```



<span data-ttu-id="b1420-361">El siguiente ejemplo de código de VBScript devuelve información acerca de la memoria física instalada en un equipo.</span><span class="sxs-lookup"><span data-stu-id="b1420-361">The following VBScript code sample returns information about the physical memory installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_PhysicalMemoryArray") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Maximum Capacity: " & objItem.MaxCapacity 
    Wscript.Echo "Memory Devices: " & objItem.MemoryDevices 
    Wscript.Echo "Memory Error Correction: " & objItem.MemoryErrorCorrection 
Next 
```



## <a name="requirements"></a><span data-ttu-id="b1420-362">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1420-362">Requirements</span></span>



| <span data-ttu-id="b1420-363">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1420-363">Requirement</span></span> | <span data-ttu-id="b1420-364">Value</span><span class="sxs-lookup"><span data-stu-id="b1420-364">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1420-365">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1420-365">Minimum supported client</span></span><br/> | <span data-ttu-id="b1420-366">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1420-366">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1420-367">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1420-367">Minimum supported server</span></span><br/> | <span data-ttu-id="b1420-368">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1420-368">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1420-369">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b1420-369">Namespace</span></span><br/>                | <span data-ttu-id="b1420-370">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b1420-370">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b1420-371">MOF</span><span class="sxs-lookup"><span data-stu-id="b1420-371">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1420-372"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1420-372"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1420-373">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1420-373">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1420-374"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1420-374"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1420-375">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1420-375">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1420-376">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="b1420-376">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="b1420-377">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="b1420-377">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b1420-378">**Win32 \_ MemoryArrayLocation**</span><span class="sxs-lookup"><span data-stu-id="b1420-378">**Win32\_MemoryArrayLocation**</span></span>](win32-memoryarraylocation.md)
</dt> </dl>

 

 
