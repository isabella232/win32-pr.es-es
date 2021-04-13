---
description: La clase SnmpNotification se asigna desde la macro NOTIFICATION-TYPE a una clase CIM encapsulada.
ms.assetid: b90d8bab-7cae-4dbe-9f6e-daba4e68a10a
ms.tgt_platform: multiple
title: Clase SnmpNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpNotification
- Root\snmp\localhost.SnmpNotification.SECURITY_DESCRIPTOR
- Root\snmp\localhost.SnmpNotification.TIME_CREATED
- Root\snmp\localhost.SnmpNotification.AgentAddress
- Root\snmp\localhost.SnmpNotification.AgentTransport
- Root\snmp\localhost.SnmpNotification.AgentTransportAddress
- Root\snmp\localhost.SnmpNotification.Community
- Root\snmp\localhost.SnmpNotification.Identification
- Root\snmp\localhost.SnmpNotification.TimeStamp
- Root\snmp\localhost.SnmpNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\localhost
ms.openlocfilehash: 89b50d04b435f862a329953f14b47646937a1d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546971"
---
# <a name="snmpnotification-class"></a><span data-ttu-id="14ef8-103">Clase SnmpNotification</span><span class="sxs-lookup"><span data-stu-id="14ef8-103">SnmpNotification class</span></span>

<span data-ttu-id="14ef8-104">La clase **SnmpNotification** se asigna desde la macro [Notification-Type](notification-type-macro.md) a una clase CIM encapsulada.</span><span class="sxs-lookup"><span data-stu-id="14ef8-104">The **SnmpNotification** class maps from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class.</span></span> <span data-ttu-id="14ef8-105">Es una clase base utilizada por el [proveedor SNMP](snmp-provider.md) para cualquier clase asignada de la macro [de tipo notificación](notification-type-macro.md) a una clase CIM encapsulada por el proveedor SNMP.</span><span class="sxs-lookup"><span data-stu-id="14ef8-105">It is a base class used by the [SNMP Provider](snmp-provider.md) for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class by the SNMP Provider.</span></span>

> [!Note]  
> <span data-ttu-id="14ef8-106">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="14ef8-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="14ef8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14ef8-107">Syntax</span></span>

