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
# <a name="snmpextendednotification-class"></a>Clase SnmpExtendedNotification

La clase **SnmpExtendedNotification** es la clase base para cualquier clase asignada de la macro de [tipo de notificación](notification-type-macro.md) a una clase CIM mediante el [proveedor SNMP](snmp-provider.md).

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

La clase **SnmpExtendedNotification** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **SnmpExtendedNotification** tiene estas propiedades.

<dl> <dt>

**AgentAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección de red de la entidad que creó la notificación. Esta es la dirección real del dispositivo. Cuando la entidad de administración usa SNMP a través de UDP, la dirección de transporte hace referencia a una dirección IP. Cuando la entidad de administración utiliza SNMP a través de IPX, la dirección de transporte se establece en **null**. Esta propiedad solo es válida para SNMPv1.

</dd> <dt>

**AgentTransport**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Protocolo de transporte utilizado por la entidad emisora. Esta propiedad es válida para SNMPv1 y SNMPv2C.

</dd> <dt>

**AgentTransportAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección de red de la entidad que envió la notificación. Esta es la dirección de la última entidad que reenvió la notificación. Cuando la entidad de administración usa SNMP a través de UDP, la dirección de transporte hace referencia a una dirección IP. Cuando la entidad de administración usa SNMP a través de IPX, la dirección de transporte hace referencia a una dirección IPX. Esta propiedad es válida para SNMPv1 y SNMPv2C.

</dd> <dt>

**AgentTransportProtocol**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Protocolo de transporte utilizado por la entidad emisora.

</dd> <dt>

**Comunidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de comunidad asociado a una instancia de la PDU. El nombre de comunidad autentica el originador de la PDU. Esta propiedad es válida para SNMPv1 y SNMPv2C.

</dd> <dt>

**Identificación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **\_ Convención textual** ("OBJECTIDENTIFIER"), **codificación** ("OBJECTIDENTIFIER"), **\_ Sintaxis de objeto** ("OBJECTIDENTIFIER"), **\_ identificador de objeto** ("1.3.6.1.6.3.1.1.4.1")
</dt> </dl>

Identificación autoritativa de esta notificación. Se asigna directamente a la entrada MIB SnmpTrapOID de variables de enlace. Esta propiedad solo es válida para SNMPv2C.

</dd> <dt>

**descriptor de seguridad \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md). Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](wmi-security-constants.md).

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601. La información está en el formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Indicaciones**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **\_ Convención textual** ("TimeTicks"), **codificación** ("TimeTicks"), **\_ Sintaxis de objeto** ("TimeTicks"), **\_ identificador de objeto** ("1.3.6.1.2.1.1.3")
</dt> </dl>

Tiempo en centésimas de segundo desde la última vez que se reinicializó la parte de administración de red del agente. Esto se asigna a la variable MIB sysUptime. 0, que es de tipo **INTEGER32**. Esta propiedad se asigna a la **marca** de tiempo de la propiedad de clase CIM, que es de tipo **UInt32**. Esta propiedad solo es válida para SNMPv2C.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una macro [de tipo de notificación](notification-type-macro.md) que contiene referencias a una macro [de tipo de objeto](object-type-macro.md) denominada **marca** de tiempo o **identificación** produce un conflicto de asignación. Si se produce este conflicto, las propiedades necesarias tienen prioridad y se debe cambiar el nombre de las referencias en conflicto.

Una macro [de tipo de notificación](notification-type-macro.md) que contiene referencias a una macro [de tipo de objeto](object-type-macro.md) denominada **Community** produce un conflicto de asignación. Si se produce este conflicto, las propiedades necesarias tienen prioridad y se debe cambiar el nombre de las referencias en conflicto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\Smir SNMP \\ raíz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>SnmpSmiR. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[NOTIFICATION-TYPE (macro)](notification-type-macro.md)
</dt> </dl>

 

