---
description: La \_ clase de ranura CIM representa los conectores en los que se insertan los paquetes.
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: CIM_Slot (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a63c8cd200096aa132d8205691669d765e54f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496625"
---
# <a name="cim_slot-class"></a><span data-ttu-id="e90e0-103">\_Clase de ranura CIM</span><span class="sxs-lookup"><span data-stu-id="e90e0-103">CIM\_Slot class</span></span>

<span data-ttu-id="e90e0-104">La clase de **\_ ranura CIM** representa los conectores en los que se insertan los paquetes.</span><span class="sxs-lookup"><span data-stu-id="e90e0-104">The **CIM\_Slot** class represents connectors into which packages are inserted.</span></span> <span data-ttu-id="e90e0-105">Por ejemplo, un paquete físico que es una unidad de disco se puede insertar en una ranura SCA o una tarjeta (una subclase de [CIM \_ PhysicalPackage](cim-physicalpackage.md)) se puede insertar en una ranura de expansión de 16, 32 o 64 bits en un panel de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="e90e0-105">For example, a physical package that is a disk drive can be inserted into an SCA slot, or a card (a subclass of [CIM\_PhysicalPackage](cim-physicalpackage.md)) can be inserted into a 16-, 32-, or 64-bit expansion slot on a hosting board.</span></span> <span data-ttu-id="e90e0-106">Las ranuras PCI o PCMCIA de tipo III son ejemplos de este último.</span><span class="sxs-lookup"><span data-stu-id="e90e0-106">PCI or PCMCIA Type III Slots are examples of the latter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e90e0-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="e90e0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e90e0-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e90e0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e90e0-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e90e0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e90e0-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e90e0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90e0-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e90e0-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
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
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
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

## <a name="members"></a><span data-ttu-id="e90e0-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="e90e0-112">Members</span></span>

<span data-ttu-id="e90e0-113">La clase de **\_ ranura CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e90e0-113">The **CIM\_Slot** class has these types of members:</span></span>

-   [<span data-ttu-id="e90e0-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e90e0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e90e0-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e90e0-115">Properties</span></span>

<span data-ttu-id="e90e0-116">La clase de **\_ ranura CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e90e0-116">The **CIM\_Slot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e90e0-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e90e0-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-120">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e90e0-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-121">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e90e0-121">Short textual description of the object.</span></span>

<span data-ttu-id="e90e0-122">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-123">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="e90e0-123">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-126">Cadena de forma libre que describe la configuración del PIN y el uso de la señal de un conector físico.</span><span class="sxs-lookup"><span data-stu-id="e90e0-126">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

<span data-ttu-id="e90e0-127">Esta propiedad se hereda de [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-127">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-128">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="e90e0-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-129">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e90e0-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-131">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ranura del sistema DMTF \| 004,2 ")</span><span class="sxs-lookup"><span data-stu-id="e90e0-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.2")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-132">Tipo de conector físico.</span><span class="sxs-lookup"><span data-stu-id="e90e0-132">Type of physical connector.</span></span> <span data-ttu-id="e90e0-133">Se especifica una matriz para permitir la descripción de las combinaciones de información del conector.</span><span class="sxs-lookup"><span data-stu-id="e90e0-133">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="e90e0-134">Por ejemplo, una entrada de matriz podría especificar RS-232, otra DB-25 y una tercera podría definir el conector como "hombre".</span><span class="sxs-lookup"><span data-stu-id="e90e0-134">For example, one array entry could specify RS-232, another DB-25, and a third could define the connector as "Male".</span></span>

<span data-ttu-id="e90e0-135">Esta propiedad se hereda de [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-135">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<dt>

<span data-ttu-id="e90e0-136">0</span><span class="sxs-lookup"><span data-stu-id="e90e0-136">0</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-137">Unknown</span><span class="sxs-lookup"><span data-stu-id="e90e0-137">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-138">1</span><span class="sxs-lookup"><span data-stu-id="e90e0-138">1</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-139">Otros</span><span class="sxs-lookup"><span data-stu-id="e90e0-139">Other</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-140">2</span><span class="sxs-lookup"><span data-stu-id="e90e0-140">2</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-141">Male</span><span class="sxs-lookup"><span data-stu-id="e90e0-141">Male</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-142">3</span><span class="sxs-lookup"><span data-stu-id="e90e0-142">3</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-143">Female</span><span class="sxs-lookup"><span data-stu-id="e90e0-143">Female</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-144">4</span><span class="sxs-lookup"><span data-stu-id="e90e0-144">4</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-145">Blindada</span><span class="sxs-lookup"><span data-stu-id="e90e0-145">Shielded</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-146">5</span><span class="sxs-lookup"><span data-stu-id="e90e0-146">5</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-147">No blindada</span><span class="sxs-lookup"><span data-stu-id="e90e0-147">Unshielded</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-148">6</span><span class="sxs-lookup"><span data-stu-id="e90e0-148">6</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-149">SCSI (A) alta densidad (50 pines)</span><span class="sxs-lookup"><span data-stu-id="e90e0-149">SCSI (A) High-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-150">7</span><span class="sxs-lookup"><span data-stu-id="e90e0-150">7</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-151">SCSI (A) de baja densidad (50 pines)</span><span class="sxs-lookup"><span data-stu-id="e90e0-151">SCSI (A) Low-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-152">8</span><span class="sxs-lookup"><span data-stu-id="e90e0-152">8</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-153">SCSI (P) alta densidad (68 pines)</span><span class="sxs-lookup"><span data-stu-id="e90e0-153">SCSI (P) High-density (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-154">9</span><span class="sxs-lookup"><span data-stu-id="e90e0-154">9</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-155">SCSI SCA-I (80 pines)</span><span class="sxs-lookup"><span data-stu-id="e90e0-155">SCSI SCA-I (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-156">10</span><span class="sxs-lookup"><span data-stu-id="e90e0-156">10</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-157">SCSI SCA-II (80 pines)</span><span class="sxs-lookup"><span data-stu-id="e90e0-157">SCSI SCA-II (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-158">11</span><span class="sxs-lookup"><span data-stu-id="e90e0-158">11</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-159">Canal de fibra SCSI (DB-9, cobre)</span><span class="sxs-lookup"><span data-stu-id="e90e0-159">SCSI Fibre Channel (DB-9, Copper)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-160">12</span><span class="sxs-lookup"><span data-stu-id="e90e0-160">12</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-161">Canal de fibra SCSI (fibra)</span><span class="sxs-lookup"><span data-stu-id="e90e0-161">SCSI Fibre Channel (Fibre)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-162">13</span><span class="sxs-lookup"><span data-stu-id="e90e0-162">13</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-163">SCSI Canal de fibra SCA-II (40 PIN)</span><span class="sxs-lookup"><span data-stu-id="e90e0-163">SCSI Fibre Channel SCA-II (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-164">14</span><span class="sxs-lookup"><span data-stu-id="e90e0-164">14</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-165">SCSI Canal de fibra SCA-II (20 clavijas)</span><span class="sxs-lookup"><span data-stu-id="e90e0-165">SCSI Fibre Channel SCA-II (20 pins)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-166">15</span><span class="sxs-lookup"><span data-stu-id="e90e0-166">15</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-167">SCSI Canal de fibra BNC</span><span class="sxs-lookup"><span data-stu-id="e90e0-167">SCSI Fibre Channel BNC</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-168">16</span><span class="sxs-lookup"><span data-stu-id="e90e0-168">16</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-169">ATA 3-1/2 pulgadas (40 PIN)</span><span class="sxs-lookup"><span data-stu-id="e90e0-169">ATA 3-1/2 Inch (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-170">17</span><span class="sxs-lookup"><span data-stu-id="e90e0-170">17</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-171">ATA 2-1/2 pulgadas (44 PIN)</span><span class="sxs-lookup"><span data-stu-id="e90e0-171">ATA 2-1/2 Inch (44 pins)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-172">18</span><span class="sxs-lookup"><span data-stu-id="e90e0-172">18</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-173">ATA-2</span><span class="sxs-lookup"><span data-stu-id="e90e0-173">ATA-2</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-174">19</span><span class="sxs-lookup"><span data-stu-id="e90e0-174">19</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-175">ATA-3</span><span class="sxs-lookup"><span data-stu-id="e90e0-175">ATA-3</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-176">20</span><span class="sxs-lookup"><span data-stu-id="e90e0-176">20</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-177">ATA/66</span><span class="sxs-lookup"><span data-stu-id="e90e0-177">ATA/66</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-178">21</span><span class="sxs-lookup"><span data-stu-id="e90e0-178">21</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-179">DB-9</span><span class="sxs-lookup"><span data-stu-id="e90e0-179">DB-9</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-180">22</span><span class="sxs-lookup"><span data-stu-id="e90e0-180">22</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-181">DB-15</span><span class="sxs-lookup"><span data-stu-id="e90e0-181">DB-15</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-182">23</span><span class="sxs-lookup"><span data-stu-id="e90e0-182">23</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-183">DB-25</span><span class="sxs-lookup"><span data-stu-id="e90e0-183">DB-25</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-184">24</span><span class="sxs-lookup"><span data-stu-id="e90e0-184">24</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-185">DB-36</span><span class="sxs-lookup"><span data-stu-id="e90e0-185">DB-36</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-186">25</span><span class="sxs-lookup"><span data-stu-id="e90e0-186">25</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-187">RS-232C</span><span class="sxs-lookup"><span data-stu-id="e90e0-187">RS-232C</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-188">26</span><span class="sxs-lookup"><span data-stu-id="e90e0-188">26</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-189">RS-422</span><span class="sxs-lookup"><span data-stu-id="e90e0-189">RS-422</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-190">27</span><span class="sxs-lookup"><span data-stu-id="e90e0-190">27</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-191">RS-423</span><span class="sxs-lookup"><span data-stu-id="e90e0-191">RS-423</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-192">28</span><span class="sxs-lookup"><span data-stu-id="e90e0-192">28</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-193">RS-485</span><span class="sxs-lookup"><span data-stu-id="e90e0-193">RS-485</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-194">29</span><span class="sxs-lookup"><span data-stu-id="e90e0-194">29</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-195">RS-449</span><span class="sxs-lookup"><span data-stu-id="e90e0-195">RS-449</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-196">30</span><span class="sxs-lookup"><span data-stu-id="e90e0-196">30</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-197">V. 35</span><span class="sxs-lookup"><span data-stu-id="e90e0-197">V.35</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-198">31</span><span class="sxs-lookup"><span data-stu-id="e90e0-198">31</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-199">X. 21</span><span class="sxs-lookup"><span data-stu-id="e90e0-199">X.21</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-200">32</span><span class="sxs-lookup"><span data-stu-id="e90e0-200">32</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-201">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="e90e0-201">IEEE-488</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-202">33</span><span class="sxs-lookup"><span data-stu-id="e90e0-202">33</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-203">AUI</span><span class="sxs-lookup"><span data-stu-id="e90e0-203">AUI</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-204">34</span><span class="sxs-lookup"><span data-stu-id="e90e0-204">34</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-205">UTP categoría 3</span><span class="sxs-lookup"><span data-stu-id="e90e0-205">UTP Category 3</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-206">35</span><span class="sxs-lookup"><span data-stu-id="e90e0-206">35</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-207">UTP categoría 4</span><span class="sxs-lookup"><span data-stu-id="e90e0-207">UTP Category 4</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-208">36</span><span class="sxs-lookup"><span data-stu-id="e90e0-208">36</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-209">UTP categoría 5</span><span class="sxs-lookup"><span data-stu-id="e90e0-209">UTP Category 5</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-210">37</span><span class="sxs-lookup"><span data-stu-id="e90e0-210">37</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-211">X</span><span class="sxs-lookup"><span data-stu-id="e90e0-211">BNC</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-212">38</span><span class="sxs-lookup"><span data-stu-id="e90e0-212">38</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-213">RJ11</span><span class="sxs-lookup"><span data-stu-id="e90e0-213">RJ11</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-214">39</span><span class="sxs-lookup"><span data-stu-id="e90e0-214">39</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-215">RJ45</span><span class="sxs-lookup"><span data-stu-id="e90e0-215">RJ45</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-216">40</span><span class="sxs-lookup"><span data-stu-id="e90e0-216">40</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-217">MIC de fibra</span><span class="sxs-lookup"><span data-stu-id="e90e0-217">Fiber MIC</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-218">41</span><span class="sxs-lookup"><span data-stu-id="e90e0-218">41</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-219">AUI de Apple</span><span class="sxs-lookup"><span data-stu-id="e90e0-219">Apple AUI</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-220">42</span><span class="sxs-lookup"><span data-stu-id="e90e0-220">42</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-221">Puerto de Apple</span><span class="sxs-lookup"><span data-stu-id="e90e0-221">Apple GeoPort</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-222">43</span><span class="sxs-lookup"><span data-stu-id="e90e0-222">43</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-223">PCI</span><span class="sxs-lookup"><span data-stu-id="e90e0-223">PCI</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-224">44</span><span class="sxs-lookup"><span data-stu-id="e90e0-224">44</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-225">ISA</span><span class="sxs-lookup"><span data-stu-id="e90e0-225">ISA</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-226">45</span><span class="sxs-lookup"><span data-stu-id="e90e0-226">45</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-227">COMPLEMENTARIA</span><span class="sxs-lookup"><span data-stu-id="e90e0-227">EISA</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-228">46</span><span class="sxs-lookup"><span data-stu-id="e90e0-228">46</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-229">VESA</span><span class="sxs-lookup"><span data-stu-id="e90e0-229">VESA</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-230">47</span><span class="sxs-lookup"><span data-stu-id="e90e0-230">47</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-231">PCMCIA</span><span class="sxs-lookup"><span data-stu-id="e90e0-231">PCMCIA</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-232">48</span><span class="sxs-lookup"><span data-stu-id="e90e0-232">48</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-233">PCMCIA tipo I</span><span class="sxs-lookup"><span data-stu-id="e90e0-233">PCMCIA Type I</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-234">49</span><span class="sxs-lookup"><span data-stu-id="e90e0-234">49</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-235">PCMCIA tipo II</span><span class="sxs-lookup"><span data-stu-id="e90e0-235">PCMCIA Type II</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-236">50</span><span class="sxs-lookup"><span data-stu-id="e90e0-236">50</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-237">PCMCIA tipo III</span><span class="sxs-lookup"><span data-stu-id="e90e0-237">PCMCIA Type III</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-238">51</span><span class="sxs-lookup"><span data-stu-id="e90e0-238">51</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-239">Puerto ZV</span><span class="sxs-lookup"><span data-stu-id="e90e0-239">ZV Port</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-240">52</span><span class="sxs-lookup"><span data-stu-id="e90e0-240">52</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-241">CardBus</span><span class="sxs-lookup"><span data-stu-id="e90e0-241">CardBus</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-242">53</span><span class="sxs-lookup"><span data-stu-id="e90e0-242">53</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-243">USB</span><span class="sxs-lookup"><span data-stu-id="e90e0-243">USB</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-244">54</span><span class="sxs-lookup"><span data-stu-id="e90e0-244">54</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-245">IEEE 1394</span><span class="sxs-lookup"><span data-stu-id="e90e0-245">IEEE 1394</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-246">55</span><span class="sxs-lookup"><span data-stu-id="e90e0-246">55</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-247">HIPPI</span><span class="sxs-lookup"><span data-stu-id="e90e0-247">HIPPI</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-248">56</span><span class="sxs-lookup"><span data-stu-id="e90e0-248">56</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-249">HSSDC (6 clavijas)</span><span class="sxs-lookup"><span data-stu-id="e90e0-249">HSSDC (6 pins)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-250">57</span><span class="sxs-lookup"><span data-stu-id="e90e0-250">57</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-251">GBIC</span><span class="sxs-lookup"><span data-stu-id="e90e0-251">GBIC</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-252">58</span><span class="sxs-lookup"><span data-stu-id="e90e0-252">58</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-253">DIN</span><span class="sxs-lookup"><span data-stu-id="e90e0-253">DIN</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-254">59</span><span class="sxs-lookup"><span data-stu-id="e90e0-254">59</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-255">Mini DIN</span><span class="sxs-lookup"><span data-stu-id="e90e0-255">Mini-DIN</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-256">60</span><span class="sxs-lookup"><span data-stu-id="e90e0-256">60</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-257">Micro DIN</span><span class="sxs-lookup"><span data-stu-id="e90e0-257">Micro-DIN</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-258">61</span><span class="sxs-lookup"><span data-stu-id="e90e0-258">61</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-259">PS/2</span><span class="sxs-lookup"><span data-stu-id="e90e0-259">PS/2</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-260">62</span><span class="sxs-lookup"><span data-stu-id="e90e0-260">62</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-261">Infrarrojos</span><span class="sxs-lookup"><span data-stu-id="e90e0-261">Infrared</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-262">63</span><span class="sxs-lookup"><span data-stu-id="e90e0-262">63</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-263">HP-HIL</span><span class="sxs-lookup"><span data-stu-id="e90e0-263">HP-HIL</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-264">64</span><span class="sxs-lookup"><span data-stu-id="e90e0-264">64</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-265">Acceso a. bus</span><span class="sxs-lookup"><span data-stu-id="e90e0-265">Access.bus</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-266">65</span><span class="sxs-lookup"><span data-stu-id="e90e0-266">65</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-267">NuBus</span><span class="sxs-lookup"><span data-stu-id="e90e0-267">NuBus</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-268">66</span><span class="sxs-lookup"><span data-stu-id="e90e0-268">66</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-269">Centronics</span><span class="sxs-lookup"><span data-stu-id="e90e0-269">Centronics</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-270">67</span><span class="sxs-lookup"><span data-stu-id="e90e0-270">67</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-271">Mini-Centronics</span><span class="sxs-lookup"><span data-stu-id="e90e0-271">Mini-Centronics</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-272">68</span><span class="sxs-lookup"><span data-stu-id="e90e0-272">68</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-273">Tipo de Mini-Centronics-14</span><span class="sxs-lookup"><span data-stu-id="e90e0-273">Mini-Centronics Type-14</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-274">69</span><span class="sxs-lookup"><span data-stu-id="e90e0-274">69</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-275">Tipo de Mini-Centronics-20</span><span class="sxs-lookup"><span data-stu-id="e90e0-275">Mini-Centronics Type-20</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-276">70</span><span class="sxs-lookup"><span data-stu-id="e90e0-276">70</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-277">Tipo de Mini-Centronics-26</span><span class="sxs-lookup"><span data-stu-id="e90e0-277">Mini-Centronics Type-26</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-278">71</span><span class="sxs-lookup"><span data-stu-id="e90e0-278">71</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-279">Mouse de bus</span><span class="sxs-lookup"><span data-stu-id="e90e0-279">Bus Mouse</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-280">72</span><span class="sxs-lookup"><span data-stu-id="e90e0-280">72</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-281">ADB</span><span class="sxs-lookup"><span data-stu-id="e90e0-281">ADB</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-282">73</span><span class="sxs-lookup"><span data-stu-id="e90e0-282">73</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-283">EXPANSIÓN</span><span class="sxs-lookup"><span data-stu-id="e90e0-283">AGP</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-284">74</span><span class="sxs-lookup"><span data-stu-id="e90e0-284">74</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-285">Bus VME</span><span class="sxs-lookup"><span data-stu-id="e90e0-285">VME Bus</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-286">75</span><span class="sxs-lookup"><span data-stu-id="e90e0-286">75</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-287">VME64</span><span class="sxs-lookup"><span data-stu-id="e90e0-287">VME64</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-288">76</span><span class="sxs-lookup"><span data-stu-id="e90e0-288">76</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-289">Propietario</span><span class="sxs-lookup"><span data-stu-id="e90e0-289">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-290">77</span><span class="sxs-lookup"><span data-stu-id="e90e0-290">77</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-291">Ranura de tarjeta del procesador de propiedad</span><span class="sxs-lookup"><span data-stu-id="e90e0-291">Proprietary Processor Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-292">78</span><span class="sxs-lookup"><span data-stu-id="e90e0-292">78</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-293">Ranura de tarjeta de memoria propietaria</span><span class="sxs-lookup"><span data-stu-id="e90e0-293">Proprietary Memory Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-294">79</span><span class="sxs-lookup"><span data-stu-id="e90e0-294">79</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-295">Ranura de aumento de e/s de propiedad</span><span class="sxs-lookup"><span data-stu-id="e90e0-295">Proprietary I/O Riser Slot</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-296">80</span><span class="sxs-lookup"><span data-stu-id="e90e0-296">80</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-297">PCI-66</span><span class="sxs-lookup"><span data-stu-id="e90e0-297">PCI-66MHZ</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-298">81</span><span class="sxs-lookup"><span data-stu-id="e90e0-298">81</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-299">AGP2X</span><span class="sxs-lookup"><span data-stu-id="e90e0-299">AGP2X</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-300">82</span><span class="sxs-lookup"><span data-stu-id="e90e0-300">82</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-301">AGP4X</span><span class="sxs-lookup"><span data-stu-id="e90e0-301">AGP4X</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-302">83</span><span class="sxs-lookup"><span data-stu-id="e90e0-302">83</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-303">PC-98</span><span class="sxs-lookup"><span data-stu-id="e90e0-303">PC-98</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-304">84</span><span class="sxs-lookup"><span data-stu-id="e90e0-304">84</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-305">PC-98-Hireso</span><span class="sxs-lookup"><span data-stu-id="e90e0-305">PC-98-Hireso</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-306">85</span><span class="sxs-lookup"><span data-stu-id="e90e0-306">85</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-307">PC-H98</span><span class="sxs-lookup"><span data-stu-id="e90e0-307">PC-H98</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-308">86</span><span class="sxs-lookup"><span data-stu-id="e90e0-308">86</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-309">PC-98Note</span><span class="sxs-lookup"><span data-stu-id="e90e0-309">PC-98Note</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-310">87</span><span class="sxs-lookup"><span data-stu-id="e90e0-310">87</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-311">PC-98Full</span><span class="sxs-lookup"><span data-stu-id="e90e0-311">PC-98Full</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-312">88</span><span class="sxs-lookup"><span data-stu-id="e90e0-312">88</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-313">SCSI SSA</span><span class="sxs-lookup"><span data-stu-id="e90e0-313">SSA SCSI</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-314">89</span><span class="sxs-lookup"><span data-stu-id="e90e0-314">89</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-315">Circular</span><span class="sxs-lookup"><span data-stu-id="e90e0-315">Circular</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-316">90</span><span class="sxs-lookup"><span data-stu-id="e90e0-316">90</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-317">Conector del IDE de la placa</span><span class="sxs-lookup"><span data-stu-id="e90e0-317">On Board IDE Connector</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-318">91</span><span class="sxs-lookup"><span data-stu-id="e90e0-318">91</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-319">Conector de disquete incorporado</span><span class="sxs-lookup"><span data-stu-id="e90e0-319">On Board Floppy Connector</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-320">92</span><span class="sxs-lookup"><span data-stu-id="e90e0-320">92</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-321">8 pines dual insertado</span><span class="sxs-lookup"><span data-stu-id="e90e0-321">9 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-322">93</span><span class="sxs-lookup"><span data-stu-id="e90e0-322">93</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-323">25 patillas en línea dual</span><span class="sxs-lookup"><span data-stu-id="e90e0-323">25 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-324">94</span><span class="sxs-lookup"><span data-stu-id="e90e0-324">94</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-325">PIN dual de 50 en línea</span><span class="sxs-lookup"><span data-stu-id="e90e0-325">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-326">95</span><span class="sxs-lookup"><span data-stu-id="e90e0-326">95</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-327">PIN dual de 68 en línea</span><span class="sxs-lookup"><span data-stu-id="e90e0-327">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-328">96</span><span class="sxs-lookup"><span data-stu-id="e90e0-328">96</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-329">Conector de sonido de la placa</span><span class="sxs-lookup"><span data-stu-id="e90e0-329">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-330">97</span><span class="sxs-lookup"><span data-stu-id="e90e0-330">97</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-331">Miniconector</span><span class="sxs-lookup"><span data-stu-id="e90e0-331">Mini-jack</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-332">98</span><span class="sxs-lookup"><span data-stu-id="e90e0-332">98</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-333">PCI-X</span><span class="sxs-lookup"><span data-stu-id="e90e0-333">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-334">99</span><span class="sxs-lookup"><span data-stu-id="e90e0-334">99</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-335">SBus IEEE 1396-1993 32 bit</span><span class="sxs-lookup"><span data-stu-id="e90e0-335">Sbus IEEE 1396-1993 32 bit</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-336">100</span><span class="sxs-lookup"><span data-stu-id="e90e0-336">100</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-337">SBus IEEE 1396-1993 64 bit</span><span class="sxs-lookup"><span data-stu-id="e90e0-337">Sbus IEEE 1396-1993 64 bit</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-338">101</span><span class="sxs-lookup"><span data-stu-id="e90e0-338">101</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-339">MCA</span><span class="sxs-lookup"><span data-stu-id="e90e0-339">MCA</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-340">102</span><span class="sxs-lookup"><span data-stu-id="e90e0-340">102</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-341">GIO</span><span class="sxs-lookup"><span data-stu-id="e90e0-341">GIO</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-342">103</span><span class="sxs-lookup"><span data-stu-id="e90e0-342">103</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-343">XIO</span><span class="sxs-lookup"><span data-stu-id="e90e0-343">XIO</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-344">104</span><span class="sxs-lookup"><span data-stu-id="e90e0-344">104</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-345">HIO</span><span class="sxs-lookup"><span data-stu-id="e90e0-345">HIO</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-346">105</span><span class="sxs-lookup"><span data-stu-id="e90e0-346">105</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-347">NGIO</span><span class="sxs-lookup"><span data-stu-id="e90e0-347">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-348">106</span><span class="sxs-lookup"><span data-stu-id="e90e0-348">106</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-349">PMC</span><span class="sxs-lookup"><span data-stu-id="e90e0-349">PMC</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-350">107</span><span class="sxs-lookup"><span data-stu-id="e90e0-350">107</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-351">MTRJ</span><span class="sxs-lookup"><span data-stu-id="e90e0-351">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-352">108</span><span class="sxs-lookup"><span data-stu-id="e90e0-352">108</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-353">VF: 45</span><span class="sxs-lookup"><span data-stu-id="e90e0-353">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-354">109</span><span class="sxs-lookup"><span data-stu-id="e90e0-354">109</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-355">E/s futura</span><span class="sxs-lookup"><span data-stu-id="e90e0-355">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-356">110</span><span class="sxs-lookup"><span data-stu-id="e90e0-356">110</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-357">SC</span><span class="sxs-lookup"><span data-stu-id="e90e0-357">SC</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-358">111</span><span class="sxs-lookup"><span data-stu-id="e90e0-358">111</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-359">SG</span><span class="sxs-lookup"><span data-stu-id="e90e0-359">SG</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-360">112</span><span class="sxs-lookup"><span data-stu-id="e90e0-360">112</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-361">Eléctricos</span><span class="sxs-lookup"><span data-stu-id="e90e0-361">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-362">113</span><span class="sxs-lookup"><span data-stu-id="e90e0-362">113</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-363">Trayecto</span><span class="sxs-lookup"><span data-stu-id="e90e0-363">Optical</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-364">114</span><span class="sxs-lookup"><span data-stu-id="e90e0-364">114</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-365">Cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="e90e0-365">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-366">115</span><span class="sxs-lookup"><span data-stu-id="e90e0-366">115</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-367">GLM</span><span class="sxs-lookup"><span data-stu-id="e90e0-367">GLM</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-368">116</span><span class="sxs-lookup"><span data-stu-id="e90e0-368">116</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-369">1x9</span><span class="sxs-lookup"><span data-stu-id="e90e0-369">1x9</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-370">117</span><span class="sxs-lookup"><span data-stu-id="e90e0-370">117</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-371">SG reducidos</span><span class="sxs-lookup"><span data-stu-id="e90e0-371">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-372">118</span><span class="sxs-lookup"><span data-stu-id="e90e0-372">118</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-373">LC</span><span class="sxs-lookup"><span data-stu-id="e90e0-373">LC</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-374">119</span><span class="sxs-lookup"><span data-stu-id="e90e0-374">119</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-375">HSSC</span><span class="sxs-lookup"><span data-stu-id="e90e0-375">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-376">120</span><span class="sxs-lookup"><span data-stu-id="e90e0-376">120</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-377">VHDCI blindado (68 pines)</span><span class="sxs-lookup"><span data-stu-id="e90e0-377">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-378">121</span><span class="sxs-lookup"><span data-stu-id="e90e0-378">121</span></span>
</dt> <dd>

<span data-ttu-id="e90e0-379">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="e90e0-379">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e90e0-380">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e90e0-380">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-381">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-383">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e90e0-383">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-384">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="e90e0-384">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e90e0-385">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="e90e0-385">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e90e0-386">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-386">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-387">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e90e0-387">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-388">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-390">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="e90e0-390">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-391">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e90e0-391">Textual description of the object.</span></span>

<span data-ttu-id="e90e0-392">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-393">**HeightAllowed**</span><span class="sxs-lookup"><span data-stu-id="e90e0-393">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-394">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="e90e0-394">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-396">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="e90e0-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-397">Alto máximo, en pulgadas, de una tarjeta adaptadora que se puede insertar en la ranura.</span><span class="sxs-lookup"><span data-stu-id="e90e0-397">Maximum height, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-398">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e90e0-398">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-399">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e90e0-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-401">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="e90e0-401">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-402">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="e90e0-402">Date and time the object was installed.</span></span> <span data-ttu-id="e90e0-403">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="e90e0-403">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e90e0-404">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-404">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-405">**LengthAllowed**</span><span class="sxs-lookup"><span data-stu-id="e90e0-405">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-406">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="e90e0-406">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-408">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="e90e0-408">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-409">Longitud máxima, en pulgadas, de una tarjeta adaptadora que se puede insertar en la ranura.</span><span class="sxs-lookup"><span data-stu-id="e90e0-409">Maximum length, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-410">**Le**</span><span class="sxs-lookup"><span data-stu-id="e90e0-410">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-411">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-412">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-413">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e90e0-413">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-414">Organización que generó el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="e90e0-414">Organization that produced the physical element.</span></span> <span data-ttu-id="e90e0-415">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-415">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="e90e0-416">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-416">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-417">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="e90e0-417">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-418">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e90e0-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-420">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ranura del sistema DMTF \| 004,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="e90e0-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-421">Ancho de bus máximo, en bits, de las tarjetas de adaptador que se pueden insertar en la ranura.</span><span class="sxs-lookup"><span data-stu-id="e90e0-421">Maximum bus width, in bits, of adapter cards that can be inserted into the slot.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="e90e0-422">**8** (0)</span><span class="sxs-lookup"><span data-stu-id="e90e0-422">**8** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="e90e0-423">**16** (1)</span><span class="sxs-lookup"><span data-stu-id="e90e0-423">**16** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="e90e0-424">**32** (2)</span><span class="sxs-lookup"><span data-stu-id="e90e0-424">**32** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="64"></span>

<span data-ttu-id="e90e0-425">**64** (3)</span><span class="sxs-lookup"><span data-stu-id="e90e0-425">**64** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="128"></span>

<span data-ttu-id="e90e0-426">**128** (4)</span><span class="sxs-lookup"><span data-stu-id="e90e0-426">**128** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e90e0-427">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="e90e0-427">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-428">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-430">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e90e0-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-431">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="e90e0-431">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="e90e0-432">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-432">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-433">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e90e0-433">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-436">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e90e0-436">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-437">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="e90e0-437">Label by which the object is known.</span></span> <span data-ttu-id="e90e0-438">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="e90e0-438">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e90e0-439">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-440">**Number**</span><span class="sxs-lookup"><span data-stu-id="e90e0-440">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-441">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e90e0-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-442">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-443">Número de ranura física, que se puede utilizar como índice en una tabla de ranuras del sistema, para determinar si la ranura está ocupada físicamente.</span><span class="sxs-lookup"><span data-stu-id="e90e0-443">Physical slot number, which can be used as an index into a system slot table, to determine whether the slot is physically occupied.</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-444">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e90e0-444">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-445">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-447">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="e90e0-447">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="e90e0-448">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="e90e0-448">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="e90e0-449">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="e90e0-449">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="e90e0-450">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-450">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-451">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="e90e0-451">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-452">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-454">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e90e0-454">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-455">Número de pieza asignado por la organización que produjo o fabricó el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="e90e0-455">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="e90e0-456">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-456">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-457">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="e90e0-457">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-458">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e90e0-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-459">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-460">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="e90e0-460">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="e90e0-461">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-461">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-462">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="e90e0-462">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-463">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-464">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-465">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ espacio CIM**.**SpecialPurpose**")</span><span class="sxs-lookup"><span data-stu-id="e90e0-465">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-466">Cadena de forma libre que describe cómo esta ranura es físicamente única y que puede contener tipos especiales de hardware.</span><span class="sxs-lookup"><span data-stu-id="e90e0-466">Free-form string that describes how this slot is physically unique and that it may hold special types of hardware.</span></span> <span data-ttu-id="e90e0-467">Esta propiedad solo tiene significado cuando la propiedad **SpecialPurpose** booleana correspondiente está establecida en **true**.</span><span class="sxs-lookup"><span data-stu-id="e90e0-467">This property only has meaning when the corresponding Boolean **SpecialPurpose** property is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-468">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="e90e0-468">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-469">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-471">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e90e0-471">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-472">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="e90e0-472">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="e90e0-473">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-473">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-474">**SKU**</span><span class="sxs-lookup"><span data-stu-id="e90e0-474">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-475">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-476">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-477">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e90e0-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-478">Número de unidad de almacén para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="e90e0-478">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="e90e0-479">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-479">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-480">**SpecialPurpose**</span><span class="sxs-lookup"><span data-stu-id="e90e0-480">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-481">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e90e0-481">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-482">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-483">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ espacio CIM**.**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="e90e0-483">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-484">Si es **true**, la ranura es físicamente única y puede contener tipos especiales de hardware (por ejemplo, una ranura de procesador de gráficos).</span><span class="sxs-lookup"><span data-stu-id="e90e0-484">If **TRUE**, the slot is physically unique and may hold special types of hardware, (for example, a graphics processor slot).</span></span> <span data-ttu-id="e90e0-485">Si es **true**, la propiedad **PurposeDescription** debe especificar el modo en que la ranura es única o el propósito de la ranura.</span><span class="sxs-lookup"><span data-stu-id="e90e0-485">If **TRUE**, the **PurposeDescription** property should specify how the slot is unique or the slot's purpose.</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-486">**Estado**</span><span class="sxs-lookup"><span data-stu-id="e90e0-486">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-487">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-488">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-489">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e90e0-489">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-490">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e90e0-490">Current status of the object.</span></span> <span data-ttu-id="e90e0-491">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-491">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e90e0-492">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e90e0-492">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e90e0-493">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="e90e0-493">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e90e0-494">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="e90e0-494">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e90e0-495">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="e90e0-495">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e90e0-496">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="e90e0-496">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e90e0-497">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="e90e0-497">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e90e0-498">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="e90e0-498">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e90e0-499">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="e90e0-499">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e90e0-500">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="e90e0-500">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e90e0-501">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="e90e0-501">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e90e0-502">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="e90e0-502">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e90e0-503">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="e90e0-503">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e90e0-504">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="e90e0-504">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e90e0-505">**SupportsHotPlug**</span><span class="sxs-lookup"><span data-stu-id="e90e0-505">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-506">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e90e0-506">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-508">Si **es true**, la ranura admite la conexión en caliente de tarjetas adaptadoras.</span><span class="sxs-lookup"><span data-stu-id="e90e0-508">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-509">**Tag**</span><span class="sxs-lookup"><span data-stu-id="e90e0-509">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-510">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-511">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-512">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e90e0-512">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-513">Cadena arbitraria que identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="e90e0-513">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="e90e0-514">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="e90e0-514">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="e90e0-515">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="e90e0-515">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="e90e0-516">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="e90e0-516">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="e90e0-517">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e90e0-517">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="e90e0-518">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="e90e0-518">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="e90e0-519">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-519">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-520">**ThermalRating**</span><span class="sxs-lookup"><span data-stu-id="e90e0-520">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-521">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e90e0-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-522">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-523">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ranura del sistema DMTF \| 004,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivatios ")</span><span class="sxs-lookup"><span data-stu-id="e90e0-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-524">Disipación térmica máxima de la ranura, en milivatios.</span><span class="sxs-lookup"><span data-stu-id="e90e0-524">Maximum thermal dissipation of the slot, in milliwatts.</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-525">**VccMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="e90e0-525">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-526">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e90e0-526">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-527">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-528">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ranura del sistema DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="e90e0-528">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-529">Voltaje VCC compatible con la ranura.</span><span class="sxs-lookup"><span data-stu-id="e90e0-529">Vcc voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e90e0-530">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e90e0-530">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e90e0-531">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e90e0-531">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="e90e0-532">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="e90e0-532">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="e90e0-533">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="e90e0-533">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e90e0-534">**Versión**</span><span class="sxs-lookup"><span data-stu-id="e90e0-534">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-535">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e90e0-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-536">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-537">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e90e0-537">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-538">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="e90e0-538">Version of the physical element.</span></span>

