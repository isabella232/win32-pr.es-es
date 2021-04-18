---
description: La \_ clase de chip CIM representa el tipo de hardware de circuito integrado, incluidos Asics, procesadores, chips de memoria, etc.
ms.assetid: 3c2b0023-5d02-49b9-90f5-d66eb8a103f0
ms.tgt_platform: multiple
title: CIM_Chip (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chip
- CIM_Chip.Caption
- CIM_Chip.Description
- CIM_Chip.InstallDate
- CIM_Chip.Name
- CIM_Chip.Status
- CIM_Chip.CreationClassName
- CIM_Chip.Manufacturer
- CIM_Chip.Model
- CIM_Chip.OtherIdentifyingInfo
- CIM_Chip.PartNumber
- CIM_Chip.PoweredOn
- CIM_Chip.SerialNumber
- CIM_Chip.SKU
- CIM_Chip.Tag
- CIM_Chip.Version
- CIM_Chip.HotSwappable
- CIM_Chip.Removable
- CIM_Chip.Replaceable
- CIM_Chip.FormFactor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 953ae371edca42409246307b21aad69a02cf4a66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496415"
---
# <a name="cim_chip-class"></a><span data-ttu-id="3b364-103">\_Clase de chip CIM</span><span class="sxs-lookup"><span data-stu-id="3b364-103">CIM\_Chip class</span></span>

<span data-ttu-id="3b364-104">La clase de **\_ chip CIM** representa el tipo de hardware de circuito integrado, incluidos Asics, procesadores, chips de memoria, etc.</span><span class="sxs-lookup"><span data-stu-id="3b364-104">The **CIM\_Chip** class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b364-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="3b364-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3b364-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3b364-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3b364-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3b364-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3b364-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3b364-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b364-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b364-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chip : CIM_PhysicalComponent
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
  uint16   FormFactor;
};
```

## <a name="members"></a><span data-ttu-id="3b364-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b364-110">Members</span></span>

<span data-ttu-id="3b364-111">La clase de **\_ chip CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3b364-111">The **CIM\_Chip** class has these types of members:</span></span>

-   [<span data-ttu-id="3b364-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b364-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b364-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b364-113">Properties</span></span>

<span data-ttu-id="3b364-114">La clase de **\_ chip CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3b364-114">The **CIM\_Chip** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b364-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3b364-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3b364-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3b364-119">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b364-119">A short textual description of the object.</span></span>

<span data-ttu-id="3b364-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3b364-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-124">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3b364-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3b364-125">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="3b364-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3b364-126">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="3b364-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3b364-127">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-127">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b364-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-131">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="3b364-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3b364-132">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b364-132">A textual description of the object.</span></span>

<span data-ttu-id="3b364-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-134">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="3b364-134">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b364-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b364-137">Factor de forma de implementación para el chip.</span><span class="sxs-lookup"><span data-stu-id="3b364-137">Implementation form factor for the chip.</span></span> <span data-ttu-id="3b364-138">Se pueden especificar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3b364-138">The following values can be specified.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b364-139">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3b364-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3b364-140">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3b364-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

<span data-ttu-id="3b364-141">**SIP** (2)</span><span class="sxs-lookup"><span data-stu-id="3b364-141">**SIP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DIP"></span><span id="dip"></span>

<span data-ttu-id="3b364-142">**DIP** (3)</span><span class="sxs-lookup"><span data-stu-id="3b364-142">**DIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP"></span><span id="zip"></span>

<span data-ttu-id="3b364-143">**Zip** (4)</span><span class="sxs-lookup"><span data-stu-id="3b364-143">**ZIP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOJ"></span><span id="soj"></span>

<span data-ttu-id="3b364-144">**SOJ** (5)</span><span class="sxs-lookup"><span data-stu-id="3b364-144">**SOJ** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="3b364-145">**Propietario** (6)</span><span class="sxs-lookup"><span data-stu-id="3b364-145">**Proprietary** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SIMM"></span><span id="simm"></span>

<span data-ttu-id="3b364-146">**SIMM** (7)</span><span class="sxs-lookup"><span data-stu-id="3b364-146">**SIMM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DIMM"></span><span id="dimm"></span>

<span data-ttu-id="3b364-147">**DIMM** (8)</span><span class="sxs-lookup"><span data-stu-id="3b364-147">**DIMM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TSOP"></span><span id="tsop"></span>

<span data-ttu-id="3b364-148">**TSOP** (9)</span><span class="sxs-lookup"><span data-stu-id="3b364-148">**TSOP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PGA"></span><span id="pga"></span>

<span data-ttu-id="3b364-149">**PGA** (10)</span><span class="sxs-lookup"><span data-stu-id="3b364-149">**PGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="RIMM"></span><span id="rimm"></span>

<span data-ttu-id="3b364-150">**RIMM** (11)</span><span class="sxs-lookup"><span data-stu-id="3b364-150">**RIMM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SODIMM"></span><span id="sodimm"></span>

<span data-ttu-id="3b364-151">**SODIMM** (12)</span><span class="sxs-lookup"><span data-stu-id="3b364-151">**SODIMM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SRIMM"></span><span id="srimm"></span>

<span data-ttu-id="3b364-152">**SRIMM** (13)</span><span class="sxs-lookup"><span data-stu-id="3b364-152">**SRIMM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SMD"></span><span id="smd"></span>

<span data-ttu-id="3b364-153">**SMD** (14)</span><span class="sxs-lookup"><span data-stu-id="3b364-153">**SMD** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSMP"></span><span id="ssmp"></span>

<span data-ttu-id="3b364-154">**SSMP** (15)</span><span class="sxs-lookup"><span data-stu-id="3b364-154">**SSMP** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="QFP"></span><span id="qfp"></span>

<span data-ttu-id="3b364-155">**QFP** (16)</span><span class="sxs-lookup"><span data-stu-id="3b364-155">**QFP** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="TQFP"></span><span id="tqfp"></span>

<span data-ttu-id="3b364-156">**TQFP** (17)</span><span class="sxs-lookup"><span data-stu-id="3b364-156">**TQFP** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SOIC"></span><span id="soic"></span>

<span data-ttu-id="3b364-157">**SOIC** (18)</span><span class="sxs-lookup"><span data-stu-id="3b364-157">**SOIC** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="LCC"></span><span id="lcc"></span>

<span data-ttu-id="3b364-158">**LCC** (19)</span><span class="sxs-lookup"><span data-stu-id="3b364-158">**LCC** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PLCC"></span><span id="plcc"></span>

<span data-ttu-id="3b364-159">**PLCC** (20)</span><span class="sxs-lookup"><span data-stu-id="3b364-159">**PLCC** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="BGA"></span><span id="bga"></span>

<span data-ttu-id="3b364-160">**BGA** (21)</span><span class="sxs-lookup"><span data-stu-id="3b364-160">**BGA** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="FPBGA"></span><span id="fpbga"></span>

<span data-ttu-id="3b364-161">**FPBGA** (22)</span><span class="sxs-lookup"><span data-stu-id="3b364-161">**FPBGA** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="LGA"></span><span id="lga"></span>

<span data-ttu-id="3b364-162">**LGA** (23)</span><span class="sxs-lookup"><span data-stu-id="3b364-162">**LGA** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="FB-DIMM"></span><span id="fb-dimm"></span>

<span data-ttu-id="3b364-163">**FB-DIMM** (24)</span><span class="sxs-lookup"><span data-stu-id="3b364-163">**FB-DIMM** (24)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b364-164">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="3b364-164">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-165">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3b364-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b364-167">Si **es true**, el paquete puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="3b364-167">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="3b364-168">Un paquete físico puede intercambiarse en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras se activa el paquete contenedor.</span><span class="sxs-lookup"><span data-stu-id="3b364-168">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="3b364-169">Por ejemplo, un componente de ventilador se puede diseñar para que se intercambie en caliente.</span><span class="sxs-lookup"><span data-stu-id="3b364-169">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="3b364-170">Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="3b364-170">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="3b364-171">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-171">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3b364-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-173">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b364-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-175">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="3b364-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3b364-176">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="3b364-176">Indicates when the object was installed.</span></span> <span data-ttu-id="3b364-177">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="3b364-177">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3b364-178">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-179">**Le**</span><span class="sxs-lookup"><span data-stu-id="3b364-179">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-182">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3b364-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3b364-183">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3b364-183">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="3b364-184">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-184">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="3b364-185">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-185">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-186">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="3b364-186">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-189">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3b364-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3b364-190">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3b364-190">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="3b364-191">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-191">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-192">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3b364-192">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-195">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3b364-195">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3b364-196">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="3b364-196">Label by which the object is known.</span></span> <span data-ttu-id="3b364-197">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="3b364-197">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="3b364-198">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-199">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3b364-199">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b364-202">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3b364-202">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="3b364-203">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="3b364-203">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="3b364-204">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="3b364-204">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="3b364-205">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-206">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="3b364-206">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-209">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3b364-209">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3b364-210">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3b364-210">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="3b364-211">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-211">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-212">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="3b364-212">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-213">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3b364-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b364-215">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="3b364-215">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="3b364-216">De lo contrario, está actualmente desactivado.</span><span class="sxs-lookup"><span data-stu-id="3b364-216">Otherwise, it is currently off.</span></span>

<span data-ttu-id="3b364-217">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-217">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-218">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="3b364-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-219">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3b364-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b364-221">Si es **true**, este elemento está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado global.</span><span class="sxs-lookup"><span data-stu-id="3b364-221">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="3b364-222">Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="3b364-222">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="3b364-223">Si la potencia puede estar activada y se ha quitado el paquete, el elemento es extraíble y se puede intercambiar en caliente.</span><span class="sxs-lookup"><span data-stu-id="3b364-223">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="3b364-224">Por ejemplo, un chip de Procesador actualizable es extraíble.</span><span class="sxs-lookup"><span data-stu-id="3b364-224">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="3b364-225">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-225">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-226">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="3b364-226">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-227">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3b364-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b364-229">Si es **true**, es posible reemplazar el elemento por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="3b364-229">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="3b364-230">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="3b364-230">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="3b364-231">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="3b364-231">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="3b364-232">Todos los componentes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="3b364-232">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="3b364-233">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-233">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-234">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3b364-234">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-237">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3b364-237">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3b364-238">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3b364-238">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="3b364-239">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-240">**SKU**</span><span class="sxs-lookup"><span data-stu-id="3b364-240">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-241">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-243">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3b364-243">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3b364-244">Número de unidad de almacén para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3b364-244">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="3b364-245">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-245">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-246">**Estado**</span><span class="sxs-lookup"><span data-stu-id="3b364-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-249">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="3b364-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3b364-250">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b364-250">String that indicates the current status of the object.</span></span> <span data-ttu-id="3b364-251">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="3b364-251">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="3b364-252">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="3b364-252">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="3b364-253">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="3b364-253">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="3b364-254">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="3b364-254">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3b364-255">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="3b364-255">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3b364-256">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="3b364-256">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3b364-257">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-257">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3b364-258">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="3b364-258">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3b364-259">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="3b364-259">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3b364-260">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="3b364-260">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3b364-261">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="3b364-261">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b364-262">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="3b364-262">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3b364-263">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="3b364-263">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3b364-264">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="3b364-264">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3b364-265">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="3b364-265">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3b364-266">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="3b364-266">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3b364-267">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="3b364-267">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3b364-268">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="3b364-268">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3b364-269">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="3b364-269">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3b364-270">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="3b364-270">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b364-271">**Tag**</span><span class="sxs-lookup"><span data-stu-id="3b364-271">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-272">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-274">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3b364-274">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3b364-275">Identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="3b364-275">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="3b364-276">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="3b364-276">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="3b364-277">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="3b364-277">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="3b364-278">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="3b364-278">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="3b364-279">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="3b364-279">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="3b364-280">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="3b364-280">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="3b364-281">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b364-282">**Versión**</span><span class="sxs-lookup"><span data-stu-id="3b364-282">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b364-283">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b364-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b364-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b364-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b364-285">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3b364-285">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3b364-286">Indica la versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3b364-286">Indicates the version of the physical element.</span></span>

<span data-ttu-id="3b364-287">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b364-288">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b364-288">Remarks</span></span>

<span data-ttu-id="3b364-289">La clase de **\_ chip CIM** se deriva [**de \_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-289">The **CIM\_Chip** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="3b364-290">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="3b364-290">WMI does not implement this class.</span></span> <span data-ttu-id="3b364-291">Para obtener más información sobre las clases derivadas del **\_ chip CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3b364-291">For more information about classes derived from **CIM\_Chip**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3b364-292">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="3b364-292">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3b364-293">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="3b364-293">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b364-294">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b364-294">Requirements</span></span>



| <span data-ttu-id="3b364-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b364-295">Requirement</span></span> | <span data-ttu-id="3b364-296">Value</span><span class="sxs-lookup"><span data-stu-id="3b364-296">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b364-297">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b364-297">Minimum supported client</span></span><br/> | <span data-ttu-id="3b364-298">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b364-298">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b364-299">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b364-299">Minimum supported server</span></span><br/> | <span data-ttu-id="3b364-300">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b364-300">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b364-301">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b364-301">Namespace</span></span><br/>                | <span data-ttu-id="3b364-302">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3b364-302">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b364-303">MOF</span><span class="sxs-lookup"><span data-stu-id="3b364-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b364-304"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b364-304"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b364-305">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b364-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b364-306"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b364-306"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b364-307">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b364-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b364-308">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3b364-308">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

