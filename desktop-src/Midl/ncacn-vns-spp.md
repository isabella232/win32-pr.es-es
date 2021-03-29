---
title: ncacn_vns_spp atributo)
description: La \_ \_ palabra clave ncacn redes virtuales spp identifica Banyan Vines spp como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790708"
---
# <a name="ncacn_vns_spp-attribute"></a>\_atributo ncacn redes virtuales \_ spp

La palabra clave **ncacn \_ redes virtuales \_ spp** identifica Banyan Vines spp como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre del servidor* 
</dt> <dd>

Especifica el nombre de StreetTalk del servidor. El nombre tiene el formato item@group @organization . El elemento puede tener una longitud de hasta 31 caracteres y el grupo y la organización pueden tener un máximo de 15 caracteres.

</dd> <dt>

*nombre del puerto* 
</dt> <dd>

Especifica un puerto de Banyan Vines SPP. El intervalo válido para los puntos de conexión estáticos es 250 – 511.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar el protocolo de transporte **ncacn \_ redes virtuales \_ spp** en aplicaciones distribuidas que se ejecutan en Windows 2000, debe instalarse el software de Banyan cliente de empresa adecuado. Después de la instalación, abra el **Panel de control**, elija **configuración y agregar** y, a continuación, seleccione **servicio \| Banyan \| RPC Services para Banyan**. La compatibilidad con clientes de 16 bits requiere el software de Vines adecuado. Para obtener más información sobre el producto de Cliente de empresa de Banyan y el software de 16 bits Vines, póngase en contacto con Banyan.

La sintaxis de la cadena de puerto de transporte de Banyan Vines SPP, como todas las cadenas de puerto, se define independientemente de la especificación de IDL. El compilador realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta. Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de en tiempo de compilación.

> [!Note]  
> Esta familia de protocolos no es compatible con Windows XP.

 

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
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

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[enlace de cadenas](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 