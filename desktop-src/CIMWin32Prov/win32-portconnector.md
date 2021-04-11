---
description: La \_ clase WMI PortConnector de Win32 representa puertos de conexión físicos, como los machos de DB-25 pin, Centronics o PS/2.
ms.assetid: 85788d1d-0641-4dba-b4ae-a84eb6c4992a
ms.tgt_platform: multiple
title: Win32_PortConnector (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortConnector
- Win32_PortConnector.Caption
- Win32_PortConnector.ConnectorPinout
- Win32_PortConnector.ConnectorType
- Win32_PortConnector.CreationClassName
- Win32_PortConnector.Description
- Win32_PortConnector.ExternalReferenceDesignator
- Win32_PortConnector.InstallDate
- Win32_PortConnector.InternalReferenceDesignator
- Win32_PortConnector.Manufacturer
- Win32_PortConnector.Model
- Win32_PortConnector.Name
- Win32_PortConnector.OtherIdentifyingInfo
- Win32_PortConnector.PartNumber
- Win32_PortConnector.PortType
- Win32_PortConnector.PoweredOn
- Win32_PortConnector.SerialNumber
- Win32_PortConnector.SKU
- Win32_PortConnector.Status
- Win32_PortConnector.Tag
- Win32_PortConnector.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dcf9eea51d3a65ad07879cca3e47ae79bde92d53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274855"
---
# <a name="win32_portconnector-class"></a><span data-ttu-id="7eb17-103">\_Clase Win32 PortConnector</span><span class="sxs-lookup"><span data-stu-id="7eb17-103">Win32\_PortConnector class</span></span>

<span data-ttu-id="7eb17-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PortConnector de Win32** representa puertos de conexión físicos, como los machos de DB-25 pin, Centronics o PS/2.</span><span class="sxs-lookup"><span data-stu-id="7eb17-104">The **Win32\_PortConnector** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection ports, such as DB-25 pin male, Centronics, or PS/2.</span></span>

<span data-ttu-id="7eb17-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7eb17-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7eb17-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7eb17-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb17-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7eb17-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B92-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortConnector : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  string   ExternalReferenceDesignator;
  datetime InstallDate;
  string   InternalReferenceDesignator;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint16   PortType;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="7eb17-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7eb17-108">Members</span></span>

<span data-ttu-id="7eb17-109">La **clase \_ PortConnector de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7eb17-109">The **Win32\_PortConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="7eb17-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7eb17-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7eb17-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7eb17-111">Properties</span></span>

<span data-ttu-id="7eb17-112">La **clase \_ PortConnector de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7eb17-112">The **Win32\_PortConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7eb17-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7eb17-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-116">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7eb17-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-117">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="7eb17-117">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="7eb17-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-119">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="7eb17-119">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-122">Configuración de PIN y uso de señal de un conector físico.</span><span class="sxs-lookup"><span data-stu-id="7eb17-122">Pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="7eb17-123">Esta propiedad se hereda de [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-123">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-124">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="7eb17-124">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-125">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eb17-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-127">Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo de \| conector interno/externo de tipo SMBIOS 8")</span><span class="sxs-lookup"><span data-stu-id="7eb17-127">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal/External Connector Type")</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-128">Matriz de atributos físicos del conector que utiliza este puerto.</span><span class="sxs-lookup"><span data-stu-id="7eb17-128">Array of physical attributes of the connector used by this port.</span></span>

<span data-ttu-id="7eb17-129">Esta propiedad se hereda de [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-129">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span> <span data-ttu-id="7eb17-130">En la lista siguiente se enumeran los valores.</span><span class="sxs-lookup"><span data-stu-id="7eb17-130">The following list lists the values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7eb17-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7eb17-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7eb17-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7eb17-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="7eb17-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Macho** (2)</span><span class="sxs-lookup"><span data-stu-id="7eb17-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="7eb17-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Hembra** (3)</span><span class="sxs-lookup"><span data-stu-id="7eb17-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="7eb17-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Blindado** (4)</span><span class="sxs-lookup"><span data-stu-id="7eb17-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="7eb17-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>No **blindado** (5)</span><span class="sxs-lookup"><span data-stu-id="7eb17-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="7eb17-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 pines)** (6)</span><span class="sxs-lookup"><span data-stu-id="7eb17-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="7eb17-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 Pin)** (7)</span><span class="sxs-lookup"><span data-stu-id="7eb17-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="7eb17-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 pines)** (8)</span><span class="sxs-lookup"><span data-stu-id="7eb17-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="7eb17-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 pines)** (9)</span><span class="sxs-lookup"><span data-stu-id="7eb17-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="7eb17-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 pines)** (10)</span><span class="sxs-lookup"><span data-stu-id="7eb17-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="7eb17-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**Canal de fibra SCSI (DB-9, cobre)** (11)</span><span class="sxs-lookup"><span data-stu-id="7eb17-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="7eb17-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**Canal de fibra SCSI (fibra)** (12)</span><span class="sxs-lookup"><span data-stu-id="7eb17-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="7eb17-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI canal de fibra SCA-II (40 pines)** (13)</span><span class="sxs-lookup"><span data-stu-id="7eb17-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="7eb17-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI canal de fibra SCA-II (20 clavijas)** (14)</span><span class="sxs-lookup"><span data-stu-id="7eb17-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="7eb17-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI canal de fibra BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="7eb17-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="7eb17-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 pulgada (40 PIN)** (16)</span><span class="sxs-lookup"><span data-stu-id="7eb17-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="7eb17-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 pulgada (44 PIN)** (17)</span><span class="sxs-lookup"><span data-stu-id="7eb17-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="7eb17-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="7eb17-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="7eb17-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="7eb17-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="7eb17-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="7eb17-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="7eb17-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="7eb17-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="7eb17-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="7eb17-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="7eb17-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="7eb17-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="7eb17-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="7eb17-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="7eb17-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="7eb17-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="7eb17-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="7eb17-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="7eb17-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="7eb17-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="7eb17-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="7eb17-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="7eb17-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="7eb17-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="7eb17-161"><span id="v.35"></span>**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="7eb17-161"><span id="v.35"></span>**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="7eb17-162"><span id="x.21"></span>**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="7eb17-162"><span id="x.21"></span>**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="7eb17-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="7eb17-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="7eb17-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="7eb17-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="7eb17-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP categoría 3** (34)</span><span class="sxs-lookup"><span data-stu-id="7eb17-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="7eb17-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP categoría 4** (35)</span><span class="sxs-lookup"><span data-stu-id="7eb17-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="7eb17-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP categoría 5** (36)</span><span class="sxs-lookup"><span data-stu-id="7eb17-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="7eb17-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="7eb17-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="7eb17-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="7eb17-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="7eb17-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="7eb17-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="7eb17-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**MIC de fibra** (40)</span><span class="sxs-lookup"><span data-stu-id="7eb17-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="7eb17-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**AUI de Apple** (41)</span><span class="sxs-lookup"><span data-stu-id="7eb17-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="7eb17-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple geoport** (42)</span><span class="sxs-lookup"><span data-stu-id="7eb17-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="7eb17-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="7eb17-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="7eb17-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="7eb17-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="7eb17-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="7eb17-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="7eb17-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="7eb17-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="7eb17-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="7eb17-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="7eb17-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**PCMCIA tipo I** (48)</span><span class="sxs-lookup"><span data-stu-id="7eb17-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="7eb17-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA (tipo II** ) (49)</span><span class="sxs-lookup"><span data-stu-id="7eb17-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="7eb17-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA, tipo III** (50)</span><span class="sxs-lookup"><span data-stu-id="7eb17-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="7eb17-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**Puerto ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="7eb17-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="7eb17-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="7eb17-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="7eb17-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="7eb17-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="7eb17-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="7eb17-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="7eb17-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)</span><span class="sxs-lookup"><span data-stu-id="7eb17-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="7eb17-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 clavijas)** (56)</span><span class="sxs-lookup"><span data-stu-id="7eb17-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="7eb17-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="7eb17-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="7eb17-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="7eb17-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="7eb17-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="7eb17-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="7eb17-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="7eb17-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="7eb17-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="7eb17-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="7eb17-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarrojos** (62)</span><span class="sxs-lookup"><span data-stu-id="7eb17-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="7eb17-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-Hil** (63)</span><span class="sxs-lookup"><span data-stu-id="7eb17-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="7eb17-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access. bus** (64)</span><span class="sxs-lookup"><span data-stu-id="7eb17-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="7eb17-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**Nubus** (65)</span><span class="sxs-lookup"><span data-stu-id="7eb17-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="7eb17-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="7eb17-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="7eb17-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Minicontrolador-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="7eb17-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="7eb17-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Mini-Centronics tipo-14** (68)</span><span class="sxs-lookup"><span data-stu-id="7eb17-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="7eb17-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Mini-Centronics tipo-20** (69)</span><span class="sxs-lookup"><span data-stu-id="7eb17-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="7eb17-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Mini-Centronics tipo-26** (70)</span><span class="sxs-lookup"><span data-stu-id="7eb17-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="7eb17-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Mouse de bus** (71)</span><span class="sxs-lookup"><span data-stu-id="7eb17-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="7eb17-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="7eb17-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="7eb17-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="7eb17-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="7eb17-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**Bus VME** (74)</span><span class="sxs-lookup"><span data-stu-id="7eb17-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="7eb17-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="7eb17-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="7eb17-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Propietario** (76)</span><span class="sxs-lookup"><span data-stu-id="7eb17-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="7eb17-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Ranura de tarjeta del procesador de propiedad** (77)</span><span class="sxs-lookup"><span data-stu-id="7eb17-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="7eb17-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Ranura de tarjeta de memoria de propiedad** (78)</span><span class="sxs-lookup"><span data-stu-id="7eb17-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="7eb17-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Ranura de aumento de e/s de propiedad** (79)</span><span class="sxs-lookup"><span data-stu-id="7eb17-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="7eb17-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66** (80)</span><span class="sxs-lookup"><span data-stu-id="7eb17-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="7eb17-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="7eb17-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="7eb17-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="7eb17-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="7eb17-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="7eb17-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>

