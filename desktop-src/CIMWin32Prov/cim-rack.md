---
description: La \_ clase de bastidor CIM representa un bastidor (una trama física o un alojamiento) en el que se almacena el chasis. Normalmente, un bastidor representa el alojamiento; todos los componentes que funcionan están empaquetados en el chasis.
ms.assetid: 1e0273ce-2a09-4f75-a82e-d0555d6a831e
ms.tgt_platform: multiple
title: CIM_Rack (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack
- CIM_Rack.AudibleAlarm
- CIM_Rack.BreachDescription
- CIM_Rack.CableManagementStrategy
- CIM_Rack.Caption
- CIM_Rack.CountryDesignation
- CIM_Rack.CreationClassName
- CIM_Rack.Depth
- CIM_Rack.Description
- CIM_Rack.Height
- CIM_Rack.HotSwappable
- CIM_Rack.InstallDate
- CIM_Rack.LockPresent
- CIM_Rack.Manufacturer
- CIM_Rack.Model
- CIM_Rack.Name
- CIM_Rack.OtherIdentifyingInfo
- CIM_Rack.PartNumber
- CIM_Rack.PoweredOn
- CIM_Rack.Removable
- CIM_Rack.Replaceable
- CIM_Rack.SecurityBreach
- CIM_Rack.SerialNumber
- CIM_Rack.ServiceDescriptions
- CIM_Rack.ServicePhilosophy
- CIM_Rack.SKU
- CIM_Rack.Status
- CIM_Rack.Tag
- CIM_Rack.TypeOfRack
- CIM_Rack.Version
- CIM_Rack.VisibleAlarm
- CIM_Rack.Weight
- CIM_Rack.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2eb5234e8dd65d7df86acec7ab121ef961c2121
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807327"
---
# <a name="cim_rack-class"></a><span data-ttu-id="efbba-104">\_Clase de bastidor CIM</span><span class="sxs-lookup"><span data-stu-id="efbba-104">CIM\_Rack class</span></span>

<span data-ttu-id="efbba-105">La clase de **\_ bastidor CIM** representa un bastidor (una trama física o un alojamiento) en el que se almacena el chasis.</span><span class="sxs-lookup"><span data-stu-id="efbba-105">The **CIM\_Rack** class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="efbba-106">Normalmente, un bastidor representa el alojamiento; todos los componentes que funcionan están empaquetados en el chasis.</span><span class="sxs-lookup"><span data-stu-id="efbba-106">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="efbba-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="efbba-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="efbba-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="efbba-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="efbba-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="efbba-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="efbba-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="efbba-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="efbba-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efbba-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B71-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Rack : CIM_PhysicalFrame
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CountryDesignation;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  uint16   TypeOfRack;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="efbba-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="efbba-112">Members</span></span>

<span data-ttu-id="efbba-113">La clase de **\_ bastidor CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="efbba-113">The **CIM\_Rack** class has these types of members:</span></span>

-   [<span data-ttu-id="efbba-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="efbba-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="efbba-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="efbba-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="efbba-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="efbba-116">Methods</span></span>

<span data-ttu-id="efbba-117">La clase de **\_ bastidor CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="efbba-117">The **CIM\_Rack** class has these methods.</span></span>



| <span data-ttu-id="efbba-118">Método</span><span class="sxs-lookup"><span data-stu-id="efbba-118">Method</span></span>                                                        | <span data-ttu-id="efbba-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="efbba-119">Description</span></span>                                                                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efbba-120">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="efbba-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-rack.md) | <span data-ttu-id="efbba-121">Comprueba si el elemento físico al que se hace referencia puede estar contenido o insertado en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="efbba-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="efbba-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="efbba-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="efbba-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="efbba-123">Properties</span></span>

<span data-ttu-id="efbba-124">La clase de **\_ bastidor CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="efbba-124">The **CIM\_Rack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efbba-125">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="efbba-125">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-126">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="efbba-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbba-128">Si es **true**, el marco está equipado con una alarma audible.</span><span class="sxs-lookup"><span data-stu-id="efbba-128">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="efbba-129">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-129">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-130">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="efbba-130">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-133">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="efbba-133">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-134">Cadena de forma libre que proporciona información si la propiedad **SecurityBreach** indica que se ha producido una infracción o algún otro evento relacionado con la seguridad.</span><span class="sxs-lookup"><span data-stu-id="efbba-134">Free-form string that provides information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="efbba-135">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-135">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-136">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="efbba-136">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbba-139">Cadena de forma libre que contiene información sobre cómo se conectan los distintos cables y se empaquetan para el marco.</span><span class="sxs-lookup"><span data-stu-id="efbba-139">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="efbba-140">Con muchos cables de red, relacionados con el almacenamiento y de alimentación, la administración de cables puede ser un esfuerzo complejo y desafiante.</span><span class="sxs-lookup"><span data-stu-id="efbba-140">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="efbba-141">Esta propiedad de cadena contiene información para ayudar en el ensamblado y el servicio del marco.</span><span class="sxs-lookup"><span data-stu-id="efbba-141">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="efbba-142">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-142">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-143">**Caption**</span><span class="sxs-lookup"><span data-stu-id="efbba-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-146">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="efbba-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-147">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="efbba-147">Short textual description of the object.</span></span>

<span data-ttu-id="efbba-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-149">**CountryDesignation**</span><span class="sxs-lookup"><span data-stu-id="efbba-149">**CountryDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-152">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ estante CIM**.**TypeOfRack**")</span><span class="sxs-lookup"><span data-stu-id="efbba-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**TypeOfRack**")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-153">País o región para el que está diseñado el bastidor.</span><span class="sxs-lookup"><span data-stu-id="efbba-153">Country or region for which the rack is designed.</span></span> <span data-ttu-id="efbba-154">Las cadenas de código de país o región son las definidas por ISO/IEC 3166.</span><span class="sxs-lookup"><span data-stu-id="efbba-154">Country or region code strings are as defined by ISO/IEC 3166.</span></span> <span data-ttu-id="efbba-155">El tipo de bastidor se especifica en la propiedad **TypeOfRack** .</span><span class="sxs-lookup"><span data-stu-id="efbba-155">The rack type is specified in the **TypeOfRack** property.</span></span>

