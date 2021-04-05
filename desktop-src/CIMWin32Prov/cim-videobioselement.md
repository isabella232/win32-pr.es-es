---
description: La \_ clase CIM VideoBIOSElement representa el software de bajo nivel que se carga en el almacenamiento no volátil y se usa para configurar y tener acceso al controlador de vídeo de un equipo y mostrarlo.
ms.assetid: f23d411f-4781-4727-abd1-61fe1a366bf0
ms.tgt_platform: multiple
title: CIM_VideoBIOSElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSElement
- CIM_VideoBIOSElement.BuildNumber
- CIM_VideoBIOSElement.Caption
- CIM_VideoBIOSElement.CodeSet
- CIM_VideoBIOSElement.Description
- CIM_VideoBIOSElement.IdentificationCode
- CIM_VideoBIOSElement.InstallDate
- CIM_VideoBIOSElement.IsShadowed
- CIM_VideoBIOSElement.LanguageEdition
- CIM_VideoBIOSElement.Manufacturer
- CIM_VideoBIOSElement.Name
- CIM_VideoBIOSElement.OtherTargetOS
- CIM_VideoBIOSElement.SerialNumber
- CIM_VideoBIOSElement.SoftwareElementID
- CIM_VideoBIOSElement.SoftwareElementState
- CIM_VideoBIOSElement.Status
- CIM_VideoBIOSElement.TargetOperatingSystem
- CIM_VideoBIOSElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d873b17f0bf0ea123d988d281c0cab728dd50f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000552"
---
# <a name="cim_videobioselement-class"></a><span data-ttu-id="17690-103">\_Clase VideoBIOSElement de CIM</span><span class="sxs-lookup"><span data-stu-id="17690-103">CIM\_VideoBIOSElement class</span></span>

<span data-ttu-id="17690-104">La clase **CIM \_ VideoBIOSElement** representa el software de bajo nivel que se carga en el almacenamiento no volátil y se usa para configurar y tener acceso al controlador de vídeo de un equipo y mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="17690-104">The **CIM\_VideoBIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17690-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="17690-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="17690-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="17690-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="17690-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="17690-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="17690-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="17690-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17690-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17690-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{76148BF6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_VideoBIOSElement : CIM_SoftwareElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
  boolean  IsShadowed;
  string   LanguageEdition;
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="17690-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="17690-110">Members</span></span>

<span data-ttu-id="17690-111">La clase **CIM \_ VideoBIOSElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="17690-111">The **CIM\_VideoBIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="17690-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17690-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17690-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17690-113">Properties</span></span>

<span data-ttu-id="17690-114">La clase **CIM \_ VideoBIOSElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="17690-114">The **CIM\_VideoBIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17690-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="17690-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-118">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="17690-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="17690-119">Identificador interno de la compilación de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="17690-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="17690-120">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="17690-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-124">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="17690-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="17690-125">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="17690-125">Short textual description of the object.</span></span>

<span data-ttu-id="17690-126">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-127">**Dese**</span><span class="sxs-lookup"><span data-stu-id="17690-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-130">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="17690-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="17690-131">Conjunto de código utilizado por el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="17690-131">Code set used by the software element.</span></span>

<span data-ttu-id="17690-132">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17690-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-136">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="17690-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="17690-137">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="17690-137">Textual description of the object.</span></span>

<span data-ttu-id="17690-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-139">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="17690-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-142">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="17690-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="17690-143">Identificador del fabricante del elemento de software, como una unidad de almacén de cotizaciones o un número de pieza.</span><span class="sxs-lookup"><span data-stu-id="17690-143">Manufacturer's identifier for the software element, such as a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="17690-144">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="17690-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-146">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="17690-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="17690-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="17690-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="17690-149">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="17690-149">Date and time the object was installed.</span></span> <span data-ttu-id="17690-150">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="17690-150">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="17690-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-152">**IsShadowed**</span><span class="sxs-lookup"><span data-stu-id="17690-152">**IsShadowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-153">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="17690-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="17690-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-155">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS de vídeo DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="17690-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="17690-156">Si es **true**, se sombrea el BIOS de vídeo.</span><span class="sxs-lookup"><span data-stu-id="17690-156">If **TRUE**, the video BIOS is shadowed.</span></span>

</dd> <dt>

