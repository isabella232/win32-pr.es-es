---
description: Actúa como clase base para todos los eventos intrínsecos que se relacionan con una instancia de.
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: __InstanceOperationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707110"
---
# <a name="__instanceoperationevent-class"></a><span data-ttu-id="2cb23-103">\_\_Clase InstanceOperationEvent</span><span class="sxs-lookup"><span data-stu-id="2cb23-103">\_\_InstanceOperationEvent class</span></span>

<span data-ttu-id="2cb23-104">La clase del sistema **\_ \_ InstanceOperationEvent** actúa como clase base para todos los eventos intrínsecos que se relacionan con una instancia de.</span><span class="sxs-lookup"><span data-stu-id="2cb23-104">The **\_\_InstanceOperationEvent** system class serves as a base class for all intrinsic events that relate to an instance.</span></span>

<span data-ttu-id="2cb23-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2cb23-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2cb23-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2cb23-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb23-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cb23-107">Syntax</span></span>

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="2cb23-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2cb23-108">Members</span></span>

<span data-ttu-id="2cb23-109">La clase **\_ \_ InstanceOperationEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2cb23-109">The **\_\_InstanceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="2cb23-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2cb23-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2cb23-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2cb23-111">Properties</span></span>

<span data-ttu-id="2cb23-112">La clase **\_ \_ InstanceOperationEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2cb23-112">The **\_\_InstanceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2cb23-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="2cb23-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb23-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="2cb23-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2cb23-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb23-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cb23-116">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="2cb23-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="2cb23-117">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="2cb23-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cb23-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="2cb23-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb23-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="2cb23-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2cb23-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb23-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cb23-121">Instancia afectada por el evento.</span><span class="sxs-lookup"><span data-stu-id="2cb23-121">Instance affected by the event.</span></span> <span data-ttu-id="2cb23-122">En el caso de los eventos de creación, esta es la instancia que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="2cb23-122">For creation events, this is the newly created instance.</span></span> <span data-ttu-id="2cb23-123">En el caso de los eventos de modificación, se trata de la nueva versión de la instancia modificada.</span><span class="sxs-lookup"><span data-stu-id="2cb23-123">For modification events, this is the new version of the changed instance.</span></span> <span data-ttu-id="2cb23-124">En el caso de los eventos de eliminación, se trata de la instancia eliminada.</span><span class="sxs-lookup"><span data-stu-id="2cb23-124">For deletion events, this is the deleted instance.</span></span>

</dd> <dt>

<span data-ttu-id="2cb23-125">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="2cb23-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb23-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2cb23-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2cb23-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb23-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cb23-128">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="2cb23-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="2cb23-129">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="2cb23-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="2cb23-130">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="2cb23-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="2cb23-131">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="2cb23-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="2cb23-132">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2cb23-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2cb23-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2cb23-133">Remarks</span></span>

<span data-ttu-id="2cb23-134">La clase **\_ \_ InstanceOperationEvent** se deriva de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="2cb23-134">The **\_\_InstanceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="2cb23-135">No se crean instancias de **\_ \_ InstanceOperationEvent** ; solo se crean las instancias de sus subclases.</span><span class="sxs-lookup"><span data-stu-id="2cb23-135">Instances of **\_\_InstanceOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="2cb23-136">Las siguientes clases se derivan de **\_ \_ InstanceOperationEvent**:</span><span class="sxs-lookup"><span data-stu-id="2cb23-136">The following classes derive from **\_\_InstanceOperationEvent**:</span></span>

[<span data-ttu-id="2cb23-137">**\_\_InstanceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="2cb23-137">**\_\_InstanceCreationEvent**</span></span>](--instancecreationevent.md)

[<span data-ttu-id="2cb23-138">**\_\_InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="2cb23-138">**\_\_InstanceModificationEvent**</span></span>](--instancemodificationevent.md)

[<span data-ttu-id="2cb23-139">**\_\_InstanceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="2cb23-139">**\_\_InstanceDeletionEvent**</span></span>](--instancedeletionevent.md)

