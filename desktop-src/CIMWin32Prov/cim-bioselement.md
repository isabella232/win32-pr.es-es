---
description: La \_ clase CIM BIOSElement representa el software de bajo nivel que se carga en el almacenamiento no volátil y que se usa para iniciar y configurar un sistema de equipo.
ms.assetid: c203244a-51e0-4733-a0bc-cf9b7957f364
ms.tgt_platform: multiple
title: CIM_BIOSElement (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Caption
- CIM_BIOSElement.Description
- CIM_BIOSElement.InstallDate
- CIM_BIOSElement.Status
- CIM_BIOSElement.Name
- CIM_BIOSElement.BuildNumber
- CIM_BIOSElement.CodeSet
- CIM_BIOSElement.IdentificationCode
- CIM_BIOSElement.LanguageEdition
- CIM_BIOSElement.OtherTargetOS
- CIM_BIOSElement.SerialNumber
- CIM_BIOSElement.SoftwareElementID
- CIM_BIOSElement.SoftwareElementState
- CIM_BIOSElement.TargetOperatingSystem
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.Version
- CIM_BIOSElement.PrimaryBIOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21cd0d13d62f5cfa70f579110480b4c11c36b77d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080240"
---
# <a name="cim_bioselement-class-cimwin32-wmi-providers"></a><span data-ttu-id="f0a38-103">CIM_BIOSElement (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="f0a38-103">CIM_BIOSElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="f0a38-104">La clase **CIM \_ BIOSElement** representa el software de bajo nivel que se carga en el almacenamiento no volátil y que se usa para iniciar y configurar un sistema de equipo.</span><span class="sxs-lookup"><span data-stu-id="f0a38-104">The **CIM\_BIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0a38-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f0a38-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f0a38-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f0a38-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f0a38-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f0a38-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f0a38-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f0a38-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a38-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0a38-109">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C562-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  string   BuildNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  uint16   TargetOperatingSystem;
  string   Manufacturer;
  string   Version;
  boolean  PrimaryBIOS;
};
```

## <a name="members"></a><span data-ttu-id="f0a38-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0a38-110">Members</span></span>

<span data-ttu-id="f0a38-111">La clase **CIM \_ BIOSElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f0a38-111">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="f0a38-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0a38-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0a38-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0a38-113">Properties</span></span>

<span data-ttu-id="f0a38-114">La clase **CIM \_ BIOSElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f0a38-114">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0a38-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="f0a38-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-118">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="f0a38-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-119">Identificador interno de la compilación de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="f0a38-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="f0a38-120">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f0a38-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-124">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f0a38-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-125">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f0a38-125">A short textual description of the object.</span></span>

<span data-ttu-id="f0a38-126">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-127">**Dese**</span><span class="sxs-lookup"><span data-stu-id="f0a38-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-130">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f0a38-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-131">Conjunto de código utilizado por el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="f0a38-131">Code set used by the software element.</span></span>

<span data-ttu-id="f0a38-132">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0a38-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-136">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="f0a38-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-137">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f0a38-137">A textual description of the object.</span></span>

<span data-ttu-id="f0a38-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-139">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="f0a38-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-142">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="f0a38-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-143">Identificador del fabricante para el elemento de software, a menudo una referencia de almacén (SKU) o un número de pieza.</span><span class="sxs-lookup"><span data-stu-id="f0a38-143">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="f0a38-144">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f0a38-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-146">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a38-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="f0a38-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-149">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="f0a38-149">Indicates when the object was installed.</span></span> <span data-ttu-id="f0a38-150">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="f0a38-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f0a38-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-152">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="f0a38-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-155">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="f0a38-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-156">Edición de idioma del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="f0a38-156">Language edition of the software element.</span></span> <span data-ttu-id="f0a38-157">Se deben usar los códigos de idioma definidos en ISO 639.</span><span class="sxs-lookup"><span data-stu-id="f0a38-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="f0a38-158">Cuando el elemento de software representa versiones multilingües o internacionales de un producto, se debe usar la cadena "multilingüe".</span><span class="sxs-lookup"><span data-stu-id="f0a38-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="f0a38-159">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-159">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-160">**Le**</span><span class="sxs-lookup"><span data-stu-id="f0a38-160">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-163">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="f0a38-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-164">Fabricante del BIOS.</span><span class="sxs-lookup"><span data-stu-id="f0a38-164">The manufacturer of the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-165">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f0a38-165">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-168">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f0a38-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-169">Nombre usado para identificar este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="f0a38-169">The name used to identify this software element</span></span>

<span data-ttu-id="f0a38-170">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-170">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-171">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="f0a38-171">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-174">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="f0a38-174">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-175">Tipo de fabricante y sistema operativo para un elemento de software cuando la propiedad **TargetOperatingSystem** tiene un valor de 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="f0a38-175">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="f0a38-176">Cuando la propiedad **TargetOperatingSystem** tiene un valor de 1, esta propiedad debe tener un valor distinto de NULL.</span><span class="sxs-lookup"><span data-stu-id="f0a38-176">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="f0a38-177">Para todos los demás valores de **TargetOperatingSystem** , esta propiedad es NULL.</span><span class="sxs-lookup"><span data-stu-id="f0a38-177">For all other **TargetOperatingSystem** values, this property is null.</span></span>

<span data-ttu-id="f0a38-178">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-178">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-179">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="f0a38-179">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-180">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f0a38-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-182">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="f0a38-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-183">Si es **true**, se trata del BIOS principal del equipo.</span><span class="sxs-lookup"><span data-stu-id="f0a38-183">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-184">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="f0a38-184">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-187">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="f0a38-187">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-188">Número de serie del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="f0a38-188">Serial number of the software element.</span></span>

<span data-ttu-id="f0a38-189">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-189">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-190">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="f0a38-190">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-193">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f0a38-193">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-194">Identificador del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="f0a38-194">Identifier for the software element.</span></span> <span data-ttu-id="f0a38-195">Está diseñado para usarse junto con otras claves para crear una representación única de este [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-195">It is designed to be used in conjunction with other keys to create a unique representation of this [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="f0a38-196">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-196">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a38-197">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="f0a38-197">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-198">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a38-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-200">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0a38-200">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-201">Estado de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="f0a38-201">State of a software element.</span></span>

<span data-ttu-id="f0a38-202">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-202">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="f0a38-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="f0a38-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-204">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="f0a38-204">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="f0a38-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a38-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-206">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="f0a38-206">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="f0a38-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a38-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-208">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="f0a38-208">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="f0a38-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="f0a38-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-210">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="f0a38-210">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f0a38-211">**Estado**</span><span class="sxs-lookup"><span data-stu-id="f0a38-211">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-212">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-214">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f0a38-214">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-215">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f0a38-215">String that indicates the current status of the object.</span></span> <span data-ttu-id="f0a38-216">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="f0a38-216">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f0a38-217">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="f0a38-217">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f0a38-218">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="f0a38-218">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f0a38-219">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="f0a38-219">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f0a38-220">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="f0a38-220">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f0a38-221">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="f0a38-221">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f0a38-222">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f0a38-223">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f0a38-223">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f0a38-224">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="f0a38-224">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f0a38-225">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="f0a38-225">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f0a38-226">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f0a38-226">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f0a38-227">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="f0a38-227">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f0a38-228">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="f0a38-228">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f0a38-229">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="f0a38-229">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f0a38-230">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="f0a38-230">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f0a38-231">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="f0a38-231">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f0a38-232">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="f0a38-232">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f0a38-233">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f0a38-233">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f0a38-234">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="f0a38-234">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f0a38-235">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="f0a38-235">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f0a38-236">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="f0a38-236">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-237">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a38-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-239">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información \| del componente de software de DMTF 002,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="f0a38-239">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-240">Entorno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f0a38-240">Operating system environment.</span></span> <span data-ttu-id="f0a38-241">El valor de esta propiedad no garantiza la ejecución binaria, se necesita más información.</span><span class="sxs-lookup"><span data-stu-id="f0a38-241">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="f0a38-242">La versión del sistema operativo debe especificarse mediante la comprobación de la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f0a38-242">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="f0a38-243">También es necesario, es la arquitectura en la que se ejecuta el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f0a38-243">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="f0a38-244">La combinación de estas construcciones permite al proveedor identificar claramente el nivel de sistema operativo necesario para un elemento de software determinado.</span><span class="sxs-lookup"><span data-stu-id="f0a38-244">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="f0a38-245">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-245">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f0a38-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f0a38-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f0a38-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a38-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="f0a38-248"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a38-248"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-249">Mac OS</span><span class="sxs-lookup"><span data-stu-id="f0a38-249">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="f0a38-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="f0a38-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-251">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="f0a38-251">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="f0a38-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="f0a38-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="f0a38-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="f0a38-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="f0a38-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="f0a38-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="f0a38-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="f0a38-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-256">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="f0a38-256">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="f0a38-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="f0a38-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-258">HP-UX</span><span class="sxs-lookup"><span data-stu-id="f0a38-258">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="f0a38-259"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="f0a38-259"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="f0a38-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="f0a38-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="f0a38-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="f0a38-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="f0a38-262"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="f0a38-262"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="f0a38-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="f0a38-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-264">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="f0a38-264">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="f0a38-265"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="f0a38-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="f0a38-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="f0a38-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-267">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="f0a38-267">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="f0a38-268"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="f0a38-268"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-269">Windows 95</span><span class="sxs-lookup"><span data-stu-id="f0a38-269">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="f0a38-270"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="f0a38-270"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-271">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f0a38-271">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="f0a38-272"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="f0a38-272"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-273">Windows NT</span><span class="sxs-lookup"><span data-stu-id="f0a38-273">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="f0a38-274"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="f0a38-274"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-275">Windows CE</span><span class="sxs-lookup"><span data-stu-id="f0a38-275">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="f0a38-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="f0a38-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-277">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="f0a38-277">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="f0a38-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="f0a38-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="f0a38-279"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="f0a38-279"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="f0a38-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="f0a38-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="f0a38-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="f0a38-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="f0a38-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="f0a38-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="f0a38-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="f0a38-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="f0a38-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="f0a38-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="f0a38-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="f0a38-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="f0a38-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="f0a38-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="f0a38-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="f0a38-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="f0a38-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="f0a38-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="f0a38-289"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="f0a38-289"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-290">Una serie</span><span class="sxs-lookup"><span data-stu-id="f0a38-290">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="f0a38-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="f0a38-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-292">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="f0a38-292">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="f0a38-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="f0a38-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-294">Tándem</span><span class="sxs-lookup"><span data-stu-id="f0a38-294">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="f0a38-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="f0a38-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-296">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="f0a38-296">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="f0a38-297"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="f0a38-297"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="f0a38-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="f0a38-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="f0a38-299"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="f0a38-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="f0a38-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="f0a38-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="f0a38-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="f0a38-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="f0a38-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="f0a38-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-303">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="f0a38-303">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="f0a38-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="f0a38-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="f0a38-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="f0a38-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="f0a38-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="f0a38-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="f0a38-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="f0a38-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-308">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="f0a38-308">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="f0a38-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="f0a38-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="f0a38-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="f0a38-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="f0a38-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="f0a38-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="f0a38-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="f0a38-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="f0a38-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="f0a38-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="f0a38-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="f0a38-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="f0a38-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="f0a38-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="f0a38-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="f0a38-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="f0a38-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="f0a38-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="f0a38-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="f0a38-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="f0a38-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="f0a38-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="f0a38-320">Palm OS</span><span class="sxs-lookup"><span data-stu-id="f0a38-320">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="f0a38-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="f0a38-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="f0a38-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="f0a38-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="f0a38-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="f0a38-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="f0a38-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="f0a38-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="f0a38-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="f0a38-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f0a38-326">**Versión**</span><span class="sxs-lookup"><span data-stu-id="f0a38-326">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a38-327">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a38-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a38-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a38-329">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="f0a38-329">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f0a38-330">Versión del BIOS.</span><span class="sxs-lookup"><span data-stu-id="f0a38-330">The version of the BIOS.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0a38-331">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0a38-331">Remarks</span></span>

<span data-ttu-id="f0a38-332">La clase **CIM \_ BIOSElement** se deriva de [**\_ SoftwareElement de CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-332">The **CIM\_BIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="f0a38-333">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="f0a38-333">WMI does not implement this class.</span></span> <span data-ttu-id="f0a38-334">Para obtener más información sobre las clases derivadas de **CIM \_ BIOSElement**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f0a38-334">For more information about classes derived from **CIM\_BIOSElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f0a38-335">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f0a38-335">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f0a38-336">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f0a38-336">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0a38-337">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0a38-337">Requirements</span></span>



| <span data-ttu-id="f0a38-338">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0a38-338">Requirement</span></span> | <span data-ttu-id="f0a38-339">Value</span><span class="sxs-lookup"><span data-stu-id="f0a38-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a38-340">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0a38-340">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a38-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0a38-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f0a38-342">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0a38-342">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a38-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0a38-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f0a38-344">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0a38-344">Namespace</span></span><br/>                | <span data-ttu-id="f0a38-345">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f0a38-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f0a38-346">MOF</span><span class="sxs-lookup"><span data-stu-id="f0a38-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0a38-347"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0a38-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0a38-348">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0a38-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0a38-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0a38-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0a38-350">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0a38-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a38-351">**\_SOFTWAREELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="f0a38-351">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

