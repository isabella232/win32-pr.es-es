---
title: ncadg_ip_udp atributo
description: La palabra clave udp de ip ncadg identifica la versión del datagrama de \_ TCP/IP como la familia de \_ protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159461"
---
# <a name="ncadg_ip_udp-attribute"></a>Atributo udp \_ de ip de ncadg \_

La **palabra clave udp de ip \_ \_ ncadg** identifica la versión del datagrama de TCP/IP como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*server-name* 
</dt> <dd>

Especifica el nombre o la dirección de Internet del servidor o host del equipo. El nombre es una cadena de caracteres y puede ser un nombre de dominio completo. La dirección de Internet es una notación de dirección de Internet común.

</dd> <dt>

*port-name* 
</dt> <dd>

Especifica un número opcional de 16 bits. Normalmente, los valores de menos de 1024 están reservados. Si no se especifica ningún valor, el servicio de asignación de puntos de conexión selecciona un valor de *nombre de puerto* válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las restricciones siguientes se aplican a los protocolos de datagrama, [**ncadg \_ ipx**](ncadg-ipx.md) y **ncadg \_ ip \_ udp**:

-   No admiten devoluciones de llamada. Se producirá un error en todas las funciones que usen **\[** [**el**](callback.md) atributo de **\]** devolución de llamada.
-   No admiten el uso del constructor [**de tipo**](pipe.md) de canalización.

La sintaxis de la cadena de puerto de transporte TCP/IP, como todas las cadenas de puerto, se define independientemente de la especificación de IDL. El compilador realiza alguna comprobación de sintaxis, pero no garantiza que la especificación del extremo sea correcta. Algunos errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ en \_ dsp**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ nsp**](ncacn-dnet-nsp.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ ipx**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[Enlace de cadena](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 