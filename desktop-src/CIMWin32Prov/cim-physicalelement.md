---
description: Las \_ subclases PhysicalElement de CIM definen cualquier componente de un sistema que tenga una identidad física distinta. Las instancias de esta clase se pueden definir en términos de etiquetas que se pueden adjuntar físicamente al objeto.
ms.assetid: 7ba6d1a9-f449-4ae2-a37c-517245bea39e
ms.tgt_platform: multiple
title: CIM_PhysicalElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElement
- CIM_PhysicalElement.Caption
- CIM_PhysicalElement.Description
- CIM_PhysicalElement.InstallDate
- CIM_PhysicalElement.Name
- CIM_PhysicalElement.Status
- CIM_PhysicalElement.CreationClassName
- CIM_PhysicalElement.Manufacturer
- CIM_PhysicalElement.Model
- CIM_PhysicalElement.OtherIdentifyingInfo
- CIM_PhysicalElement.PartNumber
- CIM_PhysicalElement.PoweredOn
- CIM_PhysicalElement.SerialNumber
- CIM_PhysicalElement.SKU
- CIM_PhysicalElement.Tag
- CIM_PhysicalElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5afeda74789bc492aac3d37629b64385b8734f60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538493"
---
# <a name="cim_physicalelement-class"></a><span data-ttu-id="c73ea-104">\_Clase PhysicalElement de CIM</span><span class="sxs-lookup"><span data-stu-id="c73ea-104">CIM\_PhysicalElement class</span></span>

<span data-ttu-id="c73ea-105">Las subclases **\_ PhysicalElement de CIM** definen cualquier componente de un sistema que tenga una identidad física distinta.</span><span class="sxs-lookup"><span data-stu-id="c73ea-105">The **CIM\_PhysicalElement** subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="c73ea-106">Las instancias de esta clase se pueden definir en términos de etiquetas que se pueden adjuntar físicamente al objeto.</span><span class="sxs-lookup"><span data-stu-id="c73ea-106">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span> <span data-ttu-id="c73ea-107">No se considera que todos los procesos, archivos y dispositivos lógicos sean elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="c73ea-107">All processes, files, and logical devices are not considered to be physical elements.</span></span> <span data-ttu-id="c73ea-108">Por ejemplo, no es posible adjuntar una etiqueta a un módem. solo es posible adjuntar una etiqueta a la tarjeta que implementa el módem.</span><span class="sxs-lookup"><span data-stu-id="c73ea-108">For example, it is not possible to attach a label to a modem; it is only possible to attach a label to the card that implements the modem.</span></span> <span data-ttu-id="c73ea-109">La misma tarjeta también podría implementar un adaptador de LAN.</span><span class="sxs-lookup"><span data-stu-id="c73ea-109">The same card could also implement a LAN adapter.</span></span>