``` syntax
class SnmpNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="14ef8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="14ef8-108">Members</span></span>

<span data-ttu-id="14ef8-109">La clase **SnmpNotification** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="14ef8-109">The **SnmpNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="14ef8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14ef8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14ef8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14ef8-111">Properties</span></span>

<span data-ttu-id="14ef8-112">La clase **SnmpNotification** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="14ef8-112">The **SnmpNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14ef8-113">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="14ef8-113">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ef8-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14ef8-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14ef8-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14ef8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14ef8-116">Dirección de red de la entidad que creó la notificación.</span><span class="sxs-lookup"><span data-stu-id="14ef8-116">Network address of the entity that created the notification.</span></span> <span data-ttu-id="14ef8-117">Esta es la dirección real del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14ef8-117">This is the actual address of the device.</span></span> <span data-ttu-id="14ef8-118">Cuando la entidad de administración usa SNMP a través de UDP, la dirección de transporte hace referencia a una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="14ef8-118">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="14ef8-119">Cuando la entidad de administración utiliza SNMP a través de IPX, la dirección de transporte se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="14ef8-119">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="14ef8-120">Esta propiedad solo es válida para SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="14ef8-120">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="14ef8-121">**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="14ef8-121">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ef8-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14ef8-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14ef8-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14ef8-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14ef8-124">Protocolo de transporte utilizado por la entidad emisora.</span><span class="sxs-lookup"><span data-stu-id="14ef8-124">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="14ef8-125">Esta propiedad es válida para SNMPv1 y SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="14ef8-125">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="14ef8-126">**AgentTransportAddress**</span><span class="sxs-lookup"><span data-stu-id="14ef8-126">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ef8-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14ef8-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14ef8-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14ef8-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14ef8-129">Dirección de red de la entidad que envió la notificación.</span><span class="sxs-lookup"><span data-stu-id="14ef8-129">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="14ef8-130">Esta es la dirección de la última entidad que reenvió la notificación.</span><span class="sxs-lookup"><span data-stu-id="14ef8-130">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="14ef8-131">Cuando la entidad de administración usa SNMP a través de UDP, la dirección de transporte hace referencia a una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="14ef8-131">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="14ef8-132">Cuando la entidad de administración usa SNMP a través de IPX, la dirección de transporte hace referencia a una dirección IPX.</span><span class="sxs-lookup"><span data-stu-id="14ef8-132">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="14ef8-133">Esta propiedad es válida para SNMPv1 y SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="14ef8-133">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="14ef8-134">**AgentTransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="14ef8-134">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ef8-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14ef8-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14ef8-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14ef8-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14ef8-137">Protocolo de transporte utilizado por la entidad emisora.</span><span class="sxs-lookup"><span data-stu-id="14ef8-137">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="14ef8-138">**Comunidad**</span><span class="sxs-lookup"><span data-stu-id="14ef8-138">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ef8-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14ef8-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14ef8-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14ef8-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14ef8-141">Nombre de comunidad asociado a una instancia de la PDU.</span><span class="sxs-lookup"><span data-stu-id="14ef8-141">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="14ef8-142">El nombre de comunidad autentica el originador de la PDU.</span><span class="sxs-lookup"><span data-stu-id="14ef8-142">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="14ef8-143">Esta propiedad es válida para SNMPv1 y SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="14ef8-143">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="14ef8-144">**Identificación**</span><span class="sxs-lookup"><span data-stu-id="14ef8-144">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ef8-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14ef8-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14ef8-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14ef8-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14ef8-147">Calificadores: **\_ Convención textual** ("OBJECTIDENTIFIER"), **codificación** ("OBJECTIDENTIFIER"), **\_ Sintaxis de objeto** ("OBJECTIDENTIFIER"), **\_ identificador de objeto** ("1.3.6.1.6.3.1.1.4.1")</span><span class="sxs-lookup"><span data-stu-id="14ef8-147">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="14ef8-148">Identificación autoritativa de esta notificación.</span><span class="sxs-lookup"><span data-stu-id="14ef8-148">Authoritative identification of this notification.</span></span> <span data-ttu-id="14ef8-149">Se asigna directamente al enlace de la variable SnmpTrapOID.</span><span class="sxs-lookup"><span data-stu-id="14ef8-149">Maps directly to the SnmpTrapOID variable binding.</span></span> <span data-ttu-id="14ef8-150">Esta propiedad solo es válida para SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="14ef8-150">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="14ef8-151">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="14ef8-151">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ef8-152">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="14ef8-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="14ef8-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14ef8-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14ef8-154">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="14ef8-154">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="14ef8-155">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="14ef8-155">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="14ef8-156">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="14ef8-156">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="14ef8-157">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="14ef8-157">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ef8-158">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="14ef8-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="14ef8-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14ef8-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14ef8-160">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="14ef8-160">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="14ef8-161">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="14ef8-161">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="14ef8-162">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="14ef8-162">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="14ef8-163">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="14ef8-163">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="14ef8-164">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="14ef8-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="14ef8-165">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="14ef8-165">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ef8-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14ef8-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14ef8-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14ef8-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14ef8-168">Calificadores: **\_ Convención textual** ("TimeTicks"), **codificación** ("TimeTicks"), **\_ Sintaxis de objeto** ("TimeTicks"), **\_ identificador de objeto** ("1.3.6.1.2.1.1.3")</span><span class="sxs-lookup"><span data-stu-id="14ef8-168">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="14ef8-169">Tiempo en centésimas de segundo desde la última vez que se reinicializó la parte de administración de red del agente.</span><span class="sxs-lookup"><span data-stu-id="14ef8-169">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="14ef8-170">Variable MIB sysUptime. 0, que es de tipo **INTEGER32**.</span><span class="sxs-lookup"><span data-stu-id="14ef8-170">MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="14ef8-171">Esta propiedad se asigna a la **marca** de tiempo de la propiedad de clase CIM, que es de tipo **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="14ef8-171">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="14ef8-172">Esta propiedad solo es válida para SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="14ef8-172">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14ef8-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14ef8-173">Remarks</span></span>

<span data-ttu-id="14ef8-174">Una macro [de tipo de notificación](notification-type-macro.md) que contiene referencias a una macro [de tipo de objeto](object-type-macro.md) denominada **marca** de tiempo o **identificación** produce un conflicto de asignación.</span><span class="sxs-lookup"><span data-stu-id="14ef8-174">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="14ef8-175">Si se produce este conflicto, las propiedades necesarias tienen prioridad y se debe cambiar el nombre de las referencias en conflicto.</span><span class="sxs-lookup"><span data-stu-id="14ef8-175">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="14ef8-176">Una macro [de tipo de notificación](notification-type-macro.md) que contiene referencias a una macro [de tipo de objeto](object-type-macro.md) denominada **Community** produce un conflicto de asignación.</span><span class="sxs-lookup"><span data-stu-id="14ef8-176">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="14ef8-177">Si se produce este conflicto, las propiedades necesarias tienen prioridad y se debe cambiar el nombre de las referencias en conflicto.</span><span class="sxs-lookup"><span data-stu-id="14ef8-177">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="14ef8-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14ef8-178">Requirements</span></span>



| <span data-ttu-id="14ef8-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="14ef8-179">Requirement</span></span> | <span data-ttu-id="14ef8-180">Value</span><span class="sxs-lookup"><span data-stu-id="14ef8-180">Value</span></span> |
|-------------------------------------|----------------------------------|
| <span data-ttu-id="14ef8-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14ef8-181">Minimum supported client</span></span><br/> | <span data-ttu-id="14ef8-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14ef8-182">Windows Vista</span></span><br/>         |
| <span data-ttu-id="14ef8-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14ef8-183">Minimum supported server</span></span><br/> | <span data-ttu-id="14ef8-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14ef8-184">Windows Server 2008</span></span><br/>   |
| <span data-ttu-id="14ef8-185">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="14ef8-185">Namespace</span></span><br/>                | <span data-ttu-id="14ef8-186">\\Localhost de SNMP raíz \\</span><span class="sxs-lookup"><span data-stu-id="14ef8-186">Root\\snmp\\localhost</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14ef8-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="14ef8-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ef8-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="14ef8-188">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="14ef8-189">NOTIFICATION-TYPE (macro)</span><span class="sxs-lookup"><span data-stu-id="14ef8-189">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

