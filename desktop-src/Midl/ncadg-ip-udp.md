---
title: ncadg_ip_udp atributo)
description: La \_ \_ palabra clave UDP de IP de ncadg identifica la versión de DATAGRAMA de TCP/IP como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp el atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149218"
---
# <a name="ncadg_ip_udp-attribute"></a>\_atributo UDP de IP ncadg \_

La palabra clave **\_ \_ UDP de IP de ncadg** identifica la versión de DATAGRAMA de TCP/IP como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre del servidor* 
</dt> <dd>

Especifica el nombre o la dirección de Internet del servidor, o host, del equipo. El nombre es una cadena de caracteres y puede ser un nombre de dominio completo. La dirección de Internet es una notación de dirección de Internet común.

</dd> <dt>

*nombre del puerto* 
</dt> <dd>

Especifica un número de 16 bits opcional. Los valores de menos de 1024 suelen estar reservados. Si no se especifica ningún valor, el servicio de asignación de puntos de conexión selecciona un valor *de nombre de Puerto* válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las siguientes restricciones se aplican a los protocolos de datagramas, [**ncadg \_ IPX**](ncadg-ipx.md) y **ncadg \_ IP \_ UDP**:

-   No admiten las devoluciones de llamada. **\[** [](callback.md) Se producirá un error en todas las funciones que utilicen el **\]** atributo callback.
-   No admiten el uso del constructor de tipo de [**canalización**](pipe.md) .

La sintaxis de la cadena de puerto de transporte TCP/IP, como todas las cadenas de puerto, se define independientemente de la especificación IDL. El compilador realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta. Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de en tiempo de compilación.

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

[**finales**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ en \_ DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ NSP**](ncacn-dnet-nsp.md)
</dt> <dt>

[**\_TCP IP \_ ncacn**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ NB \_ IPX**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**\_TCP NB \_ ncacn**](ncacn-nb-tcp.md)
</dt> <dt>

[**NP de ncacn \_**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ redes virtuales \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[Enlace de cadenas](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 