<span data-ttu-id="e90e0-539">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-539">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90e0-540">**VppMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="e90e0-540">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e90e0-541">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e90e0-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-542">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e90e0-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e90e0-543">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ranura del sistema DMTF \| 004,10 ")</span><span class="sxs-lookup"><span data-stu-id="e90e0-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="e90e0-544">Voltaje Vpp compatible con la ranura.</span><span class="sxs-lookup"><span data-stu-id="e90e0-544">Vpp voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e90e0-545">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e90e0-545">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e90e0-546">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e90e0-546">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="e90e0-547">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="e90e0-547">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="e90e0-548">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="e90e0-548">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="e90e0-549">**12V** (4)</span><span class="sxs-lookup"><span data-stu-id="e90e0-549">**12V** (4)</span></span>


<span data-ttu-id="e90e0-550"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e90e0-550"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e90e0-551">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e90e0-551">Remarks</span></span>

<span data-ttu-id="e90e0-552">La clase de **\_ ranura CIM** se deriva [**de \_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-552">The **CIM\_Slot** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="e90e0-553">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="e90e0-553">WMI does not implement this class.</span></span> <span data-ttu-id="e90e0-554">Para las clases WMI derivadas de la **\_ ranura CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e90e0-554">For WMI classes derived from **CIM\_Slot**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e90e0-555">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="e90e0-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e90e0-556">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="e90e0-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e90e0-557">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e90e0-557">Requirements</span></span>



| <span data-ttu-id="e90e0-558">Requisito</span><span class="sxs-lookup"><span data-stu-id="e90e0-558">Requirement</span></span> | <span data-ttu-id="e90e0-559">Value</span><span class="sxs-lookup"><span data-stu-id="e90e0-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e90e0-560">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e90e0-560">Minimum supported client</span></span><br/> | <span data-ttu-id="e90e0-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e90e0-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e90e0-562">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e90e0-562">Minimum supported server</span></span><br/> | <span data-ttu-id="e90e0-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e90e0-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e90e0-564">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e90e0-564">Namespace</span></span><br/>                | <span data-ttu-id="e90e0-565">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e90e0-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e90e0-566">MOF</span><span class="sxs-lookup"><span data-stu-id="e90e0-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e90e0-567"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e90e0-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e90e0-568">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e90e0-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e90e0-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e90e0-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e90e0-570">Vea también</span><span class="sxs-lookup"><span data-stu-id="e90e0-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90e0-571">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e90e0-571">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> </dl>

 

