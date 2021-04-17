---
description: La \_ clase de tarjeta CIM representa un tipo de contenedor físico que se puede conectar a otra tarjeta o panel de hospedaje, o es en sí mismo una placa de hospedaje o placa base en un chasis.
ms.assetid: edbbfe43-c8e8-4cde-9507-e0a248c15ca7
ms.tgt_platform: multiple
title: CIM_Card (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card
- CIM_Card.Caption
- CIM_Card.Description
- CIM_Card.InstallDate
- CIM_Card.Name
- CIM_Card.Status
- CIM_Card.CreationClassName
- CIM_Card.Manufacturer
- CIM_Card.Model
- CIM_Card.OtherIdentifyingInfo
- CIM_Card.PartNumber
- CIM_Card.PoweredOn
- CIM_Card.SerialNumber
- CIM_Card.SKU
- CIM_Card.Tag
- CIM_Card.Version
- CIM_Card.Depth
- CIM_Card.Height
- CIM_Card.HotSwappable
- CIM_Card.Removable
- CIM_Card.Replaceable
- CIM_Card.Weight
- CIM_Card.Width
- CIM_Card.HostingBoard
- CIM_Card.RequirementsDescription
- CIM_Card.RequiresDaughterBoard
- CIM_Card.SlotLayout
- CIM_Card.SpecialRequirements
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b10478e5d0e34020f64d8775e857d9fa6af94d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659636"
---
# <a name="cim_card-class"></a><span data-ttu-id="9a987-103">\_Clase de tarjeta CIM</span><span class="sxs-lookup"><span data-stu-id="9a987-103">CIM\_Card class</span></span>

<span data-ttu-id="9a987-104">La clase de **\_ tarjeta CIM** representa un tipo de contenedor físico que se puede conectar a otra tarjeta o panel de hospedaje, o es en sí mismo una placa de hospedaje o placa base en un chasis.</span><span class="sxs-lookup"><span data-stu-id="9a987-104">The **CIM\_Card** class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="9a987-105">Esta clase incluye cualquier paquete capaz de llevar señales y proporcionar un punto de montaje para los componentes físicos, como chips u otros paquetes físicos, como otras tarjetas.</span><span class="sxs-lookup"><span data-stu-id="9a987-105">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a987-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9a987-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9a987-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9a987-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9a987-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9a987-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9a987-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9a987-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a987-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a987-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B76-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Card : CIM_PhysicalPackage
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
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  HostingBoard;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SlotLayout;
  boolean  SpecialRequirements;
};
```

## <a name="members"></a><span data-ttu-id="9a987-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9a987-111">Members</span></span>

<span data-ttu-id="9a987-112">La clase **CIM \_ Card** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9a987-112">The **CIM\_Card** class has these types of members:</span></span>

-   [<span data-ttu-id="9a987-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="9a987-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="9a987-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a987-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9a987-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="9a987-115">Methods</span></span>

<span data-ttu-id="9a987-116">La clase **CIM \_ Card** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9a987-116">The **CIM\_Card** class has these methods.</span></span>



| <span data-ttu-id="9a987-117">Método</span><span class="sxs-lookup"><span data-stu-id="9a987-117">Method</span></span>                                                        | <span data-ttu-id="9a987-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a987-118">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a987-119">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="9a987-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-card.md) | <span data-ttu-id="9a987-120">Comprueba si el elemento físico al que se hace referencia puede incluirse o insertarse en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="9a987-120">Verifies whether the referenced physical element may be contained by or inserted into the physical package.</span></span> <span data-ttu-id="9a987-121">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="9a987-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9a987-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a987-122">Properties</span></span>

<span data-ttu-id="9a987-123">La clase **CIM \_ Card** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9a987-123">The **CIM\_Card** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a987-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9a987-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-127">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9a987-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9a987-128">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a987-128">A short textual description of the object.</span></span>

<span data-ttu-id="9a987-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9a987-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-133">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9a987-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a987-134">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="9a987-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9a987-135">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="9a987-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9a987-136">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-136">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-137">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="9a987-137">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-138">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="9a987-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-140">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="9a987-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="9a987-141">Profundidad del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="9a987-141">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="9a987-142">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-142">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a987-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-146">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="9a987-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9a987-147">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a987-147">A textual description of the object.</span></span>

<span data-ttu-id="9a987-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-149">**Height**</span><span class="sxs-lookup"><span data-stu-id="9a987-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-150">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="9a987-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-152">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="9a987-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="9a987-153">Alto del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="9a987-153">Height of the physical package, in inches.</span></span>

<span data-ttu-id="9a987-154">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-154">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-155">**HostingBoard**</span><span class="sxs-lookup"><span data-stu-id="9a987-155">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-156">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9a987-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a987-158">Si es **true**, esta tarjeta es una placa base o, más genéricamente, una placa base en un chasis.</span><span class="sxs-lookup"><span data-stu-id="9a987-158">If **TRUE**, this card is a motherboard or, more generically, a baseboard in a chassis.</span></span>

</dd> <dt>

<span data-ttu-id="9a987-159">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="9a987-159">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-160">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9a987-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a987-162">Si **es true**, el paquete puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="9a987-162">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="9a987-163">Un paquete físico puede intercambiarse en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras se activa el paquete contenedor.</span><span class="sxs-lookup"><span data-stu-id="9a987-163">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="9a987-164">Por ejemplo, un componente de ventilador se puede diseñar para que se intercambie en caliente.</span><span class="sxs-lookup"><span data-stu-id="9a987-164">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="9a987-165">Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="9a987-165">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="9a987-166">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-166">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-167">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9a987-167">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-168">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9a987-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-170">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="9a987-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9a987-171">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="9a987-171">Indicates when the object was installed.</span></span> <span data-ttu-id="9a987-172">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="9a987-172">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9a987-173">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-174">**Le**</span><span class="sxs-lookup"><span data-stu-id="9a987-174">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-177">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9a987-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a987-178">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9a987-178">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="9a987-179">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-179">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="9a987-180">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-181">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="9a987-181">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-184">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9a987-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a987-185">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9a987-185">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="9a987-186">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-186">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-187">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9a987-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-190">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9a987-190">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9a987-191">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="9a987-191">Label by which the object is known.</span></span> <span data-ttu-id="9a987-192">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="9a987-192">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9a987-193">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-194">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9a987-194">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a987-197">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9a987-197">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="9a987-198">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="9a987-198">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="9a987-199">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="9a987-199">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="9a987-200">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-201">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="9a987-201">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-204">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9a987-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a987-205">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9a987-205">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="9a987-206">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-207">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="9a987-207">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-208">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9a987-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a987-210">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="9a987-210">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="9a987-211">De lo contrario, está actualmente desactivado.</span><span class="sxs-lookup"><span data-stu-id="9a987-211">Otherwise, it is currently off.</span></span>

<span data-ttu-id="9a987-212">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-213">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="9a987-213">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-214">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9a987-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a987-216">Si es **true**, el paquete está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado global.</span><span class="sxs-lookup"><span data-stu-id="9a987-216">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="9a987-217">Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="9a987-217">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="9a987-218">Si la potencia puede estar activada y se ha quitado el paquete, el elemento es extraíble y se puede intercambiar en caliente.</span><span class="sxs-lookup"><span data-stu-id="9a987-218">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="9a987-219">Por ejemplo, un chip de Procesador actualizable es extraíble.</span><span class="sxs-lookup"><span data-stu-id="9a987-219">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="9a987-220">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-220">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-221">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="9a987-221">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-222">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9a987-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a987-224">Si es **true**, es posible reemplazar el elemento por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="9a987-224">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="9a987-225">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="9a987-225">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="9a987-226">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="9a987-226">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="9a987-227">Todos los componentes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="9a987-227">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="9a987-228">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-228">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-229">**RequirementsDescription**</span><span class="sxs-lookup"><span data-stu-id="9a987-229">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-232">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ tarjeta CIM**.**SpecialRequirements**")</span><span class="sxs-lookup"><span data-stu-id="9a987-232">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="9a987-233">Cadena de forma libre que describe las formas en que la tarjeta es única físicamente desde otras tarjetas.</span><span class="sxs-lookup"><span data-stu-id="9a987-233">Free-form string that describes the ways in which the card is physically unique from other cards.</span></span> <span data-ttu-id="9a987-234">Esta propiedad solo tiene significado cuando la propiedad booleana correspondiente, **SpecialRequirements**, se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="9a987-234">This property only has meaning when the corresponding Boolean property, **SpecialRequirements**, is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="9a987-235">**RequiresDaughterBoard**</span><span class="sxs-lookup"><span data-stu-id="9a987-235">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-236">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9a987-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a987-238">Si es **true**, para que funcione correctamente, se requiere al menos una tarjeta daughterboard o auxiliar.</span><span class="sxs-lookup"><span data-stu-id="9a987-238">If **TRUE**, to function properly, at least one daughterboard or auxiliary card is required.</span></span>

</dd> <dt>

<span data-ttu-id="9a987-239">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="9a987-239">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-242">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9a987-242">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a987-243">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9a987-243">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="9a987-244">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-244">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-245">**SKU**</span><span class="sxs-lookup"><span data-stu-id="9a987-245">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-248">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9a987-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a987-249">Número de unidad de almacén para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9a987-249">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="9a987-250">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-250">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-251">**SlotLayout**</span><span class="sxs-lookup"><span data-stu-id="9a987-251">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a987-254">Cadena de forma libre que describe el posicionamiento de la ranura, el uso típico, las restricciones, el espaciado de ranura individual u otra información pertinente para las ranuras de una tarjeta.</span><span class="sxs-lookup"><span data-stu-id="9a987-254">Free-form string that describes the slot positioning, typical usage, restrictions, individual slot spacings, or other pertinent information for the slots on a card.</span></span>

</dd> <dt>

<span data-ttu-id="9a987-255">**SpecialRequirements**</span><span class="sxs-lookup"><span data-stu-id="9a987-255">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-256">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9a987-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-258">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ tarjeta CIM**.**RequirementsDescription**")</span><span class="sxs-lookup"><span data-stu-id="9a987-258">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="9a987-259">Si es **true**, la tarjeta es única físicamente desde otras tarjetas del mismo tipo y, por lo tanto, requiere una ranura especial.</span><span class="sxs-lookup"><span data-stu-id="9a987-259">If **TRUE**, the card is physically unique from other cards of the same type and, therefore, requires a special slot.</span></span> <span data-ttu-id="9a987-260">Por ejemplo, una tarjeta de doble ancho requiere dos ranuras.</span><span class="sxs-lookup"><span data-stu-id="9a987-260">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="9a987-261">Otro ejemplo es cuando se puede usar una determinada tarjeta para la misma función general que otras tarjetas, pero requiere una ranura especial (extra larga, por ejemplo); sin embargo, se pueden colocar otras tarjetas en cualquier ranura disponible.</span><span class="sxs-lookup"><span data-stu-id="9a987-261">Another example is when a certain card can be used for the same general function as other cards, but requires a special slot (extra long, for example); whereas, other cards can be placed in any available slot.</span></span> <span data-ttu-id="9a987-262">Si **es true**, la propiedad **RequirementsDescription** correspondiente debe especificar la naturaleza de la unicidad o el propósito de la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="9a987-262">If **TRUE**, the corresponding **RequirementsDescription** property should specify the nature of the uniqueness or purpose of the card.</span></span>

</dd> <dt>

<span data-ttu-id="9a987-263">**Estado**</span><span class="sxs-lookup"><span data-stu-id="9a987-263">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-266">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9a987-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9a987-267">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a987-267">String that indicates the current status of the object.</span></span> <span data-ttu-id="9a987-268">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="9a987-268">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9a987-269">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="9a987-269">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9a987-270">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="9a987-270">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9a987-271">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="9a987-271">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9a987-272">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="9a987-272">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9a987-273">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="9a987-273">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9a987-274">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-274">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9a987-275">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9a987-275">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9a987-276">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="9a987-276">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9a987-277">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="9a987-277">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9a987-278">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="9a987-278">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9a987-279">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="9a987-279">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9a987-280">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="9a987-280">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9a987-281">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="9a987-281">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9a987-282">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="9a987-282">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9a987-283">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="9a987-283">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9a987-284">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="9a987-284">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9a987-285">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="9a987-285">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9a987-286">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="9a987-286">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9a987-287">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="9a987-287">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9a987-288">**Tag**</span><span class="sxs-lookup"><span data-stu-id="9a987-288">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-291">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9a987-291">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a987-292">Identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="9a987-292">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="9a987-293">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="9a987-293">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="9a987-294">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="9a987-294">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="9a987-295">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="9a987-295">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="9a987-296">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9a987-296">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="9a987-297">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="9a987-297">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="9a987-298">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-299">**Versión**</span><span class="sxs-lookup"><span data-stu-id="9a987-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a987-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-302">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9a987-302">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a987-303">Indica la versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="9a987-303">Indicates the version of the physical element.</span></span>

<span data-ttu-id="9a987-304">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-304">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-305">**Peso**</span><span class="sxs-lookup"><span data-stu-id="9a987-305">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-306">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="9a987-306">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-308">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="9a987-308">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="9a987-309">Peso del paquete físico, en libras.</span><span class="sxs-lookup"><span data-stu-id="9a987-309">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="9a987-310">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-310">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a987-311">**Width**</span><span class="sxs-lookup"><span data-stu-id="9a987-311">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a987-312">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="9a987-312">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9a987-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a987-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a987-314">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="9a987-314">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="9a987-315">Ancho del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="9a987-315">Width of the physical package, in inches.</span></span>

<span data-ttu-id="9a987-316">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-316">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a987-317">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a987-317">Remarks</span></span>

<span data-ttu-id="9a987-318">La clase **CIM \_ Card** se deriva de [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-318">The **CIM\_Card** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="9a987-319">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="9a987-319">WMI does not implement this class.</span></span> <span data-ttu-id="9a987-320">Para obtener más información acerca de las clases derivadas de la **\_ tarjeta CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-320">For more information about classes derived from **CIM\_Card**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9a987-321">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9a987-321">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9a987-322">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9a987-322">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a987-323">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a987-323">Requirements</span></span>



| <span data-ttu-id="9a987-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a987-324">Requirement</span></span> | <span data-ttu-id="9a987-325">Value</span><span class="sxs-lookup"><span data-stu-id="9a987-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a987-326">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a987-326">Minimum supported client</span></span><br/> | <span data-ttu-id="9a987-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a987-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a987-328">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a987-328">Minimum supported server</span></span><br/> | <span data-ttu-id="9a987-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a987-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a987-330">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9a987-330">Namespace</span></span><br/>                | <span data-ttu-id="9a987-331">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9a987-331">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a987-332">MOF</span><span class="sxs-lookup"><span data-stu-id="9a987-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a987-333"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a987-333"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a987-334">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a987-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a987-335"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a987-335"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a987-336">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a987-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a987-337">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="9a987-337">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

