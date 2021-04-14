---
description: La \_ clase CIM PhysicalComponent representa un componente de bajo nivel o básico dentro de un paquete. Un elemento físico que no es un vínculo, conector o paquete es un descendiente (o miembro) de esta clase.
ms.assetid: 079874cd-5717-4662-a192-0ced16270bbd
ms.tgt_platform: multiple
title: CIM_PhysicalComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalComponent
- CIM_PhysicalComponent.Caption
- CIM_PhysicalComponent.Description
- CIM_PhysicalComponent.InstallDate
- CIM_PhysicalComponent.Name
- CIM_PhysicalComponent.Status
- CIM_PhysicalComponent.CreationClassName
- CIM_PhysicalComponent.Manufacturer
- CIM_PhysicalComponent.Model
- CIM_PhysicalComponent.OtherIdentifyingInfo
- CIM_PhysicalComponent.PartNumber
- CIM_PhysicalComponent.PoweredOn
- CIM_PhysicalComponent.SerialNumber
- CIM_PhysicalComponent.SKU
- CIM_PhysicalComponent.Tag
- CIM_PhysicalComponent.Version
- CIM_PhysicalComponent.HotSwappable
- CIM_PhysicalComponent.Removable
- CIM_PhysicalComponent.Replaceable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e7e1db2c1d314b2d45816801643912dcf3b31bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496396"
---
# <a name="cim_physicalcomponent-class"></a><span data-ttu-id="a93ae-104">\_Clase PhysicalComponent de CIM</span><span class="sxs-lookup"><span data-stu-id="a93ae-104">CIM\_PhysicalComponent class</span></span>