<span data-ttu-id="7eb17-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="7eb17-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span></span>


</dt> <dd>

<span data-ttu-id="7eb17-216">PC-98-Hireso</span><span class="sxs-lookup"><span data-stu-id="7eb17-216">PC-98-Hireso</span></span>

</dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="7eb17-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="7eb17-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="7eb17-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="7eb17-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="7eb17-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="7eb17-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="7eb17-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Miniconector (88** )</span><span class="sxs-lookup"><span data-stu-id="7eb17-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-Jack** (88)</span></span>


</dt> <dd>

<span data-ttu-id="7eb17-221">SCSI SSA</span><span class="sxs-lookup"><span data-stu-id="7eb17-221">SSA SCSI</span></span>

</dd> <dt>

<span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>

<span data-ttu-id="7eb17-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**Disquete en la placa** (89)</span><span class="sxs-lookup"><span data-stu-id="7eb17-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**On Board Floppy** (89)</span></span>


</dt> <dd>

<span data-ttu-id="7eb17-223">Circular</span><span class="sxs-lookup"><span data-stu-id="7eb17-223">Circular</span></span>

</dd> <dt>

<span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>

<span data-ttu-id="7eb17-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**8 patillas en línea dual (corte de patilla 10)** (90)</span><span class="sxs-lookup"><span data-stu-id="7eb17-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9 Pin Dual Inline (pin 10 cut)** (90)</span></span>


