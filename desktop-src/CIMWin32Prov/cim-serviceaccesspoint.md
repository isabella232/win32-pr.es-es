---
description: La \_ clase CIM punto representa la capacidad de usar o invocar un servicio. Los puntos de acceso representan servicios que están disponibles para su uso por parte de otras entidades.
ms.assetid: caf828a1-c9a7-4ae8-9734-d77e4ba90b09
ms.tgt_platform: multiple
title: CIM_ServiceAccessPoint (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.Caption
- CIM_ServiceAccessPoint.Description
- CIM_ServiceAccessPoint.InstallDate
- CIM_ServiceAccessPoint.Status
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 681e5e11de525e535f7965b72adb8ac0e316f7aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538764"
---
# <a name="cim_serviceaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="e530f-104">CIM_ServiceAccessPoint (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="e530f-104">CIM_ServiceAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e530f-105">La clase **CIM \_ punto** representa la capacidad de usar o invocar un servicio.</span><span class="sxs-lookup"><span data-stu-id="e530f-105">The **CIM\_ServiceAccessPoint** class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="e530f-106">Los puntos de acceso representan servicios que están disponibles para su uso por parte de otras entidades.</span><span class="sxs-lookup"><span data-stu-id="e530f-106">Access points represent services that are available for use by other entities.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e530f-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="e530f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e530f-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e530f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e530f-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e530f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e530f-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e530f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e530f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e530f-111">Syntax</span></span>

``` syntax
[UUID("{F126ACC2-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessPoint : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="e530f-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="e530f-112">Members</span></span>

<span data-ttu-id="e530f-113">La clase **CIM \_ punto** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e530f-113">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="e530f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e530f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e530f-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e530f-115">Properties</span></span>

<span data-ttu-id="e530f-116">La clase **CIM \_ punto** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e530f-116">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e530f-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e530f-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e530f-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e530f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e530f-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e530f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e530f-120">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e530f-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e530f-121">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e530f-121">A short textual description of the object.</span></span>

<span data-ttu-id="e530f-122">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e530f-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e530f-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e530f-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e530f-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e530f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e530f-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e530f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e530f-126">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e530f-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e530f-127">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="e530f-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e530f-128">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="e530f-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="e530f-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e530f-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e530f-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e530f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e530f-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e530f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e530f-132">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="e530f-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e530f-133">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e530f-133">A textual description of the object.</span></span>

<span data-ttu-id="e530f-134">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e530f-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e530f-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e530f-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e530f-136">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e530f-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e530f-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e530f-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e530f-138">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="e530f-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e530f-139">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="e530f-139">Indicates when the object was installed.</span></span> <span data-ttu-id="e530f-140">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="e530f-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e530f-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e530f-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e530f-142">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e530f-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e530f-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e530f-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e530f-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e530f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e530f-145">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e530f-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e530f-146">Identifica de forma única el punto de acceso al servicio y proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="e530f-146">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="e530f-147">Esta funcionalidad se describe con más detalle en la propiedad Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e530f-147">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="e530f-148">**Estado**</span><span class="sxs-lookup"><span data-stu-id="e530f-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e530f-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e530f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e530f-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e530f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e530f-151">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e530f-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e530f-152">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e530f-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="e530f-153">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="e530f-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e530f-154">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="e530f-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e530f-155">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="e530f-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e530f-156">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="e530f-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e530f-157">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="e530f-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e530f-158">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="e530f-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e530f-159">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e530f-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e530f-160">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e530f-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e530f-161">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="e530f-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e530f-162">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="e530f-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e530f-163">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="e530f-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e530f-164">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="e530f-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e530f-165">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="e530f-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e530f-166">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="e530f-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e530f-167">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="e530f-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e530f-168">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="e530f-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e530f-169">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="e530f-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e530f-170">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="e530f-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e530f-171">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="e530f-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e530f-172">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="e530f-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e530f-173">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e530f-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e530f-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e530f-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e530f-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e530f-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e530f-176">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e530f-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e530f-177">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e530f-177">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="e530f-178">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e530f-178">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e530f-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e530f-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e530f-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e530f-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e530f-181">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e530f-181">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e530f-182">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e530f-182">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="e530f-183">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e530f-183">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e530f-184">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e530f-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e530f-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e530f-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e530f-186">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e530f-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e530f-187">Tipo de SAP, como adjuntado o redirigido.</span><span class="sxs-lookup"><span data-stu-id="e530f-187">Type of SAP, such as attached or redirected.</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="e530f-188">**Escritura** (1)</span><span class="sxs-lookup"><span data-stu-id="e530f-188">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="e530f-189">**Lectura** (2)</span><span class="sxs-lookup"><span data-stu-id="e530f-189">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="e530f-190">**Redirigido** (4)</span><span class="sxs-lookup"><span data-stu-id="e530f-190">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="e530f-191">**Net \_ Adjunta** (8)</span><span class="sxs-lookup"><span data-stu-id="e530f-191">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e530f-192">**desconocido** (16)</span><span class="sxs-lookup"><span data-stu-id="e530f-192">**unknown** (16)</span></span>


<span data-ttu-id="e530f-193"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e530f-193"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e530f-194">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e530f-194">Remarks</span></span>

<span data-ttu-id="e530f-195">La clase **CIM \_ punto** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e530f-195">The **CIM\_ServiceAccessPoint** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="e530f-196">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="e530f-196">WMI does not implement this class.</span></span> <span data-ttu-id="e530f-197">Para las clases WMI derivadas de **CIM \_ punto**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e530f-197">For WMI classes derived from **CIM\_ServiceAccessPoint**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e530f-198">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="e530f-198">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e530f-199">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="e530f-199">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e530f-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e530f-200">Requirements</span></span>



| <span data-ttu-id="e530f-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="e530f-201">Requirement</span></span> | <span data-ttu-id="e530f-202">Value</span><span class="sxs-lookup"><span data-stu-id="e530f-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e530f-203">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e530f-203">Minimum supported client</span></span><br/> | <span data-ttu-id="e530f-204">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e530f-204">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e530f-205">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e530f-205">Minimum supported server</span></span><br/> | <span data-ttu-id="e530f-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e530f-206">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e530f-207">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e530f-207">Namespace</span></span><br/>                | <span data-ttu-id="e530f-208">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e530f-208">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e530f-209">MOF</span><span class="sxs-lookup"><span data-stu-id="e530f-209">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e530f-210"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e530f-210"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e530f-211">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e530f-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e530f-212"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e530f-212"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e530f-213">Vea también</span><span class="sxs-lookup"><span data-stu-id="e530f-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e530f-214">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e530f-214">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

