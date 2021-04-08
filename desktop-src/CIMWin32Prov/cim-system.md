---
description: La \_ clase del sistema CIM agrega un conjunto enumerable de elementos del sistema administrados.
ms.assetid: cbfa60d4-36ae-4e0c-a57f-aabf219851d0
ms.tgt_platform: multiple
title: CIM_System (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.Caption
- CIM_System.Description
- CIM_System.InstallDate
- CIM_System.Status
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerContact
- CIM_System.PrimaryOwnerName
- CIM_System.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef04e472e11c848aadb63c98b3dee2ea645a3ce7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000657"
---
# <a name="cim_system-class-cimwin32-wmi-providers"></a><span data-ttu-id="f5d81-103">CIM_System (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="f5d81-103">CIM_System class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="f5d81-104">La **clase \_ del sistema CIM** agrega un conjunto enumerable de elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="f5d81-104">The **CIM\_System** class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="f5d81-105">La agregación funciona como un todo funcional.</span><span class="sxs-lookup"><span data-stu-id="f5d81-105">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="f5d81-106">Dentro de cualquier subclase del sistema, existe una lista bien definida de las clases de elementos del sistema administradas cuyas instancias deben agregarse.</span><span class="sxs-lookup"><span data-stu-id="f5d81-106">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

<span data-ttu-id="f5d81-107">El objeto de **\_ Sistema CIM** y sus derivados son objetos de nivel superior de CIM.</span><span class="sxs-lookup"><span data-stu-id="f5d81-107">The **CIM\_System** object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="f5d81-108">Proporcionan el ámbito para numerosos componentes y deben tener claves de sistema únicas.</span><span class="sxs-lookup"><span data-stu-id="f5d81-108">They provide the scope for numerous components and are required to have unique system keys.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5d81-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f5d81-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f5d81-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f5d81-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f5d81-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f5d81-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f5d81-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f5d81-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d81-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5d81-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C524-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_System : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
};
```

## <a name="members"></a><span data-ttu-id="f5d81-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="f5d81-114">Members</span></span>

<span data-ttu-id="f5d81-115">La **clase \_ del sistema CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f5d81-115">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="f5d81-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5d81-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5d81-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5d81-117">Properties</span></span>

<span data-ttu-id="f5d81-118">La **clase \_ del sistema CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f5d81-118">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5d81-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f5d81-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5d81-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5d81-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5d81-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-122">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f5d81-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f5d81-123">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f5d81-123">A short textual description of the object.</span></span>

<span data-ttu-id="f5d81-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5d81-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5d81-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f5d81-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5d81-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5d81-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5d81-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-128">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f5d81-128">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f5d81-129">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="f5d81-129">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f5d81-130">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="f5d81-130">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="f5d81-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f5d81-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5d81-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5d81-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5d81-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-134">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="f5d81-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f5d81-135">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f5d81-135">A textual description of the object.</span></span>

<span data-ttu-id="f5d81-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5d81-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5d81-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f5d81-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5d81-138">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f5d81-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5d81-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-140">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="f5d81-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f5d81-141">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="f5d81-141">Indicates when the object was installed.</span></span> <span data-ttu-id="f5d81-142">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="f5d81-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f5d81-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5d81-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5d81-144">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f5d81-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5d81-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5d81-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5d81-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-147">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f5d81-147">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f5d81-148">Define la etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="f5d81-148">Defines the label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="f5d81-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="f5d81-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5d81-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5d81-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5d81-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5d81-152">Identifica cómo se generó el nombre del sistema, mediante la heurística de subclases.</span><span class="sxs-lookup"><span data-stu-id="f5d81-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="f5d81-153">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="f5d81-153">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5d81-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5d81-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5d81-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5d81-156">Cómo se puede alcanzar el propietario del sistema principal (por ejemplo, el número de teléfono o la dirección de correo electrónico).</span><span class="sxs-lookup"><span data-stu-id="f5d81-156">How the primary system owner can be reached (for example, phone number or email address).</span></span>

</dd> <dt>

<span data-ttu-id="f5d81-157">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="f5d81-157">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5d81-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5d81-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5d81-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-160">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f5d81-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f5d81-161">Nombre del propietario del sistema principal.</span><span class="sxs-lookup"><span data-stu-id="f5d81-161">Name of the primary system owner.</span></span>

</dd> <dt>

<span data-ttu-id="f5d81-162">**Roles**</span><span class="sxs-lookup"><span data-stu-id="f5d81-162">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5d81-163">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f5d81-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-164">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f5d81-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f5d81-165">Roles que el sistema desempeña en el entorno de tecnología de la información.</span><span class="sxs-lookup"><span data-stu-id="f5d81-165">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="f5d81-166">Las subclases del sistema pueden invalidar esta propiedad para definir valores de rol explícitos.</span><span class="sxs-lookup"><span data-stu-id="f5d81-166">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="f5d81-167">Como alternativa, un grupo de trabajo puede describir la heurística, las convenciones y las directrices para especificar los roles.</span><span class="sxs-lookup"><span data-stu-id="f5d81-167">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="f5d81-168">Por ejemplo, para una instancia de un sistema de red, esta propiedad puede contener la cadena "switch" o "Bridge".</span><span class="sxs-lookup"><span data-stu-id="f5d81-168">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

</dd> <dt>

<span data-ttu-id="f5d81-169">**Estado**</span><span class="sxs-lookup"><span data-stu-id="f5d81-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5d81-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5d81-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5d81-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5d81-172">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f5d81-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f5d81-173">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f5d81-173">String that indicates the current status of the object.</span></span> <span data-ttu-id="f5d81-174">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="f5d81-174">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f5d81-175">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="f5d81-175">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f5d81-176">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="f5d81-176">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f5d81-177">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="f5d81-177">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f5d81-178">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="f5d81-178">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f5d81-179">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="f5d81-179">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f5d81-180">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5d81-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f5d81-181">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5d81-181">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f5d81-182">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="f5d81-182">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f5d81-183">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="f5d81-183">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f5d81-184">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f5d81-184">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f5d81-185">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="f5d81-185">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f5d81-186">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="f5d81-186">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f5d81-187">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="f5d81-187">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f5d81-188">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="f5d81-188">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f5d81-189">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="f5d81-189">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f5d81-190">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="f5d81-190">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f5d81-191">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f5d81-191">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f5d81-192">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="f5d81-192">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f5d81-193">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="f5d81-193">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="f5d81-194"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f5d81-194"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f5d81-195">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5d81-195">Remarks</span></span>

<span data-ttu-id="f5d81-196">La **clase \_ del sistema CIM** se deriva de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5d81-196">The **CIM\_System** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="f5d81-197">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="f5d81-197">WMI does not implement this class.</span></span> <span data-ttu-id="f5d81-198">Para las clases WMI derivadas del **\_ Sistema CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f5d81-198">For WMI classes derived from **CIM\_System**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f5d81-199">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f5d81-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f5d81-200">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f5d81-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d81-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5d81-201">Requirements</span></span>



| <span data-ttu-id="f5d81-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5d81-202">Requirement</span></span> | <span data-ttu-id="f5d81-203">Value</span><span class="sxs-lookup"><span data-stu-id="f5d81-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d81-204">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5d81-204">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d81-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5d81-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5d81-206">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5d81-206">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d81-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5d81-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5d81-208">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f5d81-208">Namespace</span></span><br/>                | <span data-ttu-id="f5d81-209">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f5d81-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f5d81-210">MOF</span><span class="sxs-lookup"><span data-stu-id="f5d81-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5d81-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5d81-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5d81-212">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5d81-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5d81-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5d81-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5d81-214">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5d81-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d81-215">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="f5d81-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