</dd> <dt>

<span data-ttu-id="efbba-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="efbba-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-159">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="efbba-159">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="efbba-160">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="efbba-160">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="efbba-161">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="efbba-161">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="efbba-162">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-162">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-163">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="efbba-163">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-164">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="efbba-164">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-166">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="efbba-166">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-167">Profundidad del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="efbba-167">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="efbba-168">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-169">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="efbba-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-172">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="efbba-172">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-173">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="efbba-173">Textual description of the object.</span></span>

<span data-ttu-id="efbba-174">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-175">**Height**</span><span class="sxs-lookup"><span data-stu-id="efbba-175">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-176">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="efbba-176">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-178">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("alto"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("EE. UU.")</span><span class="sxs-lookup"><span data-stu-id="efbba-178">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Height"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-179">Alto del paquete físico, usando la unidad de medida "U".</span><span class="sxs-lookup"><span data-stu-id="efbba-179">Height of the physical package, using the "U" unit of measure.</span></span> <span data-ttu-id="efbba-180">Una "U" es una unidad de medida estándar para el alto de un bastidor, o componente montable en bastidor, y es igual a 1,75 pulgadas o 4,445 centímetros.</span><span class="sxs-lookup"><span data-stu-id="efbba-180">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

<span data-ttu-id="efbba-181">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-181">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-182">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="efbba-182">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-183">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="efbba-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbba-185">Si **es true**, el paquete puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="efbba-185">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="efbba-186">Un paquete físico puede intercambiarse en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras se activa el paquete contenedor.</span><span class="sxs-lookup"><span data-stu-id="efbba-186">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="efbba-187">Por ejemplo, un componente de ventilador se puede diseñar para que se intercambie en caliente.</span><span class="sxs-lookup"><span data-stu-id="efbba-187">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="efbba-188">Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="efbba-188">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="efbba-189">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-189">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-190">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="efbba-190">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-191">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="efbba-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-193">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="efbba-193">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-194">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="efbba-194">Date and time the object was installed.</span></span> <span data-ttu-id="efbba-195">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="efbba-195">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="efbba-196">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-197">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="efbba-197">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-198">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="efbba-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbba-200">Si es **true**, el marco está protegido con un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="efbba-200">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="efbba-201">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-201">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-202">**Le**</span><span class="sxs-lookup"><span data-stu-id="efbba-202">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-205">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="efbba-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="efbba-206">Nombre de la organización que generó el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="efbba-206">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="efbba-207">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-207">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="efbba-208">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-208">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-209">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="efbba-209">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-212">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="efbba-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="efbba-213">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="efbba-213">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="efbba-214">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-214">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-215">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="efbba-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-218">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="efbba-218">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-219">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="efbba-219">Label by which the object is known.</span></span> <span data-ttu-id="efbba-220">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="efbba-220">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="efbba-221">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-222">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="efbba-222">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbba-225">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="efbba-225">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="efbba-226">Un ejemplo son los datos de código de barras asociados a un elemento que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="efbba-226">One example is bar-code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="efbba-227">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="efbba-228">Si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="efbba-228">If only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="efbba-229">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="efbba-229">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-232">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="efbba-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="efbba-233">Número de pieza asignado por la organización que produjo o fabricó el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="efbba-233">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="efbba-234">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-234">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-235">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="efbba-235">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-236">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="efbba-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbba-238">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="efbba-238">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="efbba-239">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-240">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="efbba-240">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-241">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="efbba-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbba-243">Si es **true**, este elemento está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado global.</span><span class="sxs-lookup"><span data-stu-id="efbba-243">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="efbba-244">Un paquete se considera extraíble incluso si la alimentación debe estar "desactivada" para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="efbba-244">A package is considered removable even if the power must be "off" to perform the removal.</span></span> <span data-ttu-id="efbba-245">Si la potencia puede estar "activada" y se ha quitado el paquete, el elemento es extraíble y puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="efbba-245">If the power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="efbba-246">Por ejemplo, una batería adicional en un equipo portátil es extraíble, como un paquete de unidad de disco insertado mediante conectores SCA; sin embargo, el último puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="efbba-246">For example, an extra battery in a laptop is removable, as is a disk-drive package inserted using SCA connectors; however, the latter can be hot-swapped.</span></span> <span data-ttu-id="efbba-247">La pantalla de un portátil no es extraíble, ni tampoco es una fuente de alimentación que no sea redundante.</span><span class="sxs-lookup"><span data-stu-id="efbba-247">A laptop's display is not removable, nor is a non-redundant power supply.</span></span> <span data-ttu-id="efbba-248">La eliminación de estos componentes afecta a la función del empaquetado global o es imposible debido a la estrecha integración del paquete.</span><span class="sxs-lookup"><span data-stu-id="efbba-248">Removing these components impacts the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="efbba-249">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-249">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-250">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="efbba-250">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-251">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="efbba-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbba-253">Si es **true**, es posible reemplazar el elemento por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="efbba-253">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="efbba-254">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="efbba-254">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="efbba-255">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="efbba-255">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="efbba-256">Todos los componentes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="efbba-256">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="efbba-257">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-257">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-258">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="efbba-258">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-259">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efbba-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-261">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Tabla global de contenedor físico DMTF \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="efbba-261">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-262">Indica si se intentó una infracción física del fotograma pero no se ha realizado correctamente, o si se ha intentado y se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="efbba-262">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span> <span data-ttu-id="efbba-263">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-263">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="efbba-264">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="efbba-264">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efbba-265">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="efbba-265">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="efbba-266">**Sin brecha** (3)</span><span class="sxs-lookup"><span data-stu-id="efbba-266">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="efbba-267">**Intento de infracción** (4)</span><span class="sxs-lookup"><span data-stu-id="efbba-267">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="efbba-268">**Infracción correcta** (5)</span><span class="sxs-lookup"><span data-stu-id="efbba-268">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efbba-269">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="efbba-269">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-270">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-272">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="efbba-272">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="efbba-273">Número asignado por el fabricante que se usa para identificar el bastidor.</span><span class="sxs-lookup"><span data-stu-id="efbba-273">Manufacturer-allocated number used to identify the rack.</span></span>

