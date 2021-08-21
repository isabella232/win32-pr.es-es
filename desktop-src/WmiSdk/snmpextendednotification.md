---
description: La clase SnmpExtendedNotification es la clase base de cualquier clase asignada desde la macro NOTIFICATION-TYPE a una clase CIM por el proveedor SNMP.
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: SnmpExtendedNotification (clase)
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
ms.openlocfilehash: d8da8533e9ac5c86dfa3291092fb5165b94e2e393e507c55f15b64c1e30cd6a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816545"
---
# <a name="snmpextendednotification-class"></a>SnmpExtendedNotification (clase)

La **clase SnmpExtendedNotification** es la clase base de cualquier clase asignada desde la macro [NOTIFICATION-TYPE](notification-type-macro.md) a una clase CIM por el [proveedor SNMP](snmp-provider.md).

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configurar el entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

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

La **clase SnmpExtendedNotification** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SnmpExtendedNotification** tiene estas propiedades.

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

Identificación autoritativa de esta notificación. Mapas directamente a la entrada de MIB Enlace de variable SnmpTrapOID. Esta propiedad solo es válida para SNMPv2C.

</dd> <dt>

**DESCRIPTOR \_ DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md). Para obtener más información sobre las constantes usadas para establecer este descriptor de seguridad, vea [Constantes de seguridad wmi](wmi-security-constants.md).

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: convención textual ("TimeTicks"),  codificación ("TimeTicks"), sintaxis de objeto ("TimeTicks"), identificador de objeto ("1.3.6.1.2.1.1.3") **\_** **\_** **\_**
</dt> </dl>

Tiempo en centésimas de segundo desde que se inicializó por última vez la parte de administración de red del agente. Esto se asigna a la variable de MIB sysUptime.0, que es de tipo **INTEGER32.** Esta propiedad se asigna a la propiedad de clase CIM **TimeStamp**, que es de tipo **uint32**. Esta propiedad solo es válida para SNMPv2C.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una [macro NOTIFICATION-TYPE que](notification-type-macro.md) contiene referencias a una macro [OBJECT-TYPE](object-type-macro.md) denominada **TimeStamp** o **Identification** provoca un conflicto de asignación. Si se produce este conflicto, las propiedades necesarias tienen prioridad y se debe cambiar el nombre de las referencias en conflicto.

Una [macro NOTIFICATION-TYPE que](notification-type-macro.md) contiene referencias a una macro [OBJECT-TYPE](object-type-macro.md) denominada **Community** provoca un conflicto de asignación. Si se produce este conflicto, las propiedades necesarias tienen prioridad y se debe cambiar el nombre de las referencias en conflicto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | SMIR \\ de Snmp \\ raíz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>SnmpSmiR.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[NOTIFICATION-TYPE Macro](notification-type-macro.md)
</dt> </dl>

 

