---
description: Representa un dispositivo de memoria física ubicado en un sistema informático y disponible para el sistema operativo.
ms.assetid: 34baca53-ab85-4e06-9853-71b904ede4ab
ms.tgt_platform: multiple
title: Win32_PhysicalMemory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemory
- Win32_PhysicalMemory.Attributes
- Win32_PhysicalMemory.BankLabel
- Win32_PhysicalMemory.Capacity
- Win32_PhysicalMemory.Caption
- Win32_PhysicalMemory.ConfiguredClockSpeed
- Win32_PhysicalMemory.ConfiguredVoltage
- Win32_PhysicalMemory.CreationClassName
- Win32_PhysicalMemory.DataWidth
- Win32_PhysicalMemory.Description
- Win32_PhysicalMemory.DeviceLocator
- Win32_PhysicalMemory.FormFactor
- Win32_PhysicalMemory.HotSwappable
- Win32_PhysicalMemory.InstallDate
- Win32_PhysicalMemory.InterleaveDataDepth
- Win32_PhysicalMemory.InterleavePosition
- Win32_PhysicalMemory.Manufacturer
- Win32_PhysicalMemory.MaxVoltage
- Win32_PhysicalMemory.MemoryType
- Win32_PhysicalMemory.MinVoltage
- Win32_PhysicalMemory.Model
- Win32_PhysicalMemory.Name
- Win32_PhysicalMemory.OtherIdentifyingInfo
- Win32_PhysicalMemory.PartNumber
- Win32_PhysicalMemory.PositionInRow
- Win32_PhysicalMemory.PoweredOn
- Win32_PhysicalMemory.Removable
- Win32_PhysicalMemory.Replaceable
- Win32_PhysicalMemory.SerialNumber
- Win32_PhysicalMemory.SKU
- Win32_PhysicalMemory.SMBIOSMemoryType
- Win32_PhysicalMemory.Speed
- Win32_PhysicalMemory.Status
- Win32_PhysicalMemory.Tag
- Win32_PhysicalMemory.TotalWidth
- Win32_PhysicalMemory.TypeDetail
- Win32_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e026c3c3d0a29bbbd10ed2b5565708f0bcb0900c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496721"
---
# <a name="win32_physicalmemory-class"></a><span data-ttu-id="0e529-103">\_Clase Win32 PhysicalMemory</span><span class="sxs-lookup"><span data-stu-id="0e529-103">Win32\_PhysicalMemory class</span></span>

<span data-ttu-id="0e529-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PhysicalMemory de Win32** representa un dispositivo de memoria física ubicado en un sistema informático y disponible para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0e529-104">The **Win32\_PhysicalMemory** [WMI class](../wmisdk/retrieving-a-class.md) represents a physical memory device located on a computer system and available to the operating system.</span></span>

<span data-ttu-id="0e529-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0e529-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0e529-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="0e529-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e529-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e529-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B93-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemory : CIM_PhysicalMemory
{
  uint32   Attributes;
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  uint32   ConfiguredClockSpeed;
  uint32   ConfiguredVoltage;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  string   DeviceLocator;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   InterleaveDataDepth;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint32   MaxVoltage;
  uint16   MemoryType;
  uint32   MinVoltage;
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
  uint32   SMBIOSMemoryType;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  uint16   TypeDetail;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="0e529-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0e529-108">Members</span></span>

<span data-ttu-id="0e529-109">La **clase \_ PhysicalMemory de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0e529-109">The **Win32\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="0e529-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e529-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e529-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e529-111">Properties</span></span>

<span data-ttu-id="0e529-112">La **clase \_ PhysicalMemory de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0e529-112">The **Win32\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e529-113">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="0e529-113">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e529-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-116">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| atributos de tipo SMBIOS 17 \| ")</span><span class="sxs-lookup"><span data-stu-id="0e529-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Attributes")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-117">SMBIOS-tipo 17-atributos.</span><span class="sxs-lookup"><span data-stu-id="0e529-117">SMBIOS - Type 17 - Attributes.</span></span> <span data-ttu-id="0e529-118">Representa el rango.</span><span class="sxs-lookup"><span data-stu-id="0e529-118">Represents the RANK.</span></span>

<span data-ttu-id="0e529-119">Este valor procede del miembro **attributes** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-119">This value comes from the **Attributes** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-120">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0e529-120">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0e529-121">**BankLabel**</span><span class="sxs-lookup"><span data-stu-id="0e529-121">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-124">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memoria DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="0e529-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-125">El Banco con etiqueta física donde se encuentra la memoria.</span><span class="sxs-lookup"><span data-stu-id="0e529-125">Physically labeled bank where the memory is located.</span></span>

<span data-ttu-id="0e529-126">Ejemplos: "Bank 0", "Bank A"</span><span class="sxs-lookup"><span data-stu-id="0e529-126">Examples: "Bank 0", "Bank A"</span></span>

