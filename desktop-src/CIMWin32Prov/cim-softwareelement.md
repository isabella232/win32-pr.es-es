---
description: La \_ clase SoftwareElement de CIM descompone un \_ objeto SOFTWAREFEATURE de CIM en un conjunto de elementos que se pueden administrar o implementar individualmente para una plataforma determinada.
ms.assetid: b2418735-b738-411a-a620-acc31662f824
ms.tgt_platform: multiple
title: CIM_SoftwareElement (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.Caption
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.Description
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.InstallDate
- CIM_SoftwareElement.LanguageEdition
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.Status
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fbe64ddfcf81a7410f5654db89c2924a8eabacc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153153"
---
# <a name="cim_softwareelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="dc13c-103">CIM_SoftwareElement (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="dc13c-103">CIM_SoftwareElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="dc13c-104">La **clase \_ SoftwareElement de CIM** descompone un [**objeto \_ SoftwareFeature de CIM**](cim-softwarefeature.md) en un conjunto de elementos que se pueden administrar o implementar individualmente para una plataforma determinada.</span><span class="sxs-lookup"><span data-stu-id="dc13c-104">The **CIM\_SoftwareElement** class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="dc13c-105">La plataforma de un elemento de software está identificada de forma exclusiva por su sistema operativo y la arquitectura de hardware subyacente.</span><span class="sxs-lookup"><span data-stu-id="dc13c-105">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

<span data-ttu-id="dc13c-106">Por lo tanto, para comprender los detalles de cómo se proporciona la funcionalidad de una característica de software determinada en una plataforma determinada, los objetos **\_ SoftwareElement de CIM** a los que hacen referencia las asociaciones de [**\_ SoftwareFeatureSoftwareElements de CIM**](cim-softwarefeaturesoftwareelements.md) se organizan en conjuntos disjuntos basados en la propiedad **TargetOperatingSystem** .</span><span class="sxs-lookup"><span data-stu-id="dc13c-106">As such, to understand the details of how the functionality of a particular software feature is provided on a particular platform, the **CIM\_SoftwareElement** objects referenced by [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) associations are organized in disjoint sets based on the **TargetOperatingSystem** property.</span></span> <span data-ttu-id="dc13c-107">Un **objeto \_ SoftwareElement de CIM** captura los detalles de administración de un elemento o componente en uno de cuatro estados caracterizados por la propiedad **SoftwareElementState** .</span><span class="sxs-lookup"><span data-stu-id="dc13c-107">A **CIM\_SoftwareElement** object captures the management details of a part or component in one of four states characterized by the **SoftwareElementState** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc13c-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="dc13c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dc13c-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dc13c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dc13c-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="dc13c-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dc13c-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="dc13c-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc13c-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc13c-112">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C561-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
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

## <a name="members"></a><span data-ttu-id="dc13c-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc13c-113">Members</span></span>

<span data-ttu-id="dc13c-114">La clase **CIM \_ SoftwareElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dc13c-114">The **CIM\_SoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="dc13c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc13c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc13c-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc13c-116">Properties</span></span>

<span data-ttu-id="dc13c-117">La clase **CIM \_ SoftwareElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dc13c-117">The **CIM\_SoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc13c-118">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="dc13c-118">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-121">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="dc13c-121">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-122">Identificador interno de la compilación de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="dc13c-122">Internal identifier for the compilation of this software element.</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dc13c-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-126">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dc13c-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-127">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="dc13c-127">Short textual description of the object.</span></span>

<span data-ttu-id="dc13c-128">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc13c-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-129">**Dese**</span><span class="sxs-lookup"><span data-stu-id="dc13c-129">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-132">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="dc13c-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-133">Conjunto de código utilizado por el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="dc13c-133">Code set used by the software element.</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dc13c-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-137">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="dc13c-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-138">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="dc13c-138">Textual description of the object.</span></span>

<span data-ttu-id="dc13c-139">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc13c-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-140">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="dc13c-140">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-143">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="dc13c-143">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-144">Identificador del fabricante para el elemento de software, a menudo una referencia de almacén (SKU) o un número de pieza.</span><span class="sxs-lookup"><span data-stu-id="dc13c-144">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dc13c-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-146">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dc13c-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="dc13c-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-149">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="dc13c-149">Date and time the object was installed.</span></span> <span data-ttu-id="dc13c-150">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="dc13c-150">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dc13c-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc13c-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-152">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="dc13c-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-155">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="dc13c-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-156">Edición de idioma del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="dc13c-156">Language edition of the software element.</span></span> <span data-ttu-id="dc13c-157">Se deben usar los códigos de idioma definidos en ISO 639.</span><span class="sxs-lookup"><span data-stu-id="dc13c-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="dc13c-158">Cuando el elemento de software representa versiones multilingües o internacionales de un producto, se debe usar la cadena "multilingüe".</span><span class="sxs-lookup"><span data-stu-id="dc13c-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-159">**Le**</span><span class="sxs-lookup"><span data-stu-id="dc13c-159">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-162">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="dc13c-162">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-163">Fabricante del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="dc13c-163">Manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-164">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="dc13c-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-167">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre")</span><span class="sxs-lookup"><span data-stu-id="dc13c-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-168">Nombre usado para identificar el elemento de software. esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc13c-168">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-169">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="dc13c-169">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-172">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="dc13c-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-173">Tipo de fabricante y sistema operativo para un elemento de software cuando la propiedad **TargetOperatingSystem** tiene un valor de 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="dc13c-173">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="dc13c-174">Cuando la propiedad **TargetOperatingSystem** tiene un valor de 1, esta propiedad debe tener un valor distinto de NULL.</span><span class="sxs-lookup"><span data-stu-id="dc13c-174">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="dc13c-175">Para todos los demás valores de **TargetOperatingSystem** , esta propiedad es NULL.</span><span class="sxs-lookup"><span data-stu-id="dc13c-175">For all other **TargetOperatingSystem** values, this property is null.</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-176">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="dc13c-176">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-179">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="dc13c-179">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-180">Número de serie del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="dc13c-180">Serial number of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-181">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="dc13c-181">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-184">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dc13c-184">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-185">Identificador del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="dc13c-185">Identifier for the software element.</span></span> <span data-ttu-id="dc13c-186">Está diseñado para usarse junto con otras claves para crear una representación única de este **\_ SoftwareElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="dc13c-186">It is designed to be used in conjunction with other keys to create a unique representation of this **CIM\_SoftwareElement**.</span></span>

