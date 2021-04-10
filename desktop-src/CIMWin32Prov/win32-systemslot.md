---
description: Win32 \_ SystemSlot &\# 32; La clase WMI representa puntos de conexión físicos, incluidos puertos, ranuras de la placa base y periféricos, y puntos de conexión de propiedad.
ms.assetid: 0bdce597-dcbe-4593-b0d6-68c3bfecd0ee
ms.tgt_platform: multiple
title: Win32_SystemSlot (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSlot
- Win32_SystemSlot.BusNumber
- Win32_SystemSlot.Caption
- Win32_SystemSlot.ConnectorPinout
- Win32_SystemSlot.ConnectorType
- Win32_SystemSlot.CreationClassName
- Win32_SystemSlot.CurrentUsage
- Win32_SystemSlot.Description
- Win32_SystemSlot.DeviceNumber
- Win32_SystemSlot.FunctionNumber
- Win32_SystemSlot.HeightAllowed
- Win32_SystemSlot.InstallDate
- Win32_SystemSlot.LengthAllowed
- Win32_SystemSlot.Manufacturer
- Win32_SystemSlot.MaxDataWidth
- Win32_SystemSlot.Model
- Win32_SystemSlot.Name
- Win32_SystemSlot.Number
- Win32_SystemSlot.OtherIdentifyingInfo
- Win32_SystemSlot.PartNumber
- Win32_SystemSlot.PMESignal
- Win32_SystemSlot.PoweredOn
- Win32_SystemSlot.PurposeDescription
- Win32_SystemSlot.SegmentGroupNumber
- Win32_SystemSlot.SerialNumber
- Win32_SystemSlot.Shared
- Win32_SystemSlot.SKU
- Win32_SystemSlot.SlotDesignation
- Win32_SystemSlot.SpecialPurpose
- Win32_SystemSlot.Status
- Win32_SystemSlot.SupportsHotPlug
- Win32_SystemSlot.Tag
- Win32_SystemSlot.ThermalRating
- Win32_SystemSlot.VccMixedVoltageSupport
- Win32_SystemSlot.Version
- Win32_SystemSlot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e2913aa2d8850aae4fdad8fbca71f216cd848f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153484"
---
# <a name="win32_systemslot-class"></a><span data-ttu-id="d0415-103">\_Clase Win32 SystemSlot</span><span class="sxs-lookup"><span data-stu-id="d0415-103">Win32\_SystemSlot class</span></span>

<span data-ttu-id="d0415-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemSlot de Win32** representa los puntos de conexión físicos, incluidos los puertos, los periféricos y las ranuras de la placa base, y los puntos de conexión de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d0415-104">The **Win32\_SystemSlot** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection points including ports, motherboard slots and peripherals, and proprietary connection points.</span></span>

<span data-ttu-id="d0415-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d0415-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d0415-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d0415-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0415-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0415-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B91-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSlot : CIM_Slot
{
  uint32   BusNumber;
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  uint16   CurrentUsage;
  string   Description;
  uint32   DeviceNumber;
  uint32   FunctionNumber;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PMESignal;
  boolean  PoweredOn;
  string   PurposeDescription;
  uint32   SegmentGroupNumber;
  string   SerialNumber;
  boolean  Shared;
  string   SKU;
  string   SlotDesignation;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a><span data-ttu-id="d0415-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d0415-108">Members</span></span>

<span data-ttu-id="d0415-109">La **clase \_ SystemSlot de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d0415-109">The **Win32\_SystemSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="d0415-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0415-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d0415-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0415-111">Properties</span></span>

<span data-ttu-id="d0415-112">La **clase \_ SystemSlot de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d0415-112">The **Win32\_SystemSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0415-113">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="d0415-113">**BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0415-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-116">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("número de bus de tipo de SMBIOS \| 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="d0415-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Bus Number")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-117">Número de bus de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-117">SMBIOS Bus Number.</span></span>

<span data-ttu-id="d0415-118">Este valor procede del miembro del **número de bus** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-118">This value comes from the **Bus Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d0415-119">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d0415-119">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="d0415-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d0415-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-123">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d0415-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-124">Breve descripción de un objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="d0415-124">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="d0415-125">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-126">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="d0415-126">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0415-129">Cadena de forma libre que describe la configuración del PIN y el uso de la señal de un conector físico.</span><span class="sxs-lookup"><span data-stu-id="d0415-129">Free-form string that describes the pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="d0415-130">Esta propiedad se hereda de [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-130">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-131">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="d0415-131">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-132">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0415-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d0415-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-134">Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo de ranura de tipo SMBIOS 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="d0415-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Type")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-135">Matriz de atributos físicos del conector que esta ranura usa.</span><span class="sxs-lookup"><span data-stu-id="d0415-135">Array of physical attributes of the connector that this slot uses.</span></span>

<span data-ttu-id="d0415-136">Este valor procede del miembro de **tipo de ranura** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-136">This value comes from the **Slot Type** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d0415-137">Esta propiedad se hereda de [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-137">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="d0415-138">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="d0415-138">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0415-139">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d0415-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d0415-140">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d0415-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="d0415-141">**Macho** (2)</span><span class="sxs-lookup"><span data-stu-id="d0415-141">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="d0415-142">**Hembra** (3)</span><span class="sxs-lookup"><span data-stu-id="d0415-142">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="d0415-143">**Blindado** (4)</span><span class="sxs-lookup"><span data-stu-id="d0415-143">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="d0415-144">No **blindado** (5)</span><span class="sxs-lookup"><span data-stu-id="d0415-144">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="d0415-145">**SCSI (A) High-Density (50 pines)** (6)</span><span class="sxs-lookup"><span data-stu-id="d0415-145">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="d0415-146">**SCSI (A) Low-Density (50 Pin)** (7)</span><span class="sxs-lookup"><span data-stu-id="d0415-146">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="d0415-147">**SCSI (P) High-Density (68 pines)** (8)</span><span class="sxs-lookup"><span data-stu-id="d0415-147">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="d0415-148">**SCSI SCA-I (80 pines)** (9)</span><span class="sxs-lookup"><span data-stu-id="d0415-148">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="d0415-149">**SCSI SCA-II (80 pines)** (10)</span><span class="sxs-lookup"><span data-stu-id="d0415-149">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="d0415-150">**Canal de fibra SCSI (DB-9, cobre)** (11)</span><span class="sxs-lookup"><span data-stu-id="d0415-150">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="d0415-151">**Canal de fibra SCSI (fibra)** (12)</span><span class="sxs-lookup"><span data-stu-id="d0415-151">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="d0415-152">**SCSI canal de fibra SCA-II (40 pines)** (13)</span><span class="sxs-lookup"><span data-stu-id="d0415-152">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="d0415-153">**SCSI canal de fibra SCA-II (20 clavijas)** (14)</span><span class="sxs-lookup"><span data-stu-id="d0415-153">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="d0415-154">**SCSI canal de fibra BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="d0415-154">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="d0415-155">**ATA 3-1/2 pulgada (40 PIN)** (16)</span><span class="sxs-lookup"><span data-stu-id="d0415-155">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="d0415-156">**ATA 2-1/2 pulgada (44 PIN)** (17)</span><span class="sxs-lookup"><span data-stu-id="d0415-156">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="d0415-157">**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="d0415-157">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="d0415-158">**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="d0415-158">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="d0415-159">**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="d0415-159">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="d0415-160">**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="d0415-160">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="d0415-161">**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="d0415-161">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="d0415-162">**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="d0415-162">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="d0415-163">**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="d0415-163">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="d0415-164">**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="d0415-164">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="d0415-165">**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="d0415-165">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="d0415-166">**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="d0415-166">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="d0415-167">**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="d0415-167">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="d0415-168">**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="d0415-168">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="d0415-169">**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="d0415-169">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="d0415-170">**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="d0415-170">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="d0415-171">**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="d0415-171">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="d0415-172">**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="d0415-172">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="d0415-173">**UTP categoría 3** (34)</span><span class="sxs-lookup"><span data-stu-id="d0415-173">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="d0415-174">**UTP categoría 4** (35)</span><span class="sxs-lookup"><span data-stu-id="d0415-174">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="d0415-175">**UTP categoría 5** (36)</span><span class="sxs-lookup"><span data-stu-id="d0415-175">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="d0415-176">**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="d0415-176">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="d0415-177">**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="d0415-177">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="d0415-178">**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="d0415-178">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="d0415-179">**MIC de fibra** (40)</span><span class="sxs-lookup"><span data-stu-id="d0415-179">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="d0415-180">**AUI de Apple** (41)</span><span class="sxs-lookup"><span data-stu-id="d0415-180">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="d0415-181">**Apple geoport** (42)</span><span class="sxs-lookup"><span data-stu-id="d0415-181">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="d0415-182">**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="d0415-182">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="d0415-183">**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="d0415-183">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="d0415-184">**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="d0415-184">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="d0415-185">**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="d0415-185">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="d0415-186">**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="d0415-186">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="d0415-187">**PCMCIA tipo I** (48)</span><span class="sxs-lookup"><span data-stu-id="d0415-187">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="d0415-188">**PCMCIA (tipo II** ) (49)</span><span class="sxs-lookup"><span data-stu-id="d0415-188">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="d0415-189">**PCMCIA, tipo III** (50)</span><span class="sxs-lookup"><span data-stu-id="d0415-189">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="d0415-190">**Puerto ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="d0415-190">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="d0415-191">**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="d0415-191">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="d0415-192">**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="d0415-192">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="d0415-193">**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="d0415-193">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="d0415-194">**HIPPI** (55)</span><span class="sxs-lookup"><span data-stu-id="d0415-194">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="d0415-195">**HSSDC (6 clavijas)** (56)</span><span class="sxs-lookup"><span data-stu-id="d0415-195">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="d0415-196">**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="d0415-196">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="d0415-197">**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="d0415-197">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="d0415-198">**Mini DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="d0415-198">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="d0415-199">**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="d0415-199">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="d0415-200">**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="d0415-200">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="d0415-201">**Infrarrojos** (62)</span><span class="sxs-lookup"><span data-stu-id="d0415-201">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="d0415-202">**HP-Hil** (63)</span><span class="sxs-lookup"><span data-stu-id="d0415-202">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="d0415-203">**Access. bus** (64)</span><span class="sxs-lookup"><span data-stu-id="d0415-203">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="d0415-204">**Nubus** (65)</span><span class="sxs-lookup"><span data-stu-id="d0415-204">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="d0415-205">**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="d0415-205">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="d0415-206">**Minicontrolador-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="d0415-206">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="d0415-207">**Mini-Centronics tipo-14** (68)</span><span class="sxs-lookup"><span data-stu-id="d0415-207">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="d0415-208">**Mini-Centronics tipo-20** (69)</span><span class="sxs-lookup"><span data-stu-id="d0415-208">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="d0415-209">**Mini-Centronics tipo-26** (70)</span><span class="sxs-lookup"><span data-stu-id="d0415-209">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="d0415-210">**Mouse de bus** (71)</span><span class="sxs-lookup"><span data-stu-id="d0415-210">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="d0415-211">**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="d0415-211">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="d0415-212">**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="d0415-212">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="d0415-213">**Bus VME** (74)</span><span class="sxs-lookup"><span data-stu-id="d0415-213">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="d0415-214">**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="d0415-214">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="d0415-215">**Propietario** (76)</span><span class="sxs-lookup"><span data-stu-id="d0415-215">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="d0415-216">**Ranura de tarjeta del procesador de propiedad** (77)</span><span class="sxs-lookup"><span data-stu-id="d0415-216">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="d0415-217">**Ranura de tarjeta de memoria de propiedad** (78)</span><span class="sxs-lookup"><span data-stu-id="d0415-217">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="d0415-218">**Ranura de aumento de e/s de propiedad** (79)</span><span class="sxs-lookup"><span data-stu-id="d0415-218">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="d0415-219">**PCI-66** (80)</span><span class="sxs-lookup"><span data-stu-id="d0415-219">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="d0415-220">**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="d0415-220">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="d0415-221">**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="d0415-221">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="d0415-222">**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="d0415-222">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="d0415-223">**PC-98-Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="d0415-223">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="d0415-224">**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="d0415-224">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="d0415-225">**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="d0415-225">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="d0415-226">**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="d0415-226">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="d0415-227">**PCI-X** (88)</span><span class="sxs-lookup"><span data-stu-id="d0415-227">**PCI-X** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="d0415-228">**SBus IEEE 1396-1993 32 bit** (89)</span><span class="sxs-lookup"><span data-stu-id="d0415-228">**Sbus IEEE 1396-1993 32 bit** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="d0415-229">**SBus IEEE 1396-1993 64 bit** (90)</span><span class="sxs-lookup"><span data-stu-id="d0415-229">**Sbus IEEE 1396-1993 64 bit** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="d0415-230">**MCA** (91)</span><span class="sxs-lookup"><span data-stu-id="d0415-230">**MCA** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="d0415-231">**Gio** (92)</span><span class="sxs-lookup"><span data-stu-id="d0415-231">**GIO** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="d0415-232">**Xio** (93)</span><span class="sxs-lookup"><span data-stu-id="d0415-232">**XIO** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="d0415-233">**Hio** (94)</span><span class="sxs-lookup"><span data-stu-id="d0415-233">**HIO** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="d0415-234">**NGIO** (95)</span><span class="sxs-lookup"><span data-stu-id="d0415-234">**NGIO** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="d0415-235">**PMC** (96)</span><span class="sxs-lookup"><span data-stu-id="d0415-235">**PMC** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="d0415-236">**E/s futura** (97)</span><span class="sxs-lookup"><span data-stu-id="d0415-236">**Future I/O** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="d0415-237">**InfiniBand** (98)</span><span class="sxs-lookup"><span data-stu-id="d0415-237">**InfiniBand** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP8X"></span><span id="agp8x"></span>

<span data-ttu-id="d0415-238">**AGP8x** (99)</span><span class="sxs-lookup"><span data-stu-id="d0415-238">**AGP8X** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-E"></span><span id="pci-e"></span>

<span data-ttu-id="d0415-239">**PCI-E** (100)</span><span class="sxs-lookup"><span data-stu-id="d0415-239">**PCI-E** (100)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0415-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d0415-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-241">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-243">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d0415-243">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d0415-244">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="d0415-244">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d0415-245">Cuando se usa con las otras propiedades clave de una clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="d0415-245">When used with the other key properties of a class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="d0415-246">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-246">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-247">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="d0415-247">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-248">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0415-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-250">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| uso actual del tipo de SMBIOS 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="d0415-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Current Usage")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-251">Estado de uso de la ranura del sistema.</span><span class="sxs-lookup"><span data-stu-id="d0415-251">Status of system slot use.</span></span>

<span data-ttu-id="d0415-252">Este valor procede del miembro de **uso actual** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-252">This value comes from the **Current Usage** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d0415-253">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="d0415-253">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d0415-254">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="d0415-254">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d0415-255">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d0415-255">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0415-256">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d0415-256">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="d0415-257">**Disponible** (3)</span><span class="sxs-lookup"><span data-stu-id="d0415-257">**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_use"></span><span id="in_use"></span><span id="IN_USE"></span>

<span data-ttu-id="d0415-258">**En uso** (4)</span><span class="sxs-lookup"><span data-stu-id="d0415-258">**In use** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0415-259">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0415-259">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-260">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-262">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="d0415-262">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-263">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d0415-263">Description of the object.</span></span>

<span data-ttu-id="d0415-264">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-264">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-265">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="d0415-265">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-266">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0415-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-268">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| número de dispositivo de tipo SMBIOS 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="d0415-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Device Number")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-269">Número de dispositivo de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-269">SMBIOS Device Number.</span></span>

<span data-ttu-id="d0415-270">Este valor procede del miembro **número de dispositivo/función** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-270">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d0415-271">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d0415-271">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="d0415-272">**FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="d0415-272">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-273">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0415-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-275">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("número de función de tipo de SMBIOS \| 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="d0415-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Function Number")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-276">Número de función de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-276">SMBIOS Function Number.</span></span>

