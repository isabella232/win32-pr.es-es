---
description: Se utiliza en el registro de los consumidores de eventos permanentes para relacionar una instancia de \_ \_ EventConsumer con una instancia de \_ \_ EventFilter.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: __FilterToConsumerBinding (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
- All
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
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716872"
---
# <a name="__filtertoconsumerbinding-class"></a><span data-ttu-id="51363-103">\_\_Clase FilterToConsumerBinding</span><span class="sxs-lookup"><span data-stu-id="51363-103">\_\_FilterToConsumerBinding class</span></span>

<span data-ttu-id="51363-104">La clase del sistema **\_ \_ FilterToConsumerBinding** se usa en el registro de los consumidores de eventos permanentes para relacionar una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) con una instancia de [**\_ \_ EventFilter**](--eventfilter.md).**\_ \_ FilterToConsumerBinding** es una clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="51363-104">The **\_\_FilterToConsumerBinding** system class is used in the registration of permanent event consumers to relate an instance of the [**\_\_EventConsumer**](--eventconsumer.md) to an instance of [**\_\_EventFilter**](--eventfilter.md).**\_\_FilterToConsumerBinding** is an association class.</span></span>

<span data-ttu-id="51363-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="51363-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="51363-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="51363-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="51363-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51363-107">Syntax</span></span>

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a><span data-ttu-id="51363-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="51363-108">Members</span></span>

<span data-ttu-id="51363-109">La clase **\_ \_ FilterToConsumerBinding** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="51363-109">The **\_\_FilterToConsumerBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="51363-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51363-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51363-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51363-111">Properties</span></span>

<span data-ttu-id="51363-112">La clase **\_ \_ FilterToConsumerBinding** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="51363-112">The **\_\_FilterToConsumerBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51363-113">**Consumidor**</span><span class="sxs-lookup"><span data-stu-id="51363-113">**Consumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51363-114">Tipo de datos: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="51363-114">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="51363-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51363-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="51363-116">Calificadores: [ **clave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="51363-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="51363-117">Referencia a una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) que representa la ruta de acceso del objeto a un consumidor lógico, el destinatario de un evento.</span><span class="sxs-lookup"><span data-stu-id="51363-117">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the object path to a logical consumer, the recipient of an event.</span></span> <span data-ttu-id="51363-118">Un consumidor lógico es una instancia de una clase derivada de **\_ \_ EventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="51363-118">A logical consumer is an instance of a class derived from **\_\_EventConsumer**.</span></span>

</dd> <dt>

<span data-ttu-id="51363-119">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="51363-119">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51363-120">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="51363-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="51363-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51363-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="51363-122">Identificador de seguridad (SID) que identifica de forma única al usuario que creó el enlace.</span><span class="sxs-lookup"><span data-stu-id="51363-122">Security identifier (SID) that uniquely identifies the user who created the binding.</span></span> <span data-ttu-id="51363-123">En función del sistema operativo, WMI almacena el SID de administrador o el SID del usuario que crea una instancia de **\_ \_ FilterToConsumerBinding**.</span><span class="sxs-lookup"><span data-stu-id="51363-123">Depending on the operating system, WMI stores the Administrator SID or the SID of the user that creates an instance of **\_\_FilterToConsumerBinding**.</span></span> <span data-ttu-id="51363-124">Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="51363-124">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="51363-125">**DeliverSynchronously**</span><span class="sxs-lookup"><span data-stu-id="51363-125">**DeliverSynchronously**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51363-126">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="51363-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51363-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51363-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="51363-128">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="51363-128">Obsolete.</span></span> <span data-ttu-id="51363-129">En su lugar, use la propiedad **DeliveryQoS** en lugar de esta propiedad, porque si **DeliverSynchronously** está establecido en **true** , invalida el valor de la propiedad **DeliveryQoS** .</span><span class="sxs-lookup"><span data-stu-id="51363-129">Instead use the **DeliveryQoS** property in place of this property, because if **DeliverSynchronously** is set to **True** it overrides the setting of the **DeliveryQoS** property.</span></span>

</dd> <dt>

<span data-ttu-id="51363-130">**DeliveryQoS**</span><span class="sxs-lookup"><span data-stu-id="51363-130">**DeliveryQoS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51363-131">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51363-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51363-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51363-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="51363-133">Calidad de servicio de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="51363-133">Quality of service for a subscription.</span></span> <span data-ttu-id="51363-134">Si la propiedad **DeliverSynchronously** está establecida en **true**, invalida el valor de la propiedad **DeliveryQoS** .</span><span class="sxs-lookup"><span data-stu-id="51363-134">If the **DeliverSynchronously** property is set to **True**, it overrides the setting of the **DeliveryQoS** property.</span></span>

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span data-ttu-id="51363-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG \_ MARCAR \_ QoS \_ sincrónico** (0)</span><span class="sxs-lookup"><span data-stu-id="51363-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG\_FLAG\_QOS\_SYNCHRONOUS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="51363-136">Entrega sincrónica</span><span class="sxs-lookup"><span data-stu-id="51363-136">Synchronous delivery</span></span>

<span data-ttu-id="51363-137">**False**.</span><span class="sxs-lookup"><span data-stu-id="51363-137">**False**.</span></span> <span data-ttu-id="51363-138">El evento se entrega al consumidor lógico sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="51363-138">The event is delivered to the logical consumer synchronously.</span></span>

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span data-ttu-id="51363-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG \_ MARCAR \_ QoS \_ Express** (1)</span><span class="sxs-lookup"><span data-stu-id="51363-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG\_FLAG\_QOS\_EXPRESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="51363-140">Entrega rápida</span><span class="sxs-lookup"><span data-stu-id="51363-140">Express delivery</span></span>

