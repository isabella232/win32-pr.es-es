---
description: La clase SnmpExtendedNotification es la clase base para cualquier clase asignada de la macro de tipo de notificación a una clase CIM mediante el proveedor SNMP.
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: Clase SnmpExtendedNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: e21fcc32976c42f41cd33a519e5fa6c684acdfc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715750"
---
# <a name="snmpextendednotification-class"></a><span data-ttu-id="59292-103">Clase SnmpExtendedNotification</span><span class="sxs-lookup"><span data-stu-id="59292-103">SnmpExtendedNotification class</span></span>

<span data-ttu-id="59292-104">La clase **SnmpExtendedNotification** es la clase base para cualquier clase asignada de la macro de [tipo de notificación](notification-type-macro.md) a una clase CIM mediante el [proveedor SNMP](snmp-provider.md).</span><span class="sxs-lookup"><span data-stu-id="59292-104">The **SnmpExtendedNotification** class is the base class for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to a CIM class by the [SNMP Provider](snmp-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="59292-105">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="59292-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="59292-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="59292-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="59292-107">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="59292-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="59292-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59292-108">Syntax</span></span>

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
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

## <a name="members"></a><span data-ttu-id="59292-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="59292-109">Members</span></span>

<span data-ttu-id="59292-110">La clase **SnmpExtendedNotification** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="59292-110">The **SnmpExtendedNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="59292-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="59292-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59292-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="59292-112">Properties</span></span>

<span data-ttu-id="59292-113">La clase **SnmpExtendedNotification** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="59292-113">The **SnmpExtendedNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59292-114">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="59292-114">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59292-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59292-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59292-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59292-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59292-117">Dirección de red de la entidad que creó la notificación.</span><span class="sxs-lookup"><span data-stu-id="59292-117">Network address of the entity that created the notification.</span></span> <span data-ttu-id="59292-118">Esta es la dirección real del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59292-118">This is the actual address of the device.</span></span> <span data-ttu-id="59292-119">Cuando la entidad de administración usa SNMP a través de UDP, la dirección de transporte hace referencia a una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="59292-119">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="59292-120">Cuando la entidad de administración utiliza SNMP a través de IPX, la dirección de transporte se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="59292-120">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="59292-121">Esta propiedad solo es válida para SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="59292-121">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="59292-122">**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="59292-122">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59292-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59292-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59292-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59292-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59292-125">Protocolo de transporte utilizado por la entidad emisora.</span><span class="sxs-lookup"><span data-stu-id="59292-125">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="59292-126">Esta propiedad es válida para SNMPv1 y SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="59292-126">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="59292-127">**AgentTransportAddress**</span><span class="sxs-lookup"><span data-stu-id="59292-127">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59292-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59292-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59292-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59292-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59292-130">Dirección de red de la entidad que envió la notificación.</span><span class="sxs-lookup"><span data-stu-id="59292-130">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="59292-131">Esta es la dirección de la última entidad que reenvió la notificación.</span><span class="sxs-lookup"><span data-stu-id="59292-131">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="59292-132">Cuando la entidad de administración usa SNMP a través de UDP, la dirección de transporte hace referencia a una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="59292-132">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="59292-133">Cuando la entidad de administración usa SNMP a través de IPX, la dirección de transporte hace referencia a una dirección IPX.</span><span class="sxs-lookup"><span data-stu-id="59292-133">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="59292-134">Esta propiedad es válida para SNMPv1 y SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="59292-134">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="59292-135">**AgentTransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="59292-135">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59292-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59292-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59292-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59292-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59292-138">Protocolo de transporte utilizado por la entidad emisora.</span><span class="sxs-lookup"><span data-stu-id="59292-138">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="59292-139">**Comunidad**</span><span class="sxs-lookup"><span data-stu-id="59292-139">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59292-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59292-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59292-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59292-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59292-142">Nombre de comunidad asociado a una instancia de la PDU.</span><span class="sxs-lookup"><span data-stu-id="59292-142">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="59292-143">El nombre de comunidad autentica el originador de la PDU.</span><span class="sxs-lookup"><span data-stu-id="59292-143">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="59292-144">Esta propiedad es válida para SNMPv1 y SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="59292-144">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="59292-145">**Identificación**</span><span class="sxs-lookup"><span data-stu-id="59292-145">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59292-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59292-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59292-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59292-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59292-148">Calificadores: **\_ Convención textual** ("OBJECTIDENTIFIER"), **codificación** ("OBJECTIDENTIFIER"), **\_ Sintaxis de objeto** ("OBJECTIDENTIFIER"), **\_ identificador de objeto** ("1.3.6.1.6.3.1.1.4.1")</span><span class="sxs-lookup"><span data-stu-id="59292-148">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="59292-149">Identificación autoritativa de esta notificación.</span><span class="sxs-lookup"><span data-stu-id="59292-149">Authoritative identification of this notification.</span></span> <span data-ttu-id="59292-150">Se asigna directamente a la entrada MIB SnmpTrapOID de variables de enlace.</span><span class="sxs-lookup"><span data-stu-id="59292-150">Maps directly to the MIB entry SnmpTrapOID variable binding.</span></span> <span data-ttu-id="59292-151">Esta propiedad solo es válida para SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="59292-151">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="59292-152">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="59292-152">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59292-153">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="59292-153">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="59292-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59292-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59292-155">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="59292-155">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="59292-156">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="59292-156">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="59292-157">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="59292-157">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="59292-158">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="59292-158">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59292-159">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59292-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59292-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59292-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59292-161">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="59292-161">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="59292-162">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="59292-162">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="59292-163">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="59292-163">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="59292-164">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="59292-164">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="59292-165">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="59292-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="59292-166">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="59292-166">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59292-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59292-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59292-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59292-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59292-169">Calificadores: **\_ Convención textual** ("TimeTicks"), **codificación** ("TimeTicks"), **\_ Sintaxis de objeto** ("TimeTicks"), **\_ identificador de objeto** ("1.3.6.1.2.1.1.3")</span><span class="sxs-lookup"><span data-stu-id="59292-169">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="59292-170">Tiempo en centésimas de segundo desde la última vez que se reinicializó la parte de administración de red del agente.</span><span class="sxs-lookup"><span data-stu-id="59292-170">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="59292-171">Esto se asigna a la variable MIB sysUptime. 0, que es de tipo **INTEGER32**.</span><span class="sxs-lookup"><span data-stu-id="59292-171">This maps to the MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="59292-172">Esta propiedad se asigna a la **marca** de tiempo de la propiedad de clase CIM, que es de tipo **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="59292-172">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="59292-173">Esta propiedad solo es válida para SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="59292-173">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59292-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59292-174">Remarks</span></span>

<span data-ttu-id="59292-175">Una macro [de tipo de notificación](notification-type-macro.md) que contiene referencias a una macro [de tipo de objeto](object-type-macro.md) denominada **marca** de tiempo o **identificación** produce un conflicto de asignación.</span><span class="sxs-lookup"><span data-stu-id="59292-175">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="59292-176">Si se produce este conflicto, las propiedades necesarias tienen prioridad y se debe cambiar el nombre de las referencias en conflicto.</span><span class="sxs-lookup"><span data-stu-id="59292-176">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="59292-177">Una macro [de tipo de notificación](notification-type-macro.md) que contiene referencias a una macro [de tipo de objeto](object-type-macro.md) denominada **Community** produce un conflicto de asignación.</span><span class="sxs-lookup"><span data-stu-id="59292-177">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="59292-178">Si se produce este conflicto, las propiedades necesarias tienen prioridad y se debe cambiar el nombre de las referencias en conflicto.</span><span class="sxs-lookup"><span data-stu-id="59292-178">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="59292-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59292-179">Requirements</span></span>



| <span data-ttu-id="59292-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="59292-180">Requirement</span></span> | <span data-ttu-id="59292-181">Value</span><span class="sxs-lookup"><span data-stu-id="59292-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59292-182">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59292-182">Minimum supported client</span></span><br/> | <span data-ttu-id="59292-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59292-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59292-184">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59292-184">Minimum supported server</span></span><br/> | <span data-ttu-id="59292-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59292-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59292-186">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="59292-186">Namespace</span></span><br/>                | <span data-ttu-id="59292-187">\\Smir SNMP \\ raíz</span><span class="sxs-lookup"><span data-stu-id="59292-187">Root\\snmp\\SMIR</span></span><br/>                                                             |
| <span data-ttu-id="59292-188">MOF</span><span class="sxs-lookup"><span data-stu-id="59292-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59292-189"><dt>SnmpSmiR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59292-189"><dt>SnmpSmiR.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59292-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="59292-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59292-191">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="59292-191">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="59292-192">NOTIFICATION-TYPE (macro)</span><span class="sxs-lookup"><span data-stu-id="59292-192">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