<span data-ttu-id="17690-157">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="17690-157">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-160">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="17690-160">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="17690-161">Edición de idioma del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="17690-161">Language edition of the software element.</span></span> <span data-ttu-id="17690-162">Se deben usar los códigos de idioma definidos en ISO 639.</span><span class="sxs-lookup"><span data-stu-id="17690-162">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="17690-163">Cuando el elemento software representa una versión multilingüe o internacional de un producto, se debe usar la cadena "multilingüe".</span><span class="sxs-lookup"><span data-stu-id="17690-163">When the software element represents a multilingual or international version of a product, the string "Multilingual" should be used.</span></span>

<span data-ttu-id="17690-164">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-164">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-165">**Le**</span><span class="sxs-lookup"><span data-stu-id="17690-165">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-168">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="17690-168">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="17690-169">Fabricante del elemento de software esta propiedad se hereda de [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-169">Manufacturer of the software element This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-170">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="17690-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-173">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17690-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17690-174">Nombre usado para identificar el elemento de software. esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-174">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-175">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="17690-175">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-178">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="17690-178">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="17690-179">Tipo de fabricante y sistema operativo para un elemento de software cuando la propiedad **TargetOperatingSystem** tiene un valor de 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="17690-179">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="17690-180">Cuando la propiedad **TargetOperatingSystem** tiene un valor de 1, esta propiedad debe tener un valor distinto de NULL.</span><span class="sxs-lookup"><span data-stu-id="17690-180">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="17690-181">Para todos los demás valores de **TargetOperatingSystem** , esta propiedad es NULL.</span><span class="sxs-lookup"><span data-stu-id="17690-181">For all other **TargetOperatingSystem** values, this property is null.</span></span> <span data-ttu-id="17690-182">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-182">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-183">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="17690-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-186">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="17690-186">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="17690-187">Número de serie asignado del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="17690-187">Assigned serial number of the software element.</span></span>

<span data-ttu-id="17690-188">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-188">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-189">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="17690-189">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-192">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17690-192">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17690-193">Identificador del elemento de software que está diseñado para usarse junto con otras claves para crear una representación única de la clase [**\_ SoftwareElement de CIM**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="17690-193">Identifier for the software element that is designed to be used in conjunction with other keys to create a unique representation of the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

<span data-ttu-id="17690-194">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-194">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17690-195">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="17690-195">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-196">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17690-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17690-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-198">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="17690-198">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="17690-199">Estado de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="17690-199">State of a software element.</span></span>

