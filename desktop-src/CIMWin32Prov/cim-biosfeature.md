---
description: Representa las capacidades del software de bajo nivel que se usa para iniciar y configurar un sistema de equipo.
ms.assetid: 54d03539-d908-4571-b8fd-934b972e8d84
ms.tgt_platform: multiple
title: CIM_BIOSFeature (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeature
- CIM_BIOSFeature.Caption
- CIM_BIOSFeature.Description
- CIM_BIOSFeature.InstallDate
- CIM_BIOSFeature.Status
- CIM_BIOSFeature.IdentifyingNumber
- CIM_BIOSFeature.ProductName
- CIM_BIOSFeature.Vendor
- CIM_BIOSFeature.Version
- CIM_BIOSFeature.Name
- CIM_BIOSFeature.CharacteristicDescriptions
- CIM_BIOSFeature.Characteristics
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 538dc9e4c18d976901519ae0e2d6f5249fd25c35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907374"
---
# <a name="cim_biosfeature-class"></a><span data-ttu-id="6277a-103">\_Clase BIOSFeature de CIM</span><span class="sxs-lookup"><span data-stu-id="6277a-103">CIM\_BIOSFeature class</span></span>

<span data-ttu-id="6277a-104">La clase **CIM \_ BIOSFeature** representa las capacidades del software de bajo nivel que se usa para iniciar y configurar un sistema de equipo.</span><span class="sxs-lookup"><span data-stu-id="6277a-104">The **CIM\_BIOSFeature** class represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6277a-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="6277a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6277a-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6277a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6277a-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6277a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6277a-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6277a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6277a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6277a-109">Syntax</span></span>

``` syntax
[UUID("{7D33100E-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   IdentifyingNumber;
  string   ProductName;
  string   Vendor;
  string   Version;
  string   Name;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="6277a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="6277a-110">Members</span></span>

<span data-ttu-id="6277a-111">La clase **CIM \_ BIOSFeature** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6277a-111">The **CIM\_BIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="6277a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6277a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6277a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6277a-113">Properties</span></span>

<span data-ttu-id="6277a-114">La clase **CIM \_ BIOSFeature** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6277a-114">The **CIM\_BIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6277a-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6277a-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6277a-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6277a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6277a-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6277a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6277a-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6277a-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6277a-119">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6277a-119">A short textual description of the object.</span></span>

<span data-ttu-id="6277a-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6277a-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6277a-121">**CharacteristicDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6277a-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6277a-122">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="6277a-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6277a-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6277a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6277a-124">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Característica BIOS \| de DMTF 003,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**.**Características**")</span><span class="sxs-lookup"><span data-stu-id="6277a-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="6277a-125">Matriz de cadenas de formato libre que proporciona explicaciones detalladas de las características del BIOS indicadas en la matriz de **características** .</span><span class="sxs-lookup"><span data-stu-id="6277a-125">Array of free-form strings that provides detailed explanations of the BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="6277a-126">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **características** , que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="6277a-126">Each entry in this array is related to the entry in the **Characteristics** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="6277a-127">**Características**</span><span class="sxs-lookup"><span data-stu-id="6277a-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6277a-128">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6277a-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6277a-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6277a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6277a-130">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Característica BIOS \| de DMTF 003,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**.**CharacteristicDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="6277a-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="6277a-131">Matriz de enteros que especifica las características admitidas por el BIOS.</span><span class="sxs-lookup"><span data-stu-id="6277a-131">Array of integers that specifies the features supported by the BIOS.</span></span> <span data-ttu-id="6277a-132">El valor 3 no es válido en el esquema CIM porque representa que no se admiten características del BIOS en DMI.</span><span class="sxs-lookup"><span data-stu-id="6277a-132">The value 3 is not valid in the CIM schema because it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="6277a-133">En ese caso, no se deben crear instancias de este objeto.</span><span class="sxs-lookup"><span data-stu-id="6277a-133">In which case, this object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6277a-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="6277a-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-135">Otros.</span><span class="sxs-lookup"><span data-stu-id="6277a-135">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6277a-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="6277a-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-137">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="6277a-137">Unknown.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="6277a-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (3)</span><span class="sxs-lookup"><span data-stu-id="6277a-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-139">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="6277a-139">Undefined.</span></span>

</dd> <dt>

<span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>

<span data-ttu-id="6277a-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**Compatibilidad con ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="6277a-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**ISA Support** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-141">Compatibilidad con ISA.</span><span class="sxs-lookup"><span data-stu-id="6277a-141">ISA support.</span></span>

</dd> <dt>

<span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>

<span data-ttu-id="6277a-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**Compatibilidad con MCA** (5)</span><span class="sxs-lookup"><span data-stu-id="6277a-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**MCA Support** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-143">Compatibilidad con MCA.</span><span class="sxs-lookup"><span data-stu-id="6277a-143">MCA support.</span></span>

</dd> <dt>

<span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>

<span data-ttu-id="6277a-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**Compatibilidad con EISA** (6)</span><span class="sxs-lookup"><span data-stu-id="6277a-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**EISA Support** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-145">Compatibilidad con EISA.</span><span class="sxs-lookup"><span data-stu-id="6277a-145">EISA support.</span></span>

</dd> <dt>

<span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>

<span data-ttu-id="6277a-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**Compatibilidad con PCI** (7)</span><span class="sxs-lookup"><span data-stu-id="6277a-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**PCI Support** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-147">Compatibilidad con PCI.</span><span class="sxs-lookup"><span data-stu-id="6277a-147">PCI support.</span></span>

</dd> <dt>

<span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>

<span data-ttu-id="6277a-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**Compatibilidad con PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="6277a-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**PCMCIA Support** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-149">Compatibilidad con PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="6277a-149">PCMCIA support.</span></span>

</dd> <dt>

<span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>

<span data-ttu-id="6277a-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**Compatibilidad con PNP** (9)</span><span class="sxs-lookup"><span data-stu-id="6277a-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**PnP Support** (9)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-151">Compatibilidad con PnP.</span><span class="sxs-lookup"><span data-stu-id="6277a-151">PnP support.</span></span>

</dd> <dt>

<span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>

<span data-ttu-id="6277a-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**Compatibilidad con APM** (10)</span><span class="sxs-lookup"><span data-stu-id="6277a-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**APM Support** (10)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-153">Compatibilidad con APM.</span><span class="sxs-lookup"><span data-stu-id="6277a-153">APM support.</span></span>

</dd> <dt>

<span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>

<span data-ttu-id="6277a-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**BIOS actualizable** (11)</span><span class="sxs-lookup"><span data-stu-id="6277a-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**Upgradeable BIOS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-155">BIOS actualizable.</span><span class="sxs-lookup"><span data-stu-id="6277a-155">Upgradeable BIOS.</span></span>

</dd> <dt>

<span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="6277a-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**Sombra del BIOS permitida** (12)</span><span class="sxs-lookup"><span data-stu-id="6277a-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**BIOS Shadowing Allowed** (12)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-157">Sombra del BIOS permitida.</span><span class="sxs-lookup"><span data-stu-id="6277a-157">BIOS shadowing allowed.</span></span>

</dd> <dt>

<span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>

<span data-ttu-id="6277a-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**Compatibilidad con VESA de VL** (13)</span><span class="sxs-lookup"><span data-stu-id="6277a-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**VL VESA Support** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-159">Compatibilidad con VESA de VL.</span><span class="sxs-lookup"><span data-stu-id="6277a-159">VL VESA support.</span></span>

</dd> <dt>

<span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>

<span data-ttu-id="6277a-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**Compatibilidad con ESCD** (14)</span><span class="sxs-lookup"><span data-stu-id="6277a-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**ESCD Support** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-161">Compatibilidad con ESCD.</span><span class="sxs-lookup"><span data-stu-id="6277a-161">ESCD support.</span></span>

</dd> <dt>

<span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>

<span data-ttu-id="6277a-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**Compatibilidad con LS-120** (15)</span><span class="sxs-lookup"><span data-stu-id="6277a-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**LS-120 Support** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-163">Compatibilidad con LS-120.</span><span class="sxs-lookup"><span data-stu-id="6277a-163">LS-120 support.</span></span>

</dd> <dt>

<span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>

<span data-ttu-id="6277a-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**Compatibilidad con ACPI** (16)</span><span class="sxs-lookup"><span data-stu-id="6277a-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**ACPI Support** (16)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-165">Compatibilidad con ACPI.</span><span class="sxs-lookup"><span data-stu-id="6277a-165">ACPI support.</span></span>

</dd> <dt>

<span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>

<span data-ttu-id="6277a-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**Compatibilidad con el arranque de I2O** (17)</span><span class="sxs-lookup"><span data-stu-id="6277a-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**I2O Boot Support** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-167">Compatibilidad con el arranque de I2O.</span><span class="sxs-lookup"><span data-stu-id="6277a-167">I2O boot support.</span></span>

</dd> <dt>

<span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>

<span data-ttu-id="6277a-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**Compatibilidad con USB Legacy** (18)</span><span class="sxs-lookup"><span data-stu-id="6277a-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**USB Legacy Support** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-169">Compatibilidad con USB Legacy.</span><span class="sxs-lookup"><span data-stu-id="6277a-169">USB legacy support.</span></span>

</dd> <dt>

<span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>

<span data-ttu-id="6277a-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**Compatibilidad con AGP** (19)</span><span class="sxs-lookup"><span data-stu-id="6277a-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**AGP Support** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-171">Compatibilidad con AGP.</span><span class="sxs-lookup"><span data-stu-id="6277a-171">AGP support.</span></span>

</dd> <dt>

<span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>

<span data-ttu-id="6277a-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**PC Card** (20)</span><span class="sxs-lookup"><span data-stu-id="6277a-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**PC Card** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-173">Tarjeta PC.</span><span class="sxs-lookup"><span data-stu-id="6277a-173">PC card.</span></span>

</dd> <dt>

<span id="IR"></span><span id="ir"></span>

<span data-ttu-id="6277a-174"><span id="IR"></span><span id="ir"></span>**Ir** (21)</span><span class="sxs-lookup"><span data-stu-id="6277a-174"><span id="IR"></span><span id="ir"></span>**IR** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-175">Distancia.</span><span class="sxs-lookup"><span data-stu-id="6277a-175">IR.</span></span>

</dd> <dt>

<span id="1394"></span>

<span data-ttu-id="6277a-176"><span id="1394"></span>**1394** (22)</span><span class="sxs-lookup"><span data-stu-id="6277a-176"><span id="1394"></span>**1394** (22)</span></span>


</dt> <dd>

1394.

</dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="6277a-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span><span class="sxs-lookup"><span data-stu-id="6277a-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-178">I2C.</span><span class="sxs-lookup"><span data-stu-id="6277a-178">I2C.</span></span>

</dd> <dt>

<span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>

<span data-ttu-id="6277a-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Batería inteligente** (24)</span><span class="sxs-lookup"><span data-stu-id="6277a-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Smart Battery** (24)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-180">Batería inteligente.</span><span class="sxs-lookup"><span data-stu-id="6277a-180">Smart battery.</span></span>

</dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="6277a-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="6277a-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>


</dt> <dd>

<span data-ttu-id="6277a-182">PC-98.</span><span class="sxs-lookup"><span data-stu-id="6277a-182">PC-98.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6277a-183">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6277a-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6277a-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6277a-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6277a-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6277a-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6277a-186">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="6277a-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6277a-187">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6277a-187">A textual description of the object.</span></span>

<span data-ttu-id="6277a-188">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6277a-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6277a-189">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="6277a-189">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6277a-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6277a-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6277a-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6277a-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6277a-192">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**IdentifyingNumber**"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="6277a-192">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="6277a-193">Identificación del producto, como un número de serie en software o un número de matriz en un chip de hardware.</span><span class="sxs-lookup"><span data-stu-id="6277a-193">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

<span data-ttu-id="6277a-194">Esta propiedad se hereda de [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="6277a-194">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="6277a-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6277a-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6277a-196">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6277a-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6277a-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6277a-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6277a-198">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="6277a-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6277a-199">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="6277a-199">Indicates when the object was installed.</span></span> <span data-ttu-id="6277a-200">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="6277a-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6277a-201">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6277a-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6277a-202">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="6277a-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6277a-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6277a-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6277a-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6277a-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6277a-205">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6277a-205">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6277a-206">La propiedad Name define la etiqueta por la que el objeto es conocido para el mundo fuera del sistema de procesamiento de datos.</span><span class="sxs-lookup"><span data-stu-id="6277a-206">The Name property defines the label by which the object is known to the world outside the data processing system.</span></span> <span data-ttu-id="6277a-207">Esta etiqueta es un nombre legible que identifica de forma única el elemento en el contexto del espacio de nombres del elemento.</span><span class="sxs-lookup"><span data-stu-id="6277a-207">This label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="6277a-208">Esta propiedad se hereda de [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="6277a-208">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="6277a-209">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="6277a-209">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6277a-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6277a-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6277a-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6277a-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6277a-212">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**Name**"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="6277a-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="6277a-213">Nombre de producto usado comúnmente.</span><span class="sxs-lookup"><span data-stu-id="6277a-213">Commonly used product name.</span></span>

<span data-ttu-id="6277a-214">Esta propiedad se hereda de [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="6277a-214">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="6277a-215">**Estado**</span><span class="sxs-lookup"><span data-stu-id="6277a-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6277a-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6277a-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6277a-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6277a-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6277a-218">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="6277a-218">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6277a-219">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6277a-219">String that indicates the current status of the object.</span></span> <span data-ttu-id="6277a-220">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="6277a-220">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6277a-221">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="6277a-221">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6277a-222">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="6277a-222">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6277a-223">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="6277a-223">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6277a-224">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="6277a-224">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6277a-225">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="6277a-225">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6277a-226">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6277a-226">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6277a-227">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6277a-227">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6277a-228">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="6277a-228">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6277a-229">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="6277a-229">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6277a-230">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="6277a-230">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6277a-231">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="6277a-231">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6277a-232">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="6277a-232">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6277a-233">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="6277a-233">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6277a-234">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="6277a-234">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6277a-235">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="6277a-235">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6277a-236">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="6277a-236">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6277a-237">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="6277a-237">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6277a-238">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="6277a-238">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6277a-239">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="6277a-239">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6277a-240">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="6277a-240">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6277a-241">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6277a-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6277a-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6277a-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6277a-243">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**Vendor**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="6277a-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="6277a-244">Nombre del proveedor del producto, que corresponde a la propiedad **Vendor** en el objeto Product del estándar de intercambio de soluciones DMTF.</span><span class="sxs-lookup"><span data-stu-id="6277a-244">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="6277a-245">Esta propiedad se hereda de [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="6277a-245">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="6277a-246">**Versión**</span><span class="sxs-lookup"><span data-stu-id="6277a-246">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6277a-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6277a-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6277a-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6277a-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6277a-249">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**Versión**"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="6277a-249">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="6277a-250">Información de versión del producto, que corresponde a la propiedad **version** en el objeto Product del estándar de intercambio de soluciones DMTF.</span><span class="sxs-lookup"><span data-stu-id="6277a-250">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="6277a-251">Esta propiedad se hereda de [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="6277a-251">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6277a-252">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6277a-252">Remarks</span></span>

<span data-ttu-id="6277a-253">La clase **CIM \_ BIOSFeature** se deriva de [**\_ SoftwareFeature de CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="6277a-253">The **CIM\_BIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="6277a-254">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="6277a-254">WMI does not implement this class.</span></span>

<span data-ttu-id="6277a-255">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="6277a-255">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6277a-256">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="6277a-256">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6277a-257">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6277a-257">Requirements</span></span>



| <span data-ttu-id="6277a-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="6277a-258">Requirement</span></span> | <span data-ttu-id="6277a-259">Value</span><span class="sxs-lookup"><span data-stu-id="6277a-259">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6277a-260">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6277a-260">Minimum supported client</span></span><br/> | <span data-ttu-id="6277a-261">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6277a-261">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6277a-262">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6277a-262">Minimum supported server</span></span><br/> | <span data-ttu-id="6277a-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6277a-263">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6277a-264">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6277a-264">Namespace</span></span><br/>                | <span data-ttu-id="6277a-265">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6277a-265">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6277a-266">MOF</span><span class="sxs-lookup"><span data-stu-id="6277a-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6277a-267"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6277a-267"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6277a-268">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6277a-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6277a-269"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6277a-269"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6277a-270">Vea también</span><span class="sxs-lookup"><span data-stu-id="6277a-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6277a-271">**\_SOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="6277a-271">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