<span data-ttu-id="51363-141">**True**.</span><span class="sxs-lookup"><span data-stu-id="51363-141">**True**.</span></span> <span data-ttu-id="51363-142">El evento se entrega al consumidor lógico de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="51363-142">The event is delivered to the logical consumer asynchronously.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51363-143">**Filter**</span><span class="sxs-lookup"><span data-stu-id="51363-143">**Filter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51363-144">Tipo de datos: **\_ \_ EventFilter**</span><span class="sxs-lookup"><span data-stu-id="51363-144">Data type: **\_\_EventFilter**</span></span>
</dt> <dt>

<span data-ttu-id="51363-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51363-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="51363-146">Calificadores: [ **clave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="51363-146">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="51363-147">Referencia a una instancia de [**\_ \_ EventFilter**](--eventfilter.md) que representa la ruta de acceso del objeto a un filtro de eventos que es una consulta que especifica el tipo de evento que se va a recibir.</span><span class="sxs-lookup"><span data-stu-id="51363-147">Reference to an instance of [**\_\_EventFilter**](--eventfilter.md) that represents the object path to an event filter which is a query that specifies the type of event to be received.</span></span>

</dd> <dt>

<span data-ttu-id="51363-148">**MaintainSecurityContext**</span><span class="sxs-lookup"><span data-stu-id="51363-148">**MaintainSecurityContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51363-149">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="51363-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51363-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51363-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="51363-151">Si **es true**, los eventos se entregan en el mismo contexto de seguridad en el que se encontraban en el momento en que se proporcionaron.</span><span class="sxs-lookup"><span data-stu-id="51363-151">If **True**, the events are delivered in the same security context that the provider was in when it provided them.</span></span>

> [!Note]  
> <span data-ttu-id="51363-152">Solo un consumidor implementado como un archivo DLL (un consumidor en proceso) puede recibir eventos en el contexto de seguridad del proveedor.</span><span class="sxs-lookup"><span data-stu-id="51363-152">Only a consumer implemented as a DLL (an in-process consumer) can receive events in the security context of the provider.</span></span> <span data-ttu-id="51363-153">Para obtener más información sobre los proveedores y la seguridad en proceso, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="51363-153">For more information about in-process providers and security, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="51363-154">Para obtener más información y ejemplos, vea reemplazar:[recibir eventos de forma segura](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="51363-154">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

 

</dd> <dt>

<span data-ttu-id="51363-155">**SlowDownProviders**</span><span class="sxs-lookup"><span data-stu-id="51363-155">**SlowDownProviders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51363-156">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="51363-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51363-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51363-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="51363-158">Si **es true**, los proveedores se ralentizan si este consumidor no puede continuar.</span><span class="sxs-lookup"><span data-stu-id="51363-158">If **True**, providers are slowed down if this consumer cannot keep up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51363-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51363-159">Remarks</span></span>

<span data-ttu-id="51363-160">La clase **\_ \_ FilterToConsumerBinding** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md), que no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="51363-160">The **\_\_FilterToConsumerBinding** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="51363-161">Los consumidores de eventos permanentes usan la clase del sistema **\_ \_ FilterToConsumerBinding** para enlazar filtros de eventos a los consumidores finales.</span><span class="sxs-lookup"><span data-stu-id="51363-161">Permanent event consumers use the **\_\_FilterToConsumerBinding** system class to bind event filters to final consumers.</span></span> <span data-ttu-id="51363-162">Una vez enlazados el filtro y el consumidor, WMI puede reenviar los eventos que coinciden con el filtro al consumidor correspondiente.</span><span class="sxs-lookup"><span data-stu-id="51363-162">After the filter and consumer are bound together, WMI can forward events that match the filter to the corresponding consumer.</span></span>

## <a name="examples"></a><span data-ttu-id="51363-163">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="51363-163">Examples</span></span>

<span data-ttu-id="51363-164">El ejemplo de [creación de registro de eventos de WMI permanente para supervisar archivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) de PowerShell en la galería de TechNet usa **\_ \_ FilterToConsumerBinding** como parte de un script complejo para configurar un registro de eventos de WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="51363-164">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_FilterToConsumerBinding** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="51363-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51363-165">Requirements</span></span>



| <span data-ttu-id="51363-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="51363-166">Requirement</span></span> | <span data-ttu-id="51363-167">Value</span><span class="sxs-lookup"><span data-stu-id="51363-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="51363-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51363-168">Minimum supported client</span></span><br/> | <span data-ttu-id="51363-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51363-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="51363-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51363-170">Minimum supported server</span></span><br/> | <span data-ttu-id="51363-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51363-171">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="51363-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="51363-172">Namespace</span></span><br/>                | <span data-ttu-id="51363-173">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="51363-173">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="51363-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="51363-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51363-175">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="51363-175">**\_\_IndicationRelated**</span></span>](--indicationrelated.md)
</dt> <dt>

[<span data-ttu-id="51363-176">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="51363-176">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="51363-177">Supervisión y respuesta a eventos con consumidores estándar</span><span class="sxs-lookup"><span data-stu-id="51363-177">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="51363-178">Supervisión de eventos</span><span class="sxs-lookup"><span data-stu-id="51363-178">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="51363-179">Crear un filtro de eventos</span><span class="sxs-lookup"><span data-stu-id="51363-179">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="51363-180">Proteger eventos WMI</span><span class="sxs-lookup"><span data-stu-id="51363-180">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




