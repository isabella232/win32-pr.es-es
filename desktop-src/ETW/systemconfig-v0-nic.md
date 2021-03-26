---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de tarjeta de interfaz de red.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: SystemConfig_V0_NIC (clase)
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
ms.openlocfilehash: 040c409564c0ad37e5208c1e91962d3f04de5fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985935"
---
# <a name="systemconfig_v0_nic-class"></a>\_Clase SystemConfig V0 \_ NIC

Esta clase es la clase de tipo de evento para los eventos de configuración de tarjeta de interfaz de red.

La siguiente sintaxis se simplifica desde el código MOF.

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

La clase **SystemConfig \_ V0 \_ NIC** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **SystemConfig \_ V0 \_ NIC** tiene estas propiedades.

<dl> <dt>

**Data**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
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

Dirección IP del servidor del Protocolo de configuración dinámica de host (DHCP). Un valor de 255.255.255.255 indica que no se pudo establecer contacto con el servidor DHCP o está en proceso de alcanzarse. Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4). El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.

</dd> <dt>

**DnsServer1**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (12)
</dt> </dl>

Primeras direcciones IP de servidor que se van a usar en la consulta de servidores DNS. Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4). El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.

</dd> <dt>

**DnsServer2**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (13)
</dt> </dl>

Segundas direcciones IP de servidor que se van a usar en la consulta de servidores DNS. Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4). El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.

</dd> <dt>

**DnsServer3**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (14)
</dt> </dl>

Direcciones IP de tercer servidor que se van a usar en la consulta de servidores DNS. Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4). El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.

</dd> <dt>

**DnsServer4**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (15)
</dt> </dl>

Cuarta direcciones IP de servidor que se van a usar en la consulta de servidores DNS. Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4). El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.

</dd> <dt>

**Puerta de enlace**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (9)
</dt> </dl>

Dirección IP de la puerta de enlace predeterminada que utiliza el sistema del equipo. Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4). El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2)
</dt> </dl>

Índice del adaptador. El índice del adaptador puede cambiar cuando un adaptador está deshabilitado y habilitado, o en otras circunstancias, y no debe considerarse persistente.

</dd> <dt>

**IpAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6)
</dt> </dl>

Direcciones IP asociadas a la tarjeta de interfaz de red. Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4). El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.

</dd> <dt>

**NICName**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **char16**
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

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3)
</dt> </dl>

Longitud de la dirección de hardware para el adaptador.

</dd> <dt>

**PrimaryWinsServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (10)
</dt> </dl>

Dirección IP del servidor WINS principal. Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4). El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.

</dd> <dt>

**SecondaryWinsServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (11)
</dt> </dl>

Dirección IP del servidor WINS secundario. Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4). El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.

</dd> <dt>

**Tamaño**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5)
</dt> </dl>

Tamaño, en bytes, de la propiedad de datos.

</dd> <dt>

**SubnetMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (7)
</dt> </dl>

Máscara de subred asociada a la tarjeta de interfaz de red. Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4). El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 