<span data-ttu-id="d0415-277">Este valor procede del miembro **número de dispositivo/función** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-277">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d0415-278">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d0415-278">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="d0415-279">**HeightAllowed**</span><span class="sxs-lookup"><span data-stu-id="d0415-279">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-280">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="d0415-280">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-282">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="d0415-282">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-283">Alto máximo de una tarjeta de adaptador que se puede insertar en la ranura, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="d0415-283">Maximum height of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="d0415-284">Esta propiedad se hereda de [**la \_ ranura CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-284">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-285">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d0415-285">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-286">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d0415-286">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-288">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="d0415-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-289">Fecha y hora de instalación del objeto.</span><span class="sxs-lookup"><span data-stu-id="d0415-289">Date and time the object is installed.</span></span> <span data-ttu-id="d0415-290">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="d0415-290">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d0415-291">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-292">**LengthAllowed**</span><span class="sxs-lookup"><span data-stu-id="d0415-292">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-293">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="d0415-293">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-295">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="d0415-295">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-296">Longitud máxima de una tarjeta adaptadora que se puede insertar en la ranura, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="d0415-296">Maximum length of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="d0415-297">Esta propiedad se hereda de [**la \_ ranura CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-297">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-298">**Le**</span><span class="sxs-lookup"><span data-stu-id="d0415-298">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-299">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-301">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d0415-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d0415-302">Nombre de la organización que produce el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="d0415-302">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="d0415-303">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-303">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-304">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="d0415-304">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-305">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0415-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-307">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Ranura del sistema DMTF \| 004,3 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="d0415-307">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-308">Ancho de bus máximo de las tarjetas adaptador que se pueden insertar en esta ranura, en bits.</span><span class="sxs-lookup"><span data-stu-id="d0415-308">Maximum bus width of adapter cards that can be inserted into this slot—in bits.</span></span> <span data-ttu-id="d0415-309">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d0415-309">This can be one of the following values.</span></span>

<span data-ttu-id="d0415-310">Este valor procede del miembro de **ancho de bus de datos de ranura** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-310">This value comes from the **Slot Data Bus Width** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d0415-311">Esta propiedad se hereda de [**la \_ ranura CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-311">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="d0415-312">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="d0415-312">The possible values are.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="d0415-313"><span id="8"></span>**8** (0)</span><span class="sxs-lookup"><span data-stu-id="d0415-313"><span id="8"></span>**8** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d0415-314">Ancho de datos máximo (bits): 8</span><span class="sxs-lookup"><span data-stu-id="d0415-314">Maximum data width (bits): 8</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="d0415-315"><span id="16"></span>**16** (1)</span><span class="sxs-lookup"><span data-stu-id="d0415-315"><span id="16"></span>**16** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d0415-316">Ancho de datos máximo (bits): 16</span><span class="sxs-lookup"><span data-stu-id="d0415-316">Maximum data width (bits): 16</span></span>

</dd> <dt>

<span id="32"></span>

<span data-ttu-id="d0415-317"><span id="32"></span>**32** (2)</span><span class="sxs-lookup"><span data-stu-id="d0415-317"><span id="32"></span>**32** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d0415-318">Ancho de datos máximo (bits): 32</span><span class="sxs-lookup"><span data-stu-id="d0415-318">Maximum data width (bits): 32</span></span>

</dd> <dt>

<span id="64"></span>

<span data-ttu-id="d0415-319"><span id="64"></span>**64** (3)</span><span class="sxs-lookup"><span data-stu-id="d0415-319"><span id="64"></span>**64** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d0415-320">Ancho de datos máximo (bits): 64</span><span class="sxs-lookup"><span data-stu-id="d0415-320">Maximum data width (bits): 64</span></span>

</dd> <dt>

<span id="128"></span>

<span data-ttu-id="d0415-321"><span id="128"></span>**128** (4)</span><span class="sxs-lookup"><span data-stu-id="d0415-321"><span id="128"></span>**128** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d0415-322">Ancho de datos máximo (bits): 128</span><span class="sxs-lookup"><span data-stu-id="d0415-322">Maximum data width (bits): 128</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d0415-323">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="d0415-323">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-326">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d0415-326">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d0415-327">Nombre del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="d0415-327">Name for the physical element.</span></span>

<span data-ttu-id="d0415-328">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-328">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-329">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d0415-329">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-330">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-332">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d0415-332">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-333">Etiqueta del objeto.</span><span class="sxs-lookup"><span data-stu-id="d0415-333">Label for the object.</span></span> <span data-ttu-id="d0415-334">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="d0415-334">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d0415-335">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-336">**Number**</span><span class="sxs-lookup"><span data-stu-id="d0415-336">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-337">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0415-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0415-339">Número de ranura física que se puede utilizar como índice en una tabla de ranuras del sistema, tanto si dicha ranura está vacía físicamente como si no.</span><span class="sxs-lookup"><span data-stu-id="d0415-339">Physical slot number that can be used as an index into a system slot table, whether or not that slot is physically empty.</span></span>

<span data-ttu-id="d0415-340">Este valor procede del miembro de ID. de **ranura** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-340">This value comes from the **Slot ID** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d0415-341">Esta propiedad se hereda de [**la \_ ranura CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-341">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d0415-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-343">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0415-345">Datos adicionales (es decir, más que la información de la etiqueta de recurso), que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="d0415-345">Additional data (that is, more than the asset tag information), that can be used to identify a physical element.</span></span> <span data-ttu-id="d0415-346">Un ejemplo son los datos de código de barras asociados a un elemento que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="d0415-346">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="d0415-347">Tenga en cuenta que si solo hay datos de código de barras disponibles y es único o se puede usar como una clave de elemento, esta propiedad es **null** y los datos de código de barras se usan como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="d0415-347">Note that if only bar code data is available, and it is unique or can be used as an element key, this property is **NULL**, and the bar code data is used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="d0415-348">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-348">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-349">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="d0415-349">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-350">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-352">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d0415-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d0415-353">Número de pieza que el productor o fabricante asigna al elemento físico.</span><span class="sxs-lookup"><span data-stu-id="d0415-353">Part number that the producer or manufacturer assigns to the physical element.</span></span>

<span data-ttu-id="d0415-354">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-355">**PMESignal**</span><span class="sxs-lookup"><span data-stu-id="d0415-355">**PMESignal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-356">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d0415-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-358">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("características de la \| ranura de tipo SMBIOS 9 \| 2")</span><span class="sxs-lookup"><span data-stu-id="d0415-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 2")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-359">Si **es true**, esta ranura admite la señal de administración de energía de bus PCI habilitada (PME).</span><span class="sxs-lookup"><span data-stu-id="d0415-359">If **TRUE**, the PCI bus Power Management Enabled (PME) signal is supported by this slot.</span></span>

<span data-ttu-id="d0415-360">Este valor procede del miembro **ranura 2** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-360">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="d0415-361">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="d0415-361">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-362">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d0415-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0415-364">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="d0415-364">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="d0415-365">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-365">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-366">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="d0415-366">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-369">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ espacio CIM**](cim-slot.md).**SpecialPurpose**")</span><span class="sxs-lookup"><span data-stu-id="d0415-369">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-370">Cadena de forma libre que describe cómo esta ranura es físicamente única y puede contener tipos especiales de hardware.</span><span class="sxs-lookup"><span data-stu-id="d0415-370">Free-form string that describes how this slot is physically unique and may hold special types of hardware.</span></span> <span data-ttu-id="d0415-371">Esta propiedad solo tiene significado cuando la propiedad **SpecialPurpose** correspondiente es **true**.</span><span class="sxs-lookup"><span data-stu-id="d0415-371">This property only has meaning when the corresponding property **SpecialPurpose** is **TRUE**.</span></span>

<span data-ttu-id="d0415-372">Esta propiedad se hereda de [**la \_ ranura CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-372">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-373">**SegmentGroupNumber**</span><span class="sxs-lookup"><span data-stu-id="d0415-373">**SegmentGroupNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-374">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0415-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-376">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| número de grupo de segmentos de tipo SMBIOS 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="d0415-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Segment Group Number")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-377">Número de grupo de segmentos de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-377">SMBIOS Segment Group Number.</span></span>

<span data-ttu-id="d0415-378">Este valor procede del miembro del **número de grupo de segmentos** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-378">This value comes from the **Segment Group Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d0415-379">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d0415-379">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="d0415-380">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d0415-380">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-381">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-383">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d0415-383">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d0415-384">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="d0415-384">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="d0415-385">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-385">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-386">**Compartido**</span><span class="sxs-lookup"><span data-stu-id="d0415-386">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-387">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d0415-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-389">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("características de la \| ranura de tipo SMBIOS 9 \| 1")</span><span class="sxs-lookup"><span data-stu-id="d0415-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 1")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-390">Si **es true**, dos o más ranuras comparten una ubicación en la placa base, como una ranura compartida PCI/EISA.</span><span class="sxs-lookup"><span data-stu-id="d0415-390">If **TRUE**, two or more slots share a location on the baseboard, such as a PCI/EISA shared slot.</span></span>

<span data-ttu-id="d0415-391">Este valor procede del miembro de la **ranura características 1** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-391">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="d0415-392">**SKU**</span><span class="sxs-lookup"><span data-stu-id="d0415-392">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-393">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-395">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d0415-395">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d0415-396">Número de unidad de almacenamiento para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="d0415-396">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="d0415-397">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-397">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-398">**SlotDesignation**</span><span class="sxs-lookup"><span data-stu-id="d0415-398">**SlotDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-399">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-401">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("designación de la \| ranura de tipo SMBIOS 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="d0415-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Designation")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-402">Cadena de SMBIOS que identifica la designación de la ranura del sistema de la ranura en la placa base.</span><span class="sxs-lookup"><span data-stu-id="d0415-402">SMBIOS string that identifies the system slot designation of the slot on the motherboard.</span></span>

