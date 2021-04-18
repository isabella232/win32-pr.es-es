---
description: La \_ clase CIM PhysicalPackage representa los elementos físicos que contienen u hospedan otros componentes. Algunos ejemplos son un alojamiento en bastidor o una tarjeta adaptadora.
ms.assetid: 9182d413-aa7e-4c2f-94fe-12e99980520c
ms.tgt_platform: multiple
title: CIM_PhysicalPackage (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage
- CIM_PhysicalPackage.Caption
- CIM_PhysicalPackage.CreationClassName
- CIM_PhysicalPackage.Depth
- CIM_PhysicalPackage.Description
- CIM_PhysicalPackage.Height
- CIM_PhysicalPackage.HotSwappable
- CIM_PhysicalPackage.InstallDate
- CIM_PhysicalPackage.Manufacturer
- CIM_PhysicalPackage.Model
- CIM_PhysicalPackage.Name
- CIM_PhysicalPackage.OtherIdentifyingInfo
- CIM_PhysicalPackage.PartNumber
- CIM_PhysicalPackage.PoweredOn
- CIM_PhysicalPackage.Removable
- CIM_PhysicalPackage.Replaceable
- CIM_PhysicalPackage.SerialNumber
- CIM_PhysicalPackage.SKU
- CIM_PhysicalPackage.Status
- CIM_PhysicalPackage.Tag
- CIM_PhysicalPackage.Version
- CIM_PhysicalPackage.Weight
- CIM_PhysicalPackage.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1905467fd949e2c18d8be9e7a7bfff39ad8d1477
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659689"
---
# <a name="cim_physicalpackage-class"></a><span data-ttu-id="9993e-104">\_Clase PhysicalPackage de CIM</span><span class="sxs-lookup"><span data-stu-id="9993e-104">CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="9993e-105">La clase **CIM \_ PhysicalPackage** representa los elementos físicos que contienen u hospedan otros componentes.</span><span class="sxs-lookup"><span data-stu-id="9993e-105">The **CIM\_PhysicalPackage** class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="9993e-106">Algunos ejemplos son un alojamiento en bastidor o una tarjeta adaptadora.</span><span class="sxs-lookup"><span data-stu-id="9993e-106">Examples are a rack enclosure or an adapter card.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9993e-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9993e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9993e-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9993e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9993e-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9993e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9993e-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9993e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9993e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9993e-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B6E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalPackage : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
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
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="9993e-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="9993e-112">Members</span></span>

<span data-ttu-id="9993e-113">La clase **CIM \_ PhysicalPackage** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9993e-113">The **CIM\_PhysicalPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="9993e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="9993e-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="9993e-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9993e-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9993e-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="9993e-116">Methods</span></span>

<span data-ttu-id="9993e-117">La clase **CIM \_ PhysicalPackage** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9993e-117">The **CIM\_PhysicalPackage** class has these methods.</span></span>



| <span data-ttu-id="9993e-118">Método</span><span class="sxs-lookup"><span data-stu-id="9993e-118">Method</span></span>                                                                   | <span data-ttu-id="9993e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="9993e-119">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9993e-120">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="9993e-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md) | <span data-ttu-id="9993e-121">Comprueba si el elemento físico al que se hace referencia puede estar contenido o insertado en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="9993e-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="9993e-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="9993e-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9993e-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9993e-123">Properties</span></span>

<span data-ttu-id="9993e-124">La clase **CIM \_ PhysicalPackage** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9993e-124">The **CIM\_PhysicalPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9993e-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9993e-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-128">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9993e-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9993e-129">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9993e-129">Short textual description of the object.</span></span>

<span data-ttu-id="9993e-130">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9993e-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-134">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9993e-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9993e-135">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="9993e-135">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9993e-136">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="9993e-136">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9993e-137">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-138">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="9993e-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-139">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="9993e-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-141">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="9993e-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="9993e-142">Profundidad del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="9993e-142">Depth of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="9993e-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9993e-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-146">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="9993e-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9993e-147">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9993e-147">Textual description of the object.</span></span>

<span data-ttu-id="9993e-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-149">**Height**</span><span class="sxs-lookup"><span data-stu-id="9993e-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-150">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="9993e-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-152">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="9993e-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="9993e-153">Alto del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="9993e-153">Height of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="9993e-154">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="9993e-154">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-155">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9993e-155">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9993e-157">Si **es true**, el paquete puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="9993e-157">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="9993e-158">Un paquete físico puede intercambiarse en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras se activa el paquete contenedor.</span><span class="sxs-lookup"><span data-stu-id="9993e-158">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="9993e-159">Por ejemplo, un componente de ventilador se puede diseñar para que se intercambie en caliente.</span><span class="sxs-lookup"><span data-stu-id="9993e-159">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="9993e-160">Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="9993e-160">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="9993e-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9993e-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-162">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9993e-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-164">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="9993e-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9993e-165">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="9993e-165">Date and time the object was installed.</span></span> <span data-ttu-id="9993e-166">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="9993e-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9993e-167">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-168">**Le**</span><span class="sxs-lookup"><span data-stu-id="9993e-168">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-171">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9993e-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9993e-172">Nombre de la organización que generó el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9993e-172">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="9993e-173">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-173">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="9993e-174">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-175">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="9993e-175">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-178">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9993e-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9993e-179">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9993e-179">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="9993e-180">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-181">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9993e-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-184">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9993e-184">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9993e-185">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="9993e-185">Label by which the object is known.</span></span> <span data-ttu-id="9993e-186">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="9993e-186">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9993e-187">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-188">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9993e-188">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9993e-191">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9993e-191">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="9993e-192">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="9993e-192">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="9993e-193">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="9993e-193">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="9993e-194">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-195">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="9993e-195">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-198">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9993e-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9993e-199">Número de pieza asignado por la organización que produjo o fabricó el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9993e-199">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="9993e-200">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-201">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="9993e-201">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-202">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9993e-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9993e-204">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="9993e-204">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="9993e-205">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-206">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="9993e-206">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-207">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9993e-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9993e-209">Si es **true**, el paquete está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado global.</span><span class="sxs-lookup"><span data-stu-id="9993e-209">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="9993e-210">Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="9993e-210">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="9993e-211">Si la potencia puede estar activada y se ha quitado el paquete, el elemento es extraíble y se puede intercambiar en caliente.</span><span class="sxs-lookup"><span data-stu-id="9993e-211">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="9993e-212">Por ejemplo, un chip de Procesador actualizable es extraíble.</span><span class="sxs-lookup"><span data-stu-id="9993e-212">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="9993e-213">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="9993e-213">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-214">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9993e-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9993e-216">Si es **true**, es posible reemplazar el elemento por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="9993e-216">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="9993e-217">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="9993e-217">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="9993e-218">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="9993e-218">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="9993e-219">Todos los componentes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="9993e-219">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="9993e-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="9993e-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-223">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9993e-223">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9993e-224">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9993e-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="9993e-225">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="9993e-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-229">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9993e-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9993e-230">Número de unidad de almacén para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9993e-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="9993e-231">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-232">**Estado**</span><span class="sxs-lookup"><span data-stu-id="9993e-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-233">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-235">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9993e-235">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9993e-236">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9993e-236">Current status of the object.</span></span>

<span data-ttu-id="9993e-237">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9993e-238">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9993e-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9993e-239">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="9993e-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9993e-240">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="9993e-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9993e-241">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="9993e-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9993e-242">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="9993e-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9993e-243">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="9993e-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9993e-244">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="9993e-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9993e-245">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="9993e-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9993e-246">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="9993e-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9993e-247">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="9993e-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9993e-248">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="9993e-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9993e-249">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="9993e-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9993e-250">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="9993e-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9993e-251">**Tag**</span><span class="sxs-lookup"><span data-stu-id="9993e-251">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-254">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9993e-254">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9993e-255">Cadena arbitraria que identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="9993e-255">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="9993e-256">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="9993e-256">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="9993e-257">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="9993e-257">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="9993e-258">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="9993e-258">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="9993e-259">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9993e-259">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="9993e-260">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="9993e-260">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="9993e-261">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-262">**Versión**</span><span class="sxs-lookup"><span data-stu-id="9993e-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-263">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9993e-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-265">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9993e-265">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9993e-266">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9993e-266">Version of the physical element.</span></span>

<span data-ttu-id="9993e-267">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-267">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9993e-268">**Peso**</span><span class="sxs-lookup"><span data-stu-id="9993e-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-269">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="9993e-269">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-271">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="9993e-271">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="9993e-272">Peso del paquete físico, en libras.</span><span class="sxs-lookup"><span data-stu-id="9993e-272">Weight of the physical package, in pounds.</span></span>

</dd> <dt>

<span data-ttu-id="9993e-273">**Width**</span><span class="sxs-lookup"><span data-stu-id="9993e-273">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9993e-274">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="9993e-274">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9993e-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9993e-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9993e-276">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="9993e-276">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="9993e-277">Ancho del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="9993e-277">Width of the physical package, in inches.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9993e-278">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9993e-278">Remarks</span></span>

<span data-ttu-id="9993e-279">La clase **CIM \_ PhysicalPackage** se deriva de [**\_ PhysicalElement de CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-279">The **CIM\_PhysicalPackage** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="9993e-280">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="9993e-280">WMI does not implement this class.</span></span> <span data-ttu-id="9993e-281">Para las clases WMI que se derivan de **\_ PhysicalPackage CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9993e-281">For WMI classes that are derived from **CIM\_PhysicalPackage**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9993e-282">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9993e-282">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9993e-283">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9993e-283">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9993e-284">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9993e-284">Requirements</span></span>



| <span data-ttu-id="9993e-285">Requisito</span><span class="sxs-lookup"><span data-stu-id="9993e-285">Requirement</span></span> | <span data-ttu-id="9993e-286">Value</span><span class="sxs-lookup"><span data-stu-id="9993e-286">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9993e-287">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9993e-287">Minimum supported client</span></span><br/> | <span data-ttu-id="9993e-288">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9993e-288">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9993e-289">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9993e-289">Minimum supported server</span></span><br/> | <span data-ttu-id="9993e-290">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9993e-290">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9993e-291">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9993e-291">Namespace</span></span><br/>                | <span data-ttu-id="9993e-292">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9993e-292">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9993e-293">MOF</span><span class="sxs-lookup"><span data-stu-id="9993e-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9993e-294"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9993e-294"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9993e-295">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9993e-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9993e-296"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9993e-296"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9993e-297">Vea también</span><span class="sxs-lookup"><span data-stu-id="9993e-297">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9993e-298">**\_PHYSICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9993e-298">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