</dd> <dt>

<span data-ttu-id="dc13c-187">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="dc13c-187">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-188">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc13c-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-190">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dc13c-190">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-191">Estado de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="dc13c-191">State of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="dc13c-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="dc13c-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-193">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="dc13c-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="dc13c-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="dc13c-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-195">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="dc13c-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="dc13c-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="dc13c-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-197">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="dc13c-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="dc13c-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="dc13c-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-199">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="dc13c-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc13c-200">**Estado**</span><span class="sxs-lookup"><span data-stu-id="dc13c-200">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-203">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="dc13c-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-204">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="dc13c-204">Current status of the object.</span></span>

<span data-ttu-id="dc13c-205">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc13c-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dc13c-206">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="dc13c-206">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dc13c-207">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="dc13c-207">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dc13c-208">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="dc13c-208">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dc13c-209">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="dc13c-209">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc13c-210">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="dc13c-210">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dc13c-211">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="dc13c-211">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dc13c-212">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="dc13c-212">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dc13c-213">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="dc13c-213">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dc13c-214">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="dc13c-214">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dc13c-215">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="dc13c-215">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dc13c-216">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="dc13c-216">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dc13c-217">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="dc13c-217">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dc13c-218">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="dc13c-218">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc13c-219">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="dc13c-219">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-220">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc13c-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-222">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información \| del componente de software de DMTF 002,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="dc13c-222">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-223">Entorno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc13c-223">Operating system environment.</span></span> <span data-ttu-id="dc13c-224">El valor de esta propiedad no garantiza la ejecución binaria, se necesita más información.</span><span class="sxs-lookup"><span data-stu-id="dc13c-224">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="dc13c-225">La versión del sistema operativo debe especificarse mediante la comprobación de la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc13c-225">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="dc13c-226">También es necesario, es la arquitectura en la que se ejecuta el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc13c-226">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="dc13c-227">La combinación de estas construcciones permite al proveedor identificar claramente el nivel de sistema operativo necesario para un elemento de software determinado.</span><span class="sxs-lookup"><span data-stu-id="dc13c-227">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc13c-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="dc13c-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc13c-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="dc13c-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="dc13c-230"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="dc13c-230"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-231">Mac OS</span><span class="sxs-lookup"><span data-stu-id="dc13c-231">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="dc13c-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="dc13c-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-233">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="dc13c-233">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="dc13c-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="dc13c-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="dc13c-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="dc13c-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="dc13c-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="dc13c-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="dc13c-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="dc13c-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-238">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="dc13c-238">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="dc13c-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="dc13c-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-240">HP-UX</span><span class="sxs-lookup"><span data-stu-id="dc13c-240">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="dc13c-241"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="dc13c-241"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="dc13c-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="dc13c-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="dc13c-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="dc13c-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="dc13c-244"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="dc13c-244"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="dc13c-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="dc13c-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-246">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="dc13c-246">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="dc13c-247"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="dc13c-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="dc13c-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="dc13c-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-249">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="dc13c-249">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="dc13c-250"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="dc13c-250"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-251">Windows 95</span><span class="sxs-lookup"><span data-stu-id="dc13c-251">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="dc13c-252"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="dc13c-252"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-253">Windows 98</span><span class="sxs-lookup"><span data-stu-id="dc13c-253">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="dc13c-254"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="dc13c-254"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-255">Windows NT</span><span class="sxs-lookup"><span data-stu-id="dc13c-255">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="dc13c-256"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="dc13c-256"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-257">Windows CE</span><span class="sxs-lookup"><span data-stu-id="dc13c-257">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="dc13c-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="dc13c-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-259">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="dc13c-259">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="dc13c-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="dc13c-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="dc13c-261"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="dc13c-261"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="dc13c-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="dc13c-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="dc13c-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="dc13c-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="dc13c-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="dc13c-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="dc13c-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="dc13c-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="dc13c-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="dc13c-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="dc13c-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="dc13c-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="dc13c-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="dc13c-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="dc13c-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="dc13c-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="dc13c-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="dc13c-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="dc13c-271"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="dc13c-271"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-272">Una serie</span><span class="sxs-lookup"><span data-stu-id="dc13c-272">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="dc13c-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="dc13c-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-274">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="dc13c-274">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="dc13c-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="dc13c-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-276">Tándem</span><span class="sxs-lookup"><span data-stu-id="dc13c-276">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="dc13c-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="dc13c-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-278">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="dc13c-278">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="dc13c-279"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="dc13c-279"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="dc13c-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="dc13c-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="dc13c-281"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="dc13c-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="dc13c-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="dc13c-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="dc13c-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="dc13c-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="dc13c-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="dc13c-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-285">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="dc13c-285">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="dc13c-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="dc13c-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="dc13c-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="dc13c-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="dc13c-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="dc13c-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="dc13c-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="dc13c-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-290">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="dc13c-290">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="dc13c-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="dc13c-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="dc13c-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="dc13c-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="dc13c-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="dc13c-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="dc13c-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="dc13c-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="dc13c-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="dc13c-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="dc13c-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="dc13c-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="dc13c-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="dc13c-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="dc13c-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="dc13c-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="dc13c-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="dc13c-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="dc13c-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="dc13c-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="dc13c-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="dc13c-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="dc13c-302">Palm OS</span><span class="sxs-lookup"><span data-stu-id="dc13c-302">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="dc13c-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="dc13c-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="dc13c-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="dc13c-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="dc13c-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="dc13c-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="dc13c-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="dc13c-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="dc13c-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="dc13c-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc13c-308">**Versión**</span><span class="sxs-lookup"><span data-stu-id="dc13c-308">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc13c-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc13c-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc13c-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc13c-311">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="dc13c-311">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="dc13c-312">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="dc13c-312">Version of the operation.</span></span>