</dt> <dd>

<span data-ttu-id="7eb17-225">Conector del IDE de la placa</span><span class="sxs-lookup"><span data-stu-id="7eb17-225">On Board IDE Connector</span></span>

</dd> <dt>

<span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>

<span data-ttu-id="7eb17-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**inline de 25 pines dual (corte 26)** (91)</span><span class="sxs-lookup"><span data-stu-id="7eb17-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 Pin Dual Inline (pin 26 cut)** (91)</span></span>


</dt> <dd>

<span data-ttu-id="7eb17-227">Conector de disquete incorporado</span><span class="sxs-lookup"><span data-stu-id="7eb17-227">On Board Floppy Connector</span></span>

</dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="7eb17-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**PIN dual de 50 en línea** (92)</span><span class="sxs-lookup"><span data-stu-id="7eb17-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50 Pin Dual Inline** (92)</span></span>


</dt> <dd>

<span data-ttu-id="7eb17-229">8 pines dual insertado</span><span class="sxs-lookup"><span data-stu-id="7eb17-229">9 Pin Dual Inline</span></span>

</dd> <dt>

<span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>

<span data-ttu-id="7eb17-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**PIN dual de 68 en línea** (93)</span><span class="sxs-lookup"><span data-stu-id="7eb17-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68 Pin Dual Inline** (93)</span></span>


</dt> <dd>

<span data-ttu-id="7eb17-231">25 patillas en línea dual</span><span class="sxs-lookup"><span data-stu-id="7eb17-231">25 Pin Dual Inline</span></span>

</dd> <dt>

<span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>

