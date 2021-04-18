---
description: La \_ clase de servicio CIM representa un elemento lógico que contiene información para representar y administrar la funcionalidad proporcionada por una característica de dispositivo o software.
ms.assetid: b95e8ea7-4daf-4dcf-817c-b872560b62df
ms.tgt_platform: multiple
title: CIM_Service (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.Caption
- CIM_Service.Description
- CIM_Service.InstallDate
- CIM_Service.Status
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.Started
- CIM_Service.StartMode
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1656d9aa5e5ee8c58c5895a444afd7552227108c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659512"
---
# <a name="cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="6071b-103">CIM_Service (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="6071b-103">CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="6071b-104">La clase de **\_ servicio CIM** representa un elemento lógico que contiene información para representar y administrar la funcionalidad proporcionada por una característica de dispositivo o software.</span><span class="sxs-lookup"><span data-stu-id="6071b-104">The **CIM\_Service** class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="6071b-105">Un servicio es un objeto de uso general para configurar y administrar la implementación de la funcionalidad. no es la propia funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="6071b-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6071b-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="6071b-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6071b-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6071b-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6071b-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6071b-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6071b-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6071b-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6071b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6071b-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C527-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services (CIM)"), AMENDMENT]
class CIM_Service : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="6071b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="6071b-111">Members</span></span>

<span data-ttu-id="6071b-112">La clase de **\_ servicio CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6071b-112">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="6071b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="6071b-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="6071b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6071b-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6071b-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="6071b-115">Methods</span></span>

<span data-ttu-id="6071b-116">La clase de **\_ servicio CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6071b-116">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="6071b-117">Método</span><span class="sxs-lookup"><span data-stu-id="6071b-117">Method</span></span>                                                           | <span data-ttu-id="6071b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="6071b-118">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6071b-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="6071b-119">**StartService**</span></span>](startservice-method-in-class-cim-service.md) | <span data-ttu-id="6071b-120">Intenta poner el servicio en su estado de inicio.</span><span class="sxs-lookup"><span data-stu-id="6071b-120">Attempts to put the service into its start-up state.</span></span> <span data-ttu-id="6071b-121">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="6071b-121">Not implemented by WMI.</span></span><br/>     |
| [<span data-ttu-id="6071b-122">**StopService**</span><span class="sxs-lookup"><span data-stu-id="6071b-122">**StopService**</span></span>](stopservice-method-in-class-cim-service.md)   | <span data-ttu-id="6071b-123">Método de clase que coloca el servicio en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="6071b-123">Class method that puts the service in the stopped state.</span></span> <span data-ttu-id="6071b-124">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="6071b-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6071b-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6071b-125">Properties</span></span>

<span data-ttu-id="6071b-126">La clase de **\_ servicio CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6071b-126">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6071b-127">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6071b-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6071b-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6071b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6071b-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6071b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6071b-130">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6071b-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6071b-131">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6071b-131">A short textual description of the object.</span></span>

<span data-ttu-id="6071b-132">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6071b-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6071b-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6071b-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6071b-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6071b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6071b-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6071b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6071b-136">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="6071b-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6071b-137">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="6071b-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6071b-138">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="6071b-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="6071b-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6071b-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6071b-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6071b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6071b-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6071b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6071b-142">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="6071b-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6071b-143">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6071b-143">A textual description of the object.</span></span>

<span data-ttu-id="6071b-144">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6071b-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6071b-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6071b-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6071b-146">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6071b-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6071b-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6071b-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6071b-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="6071b-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6071b-149">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="6071b-149">Indicates when the object was installed.</span></span> <span data-ttu-id="6071b-150">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="6071b-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6071b-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6071b-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6071b-152">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="6071b-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6071b-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6071b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6071b-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6071b-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6071b-155">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6071b-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6071b-156">La propiedad Name identifica de forma única el servicio y proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="6071b-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="6071b-157">Esta funcionalidad se describe con más detalle en la propiedad Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="6071b-157">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="6071b-158">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="6071b-158">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6071b-159">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6071b-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6071b-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6071b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6071b-161">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="6071b-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="6071b-162">Si **es true**, el servicio se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="6071b-162">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="6071b-163">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="6071b-163">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6071b-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6071b-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6071b-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6071b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6071b-166">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modo de inicio")</span><span class="sxs-lookup"><span data-stu-id="6071b-166">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="6071b-167">Indica si el servicio se inicia automáticamente (por ejemplo, por un sistema operativo) o solo se inicia después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6071b-167">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="6071b-168">**Automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="6071b-168">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="6071b-169">**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="6071b-169">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6071b-170">**Estado**</span><span class="sxs-lookup"><span data-stu-id="6071b-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6071b-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6071b-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6071b-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6071b-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6071b-173">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="6071b-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6071b-174">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6071b-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="6071b-175">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="6071b-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6071b-176">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="6071b-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6071b-177">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="6071b-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6071b-178">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="6071b-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6071b-179">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="6071b-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6071b-180">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="6071b-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6071b-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6071b-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6071b-182">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6071b-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6071b-183">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="6071b-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6071b-184">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="6071b-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6071b-185">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="6071b-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6071b-186">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="6071b-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6071b-187">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="6071b-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6071b-188">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="6071b-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6071b-189">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="6071b-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6071b-190">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="6071b-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6071b-191">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="6071b-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6071b-192">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="6071b-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6071b-193">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="6071b-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6071b-194">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="6071b-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6071b-195">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6071b-195">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6071b-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6071b-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6071b-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6071b-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6071b-198">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class name ")</span><span class="sxs-lookup"><span data-stu-id="6071b-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6071b-199">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="6071b-199">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="6071b-200">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6071b-200">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6071b-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6071b-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6071b-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6071b-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6071b-203">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema ")</span><span class="sxs-lookup"><span data-stu-id="6071b-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6071b-204">Nombre del sistema que hospeda el servicio.</span><span class="sxs-lookup"><span data-stu-id="6071b-204">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6071b-205">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6071b-205">Remarks</span></span>

<span data-ttu-id="6071b-206">La clase de **\_ servicio CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6071b-206">The **CIM\_Service** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6071b-207">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="6071b-207">WMI does not implement this class.</span></span> <span data-ttu-id="6071b-208">Para las clases WMI que se derivan del **\_ servicio CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6071b-208">For WMI classes that are derived from **CIM\_Service**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6071b-209">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="6071b-209">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6071b-210">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="6071b-210">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6071b-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6071b-211">Requirements</span></span>



| <span data-ttu-id="6071b-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="6071b-212">Requirement</span></span> | <span data-ttu-id="6071b-213">Value</span><span class="sxs-lookup"><span data-stu-id="6071b-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6071b-214">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6071b-214">Minimum supported client</span></span><br/> | <span data-ttu-id="6071b-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6071b-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6071b-216">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6071b-216">Minimum supported server</span></span><br/> | <span data-ttu-id="6071b-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6071b-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6071b-218">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6071b-218">Namespace</span></span><br/>                | <span data-ttu-id="6071b-219">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6071b-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6071b-220">MOF</span><span class="sxs-lookup"><span data-stu-id="6071b-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6071b-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6071b-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6071b-222">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6071b-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6071b-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6071b-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6071b-224">Vea también</span><span class="sxs-lookup"><span data-stu-id="6071b-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6071b-225">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6071b-225">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

