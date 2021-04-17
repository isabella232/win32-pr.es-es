---
title: ncacn_ip_tcp atributo)
description: La \_ \_ palabra clave TCP de IP de NCACN identifica TCP/IP como la familia de protocolos para el extremo.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651371"
---
# <a name="ncacn_ip_tcp-attribute"></a>\_atributo TCP de IP de ncacn \_

La palabra clave **\_ \_ TCP de IP de ncacn** identifica TCP/IP como la familia de protocolos para el extremo.

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre del servidor* 
</dt> <dd>

Especifica el nombre o la dirección de Internet del servidor, o host, del equipo. El nombre es una cadena de caracteres. La dirección de Internet es una notación de dirección de Internet común.

</dd> <dt>

*nombre del puerto* 
</dt> <dd>

Especifica un número de 16 bits opcional. Los valores de menos de 1024 suelen estar reservados. Si no se especifica ningún valor, el servicio de asignación de puntos de conexión selecciona un valor *de nombre de Puerto* válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La sintaxis de la cadena de puerto de transporte TCP/IP, como todas las cadenas de puerto, se define independientemente de la especificación IDL. El compilador realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta. Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de en tiempo de compilación.

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

[**finales**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_TCP NB \_ ncacn**](ncacn-nb-tcp.md)
</dt> <dt>

[**NP de ncacn \_**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**enlace de cadenas**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 