<span data-ttu-id="7eb17-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**Entrada de sonido en el panel de CD-ROM** (94)</span><span class="sxs-lookup"><span data-stu-id="7eb17-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**On Board Sound Input from CD-ROM** (94)</span></span>


</dt> <dd>

<span data-ttu-id="7eb17-233">PIN dual de 50 en línea</span><span class="sxs-lookup"><span data-stu-id="7eb17-233">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-234">95</span><span class="sxs-lookup"><span data-stu-id="7eb17-234">95</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-235">PIN dual de 68 en línea</span><span class="sxs-lookup"><span data-stu-id="7eb17-235">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-236">96</span><span class="sxs-lookup"><span data-stu-id="7eb17-236">96</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-237">Conector de sonido de la placa</span><span class="sxs-lookup"><span data-stu-id="7eb17-237">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-238">97</span><span class="sxs-lookup"><span data-stu-id="7eb17-238">97</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-239">Mini-Jack</span><span class="sxs-lookup"><span data-stu-id="7eb17-239">Mini-Jack</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-240">98</span><span class="sxs-lookup"><span data-stu-id="7eb17-240">98</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-241">PCI-X</span><span class="sxs-lookup"><span data-stu-id="7eb17-241">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-242">99</span><span class="sxs-lookup"><span data-stu-id="7eb17-242">99</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-243">SBus IEEE 1396-1993 32 bit</span><span class="sxs-lookup"><span data-stu-id="7eb17-243">Sbus IEEE 1396-1993 32 Bit</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-244">100</span><span class="sxs-lookup"><span data-stu-id="7eb17-244">100</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-245">SBus IEEE 1396-1993 64 bit</span><span class="sxs-lookup"><span data-stu-id="7eb17-245">Sbus IEEE 1396-1993 64 Bit</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-246">101</span><span class="sxs-lookup"><span data-stu-id="7eb17-246">101</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-247">MCA</span><span class="sxs-lookup"><span data-stu-id="7eb17-247">MCA</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-248">102</span><span class="sxs-lookup"><span data-stu-id="7eb17-248">102</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-249">GIO</span><span class="sxs-lookup"><span data-stu-id="7eb17-249">GIO</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-250">103</span><span class="sxs-lookup"><span data-stu-id="7eb17-250">103</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-251">XIO</span><span class="sxs-lookup"><span data-stu-id="7eb17-251">XIO</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-252">104</span><span class="sxs-lookup"><span data-stu-id="7eb17-252">104</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-253">HIO</span><span class="sxs-lookup"><span data-stu-id="7eb17-253">HIO</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-254">105</span><span class="sxs-lookup"><span data-stu-id="7eb17-254">105</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-255">NGIO</span><span class="sxs-lookup"><span data-stu-id="7eb17-255">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-256">106</span><span class="sxs-lookup"><span data-stu-id="7eb17-256">106</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-257">PMC</span><span class="sxs-lookup"><span data-stu-id="7eb17-257">PMC</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-258">107</span><span class="sxs-lookup"><span data-stu-id="7eb17-258">107</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-259">MTRJ</span><span class="sxs-lookup"><span data-stu-id="7eb17-259">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-260">108</span><span class="sxs-lookup"><span data-stu-id="7eb17-260">108</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-261">VF: 45</span><span class="sxs-lookup"><span data-stu-id="7eb17-261">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-262">109</span><span class="sxs-lookup"><span data-stu-id="7eb17-262">109</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-263">E/s futura</span><span class="sxs-lookup"><span data-stu-id="7eb17-263">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-264">110</span><span class="sxs-lookup"><span data-stu-id="7eb17-264">110</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-265">SC</span><span class="sxs-lookup"><span data-stu-id="7eb17-265">SC</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-266">111</span><span class="sxs-lookup"><span data-stu-id="7eb17-266">111</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-267">SG</span><span class="sxs-lookup"><span data-stu-id="7eb17-267">SG</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-268">112</span><span class="sxs-lookup"><span data-stu-id="7eb17-268">112</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-269">Eléctricos</span><span class="sxs-lookup"><span data-stu-id="7eb17-269">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-270">113</span><span class="sxs-lookup"><span data-stu-id="7eb17-270">113</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-271">Trayecto</span><span class="sxs-lookup"><span data-stu-id="7eb17-271">Optical</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-272">114</span><span class="sxs-lookup"><span data-stu-id="7eb17-272">114</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-273">Cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="7eb17-273">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-274">115</span><span class="sxs-lookup"><span data-stu-id="7eb17-274">115</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-275">GLM</span><span class="sxs-lookup"><span data-stu-id="7eb17-275">GLM</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-276">116</span><span class="sxs-lookup"><span data-stu-id="7eb17-276">116</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-277">1x9</span><span class="sxs-lookup"><span data-stu-id="7eb17-277">1x9</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-278">117</span><span class="sxs-lookup"><span data-stu-id="7eb17-278">117</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-279">SG reducidos</span><span class="sxs-lookup"><span data-stu-id="7eb17-279">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-280">118</span><span class="sxs-lookup"><span data-stu-id="7eb17-280">118</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-281">LC</span><span class="sxs-lookup"><span data-stu-id="7eb17-281">LC</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-282">119</span><span class="sxs-lookup"><span data-stu-id="7eb17-282">119</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-283">HSSC</span><span class="sxs-lookup"><span data-stu-id="7eb17-283">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-284">120</span><span class="sxs-lookup"><span data-stu-id="7eb17-284">120</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-285">VHDCI blindado (68 pines)</span><span class="sxs-lookup"><span data-stu-id="7eb17-285">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-286">121</span><span class="sxs-lookup"><span data-stu-id="7eb17-286">121</span></span>
</dt> <dd>

