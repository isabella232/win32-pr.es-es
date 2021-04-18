---
description: La \_ clase CIM ClusteringService representa la funcionalidad proporcionada por un clúster. Por ejemplo, la funcionalidad de conmutación por error se puede modelar como un servicio de un clúster de conmutación por error.
ms.assetid: 550e3be3-c1e2-4714-b702-49cb1213c65b
ms.tgt_platform: multiple
title: CIM_ClusteringService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService
- CIM_ClusteringService.Caption
- CIM_ClusteringService.Description
- CIM_ClusteringService.InstallDate
- CIM_ClusteringService.Status
- CIM_ClusteringService.CreationClassName
- CIM_ClusteringService.Name
- CIM_ClusteringService.Started
- CIM_ClusteringService.StartMode
- CIM_ClusteringService.SystemCreationClassName
- CIM_ClusteringService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 40dc0ebd8daebb79c323d54591fc16126e0ef97a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659633"
---
# <a name="cim_clusteringservice-class"></a><span data-ttu-id="1115e-104">\_Clase ClusteringService de CIM</span><span class="sxs-lookup"><span data-stu-id="1115e-104">CIM\_ClusteringService class</span></span>

<span data-ttu-id="1115e-105">La clase **CIM \_ ClusteringService** representa la funcionalidad proporcionada por un clúster.</span><span class="sxs-lookup"><span data-stu-id="1115e-105">The **CIM\_ClusteringService** class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="1115e-106">Por ejemplo, la funcionalidad de conmutación por error se puede modelar como un servicio de un clúster de conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="1115e-106">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1115e-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="1115e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1115e-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1115e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1115e-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1115e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1115e-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1115e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1115e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1115e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{debac832-6b54-4add-8a62-8d3861b97b1d}"), AMENDMENT]
class CIM_ClusteringService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="1115e-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="1115e-112">Members</span></span>

<span data-ttu-id="1115e-113">La clase **CIM \_ ClusteringService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1115e-113">The **CIM\_ClusteringService** class has these types of members:</span></span>

