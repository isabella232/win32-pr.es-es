---
description: El registro de un consumidor de eventos permanente requiere una instancia de la \_ \_ clase del sistema EventFilter.
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: __EventFilter (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706659"
---
# <a name="__eventfilter-class"></a><span data-ttu-id="82c18-103">\_\_Clase EventFilter</span><span class="sxs-lookup"><span data-stu-id="82c18-103">\_\_EventFilter class</span></span>

<span data-ttu-id="82c18-104">El registro de un consumidor de eventos permanente requiere una instancia de la clase del sistema **\_ \_ EventFilter** .</span><span class="sxs-lookup"><span data-stu-id="82c18-104">The registration of a permanent event consumer requires an instance of the **\_\_EventFilter** system class.</span></span>

<span data-ttu-id="82c18-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="82c18-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="82c18-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="82c18-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="82c18-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82c18-107">Syntax</span></span>

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a><span data-ttu-id="82c18-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="82c18-108">Members</span></span>

<span data-ttu-id="82c18-109">La clase **\_ \_ EventFilter** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="82c18-109">The **\_\_EventFilter** class has these types of members:</span></span>

-   [<span data-ttu-id="82c18-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82c18-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82c18-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82c18-111">Properties</span></span>

<span data-ttu-id="82c18-112">La clase **\_ \_ EventFilter** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="82c18-112">The **\_\_EventFilter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82c18-113">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="82c18-113">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82c18-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="82c18-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="82c18-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82c18-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82c18-116">Identificador de seguridad (SID) que identifica de forma única al usuario que crea este filtro.</span><span class="sxs-lookup"><span data-stu-id="82c18-116">Security identifier (SID) that uniquely identifies the user who creates this filter.</span></span> <span data-ttu-id="82c18-117">Instrumental de administración de Windows (WMI) almacena el SID del usuario que crea una instancia de **\_ \_ EventFilter** o el SID de administrador, dependiendo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="82c18-117">Windows Management Instrumentation (WMI) stores the SID of the user that creates an instance of **\_\_EventFilter** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="82c18-118">Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="82c18-118">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="82c18-119">**EventAccess**</span><span class="sxs-lookup"><span data-stu-id="82c18-119">**EventAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82c18-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="82c18-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82c18-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82c18-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82c18-122">Descriptor de seguridad (SD) en el lenguaje de definición de descriptores de seguridad (SDDL) que controla el acceso a los eventos entregados al filtro.</span><span class="sxs-lookup"><span data-stu-id="82c18-122">Security descriptor (SD) in Security Descriptor Definition Language (SDDL) that controls access for events delivered to the filter.</span></span> <span data-ttu-id="82c18-123">Utilice esta propiedad para especificar que solo se puedan entregar a este filtro los eventos en el contexto de seguridad de cuentas específicas.</span><span class="sxs-lookup"><span data-stu-id="82c18-123">Use this property to specify that only events in the security context of specific accounts can be delivered to this filter.</span></span> <span data-ttu-id="82c18-124">Por ejemplo, un consumidor de eventos permanente puede borrar los registros de seguridad solo cuando un usuario específico genera un evento específico.</span><span class="sxs-lookup"><span data-stu-id="82c18-124">For example, a permanent event consumer may clear the security logs only when a specific event is generated by a specific user.</span></span> <span data-ttu-id="82c18-125">Para especificar quién puede publicar eventos en este filtro, use la máscara de **\_ \_ publicación derecha de WBEM** en la entrada de Access Control (ACE) para la propiedad [**\_ descriptor de seguridad**](--event.md) .</span><span class="sxs-lookup"><span data-stu-id="82c18-125">To specify who can publish events to this filter, use the **WBEM\_RIGHT\_PUBLISH** mask in the Access Control Entry (ACE) for the [**SECURITY\_DESCRIPTOR**](--event.md) property.</span></span> <span data-ttu-id="82c18-126">Para obtener más información, vea [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="82c18-126">For more information, see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span> <span data-ttu-id="82c18-127">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="82c18-127">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span> <span data-ttu-id="82c18-128">Para obtener más información y ejemplos, vea reemplazar:[recibir eventos de forma segura](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="82c18-128">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="82c18-129">Puede configurar un descriptor de seguridad de acceso a eventos para permitir que se entregue un evento solo cuando la cuenta de sistema local genera el evento.</span><span class="sxs-lookup"><span data-stu-id="82c18-129">You can configure an event access security descriptor to allow an event to be delivered only when the local system account generates the event.</span></span> <span data-ttu-id="82c18-130">Para obtener más información sobre cómo crear un descriptor de seguridad y autorizar el acceso, consulte [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="82c18-130">For more information about creating security descriptor and authorizing access, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="82c18-131">Ejemplo: la siguiente cadena SDDL permite que solo los administradores proporcionen eventos al filtro.</span><span class="sxs-lookup"><span data-stu-id="82c18-131">Example: The following SDDL string allows only administrators to provide events to the filter.</span></span> <span data-ttu-id="82c18-132">El derecho necesario para proporcionar eventos es **WBEM \_ right \_ PUBLISH** (x80).</span><span class="sxs-lookup"><span data-stu-id="82c18-132">The right required to provide events is **WBEM\_RIGHT\_PUBLISH** (x80).</span></span>


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

<span data-ttu-id="82c18-133">**EventNamespace**</span><span class="sxs-lookup"><span data-stu-id="82c18-133">**EventNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82c18-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="82c18-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82c18-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82c18-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82c18-136">Espacio de nombres de la instancia de evento utilizada para las suscripciones entre espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="82c18-136">Namespace of the event instance used for cross-namespace subscriptions.</span></span>

</dd> <dt>

<span data-ttu-id="82c18-137">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="82c18-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82c18-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="82c18-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82c18-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82c18-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="82c18-140">Calificadores: [ **clave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="82c18-140">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="82c18-141">Identificador único de un filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="82c18-141">Unique identifier of an event filter.</span></span> <span data-ttu-id="82c18-142">Dado que WMI solo usa un filtro de eventos, se recomienda que establezca esta propiedad en un identificador único global (**GUID**) convertido en una cadena.</span><span class="sxs-lookup"><span data-stu-id="82c18-142">Because an event filter is only used internally by WMI, it is recommended that you set this property to a globally unique identifier (**GUID**) converted to a string.</span></span> <span data-ttu-id="82c18-143">Sin embargo, los consumidores pueden usar cualquier esquema privado para un nombre de filtro siempre y cuando no haya ningún conflicto con otros filtros.</span><span class="sxs-lookup"><span data-stu-id="82c18-143">However, consumers can use any private scheme for a filter name as long as there is not a conflict with other filters.</span></span>

</dd> <dt>

<span data-ttu-id="82c18-144">**Consultar**</span><span class="sxs-lookup"><span data-stu-id="82c18-144">**Query**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82c18-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="82c18-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82c18-146">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82c18-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82c18-147">Instrumental de administración de Windows consulta de eventos del lenguaje de consulta (WQL) que especifica el conjunto de eventos para la notificación del consumidor y las condiciones específicas para la notificación.</span><span class="sxs-lookup"><span data-stu-id="82c18-147">Windows Management Instrumentation Query Language (WQL) event query that specifies the set of events for consumer notification, and the specific conditions for notification.</span></span>

</dd> <dt>

<span data-ttu-id="82c18-148">**QueryLanguage**</span><span class="sxs-lookup"><span data-stu-id="82c18-148">**QueryLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82c18-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="82c18-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82c18-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82c18-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82c18-151">Lenguaje usado para la consulta.</span><span class="sxs-lookup"><span data-stu-id="82c18-151">Language used for the query.</span></span> <span data-ttu-id="82c18-152">Dado que WMI actualmente solo admite lenguaje de consulta de WMI (WQL) como lenguaje de consulta, esta propiedad debe establecerse en "WQL".</span><span class="sxs-lookup"><span data-stu-id="82c18-152">Because WMI currently supports only WMI Query Language (WQL) as a query language, this property must be set to "WQL".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82c18-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82c18-153">Remarks</span></span>

<span data-ttu-id="82c18-154">La clase **\_ \_ EventFilter** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md).</span><span class="sxs-lookup"><span data-stu-id="82c18-154">The **\_\_EventFilter** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md).</span></span>

## <a name="examples"></a><span data-ttu-id="82c18-155">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="82c18-155">Examples</span></span>

<span data-ttu-id="82c18-156">El ejemplo de [creación de registro de eventos de WMI permanente para supervisar archivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) de PowerShell en la galería de TechNet usa **\_ \_ EventFilter** como parte de un script complejo para configurar un registro de eventos de WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="82c18-156">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_EventFilter** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="82c18-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82c18-157">Requirements</span></span>



| <span data-ttu-id="82c18-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="82c18-158">Requirement</span></span> | <span data-ttu-id="82c18-159">Value</span><span class="sxs-lookup"><span data-stu-id="82c18-159">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="82c18-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82c18-160">Minimum supported client</span></span><br/> | <span data-ttu-id="82c18-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82c18-161">Windows Vista</span></span><br/>       |
| <span data-ttu-id="82c18-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82c18-162">Minimum supported server</span></span><br/> | <span data-ttu-id="82c18-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82c18-163">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="82c18-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="82c18-164">Namespace</span></span><br/>                | <span data-ttu-id="82c18-165">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="82c18-165">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="82c18-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="82c18-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82c18-167">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="82c18-167">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="82c18-168">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="82c18-168">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="82c18-169">Crear un filtro de eventos</span><span class="sxs-lookup"><span data-stu-id="82c18-169">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="82c18-170">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="82c18-170">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="82c18-171">Supervisión y respuesta a eventos con consumidores estándar</span><span class="sxs-lookup"><span data-stu-id="82c18-171">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="82c18-172">Supervisión de eventos</span><span class="sxs-lookup"><span data-stu-id="82c18-172">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="82c18-173">Clases de consumidor estándar</span><span class="sxs-lookup"><span data-stu-id="82c18-173">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="82c18-174">Proteger eventos WMI</span><span class="sxs-lookup"><span data-stu-id="82c18-174">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