<span data-ttu-id="7eb17-287">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="7eb17-287">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7eb17-288">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7eb17-288">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-291">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="7eb17-291">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-292">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="7eb17-292">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="7eb17-293">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="7eb17-293">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="7eb17-294">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-294">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-295">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7eb17-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-296">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-298">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7eb17-298">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-299">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="7eb17-299">Description of the object.</span></span>

<span data-ttu-id="7eb17-300">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-301">**ExternalReferenceDesignator**</span><span class="sxs-lookup"><span data-stu-id="7eb17-301">**ExternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-302">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-304">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| designador de referencia externa de tipo SMBIOS 8 \| ")</span><span class="sxs-lookup"><span data-stu-id="7eb17-304">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|External Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-305">Designador de referencia externa del puerto.</span><span class="sxs-lookup"><span data-stu-id="7eb17-305">External reference designator of the port.</span></span> <span data-ttu-id="7eb17-306">Los designadores de referencia externa son identificadores que determinan el tipo y el uso del puerto.</span><span class="sxs-lookup"><span data-stu-id="7eb17-306">External reference designators are identifiers that determine the type and use of the port.</span></span>

<span data-ttu-id="7eb17-307">Ejemplo: "COM1"</span><span class="sxs-lookup"><span data-stu-id="7eb17-307">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7eb17-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-309">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7eb17-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-311">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7eb17-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-312">Fecha y hora de instalación del objeto.</span><span class="sxs-lookup"><span data-stu-id="7eb17-312">Date and time the object is installed.</span></span> <span data-ttu-id="7eb17-313">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="7eb17-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7eb17-314">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-315">**InternalReferenceDesignator**</span><span class="sxs-lookup"><span data-stu-id="7eb17-315">**InternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-318">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| designador de referencia interna de tipo de SMBIOS 8 \| ")</span><span class="sxs-lookup"><span data-stu-id="7eb17-318">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-319">Designador de referencia interno del puerto.</span><span class="sxs-lookup"><span data-stu-id="7eb17-319">Internal reference designator of the port.</span></span> <span data-ttu-id="7eb17-320">Los designadores de referencia internos son específicos del fabricante e identifican la ubicación del panel de circuitos o el uso del puerto.</span><span class="sxs-lookup"><span data-stu-id="7eb17-320">Internal reference designators are specific to the manufacturer, and identify the circuit board location or use of the port.</span></span>

<span data-ttu-id="7eb17-321">Ejemplo: "J101"</span><span class="sxs-lookup"><span data-stu-id="7eb17-321">Example: "J101"</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-322">**Le**</span><span class="sxs-lookup"><span data-stu-id="7eb17-322">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-323">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-325">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="7eb17-325">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-326">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="7eb17-326">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="7eb17-327">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-327">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-328">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="7eb17-328">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-329">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-331">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="7eb17-331">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-332">Nombre del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="7eb17-332">Name for the physical element.</span></span>