<span data-ttu-id="2cb23-140">**Información general**</span><span class="sxs-lookup"><span data-stu-id="2cb23-140">**Overview**</span></span>

<span data-ttu-id="2cb23-141">Del mismo modo que hay una clase WMI que representa cada tipo de recurso del sistema que se puede administrar mediante WMI, existe una clase WMI que representa cada tipo de evento WMI.</span><span class="sxs-lookup"><span data-stu-id="2cb23-141">Just as there is a WMI class that represents each type of system resource that can be managed using WMI, there is a WMI class that represents each type of WMI event.</span></span> <span data-ttu-id="2cb23-142">Cuando se produce un evento que se puede supervisar mediante WMI, se crea una instancia de la clase de eventos de WMI correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2cb23-142">When an event that can be monitored by WMI occurs, an instance of the corresponding WMI event class is created.</span></span> <span data-ttu-id="2cb23-143">Se produce un evento WMI cuando se crea la instancia.</span><span class="sxs-lookup"><span data-stu-id="2cb23-143">A WMI event occurs when that instance is created.</span></span>

<span data-ttu-id="2cb23-144">Hay tres tipos principales de clases de eventos de WMI, que se derivan de la clase WMI de [**\_ \_ eventos**](--event.md) : eventos intrínsecos, eventos extrínsecos y eventos de temporizador.</span><span class="sxs-lookup"><span data-stu-id="2cb23-144">There are three major types of WMI event classes, all of which are derived from the [**\_\_Event**](--event.md) WMI class: Intrinsic Events, Extrinsic Events, and Timer Events.</span></span> <span data-ttu-id="2cb23-145">A su vez, los eventos intrínsecos se representan mediante tres clases distintas derivadas de la clase de **\_ \_ evento** : [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md), **\_ \_ InstanceOperationEvent** y [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="2cb23-145">Intrinsic Events, in turn, are represented by three distinct classes derived from the **\_\_Event** class: [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md), **\_\_InstanceOperationEvent**, and [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="2cb23-146">Eventos intrínsecos</span><span class="sxs-lookup"><span data-stu-id="2cb23-146">Intrinsic Events</span></span>

<span data-ttu-id="2cb23-147">Los eventos intrínsecos se utilizan para supervisar un recurso representado por una clase en el repositorio CIM.</span><span class="sxs-lookup"><span data-stu-id="2cb23-147">Intrinsic events are used to monitor a resource represented by a class in the CIM repository.</span></span> <span data-ttu-id="2cb23-148">Cada recurso se representa mediante una instancia de una clase.</span><span class="sxs-lookup"><span data-stu-id="2cb23-148">Each resource is represented by an instance of a class.</span></span> <span data-ttu-id="2cb23-149">Esto significa que la supervisión de un recurso mediante WMI implica realmente la supervisión de las instancias que se corresponden con el recurso.</span><span class="sxs-lookup"><span data-stu-id="2cb23-149">This means that monitoring a resource using WMI actually involves monitoring the instances that correspond to the resource.</span></span>

<span data-ttu-id="2cb23-150">Los eventos intrínsecos también se pueden usar para supervisar los cambios en un espacio de nombres o una clase en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="2cb23-150">Intrinsic events can also be used to monitor changes to a namespace or class in the repository.</span></span> <span data-ttu-id="2cb23-151">Sin embargo, la supervisión de los cambios en los espacios de nombres o las clases es de un valor limitado para los administradores del sistema.</span><span class="sxs-lookup"><span data-stu-id="2cb23-151">However, monitoring changes to namespaces or classes is of limited value to system administrators.</span></span>

<span data-ttu-id="2cb23-152">Un evento intrínseco se representa mediante una instancia de una clase derivada de \_ \_ InstanceOperationEvent, \_ \_ NamespaceOperationEvent o \_ \_ ClassOperationEvent.</span><span class="sxs-lookup"><span data-stu-id="2cb23-152">An intrinsic event is represented by an instance of a class derived from \_\_InstanceOperationEvent, \_\_NamespaceOperationEvent, or \_\_ClassOperationEvent.</span></span> <span data-ttu-id="2cb23-153">Los cambios en las instancias de WMI se representan mediante la \_ \_ clase InstanceOperationEvent y las clases derivadas de ella: \_ \_ InstanceCreationEvent, \_ \_ InstanceModificationEvent y \_ \_ InstanceDeletionEvent.</span><span class="sxs-lookup"><span data-stu-id="2cb23-153">Any changes to instances in WMI are represented by the \_\_InstanceOperationEvent class and the classes derived from it: \_\_InstanceCreationEvent, \_\_InstanceModificationEvent, and \_\_InstanceDeletionEvent.</span></span>

<span data-ttu-id="2cb23-154">La supervisión de recursos mediante WMI implica la supervisión de instancias y todos los cambios en las instancias se representan mediante \_ \_ InstanceOperationEvent y las clases derivadas de ella.</span><span class="sxs-lookup"><span data-stu-id="2cb23-154">Monitoring resources using WMI involves monitoring instances and all changes to instances are represented by \_\_InstanceOperationEvent and the classes derived from it.</span></span> <span data-ttu-id="2cb23-155">Esto significa que, en última instancia, los recursos de supervisión implican la supervisión de instancias de \_ \_ clases derivadas de InstanceOperationEvent.</span><span class="sxs-lookup"><span data-stu-id="2cb23-155">This means that monitoring resources ultimately involves monitoring instances of \_\_InstanceOperationEvent-derived classes.</span></span>

<span data-ttu-id="2cb23-156">Para registrar el interés en instancias de una de estas clases, se emite una consulta de notificación expresada en WQL.</span><span class="sxs-lookup"><span data-stu-id="2cb23-156">You register interest in instances of one of these classes by issuing a notification query expressed in WQL.</span></span> <span data-ttu-id="2cb23-157">La consulta utiliza una sintaxis similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="2cb23-157">The query uses syntax similar to the following:</span></span>

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

<span data-ttu-id="2cb23-158">Para obtener una explicación más detallada del uso de los eventos de instancia de WMI para supervisar la actividad del equipo, consulte [¿Cómo puedo supervisar distintos tipos de eventos con un solo script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span><span class="sxs-lookup"><span data-stu-id="2cb23-158">For a longer discussion of using the WMI instance events to monitor computer activity, see [How Can I Monitor for Different Types of Events With Just One Script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="2cb23-159">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2cb23-159">Examples</span></span>

<span data-ttu-id="2cb23-160">El ejemplo de código VBScript del [evento de proceso de supervisión](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) en la galería de TechNet usa **\_ \_ InstanceOperationEvent** para supervisar el primer evento de instancia de WMI para el [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="2cb23-160">The [Monitor process event](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript code sample on TechNet Gallery uses **\_\_InstanceOperationEvent** to monitors the first WMI instance event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cb23-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cb23-161">Requirements</span></span>



| <span data-ttu-id="2cb23-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cb23-162">Requirement</span></span> | <span data-ttu-id="2cb23-163">Value</span><span class="sxs-lookup"><span data-stu-id="2cb23-163">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2cb23-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cb23-164">Minimum supported client</span></span><br/> | <span data-ttu-id="2cb23-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cb23-165">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2cb23-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cb23-166">Minimum supported server</span></span><br/> | <span data-ttu-id="2cb23-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cb23-167">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="2cb23-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2cb23-168">Namespace</span></span><br/>                | <span data-ttu-id="2cb23-169">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="2cb23-169">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2cb23-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cb23-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb23-171">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="2cb23-171">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="2cb23-172">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="2cb23-172">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="2cb23-173">Determinar el tipo de evento que se va a recibir</span><span class="sxs-lookup"><span data-stu-id="2cb23-173">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="2cb23-174">Escribir en un archivo de registro basado en un evento</span><span class="sxs-lookup"><span data-stu-id="2cb23-174">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

