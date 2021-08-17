---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de tarjetas de interfaz de red.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: SystemConfig_V0_NIC clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6abe9356ce222d8f461509ec9cfa25ab0a49b8583022ee5e1d832cf29a226dcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746475"
---
# <a name="systemconfig_v0_nic-class"></a>Clase NIC SystemConfig \_ V0 \_

Esta clase es la clase de tipo de evento para los eventos de configuración de tarjetas de interfaz de red.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a>Miembros

La **clase NIC SystemConfig \_ V0 \_** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase NIC SystemConfig \_ V0 \_** tiene estas propiedades.

<dl> <dt>

**Datos**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (16)
</dt> </dl>

Campo de datos.

</dd> <dt>

**DhcpServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (8)
</dt> </dl>

Dirección IP del servidor del protocolo de configuración dinámica de host (DHCP). Un valor de 255.255.255.255 indica que no se pudo alcanzar el servidor DHCP o que está en proceso de ser alcanzado. Cada byte del sint32 representa una de las cuatro partes de la dirección IP (p1.p2.p3.p4). El byte de orden bajo contiene el valor de p1, el byte siguiente contiene el valor de p2, y así sucesivamente.

</dd> <dt>

**DnsServer1**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (12)
</dt> </dl>

Primera dirección IP del servidor que se usará en la consulta de servidores DNS. Cada byte del sint32 representa una de las cuatro partes de la dirección IP (p1.p2.p3.p4). El byte de orden bajo contiene el valor de p1, el byte siguiente contiene el valor de p2, y así sucesivamente.

</dd> <dt>

**DnsServer2**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (13)
</dt> </dl>

Segundas direcciones IP de servidor que se usarán en las consultas de servidores DNS. Cada byte del sint32 representa una de las cuatro partes de la dirección IP (p1.p2.p3.p4). El byte de orden bajo contiene el valor de p1, el byte siguiente contiene el valor de p2, y así sucesivamente.

</dd> <dt>

**DnsServer3**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (14)
</dt> </dl>

Terceras direcciones IP de servidor que se usarán en las consultas de servidores DNS. Cada byte del sint32 representa una de las cuatro partes de la dirección IP (p1.p2.p3.p4). El byte de orden bajo contiene el valor de p1, el byte siguiente contiene el valor de p2, y así sucesivamente.

</dd> <dt>

**DnsServer4**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (15)
</dt> </dl>

Cuartas direcciones IP de servidor que se usarán en las consultas de servidores DNS. Cada byte del sint32 representa una de las cuatro partes de la dirección IP (p1.p2.p3.p4). El byte de orden bajo contiene el valor de p1, el byte siguiente contiene el valor de p2, y así sucesivamente.

</dd> <dt>

**Puerta de enlace**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (9)
</dt> </dl>

Dirección IP de la puerta de enlace predeterminada que usa el sistema informático. Cada byte del sint32 representa una de las cuatro partes de la dirección IP (p1.p2.p3.p4). El byte de orden bajo contiene el valor de p1, el byte siguiente contiene el valor de p2, y así sucesivamente.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2)
</dt> </dl>

Índice del adaptador. El índice del adaptador puede cambiar cuando un adaptador está deshabilitado y, a continuación, habilitado, o en otras circunstancias, y no debe considerarse persistente.

</dd> <dt>

**Ipaddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6)
</dt> </dl>

Direcciones IP asociadas a la tarjeta de interfaz de red. Cada byte del sint32 representa una de las cuatro partes de la dirección IP (p1.p2.p3.p4). El byte de orden bajo contiene el valor de p1, el byte siguiente contiene el valor de p2, y así sucesivamente.

</dd> <dt>

**NICName**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1), **Max** (256)
</dt> </dl>

Nombre de la tarjeta de interfaz de red.

</dd> <dt>

**PhysicalAddr**
</dt> <dd> <dl> <dt>

Tipo de datos: **char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4), **Max** (8)
</dt> </dl>

Dirección de hardware del adaptador.

</dd> <dt>

**PhysicalAddrLen**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3)
</dt> </dl>

Longitud de la dirección de hardware del adaptador.

</dd> <dt>

**PrimaryWinsServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (10)
</dt> </dl>

Dirección IP del servidor WINS principal. Cada byte del sint32 representa una de las cuatro partes de la dirección IP (p1.p2.p3.p4). El byte de orden bajo contiene el valor de p1, el byte siguiente contiene el valor de p2, y así sucesivamente.

</dd> <dt>

**SecondaryWinsServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (11)
</dt> </dl>

Dirección IP del servidor WINS secundario. Cada byte del sint32 representa una de las cuatro partes de la dirección IP (p1.p2.p3.p4). El byte de orden bajo contiene el valor de p1, el byte siguiente contiene el valor de p2, y así sucesivamente.

</dd> <dt>

**Tamaño**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5)
</dt> </dl>

Tamaño, en bytes, de la propiedad Data.

</dd> <dt>

**SubnetMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (7)
</dt> </dl>

Máscara de subred asociada a la tarjeta de interfaz de red. Cada byte del sint32 representa una de las cuatro partes de la dirección IP (p1.p2.p3.p4). El byte de orden bajo contiene el valor de p1, el byte siguiente contiene el valor de p2, y así sucesivamente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