<span data-ttu-id="d0415-403">Ejemplo: "PCI-1"</span><span class="sxs-lookup"><span data-stu-id="d0415-403">Example: "PCI-1"</span></span>

<span data-ttu-id="d0415-404">Este valor procede del miembro de **designación de ranura** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-404">This value comes from the **Slot Designation** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="d0415-405">**SpecialPurpose**</span><span class="sxs-lookup"><span data-stu-id="d0415-405">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-406">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d0415-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-408">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ espacio CIM**](cim-slot.md).**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="d0415-408">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-409">Si es **true**, esta ranura es físicamente única y puede contener tipos especiales de hardware, como una ranura de procesador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="d0415-409">If **TRUE**, this slot is physically unique and may hold special types of hardware, such as a graphics processor slot.</span></span> <span data-ttu-id="d0415-410">Si **es true**, **PurposeDescription** debe especificar la naturaleza de la unicidad o el propósito de la ranura.</span><span class="sxs-lookup"><span data-stu-id="d0415-410">If **TRUE**, then **PurposeDescription** should specify the nature of the uniqueness or purpose of the slot.</span></span>

<span data-ttu-id="d0415-411">Esta propiedad se hereda de [**la \_ ranura CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-411">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-412">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d0415-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-413">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-414">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-415">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="d0415-415">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-416">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d0415-416">Current status of the object.</span></span> <span data-ttu-id="d0415-417">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="d0415-417">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d0415-418">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d0415-418">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d0415-419">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="d0415-419">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d0415-420">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d0415-420">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d0415-421">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="d0415-421">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d0415-422">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d0415-423">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="d0415-423">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d0415-424">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="d0415-424">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d0415-425">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="d0415-425">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d0415-426">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="d0415-426">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0415-427">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="d0415-427">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d0415-428">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="d0415-428">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d0415-429">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="d0415-429">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d0415-430">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="d0415-430">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d0415-431">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="d0415-431">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d0415-432">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="d0415-432">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d0415-433">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="d0415-433">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d0415-434">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="d0415-434">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d0415-435">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="d0415-435">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0415-436">**SupportsHotPlug**</span><span class="sxs-lookup"><span data-stu-id="d0415-436">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-437">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d0415-437">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-438">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0415-439">Si **es true**, la ranura admite la conexión en caliente de tarjetas adaptadoras.</span><span class="sxs-lookup"><span data-stu-id="d0415-439">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

<span data-ttu-id="d0415-440">Este valor procede del miembro **ranura 2** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-440">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d0415-441">Esta propiedad se hereda de [**la \_ ranura CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-441">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-442">**Tag**</span><span class="sxs-lookup"><span data-stu-id="d0415-442">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-443">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-445">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**invalidación**](../wmisdk/standard-qualifiers.md) ("etiqueta"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d0415-445">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-446">Ranura del sistema representada por una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="d0415-446">System slot represented by an instance of this class.</span></span>

<span data-ttu-id="d0415-447">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="d0415-448">Ejemplo: "ranura del sistema 1"</span><span class="sxs-lookup"><span data-stu-id="d0415-448">Example: "System Slot 1"</span></span>

</dd> <dt>

<span data-ttu-id="d0415-449">**ThermalRating**</span><span class="sxs-lookup"><span data-stu-id="d0415-449">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-450">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0415-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-451">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-452">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Ranura del sistema DMTF \| 004,11 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivatios ")</span><span class="sxs-lookup"><span data-stu-id="d0415-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-453">Disipación térmica máxima de la ranura en milivatios.</span><span class="sxs-lookup"><span data-stu-id="d0415-453">Maximum thermal dissipation of the slot in milliwatts.</span></span>

<span data-ttu-id="d0415-454">Esta propiedad se hereda de [**la \_ ranura CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-454">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-455">**VccMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="d0415-455">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-456">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0415-456">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d0415-457">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-458">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Ranura del sistema DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="d0415-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-459">Matriz de enteros enumerados que indica el voltaje VCC compatible con esta ranura.</span><span class="sxs-lookup"><span data-stu-id="d0415-459">Array of enumerated integers indicating the Vcc voltage supported by this slot.</span></span>

<span data-ttu-id="d0415-460">Este valor procede del miembro de la **ranura características 1** de la estructura **ranuras del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0415-460">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d0415-461">Esta propiedad se hereda de [**la \_ ranura CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-461">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="d0415-462">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="d0415-462">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0415-463">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d0415-463">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d0415-464">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d0415-464">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="d0415-465">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="d0415-465">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="d0415-466">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="d0415-466">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0415-467">**Versión**</span><span class="sxs-lookup"><span data-stu-id="d0415-467">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-468">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d0415-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0415-469">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-470">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d0415-470">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d0415-471">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="d0415-471">Version of the physical element.</span></span>

<span data-ttu-id="d0415-472">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-472">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0415-473">**VppMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="d0415-473">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0415-474">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0415-474">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d0415-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0415-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0415-476">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Ranura del sistema DMTF \| 004,10 ")</span><span class="sxs-lookup"><span data-stu-id="d0415-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="d0415-477">Matriz de enteros enumerados que indican el voltaje Vpp compatible con esta ranura.</span><span class="sxs-lookup"><span data-stu-id="d0415-477">Array of enumerated integers indicating the Vpp voltage supported by this slot.</span></span>

<span data-ttu-id="d0415-478">Esta propiedad se hereda de [**la \_ ranura CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-478">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="d0415-479">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="d0415-479">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0415-480">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d0415-480">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d0415-481">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d0415-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="d0415-482">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="d0415-482">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="d0415-483">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="d0415-483">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="d0415-484">**12V** (4)</span><span class="sxs-lookup"><span data-stu-id="d0415-484">**12V** (4)</span></span>


<span data-ttu-id="d0415-485"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d0415-485"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d0415-486">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0415-486">Remarks</span></span>

<span data-ttu-id="d0415-487">La clase **Win32 \_ SystemSlot** se deriva de [**la \_ ranura CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="d0415-487">The **Win32\_SystemSlot** class is derived from [**CIM\_Slot**](cim-slot.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0415-488">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0415-488">Requirements</span></span>



| <span data-ttu-id="d0415-489">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0415-489">Requirement</span></span> | <span data-ttu-id="d0415-490">Value</span><span class="sxs-lookup"><span data-stu-id="d0415-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0415-491">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0415-491">Minimum supported client</span></span><br/> | <span data-ttu-id="d0415-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0415-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0415-493">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0415-493">Minimum supported server</span></span><br/> | <span data-ttu-id="d0415-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0415-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0415-495">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d0415-495">Namespace</span></span><br/>                | <span data-ttu-id="d0415-496">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d0415-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d0415-497">MOF</span><span class="sxs-lookup"><span data-stu-id="d0415-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0415-498"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0415-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0415-499">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0415-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0415-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0415-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0415-501">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0415-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0415-502">**\_Ranura CIM**</span><span class="sxs-lookup"><span data-stu-id="d0415-502">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dt>

[<span data-ttu-id="d0415-503">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="d0415-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
