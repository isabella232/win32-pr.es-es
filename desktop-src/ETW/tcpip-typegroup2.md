---
description: Esta clase es la clase de tipo de evento para eventos de conexión y aceptación TCP/IP IPv4. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: TcpIp_TypeGroup2 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 316daec5b6bb186756f8597a63ee35d18125181b6575ae24c8ba8fae63f53d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814505"
---
# <a name="tcpip_typegroup2-class"></a>Clase \_ TypeGroup2 de TcpIp

Esta clase es la clase de tipo de evento para eventos de conexión y aceptación TCP/IP IPv4.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>Miembros

La **clase \_ TypeGroup2** de TcpIp tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TypeGroup2** de TcpIp tiene estas propiedades.

<dl> <dt>

**connid**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(15)**, **Pointer**
</dt> </dl>

Identificador de conexión único para poner en correlación los eventos que pertenecen a la misma conexión.

</dd> <dt>

**dr**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(3)**, **Extension("IPAddrV4")**
</dt> </dl>

Dirección IP de destino.

</dd> <dt>

**dport**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(5)**, **Extension("Port")**
</dt> </dl>

Número de puerto de destino.

</dd> <dt>

**Mss**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(7)**
</dt> </dl>

Tamaño máximo del segmento.

</dd> <dt>

**Pid**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(1)**
</dt> </dl>

Identificador del proceso asociado a la solicitud.

</dd> <dt>

**rcvwin**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(11)**
</dt> </dl>

Tamaño de la ventana de recepción TCP.

</dd> <dt>

**rcvwinscale**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(12)**
</dt> </dl>

Factor de escalado de ventana de recepción TCP.

</dd> <dt>

**tabotón**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(8)**
</dt> </dl>

Opción confirmación selectiva (SOAP) en el encabezado TCP.

</dd> <dt>

**saddr**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(4)**, **Extension("IPAddrV4")**
</dt> </dl>

Dirección IP de origen.

</dd> <dt>

**seqnum**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(14)**
</dt> </dl>

Número de secuencia.

</dd> <dt>

**size**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(2)**
</dt> </dl>

Tamaño del paquete.

</dd> <dt>

**sndwinscale**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(13)**
</dt> </dl>

Factor de escalado de ventana de envío TCP.

</dd> <dt>

**Deporte**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(6)**, **Extension("Port")**
</dt> </dl>

Número de puerto de origen.

</dd> <dt>

**tsopt**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(9)**
</dt> </dl>

Opción Marca de tiempo en el encabezado TCP.

</dd> <dt>

**wsopt**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId(10)**
</dt> </dl>

Opción Escala de ventana en el encabezado TCP.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tcpip**](tcpip.md)
</dt> </dl>

 

 