<span data-ttu-id="dc13c-313">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="dc13c-313">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="dc13c-314"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="dc13c-314"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="dc13c-315"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="dc13c-315"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc13c-316">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc13c-316">Remarks</span></span>

<span data-ttu-id="dc13c-317">La clase **CIM \_ SoftwareElement** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc13c-317">The **CIM\_SoftwareElement** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="dc13c-318">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="dc13c-318">WMI does not implement this class.</span></span> <span data-ttu-id="dc13c-319">Para las clases WMI derivadas de **CIM \_ SoftwareElement**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="dc13c-319">For WMI classes derived from **CIM\_SoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="dc13c-320">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="dc13c-320">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dc13c-321">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="dc13c-321">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc13c-322">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc13c-322">Requirements</span></span>



| <span data-ttu-id="dc13c-323">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc13c-323">Requirement</span></span> | <span data-ttu-id="dc13c-324">Value</span><span class="sxs-lookup"><span data-stu-id="dc13c-324">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc13c-325">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc13c-325">Minimum supported client</span></span><br/> | <span data-ttu-id="dc13c-326">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc13c-326">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc13c-327">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc13c-327">Minimum supported server</span></span><br/> | <span data-ttu-id="dc13c-328">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc13c-328">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc13c-329">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc13c-329">Namespace</span></span><br/>                | <span data-ttu-id="dc13c-330">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dc13c-330">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc13c-331">MOF</span><span class="sxs-lookup"><span data-stu-id="dc13c-331">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc13c-332"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc13c-332"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc13c-333">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc13c-333">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc13c-334"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc13c-334"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc13c-335">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc13c-335">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc13c-336">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="dc13c-336">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