<span data-ttu-id="7eb17-333">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-333">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-334">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7eb17-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-335">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-337">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7eb17-337">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-338">Etiqueta del objeto.</span><span class="sxs-lookup"><span data-stu-id="7eb17-338">Label for the object.</span></span> <span data-ttu-id="7eb17-339">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="7eb17-339">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="7eb17-340">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="7eb17-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-342">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-344">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="7eb17-344">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="7eb17-345">Un ejemplo son los datos de código de barras asociados a un elemento que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="7eb17-345">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="7eb17-346">Si solo los datos de código de barras están disponibles y son únicos o se pueden usar como una clave de elemento, esta propiedad es **null** y los datos de código de barras se usan como clave de clase en la propiedad de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="7eb17-346">If only bar code data is available and unique or able to be used as an element key, this property is **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="7eb17-347">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-347">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-348">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="7eb17-348">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-351">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="7eb17-351">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-352">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="7eb17-352">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="7eb17-353">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-353">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-354">**PortType**</span><span class="sxs-lookup"><span data-stu-id="7eb17-354">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-355">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eb17-355">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-357">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (tipo de \| Puerto de tipo SMBIOS 8 \| )</span><span class="sxs-lookup"><span data-stu-id="7eb17-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Port Type")</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-358">Función del puerto.</span><span class="sxs-lookup"><span data-stu-id="7eb17-358">Function of the port.</span></span> <span data-ttu-id="7eb17-359">En la lista siguiente se enumeran los valores.</span><span class="sxs-lookup"><span data-stu-id="7eb17-359">The following list lists the values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="7eb17-360">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="7eb17-360">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_XT_AT_Compatible"></span><span id="parallel_port_xt_at_compatible"></span><span id="PARALLEL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="7eb17-361">**Puerto paralelo XT/at compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="7eb17-361">**Parallel Port XT/AT Compatible** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_PS_2"></span><span id="parallel_port_ps_2"></span><span id="PARALLEL_PORT_PS_2"></span>

<span data-ttu-id="7eb17-362">**Puerto paralelo PS/2** (2)</span><span class="sxs-lookup"><span data-stu-id="7eb17-362">**Parallel Port PS/2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP"></span><span id="parallel_port_ecp"></span><span id="PARALLEL_PORT_ECP"></span>

<span data-ttu-id="7eb17-363">**Puerto paralelo ECP** (3)</span><span class="sxs-lookup"><span data-stu-id="7eb17-363">**Parallel Port ECP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_EPP"></span><span id="parallel_port_epp"></span><span id="PARALLEL_PORT_EPP"></span>

<span data-ttu-id="7eb17-364">**Puerto paralelo EPP** (4)</span><span class="sxs-lookup"><span data-stu-id="7eb17-364">**Parallel Port EPP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP_EPP"></span><span id="parallel_port_ecp_epp"></span><span id="PARALLEL_PORT_ECP_EPP"></span>

<span data-ttu-id="7eb17-365">**Puerto paralelo ECP/EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="7eb17-365">**Parallel Port ECP/EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_XT_AT_Compatible"></span><span id="serial_port_xt_at_compatible"></span><span id="SERIAL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="7eb17-366">**Puerto serie XT/at compatible** (6)</span><span class="sxs-lookup"><span data-stu-id="7eb17-366">**Serial Port XT/AT Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16450_Compatible"></span><span id="serial_port_16450_compatible"></span><span id="SERIAL_PORT_16450_COMPATIBLE"></span>

<span data-ttu-id="7eb17-367">**Puerto serie 16450 compatible** (7)</span><span class="sxs-lookup"><span data-stu-id="7eb17-367">**Serial Port 16450 Compatible** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550_Compatible"></span><span id="serial_port_16550_compatible"></span><span id="SERIAL_PORT_16550_COMPATIBLE"></span>

<span data-ttu-id="7eb17-368">**Puerto serie 16550 compatible** (8)</span><span class="sxs-lookup"><span data-stu-id="7eb17-368">**Serial Port 16550 Compatible** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550A_Compatible"></span><span id="serial_port_16550a_compatible"></span><span id="SERIAL_PORT_16550A_COMPATIBLE"></span>

<span data-ttu-id="7eb17-369">**Puerto serie 16550A compatible** (9)</span><span class="sxs-lookup"><span data-stu-id="7eb17-369">**Serial Port 16550A Compatible** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Port"></span><span id="scsi_port"></span><span id="SCSI_PORT"></span>

<span data-ttu-id="7eb17-370">**Puerto SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="7eb17-370">**SCSI Port** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MIDI_Port"></span><span id="midi_port"></span><span id="MIDI_PORT"></span>

