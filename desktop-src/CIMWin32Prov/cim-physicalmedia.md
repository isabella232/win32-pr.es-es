---
description: La \_ clase CIM PhysicalMedia representa los tipos de documentación y el medio de almacenamiento, como cintas, CD-ROM, etc.
ms.assetid: ba258e53-4a82-4b30-aadd-54448841cd06
ms.tgt_platform: multiple
title: CIM_PhysicalMedia (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMedia
- CIM_PhysicalMedia.Capacity
- CIM_PhysicalMedia.Caption
- CIM_PhysicalMedia.CleanerMedia
- CIM_PhysicalMedia.CreationClassName
- CIM_PhysicalMedia.Description
- CIM_PhysicalMedia.HotSwappable
- CIM_PhysicalMedia.InstallDate
- CIM_PhysicalMedia.Manufacturer
- CIM_PhysicalMedia.MediaDescription
- CIM_PhysicalMedia.MediaType
- CIM_PhysicalMedia.Model
- CIM_PhysicalMedia.Name
- CIM_PhysicalMedia.OtherIdentifyingInfo
- CIM_PhysicalMedia.PartNumber
- CIM_PhysicalMedia.PoweredOn
- CIM_PhysicalMedia.Removable
- CIM_PhysicalMedia.Replaceable
- CIM_PhysicalMedia.SerialNumber
- CIM_PhysicalMedia.SKU
- CIM_PhysicalMedia.Status
- CIM_PhysicalMedia.Tag
- CIM_PhysicalMedia.Version
- CIM_PhysicalMedia.WriteProtectOn
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8709128c189956bba4bc371e0f5bfb30d67b49f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279826"
---
# <a name="cim_physicalmedia-class"></a><span data-ttu-id="5d232-103">\_Clase PhysicalMedia de CIM</span><span class="sxs-lookup"><span data-stu-id="5d232-103">CIM\_PhysicalMedia class</span></span>

<span data-ttu-id="5d232-104">La clase **CIM \_ PhysicalMedia** representa los tipos de documentación y el medio de almacenamiento, como cintas, CD-ROM, etc.</span><span class="sxs-lookup"><span data-stu-id="5d232-104">The **CIM\_PhysicalMedia** class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span> <span data-ttu-id="5d232-105">Esta clase se usa normalmente para buscar y administrar medios extraíbles (en lugar de medios sellados con el dispositivo de acceso a medios como un solo paquete, como discos duros).</span><span class="sxs-lookup"><span data-stu-id="5d232-105">This class is typically used to locate and manage removable media (versus media sealed with the media access device as a single package, such as hard disks).</span></span> <span data-ttu-id="5d232-106">Sin embargo, los medios sellados también se pueden modelar con esta clase cuando el medio está asociado al paquete físico mediante la relación [**\_ PackagedComponent de CIM**](cim-packagedcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="5d232-106">Sealed media, however, can also be modeled using this class when the media is associated with the physical package using the [**CIM\_PackagedComponent**](cim-packagedcomponent.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d232-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="5d232-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5d232-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5d232-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5d232-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5d232-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5d232-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5d232-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d232-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d232-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMedia : CIM_PhysicalComponent
{
  uint64   Capacity;
  string   Caption;
  boolean  CleanerMedia;
  string   CreationClassName;
  string   Description;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   MediaDescription;
  uint16   MediaType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  WriteProtectOn;
};
```

## <a name="members"></a><span data-ttu-id="5d232-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="5d232-112">Members</span></span>

<span data-ttu-id="5d232-113">La clase **CIM \_ PhysicalMedia** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5d232-113">The **CIM\_PhysicalMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="5d232-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d232-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d232-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d232-115">Properties</span></span>

<span data-ttu-id="5d232-116">La clase **CIM \_ PhysicalMedia** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5d232-116">The **CIM\_PhysicalMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d232-117">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="5d232-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-118">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d232-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-120">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="5d232-120">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5d232-121">Número de bytes que se pueden leer o escribir en un medio.</span><span class="sxs-lookup"><span data-stu-id="5d232-121">Number of bytes that can be read from, or written to, a media.</span></span> <span data-ttu-id="5d232-122">Esta propiedad no es aplicable a los medios de copia impresa (documentación) o de limpiador.</span><span class="sxs-lookup"><span data-stu-id="5d232-122">This property is not applicable to hard copy (documentation) or cleaner media.</span></span> <span data-ttu-id="5d232-123">No se debería suponer la compresión de datos, ya que aumentaría el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="5d232-123">Data compression should not be assumed, as it would increase the value in this property.</span></span> <span data-ttu-id="5d232-124">En el caso de las cintas, se debe suponer que no hay marcas de archivo ni áreas de espacio en blanco registradas en el medio.</span><span class="sxs-lookup"><span data-stu-id="5d232-124">For tapes, it should be assumed that no file marks or blank space areas are recorded on the media.</span></span>

<span data-ttu-id="5d232-125">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5d232-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5d232-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-129">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5d232-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5d232-130">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5d232-130">Short textual description of the object.</span></span>

<span data-ttu-id="5d232-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-132">**CleanerMedia**</span><span class="sxs-lookup"><span data-stu-id="5d232-132">**CleanerMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-133">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5d232-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d232-135">Si es **true**, el medio físico se utiliza para la limpieza, no para el almacenamiento de datos.</span><span class="sxs-lookup"><span data-stu-id="5d232-135">If **TRUE**, the physical media is used for cleaning purposes, not data storage.</span></span>

</dd> <dt>

<span data-ttu-id="5d232-136">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5d232-136">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-139">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5d232-139">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5d232-140">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="5d232-140">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5d232-141">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="5d232-141">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5d232-142">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-142">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d232-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-146">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="5d232-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5d232-147">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5d232-147">Textual description of the object.</span></span>

<span data-ttu-id="5d232-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-149">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="5d232-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-150">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5d232-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d232-152">Si **es true**, el paquete puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="5d232-152">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="5d232-153">Un paquete físico puede intercambiarse en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras se activa el paquete contenedor.</span><span class="sxs-lookup"><span data-stu-id="5d232-153">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="5d232-154">Por ejemplo, un componente de ventilador se puede diseñar para que se intercambie en caliente.</span><span class="sxs-lookup"><span data-stu-id="5d232-154">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="5d232-155">Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="5d232-155">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="5d232-156">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-156">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5d232-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-158">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5d232-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-160">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="5d232-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5d232-161">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="5d232-161">Date and time the object was installed.</span></span> <span data-ttu-id="5d232-162">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5d232-162">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5d232-163">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-164">**Le**</span><span class="sxs-lookup"><span data-stu-id="5d232-164">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-167">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5d232-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5d232-168">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5d232-168">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="5d232-169">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-169">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="5d232-170">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-170">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-171">**MediaDescription**</span><span class="sxs-lookup"><span data-stu-id="5d232-171">**MediaDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-174">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalMedia**.**MediaType**")</span><span class="sxs-lookup"><span data-stu-id="5d232-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaType**")</span></span>
</dt> </dl>

<span data-ttu-id="5d232-175">Detalles adicionales relacionados con la enumeración **mediatype** .</span><span class="sxs-lookup"><span data-stu-id="5d232-175">Additional detail related to the **MediaType** enumeration.</span></span> <span data-ttu-id="5d232-176">Por ejemplo, si se especifica el valor 3 ("cartucho QIC"), esta propiedad indicará si la cinta es ancha o 1/4, con formato previo, compatible con Travan, etc.</span><span class="sxs-lookup"><span data-stu-id="5d232-176">For example, if value 3 ("QIC Cartridge") is specified, this property would indicate whether the tape is wide or 1/4 inch, pre-formatted, Travan compatible, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="5d232-177">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="5d232-177">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-178">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d232-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-180">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalMedia**.**MediaDescription**")</span><span class="sxs-lookup"><span data-stu-id="5d232-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="5d232-181">Tipo de medio físico.</span><span class="sxs-lookup"><span data-stu-id="5d232-181">Type of physical media.</span></span> <span data-ttu-id="5d232-182">La propiedad **MediaDescription** proporciona una definición más explícita del tipo de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="5d232-182">The **MediaDescription** property provides more explicit definition of the media type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d232-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5d232-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5d232-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5d232-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>

<span data-ttu-id="5d232-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Cartucho de cinta** (2)</span><span class="sxs-lookup"><span data-stu-id="5d232-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Tape Cartridge** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>

<span data-ttu-id="5d232-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**Cartucho QIC** (3)</span><span class="sxs-lookup"><span data-stu-id="5d232-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**QIC Cartridge** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>

<span data-ttu-id="5d232-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**Cartucho AIT** (4)</span><span class="sxs-lookup"><span data-stu-id="5d232-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**AIT Cartridge** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>

<span data-ttu-id="5d232-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**Cartucho DTF** (5)</span><span class="sxs-lookup"><span data-stu-id="5d232-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**DTF Cartridge** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>

<span data-ttu-id="5d232-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**Cartucho DAT** (6)</span><span class="sxs-lookup"><span data-stu-id="5d232-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**DAT Cartridge** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="5d232-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**cartucho de cinta de 8mm** (7)</span><span class="sxs-lookup"><span data-stu-id="5d232-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**8mm Tape Cartridge** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="5d232-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**cartucho de cinta 19mm** (8)</span><span class="sxs-lookup"><span data-stu-id="5d232-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**19mm Tape Cartridge** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>

<span data-ttu-id="5d232-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**Cartucho DLT** (9)</span><span class="sxs-lookup"><span data-stu-id="5d232-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**DLT Cartridge** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>

<span data-ttu-id="5d232-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Cartucho de cinta magnética de 1/2 pulgada** (10)</span><span class="sxs-lookup"><span data-stu-id="5d232-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Half-Inch Magnetic Tape Cartridge** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>

<span data-ttu-id="5d232-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Disco de cartucho** (11)</span><span class="sxs-lookup"><span data-stu-id="5d232-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Cartridge Disk** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>

<span data-ttu-id="5d232-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**Disco Jaz** (12)</span><span class="sxs-lookup"><span data-stu-id="5d232-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**JAZ Disk** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>

<span data-ttu-id="5d232-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**Disco Zip** (13)</span><span class="sxs-lookup"><span data-stu-id="5d232-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**ZIP Disk** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>

<span data-ttu-id="5d232-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**Disco Syquest** (14)</span><span class="sxs-lookup"><span data-stu-id="5d232-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**SyQuest Disk** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>

<span data-ttu-id="5d232-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Disco extraíble Winchester** (15)</span><span class="sxs-lookup"><span data-stu-id="5d232-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Winchester Removable Disk** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="5d232-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="5d232-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span data-ttu-id="5d232-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="5d232-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span data-ttu-id="5d232-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="5d232-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span data-ttu-id="5d232-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD grabable** (19)</span><span class="sxs-lookup"><span data-stu-id="5d232-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="WORM"></span><span id="worm"></span>

<span data-ttu-id="5d232-203"><span id="WORM"></span><span id="worm"></span>**Gusano** (20)</span><span class="sxs-lookup"><span data-stu-id="5d232-203"><span id="WORM"></span><span id="worm"></span>**WORM** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>

<span data-ttu-id="5d232-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-óptico** (21)</span><span class="sxs-lookup"><span data-stu-id="5d232-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-Optical** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span data-ttu-id="5d232-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="5d232-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_RW"></span><span id="dvd_rw"></span>

<span data-ttu-id="5d232-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD + RW** (23)</span><span class="sxs-lookup"><span data-stu-id="5d232-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD+RW** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span data-ttu-id="5d232-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="5d232-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span data-ttu-id="5d232-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="5d232-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span data-ttu-id="5d232-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-vídeo** (26)</span><span class="sxs-lookup"><span data-stu-id="5d232-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span data-ttu-id="5d232-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**DivX** (27)</span><span class="sxs-lookup"><span data-stu-id="5d232-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>

<span data-ttu-id="5d232-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Disquete o disquete** (28)</span><span class="sxs-lookup"><span data-stu-id="5d232-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Floppy/Diskette** (28)</span></span>


</dt> <dd>

<span data-ttu-id="5d232-212">Disquete</span><span class="sxs-lookup"><span data-stu-id="5d232-212">Floppy disk</span></span>

</dd> <dt>

<span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>

<span data-ttu-id="5d232-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Disco duro** (29)</span><span class="sxs-lookup"><span data-stu-id="5d232-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Hard Disk** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>

<span data-ttu-id="5d232-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Tarjeta de memoria** (30)</span><span class="sxs-lookup"><span data-stu-id="5d232-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Memory Card** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>

<span data-ttu-id="5d232-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Copia impresa** (31)</span><span class="sxs-lookup"><span data-stu-id="5d232-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Hard Copy** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>

<span data-ttu-id="5d232-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Disco clik** (32)</span><span class="sxs-lookup"><span data-stu-id="5d232-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Clik Disk** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span data-ttu-id="5d232-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="5d232-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span data-ttu-id="5d232-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-da** (34)</span><span class="sxs-lookup"><span data-stu-id="5d232-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span data-ttu-id="5d232-219"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="5d232-219"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span data-ttu-id="5d232-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD grabable** (36)</span><span class="sxs-lookup"><span data-stu-id="5d232-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span data-ttu-id="5d232-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="5d232-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span data-ttu-id="5d232-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-audio** (38)</span><span class="sxs-lookup"><span data-stu-id="5d232-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span data-ttu-id="5d232-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="5d232-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span data-ttu-id="5d232-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="5d232-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span data-ttu-id="5d232-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="5d232-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span data-ttu-id="5d232-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="5d232-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>

<span data-ttu-id="5d232-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magneto-óptico regrabable** (43)</span><span class="sxs-lookup"><span data-stu-id="5d232-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magneto-Optical Rewriteable** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>

<span data-ttu-id="5d232-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Escritura magneto-óptica** (44)</span><span class="sxs-lookup"><span data-stu-id="5d232-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Magneto-Optical Write Once** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>

<span data-ttu-id="5d232-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magneto-ópticos regrabables (LIMDOW)** (45)</span><span class="sxs-lookup"><span data-stu-id="5d232-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magneto-Optical Rewriteable (LIMDOW)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>

<span data-ttu-id="5d232-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Cambio de fase de escritura una vez** (46)</span><span class="sxs-lookup"><span data-stu-id="5d232-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Phase Change Write Once** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>

<span data-ttu-id="5d232-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Cambio de fase regrabable** (47)</span><span class="sxs-lookup"><span data-stu-id="5d232-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Phase Change Rewriteable** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>

<span data-ttu-id="5d232-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Cambio de fase dual regrabable** (48)</span><span class="sxs-lookup"><span data-stu-id="5d232-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Phase Change Dual Rewriteable** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>

<span data-ttu-id="5d232-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Ablative escritura una vez** (49)</span><span class="sxs-lookup"><span data-stu-id="5d232-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Ablative Write Once** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>

<span data-ttu-id="5d232-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Grabación de campos Near** (50)</span><span class="sxs-lookup"><span data-stu-id="5d232-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Near Field Recording** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>

<span data-ttu-id="5d232-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQic** (51)</span><span class="sxs-lookup"><span data-stu-id="5d232-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQic** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>

<span data-ttu-id="5d232-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)</span><span class="sxs-lookup"><span data-stu-id="5d232-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>

<span data-ttu-id="5d232-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**partículas metal de 8 mm** (53)</span><span class="sxs-lookup"><span data-stu-id="5d232-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**8mm Metal Particle** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>

<span data-ttu-id="5d232-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**evaporación de metal avanzado de 8mm** (54)</span><span class="sxs-lookup"><span data-stu-id="5d232-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**8mm Advanced Metal Evaporate** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NCTP"></span><span id="nctp"></span>

<span data-ttu-id="5d232-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)</span><span class="sxs-lookup"><span data-stu-id="5d232-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>

<span data-ttu-id="5d232-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span><span class="sxs-lookup"><span data-stu-id="5d232-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>

<span data-ttu-id="5d232-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**Aceleración LTO** (57)</span><span class="sxs-lookup"><span data-stu-id="5d232-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**LTO Accelis** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>

<span data-ttu-id="5d232-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 cinta de seguimiento** (58)</span><span class="sxs-lookup"><span data-stu-id="5d232-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 Track Tape** (58)</span></span>


</dt> <dd>

<span data-ttu-id="5d232-243">9-pista de cinta</span><span class="sxs-lookup"><span data-stu-id="5d232-243">9-track tape</span></span>

</dd> <dt>

<span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>

<span data-ttu-id="5d232-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 cinta de pista** (59)</span><span class="sxs-lookup"><span data-stu-id="5d232-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 Track Tape** (59)</span></span>


</dt> <dd>

<span data-ttu-id="5d232-245">cinta de 18 pistas</span><span class="sxs-lookup"><span data-stu-id="5d232-245">18-track tape</span></span>

</dd> <dt>

<span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>

<span data-ttu-id="5d232-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 pista de cinta** (60)</span><span class="sxs-lookup"><span data-stu-id="5d232-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 Track Tape** (60)</span></span>


</dt> <dd>

<span data-ttu-id="5d232-247">36: realizar un seguimiento de la cinta</span><span class="sxs-lookup"><span data-stu-id="5d232-247">36-track tape</span></span>

</dd> <dt>

<span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>

<span data-ttu-id="5d232-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span><span class="sxs-lookup"><span data-stu-id="5d232-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>

<span data-ttu-id="5d232-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**Módulo de administración de Magstar** (62)</span><span class="sxs-lookup"><span data-stu-id="5d232-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**Magstar MP** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>

<span data-ttu-id="5d232-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**Cinta D2** (63)</span><span class="sxs-lookup"><span data-stu-id="5d232-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**D2 Tape** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>

<span data-ttu-id="5d232-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Cinta-DST pequeño** (64)</span><span class="sxs-lookup"><span data-stu-id="5d232-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Tape - DST Small** (64)</span></span>


</dt> <dd>

<span data-ttu-id="5d232-252">Cinta DST pequeña</span><span class="sxs-lookup"><span data-stu-id="5d232-252">Tape   DST small</span></span>

</dd> <dt>

<span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>

<span data-ttu-id="5d232-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Cinta-DST medio** (65)</span><span class="sxs-lookup"><span data-stu-id="5d232-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Tape - DST Medium** (65)</span></span>


</dt> <dd>

<span data-ttu-id="5d232-254">Cinta DST media</span><span class="sxs-lookup"><span data-stu-id="5d232-254">Tape   DST medium</span></span>

</dd> <dt>

<span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>

<span data-ttu-id="5d232-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Cinta-DST grande** (66)</span><span class="sxs-lookup"><span data-stu-id="5d232-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Tape - DST Large** (66)</span></span>


</dt> <dd>

<span data-ttu-id="5d232-256">Cinta DST grande</span><span class="sxs-lookup"><span data-stu-id="5d232-256">Tape   DST large</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5d232-257">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="5d232-257">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-260">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5d232-260">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5d232-261">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5d232-261">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="5d232-262">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-263">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5d232-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-266">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5d232-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5d232-267">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="5d232-267">Label by which the object is known.</span></span> <span data-ttu-id="5d232-268">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="5d232-268">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5d232-269">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-269">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-270">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5d232-270">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-271">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d232-273">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5d232-273">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="5d232-274">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="5d232-274">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="5d232-275">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="5d232-275">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="5d232-276">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-276">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-277">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="5d232-277">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-280">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5d232-280">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5d232-281">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5d232-281">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="5d232-282">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-283">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="5d232-283">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-284">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5d232-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d232-286">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="5d232-286">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="5d232-287">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-288">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="5d232-288">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-289">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5d232-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d232-291">Si es **true**, este elemento está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado global.</span><span class="sxs-lookup"><span data-stu-id="5d232-291">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="5d232-292">Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="5d232-292">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="5d232-293">Si la potencia puede estar activada y se ha quitado el paquete, el elemento es extraíble y se puede intercambiar en caliente.</span><span class="sxs-lookup"><span data-stu-id="5d232-293">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="5d232-294">Por ejemplo, un chip de procesador no reduciendo es extraíble.</span><span class="sxs-lookup"><span data-stu-id="5d232-294">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="5d232-295">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-295">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-296">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="5d232-296">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-297">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5d232-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d232-299">Si es **true**, es posible reemplazar el elemento por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="5d232-299">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="5d232-300">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="5d232-300">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="5d232-301">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="5d232-301">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="5d232-302">Todos los componentes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="5d232-302">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="5d232-303">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-303">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-304">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="5d232-304">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-305">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-307">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5d232-307">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5d232-308">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5d232-308">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="5d232-309">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-309">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-310">**SKU**</span><span class="sxs-lookup"><span data-stu-id="5d232-310">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-311">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-313">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5d232-313">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5d232-314">Número de unidad de almacén para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5d232-314">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="5d232-315">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-315">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-316">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5d232-316">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-319">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5d232-319">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5d232-320">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5d232-320">Current status of the object.</span></span>

<span data-ttu-id="5d232-321">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5d232-322">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5d232-322">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5d232-323">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="5d232-323">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5d232-324">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="5d232-324">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5d232-325">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5d232-325">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d232-326">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="5d232-326">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5d232-327">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="5d232-327">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5d232-328">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="5d232-328">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5d232-329">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="5d232-329">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5d232-330">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="5d232-330">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5d232-331">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="5d232-331">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5d232-332">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5d232-332">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5d232-333">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="5d232-333">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5d232-334">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="5d232-334">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d232-335">**Tag**</span><span class="sxs-lookup"><span data-stu-id="5d232-335">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-336">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-338">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5d232-338">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5d232-339">Cadena arbitraria que identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="5d232-339">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="5d232-340">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="5d232-340">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="5d232-341">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="5d232-341">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="5d232-342">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="5d232-342">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="5d232-343">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5d232-343">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="5d232-344">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="5d232-344">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="5d232-345">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-345">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-346">**Versión**</span><span class="sxs-lookup"><span data-stu-id="5d232-346">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d232-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d232-349">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5d232-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5d232-350">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5d232-350">Version of the physical element.</span></span>

<span data-ttu-id="5d232-351">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-351">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d232-352">**WriteProtectOn**</span><span class="sxs-lookup"><span data-stu-id="5d232-352">**WriteProtectOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d232-353">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5d232-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d232-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d232-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d232-355">Si es **true**, el medio está protegido contra escritura por un mecanismo físico, como una pestaña proteger en un disquete.</span><span class="sxs-lookup"><span data-stu-id="5d232-355">If **TRUE**, the media is currently write-protected by a physical mechanism, such as a protect tab on a floppy disk.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d232-356">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d232-356">Remarks</span></span>

<span data-ttu-id="5d232-357">La clase **CIM \_ PhysicalMedia** se deriva de [**\_ PhysicalComponent de CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5d232-357">The **CIM\_PhysicalMedia** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="5d232-358">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="5d232-358">WMI does not implement this class.</span></span>

<span data-ttu-id="5d232-359">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="5d232-359">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5d232-360">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="5d232-360">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d232-361">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d232-361">Requirements</span></span>



| <span data-ttu-id="5d232-362">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d232-362">Requirement</span></span> | <span data-ttu-id="5d232-363">Value</span><span class="sxs-lookup"><span data-stu-id="5d232-363">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d232-364">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d232-364">Minimum supported client</span></span><br/> | <span data-ttu-id="5d232-365">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d232-365">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d232-366">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d232-366">Minimum supported server</span></span><br/> | <span data-ttu-id="5d232-367">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d232-367">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d232-368">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5d232-368">Namespace</span></span><br/>                | <span data-ttu-id="5d232-369">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5d232-369">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d232-370">MOF</span><span class="sxs-lookup"><span data-stu-id="5d232-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d232-371"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d232-371"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d232-372">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d232-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d232-373"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d232-373"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d232-374">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d232-374">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d232-375">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="5d232-375">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

