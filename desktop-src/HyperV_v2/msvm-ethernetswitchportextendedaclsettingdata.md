---
description: Representa la configuración de ACL de puerto extendido.
ms.assetid: 357dd891-6692-4ffc-b8a8-4ece40d4af28
title: Msvm_EthernetSwitchPortExtendedAclSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortExtendedAclSettingData
- Msvm_EthernetSwitchPortExtendedAclSettingData.Name
- Msvm_EthernetSwitchPortExtendedAclSettingData.Direction
- Msvm_EthernetSwitchPortExtendedAclSettingData.Action
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemoteIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalPort
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemotePort
- Msvm_EthernetSwitchPortExtendedAclSettingData.Protocol
- Msvm_EthernetSwitchPortExtendedAclSettingData.Weight
- Msvm_EthernetSwitchPortExtendedAclSettingData.Stateful
- Msvm_EthernetSwitchPortExtendedAclSettingData.IdleSessionTimeout
- Msvm_EthernetSwitchPortExtendedAclSettingData.IsolationID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27f94de089df73c246de887268d34c187bef2507391ceeb33dd7c8cc8068bc43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148324"
---
# <a name="msvm_ethernetswitchportextendedaclsettingdata-class"></a>Clase Msvm \_ EthernetSwitchPortExtendedAclSettingData

Representa la configuración de ACL de puerto extendido.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, UUID("CD168FF0-A16D-4514-B7B5-8BBBA791A928"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Extended ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortExtendedAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  Name = "";
  uint8   Direction = 0;
  uint8   Action = 0;
  string  LocalIPAddress = "ANY";
  string  RemoteIPAddress = "ANY";
  string  LocalPort = "ANY";
  string  RemotePort = "ANY";
  string  Protocol = "ANY";
  Uint16  Weight = 0;
  Boolean Stateful = FALSE;
  Uint16  IdleSessionTimeout = 255;
  Uint32  IsolationID = 0;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ EthernetSwitchPortExtendedAclSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ EthernetSwitchPortExtendedAclSettingData** tiene estas propiedades.

<dl> <dt>

**Acción**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Acción de la ACL extendida.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

**Permitir** (1)


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

**Denegar** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica si la ACL extendida se aplica a la dirección entrante o saliente.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

**Entrante** (1)


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

**Saliente** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IdleSessionTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Valor de tiempo de espera de sesión inactiva (en segundos) para la ACL con estado.

</dd> <dt>

**IsolationID**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)
</dt> </dl>

Id. de aislamiento para el que se debe aplicar la ACL extendida.

</dd> <dt>

**LocalIPAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Dirección IP local.

</dd> <dt>

**LocalPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Intervalo de puertos local.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Nombre descriptivo de la ACL extendida.

</dd> <dt>

**Protocolo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Cadena de protocolo.

</dd> <dt>

**RemoteIPAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Dirección IP remota.

</dd> <dt>

**RemotePort**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Intervalo de puertos remotos.

</dd> <dt>

**Con estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica si la ACL extendida tiene estado o no tiene estado.

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Peso aplicado a la ACL extendida.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