<span data-ttu-id="7eb17-371">**Puerto MIDI** (11)</span><span class="sxs-lookup"><span data-stu-id="7eb17-371">**MIDI Port** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Joy_Stick_Port"></span><span id="joy_stick_port"></span><span id="JOY_STICK_PORT"></span>

<span data-ttu-id="7eb17-372">**Puerto de Joy Stick** (12)</span><span class="sxs-lookup"><span data-stu-id="7eb17-372">**Joy Stick Port** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Keyboard_Port"></span><span id="keyboard_port"></span><span id="KEYBOARD_PORT"></span>

<span data-ttu-id="7eb17-373">**Puerto de teclado** (13)</span><span class="sxs-lookup"><span data-stu-id="7eb17-373">**Keyboard Port** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_Port"></span><span id="mouse_port"></span><span id="MOUSE_PORT"></span>

<span data-ttu-id="7eb17-374">**Puerto del mouse** (14)</span><span class="sxs-lookup"><span data-stu-id="7eb17-374">**Mouse Port** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="7eb17-375">**SCSI SSA** (15)</span><span class="sxs-lookup"><span data-stu-id="7eb17-375">**SSA SCSI** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="7eb17-376">**USB** (16)</span><span class="sxs-lookup"><span data-stu-id="7eb17-376">**USB** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FireWire__IEEE_P1394_"></span><span id="firewire__ieee_p1394_"></span><span id="FIREWIRE__IEEE_P1394_"></span>

<span data-ttu-id="7eb17-377">**FireWire (IEEE P1394)** (17)</span><span class="sxs-lookup"><span data-stu-id="7eb17-377">**FireWire (IEEE P1394)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="7eb17-378">**PCMCIA tipo II** (18)</span><span class="sxs-lookup"><span data-stu-id="7eb17-378">**PCMCIA Type II** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="7eb17-379">**PCMCIA tipo II** (19)</span><span class="sxs-lookup"><span data-stu-id="7eb17-379">**PCMCIA Type II** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="7eb17-380">**PCMCIA, tipo III** (20)</span><span class="sxs-lookup"><span data-stu-id="7eb17-380">**PCMCIA Type III** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Cardbus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="7eb17-381">**CardBus** (21)</span><span class="sxs-lookup"><span data-stu-id="7eb17-381">**Cardbus** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Bus_Port"></span><span id="access_bus_port"></span><span id="ACCESS_BUS_PORT"></span>

<span data-ttu-id="7eb17-382">**Puerto de bus de acceso** (22)</span><span class="sxs-lookup"><span data-stu-id="7eb17-382">**Access Bus Port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_II"></span><span id="scsi_ii"></span>

<span data-ttu-id="7eb17-383">**SCSI II** (23)</span><span class="sxs-lookup"><span data-stu-id="7eb17-383">**SCSI II** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Wide"></span><span id="scsi_wide"></span><span id="SCSI_WIDE"></span>

<span data-ttu-id="7eb17-384">**SCSI de ancho** (24)</span><span class="sxs-lookup"><span data-stu-id="7eb17-384">**SCSI Wide** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="7eb17-385">**PC-98** (25)</span><span class="sxs-lookup"><span data-stu-id="7eb17-385">**PC-98** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="7eb17-386">**PC-98-Hireso** (26)</span><span class="sxs-lookup"><span data-stu-id="7eb17-386">**PC-98-Hireso** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="7eb17-387">**PC-H98** (27)</span><span class="sxs-lookup"><span data-stu-id="7eb17-387">**PC-H98** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Port"></span><span id="video_port"></span><span id="VIDEO_PORT"></span>

<span data-ttu-id="7eb17-388">**Puerto de vídeo** (28)</span><span class="sxs-lookup"><span data-stu-id="7eb17-388">**Video Port** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Audio_Port"></span><span id="audio_port"></span><span id="AUDIO_PORT"></span>

<span data-ttu-id="7eb17-389">**Puerto de audio** (29)</span><span class="sxs-lookup"><span data-stu-id="7eb17-389">**Audio Port** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Port"></span><span id="modem_port"></span><span id="MODEM_PORT"></span>

<span data-ttu-id="7eb17-390">**Puerto del módem** (30)</span><span class="sxs-lookup"><span data-stu-id="7eb17-390">**Modem Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Port"></span><span id="network_port"></span><span id="NETWORK_PORT"></span>