<span data-ttu-id="c73ea-110">Los elementos del sistema administrado tangible (normalmente elementos de hardware) tienen una manifestación física.</span><span class="sxs-lookup"><span data-stu-id="c73ea-110">Tangible managed system elements (usually hardware items) have a physical manifestation.</span></span> <span data-ttu-id="c73ea-111">Un elemento del sistema administrado no es necesariamente un componente discreto.</span><span class="sxs-lookup"><span data-stu-id="c73ea-111">A managed system element is not necessarily a discrete component.</span></span> <span data-ttu-id="c73ea-112">Por ejemplo, es posible que una sola tarjeta (un tipo de elemento físico) hospede más de un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c73ea-112">For example, it is possible for a single card (a type of physical element) to host more than one logical device.</span></span> <span data-ttu-id="c73ea-113">La tarjeta se representaría mediante un único elemento físico asociado a varios dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="c73ea-113">The card would be represented by a single physical element associated with multiple logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c73ea-114">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c73ea-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c73ea-115">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c73ea-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c73ea-116">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c73ea-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c73ea-117">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c73ea-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c73ea-118">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c73ea-118">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B61-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElement : CIM_ManagedSystemElement
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
};
```

## <a name="members"></a><span data-ttu-id="c73ea-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="c73ea-119">Members</span></span>

<span data-ttu-id="c73ea-120">La clase **CIM \_ PhysicalElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c73ea-120">The **CIM\_PhysicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="c73ea-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c73ea-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c73ea-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c73ea-122">Properties</span></span>

<span data-ttu-id="c73ea-123">La clase **CIM \_ PhysicalElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c73ea-123">The **CIM\_PhysicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c73ea-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c73ea-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-127">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c73ea-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-128">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c73ea-128">A short textual description of the object.</span></span>

<span data-ttu-id="c73ea-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c73ea-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c73ea-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-133">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c73ea-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-134">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="c73ea-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c73ea-135">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="c73ea-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-136">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c73ea-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-139">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="c73ea-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-140">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c73ea-140">A textual description of the object.</span></span>

<span data-ttu-id="c73ea-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c73ea-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c73ea-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-143">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c73ea-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-145">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="c73ea-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-146">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="c73ea-146">Indicates when the object was installed.</span></span> <span data-ttu-id="c73ea-147">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="c73ea-147">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c73ea-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c73ea-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-149">**Le**</span><span class="sxs-lookup"><span data-stu-id="c73ea-149">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-152">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c73ea-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-153">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c73ea-153">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="c73ea-154">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="c73ea-154">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-155">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="c73ea-155">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-158">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c73ea-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-159">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c73ea-159">Name by which the physical element is generally known.</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-160">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c73ea-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-163">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c73ea-163">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-164">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="c73ea-164">Label by which the object is known.</span></span> <span data-ttu-id="c73ea-165">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="c73ea-165">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c73ea-166">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c73ea-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-167">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c73ea-167">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-170">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c73ea-170">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="c73ea-171">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="c73ea-171">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="c73ea-172">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="c73ea-172">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-173">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="c73ea-173">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-176">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c73ea-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-177">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c73ea-177">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-178">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="c73ea-178">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-179">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c73ea-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-181">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="c73ea-181">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="c73ea-182">De lo contrario, está actualmente desactivado.</span><span class="sxs-lookup"><span data-stu-id="c73ea-182">Otherwise, it is currently off.</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-183">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="c73ea-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-186">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c73ea-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-187">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c73ea-187">Manufacturer-allocated number used to identify the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-188">**SKU**</span><span class="sxs-lookup"><span data-stu-id="c73ea-188">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-191">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c73ea-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-192">Número de unidad de almacén para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c73ea-192">Stock-keeping unit number for this physical element.</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-193">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c73ea-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-196">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c73ea-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-197">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c73ea-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="c73ea-198">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="c73ea-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c73ea-199">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="c73ea-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c73ea-200">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="c73ea-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c73ea-201">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="c73ea-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c73ea-202">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="c73ea-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c73ea-203">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="c73ea-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c73ea-204">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c73ea-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c73ea-205">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c73ea-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c73ea-206">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="c73ea-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c73ea-207">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="c73ea-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c73ea-208">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c73ea-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c73ea-209">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="c73ea-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c73ea-210">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="c73ea-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c73ea-211">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="c73ea-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c73ea-212">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="c73ea-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c73ea-213">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="c73ea-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c73ea-214">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="c73ea-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c73ea-215">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c73ea-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c73ea-216">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="c73ea-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c73ea-217">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="c73ea-217">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c73ea-218">**Tag**</span><span class="sxs-lookup"><span data-stu-id="c73ea-218">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-221">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c73ea-221">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-222">Identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="c73ea-222">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="c73ea-223">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="c73ea-223">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="c73ea-224">La clave de **\_ PhysicalElement de CIM** se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="c73ea-224">The key for **CIM\_PhysicalElement** is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="c73ea-225">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="c73ea-225">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="c73ea-226">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c73ea-226">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="c73ea-227">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="c73ea-227">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="c73ea-228">**Versión**</span><span class="sxs-lookup"><span data-stu-id="c73ea-228">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c73ea-229">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c73ea-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c73ea-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c73ea-231">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c73ea-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c73ea-232">Indica la versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c73ea-232">Indicates the version of the physical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c73ea-233">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c73ea-233">Remarks</span></span>

<span data-ttu-id="c73ea-234">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="c73ea-234">WMI does not implement this class.</span></span> <span data-ttu-id="c73ea-235">Para las clases WMI derivadas de **CIM \_ PhysicalElement**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c73ea-235">For WMI classes derived from **CIM\_PhysicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c73ea-236">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c73ea-236">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c73ea-237">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c73ea-237">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c73ea-238">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c73ea-238">Requirements</span></span>



| <span data-ttu-id="c73ea-239">Requisito</span><span class="sxs-lookup"><span data-stu-id="c73ea-239">Requirement</span></span> | <span data-ttu-id="c73ea-240">Value</span><span class="sxs-lookup"><span data-stu-id="c73ea-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c73ea-241">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c73ea-241">Minimum supported client</span></span><br/> | <span data-ttu-id="c73ea-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c73ea-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c73ea-243">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c73ea-243">Minimum supported server</span></span><br/> | <span data-ttu-id="c73ea-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c73ea-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c73ea-245">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c73ea-245">Namespace</span></span><br/>                | <span data-ttu-id="c73ea-246">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c73ea-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c73ea-247">MOF</span><span class="sxs-lookup"><span data-stu-id="c73ea-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c73ea-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c73ea-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c73ea-249">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c73ea-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c73ea-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c73ea-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c73ea-251">Vea también</span><span class="sxs-lookup"><span data-stu-id="c73ea-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c73ea-252">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="c73ea-252">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

