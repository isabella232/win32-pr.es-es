---
description: Representa el software de bajo nivel que se carga en el almacenamiento no volátil y que se usa para iniciar y configurar un sistema informático (CIM \_ ComputerSystem).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: CIM_BIOSElement (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669948"
---
# <a name="cim_bioselement-class-hyper-v-management"></a><span data-ttu-id="807da-103">CIM_BIOSElement (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="807da-103">CIM_BIOSElement class (Hyper-V management)</span></span>

<span data-ttu-id="807da-104">Representa el software de bajo nivel que se carga en el almacenamiento no volátil y que se usa para iniciar y configurar un sistema informático ([**CIM \_ ComputerSystem**](cim-computersystem.md)).</span><span class="sxs-lookup"><span data-stu-id="807da-104">Represents the low-level software that is loaded into non-volatile storage and used to start up and configure a computer system ([**CIM\_ComputerSystem**](cim-computersystem.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="807da-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="807da-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a><span data-ttu-id="807da-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="807da-106">Members</span></span>

<span data-ttu-id="807da-107">La clase **CIM \_ BIOSElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="807da-107">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="807da-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="807da-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="807da-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="807da-109">Properties</span></span>

<span data-ttu-id="807da-110">La clase **CIM \_ BIOSElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="807da-110">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="807da-111">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="807da-111">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807da-112">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="807da-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807da-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807da-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="807da-114">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSElement**.**ListOfLanguages**")</span><span class="sxs-lookup"><span data-stu-id="807da-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSElement**.**ListOfLanguages**")</span></span>
</dt> </dl>

<span data-ttu-id="807da-115">Idioma seleccionado actualmente para el BIOS.</span><span class="sxs-lookup"><span data-stu-id="807da-115">The currently selected language for the BIOS.</span></span> <span data-ttu-id="807da-116">Esta información se puede obtener del BIOS de administración del sistema (SMBIOS) mediante el atributo de idioma actual de la estructura de tipo 13 para indizar en la lista de cadenas que sigue a la estructura.</span><span class="sxs-lookup"><span data-stu-id="807da-116">This information can be obtained from the System Management BIOS (SMBIOS) using the Current Language attribute of the Type 13 structure to index into the string list that follows the structure.</span></span> <span data-ttu-id="807da-117">A esta propiedad se le aplica el formato con el nombre de lenguaje ISO 639 y puede ir seguido del nombre del territorio ISO 3166 y el método de codificación.</span><span class="sxs-lookup"><span data-stu-id="807da-117">This property is formatted using the ISO 639 Language Name, and may be followed by the ISO 3166 Territory Name and the encoding method.</span></span>

</dd> <dt>

<span data-ttu-id="807da-118">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="807da-118">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807da-119">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="807da-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="807da-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807da-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="807da-121">Una lista de idiomas instalables para el BIOS.</span><span class="sxs-lookup"><span data-stu-id="807da-121">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="807da-122">Esta información se puede obtener de SMBIOS desde la lista de cadenas que sigue a la estructura de tipo 13.</span><span class="sxs-lookup"><span data-stu-id="807da-122">This information can be obtained from SMBIOS, from the string list that follows the Type 13 structure.</span></span> <span data-ttu-id="807da-123">Se debe usar un nombre de idioma ISO 639 para especificar los idiomas instalables del BIOS.</span><span class="sxs-lookup"><span data-stu-id="807da-123">An ISO 639 Language Name should be used to specify the BIOS' installable languages.</span></span> <span data-ttu-id="807da-124">También se puede especificar el nombre del territorio ISO 3166 y el método de codificación, siguiendo el nombre del idioma.</span><span class="sxs-lookup"><span data-stu-id="807da-124">The ISO 3166 Territory Name and the encoding method may also be specified, following the Language Name.</span></span>

</dd> <dt>

<span data-ttu-id="807da-125">**LoadedEndingAddress**</span><span class="sxs-lookup"><span data-stu-id="807da-125">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807da-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="807da-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="807da-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807da-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="807da-128">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="807da-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="807da-129">Dirección final de la memoria ocupada por el BIOS.</span><span class="sxs-lookup"><span data-stu-id="807da-129">The ending address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="807da-130">**LoadedStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="807da-130">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807da-131">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="807da-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="807da-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807da-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="807da-133">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="807da-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="807da-134">Dirección inicial de la memoria ocupada por el BIOS.</span><span class="sxs-lookup"><span data-stu-id="807da-134">The starting address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="807da-135">**LoadUtilityInformation**</span><span class="sxs-lookup"><span data-stu-id="807da-135">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807da-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="807da-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807da-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807da-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="807da-138">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="807da-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="807da-139">Cadena de forma libre que describe la utilidad Flash/Load de BIOS necesaria para actualizar el objeto **CIM \_ BIOSElement** .</span><span class="sxs-lookup"><span data-stu-id="807da-139">A free form string that describes the BIOS flash/load utility that is required to update the **CIM\_BIOSElement** object.</span></span> <span data-ttu-id="807da-140">En esta propiedad se puede indicar la versión y otra información.</span><span class="sxs-lookup"><span data-stu-id="807da-140">Version and other information may be indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="807da-141">**Le**</span><span class="sxs-lookup"><span data-stu-id="807da-141">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807da-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="807da-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807da-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807da-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="807da-144">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="807da-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="807da-145">Fabricante del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="807da-145">The manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="807da-146">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="807da-146">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807da-147">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="807da-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="807da-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807da-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="807da-149">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="807da-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="807da-150">True si se trata del BIOS principal del equipo; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="807da-150">True if this is the primary BIOS of the computer system; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="807da-151">**RegistryURIs**</span><span class="sxs-lookup"><span data-stu-id="807da-151">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807da-152">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="807da-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="807da-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807da-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="807da-154">La ubicación de publicación de los registros de atributos de BIOS a los que la implementación del BIOS cumple.</span><span class="sxs-lookup"><span data-stu-id="807da-154">The publication location of the BIOS attribute registries to which the BIOS implementation complies.</span></span>

</dd> <dt>

<span data-ttu-id="807da-155">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="807da-155">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807da-156">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="807da-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="807da-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807da-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="807da-158">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="807da-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="807da-159">La fecha en la que se liberó este BIOS.</span><span class="sxs-lookup"><span data-stu-id="807da-159">The Date on which this BIOS was released.</span></span>

</dd> <dt>

<span data-ttu-id="807da-160">**Versión**</span><span class="sxs-lookup"><span data-stu-id="807da-160">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807da-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="807da-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807da-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807da-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="807da-163">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="807da-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="807da-164">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="807da-164">The version of the operation.</span></span> <span data-ttu-id="807da-165">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="807da-165">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="807da-166">*<major>*.*<minor>*.*<revision>*</span><span class="sxs-lookup"><span data-stu-id="807da-166">*<major>*.*<minor>*.*<revision>*</span></span>
-   <span data-ttu-id="807da-167">*<major>*.*<minor><letter><revision>*</span><span class="sxs-lookup"><span data-stu-id="807da-167">*<major>*.*<minor><letter><revision>*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="807da-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="807da-168">Requirements</span></span>



| <span data-ttu-id="807da-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="807da-169">Requirement</span></span> | <span data-ttu-id="807da-170">Value</span><span class="sxs-lookup"><span data-stu-id="807da-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="807da-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="807da-171">Minimum supported client</span></span><br/> | <span data-ttu-id="807da-172">Windows 8</span><span class="sxs-lookup"><span data-stu-id="807da-172">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="807da-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="807da-173">Minimum supported server</span></span><br/> | <span data-ttu-id="807da-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="807da-174">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="807da-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="807da-175">Namespace</span></span><br/>                | <span data-ttu-id="807da-176">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="807da-176">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="807da-177">MOF</span><span class="sxs-lookup"><span data-stu-id="807da-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="807da-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="807da-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="807da-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="807da-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="807da-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="807da-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="807da-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="807da-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="807da-182">**\_SOFTWAREELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="807da-182">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