<span data-ttu-id="efbba-274">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-274">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-275">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="efbba-275">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-276">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="efbba-276">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="efbba-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-278">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="efbba-278">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-279">Cadenas de forma libre que proporcionan explicaciones detalladas para las entradas de la matriz **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="efbba-279">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="efbba-280">Tenga en cuenta que cada entrada de la matriz está relacionada con la entrada de **ServicePhilosophy** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="efbba-280">Note, each entry of the array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="efbba-281">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-281">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-282">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="efbba-282">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-283">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efbba-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="efbba-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-285">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="efbba-285">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-286">Indica si el marco se va a atender desde la parte superior, delantera, posterior o lateral; y si tienen bandejas deslizantes o laterales extraíbles, y si el fotograma se va a mover (por ejemplo, con rodillos).</span><span class="sxs-lookup"><span data-stu-id="efbba-286">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="efbba-287">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-287">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efbba-288">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="efbba-288">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="efbba-289">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="efbba-289">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="efbba-290">**Servicio desde arriba** (2)</span><span class="sxs-lookup"><span data-stu-id="efbba-290">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="efbba-291">**Servicio desde delante** (3)</span><span class="sxs-lookup"><span data-stu-id="efbba-291">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="efbba-292">**Servicio de atrás** (4)</span><span class="sxs-lookup"><span data-stu-id="efbba-292">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="efbba-293">**Servicio desde el lado** (5)</span><span class="sxs-lookup"><span data-stu-id="efbba-293">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="efbba-294">**Bandejas deslizantes** (6)</span><span class="sxs-lookup"><span data-stu-id="efbba-294">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="efbba-295">**Lados extraíbles** (7)</span><span class="sxs-lookup"><span data-stu-id="efbba-295">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="efbba-296">**Móvil** (8)</span><span class="sxs-lookup"><span data-stu-id="efbba-296">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efbba-297">**SKU**</span><span class="sxs-lookup"><span data-stu-id="efbba-297">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-298">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-300">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="efbba-300">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="efbba-301">Número de unidad de almacén para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="efbba-301">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="efbba-302">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-303">**Estado**</span><span class="sxs-lookup"><span data-stu-id="efbba-303">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-306">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="efbba-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-307">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="efbba-307">Current status of the object.</span></span> <span data-ttu-id="efbba-308">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="efbba-309">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="efbba-309">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="efbba-310">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="efbba-310">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="efbba-311">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="efbba-311">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="efbba-312">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="efbba-312">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efbba-313">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="efbba-313">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="efbba-314">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="efbba-314">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="efbba-315">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="efbba-315">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="efbba-316">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="efbba-316">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="efbba-317">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="efbba-317">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="efbba-318">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="efbba-318">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="efbba-319">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="efbba-319">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="efbba-320">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="efbba-320">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="efbba-321">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="efbba-321">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efbba-322">**Tag**</span><span class="sxs-lookup"><span data-stu-id="efbba-322">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-323">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-325">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="efbba-325">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="efbba-326">Cadena arbitraria que identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="efbba-326">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="efbba-327">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="efbba-327">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="efbba-328">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="efbba-328">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="efbba-329">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="efbba-329">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="efbba-330">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="efbba-330">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="efbba-331">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="efbba-331">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="efbba-332">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-332">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-333">**TypeOfRack**</span><span class="sxs-lookup"><span data-stu-id="efbba-333">**TypeOfRack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-334">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efbba-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-336">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ estante CIM**.**CountryDesignation**")</span><span class="sxs-lookup"><span data-stu-id="efbba-336">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**CountryDesignation**")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-337">Tipo de bastidor.</span><span class="sxs-lookup"><span data-stu-id="efbba-337">Type of rack.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efbba-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="efbba-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>