<span data-ttu-id="0e529-127">Este valor procede del miembro del **localizador bancario** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-127">This value comes from the **Bank Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-128">Esta propiedad se hereda de [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-128">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-129">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="0e529-129">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-130">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e529-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-132">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memoria DMTF \| 002,5 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="0e529-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-133">Capacidad total de la memoria física, en bytes.</span><span class="sxs-lookup"><span data-stu-id="0e529-133">Total capacity of the physical memory—in bytes.</span></span>

<span data-ttu-id="0e529-134">Este valor procede de la estructura del **dispositivo de memoria** en la información de la versión de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-134">This value comes from the **Memory Device** structure in the SMBIOS version information.</span></span> <span data-ttu-id="0e529-135">En el caso de las versiones de SMBIOS 2,1 a 2,6, el valor procede del miembro **size** .</span><span class="sxs-lookup"><span data-stu-id="0e529-135">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Size** member.</span></span> <span data-ttu-id="0e529-136">En el caso de la versión 2.7 de SMBIOS, el valor procede del miembro de **tamaño extendido** .</span><span class="sxs-lookup"><span data-stu-id="0e529-136">For SMBIOS version 2.7+ the value comes from the **Extended Size** member.</span></span>

<span data-ttu-id="0e529-137">Esta propiedad se hereda de [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-137">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<span data-ttu-id="0e529-138">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0e529-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-142">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0e529-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-143">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="0e529-143">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="0e529-144">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-145">**ConfiguredClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="0e529-145">**ConfiguredClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e529-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-148">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (tipo de SMBIOS \| 17 \| velocidad del reloj de memoria configurada ")</span><span class="sxs-lookup"><span data-stu-id="0e529-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured Memory Clock Speed")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-149">La velocidad de reloj configurada del dispositivo de memoria, en megahercios (MHz) o 0, si se desconoce la velocidad.</span><span class="sxs-lookup"><span data-stu-id="0e529-149">The configured clock speed of the memory device, in megahertz (MHz), or 0, if the speed is unknown.</span></span>

<span data-ttu-id="0e529-150">Este valor procede del miembro de **velocidad del reloj de memoria configurada** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-150">This value comes from the **Configured Memory Clock Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-151">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0e529-151">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0e529-152">**ConfiguredVoltage**</span><span class="sxs-lookup"><span data-stu-id="0e529-152">**ConfiguredVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-153">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e529-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-155">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| voltaje de tipo 17 configurado de SMBIOS \| ")</span><span class="sxs-lookup"><span data-stu-id="0e529-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured voltage")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-156">Voltaje configurado para este dispositivo, en milivoltios o 0, si se desconoce la tensión.</span><span class="sxs-lookup"><span data-stu-id="0e529-156">Configured voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="0e529-157">Este valor procede del miembro de **voltaje configurado** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-157">This value comes from the **Configured voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-158">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0e529-158">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0e529-159">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e529-159">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-162">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0e529-162">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e529-163">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="0e529-163">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0e529-164">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="0e529-164">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="0e529-165">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-165">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-166">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="0e529-166">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e529-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-169">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memoria DMTF \| 002,8 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="0e529-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-170">Ancho de datos de la memoria física, en bits.</span><span class="sxs-lookup"><span data-stu-id="0e529-170">Data width of the physical memory—in bits.</span></span> <span data-ttu-id="0e529-171">Un ancho de datos de 0 (cero) y un ancho total de 8 (ocho) indica que la memoria se usa únicamente para proporcionar bits de corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="0e529-171">A data width of 0 (zero) and a total width of 8 (eight) indicates that the memory is used solely to provide error correction bits.</span></span>

