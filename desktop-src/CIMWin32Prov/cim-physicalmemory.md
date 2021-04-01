---
description: La \_ clase CIM PhysicalMemory representa dispositivos de memoria de bajo nivel, como SIMM, DIMM, chips de memoria sin procesar, etc.
ms.assetid: a25c5f00-cd85-42e6-9b26-8e9380b3c73b
ms.tgt_platform: multiple
title: CIM_PhysicalMemory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMemory
- CIM_PhysicalMemory.BankLabel
- CIM_PhysicalMemory.Capacity
- CIM_PhysicalMemory.Caption
- CIM_PhysicalMemory.CreationClassName
- CIM_PhysicalMemory.DataWidth
- CIM_PhysicalMemory.Description
- CIM_PhysicalMemory.FormFactor
- CIM_PhysicalMemory.HotSwappable
- CIM_PhysicalMemory.InstallDate
- CIM_PhysicalMemory.InterleavePosition
- CIM_PhysicalMemory.Manufacturer
- CIM_PhysicalMemory.MemoryType
- CIM_PhysicalMemory.Model
- CIM_PhysicalMemory.Name
- CIM_PhysicalMemory.OtherIdentifyingInfo
- CIM_PhysicalMemory.PartNumber
- CIM_PhysicalMemory.PositionInRow
- CIM_PhysicalMemory.PoweredOn
- CIM_PhysicalMemory.Removable
- CIM_PhysicalMemory.Replaceable
- CIM_PhysicalMemory.SerialNumber
- CIM_PhysicalMemory.SKU
- CIM_PhysicalMemory.Speed
- CIM_PhysicalMemory.Status
- CIM_PhysicalMemory.Tag
- CIM_PhysicalMemory.TotalWidth
- CIM_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bd46ebde99ae6c6d9e28975d67563424619db84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907433"
---
# <a name="cim_physicalmemory-class"></a><span data-ttu-id="f1cd3-103">\_Clase PhysicalMemory de CIM</span><span class="sxs-lookup"><span data-stu-id="f1cd3-103">CIM\_PhysicalMemory class</span></span>

