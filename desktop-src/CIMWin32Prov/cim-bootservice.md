---
description: La \_ clase CIM BootService representa la funcionalidad proporcionada por un dispositivo o software, o por una red, para cargar un sistema operativo en un sistema de equipo unitario.
ms.assetid: d9c969bb-0f54-4e94-8e19-7ccd6f5adfb3
ms.tgt_platform: multiple
title: CIM_BootService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService
- CIM_BootService.Caption
- CIM_BootService.Description
- CIM_BootService.InstallDate
- CIM_BootService.Status
- CIM_BootService.CreationClassName
- CIM_BootService.Name
- CIM_BootService.Started
- CIM_BootService.StartMode
- CIM_BootService.SystemCreationClassName
- CIM_BootService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d32a8fdfe61e02e6ffe3a8dd2f115e57f338aec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659639"
---
# <a name="cim_bootservice-class"></a><span data-ttu-id="779ac-103">\_Clase BootService de CIM</span><span class="sxs-lookup"><span data-stu-id="779ac-103">CIM\_BootService class</span></span>

<span data-ttu-id="779ac-104">La clase **CIM \_ BootService** representa la funcionalidad proporcionada por un dispositivo o software, o por una red, para cargar un sistema operativo en un sistema de equipo unitario.</span><span class="sxs-lookup"><span data-stu-id="779ac-104">The **CIM\_BootService** class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="779ac-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="779ac-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="779ac-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="779ac-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="779ac-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="779ac-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="779ac-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="779ac-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="779ac-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="779ac-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FE-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_BootService : CIM_Service
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="779ac-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="779ac-110">Members</span></span>

<span data-ttu-id="779ac-111">La clase **CIM \_ BootService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="779ac-111">The **CIM\_BootService** class has these types of members:</span></span>

-   [<span data-ttu-id="779ac-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="779ac-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="779ac-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="779ac-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="779ac-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="779ac-114">Methods</span></span>

<span data-ttu-id="779ac-115">La clase **CIM \_ BootService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="779ac-115">The **CIM\_BootService** class has these methods.</span></span>



| <span data-ttu-id="779ac-116">Método</span><span class="sxs-lookup"><span data-stu-id="779ac-116">Method</span></span>                                                               | <span data-ttu-id="779ac-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="779ac-117">Description</span></span>                                                               |
|:---------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="779ac-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="779ac-118">**StartService**</span></span>](startservice-method-in-class-cim-bootservice.md) | <span data-ttu-id="779ac-119">Pone el servicio en estado Iniciado.</span><span class="sxs-lookup"><span data-stu-id="779ac-119">Puts the service in the started state.</span></span> <span data-ttu-id="779ac-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="779ac-120">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="779ac-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="779ac-121">**StopService**</span></span>](stopservice-method-in-class-cim-bootservice.md)   | <span data-ttu-id="779ac-122">Pone el servicio en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="779ac-122">Puts the service in the stopped state.</span></span> <span data-ttu-id="779ac-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="779ac-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="779ac-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="779ac-124">Properties</span></span>

<span data-ttu-id="779ac-125">La clase **CIM \_ BootService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="779ac-125">The **CIM\_BootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="779ac-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="779ac-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="779ac-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="779ac-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="779ac-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="779ac-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="779ac-129">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="779ac-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="779ac-130">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="779ac-130">A short textual description of the object.</span></span>

<span data-ttu-id="779ac-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="779ac-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="779ac-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="779ac-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="779ac-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="779ac-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="779ac-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="779ac-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="779ac-135">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="779ac-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="779ac-136">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="779ac-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="779ac-137">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="779ac-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="779ac-138">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="779ac-138">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="779ac-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="779ac-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="779ac-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="779ac-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="779ac-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="779ac-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="779ac-142">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="779ac-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="779ac-143">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="779ac-143">A textual description of the object.</span></span>

<span data-ttu-id="779ac-144">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="779ac-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="779ac-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="779ac-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="779ac-146">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="779ac-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="779ac-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="779ac-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="779ac-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="779ac-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="779ac-149">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="779ac-149">Indicates when the object was installed.</span></span> <span data-ttu-id="779ac-150">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="779ac-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="779ac-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="779ac-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="779ac-152">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="779ac-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="779ac-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="779ac-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="779ac-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="779ac-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="779ac-155">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="779ac-155">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="779ac-156">La propiedad Name identifica de forma única el servicio y proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="779ac-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="779ac-157">Esta funcionalidad se describe con más detalle en la propiedad **Descripción** del objeto.</span><span class="sxs-lookup"><span data-stu-id="779ac-157">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="779ac-158">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="779ac-158">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="779ac-159">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="779ac-159">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="779ac-160">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="779ac-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="779ac-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="779ac-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="779ac-162">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="779ac-162">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="779ac-163">Si **es true**, el servicio se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="779ac-163">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="779ac-164">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="779ac-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="779ac-165">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="779ac-165">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="779ac-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="779ac-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="779ac-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="779ac-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="779ac-168">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modo de inicio")</span><span class="sxs-lookup"><span data-stu-id="779ac-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="779ac-169">Indica si el servicio se inicia automáticamente (por ejemplo, por un sistema operativo) o solo se inicia después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="779ac-169">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="779ac-170">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="779ac-170">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="779ac-171">**Automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="779ac-171">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="779ac-172">**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="779ac-172">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="779ac-173">**Estado**</span><span class="sxs-lookup"><span data-stu-id="779ac-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="779ac-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="779ac-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="779ac-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="779ac-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="779ac-176">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="779ac-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="779ac-177">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="779ac-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="779ac-178">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="779ac-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="779ac-179">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="779ac-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="779ac-180">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="779ac-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="779ac-181">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="779ac-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="779ac-182">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="779ac-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="779ac-183">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="779ac-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="779ac-184">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="779ac-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="779ac-185">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="779ac-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="779ac-186">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="779ac-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="779ac-187">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="779ac-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="779ac-188">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="779ac-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="779ac-189">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="779ac-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="779ac-190">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="779ac-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="779ac-191">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="779ac-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="779ac-192">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="779ac-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="779ac-193">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="779ac-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="779ac-194">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="779ac-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="779ac-195">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="779ac-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="779ac-196">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="779ac-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="779ac-197">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="779ac-197">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="779ac-198">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="779ac-198">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="779ac-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="779ac-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="779ac-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="779ac-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="779ac-201">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class name ")</span><span class="sxs-lookup"><span data-stu-id="779ac-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="779ac-202">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="779ac-202">Scoping system's creation class name.</span></span>