<span data-ttu-id="efbba-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Estándar 19 pulgadas** (1)</span><span class="sxs-lookup"><span data-stu-id="efbba-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Standard 19 Inch** (1)</span></span>


</dt> <dd>

<span data-ttu-id="efbba-340">Estándar de 19 pulgadas</span><span class="sxs-lookup"><span data-stu-id="efbba-340">Standard 19-inch</span></span>

</dd> <dt>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>

<span data-ttu-id="efbba-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span><span class="sxs-lookup"><span data-stu-id="efbba-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>

<span data-ttu-id="efbba-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Estante de equipo** (3)</span><span class="sxs-lookup"><span data-stu-id="efbba-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Equipment Shelf** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>

<span data-ttu-id="efbba-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**No estándar** (4)</span><span class="sxs-lookup"><span data-stu-id="efbba-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Non-Standard** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efbba-344">**Versión**</span><span class="sxs-lookup"><span data-stu-id="efbba-344">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-345">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efbba-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-347">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="efbba-347">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="efbba-348">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="efbba-348">Version of the physical element.</span></span>

<span data-ttu-id="efbba-349">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-349">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-350">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="efbba-350">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-351">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="efbba-351">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbba-353">Si **es true**, el equipo incluye una alarma visible.</span><span class="sxs-lookup"><span data-stu-id="efbba-353">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="efbba-354">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-354">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-355">**Peso**</span><span class="sxs-lookup"><span data-stu-id="efbba-355">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-356">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="efbba-356">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-358">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="efbba-358">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-359">Peso del paquete físico, en libras.</span><span class="sxs-lookup"><span data-stu-id="efbba-359">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="efbba-360">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-360">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="efbba-361">**Width**</span><span class="sxs-lookup"><span data-stu-id="efbba-361">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbba-362">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="efbba-362">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="efbba-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efbba-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbba-364">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="efbba-364">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="efbba-365">Ancho del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="efbba-365">Width of the physical package, in inches.</span></span>

