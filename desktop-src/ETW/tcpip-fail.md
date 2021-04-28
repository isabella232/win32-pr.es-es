---
description: 'TcpIp_Fail clase : esta clase es la clase de tipo de evento para los eventos de error de TCP/IP. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 1fe20b8c-b8f1-4db0-af78-1ebfc40b2bbd
title: TcpIp_Fail clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_Fail
- TcpIp_Fail.Proto
- TcpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 897c42a1c2530d3e41d1f937d5d59356a2913e2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105853"
---
# <a name="tcpip_fail-class"></a>TcpIp \_ Fail (clase)

Esta clase es la clase de tipo de evento para los eventos de error de TCP/IP.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a>Miembros

La **clase TcpIp \_ Fail** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase TcpIp \_ Fail** tiene estas propiedades.

<dl> <dt>

**Código de error**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Motivo del error. Puede ser uno de los códigos siguientes:

<dl> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR \_ RECURSOS \_ INSUFICIENTES** (1)
</dt> <dt>

<span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR \_ DEMASIADAS \_ \_ DIRECCIONES** (2)
</dt> <dt>

<span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR \_ ADDRESS \_ EXISTS** (3)
</dt> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR \_ DIRECCIÓN \_ NO VÁLIDA** (4)
</dt> <dt>

<span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR \_ OTHER** (5)
</dt> <dt>

<span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR \_ TIMEWAIT \_ ADDRESS \_ EXIST** (6)
</dt> </dl>

</dd> <dt>

**Proto**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica el protocolo. Puede ser uno de los siguientes valores:



| Valor                                                                                                                                                                                                  | Significado                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>     | La familia de direcciones IPv4 (Protocolo de Internet versión 4).<br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl> | La familia de direcciones IPv6 (Protocolo de Internet versión 6).<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tcpip**](tcpip.md)
</dt> </dl>

 

 




