---
description: 'UdpIp_V1_TypeGroup1 clase : esta clase es la clase de tipo de evento para eventos UDP/IP. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: UdpIp_V1_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2c4a16dc8e0d08ab70a15b1d6a887ff8863a1b81c46c4318421df2169fd5d196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069345"
---
# <a name="udpip_v1_typegroup1-class"></a>Clase \_ \_ TypeGroup1 udpIp V1

Esta clase es la clase de tipo de evento para eventos UDP/IP.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a>Miembros

La **clase UdpIp \_ V1 \_ TypeGroup1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ TypeGroup1 UdpIp V1** tiene estas propiedades.

<dl> <dt>

dr
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3), Extension("IPAddr")
</dt> </dl>

Dirección IP de destino.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(5), Extension("Port")
</dt> </dl>

Número de puerto de destino.

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1)
</dt> </dl>

Identificador del proceso asociado a la solicitud.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4), Extension("IPAddr")
</dt> </dl>

Dirección IP de origen.

</dd> <dt>

tamaño
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2)
</dt> </dl>

Tamaño del paquete.

</dd> <dt>

Deporte
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(6), Extension("Port")
</dt> </dl>

Número de puerto de origen.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**UdpIp \_ V1**](udpip-v1.md)
</dt> <dt>

[**UdpIp**](udpip.md)
</dt> </dl>

 

 




