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
ms.openlocfilehash: be0847c7a7d96fb7491274350c828d0cc319240823fa006e972bb295ad477773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860365"
---
# <a name="snmpnotification-class"></a>Clase SnmpNotification

La **clase SnmpNotification** se asigna desde la macro [NOTIFICATION-TYPE](notification-type-macro.md) a una clase CIM encapsulada. Es una clase base utilizada por el proveedor [SNMP](snmp-provider.md) para cualquier clase asignada desde la macro [NOTIFICATION-TYPE](notification-type-macro.md) a una clase CIM encapsulada por el proveedor SNMP.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

La **clase SnmpNotification** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SnmpNotification** tiene estas propiedades.

<dl> <dt>

**AgentAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección de red de la entidad que creó la notificación. Esta es la dirección real del dispositivo. Cuando la entidad de administración usa SNMP sobre UDP, la dirección de transporte hace referencia a una dirección IP. Cuando la entidad de administración usa SNMP sobre IPX, la dirección de transporte se establece en **NULL.** Esta propiedad solo es válida para SNMPv1.

</dd> <dt>

**AgentTransport**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Protocolo de transporte utilizado por la entidad de envío. Esta propiedad es válida para SNMPv1 y SNMPv2C.

</dd> <dt>

**AgentTransportAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección de red de la entidad que envió la notificación. Esta es la dirección de la última entidad que reenvía la notificación. Cuando la entidad de administración usa SNMP sobre UDP, la dirección de transporte hace referencia a una dirección IP. Cuando la entidad de administración usa SNMP sobre IPX, la dirección de transporte hace referencia a una dirección IPX. Esta propiedad es válida para SNMPv1 y SNMPv2C.

</dd> <dt>

**AgentTransportProtocol**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Protocolo de transporte utilizado por la entidad de envío.

</dd> <dt>

**Comunidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Community nombre asociado a una instancia de la PDU. El nombre de la comunidad autentica el originador de la PDU. Esta propiedad es válida para SNMPv1 y SNMPv2C.

</dd> <dt>

**Identificación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: convención textual ("OBJECTIDENTIFIER"),  codificación ("OBJECTIDENTIFIER"), sintaxis de objeto ("OBJECTIDENTIFIER"), identificador de objeto ("1.3.6.1.6.3.1.1.4.1") **\_** **\_** **\_**
</dt> </dl>

Identificación autoritativa de esta notificación. Mapas directamente al enlace de variable SnmpTrapOID. Esta propiedad solo es válida para SNMPv2C.

</dd> <dt>

**\_DESCRIPTOR DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md). Para obtener más información sobre las constantes usadas para establecer este descriptor de seguridad, vea [Constantes de seguridad WMI](wmi-security-constants.md).

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: convención textual ("TimeTicks"),  codificación ("TimeTicks"), sintaxis de objeto ("TimeTicks"), identificador de objeto ("1.3.6.1.2.1.1.3") **\_** **\_** **\_**
</dt> </dl>

Tiempo en centésimas de segundo desde que se inicializó por última vez la parte de administración de red del agente. Variable de MIB sysUptime.0, que es de tipo **INTEGER32.** Esta propiedad se asigna a la propiedad de clase CIM **TimeStamp**, que es de tipo **uint32**. Esta propiedad solo es válida para SNMPv2C.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una [macro NOTIFICATION-TYPE que](notification-type-macro.md) contiene referencias a una macro [OBJECT-TYPE](object-type-macro.md) denominada **TimeStamp** o **Identification** provoca un conflicto de asignación. Si se produce este conflicto, las propiedades necesarias tienen prioridad y se debe cambiar el nombre de las referencias en conflicto.

Una [macro NOTIFICATION-TYPE que](notification-type-macro.md) contiene referencias a una macro [OBJECT-TYPE](object-type-macro.md) denominada **Community** un conflicto de asignación. Si se produce este conflicto, las propiedades necesarias tienen prioridad y se debe cambiar el nombre de las referencias en conflicto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>   |
| Espacio de nombres<br/>                | Host \\ local de snmp \\ raíz<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[NOTIFICATION-TYPE (Macro)](notification-type-macro.md)
</dt> </dl>

 