<span data-ttu-id="f1cd3-104">La clase **CIM \_ PhysicalMemory** representa dispositivos de memoria de bajo nivel, como SIMM, DIMM, chips de memoria sin procesar, etc.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-104">The **CIM\_PhysicalMemory** class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1cd3-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f1cd3-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f1cd3-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f1cd3-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1cd3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1cd3-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMemory : CIM_Chip
{
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint16   MemoryType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="f1cd3-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f1cd3-110">Members</span></span>

<span data-ttu-id="f1cd3-111">La clase **CIM \_ PhysicalMemory** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f1cd3-111">The **CIM\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="f1cd3-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f1cd3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1cd3-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f1cd3-113">Properties</span></span>

<span data-ttu-id="f1cd3-114">La clase **CIM \_ PhysicalMemory** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-114">The **CIM\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1cd3-115">**BankLabel**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-115">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-119">La etiqueta Bank en la que se encuentra la memoria.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-119">Labeled bank in which the memory is located.</span></span> <span data-ttu-id="f1cd3-120">Por ejemplo, "Bank 0" o "Bank A".</span><span class="sxs-lookup"><span data-stu-id="f1cd3-120">For example, "Bank 0" or "Bank A".</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-121">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-121">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-122">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-124">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-125">Capacidad total de la memoria física, en bytes.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-125">Total capacity of the physical memory, in bytes.</span></span>

<span data-ttu-id="f1cd3-126">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-127">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-130">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-131">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-131">Short textual description of the object.</span></span>

<span data-ttu-id="f1cd3-132">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-136">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-137">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f1cd3-138">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f1cd3-139">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-139">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-140">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-140">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-141">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-143">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-144">Ancho de datos de la memoria física, en bits.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-144">Data width of the physical memory, in bits.</span></span> <span data-ttu-id="f1cd3-145">Un ancho de datos de 0 (cero) y un ancho total de 8, indica que la memoria se usa únicamente para proporcionar bits de corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-145">A data width of 0 (zero) , and a total width of 8, indicates that the memory is solely used to provide error correction bits.</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-149">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-149">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-150">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-150">Textual description of the object.</span></span>

<span data-ttu-id="f1cd3-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-152">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-152">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-153">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-155">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-156">Factor de forma de implementación para el chip.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-156">Implementation form factor for the chip.</span></span> <span data-ttu-id="f1cd3-157">Por ejemplo, se pueden especificar valores como SIMM, TSOP o PGA.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-157">For example, values such as SIMM, TSOP, or PGA can be specified.</span></span>

<span data-ttu-id="f1cd3-158">Esta propiedad se hereda del [**\_ chip CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-158">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>

<span data-ttu-id="f1cd3-159">0</span><span class="sxs-lookup"><span data-stu-id="f1cd3-159">0</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-160">Unknown</span><span class="sxs-lookup"><span data-stu-id="f1cd3-160">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-161">1</span><span class="sxs-lookup"><span data-stu-id="f1cd3-161">1</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-162">Otros</span><span class="sxs-lookup"><span data-stu-id="f1cd3-162">Other</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-163">2</span><span class="sxs-lookup"><span data-stu-id="f1cd3-163">2</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-164">SIP</span><span class="sxs-lookup"><span data-stu-id="f1cd3-164">SIP</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-165">3</span><span class="sxs-lookup"><span data-stu-id="f1cd3-165">3</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-166">DIP</span><span class="sxs-lookup"><span data-stu-id="f1cd3-166">DIP</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-167">4</span><span class="sxs-lookup"><span data-stu-id="f1cd3-167">4</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-168">ZIP</span><span class="sxs-lookup"><span data-stu-id="f1cd3-168">ZIP</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-169">5</span><span class="sxs-lookup"><span data-stu-id="f1cd3-169">5</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-170">SOJ</span><span class="sxs-lookup"><span data-stu-id="f1cd3-170">SOJ</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-171">6</span><span class="sxs-lookup"><span data-stu-id="f1cd3-171">6</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-172">Propietario</span><span class="sxs-lookup"><span data-stu-id="f1cd3-172">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-173">7</span><span class="sxs-lookup"><span data-stu-id="f1cd3-173">7</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-174">SIMM</span><span class="sxs-lookup"><span data-stu-id="f1cd3-174">SIMM</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-175">8</span><span class="sxs-lookup"><span data-stu-id="f1cd3-175">8</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-176">APARECERÁ</span><span class="sxs-lookup"><span data-stu-id="f1cd3-176">DIMM</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-177">9</span><span class="sxs-lookup"><span data-stu-id="f1cd3-177">9</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-178">TSOP</span><span class="sxs-lookup"><span data-stu-id="f1cd3-178">TSOP</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-179">10</span><span class="sxs-lookup"><span data-stu-id="f1cd3-179">10</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-180">PGA</span><span class="sxs-lookup"><span data-stu-id="f1cd3-180">PGA</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-181">11</span><span class="sxs-lookup"><span data-stu-id="f1cd3-181">11</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-182">SEMÁFORO</span><span class="sxs-lookup"><span data-stu-id="f1cd3-182">RIMM</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-183">12</span><span class="sxs-lookup"><span data-stu-id="f1cd3-183">12</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-184">SODIMM</span><span class="sxs-lookup"><span data-stu-id="f1cd3-184">SODIMM</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-185">13</span><span class="sxs-lookup"><span data-stu-id="f1cd3-185">13</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-186">SRIMM</span><span class="sxs-lookup"><span data-stu-id="f1cd3-186">SRIMM</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-187">14</span><span class="sxs-lookup"><span data-stu-id="f1cd3-187">14</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-188">SMD</span><span class="sxs-lookup"><span data-stu-id="f1cd3-188">SMD</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-189">15</span><span class="sxs-lookup"><span data-stu-id="f1cd3-189">15</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-190">SSMP</span><span class="sxs-lookup"><span data-stu-id="f1cd3-190">SSMP</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-191">16</span><span class="sxs-lookup"><span data-stu-id="f1cd3-191">16</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-192">QFP</span><span class="sxs-lookup"><span data-stu-id="f1cd3-192">QFP</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-193">17</span><span class="sxs-lookup"><span data-stu-id="f1cd3-193">17</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-194">TQFP</span><span class="sxs-lookup"><span data-stu-id="f1cd3-194">TQFP</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-195">18</span><span class="sxs-lookup"><span data-stu-id="f1cd3-195">18</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-196">SOIC</span><span class="sxs-lookup"><span data-stu-id="f1cd3-196">SOIC</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-197">19</span><span class="sxs-lookup"><span data-stu-id="f1cd3-197">19</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-198">LCC</span><span class="sxs-lookup"><span data-stu-id="f1cd3-198">LCC</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-199">20</span><span class="sxs-lookup"><span data-stu-id="f1cd3-199">20</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-200">PLCC</span><span class="sxs-lookup"><span data-stu-id="f1cd3-200">PLCC</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-201">21</span><span class="sxs-lookup"><span data-stu-id="f1cd3-201">21</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-202">BGA</span><span class="sxs-lookup"><span data-stu-id="f1cd3-202">BGA</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-203">22</span><span class="sxs-lookup"><span data-stu-id="f1cd3-203">22</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-204">FPBGA</span><span class="sxs-lookup"><span data-stu-id="f1cd3-204">FPBGA</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-205">23</span><span class="sxs-lookup"><span data-stu-id="f1cd3-205">23</span></span>
</dt> <dd>

<span data-ttu-id="f1cd3-206">LGA</span><span class="sxs-lookup"><span data-stu-id="f1cd3-206">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1cd3-207">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-207">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-208">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-210">Si **es true**, el paquete puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-210">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="f1cd3-211">Un paquete físico puede intercambiarse en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras se activa el paquete contenedor.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-211">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="f1cd3-212">Por ejemplo, un componente de ventilador se puede diseñar para que se intercambie en caliente.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-212">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="f1cd3-213">Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-213">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="f1cd3-214">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-214">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-216">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-218">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-219">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-219">Date and time the object was installed.</span></span> <span data-ttu-id="f1cd3-220">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-220">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f1cd3-221">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-222">**InterleavePosition**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-222">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-223">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-225">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Direcciones asignadas del dispositivo de memoria DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-226">Posición de la memoria física en una intercalación.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-226">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="f1cd3-227">Un valor de 0 indica que no está entrelazado, 1 indica la primera posición, 2 indica la segunda posición, etc.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-227">A value of 0 indicates non-interleaved, 1 indicates the first position, 2 indicates the second position, and so on.</span></span> <span data-ttu-id="f1cd3-228">Por ejemplo, en un 2:1 intercalación, el valor 1 indica que la memoria está en la posición uniforme.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-228">For example, in a 2:1 interleave, a value of 1 indicates that the memory is in the even position.</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-229">**Le**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-229">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-232">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-233">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-233">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="f1cd3-234">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-234">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="f1cd3-235">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-236">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-236">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-237">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-239">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,9 ")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-240">Tipo de memoria física.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-240">Type of physical memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1cd3-241">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-241">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1cd3-242">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-242">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="f1cd3-243">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-243">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="f1cd3-244">**DRAM sincrónica** (3)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-244">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="f1cd3-245">**DRAM de caché** (4)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-245">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="f1cd3-246">**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-246">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="f1cd3-247">**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-247">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="f1cd3-248">**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-248">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="f1cd3-249">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-249">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="f1cd3-250">**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-250">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="f1cd3-251">**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-251">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="f1cd3-252">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-252">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="f1cd3-253">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-253">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="f1cd3-254">**Feprom** (13)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-254">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="f1cd3-255">**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-255">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="f1cd3-256">**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-256">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="f1cd3-257">**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-257">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="f1cd3-258">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-258">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="f1cd3-259">**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-259">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="f1cd3-260">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-260">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="f1cd3-261">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-261">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="f1cd3-262">**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-262">**DDR2** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="f1cd3-263">**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-263">**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1cd3-264">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-264">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-265">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-267">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-267">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-268">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-268">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="f1cd3-269">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-269">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-270">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-270">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-271">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-273">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-274">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-274">Label by which the object is known.</span></span> <span data-ttu-id="f1cd3-275">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-275">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f1cd3-276">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-277">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-277">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-280">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-280">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="f1cd3-281">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-281">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="f1cd3-282">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="f1cd3-282">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="f1cd3-283">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-283">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-284">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-284">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-285">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-287">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-287">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-288">Número de pieza asignado por la organización que produjo o fabricó el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-288">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="f1cd3-289">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-289">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-290">**PositionInRow**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-290">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-291">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-293">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Direcciones asignadas del dispositivo de memoria DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-293">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-294">Posición de la memoria física en una fila.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-294">Position of the physical memory in a row.</span></span> <span data-ttu-id="f1cd3-295">Por ejemplo, si toma dispositivos de memoria de 2 8 bits para formar una fila de 16 bits, un valor de 2 indica que la memoria es el segundo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-295">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 indicates that the memory is the second device.</span></span> <span data-ttu-id="f1cd3-296">Un valor de 0 es un valor no válido para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-296">A value of 0 is an invalid value for this property.</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-297">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-297">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-298">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-300">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-300">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="f1cd3-301">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-301">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-302">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-302">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-303">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-305">Si es **true**, este elemento está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado global.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-305">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="f1cd3-306">Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-306">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="f1cd3-307">Si la potencia puede estar activada y se ha quitado el paquete, el elemento es extraíble y se puede intercambiar en caliente.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-307">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="f1cd3-308">Por ejemplo, un chip de procesador no reduciendo es extraíble.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-308">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="f1cd3-309">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-309">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-310">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-310">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-311">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-313">Si es **true**, es posible reemplazar el elemento por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-313">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="f1cd3-314">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-314">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="f1cd3-315">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-315">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="f1cd3-316">Todos los componentes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-316">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="f1cd3-317">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-317">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-318">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-318">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-321">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-321">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-322">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-322">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="f1cd3-323">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-323">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-324">**SKU**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-324">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-327">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-327">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-328">Número de unidad de almacén para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-328">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="f1cd3-329">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-329">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-330">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-330">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-331">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-333">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanosegundos")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-334">Velocidad de la memoria física, en nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-334">Speed of the physical memory, in nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-335">**Estado**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-336">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-338">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-338">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-339">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-339">Current status of the object.</span></span> <span data-ttu-id="f1cd3-340">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f1cd3-341">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f1cd3-341">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f1cd3-342">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-342">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f1cd3-343">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-343">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f1cd3-344">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-344">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1cd3-345">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-345">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f1cd3-346">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-346">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f1cd3-347">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-347">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f1cd3-348">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-348">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f1cd3-349">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-349">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f1cd3-350">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-350">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f1cd3-351">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-351">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f1cd3-352">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-352">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f1cd3-353">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-353">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1cd3-354">**Tag**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-354">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-357">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-358">Cadena arbitraria que identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-358">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="f1cd3-359">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-359">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="f1cd3-360">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-360">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="f1cd3-361">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-361">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="f1cd3-362">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-362">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="f1cd3-363">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-363">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="f1cd3-364">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-364">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-365">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-365">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-366">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-368">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memoria DMTF \| 002,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="f1cd3-368">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-369">Ancho total, en bits, de la memoria física, incluidos bits de corrección de comprobación o de errores.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-369">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="f1cd3-370">Si no hay bits de corrección de errores, el valor de esta propiedad debe coincidir con el especificado para la propiedad **width** .</span><span class="sxs-lookup"><span data-stu-id="f1cd3-370">If there are no error correction bits, the value in this property should match that specified for the **DataWidth** property.</span></span>

</dd> <dt>

<span data-ttu-id="f1cd3-371">**Versión**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-371">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1cd3-372">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1cd3-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1cd3-374">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f1cd3-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f1cd3-375">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-375">Version of the physical element.</span></span>

<span data-ttu-id="f1cd3-376">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-376">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1cd3-377">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1cd3-377">Remarks</span></span>

<span data-ttu-id="f1cd3-378">La clase **CIM \_ PhysicalMemory** se deriva del [**\_ chip CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-378">The **CIM\_PhysicalMemory** class is derived from [**CIM\_Chip**](cim-chip.md).</span></span>

<span data-ttu-id="f1cd3-379">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-379">WMI does not implement this class.</span></span> <span data-ttu-id="f1cd3-380">Para las clases WMI derivadas de **CIM \_ PhysicalMemory**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd3-380">For WMI classes derived from **CIM\_PhysicalMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f1cd3-381">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-381">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f1cd3-382">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f1cd3-382">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1cd3-383">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1cd3-383">Requirements</span></span>



| <span data-ttu-id="f1cd3-384">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1cd3-384">Requirement</span></span> | <span data-ttu-id="f1cd3-385">Value</span><span class="sxs-lookup"><span data-stu-id="f1cd3-385">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1cd3-386">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1cd3-386">Minimum supported client</span></span><br/> | <span data-ttu-id="f1cd3-387">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1cd3-387">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1cd3-388">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1cd3-388">Minimum supported server</span></span><br/> | <span data-ttu-id="f1cd3-389">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1cd3-389">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1cd3-390">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f1cd3-390">Namespace</span></span><br/>                | <span data-ttu-id="f1cd3-391">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f1cd3-391">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1cd3-392">MOF</span><span class="sxs-lookup"><span data-stu-id="f1cd3-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1cd3-393"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1cd3-393"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1cd3-394">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f1cd3-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1cd3-395"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1cd3-395"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1cd3-396">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1cd3-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1cd3-397">**\_Chip CIM**</span><span class="sxs-lookup"><span data-stu-id="f1cd3-397">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> </dl>

 

