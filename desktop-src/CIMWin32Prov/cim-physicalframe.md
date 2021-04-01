---
description: La \_ clase CIM PhysicalFrame es una clase primaria de bastidores, chasis y otros alojamientos de fotogramas, tal y como se definen en las clases de extensión.
ms.assetid: 571c8ca2-1644-4060-8d89-d9625a591f86
ms.tgt_platform: multiple
title: CIM_PhysicalFrame (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame
- CIM_PhysicalFrame.AudibleAlarm
- CIM_PhysicalFrame.BreachDescription
- CIM_PhysicalFrame.CableManagementStrategy
- CIM_PhysicalFrame.Caption
- CIM_PhysicalFrame.CreationClassName
- CIM_PhysicalFrame.Depth
- CIM_PhysicalFrame.Description
- CIM_PhysicalFrame.Height
- CIM_PhysicalFrame.HotSwappable
- CIM_PhysicalFrame.InstallDate
- CIM_PhysicalFrame.LockPresent
- CIM_PhysicalFrame.Manufacturer
- CIM_PhysicalFrame.Model
- CIM_PhysicalFrame.Name
- CIM_PhysicalFrame.OtherIdentifyingInfo
- CIM_PhysicalFrame.PartNumber
- CIM_PhysicalFrame.PoweredOn
- CIM_PhysicalFrame.Removable
- CIM_PhysicalFrame.Replaceable
- CIM_PhysicalFrame.SecurityBreach
- CIM_PhysicalFrame.SerialNumber
- CIM_PhysicalFrame.ServiceDescriptions
- CIM_PhysicalFrame.ServicePhilosophy
- CIM_PhysicalFrame.SKU
- CIM_PhysicalFrame.Status
- CIM_PhysicalFrame.Tag
- CIM_PhysicalFrame.Version
- CIM_PhysicalFrame.VisibleAlarm
- CIM_PhysicalFrame.Weight
- CIM_PhysicalFrame.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b445c928412bc475a3269ba59be48395b254efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153378"
---
# <a name="cim_physicalframe-class"></a><span data-ttu-id="f9fd4-103">\_Clase PhysicalFrame de CIM</span><span class="sxs-lookup"><span data-stu-id="f9fd4-103">CIM\_PhysicalFrame class</span></span>

<span data-ttu-id="f9fd4-104">La clase **CIM \_ PhysicalFrame** es una clase primaria de bastidores, chasis y otros alojamientos de fotogramas, tal y como se definen en las clases de extensión.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-104">The **CIM\_PhysicalFrame** class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="f9fd4-105">En esta clase primaria se incluyen propiedades como **VisibleAlarm** y **AudibleAlarm**, y datos relacionados con las infracciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-105">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9fd4-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f9fd4-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f9fd4-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f9fd4-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fd4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9fd4-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B70-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalFrame : CIM_PhysicalPackage
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
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
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="f9fd4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9fd4-111">Members</span></span>

<span data-ttu-id="f9fd4-112">La clase **CIM \_ PhysicalFrame** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f9fd4-112">The **CIM\_PhysicalFrame** class has these types of members:</span></span>

-   [<span data-ttu-id="f9fd4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f9fd4-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="f9fd4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9fd4-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f9fd4-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="f9fd4-115">Methods</span></span>

<span data-ttu-id="f9fd4-116">La clase **CIM \_ PhysicalFrame** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-116">The **CIM\_PhysicalFrame** class has these methods.</span></span>



| <span data-ttu-id="f9fd4-117">Método</span><span class="sxs-lookup"><span data-stu-id="f9fd4-117">Method</span></span>                                                                 | <span data-ttu-id="f9fd4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9fd4-118">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9fd4-119">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalframe.md) | <span data-ttu-id="f9fd4-120">Comprueba si el elemento físico al que se hace referencia puede estar contenido o insertado en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-120">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="f9fd4-121">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f9fd4-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9fd4-122">Properties</span></span>

<span data-ttu-id="f9fd4-123">La clase **CIM \_ PhysicalFrame** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-123">The **CIM\_PhysicalFrame** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9fd4-124">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-124">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-125">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-127">Si es **true**, el marco está equipado con una alarma audible.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-127">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-131">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-132">Cadena de forma libre que proporciona más información si la propiedad **SecurityBreach** indica que se ha producido una infracción o algún otro evento relacionado con la seguridad.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-133">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-133">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-136">Cadena de forma libre que contiene información sobre cómo se conectan los distintos cables y se empaquetan para el marco.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-136">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="f9fd4-137">Con muchos cables de red, relacionados con el almacenamiento y de alimentación, la administración de cables puede ser un esfuerzo complejo y desafiante.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-137">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="f9fd4-138">Esta propiedad de cadena contiene información para ayudar en el ensamblado y el servicio del marco.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-138">This string property contains information to aid in assembly and service of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-142">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-143">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-143">Short textual description of the object.</span></span>

<span data-ttu-id="f9fd4-144">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-148">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-148">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-149">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-149">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f9fd4-150">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-150">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f9fd4-151">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-151">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-152">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-152">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-153">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-153">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-155">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-155">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-156">Profundidad del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-156">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="f9fd4-157">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-157">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-161">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-162">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-162">Textual description of the object.</span></span>

<span data-ttu-id="f9fd4-163">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-164">**Height**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-164">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-165">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-165">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-167">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-168">Alto del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-168">Height of the physical package, in inches.</span></span>

<span data-ttu-id="f9fd4-169">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-169">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-170">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-170">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-171">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-173">Si **es true**, el paquete puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-173">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="f9fd4-174">Un paquete físico puede intercambiarse en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras se activa el paquete contenedor.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-174">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="f9fd4-175">Por ejemplo, un componente de ventilador se puede diseñar para que se intercambie en caliente.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-175">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="f9fd4-176">Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-176">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="f9fd4-177">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-177">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-178">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-178">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-179">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-179">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-181">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-182">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-182">Date and time the object was installed.</span></span> <span data-ttu-id="f9fd4-183">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-183">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f9fd4-184">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-185">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-185">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-186">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-188">Si es **true**, el marco está protegido con un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-188">If **TRUE**, the frame is protected with a lock.</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-189">**Le**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-189">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-192">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-193">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-193">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="f9fd4-194">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-194">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="f9fd4-195">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-195">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-196">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-196">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-199">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-199">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-200">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-200">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="f9fd4-201">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-202">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-205">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-206">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-206">Label by which the object is known.</span></span> <span data-ttu-id="f9fd4-207">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-207">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f9fd4-208">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-209">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-209">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-212">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-212">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="f9fd4-213">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-213">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="f9fd4-214">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="f9fd4-214">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="f9fd4-215">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-216">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-216">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-219">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-220">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-220">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="f9fd4-221">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-222">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-222">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-223">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-225">Si es **true**, el elemento físico está encendido; de lo contrario, está actualmente desactivado.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-225">If **TRUE**, the physical element is powered on; otherwise, it is currently off.</span></span>

<span data-ttu-id="f9fd4-226">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-226">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-227">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-227">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-228">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-230">Si es **true**, este elemento está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado global.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-230">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="f9fd4-231">Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-231">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="f9fd4-232">Si la potencia puede estar activada y se ha quitado el paquete, el elemento es extraíble y se puede intercambiar en caliente.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-232">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="f9fd4-233">Por ejemplo, un chip de Procesador actualizable es extraíble.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-233">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="f9fd4-234">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-234">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-235">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-235">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-236">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-238">Si es **true**, es posible reemplazar el elemento por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-238">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="f9fd4-239">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-239">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="f9fd4-240">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-240">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="f9fd4-241">Todos los componentes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-241">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="f9fd4-242">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-242">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-243">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-243">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-244">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-246">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Tabla global de contenedor físico DMTF \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-246">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-247">Indica si se intentó una infracción física del fotograma pero no se ha realizado correctamente, o si se ha intentado y se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-247">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f9fd4-248">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-248">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f9fd4-249">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-249">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="f9fd4-250">**Sin brecha** (3)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-250">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="f9fd4-251">**Intento de infracción** (4)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-251">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="f9fd4-252">**Infracción correcta** (5)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-252">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f9fd4-253">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-253">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-254">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-256">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-256">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-257">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-257">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="f9fd4-258">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-258">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-259">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-259">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-260">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-262">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-262">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-263">Cadenas de forma libre que proporcionan explicaciones detalladas para las entradas de la matriz **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="f9fd4-263">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="f9fd4-264">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **ServicePhilosophy** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-264">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="f9fd4-265">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-265">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-266">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-266">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-268">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-269">Indica si el marco se va a atender desde la parte superior, delantera, posterior o lateral; y si tienen bandejas deslizantes o laterales extraíbles, y si el fotograma se va a mover (por ejemplo, con rodillos).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-269">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f9fd4-270">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-270">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f9fd4-271">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-271">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="f9fd4-272">**Servicio desde arriba** (2)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-272">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="f9fd4-273">**Servicio desde delante** (3)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-273">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="f9fd4-274">**Servicio de atrás** (4)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-274">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="f9fd4-275">**Servicio desde el lado** (5)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-275">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="f9fd4-276">**Bandejas deslizantes** (6)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-276">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="f9fd4-277">**Lados extraíbles** (7)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-277">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="f9fd4-278">**Móvil** (8)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-278">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f9fd4-279">**SKU**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-279">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-280">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-282">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-282">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-283">Número de unidad de almacén para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-283">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="f9fd4-284">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-284">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-285">**Estado**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-288">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-288">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-289">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-289">Current status of the object.</span></span>

<span data-ttu-id="f9fd4-290">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f9fd4-291">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f9fd4-291">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f9fd4-292">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-292">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f9fd4-293">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-293">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f9fd4-294">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-294">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f9fd4-295">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-295">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f9fd4-296">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-296">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f9fd4-297">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-297">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f9fd4-298">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-298">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f9fd4-299">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-299">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f9fd4-300">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-300">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f9fd4-301">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-301">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f9fd4-302">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-302">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f9fd4-303">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-303">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f9fd4-304">**Tag**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-304">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-305">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-307">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-308">Cadena arbitraria que identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-308">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="f9fd4-309">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-309">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="f9fd4-310">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-310">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="f9fd4-311">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-311">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="f9fd4-312">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-312">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="f9fd4-313">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-313">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="f9fd4-314">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-315">**Versión**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-315">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-318">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f9fd4-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-319">Cadena que indica la versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-319">String that indicates the version of the physical element.</span></span>

<span data-ttu-id="f9fd4-320">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-321">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-321">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-322">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-324">Si **es true**, el equipo incluye una alarma visible.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-324">If **TRUE**, the equipment includes a visible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-325">**Peso**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-325">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-326">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-326">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-328">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-328">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-329">Peso del paquete físico, en libras.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-329">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="f9fd4-330">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-330">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fd4-331">**Width**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-331">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9fd4-332">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-332">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9fd4-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9fd4-334">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="f9fd4-334">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="f9fd4-335">Ancho del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-335">Width of the physical package, in inches.</span></span>

<span data-ttu-id="f9fd4-336">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-336">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9fd4-337">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9fd4-337">Remarks</span></span>

<span data-ttu-id="f9fd4-338">La clase **CIM \_ PhysicalFrame** se deriva de [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-338">The **CIM\_PhysicalFrame** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="f9fd4-339">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-339">WMI does not implement this class.</span></span> <span data-ttu-id="f9fd4-340">Para las clases WMI derivadas de **CIM \_ PhysicalFrame**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f9fd4-340">For WMI classes derived from **CIM\_PhysicalFrame**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f9fd4-341">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-341">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f9fd4-342">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f9fd4-342">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9fd4-343">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9fd4-343">Requirements</span></span>



| <span data-ttu-id="f9fd4-344">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9fd4-344">Requirement</span></span> | <span data-ttu-id="f9fd4-345">Value</span><span class="sxs-lookup"><span data-stu-id="f9fd4-345">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9fd4-346">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9fd4-346">Minimum supported client</span></span><br/> | <span data-ttu-id="f9fd4-347">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9fd4-347">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9fd4-348">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9fd4-348">Minimum supported server</span></span><br/> | <span data-ttu-id="f9fd4-349">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9fd4-349">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9fd4-350">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f9fd4-350">Namespace</span></span><br/>                | <span data-ttu-id="f9fd4-351">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f9fd4-351">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f9fd4-352">MOF</span><span class="sxs-lookup"><span data-stu-id="f9fd4-352">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9fd4-353"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd4-353"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9fd4-354">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9fd4-354">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9fd4-355"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd4-355"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9fd4-356">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9fd4-356">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9fd4-357">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="f9fd4-357">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

