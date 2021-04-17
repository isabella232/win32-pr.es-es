---
description: La \_ clase CIM PhysicalConnector representa cualquier elemento físico que se utiliza para conectarse a otros elementos. Cualquier objeto que pueda conectarse y transmitir señales o potencia entre dos o más elementos físicos es un descendiente (o miembro) de esta clase.
ms.assetid: cc135ae8-5ae1-4028-a2e3-a81db8694d9d
ms.tgt_platform: multiple
title: CIM_PhysicalConnector (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalConnector
- CIM_PhysicalConnector.Caption
- CIM_PhysicalConnector.Description
- CIM_PhysicalConnector.InstallDate
- CIM_PhysicalConnector.Name
- CIM_PhysicalConnector.Status
- CIM_PhysicalConnector.CreationClassName
- CIM_PhysicalConnector.Manufacturer
- CIM_PhysicalConnector.Model
- CIM_PhysicalConnector.OtherIdentifyingInfo
- CIM_PhysicalConnector.PartNumber
- CIM_PhysicalConnector.PoweredOn
- CIM_PhysicalConnector.SerialNumber
- CIM_PhysicalConnector.SKU
- CIM_PhysicalConnector.Tag
- CIM_PhysicalConnector.Version
- CIM_PhysicalConnector.ConnectorPinout
- CIM_PhysicalConnector.ConnectorType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 106b8ab30296b77be550809771db3b0208485872
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659624"
---
# <a name="cim_physicalconnector-class"></a><span data-ttu-id="8a595-104">\_Clase PhysicalConnector de CIM</span><span class="sxs-lookup"><span data-stu-id="8a595-104">CIM\_PhysicalConnector class</span></span>

<span data-ttu-id="8a595-105">La clase **CIM \_ PhysicalConnector** representa cualquier elemento físico que se utiliza para conectarse a otros elementos.</span><span class="sxs-lookup"><span data-stu-id="8a595-105">The **CIM\_PhysicalConnector** class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="8a595-106">Cualquier objeto que pueda conectarse y transmitir señales o potencia entre dos o más elementos físicos es un descendiente (o miembro) de esta clase.</span><span class="sxs-lookup"><span data-stu-id="8a595-106">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span> <span data-ttu-id="8a595-107">Por ejemplo, las ranuras y los conectores de shell D son tipos de conectores físicos.</span><span class="sxs-lookup"><span data-stu-id="8a595-107">For example, slots and D-shell connectors are types of physical connectors.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a595-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="8a595-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8a595-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8a595-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8a595-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8a595-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8a595-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="8a595-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a595-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a595-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B84-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalConnector : CIM_PhysicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  string   ConnectorPinout;
  uint16   ConnectorType[];
};
```

## <a name="members"></a><span data-ttu-id="8a595-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a595-113">Members</span></span>

<span data-ttu-id="8a595-114">La clase **CIM \_ PhysicalConnector** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8a595-114">The **CIM\_PhysicalConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="8a595-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a595-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a595-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a595-116">Properties</span></span>

<span data-ttu-id="8a595-117">La clase **CIM \_ PhysicalConnector** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8a595-117">The **CIM\_PhysicalConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a595-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8a595-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-121">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8a595-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8a595-122">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="8a595-122">A short textual description of the object.</span></span>

<span data-ttu-id="8a595-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-124">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="8a595-124">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a595-127">Cadena de forma libre que describe la configuración del PIN y el uso de la señal de un conector físico.</span><span class="sxs-lookup"><span data-stu-id="8a595-127">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

</dd> <dt>

<span data-ttu-id="8a595-128">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="8a595-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-129">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a595-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8a595-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a595-131">Tipo de conector físico.</span><span class="sxs-lookup"><span data-stu-id="8a595-131">Type of physical connector.</span></span> <span data-ttu-id="8a595-132">Se especifica una matriz para permitir la descripción de las combinaciones de información del conector.</span><span class="sxs-lookup"><span data-stu-id="8a595-132">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="8a595-133">Por ejemplo, una entrada de matriz podría especificar RS-232, otra DB-25 y una tercera entrada podría definir el conector como "hombre".</span><span class="sxs-lookup"><span data-stu-id="8a595-133">For example, one array entry could specify RS-232, another DB-25, and a third entry could define the connector as "male".</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8a595-134">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8a595-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8a595-135">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8a595-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="8a595-136">**Macho** (2)</span><span class="sxs-lookup"><span data-stu-id="8a595-136">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="8a595-137">**Hembra** (3)</span><span class="sxs-lookup"><span data-stu-id="8a595-137">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="8a595-138">**Blindado** (4)</span><span class="sxs-lookup"><span data-stu-id="8a595-138">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="8a595-139">No **blindado** (5)</span><span class="sxs-lookup"><span data-stu-id="8a595-139">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="8a595-140">**SCSI (A) High-Density (50 pines)** (6)</span><span class="sxs-lookup"><span data-stu-id="8a595-140">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="8a595-141">**SCSI (A) Low-Density (50 Pin)** (7)</span><span class="sxs-lookup"><span data-stu-id="8a595-141">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="8a595-142">**SCSI (P) High-Density (68 pines)** (8)</span><span class="sxs-lookup"><span data-stu-id="8a595-142">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="8a595-143">**SCSI SCA-I (80 pines)** (9)</span><span class="sxs-lookup"><span data-stu-id="8a595-143">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="8a595-144">**SCSI SCA-II (80 pines)** (10)</span><span class="sxs-lookup"><span data-stu-id="8a595-144">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="8a595-145">**Canal de fibra SCSI (DB-9, cobre)** (11)</span><span class="sxs-lookup"><span data-stu-id="8a595-145">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="8a595-146">**Canal de fibra SCSI (fibra)** (12)</span><span class="sxs-lookup"><span data-stu-id="8a595-146">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="8a595-147">**SCSI canal de fibra SCA-II (40 pines)** (13)</span><span class="sxs-lookup"><span data-stu-id="8a595-147">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="8a595-148">**SCSI canal de fibra SCA-II (20 clavijas)** (14)</span><span class="sxs-lookup"><span data-stu-id="8a595-148">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="8a595-149">**SCSI canal de fibra BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="8a595-149">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="8a595-150">**ATA 3-1/2 pulgada (40 PIN)** (16)</span><span class="sxs-lookup"><span data-stu-id="8a595-150">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="8a595-151">**ATA 2-1/2 pulgada (44 PIN)** (17)</span><span class="sxs-lookup"><span data-stu-id="8a595-151">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="8a595-152">**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="8a595-152">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="8a595-153">**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="8a595-153">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="8a595-154">**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="8a595-154">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="8a595-155">**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="8a595-155">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="8a595-156">**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="8a595-156">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="8a595-157">**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="8a595-157">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="8a595-158">**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="8a595-158">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="8a595-159">**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="8a595-159">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="8a595-160">**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="8a595-160">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="8a595-161">**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="8a595-161">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="8a595-162">**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="8a595-162">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="8a595-163">**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="8a595-163">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="8a595-164">**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="8a595-164">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="8a595-165">**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="8a595-165">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="8a595-166">**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="8a595-166">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="8a595-167">**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="8a595-167">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="8a595-168">**UTP categoría 3** (34)</span><span class="sxs-lookup"><span data-stu-id="8a595-168">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="8a595-169">**UTP categoría 4** (35)</span><span class="sxs-lookup"><span data-stu-id="8a595-169">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="8a595-170">**UTP categoría 5** (36)</span><span class="sxs-lookup"><span data-stu-id="8a595-170">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="8a595-171">**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="8a595-171">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="8a595-172">**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="8a595-172">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="8a595-173">**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="8a595-173">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="8a595-174">**MIC de fibra** (40)</span><span class="sxs-lookup"><span data-stu-id="8a595-174">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="8a595-175">**AUI de Apple** (41)</span><span class="sxs-lookup"><span data-stu-id="8a595-175">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="8a595-176">**Apple geoport** (42)</span><span class="sxs-lookup"><span data-stu-id="8a595-176">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="8a595-177">**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="8a595-177">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="8a595-178">**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="8a595-178">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="8a595-179">**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="8a595-179">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="8a595-180">**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="8a595-180">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="8a595-181">**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="8a595-181">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="8a595-182">**PCMCIA tipo I** (48)</span><span class="sxs-lookup"><span data-stu-id="8a595-182">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="8a595-183">**PCMCIA (tipo II** ) (49)</span><span class="sxs-lookup"><span data-stu-id="8a595-183">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="8a595-184">**PCMCIA, tipo III** (50)</span><span class="sxs-lookup"><span data-stu-id="8a595-184">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="8a595-185">**Puerto ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="8a595-185">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="8a595-186">**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="8a595-186">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="8a595-187">**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="8a595-187">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="8a595-188">**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="8a595-188">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="8a595-189">**HIPPI** (55)</span><span class="sxs-lookup"><span data-stu-id="8a595-189">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="8a595-190">**HSSDC (6 clavijas)** (56)</span><span class="sxs-lookup"><span data-stu-id="8a595-190">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="8a595-191">**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="8a595-191">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="8a595-192">**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="8a595-192">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="8a595-193">**Mini DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="8a595-193">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="8a595-194">**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="8a595-194">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="8a595-195">**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="8a595-195">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="8a595-196">**Infrarrojos** (62)</span><span class="sxs-lookup"><span data-stu-id="8a595-196">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="8a595-197">**HP-Hil** (63)</span><span class="sxs-lookup"><span data-stu-id="8a595-197">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="8a595-198">**Access. bus** (64)</span><span class="sxs-lookup"><span data-stu-id="8a595-198">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="8a595-199">**Nubus** (65)</span><span class="sxs-lookup"><span data-stu-id="8a595-199">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="8a595-200">**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="8a595-200">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="8a595-201">**Minicontrolador-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="8a595-201">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="8a595-202">**Mini-Centronics tipo-14** (68)</span><span class="sxs-lookup"><span data-stu-id="8a595-202">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="8a595-203">**Mini-Centronics tipo-20** (69)</span><span class="sxs-lookup"><span data-stu-id="8a595-203">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="8a595-204">**Mini-Centronics tipo-26** (70)</span><span class="sxs-lookup"><span data-stu-id="8a595-204">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="8a595-205">**Mouse de bus** (71)</span><span class="sxs-lookup"><span data-stu-id="8a595-205">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="8a595-206">**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="8a595-206">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="8a595-207">**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="8a595-207">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="8a595-208">**Bus VME** (74)</span><span class="sxs-lookup"><span data-stu-id="8a595-208">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="8a595-209">**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="8a595-209">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="8a595-210">**Propietario** (76)</span><span class="sxs-lookup"><span data-stu-id="8a595-210">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="8a595-211">**Ranura de tarjeta del procesador de propiedad** (77)</span><span class="sxs-lookup"><span data-stu-id="8a595-211">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="8a595-212">**Ranura de tarjeta de memoria de propiedad** (78)</span><span class="sxs-lookup"><span data-stu-id="8a595-212">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="8a595-213">**Ranura de aumento de e/s de propiedad** (79)</span><span class="sxs-lookup"><span data-stu-id="8a595-213">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="8a595-214">**PCI-66** (80)</span><span class="sxs-lookup"><span data-stu-id="8a595-214">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="8a595-215">**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="8a595-215">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="8a595-216">**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="8a595-216">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="8a595-217">**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="8a595-217">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="8a595-218">**PC-98-Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="8a595-218">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="8a595-219">**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="8a595-219">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="8a595-220">**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="8a595-220">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="8a595-221">**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="8a595-221">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="8a595-222">**SCSI SSA** (88)</span><span class="sxs-lookup"><span data-stu-id="8a595-222">**SSA SCSI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Circular"></span><span id="circular"></span><span id="CIRCULAR"></span>

<span data-ttu-id="8a595-223">**Circular** (89)</span><span class="sxs-lookup"><span data-stu-id="8a595-223">**Circular** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_IDE_Connector"></span><span id="on_board_ide_connector"></span><span id="ON_BOARD_IDE_CONNECTOR"></span>

<span data-ttu-id="8a595-224">**Conector IDE incorporado** (90)</span><span class="sxs-lookup"><span data-stu-id="8a595-224">**On Board IDE Connector** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Floppy_Connector"></span><span id="on_board_floppy_connector"></span><span id="ON_BOARD_FLOPPY_CONNECTOR"></span>

<span data-ttu-id="8a595-225">**Conector de disquete incorporado** (91)</span><span class="sxs-lookup"><span data-stu-id="8a595-225">**On Board Floppy Connector** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Pin_Dual_Inline"></span><span id="9_pin_dual_inline"></span><span id="9_PIN_DUAL_INLINE"></span>

<span data-ttu-id="8a595-226">**8 pines Dual Inline** (92)</span><span class="sxs-lookup"><span data-stu-id="8a595-226">**9 Pin Dual Inline** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="25_Pin_Dual_Inline"></span><span id="25_pin_dual_inline"></span><span id="25_PIN_DUAL_INLINE"></span>

<span data-ttu-id="8a595-227">**25 patillas en línea dual** (93)</span><span class="sxs-lookup"><span data-stu-id="8a595-227">**25 Pin Dual Inline** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="8a595-228">**PIN dual de 50 en línea** (94)</span><span class="sxs-lookup"><span data-stu-id="8a595-228">**50 Pin Dual Inline** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="68_Pin_Dual_Inline"></span><span id="68_pin_dual_inline"></span><span id="68_PIN_DUAL_INLINE"></span>

<span data-ttu-id="8a595-229">**PIN dual de 68 en línea** (95)</span><span class="sxs-lookup"><span data-stu-id="8a595-229">**68 Pin Dual Inline** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Sound_Connector"></span><span id="on_board_sound_connector"></span><span id="ON_BOARD_SOUND_CONNECTOR"></span>

<span data-ttu-id="8a595-230">**Conector de sonido de la placa** (96)</span><span class="sxs-lookup"><span data-stu-id="8a595-230">**On Board Sound Connector** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="8a595-231">**Miniconector (97** )</span><span class="sxs-lookup"><span data-stu-id="8a595-231">**Mini-jack** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="8a595-232">**PCI-X** (98)</span><span class="sxs-lookup"><span data-stu-id="8a595-232">**PCI-X** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="8a595-233">**SBus IEEE 1396-1993 32 bit** (99)</span><span class="sxs-lookup"><span data-stu-id="8a595-233">**Sbus IEEE 1396-1993 32 bit** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="8a595-234">**SBus IEEE 1396-1993 64 bit** (100)</span><span class="sxs-lookup"><span data-stu-id="8a595-234">**Sbus IEEE 1396-1993 64 bit** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="8a595-235">**MCA** (101)</span><span class="sxs-lookup"><span data-stu-id="8a595-235">**MCA** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="8a595-236">**Gio** (102)</span><span class="sxs-lookup"><span data-stu-id="8a595-236">**GIO** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="8a595-237">**Xio** (103)</span><span class="sxs-lookup"><span data-stu-id="8a595-237">**XIO** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="8a595-238">**Hio** (104)</span><span class="sxs-lookup"><span data-stu-id="8a595-238">**HIO** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="8a595-239">**NGIO** (105)</span><span class="sxs-lookup"><span data-stu-id="8a595-239">**NGIO** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="8a595-240">**PMC** (106)</span><span class="sxs-lookup"><span data-stu-id="8a595-240">**PMC** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="MTRJ"></span><span id="mtrj"></span>

<span data-ttu-id="8a595-241">**MTRJ** (107)</span><span class="sxs-lookup"><span data-stu-id="8a595-241">**MTRJ** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="VF-45"></span><span id="vf-45"></span>

<span data-ttu-id="8a595-242">**VF-45** (108)</span><span class="sxs-lookup"><span data-stu-id="8a595-242">**VF-45** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="8a595-243">**E/s futura** (109)</span><span class="sxs-lookup"><span data-stu-id="8a595-243">**Future I/O** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="SC"></span><span id="sc"></span>

<span data-ttu-id="8a595-244">**SC** (110)</span><span class="sxs-lookup"><span data-stu-id="8a595-244">**SC** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="SG"></span><span id="sg"></span>

<span data-ttu-id="8a595-245">**SG** (111)</span><span class="sxs-lookup"><span data-stu-id="8a595-245">**SG** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrical"></span><span id="electrical"></span><span id="ELECTRICAL"></span>

<span data-ttu-id="8a595-246">**Eléctrico** (112)</span><span class="sxs-lookup"><span data-stu-id="8a595-246">**Electrical** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical"></span><span id="optical"></span><span id="OPTICAL"></span>

<span data-ttu-id="8a595-247">**Óptico** (113)</span><span class="sxs-lookup"><span data-stu-id="8a595-247">**Optical** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon"></span><span id="ribbon"></span><span id="RIBBON"></span>

<span data-ttu-id="8a595-248">**Cinta** (114)</span><span class="sxs-lookup"><span data-stu-id="8a595-248">**Ribbon** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="GLM"></span><span id="glm"></span>

<span data-ttu-id="8a595-249">**GLM** (115)</span><span class="sxs-lookup"><span data-stu-id="8a595-249">**GLM** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="1x9"></span><span id="1X9"></span>

<span data-ttu-id="8a595-250">**1x9** (116)</span><span class="sxs-lookup"><span data-stu-id="8a595-250">**1x9** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_SG"></span><span id="mini_sg"></span><span id="MINI_SG"></span>

<span data-ttu-id="8a595-251">**Mini SG** (117)</span><span class="sxs-lookup"><span data-stu-id="8a595-251">**Mini SG** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="LC"></span><span id="lc"></span>

<span data-ttu-id="8a595-252">**LC** (118)</span><span class="sxs-lookup"><span data-stu-id="8a595-252">**LC** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSC"></span><span id="hssc"></span>

<span data-ttu-id="8a595-253">**HSSC** (119)</span><span class="sxs-lookup"><span data-stu-id="8a595-253">**HSSC** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDCI_Shielded__68_pins_"></span><span id="vhdci_shielded__68_pins_"></span><span id="VHDCI_SHIELDED__68_PINS_"></span>

<span data-ttu-id="8a595-254">**VHDCI blindado (68 pines)** (120)</span><span class="sxs-lookup"><span data-stu-id="8a595-254">**VHDCI Shielded (68 pins)** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="8a595-255">**InfiniBand** (121)</span><span class="sxs-lookup"><span data-stu-id="8a595-255">**InfiniBand** (121)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a595-256">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8a595-256">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-259">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8a595-259">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8a595-260">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="8a595-260">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8a595-261">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="8a595-261">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8a595-262">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-263">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8a595-263">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-266">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="8a595-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8a595-267">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="8a595-267">A textual description of the object.</span></span>

<span data-ttu-id="8a595-268">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-268">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-269">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8a595-269">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-270">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8a595-270">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-272">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="8a595-272">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8a595-273">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="8a595-273">Indicates when the object was installed.</span></span> <span data-ttu-id="8a595-274">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="8a595-274">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8a595-275">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-276">**Le**</span><span class="sxs-lookup"><span data-stu-id="8a595-276">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-277">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-279">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8a595-279">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8a595-280">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8a595-280">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="8a595-281">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-281">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="8a595-282">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-283">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="8a595-283">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-284">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-286">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8a595-286">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8a595-287">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8a595-287">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="8a595-288">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-288">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-289">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8a595-289">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-290">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-292">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8a595-292">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8a595-293">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="8a595-293">Label by which the object is known.</span></span> <span data-ttu-id="8a595-294">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="8a595-294">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8a595-295">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-296">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8a595-296">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a595-299">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8a595-299">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="8a595-300">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="8a595-300">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="8a595-301">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="8a595-301">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="8a595-302">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-303">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="8a595-303">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-306">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8a595-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8a595-307">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8a595-307">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="8a595-308">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-308">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-309">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="8a595-309">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-310">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8a595-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a595-312">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="8a595-312">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="8a595-313">De lo contrario, está actualmente desactivado.</span><span class="sxs-lookup"><span data-stu-id="8a595-313">Otherwise, it is currently off.</span></span>

<span data-ttu-id="8a595-314">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-315">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="8a595-315">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-318">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8a595-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8a595-319">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8a595-319">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="8a595-320">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-321">**SKU**</span><span class="sxs-lookup"><span data-stu-id="8a595-321">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-324">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8a595-324">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8a595-325">Número de unidad de almacén para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8a595-325">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="8a595-326">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-327">**Estado**</span><span class="sxs-lookup"><span data-stu-id="8a595-327">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-328">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-330">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="8a595-330">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8a595-331">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="8a595-331">String that indicates the current status of the object.</span></span> <span data-ttu-id="8a595-332">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="8a595-332">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8a595-333">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="8a595-333">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8a595-334">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="8a595-334">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8a595-335">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="8a595-335">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8a595-336">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="8a595-336">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8a595-337">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="8a595-337">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8a595-338">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8a595-339">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8a595-339">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8a595-340">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="8a595-340">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8a595-341">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="8a595-341">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8a595-342">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="8a595-342">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8a595-343">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="8a595-343">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8a595-344">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="8a595-344">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8a595-345">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="8a595-345">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8a595-346">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="8a595-346">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8a595-347">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="8a595-347">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8a595-348">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="8a595-348">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8a595-349">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="8a595-349">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8a595-350">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="8a595-350">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8a595-351">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="8a595-351">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a595-352">**Tag**</span><span class="sxs-lookup"><span data-stu-id="8a595-352">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-355">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8a595-355">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8a595-356">Identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="8a595-356">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="8a595-357">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="8a595-357">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="8a595-358">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="8a595-358">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="8a595-359">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="8a595-359">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="8a595-360">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8a595-360">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="8a595-361">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="8a595-361">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="8a595-362">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-362">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a595-363">**Versión**</span><span class="sxs-lookup"><span data-stu-id="8a595-363">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a595-364">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a595-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a595-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a595-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a595-366">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8a595-366">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8a595-367">Indica la versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8a595-367">Indicates the version of the physical element.</span></span>

<span data-ttu-id="8a595-368">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-368">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a595-369">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a595-369">Remarks</span></span>

<span data-ttu-id="8a595-370">La clase **CIM \_ PhysicalConnector** se deriva de [**\_ PhysicalElement de CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-370">The **CIM\_PhysicalConnector** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="8a595-371">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="8a595-371">WMI does not implement this class.</span></span> <span data-ttu-id="8a595-372">Para las clases WMI que se derivan de **\_ PhysicalConnector CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8a595-372">For WMI classes that are derived from **CIM\_PhysicalConnector**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8a595-373">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="8a595-373">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8a595-374">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="8a595-374">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a595-375">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a595-375">Requirements</span></span>



| <span data-ttu-id="8a595-376">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a595-376">Requirement</span></span> | <span data-ttu-id="8a595-377">Value</span><span class="sxs-lookup"><span data-stu-id="8a595-377">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a595-378">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a595-378">Minimum supported client</span></span><br/> | <span data-ttu-id="8a595-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a595-379">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a595-380">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a595-380">Minimum supported server</span></span><br/> | <span data-ttu-id="8a595-381">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a595-381">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a595-382">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8a595-382">Namespace</span></span><br/>                | <span data-ttu-id="8a595-383">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8a595-383">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8a595-384">MOF</span><span class="sxs-lookup"><span data-stu-id="8a595-384">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a595-385"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a595-385"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a595-386">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a595-386">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a595-387"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a595-387"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a595-388">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a595-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a595-389">**\_PHYSICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8a595-389">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

