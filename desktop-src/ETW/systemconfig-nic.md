---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de tarjetas de interfaz de red. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: SystemConfig_NIC clase
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
ms.openlocfilehash: 822e8404137eee9731bbfcee9f5d9f4495609078c4251b53269371dd4904cea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393821"
---
# <a name="systemconfig_nic-class"></a>Clase NIC SystemConfig \_

Esta clase es la clase de tipo de evento para los eventos de configuración de tarjetas de interfaz de red.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase \_ NIC SystemConfig** tiene estas propiedades.

<dl> <dt>

DnsServerAddresses
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(7), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Direcciones IP que se usarán para consultar servidores DNS. La lista de direcciones está delimitada por comas.

</dd> <dt>

IpAddresses
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(6), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Direcciones IP asociadas a la tarjeta de interfaz de red. La lista de direcciones está delimitada por comas.

</dd> <dt>

Ipv4Index
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

Índice del adaptador para la NIC IPv4. El índice del adaptador puede cambiar cuando un adaptador está deshabilitado y habilitado, o en otras circunstancias, y no debe considerarse persistente.

</dd> <dt>

Ipv6Index
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4)
</dt> </dl>

Índice del adaptador para la NIC IPv6. El índice del adaptador puede cambiar cuando un adaptador está deshabilitado y habilitado, o en otras circunstancias, y no debe considerarse persistente.

</dd> <dt>

NICDescription
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(5), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Descripción del adaptador.

</dd> <dt>

PhysicalAddr
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Format("x")
</dt> </dl>

Dirección de hardware del adaptador.

</dd> <dt>

PhysicalAddrLen
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2)
</dt> </dl>

Longitud de la dirección de hardware del adaptador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