<span data-ttu-id="a93ae-105">La clase **CIM \_ PhysicalComponent** representa un componente de bajo nivel o básico dentro de un paquete.</span><span class="sxs-lookup"><span data-stu-id="a93ae-105">The **CIM\_PhysicalComponent** class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="a93ae-106">Un elemento físico que no es un vínculo, conector o paquete es un descendiente (o miembro) de esta clase.</span><span class="sxs-lookup"><span data-stu-id="a93ae-106">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span> <span data-ttu-id="a93ae-107">Por ejemplo, el conjunto de chips UART de una tarjeta módem interna sería una subclase (si se definen propiedades o asociaciones adicionales) o una instancia de **CIM \_ PhysicalComponent**.</span><span class="sxs-lookup"><span data-stu-id="a93ae-107">For example, the UART chipset on an internal modem card would be a subclass (if additional properties or associations are defined) or an instance of **CIM\_PhysicalComponent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a93ae-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a93ae-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a93ae-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a93ae-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a93ae-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a93ae-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a93ae-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a93ae-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a93ae-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a93ae-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B78-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalComponent : CIM_PhysicalElement
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
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
};
```

## <a name="members"></a><span data-ttu-id="a93ae-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="a93ae-113">Members</span></span>

<span data-ttu-id="a93ae-114">La clase **CIM \_ PhysicalComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a93ae-114">The **CIM\_PhysicalComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="a93ae-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a93ae-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a93ae-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a93ae-116">Properties</span></span>

<span data-ttu-id="a93ae-117">La clase **CIM \_ PhysicalComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a93ae-117">The **CIM\_PhysicalComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a93ae-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a93ae-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-121">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a93ae-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-122">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a93ae-122">A short textual description of the object.</span></span>

<span data-ttu-id="a93ae-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a93ae-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-127">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a93ae-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-128">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="a93ae-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a93ae-129">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="a93ae-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a93ae-130">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a93ae-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-134">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="a93ae-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-135">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a93ae-135">A textual description of the object.</span></span>

<span data-ttu-id="a93ae-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-137">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="a93ae-137">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-138">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a93ae-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-140">Si **es true**, el paquete puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="a93ae-140">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="a93ae-141">Un paquete físico puede intercambiarse en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras se activa el paquete contenedor.</span><span class="sxs-lookup"><span data-stu-id="a93ae-141">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="a93ae-142">Por ejemplo, un componente de ventilador se puede diseñar para que se intercambie en caliente.</span><span class="sxs-lookup"><span data-stu-id="a93ae-142">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="a93ae-143">Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="a93ae-143">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a93ae-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-145">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a93ae-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-147">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="a93ae-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-148">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="a93ae-148">Indicates when the object was installed.</span></span> <span data-ttu-id="a93ae-149">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="a93ae-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a93ae-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-151">**Le**</span><span class="sxs-lookup"><span data-stu-id="a93ae-151">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-154">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a93ae-154">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-155">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a93ae-155">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="a93ae-156">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-156">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="a93ae-157">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-157">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-158">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="a93ae-158">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-161">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a93ae-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-162">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a93ae-162">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="a93ae-163">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-163">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-164">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a93ae-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-167">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a93ae-167">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-168">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="a93ae-168">Label by which the object is known.</span></span> <span data-ttu-id="a93ae-169">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="a93ae-169">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a93ae-170">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-171">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a93ae-171">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-174">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a93ae-174">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="a93ae-175">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="a93ae-175">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="a93ae-176">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="a93ae-176">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="a93ae-177">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-177">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-178">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="a93ae-178">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-181">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a93ae-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-182">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a93ae-182">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="a93ae-183">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-183">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-184">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="a93ae-184">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-185">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a93ae-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-187">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="a93ae-187">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="a93ae-188">De lo contrario, está actualmente desactivado.</span><span class="sxs-lookup"><span data-stu-id="a93ae-188">Otherwise, it is currently off.</span></span>

<span data-ttu-id="a93ae-189">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-189">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-190">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="a93ae-190">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-191">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a93ae-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-193">Si es **true**, este elemento está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado global.</span><span class="sxs-lookup"><span data-stu-id="a93ae-193">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="a93ae-194">Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="a93ae-194">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="a93ae-195">Si la potencia puede estar activada y se ha quitado el paquete, el elemento es extraíble y se puede intercambiar en caliente.</span><span class="sxs-lookup"><span data-stu-id="a93ae-195">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="a93ae-196">Por ejemplo, un chip de Procesador actualizable es extraíble.</span><span class="sxs-lookup"><span data-stu-id="a93ae-196">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-197">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="a93ae-197">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-198">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a93ae-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-200">Si es **true**, es posible reemplazar el elemento por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="a93ae-200">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="a93ae-201">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="a93ae-201">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="a93ae-202">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="a93ae-202">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="a93ae-203">Todos los componentes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="a93ae-203">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-204">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="a93ae-204">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-205">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-207">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a93ae-207">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-208">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a93ae-208">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="a93ae-209">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-209">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-210">**SKU**</span><span class="sxs-lookup"><span data-stu-id="a93ae-210">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-211">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-213">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a93ae-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-214">Número de unidad de almacén para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a93ae-214">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="a93ae-215">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-216">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a93ae-216">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-219">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a93ae-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-220">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a93ae-220">String that indicates the current status of the object.</span></span> <span data-ttu-id="a93ae-221">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="a93ae-221">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a93ae-222">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="a93ae-222">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a93ae-223">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="a93ae-223">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a93ae-224">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="a93ae-224">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a93ae-225">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="a93ae-225">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a93ae-226">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="a93ae-226">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a93ae-227">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a93ae-228">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a93ae-228">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a93ae-229">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="a93ae-229">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a93ae-230">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="a93ae-230">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a93ae-231">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a93ae-231">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a93ae-232">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="a93ae-232">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a93ae-233">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="a93ae-233">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a93ae-234">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="a93ae-234">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a93ae-235">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="a93ae-235">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a93ae-236">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="a93ae-236">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a93ae-237">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="a93ae-237">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a93ae-238">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a93ae-238">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a93ae-239">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="a93ae-239">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a93ae-240">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="a93ae-240">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a93ae-241">**Tag**</span><span class="sxs-lookup"><span data-stu-id="a93ae-241">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-244">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a93ae-244">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-245">Identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="a93ae-245">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="a93ae-246">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="a93ae-246">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="a93ae-247">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="a93ae-247">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="a93ae-248">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="a93ae-248">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="a93ae-249">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a93ae-249">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="a93ae-250">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="a93ae-250">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="a93ae-251">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-251">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a93ae-252">**Versión**</span><span class="sxs-lookup"><span data-stu-id="a93ae-252">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a93ae-253">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a93ae-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a93ae-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a93ae-255">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a93ae-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a93ae-256">Indica la versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a93ae-256">Indicates the version of the physical element.</span></span>

<span data-ttu-id="a93ae-257">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a93ae-258">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a93ae-258">Remarks</span></span>

<span data-ttu-id="a93ae-259">La clase **CIM \_ PhysicalComponent** se deriva de [**\_ PhysicalElement de CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-259">The **CIM\_PhysicalComponent** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="a93ae-260">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="a93ae-260">WMI does not implement this class.</span></span> <span data-ttu-id="a93ae-261">Para las clases WMI derivadas de **CIM \_ PhysicalComponent**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a93ae-261">For WMI classes derived from **CIM\_PhysicalComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a93ae-262">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a93ae-262">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a93ae-263">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a93ae-263">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a93ae-264">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a93ae-264">Requirements</span></span>



| <span data-ttu-id="a93ae-265">Requisito</span><span class="sxs-lookup"><span data-stu-id="a93ae-265">Requirement</span></span> | <span data-ttu-id="a93ae-266">Value</span><span class="sxs-lookup"><span data-stu-id="a93ae-266">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a93ae-267">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a93ae-267">Minimum supported client</span></span><br/> | <span data-ttu-id="a93ae-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a93ae-268">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a93ae-269">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a93ae-269">Minimum supported server</span></span><br/> | <span data-ttu-id="a93ae-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a93ae-270">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a93ae-271">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a93ae-271">Namespace</span></span><br/>                | <span data-ttu-id="a93ae-272">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a93ae-272">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a93ae-273">MOF</span><span class="sxs-lookup"><span data-stu-id="a93ae-273">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a93ae-274"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a93ae-274"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a93ae-275">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a93ae-275">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a93ae-276"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a93ae-276"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a93ae-277">Vea también</span><span class="sxs-lookup"><span data-stu-id="a93ae-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a93ae-278">**\_PHYSICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a93ae-278">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

