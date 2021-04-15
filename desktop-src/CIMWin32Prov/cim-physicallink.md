---
description: La \_ clase CIM PhysicalLink representa el cableado de los elementos físicos.
ms.assetid: 0d96cb7f-ca50-4eb2-b8d4-e749bbe67ad7
ms.tgt_platform: multiple
title: CIM_PhysicalLink (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalLink
- CIM_PhysicalLink.Caption
- CIM_PhysicalLink.CreationClassName
- CIM_PhysicalLink.Description
- CIM_PhysicalLink.InstallDate
- CIM_PhysicalLink.Length
- CIM_PhysicalLink.Manufacturer
- CIM_PhysicalLink.MaxLength
- CIM_PhysicalLink.MediaType
- CIM_PhysicalLink.Model
- CIM_PhysicalLink.Name
- CIM_PhysicalLink.OtherIdentifyingInfo
- CIM_PhysicalLink.PartNumber
- CIM_PhysicalLink.PoweredOn
- CIM_PhysicalLink.SerialNumber
- CIM_PhysicalLink.SKU
- CIM_PhysicalLink.Status
- CIM_PhysicalLink.Tag
- CIM_PhysicalLink.Version
- CIM_PhysicalLink.Wired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 659e73d9f5331d5c6648af00e147797dc6424130
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539160"
---
# <a name="cim_physicallink-class"></a><span data-ttu-id="1d9a8-103">\_Clase PhysicalLink de CIM</span><span class="sxs-lookup"><span data-stu-id="1d9a8-103">CIM\_PhysicalLink class</span></span>

<span data-ttu-id="1d9a8-104">La clase **CIM \_ PhysicalLink** representa el cableado de los elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-104">The **CIM\_PhysicalLink** class represents the cabling of physical elements.</span></span> <span data-ttu-id="1d9a8-105">Por ejemplo, los cables de serie o Ethernet y los vínculos de infrarrojos serían subclases (si se definen propiedades o asociaciones adicionales) o instancias de **CIM \_ PhysicalLink**.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-105">For example, serial or Ethernet cables and infrared links would be subclasses (if additional properties or associations are defined) or instances of **CIM\_PhysicalLink**.</span></span> <span data-ttu-id="1d9a8-106">Normalmente, no se modelan los numerosos cables físicos dentro de un paquete físico o de una red.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-106">Typically, the numerous physical cables within a physical package or network are not modeled.</span></span> <span data-ttu-id="1d9a8-107">Sin embargo, cuando los cables o los vínculos son componentes críticos o activos etiquetados de la empresa, se pueden crear instancias de los objetos utilizando esta clase o una de sus clases descendientes.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-107">However, when the cables or links are critical components or tagged assets of the company, the objects can be instantiated using this class or one of its descendant classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d9a8-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1d9a8-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1d9a8-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1d9a8-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9a8-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d9a8-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B82-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalLink : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  real64   Length;
  string   Manufacturer;
  real64   MaxLength;
  uint16   MediaType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  Wired;
};
```

## <a name="members"></a><span data-ttu-id="1d9a8-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d9a8-113">Members</span></span>

<span data-ttu-id="1d9a8-114">La clase **CIM \_ PhysicalLink** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1d9a8-114">The **CIM\_PhysicalLink** class has these types of members:</span></span>

-   [<span data-ttu-id="1d9a8-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d9a8-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d9a8-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d9a8-116">Properties</span></span>

<span data-ttu-id="1d9a8-117">La clase **CIM \_ PhysicalLink** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-117">The **CIM\_PhysicalLink** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d9a8-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-121">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-122">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-122">Short textual description of the object.</span></span>

<span data-ttu-id="1d9a8-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-127">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-128">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1d9a8-129">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1d9a8-130">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-134">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-135">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-135">Textual description of the object.</span></span>

<span data-ttu-id="1d9a8-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-138">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-140">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-141">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-141">Date and time the object was installed.</span></span> <span data-ttu-id="1d9a8-142">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1d9a8-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-144">**Duración**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-145">Tipo de datos: **real64**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-145">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-147">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pies")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-147">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-148">Longitud actual del vínculo físico, en metros.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-148">Current length of the physical link, in feet.</span></span> <span data-ttu-id="1d9a8-149">En el caso de algunas conexiones, especialmente en tecnologías inalámbricas, es posible que esta propiedad no sea aplicable y deba dejarse sin inicializar.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-149">For some connections, especially wireless technologies, this property might not be applicable and should be left uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-150">**Le**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-150">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-153">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-153">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-154">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-154">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="1d9a8-155">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-155">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="1d9a8-156">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-156">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-157">**MaxLength**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-157">**MaxLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-158">Tipo de datos: **real64**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-158">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-160">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pies")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-160">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-161">Longitud máxima del vínculo físico en metros.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-161">Maximum length of the physical link in feet.</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-162">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-162">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-163">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-165">Tipo de medio a través del cual pasan las señales de transmisión.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-165">Type of media through which transmission signals pass.</span></span> <span data-ttu-id="1d9a8-166">Entre los medios de red más comunes se incluyen los cables de par trenzado, coaxial y de fibra óptica.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-166">Common network media include twisted-pair, coaxial, and fiber-optic cable.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d9a8-167">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-167">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d9a8-168">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat1"></span><span id="cat1"></span><span id="CAT1"></span>

<span data-ttu-id="1d9a8-169">**CAT1** (2)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-169">**Cat1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat2"></span><span id="cat2"></span><span id="CAT2"></span>

<span data-ttu-id="1d9a8-170">**CAT2** (3)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-170">**Cat2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat3"></span><span id="cat3"></span><span id="CAT3"></span>

<span data-ttu-id="1d9a8-171">**Cat3** (4)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-171">**Cat3** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat4"></span><span id="cat4"></span><span id="CAT4"></span>

<span data-ttu-id="1d9a8-172">**Cat4** (5)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-172">**Cat4** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat5"></span><span id="cat5"></span><span id="CAT5"></span>

<span data-ttu-id="1d9a8-173">**CAT5** (6)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-173">**Cat5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="50-ohm_Coaxial"></span><span id="50-ohm_coaxial"></span><span id="50-OHM_COAXIAL"></span>

<span data-ttu-id="1d9a8-174">**50-Ohm coaxial** (7)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-174">**50-ohm Coaxial** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="75-ohm_Coaxial"></span><span id="75-ohm_coaxial"></span><span id="75-OHM_COAXIAL"></span>

<span data-ttu-id="1d9a8-175">**75-ohm coaxial** (8)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-175">**75-ohm Coaxial** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="100-ohm_Coaxial"></span><span id="100-ohm_coaxial"></span><span id="100-OHM_COAXIAL"></span>

<span data-ttu-id="1d9a8-176">**100-Ohm coaxial** (9)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-176">**100-ohm Coaxial** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber-optic"></span><span id="fiber-optic"></span><span id="FIBER-OPTIC"></span>

<span data-ttu-id="1d9a8-177">**Fibra óptica** (10)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-177">**Fiber-optic** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP"></span><span id="utp"></span>

<span data-ttu-id="1d9a8-178">**UTP** (11)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-178">**UTP** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="STP"></span><span id="stp"></span>

<span data-ttu-id="1d9a8-179">**STP** (12)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-179">**STP** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon_Cable"></span><span id="ribbon_cable"></span><span id="RIBBON_CABLE"></span>

<span data-ttu-id="1d9a8-180">**Cable de cinta** (13)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-180">**Ribbon Cable** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Twinaxial"></span><span id="twinaxial"></span><span id="TWINAXIAL"></span>

<span data-ttu-id="1d9a8-181">**Twinaxial** (14)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-181">**Twinaxial** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_9um"></span><span id="optical_9um"></span><span id="OPTICAL_9UM"></span>

<span data-ttu-id="1d9a8-182">**9Um óptico** (15)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-182">**Optical 9um** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_50um"></span><span id="optical_50um"></span><span id="OPTICAL_50UM"></span>

<span data-ttu-id="1d9a8-183">**50Um óptico** (16)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-183">**Optical 50um** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_62.5um"></span><span id="optical_62.5um"></span><span id="OPTICAL_62.5UM"></span>

<span data-ttu-id="1d9a8-184">**Um de la 62,5 óptica** (17)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-184">**Optical 62.5um** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d9a8-185">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-185">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-188">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-189">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-189">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="1d9a8-190">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-190">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-191">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-191">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-194">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-194">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-195">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-195">Label by which the object is known.</span></span> <span data-ttu-id="1d9a8-196">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-196">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="1d9a8-197">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-198">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-198">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-201">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-201">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="1d9a8-202">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-202">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="1d9a8-203">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="1d9a8-203">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="1d9a8-204">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-204">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-205">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-205">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-206">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-208">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-209">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-209">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="1d9a8-210">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-210">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-211">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-211">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-212">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-214">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-214">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="1d9a8-215">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-216">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-216">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-219">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-220">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-220">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="1d9a8-221">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-222">**SKU**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-222">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-225">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-225">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-226">Número de unidad de almacén para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-226">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="1d9a8-227">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-228">**Estado**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-228">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-229">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-231">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-232">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-232">Current status of the object.</span></span>

<span data-ttu-id="1d9a8-233">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-233">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1d9a8-234">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d9a8-234">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1d9a8-235">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-235">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1d9a8-236">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-236">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1d9a8-237">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-237">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d9a8-238">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-238">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1d9a8-239">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-239">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1d9a8-240">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-240">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1d9a8-241">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-241">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1d9a8-242">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-242">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1d9a8-243">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-243">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1d9a8-244">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-244">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1d9a8-245">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-245">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1d9a8-246">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="1d9a8-246">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d9a8-247">**Tag**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-247">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-248">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-250">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-250">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-251">Cadena arbitraria que identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-251">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="1d9a8-252">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-252">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="1d9a8-253">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-253">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="1d9a8-254">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-254">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="1d9a8-255">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-255">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="1d9a8-256">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-256">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="1d9a8-257">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-258">**Versión**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-259">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-261">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1d9a8-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-262">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-262">Version of the physical element.</span></span>

<span data-ttu-id="1d9a8-263">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d9a8-264">**Con cable**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-264">**Wired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9a8-265">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d9a8-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d9a8-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9a8-267">Si es **true**, el vínculo físico es un cable.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-267">If **TRUE**, the physical link is a cable.</span></span> <span data-ttu-id="1d9a8-268">De lo contrario, es una conexión inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-268">Otherwise, it is a wireless connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d9a8-269">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d9a8-269">Remarks</span></span>

<span data-ttu-id="1d9a8-270">La clase **CIM \_ PhysicalLink** se deriva de [**\_ PhysicalElement de CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a8-270">The **CIM\_PhysicalLink** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="1d9a8-271">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-271">WMI does not implement this class.</span></span>

<span data-ttu-id="1d9a8-272">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-272">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1d9a8-273">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="1d9a8-273">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d9a8-274">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d9a8-274">Requirements</span></span>



| <span data-ttu-id="1d9a8-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d9a8-275">Requirement</span></span> | <span data-ttu-id="1d9a8-276">Value</span><span class="sxs-lookup"><span data-stu-id="1d9a8-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d9a8-277">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d9a8-277">Minimum supported client</span></span><br/> | <span data-ttu-id="1d9a8-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d9a8-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d9a8-279">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d9a8-279">Minimum supported server</span></span><br/> | <span data-ttu-id="1d9a8-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d9a8-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d9a8-281">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d9a8-281">Namespace</span></span><br/>                | <span data-ttu-id="1d9a8-282">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1d9a8-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d9a8-283">MOF</span><span class="sxs-lookup"><span data-stu-id="1d9a8-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d9a8-284"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a8-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d9a8-285">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d9a8-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d9a8-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a8-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d9a8-287">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d9a8-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d9a8-288">**\_PHYSICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="1d9a8-288">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

