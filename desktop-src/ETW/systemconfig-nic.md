---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de tarjeta de interfaz de red. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: SystemConfig_NIC (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63d522eee993f0766554eb9bc4fb09d842e9cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001175"
---
# <a name="systemconfig_nic-class"></a>\_Clase SystemConfig NIC

Esta clase es la clase de tipo de evento para los eventos de configuración de tarjeta de interfaz de red.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a>Miembros

La **clase \_ NIC SystemConfig** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **SystemConfig \_ NIC** tiene estas propiedades.

<dl> <dt>

DnsServerAddresses
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (7), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Direcciones IP que se van a usar en la consulta de servidores DNS. La lista de direcciones está delimitada por comas.

</dd> <dt>

IpAddresses
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (6), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Direcciones IP asociadas a la tarjeta de interfaz de red. La lista de direcciones está delimitada por comas.

</dd> <dt>

Ipv4Index
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

Índice de adaptador para NIC IPv4. El índice del adaptador puede cambiar cuando un adaptador está deshabilitado y habilitado, o en otras circunstancias, y no debe considerarse persistente.

</dd> <dt>

Ipv6Index
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4)
</dt> </dl>

Índice de adaptador para NIC IPv6. El índice del adaptador puede cambiar cuando un adaptador está deshabilitado y habilitado, o en otras circunstancias, y no debe considerarse persistente.

</dd> <dt>

NICDescription
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Descripción del adaptador.

</dd> <dt>

PhysicalAddr
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), Format ("x")
</dt> </dl>

Dirección de hardware del adaptador.

</dd> <dt>

PhysicalAddrLen
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2)
</dt> </dl>

Longitud de la dirección de hardware para el adaptador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