<span data-ttu-id="0e529-172">Este valor procede del miembro de **ancho de datos** de la estructura del dispositivo de **memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-172">This value comes from the **Data Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-173">Esta propiedad se hereda de [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-173">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-174">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e529-174">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-177">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="0e529-177">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-178">Descripción de un objeto.</span><span class="sxs-lookup"><span data-stu-id="0e529-178">Description of an object.</span></span>

<span data-ttu-id="0e529-179">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-180">**DeviceLocator**</span><span class="sxs-lookup"><span data-stu-id="0e529-180">**DeviceLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-183">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| localizador de dispositivos de tipo SMBIOS 17 \| ")</span><span class="sxs-lookup"><span data-stu-id="0e529-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Device Locator")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-184">Etiqueta del socket o tablero de circuitos que contiene la memoria.</span><span class="sxs-lookup"><span data-stu-id="0e529-184">Label of the socket or circuit board that holds the memory.</span></span>

<span data-ttu-id="0e529-185">Ejemplo: "SIMM 3"</span><span class="sxs-lookup"><span data-stu-id="0e529-185">Example: "SIMM 3"</span></span>

<span data-ttu-id="0e529-186">Este valor procede del miembro del **localizador de dispositivos** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-186">This value comes from the **Device Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="0e529-187">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="0e529-187">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-188">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e529-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-190">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memoria DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="0e529-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-191">Factor de forma de implementación para el chip.</span><span class="sxs-lookup"><span data-stu-id="0e529-191">Implementation form factor for the chip.</span></span>

<span data-ttu-id="0e529-192">Este valor procede del miembro **factor de forma** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-192">This value comes from the **Form Factor** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-193">Esta propiedad se hereda del [**\_ chip CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-193">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>



 <span data-ttu-id="0e529-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="0e529-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-195">Unknown</span><span class="sxs-lookup"><span data-stu-id="0e529-195">Unknown</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-196">(1)</span><span class="sxs-lookup"><span data-stu-id="0e529-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-197">Otros</span><span class="sxs-lookup"><span data-stu-id="0e529-197">Other</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-198">(2)</span><span class="sxs-lookup"><span data-stu-id="0e529-198">(2)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-199">SIP</span><span class="sxs-lookup"><span data-stu-id="0e529-199">SIP</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-200">(3)</span><span class="sxs-lookup"><span data-stu-id="0e529-200">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-201">DIP</span><span class="sxs-lookup"><span data-stu-id="0e529-201">DIP</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-202">(4)</span><span class="sxs-lookup"><span data-stu-id="0e529-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-203">ZIP</span><span class="sxs-lookup"><span data-stu-id="0e529-203">ZIP</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-204">(5)</span><span class="sxs-lookup"><span data-stu-id="0e529-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-205">SOJ</span><span class="sxs-lookup"><span data-stu-id="0e529-205">SOJ</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="0e529-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-207">Propietario</span><span class="sxs-lookup"><span data-stu-id="0e529-207">Proprietary</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-208">(7)</span><span class="sxs-lookup"><span data-stu-id="0e529-208">(7)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-209">SIMM</span><span class="sxs-lookup"><span data-stu-id="0e529-209">SIMM</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-210">(8)</span><span class="sxs-lookup"><span data-stu-id="0e529-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-211">APARECERÁ</span><span class="sxs-lookup"><span data-stu-id="0e529-211">DIMM</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-212">(9)</span><span class="sxs-lookup"><span data-stu-id="0e529-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-213">TSOP</span><span class="sxs-lookup"><span data-stu-id="0e529-213">TSOP</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-214">(10)</span><span class="sxs-lookup"><span data-stu-id="0e529-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-215">PGA</span><span class="sxs-lookup"><span data-stu-id="0e529-215">PGA</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-216">(11)</span><span class="sxs-lookup"><span data-stu-id="0e529-216">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-217">SEMÁFORO</span><span class="sxs-lookup"><span data-stu-id="0e529-217">RIMM</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-218">(12)</span><span class="sxs-lookup"><span data-stu-id="0e529-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-219">SODIMM</span><span class="sxs-lookup"><span data-stu-id="0e529-219">SODIMM</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-220">(13)</span><span class="sxs-lookup"><span data-stu-id="0e529-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-221">SRIMM</span><span class="sxs-lookup"><span data-stu-id="0e529-221">SRIMM</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-222">(14)</span><span class="sxs-lookup"><span data-stu-id="0e529-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-223">SMD</span><span class="sxs-lookup"><span data-stu-id="0e529-223">SMD</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-224">(15)</span><span class="sxs-lookup"><span data-stu-id="0e529-224">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-225">SSMP</span><span class="sxs-lookup"><span data-stu-id="0e529-225">SSMP</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-226">(16)</span><span class="sxs-lookup"><span data-stu-id="0e529-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-227">QFP</span><span class="sxs-lookup"><span data-stu-id="0e529-227">QFP</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-228">(17)</span><span class="sxs-lookup"><span data-stu-id="0e529-228">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-229">TQFP</span><span class="sxs-lookup"><span data-stu-id="0e529-229">TQFP</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-230">(18)</span><span class="sxs-lookup"><span data-stu-id="0e529-230">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-231">SOIC</span><span class="sxs-lookup"><span data-stu-id="0e529-231">SOIC</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-232">(19)</span><span class="sxs-lookup"><span data-stu-id="0e529-232">(19)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-233">LCC</span><span class="sxs-lookup"><span data-stu-id="0e529-233">LCC</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-234">(20)</span><span class="sxs-lookup"><span data-stu-id="0e529-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-235">PLCC</span><span class="sxs-lookup"><span data-stu-id="0e529-235">PLCC</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-236">(21)</span><span class="sxs-lookup"><span data-stu-id="0e529-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-237">BGA</span><span class="sxs-lookup"><span data-stu-id="0e529-237">BGA</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-238">(22)</span><span class="sxs-lookup"><span data-stu-id="0e529-238">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-239">FPBGA</span><span class="sxs-lookup"><span data-stu-id="0e529-239">FPBGA</span></span>

</dd> <dt>



 <span data-ttu-id="0e529-240">(23)</span><span class="sxs-lookup"><span data-stu-id="0e529-240">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-241">LGA</span><span class="sxs-lookup"><span data-stu-id="0e529-241">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e529-242">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="0e529-242">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-243">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0e529-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e529-245">Si **es true**, este componente de medios físicos se puede reemplazar por uno físicamente diferente pero equivalente mientras el paquete contenedor tiene la energía aplicada.</span><span class="sxs-lookup"><span data-stu-id="0e529-245">If **TRUE**, this physical media component can be replaced with a physically different but equivalent one while the containing package has the power applied.</span></span> <span data-ttu-id="0e529-246">Por ejemplo, un componente de ventilador se puede diseñar para que se intercambie en caliente.</span><span class="sxs-lookup"><span data-stu-id="0e529-246">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="0e529-247">Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="0e529-247">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="0e529-248">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-248">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0e529-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-250">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e529-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-252">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="0e529-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-253">Fecha y hora de instalación del objeto.</span><span class="sxs-lookup"><span data-stu-id="0e529-253">Date and time the object is installed.</span></span> <span data-ttu-id="0e529-254">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="0e529-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0e529-255">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-256">**InterleaveDataDepth**</span><span class="sxs-lookup"><span data-stu-id="0e529-256">**InterleaveDataDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-257">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e529-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-259">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| profundidad de \| datos intercalados de tipo SMBIOS 20")</span><span class="sxs-lookup"><span data-stu-id="0e529-259">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Interleaved Data Depth")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-260">Entero de 16 bits sin signo número máximo de filas consecutivas de datos a las que se tiene acceso en una única transferencia intercalada desde el dispositivo de memoria.</span><span class="sxs-lookup"><span data-stu-id="0e529-260">Unsigned 16-bit integer maximum number of consecutive rows of data that are accessed in a single interleaved transfer from the memory device.</span></span> <span data-ttu-id="0e529-261">Si el valor es 0 (cero), la memoria no se intercalará.</span><span class="sxs-lookup"><span data-stu-id="0e529-261">If the value is 0 (zero), the memory is not interleaved.</span></span>

</dd> <dt>

<span data-ttu-id="0e529-262">**InterleavePosition**</span><span class="sxs-lookup"><span data-stu-id="0e529-262">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-263">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e529-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-265">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Direcciones asignadas del dispositivo de memoria DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="0e529-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-266">Posición de la memoria física en una intercalación.</span><span class="sxs-lookup"><span data-stu-id="0e529-266">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="0e529-267">Por ejemplo, en un 2:1 intercalación, un valor de "1" indica que la memoria está en la posición "incluso".</span><span class="sxs-lookup"><span data-stu-id="0e529-267">For example, in a 2:1 interleave, a value of "1" indicates that the memory is in the "even" position.</span></span>

<span data-ttu-id="0e529-268">Esta propiedad se hereda de [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-268">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span data-ttu-id="0e529-269">0</span><span class="sxs-lookup"><span data-stu-id="0e529-269">0</span></span>
</dt> <dd>

<span data-ttu-id="0e529-270">No intercalado</span><span class="sxs-lookup"><span data-stu-id="0e529-270">Noninterleaved</span></span>

</dd> <dt>

<span data-ttu-id="0e529-271">1</span><span class="sxs-lookup"><span data-stu-id="0e529-271">1</span></span>
</dt> <dd>

<span data-ttu-id="0e529-272">Primera posición</span><span class="sxs-lookup"><span data-stu-id="0e529-272">First position</span></span>

</dd> <dt>

<span data-ttu-id="0e529-273">2</span><span class="sxs-lookup"><span data-stu-id="0e529-273">2</span></span>
</dt> <dd>

<span data-ttu-id="0e529-274">Segunda posición</span><span class="sxs-lookup"><span data-stu-id="0e529-274">Second position</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e529-275">**Le**</span><span class="sxs-lookup"><span data-stu-id="0e529-275">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-276">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-278">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0e529-278">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e529-279">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="0e529-279">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="0e529-280">Este valor procede del miembro **manufacturer** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-280">This value comes from the **Manufacturer** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-281">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-282">**MaxVoltage**</span><span class="sxs-lookup"><span data-stu-id="0e529-282">**MaxVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-283">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e529-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-285">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| voltaje máximo de tipo SMBIOS 17 \| ")</span><span class="sxs-lookup"><span data-stu-id="0e529-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Maximum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-286">El voltaje de funcionamiento máximo para este dispositivo, en milivoltios o 0, si se desconoce la tensión.</span><span class="sxs-lookup"><span data-stu-id="0e529-286">The maximum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="0e529-287">Este valor procede del miembro de **voltaje máximo** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-287">This value comes from the **Maximum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-288">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0e529-288">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0e529-289">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="0e529-289">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-290">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e529-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-292">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memoria DMTF \| 002,9 ")</span><span class="sxs-lookup"><span data-stu-id="0e529-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-293">Tipo de memoria física.</span><span class="sxs-lookup"><span data-stu-id="0e529-293">Type of physical memory.</span></span> <span data-ttu-id="0e529-294">Se trata de un valor de CIM que se asigna al valor de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-294">This is a CIM value that is mapped to the SMBIOS value.</span></span> <span data-ttu-id="0e529-295">La propiedad **SMBIOSMemoryType** contiene el tipo de memoria de SMBIOS sin procesar.</span><span class="sxs-lookup"><span data-stu-id="0e529-295">The **SMBIOSMemoryType** property contains the raw SMBIOS memory type.</span></span>

<span data-ttu-id="0e529-296">Este valor procede del miembro de **tipo de memoria** de la estructura del dispositivo de **memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-296">This value comes from the **Memory Type** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-297">Esta propiedad se hereda de [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-297">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e529-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0e529-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e529-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="0e529-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="0e529-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="0e529-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="0e529-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**DRAM sincrónica** (3)</span><span class="sxs-lookup"><span data-stu-id="0e529-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="0e529-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**DRAM de caché** (4)</span><span class="sxs-lookup"><span data-stu-id="0e529-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="0e529-303"><span id="EDO"></span><span id="edo"></span>**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="0e529-303"><span id="EDO"></span><span id="edo"></span>**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="0e529-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="0e529-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="0e529-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="0e529-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="0e529-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="0e529-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="0e529-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="0e529-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="0e529-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="0e529-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="0e529-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="0e529-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="0e529-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="0e529-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="0e529-311"><span id="FEPROM"></span><span id="feprom"></span>**Feprom** (13)</span><span class="sxs-lookup"><span data-stu-id="0e529-311"><span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="0e529-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="0e529-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="0e529-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="0e529-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="0e529-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="0e529-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="0e529-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="0e529-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="0e529-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="0e529-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="0e529-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="0e529-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="0e529-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="0e529-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="0e529-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="0e529-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-320">DDR2: puede que no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="0e529-320">DDR2—May not be available.</span></span>

</dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="0e529-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="0e529-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-322">DDR2: FB-DIMM, puede que no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="0e529-322">DDR2—FB-DIMM,May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="0e529-323">24</span><span class="sxs-lookup"><span data-stu-id="0e529-323">24</span></span>
</dt> <dd>

<span data-ttu-id="0e529-324">DDR3: puede que no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="0e529-324">DDR3—May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="0e529-325">25</span><span class="sxs-lookup"><span data-stu-id="0e529-325">25</span></span>
</dt> <dd>

<span data-ttu-id="0e529-326">FBD2</span><span class="sxs-lookup"><span data-stu-id="0e529-326">FBD2</span></span>

</dt> <dd></dd> <dt>

<span data-ttu-id="0e529-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span><span class="sxs-lookup"><span data-stu-id="0e529-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e529-328">**MinVoltage**</span><span class="sxs-lookup"><span data-stu-id="0e529-328">**MinVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-329">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e529-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-331">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| voltaje mínimo de tipo de SMBIOS 20 \| ")</span><span class="sxs-lookup"><span data-stu-id="0e529-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Minimum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-332">La tensión de funcionamiento mínima para este dispositivo, en milivoltios o 0, si se desconoce la tensión.</span><span class="sxs-lookup"><span data-stu-id="0e529-332">The minimum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="0e529-333">Este valor procede del miembro de **voltaje mínimo** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-333">This value comes from the **Minimum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-334">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0e529-334">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0e529-335">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="0e529-335">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-336">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-338">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0e529-338">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e529-339">Nombre del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="0e529-339">Name for the physical element.</span></span>

<span data-ttu-id="0e529-340">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-340">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-341">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0e529-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-342">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-344">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0e529-344">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-345">Etiqueta del objeto.</span><span class="sxs-lookup"><span data-stu-id="0e529-345">Label for the object.</span></span> <span data-ttu-id="0e529-346">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="0e529-346">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="0e529-347">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0e529-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e529-351">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="0e529-351">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="0e529-352">Un ejemplo son los datos de código de barras asociados a un elemento que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="0e529-352">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="0e529-353">Si solo los datos de código de barras están disponibles y son únicos o se pueden usar como una clave de elemento, esta propiedad será **null** y los datos de código de barras se utilizarán como clave de clase en la propiedad de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="0e529-353">If only bar code data is available and unique or able to be used as an element key, this property is be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="0e529-354">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-355">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="0e529-355">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-356">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-358">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0e529-358">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e529-359">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="0e529-359">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="0e529-360">Este valor procede del miembro **número de pieza** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-360">This value comes from the **Part Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-361">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-361">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-362">**PositionInRow**</span><span class="sxs-lookup"><span data-stu-id="0e529-362">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-363">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e529-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-365">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Direcciones asignadas del dispositivo de memoria DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="0e529-365">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-366">Posición de la memoria física en una fila.</span><span class="sxs-lookup"><span data-stu-id="0e529-366">Position of the physical memory in a row.</span></span> <span data-ttu-id="0e529-367">Por ejemplo, si toma dispositivos de memoria de 2 8 bits para formar una fila de 16 bits, un valor de 2 (dos) significa que esta memoria es el segundo dispositivo; 0 (cero) es un valor no válido para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0e529-367">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 (two) means that this memory is the second device—0 (zero) is an invalid value for this property.</span></span>

<span data-ttu-id="0e529-368">Esta propiedad se hereda de [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-368">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-369">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="0e529-369">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-370">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0e529-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e529-372">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="0e529-372">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="0e529-373">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-373">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-374">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="0e529-374">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-375">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0e529-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e529-377">Si es **true**, un componente físico es extraíble (si está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado general).</span><span class="sxs-lookup"><span data-stu-id="0e529-377">If **TRUE**, a physical component is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="0e529-378">Un componente puede seguir siendo extraíble si la alimentación debe estar "desactivada" para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="0e529-378">A component can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="0e529-379">Si la potencia puede ser "ON" y se ha quitado el componente, el elemento es extraíble y puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="0e529-379">If power can be "on" and the component removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="0e529-380">Por ejemplo, un chip de Procesador actualizable es extraíble.</span><span class="sxs-lookup"><span data-stu-id="0e529-380">For example, an upgradable processor chip is removable.</span></span>

<span data-ttu-id="0e529-381">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-381">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-382">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="0e529-382">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-383">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0e529-383">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e529-385">Si **es true**, este componente de medio físico se puede reemplazar por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="0e529-385">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="0e529-386">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="0e529-386">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="0e529-387">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="0e529-387">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="0e529-388">Todos los componentes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="0e529-388">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="0e529-389">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-389">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-390">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="0e529-390">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-391">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-393">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0e529-393">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e529-394">Número asignado por el fabricante para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="0e529-394">Manufacturer-allocated number to identify the physical element.</span></span>

<span data-ttu-id="0e529-395">Este valor procede del miembro del **número de serie** de la estructura del dispositivo de **memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-395">This value comes from the **Serial Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-396">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-396">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-397">**SKU**</span><span class="sxs-lookup"><span data-stu-id="0e529-397">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-398">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-400">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0e529-400">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e529-401">Número de referencia de almacén para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="0e529-401">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="0e529-402">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-402">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-403">**SMBIOSMemoryType**</span><span class="sxs-lookup"><span data-stu-id="0e529-403">**SMBIOSMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-404">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e529-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-406">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (tipo de \| memoria de tipo SMBIOS 17 \| \_ )</span><span class="sxs-lookup"><span data-stu-id="0e529-406">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Memory\_Type")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-407">El tipo de memoria de SMBIOS sin procesar.</span><span class="sxs-lookup"><span data-stu-id="0e529-407">The raw SMBIOS memory type.</span></span> <span data-ttu-id="0e529-408">El valor de la propiedad **MemoryType** es un valor de CIM que se asigna al valor de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-408">The value of the **MemoryType** property is a CIM value that is mapped to the SMBIOS value.</span></span>

<span data-ttu-id="0e529-409">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0e529-409">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="0e529-410">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="0e529-410">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-411">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e529-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-412">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-413">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("nanosegundos")</span><span class="sxs-lookup"><span data-stu-id="0e529-413">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-414">Velocidad de la memoria física: en nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="0e529-414">Speed of the physical memory—in nanoseconds.</span></span>

<span data-ttu-id="0e529-415">Este valor procede del miembro **Speed** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-415">This value comes from the **Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-416">Esta propiedad se hereda de [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-416">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-417">**Estado**</span><span class="sxs-lookup"><span data-stu-id="0e529-417">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-418">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-420">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="0e529-420">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-421">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="0e529-421">Current status of the object.</span></span> <span data-ttu-id="0e529-422">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="0e529-422">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0e529-423">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="0e529-423">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0e529-424">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="0e529-424">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0e529-425">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="0e529-425">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0e529-426">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="0e529-426">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0e529-427">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-427">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0e529-428">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="0e529-428">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0e529-429">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="0e529-429">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0e529-430">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="0e529-430">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0e529-431">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="0e529-431">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e529-432">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="0e529-432">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0e529-433">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="0e529-433">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0e529-434">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="0e529-434">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0e529-435">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="0e529-435">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0e529-436">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="0e529-436">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0e529-437">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="0e529-437">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0e529-438">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="0e529-438">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0e529-439">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="0e529-439">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0e529-440">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="0e529-440">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e529-441">**Tag**</span><span class="sxs-lookup"><span data-stu-id="0e529-441">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-442">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-443">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-444">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**invalidación**](../wmisdk/standard-qualifiers.md) ("etiqueta"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="0e529-444">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-445">Identificador único para el dispositivo de memoria física representado por una instancia de **Win32 \_ PhysicalMemory**.</span><span class="sxs-lookup"><span data-stu-id="0e529-445">Unique identifier for the physical memory device that is represented by an instance of **Win32\_PhysicalMemory**.</span></span> <span data-ttu-id="0e529-446">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-446">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="0e529-447">Ejemplo: "memoria física 1"</span><span class="sxs-lookup"><span data-stu-id="0e529-447">Example: "Physical Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="0e529-448">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="0e529-448">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-449">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e529-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-451">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memoria DMTF \| 002,7 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="0e529-451">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-452">Ancho total, en bits, de la memoria física, incluidos bits de corrección de comprobación o de errores.</span><span class="sxs-lookup"><span data-stu-id="0e529-452">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="0e529-453">Si no hay bits de corrección de errores, el valor de esta propiedad debe coincidir con lo que se especifica para la propiedad de **ancho** de campo.</span><span class="sxs-lookup"><span data-stu-id="0e529-453">If there are no error correction bits, the value in this property should match what is specified for the **DataWidth** property.</span></span>

<span data-ttu-id="0e529-454">Este valor procede del miembro de **ancho total** de la estructura del **dispositivo de memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-454">This value comes from the **Total Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e529-455">Esta propiedad se hereda de [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-455">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e529-456">**TypeDetail**</span><span class="sxs-lookup"><span data-stu-id="0e529-456">**TypeDetail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-457">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e529-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-458">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-459">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| detalle del tipo de SMBIOS de tipo 17 \| ")</span><span class="sxs-lookup"><span data-stu-id="0e529-459">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Type Detail")</span></span>
</dt> </dl>

<span data-ttu-id="0e529-460">Tipo de memoria física representada.</span><span class="sxs-lookup"><span data-stu-id="0e529-460">Type of physical memory represented.</span></span>

<span data-ttu-id="0e529-461">Este valor procede del miembro de **detalle de tipo** de la estructura del dispositivo de **memoria** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e529-461">This value comes from the **Type Detail** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="0e529-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (1)</span><span class="sxs-lookup"><span data-stu-id="0e529-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e529-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (2)</span><span class="sxs-lookup"><span data-stu-id="0e529-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e529-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (4)</span><span class="sxs-lookup"><span data-stu-id="0e529-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>

<span data-ttu-id="0e529-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Paginación rápida** (8)</span><span class="sxs-lookup"><span data-stu-id="0e529-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Fast-paged** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>

<span data-ttu-id="0e529-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Columna estática** (16)</span><span class="sxs-lookup"><span data-stu-id="0e529-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Static column** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>

<span data-ttu-id="0e529-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-estático** (32)</span><span class="sxs-lookup"><span data-stu-id="0e529-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-static** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="RAMBUS"></span><span id="rambus"></span>

<span data-ttu-id="0e529-468"><span id="RAMBUS"></span><span id="rambus"></span>**Rambus** (64)</span><span class="sxs-lookup"><span data-stu-id="0e529-468"><span id="RAMBUS"></span><span id="rambus"></span>**RAMBUS** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="0e529-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Sincrónicos** (128)</span><span class="sxs-lookup"><span data-stu-id="0e529-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchronous** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="CMOS"></span><span id="cmos"></span>

<span data-ttu-id="0e529-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span><span class="sxs-lookup"><span data-stu-id="0e529-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="0e529-471"><span id="EDO"></span><span id="edo"></span>**Edo** (512)</span><span class="sxs-lookup"><span data-stu-id="0e529-471"><span id="EDO"></span><span id="edo"></span>**EDO** (512)</span></span>


</dt> <dd></dd> <dt>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>

<span data-ttu-id="0e529-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**DRAM de ventana** (1024)</span><span class="sxs-lookup"><span data-stu-id="0e529-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**Window DRAM** (1024)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="0e529-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**DRAM de caché** (2048)</span><span class="sxs-lookup"><span data-stu-id="0e529-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (2048)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>

<span data-ttu-id="0e529-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**No volátil** (4096)</span><span class="sxs-lookup"><span data-stu-id="0e529-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Non-volatile** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="0e529-475">No volátil</span><span class="sxs-lookup"><span data-stu-id="0e529-475">Nonvolatile</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e529-476">**Versión**</span><span class="sxs-lookup"><span data-stu-id="0e529-476">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e529-477">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e529-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e529-478">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e529-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e529-479">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0e529-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e529-480">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="0e529-480">Version of the physical element.</span></span>

<span data-ttu-id="0e529-481">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-481">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e529-482">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e529-482">Remarks</span></span>

<span data-ttu-id="0e529-483">La **clase \_ PhysicalMemory de Win32** se deriva de [**\_ PhysicalMemory de CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e529-483">The **Win32\_PhysicalMemory** class is derived from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0e529-484">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0e529-484">Examples</span></span>

<span data-ttu-id="0e529-485">El ejemplo de PowerShell [Get-ComputerInfo-Query Computer info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) de PowerShell en la galería de TechNet utiliza varias llamadas a hardware y software, incluido **Win32 \_ PhysicalMemory**, para mostrar información acerca de un sistema local o remoto.</span><span class="sxs-lookup"><span data-stu-id="0e529-485">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to display information about a local or remote system.</span></span>

<span data-ttu-id="0e529-486">El ejemplo de PowerShell para [informes de servidor](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) en la galería de TechNet usa una serie de llamadas a hardware y software, incluido **Win32 \_ PhysicalMemory**, para recopilar información del servidor y publicarla en un documento de Word.</span><span class="sxs-lookup"><span data-stu-id="0e529-486">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to gather server information and publish in Word document.</span></span>

<span data-ttu-id="0e529-487">El siguiente ejemplo de código de PowerShell recupera información relacionada con la memoria física del equipo local.</span><span class="sxs-lookup"><span data-stu-id="0e529-487">The following PowerShell code sample retrieves information regarding the physical memory of the local computer.</span></span>


```PowerShell
function get-WmiMemoryFormFactor {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 22) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-SiP"}
3     {"03-DIP"}
4     {"04-ZIP"}
5     {"05-SOJ"}
6     {"06-Proprietary"}
7     {"07-SIMM"}
8     {"08-DIMM"}
9     {"09-TSOPO"}
10     {"10-PGA"}
11     {"11-RIM"}
12     {"12-SODIMM"}
13     {"13-SRIMM"}
14     {"14-SMD"}
15     {"15-SSMP"}
16     {"16-QFP"}
17     {"17-TQFP"}
18     {"18-SOIC"}
19     {"19-LCC"}
20     {"20-PLCC"}
21     {"21-FPGA"}
22     {"22-LGA"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}

# Helper function to return memory Interleave  Position

function get-WmiInterleavePosition {
param ([uint32] $char)

If ($char -ge 0 -and  $char -le 2) {

switch ($char) {
0     {"00-Non-Interleaved"}
1     {"01-First Position"}
2     {"02-Second Position"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}


# Helper function to return Memory Tupe
function get-WmiMemoryType {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 20) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-DRAM"}
3     {"03-Synchronous DRAM"}
4     {"04-Cache DRAM"}
5     {"05-EDO"}
6     {"06-EDRAM"}
7     {"07-VRAM"}
8     {"08-SRAM"}
9     {"09-ROM"}
10     {"10-ROM"}
11     {"11-FLASH"}
12     {"12-EEPROM"}
13     {"13-FEPROM"}
14     {"14-EPROM"}
15     {"15-CDRAM"}
16     {"16-3DRAM"}
17     {"17-SDRAM"}
18     {"18-SGRAM"}
19     {"19-RDRAM"}
20     {"20-DDR"}
}

}

else {"{0} - undefined value" -f $char
}

Return
}


# Get the object
$memory = Get-WMIObject Win32_PhysicalMemory

#  Format and Print
"System has {0} memory sticks:" -f $memory.count

Foreach ($stick in $memory) {

# Do some conversions
$cap=$stick.capacity/1mb
$ff=get-WmiMemoryFormFactor($stick.FormFactor)
$ilp=get-WmiInterleavePosition($stick.InterleavePosition)
$mt=get-WMIMemoryType($stick.MemoryType)

# print details of each stick
"BankLabel            {0}"  -f $stick.banklabel
"Capacity (MB)        {0}"  -f $cap
"Caption              {0}"  -f $stick.Caption
"CreationClassName    {0}"  -f $stick.creationclassname
"DataWidth            {0}"  -f $stick.DataWidth
"Description          {0}"  -f $stick.Description
"DeviceLocator        {0}"  -f $stick.DeviceLocator
"FormFactor           {0}"  -f $ff
"HotSwappable         {0}"  -f $stick.HotSwappable
"InstallDate          {0}"  -f $stick.InstallDate
"InterleaveDataDepth  {0}"  -f $stick.InterleaveDataDepth
"InterleavePosition   {0}"  -f $ilp
"Manufacturer         {0}"  -f $stick.Manufacturer
"MemoryType           {0}"  -f $mt
"Model                {0}"  -f $stick.Model
"Name                 {0}"  -f $stick.Name
"OtherIdentifyingInfo {0}"  -f $stick.OtherIdentifyingInfo
"PartNumber           {0}"  -f $stick.PartNumber
"PositionInRow        {0}"  -f $stick.PositionInRow
"PoweredOn            {0}"  -f $stick.PoweredOn
"Removable            {0}"  -f $stick.Removable
"Replaceable          {0}"  -f $stick.Replaceable
"SerialNumber         {0}"  -f $stick.SerialNumber
"SKU                  {0}"  -f $stick.SKU 
"Speed                {0}"  -f $stick.Speed 
"Status               {0}"  -f $stick.Status
"Tag                  {0}"  -f $stick.Tag
"TotalWidth           {0}"  -f $stick.TotalWidth 
"TypeDetail           {0}"  -f $stick.TypeDetail
"Version              {0}"  -f $stick.Version
""
}
"-----"
```



## <a name="requirements"></a><span data-ttu-id="0e529-488">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e529-488">Requirements</span></span>



| <span data-ttu-id="0e529-489">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e529-489">Requirement</span></span> | <span data-ttu-id="0e529-490">Value</span><span class="sxs-lookup"><span data-stu-id="0e529-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e529-491">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e529-491">Minimum supported client</span></span><br/> | <span data-ttu-id="0e529-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e529-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e529-493">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e529-493">Minimum supported server</span></span><br/> | <span data-ttu-id="0e529-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e529-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e529-495">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0e529-495">Namespace</span></span><br/>                | <span data-ttu-id="0e529-496">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0e529-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e529-497">MOF</span><span class="sxs-lookup"><span data-stu-id="0e529-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e529-498"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e529-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e529-499">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0e529-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e529-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e529-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e529-501">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e529-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e529-502">**\_PHYSICALMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="0e529-502">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dt>

[<span data-ttu-id="0e529-503">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="0e529-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
