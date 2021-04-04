---
description: La \_ clase CIM UnitaryComputerSystem representa un equipo de escritorio, móvil, de red, servidor u otro tipo de sistema de un solo nodo.
ms.assetid: c696050d-c921-4056-adc7-e4a2e9f4e119
ms.tgt_platform: multiple
title: CIM_UnitaryComputerSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem
- CIM_UnitaryComputerSystem.Caption
- CIM_UnitaryComputerSystem.CreationClassName
- CIM_UnitaryComputerSystem.Description
- CIM_UnitaryComputerSystem.InitialLoadInfo
- CIM_UnitaryComputerSystem.InstallDate
- CIM_UnitaryComputerSystem.LastLoadInfo
- CIM_UnitaryComputerSystem.Name
- CIM_UnitaryComputerSystem.NameFormat
- CIM_UnitaryComputerSystem.PowerManagementCapabilities
- CIM_UnitaryComputerSystem.PowerManagementSupported
- CIM_UnitaryComputerSystem.PowerState
- CIM_UnitaryComputerSystem.PrimaryOwnerContact
- CIM_UnitaryComputerSystem.PrimaryOwnerName
- CIM_UnitaryComputerSystem.ResetCapability
- CIM_UnitaryComputerSystem.Roles
- CIM_UnitaryComputerSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e14812fda7971ffe045e8e36752c983cf5350402
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998166"
---
# <a name="cim_unitarycomputersystem-class"></a><span data-ttu-id="c0f1e-103">\_Clase UnitaryComputerSystem de CIM</span><span class="sxs-lookup"><span data-stu-id="c0f1e-103">CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="c0f1e-104">La clase **CIM \_ UnitaryComputerSystem** representa un equipo de escritorio, móvil, de red, servidor u otro tipo de sistema de un solo nodo.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-104">The **CIM\_UnitaryComputerSystem** class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0f1e-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c0f1e-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c0f1e-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c0f1e-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f1e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0f1e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C526-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UnitaryComputerSystem : CIM_ComputerSystem
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  string   InitialLoadInfo[];
  datetime InstallDate;
  string   LastLoadInfo;
  string   Name;
  string   NameFormat;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  string   Roles[];
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="c0f1e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c0f1e-110">Members</span></span>

<span data-ttu-id="c0f1e-111">La clase **CIM \_ UnitaryComputerSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c0f1e-111">The **CIM\_UnitaryComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="c0f1e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c0f1e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c0f1e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c0f1e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c0f1e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c0f1e-114">Methods</span></span>

<span data-ttu-id="c0f1e-115">La clase **CIM \_ UnitaryComputerSystem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-115">The **CIM\_UnitaryComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="c0f1e-116">Método</span><span class="sxs-lookup"><span data-stu-id="c0f1e-116">Method</span></span>                                                                           | <span data-ttu-id="c0f1e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0f1e-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0f1e-118">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-118">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md) | <span data-ttu-id="c0f1e-119">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-119">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c0f1e-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c0f1e-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c0f1e-121">Properties</span></span>

<span data-ttu-id="c0f1e-122">La clase **CIM \_ UnitaryComputerSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-122">The **CIM\_UnitaryComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0f1e-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-126">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-127">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-127">Short textual description of the object.</span></span>

<span data-ttu-id="c0f1e-128">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0f1e-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-132">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-132">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-133">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c0f1e-134">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c0f1e-135">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-135">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0f1e-136">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-139">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-140">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-140">Textual description of the object.</span></span>