<span data-ttu-id="779ac-203">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="779ac-203">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="779ac-204">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="779ac-204">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="779ac-205">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="779ac-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="779ac-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="779ac-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="779ac-207">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema ")</span><span class="sxs-lookup"><span data-stu-id="779ac-207">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="779ac-208">Nombre del sistema que hospeda el servicio.</span><span class="sxs-lookup"><span data-stu-id="779ac-208">Name of the system that hosts the service.</span></span>

<span data-ttu-id="779ac-209">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="779ac-209">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="779ac-210">Observaciones</span><span class="sxs-lookup"><span data-stu-id="779ac-210">Remarks</span></span>

<span data-ttu-id="779ac-211">La clase **CIM \_ BootService** se deriva del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="779ac-211">The **CIM\_BootService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="779ac-212">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="779ac-212">WMI does not implement this class.</span></span>

<span data-ttu-id="779ac-213">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="779ac-213">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="779ac-214">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="779ac-214">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="779ac-215">Requisitos</span><span class="sxs-lookup"><span data-stu-id="779ac-215">Requirements</span></span>



| <span data-ttu-id="779ac-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="779ac-216">Requirement</span></span> | <span data-ttu-id="779ac-217">Value</span><span class="sxs-lookup"><span data-stu-id="779ac-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="779ac-218">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="779ac-218">Minimum supported client</span></span><br/> | <span data-ttu-id="779ac-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="779ac-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="779ac-220">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="779ac-220">Minimum supported server</span></span><br/> | <span data-ttu-id="779ac-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="779ac-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="779ac-222">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="779ac-222">Namespace</span></span><br/>                | <span data-ttu-id="779ac-223">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="779ac-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="779ac-224">MOF</span><span class="sxs-lookup"><span data-stu-id="779ac-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="779ac-225"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="779ac-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="779ac-226">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="779ac-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="779ac-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="779ac-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="779ac-228">Vea también</span><span class="sxs-lookup"><span data-stu-id="779ac-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="779ac-229">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="779ac-229">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

