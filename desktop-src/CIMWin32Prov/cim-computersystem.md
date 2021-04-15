---
description: Una \_ clase de ComputerSystem de CIM representa una colección especial de instancias de los ManagedSystemElement de CIM \_ .
ms.assetid: c4fd0598-3cb3-428f-ad39-a14232ef7c17
ms.tgt_platform: multiple
title: CIM_ComputerSystem (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.Caption
- CIM_ComputerSystem.Description
- CIM_ComputerSystem.InstallDate
- CIM_ComputerSystem.Status
- CIM_ComputerSystem.CreationClassName
- CIM_ComputerSystem.Name
- CIM_ComputerSystem.PrimaryOwnerContact
- CIM_ComputerSystem.PrimaryOwnerName
- CIM_ComputerSystem.Roles
- CIM_ComputerSystem.NameFormat
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4645a8d4b2440b0b102658d3eca74d825d774dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496403"
---
# <a name="cim_computersystem-class-cimwin32-wmi-providers"></a><span data-ttu-id="1a6f9-103">CIM_ComputerSystem (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="1a6f9-103">CIM_ComputerSystem class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="1a6f9-104">Una clase de **\_ ComputerSystem de CIM** representa una colección especial de instancias de los [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="1a6f9-104">A **CIM\_ComputerSystem** class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="1a6f9-105">Esta colección proporciona funciones de equipo y actúa como un punto de agregación para asociar uno o varios de los siguientes elementos: sistema de archivos, sistema operativo, procesador y memoria (almacenamiento volátil y no volátil).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-105">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="1a6f9-106">Esta clase se deriva del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-106">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a6f9-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1a6f9-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1a6f9-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1a6f9-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a6f9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a6f9-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C525-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
  string   NameFormat;
};
```

## <a name="members"></a><span data-ttu-id="1a6f9-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="1a6f9-112">Members</span></span>

<span data-ttu-id="1a6f9-113">La clase de **\_ ComputerSystem de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1a6f9-113">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="1a6f9-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a6f9-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a6f9-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a6f9-115">Properties</span></span>

<span data-ttu-id="1a6f9-116">La clase de **\_ ComputerSystem de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-116">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a6f9-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6f9-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a6f9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-120">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1a6f9-121">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-121">A short textual description of the object.</span></span>

<span data-ttu-id="1a6f9-122">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a6f9-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6f9-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a6f9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-126">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1a6f9-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1a6f9-127">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1a6f9-128">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1a6f9-129">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a6f9-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6f9-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a6f9-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-133">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1a6f9-134">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-134">A textual description of the object.</span></span>

<span data-ttu-id="1a6f9-135">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a6f9-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6f9-137">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a6f9-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-139">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1a6f9-140">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-140">Indicates when the object was installed.</span></span> <span data-ttu-id="1a6f9-141">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1a6f9-142">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a6f9-143">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6f9-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a6f9-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-146">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a6f9-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1a6f9-147">Define la etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="1a6f9-148">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a6f9-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6f9-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a6f9-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-152">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-152">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="1a6f9-153">Identifica cómo se genera el nombre del equipo, mediante una heurística.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-153">Identifies how the computer system name is generated, using a heuristic.</span></span> <span data-ttu-id="1a6f9-154">La heurística se describe, en detalle, en la especificación del modelo común de CIM V2.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-154">The heuristic is outlined, in detail, in the CIM V2 Common Model specification.</span></span> <span data-ttu-id="1a6f9-155">Se supone que las reglas documentadas se recorren en orden, para determinar y asignar un nombre.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-155">It assumes that the documented rules are traversed in order, to determine and assign a name.</span></span> <span data-ttu-id="1a6f9-156">La lista de valores de **NameFormat** define el orden de prioridad para asignar el nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-156">The **NameFormat** values list defines the precedence order for assigning the computer system name.</span></span> <span data-ttu-id="1a6f9-157">Varias reglas se asignan al mismo valor.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-157">Several rules do map to the same Value.</span></span>

<span data-ttu-id="1a6f9-158">Tenga en cuenta que el **nombre** del objeto se calcula con la heurística es el valor de clave del sistema.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-158">Note that the object's **Name** is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="1a6f9-159">Se pueden asignar otros nombres y usarse para el objeto que mejor se adapte a la empresa mediante el uso de alias.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-159">Other names can be assigned and used for the object that better suit the business, using Aliases.</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="1a6f9-160">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-160">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="1a6f9-161">**Dial** ("dial")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-161">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="1a6f9-162">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-162">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="1a6f9-163">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-163">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="1a6f9-164">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-164">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="1a6f9-165">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-165">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="1a6f9-166">**ISDN (RDSI** ) ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-166">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="1a6f9-167">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-167">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="1a6f9-168">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-168">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="1a6f9-169">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-169">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="1a6f9-170">**E. 164** ("E. 164")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-170">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="1a6f9-171">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-171">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="1a6f9-172">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-172">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1a6f9-173">**Otro** ("otro")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-173">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1a6f9-174">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-174">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6f9-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a6f9-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6f9-177">Cómo se puede alcanzar el propietario del sistema principal (por ejemplo, el número de teléfono o la dirección de correo electrónico).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-177">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="1a6f9-178">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-178">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a6f9-179">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-179">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6f9-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a6f9-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-182">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1a6f9-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1a6f9-183">Nombre del propietario del sistema principal.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-183">Name of the primary system owner.</span></span>

<span data-ttu-id="1a6f9-184">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-184">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a6f9-185">**Roles**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-185">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6f9-186">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1a6f9-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1a6f9-188">Roles que el sistema desempeña en el entorno de tecnología de la información.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-188">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="1a6f9-189">Las subclases del sistema pueden invalidar esta propiedad para definir valores de rol explícitos.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-189">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="1a6f9-190">Como alternativa, un grupo de trabajo puede describir la heurística, las convenciones y las directrices para especificar los roles.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-190">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="1a6f9-191">Por ejemplo, para una instancia de un sistema de red, esta propiedad puede contener la cadena "switch" o "Bridge".</span><span class="sxs-lookup"><span data-stu-id="1a6f9-191">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="1a6f9-192">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-192">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a6f9-193">**Estado**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6f9-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a6f9-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a6f9-196">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1a6f9-197">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="1a6f9-198">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="1a6f9-199">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="1a6f9-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="1a6f9-200">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="1a6f9-201">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="1a6f9-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1a6f9-202">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1a6f9-203">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1a6f9-204">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1a6f9-205">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1a6f9-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1a6f9-206">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1a6f9-207">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1a6f9-208">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a6f9-209">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1a6f9-210">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1a6f9-211">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1a6f9-212">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1a6f9-213">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1a6f9-214">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1a6f9-215">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1a6f9-216">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1a6f9-217">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="1a6f9-217">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="1a6f9-218"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1a6f9-218"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="1a6f9-219">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a6f9-219">Remarks</span></span>

<span data-ttu-id="1a6f9-220">La clase de **\_ ComputerSystem de CIM** se deriva del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-220">The **CIM\_ComputerSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="1a6f9-221">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-221">WMI does not implement this class.</span></span> <span data-ttu-id="1a6f9-222">Para obtener más información acerca de las clases derivadas de un **\_ ComputerSystem de CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f9-222">For more information about classes derived from **CIM\_ComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1a6f9-223">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-223">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1a6f9-224">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="1a6f9-224">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6f9-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a6f9-225">Requirements</span></span>



| <span data-ttu-id="1a6f9-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a6f9-226">Requirement</span></span> | <span data-ttu-id="1a6f9-227">Value</span><span class="sxs-lookup"><span data-stu-id="1a6f9-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6f9-228">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a6f9-228">Minimum supported client</span></span><br/> | <span data-ttu-id="1a6f9-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a6f9-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a6f9-230">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a6f9-230">Minimum supported server</span></span><br/> | <span data-ttu-id="1a6f9-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a6f9-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a6f9-232">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a6f9-232">Namespace</span></span><br/>                | <span data-ttu-id="1a6f9-233">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1a6f9-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1a6f9-234">MOF</span><span class="sxs-lookup"><span data-stu-id="1a6f9-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a6f9-235"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a6f9-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a6f9-236">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a6f9-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a6f9-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a6f9-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a6f9-238">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a6f9-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a6f9-239">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="1a6f9-239">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