<span data-ttu-id="c0f1e-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0f1e-142">**InitialLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-142">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-143">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-145">Datos necesarios para buscar el dispositivo de carga inicial (su clave) o el servicio de arranque para solicitar que se inicie el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-145">Data needed to find either the initial load device (its key) or the boot service to request the operating system to start.</span></span> <span data-ttu-id="c0f1e-146">Además, también se pueden especificar los parámetros de carga (es decir, un nombre de ruta de acceso y parámetros).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-146">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="c0f1e-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-148">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-150">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-151">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-151">Date and time the object was installed.</span></span> <span data-ttu-id="c0f1e-152">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-152">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c0f1e-153">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0f1e-154">**LastLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-154">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-157">Datos que identifican el dispositivo de carga inicial (su clave) o el servicio de arranque que solicitó la última carga del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-157">Data that identifies either the initial load device (its key) or the boot service that requested the last operating system load.</span></span> <span data-ttu-id="c0f1e-158">Además, también se pueden especificar los parámetros de carga (es decir, un nombre de ruta de acceso y parámetros).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-158">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="c0f1e-159">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-162">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-162">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-163">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-163">Label by which the object is known.</span></span> <span data-ttu-id="c0f1e-164">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-164">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c0f1e-165">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0f1e-166">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-166">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-169">El objeto de [**\_ ComputerSystem de CIM**](cim-computersystem.md) y sus derivados son objetos de nivel superior de CIM que proporcionan el ámbito de numerosos componentes y requieren claves de [**\_ Sistema CIM**](cim-system.md) únicas.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-169">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of CIM that provide the scope for numerous components and require unique [**CIM\_System**](cim-system.md) keys.</span></span> <span data-ttu-id="c0f1e-170">Se define una heurística para crear el nombre de **\_ ComputerSystem de CIM** en un intento de generar siempre el mismo nombre de sistema, independientemente del Protocolo de detección.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-170">A heuristic is defined to create the **CIM\_ComputerSystem** name in an attempt to always generate the same system name, independent of discovery protocol.</span></span> <span data-ttu-id="c0f1e-171">Esto evita los problemas de inventario y administración en los que se detecta el mismo recurso o entidad varias veces, pero no se puede resolver en un solo objeto.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-171">This prevents inventory and management problems where the same asset or entity is discovered multiple times, but cannot be resolved to a single object.</span></span> <span data-ttu-id="c0f1e-172">Esta propiedad identifica cómo se generó el nombre del sistema mediante la heurística de subclases.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-172">This property identifies how the system name was generated by using the subclass heuristic.</span></span> <span data-ttu-id="c0f1e-173">La heurística se describe en la especificación de modelo común de CIM V2 y da por supuesto que las reglas documentadas se recorren para determinar y asignar un nombre.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-173">The heuristic is outlined in the CIM V2 Common Model specification and assumes that the documented rules are traversed to determine and assign a name.</span></span> <span data-ttu-id="c0f1e-174">La lista de valores de **NameFormat** define el orden de prioridad para asignar el nombre del sistema con varias reglas asignadas al mismo valor.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-174">The **NameFormat** values list defines the precedence order for assigning the system name with several rules mapping to the same value.</span></span> <span data-ttu-id="c0f1e-175">Tenga en cuenta que el nombre del equipo **CIM \_** que se calcula con la heurística es el valor de clave del sistema.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-175">Note that the **CIM\_ComputerSystem** name that is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="c0f1e-176">Se pueden asignar otros nombres y usarse para **el \_ ComputerSystem de CIM** que mejor se adapte a la empresa, mediante alias.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-176">Other names can be assigned and used for the **CIM\_ComputerSystem** that better suit the business, using aliases.</span></span>

<span data-ttu-id="c0f1e-177">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-177">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="c0f1e-178">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c0f1e-178">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="c0f1e-179">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-179">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="c0f1e-180">**Dial** ("dial")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-180">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="c0f1e-181">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-181">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="c0f1e-182">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-182">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="c0f1e-183">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-183">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="c0f1e-184">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-184">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="c0f1e-185">**ISDN (RDSI** ) ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-185">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="c0f1e-186">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-186">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="c0f1e-187">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-187">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="c0f1e-188">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-188">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="c0f1e-189">**E. 164** ("E. 164")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-189">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="c0f1e-190">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-190">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="c0f1e-191">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-191">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c0f1e-192">**Otro** ("otro")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-192">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0f1e-193">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-193">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-194">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-194">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-196">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controles de alimentación del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-196">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-197">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-197">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c0f1e-198">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-198">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0f1e-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c0f1e-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c0f1e-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c0f1e-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-203">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-203">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c0f1e-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-205">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-205">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c0f1e-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-207">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="c0f1e-207">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c0f1e-208">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-208">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c0f1e-209">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-209">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c0f1e-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-211">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-211">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c0f1e-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-213">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-213">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0f1e-214">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-214">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-215">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-217">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-217">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c0f1e-218">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c0f1e-218">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c0f1e-219">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-219">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c0f1e-220">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c0f1e-220">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="c0f1e-221">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-221">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-222">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-224">Estado de energía actual del equipo y su sistema operativo asociado.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-224">Current power state of the computer system and its associated operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0f1e-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-226">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-226">Unknown.</span></span>

</dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="c0f1e-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Potencia completa** (1)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-228">Potencia completa.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-228">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c0f1e-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (2)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-230">El sistema se encuentra en un estado de ahorro de energía y sigue funcionando, pero puede presentar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-230">System is in a power-save state and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c0f1e-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (3)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-232">El sistema no funciona, pero puede que se ponga a pleno rendimiento rápidamente.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-232">System is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c0f1e-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (4)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-234">Se sabe que el sistema está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-234">System is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c0f1e-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (5)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-236">Ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-236">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c0f1e-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (6** )</span><span class="sxs-lookup"><span data-stu-id="c0f1e-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-238">Desconectar.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-238">Power off.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c0f1e-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (7)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-240">El sistema está en un estado de advertencia y también en un modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-240">System is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="c0f1e-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>Ahorro **de energía: hibernación** (8)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-242">Power Save Hibernate.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-242">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="c0f1e-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Ahorro **de energía: Soft off** (9)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="c0f1e-244">Ahorro flexible de energía.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-244">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0f1e-245">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-245">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-248">Cadena que proporciona información sobre cómo ponerse en contacto con el propietario del sistema principal (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-248">String that provides information on how to reach the primary system owner (for example, phone number, email address, and so on).</span></span>

<span data-ttu-id="c0f1e-249">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-249">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0f1e-250">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-250">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-253">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-253">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-254">Nombre del propietario del sistema principal.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-254">Name of the primary system owner.</span></span>

<span data-ttu-id="c0f1e-255">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-255">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0f1e-256">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-256">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-257">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-259">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Seguridad de hardware del sistema DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-260">Si está habilitada, el sistema del equipo unitario puede restablecerse con hardware (por ejemplo, con los botones de encendido y de restablecimiento).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-260">If enabled, the unitary computer system can be reset with hardware (for example, with the power and reset buttons).</span></span> <span data-ttu-id="c0f1e-261">Si está deshabilitado, no se permite el restablecimiento de hardware.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-261">If disabled, hardware reset is not allowed.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c0f1e-262">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-262">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0f1e-263">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-263">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c0f1e-264">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-264">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c0f1e-265">**Habilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-265">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="c0f1e-266">**No implementado** (5)</span><span class="sxs-lookup"><span data-stu-id="c0f1e-266">**Not Implemented** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0f1e-267">**Roles**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-267">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-268">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-269">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-270">Roles que el sistema desempeña en el entorno de tecnología de la información.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-270">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="c0f1e-271">Las subclases del sistema pueden invalidar esta propiedad para definir valores de rol explícitos.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-271">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="c0f1e-272">Como alternativa, un grupo de trabajo puede describir la heurística, las convenciones y las directrices para especificar los roles.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-272">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="c0f1e-273">Por ejemplo, para una instancia de un sistema de red, esta propiedad puede contener la cadena "switch" o "Bridge".</span><span class="sxs-lookup"><span data-stu-id="c0f1e-273">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="c0f1e-274">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-274">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0f1e-275">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-275">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f1e-276">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0f1e-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f1e-278">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-278">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c0f1e-279">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-279">Current status of the object.</span></span> <span data-ttu-id="c0f1e-280">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c0f1e-281">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c0f1e-281">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c0f1e-282">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-282">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c0f1e-283">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-283">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c0f1e-284">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-284">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0f1e-285">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-285">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c0f1e-286">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-286">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c0f1e-287">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-287">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c0f1e-288">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-288">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c0f1e-289">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-289">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c0f1e-290">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-290">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c0f1e-291">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-291">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c0f1e-292">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-292">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c0f1e-293">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="c0f1e-293">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="c0f1e-294"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c0f1e-294"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c0f1e-295">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0f1e-295">Remarks</span></span>

<span data-ttu-id="c0f1e-296">La clase **CIM \_ UnitaryComputerSystem** se deriva de la clase [**CIM \_ ComputerSystem**](cim-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-296">The **CIM\_UnitaryComputerSystem** class is derived from [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="c0f1e-297">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-297">WMI does not implement this class.</span></span> <span data-ttu-id="c0f1e-298">Para las clases WMI derivadas de **CIM \_ UnitaryComputerSystem**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c0f1e-298">For WMI classes derived from **CIM\_UnitaryComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c0f1e-299">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-299">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c0f1e-300">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c0f1e-300">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f1e-301">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0f1e-301">Requirements</span></span>



| <span data-ttu-id="c0f1e-302">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0f1e-302">Requirement</span></span> | <span data-ttu-id="c0f1e-303">Value</span><span class="sxs-lookup"><span data-stu-id="c0f1e-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f1e-304">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0f1e-304">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f1e-305">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0f1e-305">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0f1e-306">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0f1e-306">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f1e-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0f1e-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0f1e-308">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c0f1e-308">Namespace</span></span><br/>                | <span data-ttu-id="c0f1e-309">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c0f1e-309">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c0f1e-310">MOF</span><span class="sxs-lookup"><span data-stu-id="c0f1e-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0f1e-311"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0f1e-311"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0f1e-312">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c0f1e-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0f1e-313"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0f1e-313"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f1e-314">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0f1e-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f1e-315">**ComputerSystem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="c0f1e-315">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