-   [<span data-ttu-id="1115e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="1115e-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="1115e-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1115e-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1115e-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="1115e-116">Methods</span></span>

<span data-ttu-id="1115e-117">La clase **CIM \_ ClusteringService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1115e-117">The **CIM\_ClusteringService** class has these methods.</span></span>



| <span data-ttu-id="1115e-118">Método</span><span class="sxs-lookup"><span data-stu-id="1115e-118">Method</span></span>                                                                     | <span data-ttu-id="1115e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1115e-119">Description</span></span>                                                                                                |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1115e-120">**AddNode**</span><span class="sxs-lookup"><span data-stu-id="1115e-120">**AddNode**</span></span>](addnode-method-in-class-cim-clusteringservice.md)           | <span data-ttu-id="1115e-121">Método de clase que pone un nuevo sistema de equipo en un clúster.</span><span class="sxs-lookup"><span data-stu-id="1115e-121">Class method that brings a new computer system into a cluster.</span></span> <span data-ttu-id="1115e-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="1115e-122">Not implemented by WMI.</span></span><br/>          |
| [<span data-ttu-id="1115e-123">**EvictNode**</span><span class="sxs-lookup"><span data-stu-id="1115e-123">**EvictNode**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)       | <span data-ttu-id="1115e-124">Método de clase que quita un equipo de un clúster.</span><span class="sxs-lookup"><span data-stu-id="1115e-124">Class method that removes a computer system from a cluster.</span></span> <span data-ttu-id="1115e-125">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="1115e-125">Not implemented by WMI.</span></span><br/>             |
| [<span data-ttu-id="1115e-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="1115e-126">**StartService**</span></span>](startservice-method-in-class-cim-clusteringservice.md) | <span data-ttu-id="1115e-127">Método de clase que intenta poner el servicio en su estado de inicio.</span><span class="sxs-lookup"><span data-stu-id="1115e-127">Class method that attempts to place the service into its startup state.</span></span> <span data-ttu-id="1115e-128">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="1115e-128">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="1115e-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="1115e-129">**StopService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)   | <span data-ttu-id="1115e-130">Método de clase que coloca el servicio en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="1115e-130">Class method that places the service in the stopped state.</span></span> <span data-ttu-id="1115e-131">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="1115e-131">Not implemented by WMI.</span></span><br/>              |



 

### <a name="properties"></a><span data-ttu-id="1115e-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1115e-132">Properties</span></span>

<span data-ttu-id="1115e-133">La clase **CIM \_ ClusteringService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1115e-133">The **CIM\_ClusteringService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1115e-134">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1115e-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1115e-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1115e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1115e-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1115e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1115e-137">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1115e-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1115e-138">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1115e-138">A short textual description of the object.</span></span>

<span data-ttu-id="1115e-139">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1115e-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1115e-140">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1115e-140">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1115e-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1115e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1115e-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1115e-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1115e-143">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="1115e-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="1115e-144">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="1115e-144">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1115e-145">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="1115e-145">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1115e-146">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1115e-146">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1115e-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1115e-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1115e-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1115e-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1115e-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1115e-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1115e-150">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="1115e-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1115e-151">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1115e-151">A textual description of the object.</span></span>

<span data-ttu-id="1115e-152">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1115e-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1115e-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1115e-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1115e-154">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1115e-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1115e-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1115e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1115e-156">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="1115e-156">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1115e-157">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="1115e-157">Indicates when the object was installed.</span></span> <span data-ttu-id="1115e-158">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="1115e-158">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1115e-159">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1115e-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1115e-160">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1115e-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1115e-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1115e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1115e-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1115e-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1115e-163">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1115e-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1115e-164">La propiedad Name identifica de forma única el servicio y proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="1115e-164">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="1115e-165">Esta funcionalidad se describe con más detalle en la propiedad Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="1115e-165">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="1115e-166">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1115e-166">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1115e-167">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="1115e-167">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1115e-168">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1115e-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1115e-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1115e-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1115e-170">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="1115e-170">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="1115e-171">Si **es true**, el servicio se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="1115e-171">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="1115e-172">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1115e-172">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1115e-173">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="1115e-173">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1115e-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1115e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1115e-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1115e-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1115e-176">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modo de inicio")</span><span class="sxs-lookup"><span data-stu-id="1115e-176">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="1115e-177">Indica si el servicio se inicia automáticamente (por ejemplo, por un sistema operativo) o solo se inicia después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1115e-177">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="1115e-178">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1115e-178">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="1115e-179">**Automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="1115e-179">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="1115e-180">**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="1115e-180">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1115e-181">**Estado**</span><span class="sxs-lookup"><span data-stu-id="1115e-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1115e-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1115e-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1115e-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1115e-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1115e-184">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="1115e-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1115e-185">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1115e-185">String that indicates the current status of the object.</span></span> <span data-ttu-id="1115e-186">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="1115e-186">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="1115e-187">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="1115e-187">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="1115e-188">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="1115e-188">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="1115e-189">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="1115e-189">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1115e-190">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="1115e-190">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1115e-191">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="1115e-191">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1115e-192">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1115e-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1115e-193">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1115e-193">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1115e-194">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="1115e-194">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1115e-195">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="1115e-195">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1115e-196">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="1115e-196">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1115e-197">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="1115e-197">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1115e-198">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="1115e-198">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1115e-199">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="1115e-199">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1115e-200">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="1115e-200">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1115e-201">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="1115e-201">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1115e-202">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="1115e-202">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1115e-203">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="1115e-203">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1115e-204">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="1115e-204">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1115e-205">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="1115e-205">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1115e-206">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1115e-206">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1115e-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1115e-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1115e-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1115e-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1115e-209">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class name ")</span><span class="sxs-lookup"><span data-stu-id="1115e-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="1115e-210">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1115e-210">Scoping system's creation class name.</span></span>

<span data-ttu-id="1115e-211">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1115e-211">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1115e-212">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1115e-212">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1115e-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1115e-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1115e-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1115e-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1115e-215">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema ")</span><span class="sxs-lookup"><span data-stu-id="1115e-215">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="1115e-216">Nombre del sistema que hospeda el servicio.</span><span class="sxs-lookup"><span data-stu-id="1115e-216">Name of the system that hosts the service.</span></span>

<span data-ttu-id="1115e-217">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1115e-217">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1115e-218">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1115e-218">Remarks</span></span>

<span data-ttu-id="1115e-219">La clase **CIM \_ ClusteringService** se deriva del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1115e-219">The **CIM\_ClusteringService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="1115e-220">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="1115e-220">WMI does not implement this class.</span></span>

<span data-ttu-id="1115e-221">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="1115e-221">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1115e-222">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="1115e-222">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1115e-223">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1115e-223">Requirements</span></span>



| <span data-ttu-id="1115e-224">Requisito</span><span class="sxs-lookup"><span data-stu-id="1115e-224">Requirement</span></span> | <span data-ttu-id="1115e-225">Value</span><span class="sxs-lookup"><span data-stu-id="1115e-225">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1115e-226">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1115e-226">Minimum supported client</span></span><br/> | <span data-ttu-id="1115e-227">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1115e-227">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1115e-228">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1115e-228">Minimum supported server</span></span><br/> | <span data-ttu-id="1115e-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1115e-229">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1115e-230">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1115e-230">Namespace</span></span><br/>                | <span data-ttu-id="1115e-231">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1115e-231">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1115e-232">MOF</span><span class="sxs-lookup"><span data-stu-id="1115e-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1115e-233"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1115e-233"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1115e-234">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1115e-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1115e-235"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1115e-235"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1115e-236">Vea también</span><span class="sxs-lookup"><span data-stu-id="1115e-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1115e-237">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="1115e-237">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