<span data-ttu-id="17690-200">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-200">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="17690-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="17690-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="17690-202">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="17690-202">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="17690-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="17690-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="17690-204">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="17690-204">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="17690-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="17690-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="17690-206">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="17690-206">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="17690-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="17690-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="17690-208">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="17690-208">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="17690-209">**Estado**</span><span class="sxs-lookup"><span data-stu-id="17690-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-212">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="17690-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="17690-213">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="17690-213">Current status of the object.</span></span> <span data-ttu-id="17690-214">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="17690-215">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="17690-215">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="17690-216">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="17690-216">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="17690-217">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="17690-217">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="17690-218">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="17690-218">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="17690-219">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="17690-219">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="17690-220">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="17690-220">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="17690-221">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="17690-221">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="17690-222">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="17690-222">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="17690-223">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="17690-223">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="17690-224">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="17690-224">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="17690-225">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="17690-225">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="17690-226">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="17690-226">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="17690-227">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="17690-227">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="17690-228">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="17690-228">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-229">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17690-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17690-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-231">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información \| del componente de software de DMTF 002,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="17690-231">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="17690-232">Entorno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="17690-232">Operating system environment.</span></span> <span data-ttu-id="17690-233">El valor de esta propiedad no garantiza la ejecución binaria.</span><span class="sxs-lookup"><span data-stu-id="17690-233">The value of this property does not ensure binary execution.</span></span> <span data-ttu-id="17690-234">La versión del sistema operativo debe especificarse mediante la comprobación de la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="17690-234">The version of the operating system must be specified using the operating system version check.</span></span> <span data-ttu-id="17690-235">También se requiere la arquitectura en la que se ejecuta el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="17690-235">Also required is the architecture on which the operating system runs.</span></span> <span data-ttu-id="17690-236">La combinación de estas construcciones permite al proveedor identificar claramente el nivel de sistema operativo necesario para un elemento de software determinado.</span><span class="sxs-lookup"><span data-stu-id="17690-236">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="17690-237">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-237">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="17690-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="17690-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="17690-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="17690-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="17690-240"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="17690-240"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="17690-241">Mac OS</span><span class="sxs-lookup"><span data-stu-id="17690-241">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="17690-242"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="17690-242"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="17690-243">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="17690-243">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="17690-244"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="17690-244"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="17690-245"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="17690-245"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="17690-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="17690-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="17690-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="17690-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="17690-248">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="17690-248">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="17690-249"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="17690-249"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="17690-250">HP-UX</span><span class="sxs-lookup"><span data-stu-id="17690-250">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="17690-251"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="17690-251"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="17690-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="17690-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="17690-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="17690-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="17690-254"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="17690-254"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="17690-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="17690-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="17690-256">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="17690-256">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="17690-257"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="17690-257"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="17690-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="17690-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="17690-259">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="17690-259">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="17690-260"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="17690-260"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="17690-261">Windows 95</span><span class="sxs-lookup"><span data-stu-id="17690-261">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="17690-262"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="17690-262"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="17690-263">Windows 98</span><span class="sxs-lookup"><span data-stu-id="17690-263">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="17690-264"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="17690-264"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="17690-265">Windows NT</span><span class="sxs-lookup"><span data-stu-id="17690-265">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="17690-266"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="17690-266"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="17690-267">Windows CE</span><span class="sxs-lookup"><span data-stu-id="17690-267">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="17690-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="17690-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="17690-269">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="17690-269">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="17690-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="17690-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="17690-271"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="17690-271"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="17690-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="17690-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="17690-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="17690-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="17690-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="17690-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="17690-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="17690-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="17690-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="17690-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="17690-277"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="17690-277"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="17690-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="17690-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="17690-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="17690-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="17690-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="17690-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="17690-281"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="17690-281"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="17690-282">Una serie</span><span class="sxs-lookup"><span data-stu-id="17690-282">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="17690-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="17690-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="17690-284">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="17690-284">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="17690-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="17690-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="17690-286">Tándem</span><span class="sxs-lookup"><span data-stu-id="17690-286">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="17690-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="17690-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="17690-288">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="17690-288">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="17690-289"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="17690-289"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="17690-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="17690-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="17690-291"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="17690-291"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="17690-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="17690-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="17690-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="17690-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="17690-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="17690-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="17690-295">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="17690-295">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="17690-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="17690-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="17690-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="17690-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="17690-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="17690-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="17690-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="17690-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="17690-300">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="17690-300">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="17690-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="17690-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="17690-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="17690-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="17690-303"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="17690-303"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="17690-304"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="17690-304"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="17690-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="17690-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="17690-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="17690-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="17690-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="17690-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="17690-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="17690-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="17690-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="17690-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="17690-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="17690-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="17690-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="17690-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="17690-312">Palm OS</span><span class="sxs-lookup"><span data-stu-id="17690-312">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="17690-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="17690-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="17690-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="17690-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="17690-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="17690-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="17690-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="17690-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="17690-317"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="17690-317"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="17690-318">**Versión**</span><span class="sxs-lookup"><span data-stu-id="17690-318">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17690-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17690-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17690-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17690-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17690-321">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="17690-321">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="17690-322">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="17690-322">Version of the operation.</span></span>

<span data-ttu-id="17690-323">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="17690-323">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="17690-324"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="17690-324"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="17690-325"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="17690-325"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="17690-326">Esta propiedad se hereda de la [**clase \_ SoftwareElement de CIM**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="17690-326">This property is inherited from the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17690-327">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17690-327">Remarks</span></span>

<span data-ttu-id="17690-328">La clase **CIM \_ VideoBIOSElement** se deriva de [**\_ SoftwareElement de CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="17690-328">The **CIM\_VideoBIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="17690-329">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="17690-329">WMI does not implement this class.</span></span>

<span data-ttu-id="17690-330">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="17690-330">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="17690-331">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="17690-331">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="17690-332">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17690-332">Requirements</span></span>



| <span data-ttu-id="17690-333">Requisito</span><span class="sxs-lookup"><span data-stu-id="17690-333">Requirement</span></span> | <span data-ttu-id="17690-334">Value</span><span class="sxs-lookup"><span data-stu-id="17690-334">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17690-335">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17690-335">Minimum supported client</span></span><br/> | <span data-ttu-id="17690-336">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17690-336">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17690-337">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17690-337">Minimum supported server</span></span><br/> | <span data-ttu-id="17690-338">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17690-338">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17690-339">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17690-339">Namespace</span></span><br/>                | <span data-ttu-id="17690-340">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="17690-340">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17690-341">MOF</span><span class="sxs-lookup"><span data-stu-id="17690-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17690-342"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17690-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17690-343">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17690-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17690-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17690-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17690-345">Vea también</span><span class="sxs-lookup"><span data-stu-id="17690-345">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17690-346">**\_SOFTWAREELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="17690-346">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

