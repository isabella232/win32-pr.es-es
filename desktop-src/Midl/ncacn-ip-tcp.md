---
title: ncacn_ip_tcp atributo
description: La palabra clave ncacn \_ ip tcp identifica TCP/IP como la familia de \_ protocolos para el punto de conexión.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34ba0a872af79245469818121761a38d356316b53a31743f9ebf2cd66f72325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642236"
---
# <a name="ncacn_ip_tcp-attribute"></a>Atributo \_ tcp de ip \_ ncacn

La **palabra clave ncacn \_ ip \_ tcp** identifica TCP/IP como la familia de protocolos para el punto de conexión.

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*server-name* 
</dt> <dd>

Especifica el nombre o la dirección de Internet del servidor o host del equipo. El nombre es una cadena de caracteres. La dirección de Internet es una notación de dirección de Internet común.

</dd> <dt>

*port-name* 
</dt> <dd>

Especifica un número opcional de 16 bits. Los valores de menor que 1024 normalmente se reservan. Si no se especifica ningún valor, el servicio de asignación de puntos de conexión selecciona un valor *de nombre de puerto* válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La sintaxis de la cadena de puerto de transporte TCP/IP, como todas las cadenas de puerto, se define independientemente de la especificación de IDL. El compilador realiza alguna comprobación de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta. Algunos errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

## <a name="examples"></a>Ejemplos

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Extremo**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**enlace de cadena**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 