<span data-ttu-id="efbba-366">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-366">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efbba-367">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efbba-367">Remarks</span></span>

<span data-ttu-id="efbba-368">La clase de **\_ bastidor CIM** se deriva [**de \_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="efbba-368">The **CIM\_Rack** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="efbba-369">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="efbba-369">WMI does not implement this class.</span></span>

<span data-ttu-id="efbba-370">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="efbba-370">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="efbba-371">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="efbba-371">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="efbba-372">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efbba-372">Requirements</span></span>



| <span data-ttu-id="efbba-373">Requisito</span><span class="sxs-lookup"><span data-stu-id="efbba-373">Requirement</span></span> | <span data-ttu-id="efbba-374">Value</span><span class="sxs-lookup"><span data-stu-id="efbba-374">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efbba-375">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efbba-375">Minimum supported client</span></span><br/> | <span data-ttu-id="efbba-376">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efbba-376">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="efbba-377">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efbba-377">Minimum supported server</span></span><br/> | <span data-ttu-id="efbba-378">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efbba-378">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="efbba-379">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="efbba-379">Namespace</span></span><br/>                | <span data-ttu-id="efbba-380">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="efbba-380">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="efbba-381">MOF</span><span class="sxs-lookup"><span data-stu-id="efbba-381">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efbba-382"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efbba-382"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="efbba-383">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="efbba-383">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efbba-384"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efbba-384"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efbba-385">Vea también</span><span class="sxs-lookup"><span data-stu-id="efbba-385">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efbba-386">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="efbba-386">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