<span data-ttu-id="7eb17-391">**Puerto de red** (31)</span><span class="sxs-lookup"><span data-stu-id="7eb17-391">**Network Port** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="7eb17-392">**compatible con 8251** (32)</span><span class="sxs-lookup"><span data-stu-id="7eb17-392">**8251 Compatible** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_FIFO_Compatible"></span><span id="8251_fifo_compatible"></span><span id="8251_FIFO_COMPATIBLE"></span>

<span data-ttu-id="7eb17-393">**8251 FIFO compatible** (33)</span><span class="sxs-lookup"><span data-stu-id="7eb17-393">**8251 FIFO Compatible** (33)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7eb17-394">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="7eb17-394">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-395">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7eb17-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-397">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="7eb17-397">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="7eb17-398">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-398">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-399">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="7eb17-399">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-400">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-401">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-402">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="7eb17-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-403">Número asignado por el fabricante que se usa para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="7eb17-403">Manufacturer-allocated number used to identify a physical element.</span></span>

<span data-ttu-id="7eb17-404">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-404">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-405">**SKU**</span><span class="sxs-lookup"><span data-stu-id="7eb17-405">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-406">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-408">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="7eb17-408">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-409">Número de referencia de almacén para un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="7eb17-409">Stock keeping unit number for a physical element.</span></span>

<span data-ttu-id="7eb17-410">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-410">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-411">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7eb17-411">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-412">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-414">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="7eb17-414">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-415">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7eb17-415">Current status of the object.</span></span> <span data-ttu-id="7eb17-416">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="7eb17-416">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7eb17-417">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="7eb17-417">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7eb17-418">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="7eb17-418">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7eb17-419">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="7eb17-419">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7eb17-420">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="7eb17-420">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7eb17-421">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7eb17-422">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7eb17-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7eb17-423">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7eb17-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7eb17-424">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7eb17-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7eb17-425">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7eb17-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7eb17-426">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7eb17-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7eb17-427">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7eb17-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7eb17-428">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7eb17-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7eb17-429">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7eb17-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7eb17-430">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7eb17-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7eb17-431">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7eb17-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7eb17-432">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7eb17-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7eb17-433">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7eb17-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7eb17-434">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7eb17-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7eb17-435">**Tag**</span><span class="sxs-lookup"><span data-stu-id="7eb17-435">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-436">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-438">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**invalidación**](../wmisdk/standard-qualifiers.md) ("etiqueta"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="7eb17-438">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-439">Identificador único de una conexión de puerto en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="7eb17-439">Unique identifier of a port connection on the computer system.</span></span>

<span data-ttu-id="7eb17-440">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-440">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="7eb17-441">Ejemplo: "conector de puerto 1"</span><span class="sxs-lookup"><span data-stu-id="7eb17-441">Example: "Port Connector 1"</span></span>

</dd> <dt>

<span data-ttu-id="7eb17-442">**Versión**</span><span class="sxs-lookup"><span data-stu-id="7eb17-442">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eb17-443">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7eb17-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eb17-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eb17-445">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="7eb17-445">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7eb17-446">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="7eb17-446">Version of the physical element.</span></span>

<span data-ttu-id="7eb17-447">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7eb17-448">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7eb17-448">Remarks</span></span>

<span data-ttu-id="7eb17-449">La **clase \_ PortConnector de Win32** se deriva de [**\_ PhysicalConnector de CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="7eb17-449">The **Win32\_PortConnector** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7eb17-450">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eb17-450">Requirements</span></span>



| <span data-ttu-id="7eb17-451">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eb17-451">Requirement</span></span> | <span data-ttu-id="7eb17-452">Value</span><span class="sxs-lookup"><span data-stu-id="7eb17-452">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb17-453">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7eb17-453">Minimum supported client</span></span><br/> | <span data-ttu-id="7eb17-454">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7eb17-454">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7eb17-455">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7eb17-455">Minimum supported server</span></span><br/> | <span data-ttu-id="7eb17-456">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7eb17-456">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7eb17-457">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7eb17-457">Namespace</span></span><br/>                | <span data-ttu-id="7eb17-458">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7eb17-458">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7eb17-459">MOF</span><span class="sxs-lookup"><span data-stu-id="7eb17-459">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7eb17-460"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7eb17-460"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7eb17-461">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7eb17-461">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eb17-462"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eb17-462"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eb17-463">Vea también</span><span class="sxs-lookup"><span data-stu-id="7eb17-463">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb17-464">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="7eb17-464">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dt>

[<span data-ttu-id="7eb17-465">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="7eb17-465">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
