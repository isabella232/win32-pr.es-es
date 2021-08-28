---
title: ncacn_vns_spp atributo
description: La palabra clave ncacn \_ vns \_ spp identifica a BanyanHibs SPP como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8409e7e9e0bfc01545ac73673f0653c5a4940c65422223233ec5005f5c9fc02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560285"
---
# <a name="ncacn_vns_spp-attribute"></a>Atributo ncacn \_ vns \_ spp

La **palabra clave ncacn \_ vns \_ spp** identifica a BanyanHibs SPP como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*server-name* 
</dt> <dd>

Especifica el nombre de StreetTalk del servidor. El nombre tiene el formato item@group @organization . El elemento puede tener hasta 31 caracteres y el grupo y la organización pueden tener hasta 15 caracteres.

</dd> <dt>

*port-name* 
</dt> <dd>

Especifica un puerto de SPP de Banyan Queryan. El intervalo válido para los puntos de conexión estáticos es de 250 a 511.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para usar el protocolo de transporte **ncacn \_ vns \_ spp** en aplicaciones distribuidas que se ejecutan en Windows 2000, debe instalarse el software cliente de Enterprise De Banyan adecuado. Después de la instalación, **abra Panel de control**, elija Configuración y **Agregar** y, a continuación, seleccione Servicios RPC **de \| Banyan de servicio para \| Banyan.** La compatibilidad con clientes de 16 bits requiere el software adecuado de Ques. Para obtener más información sobre el producto Enterprise cliente de Banyan y el software de 16 bits de Banyan, póngase en contacto con Banyan.

La sintaxis de la cadena de puerto de transporte de SPP de BanyanTaxis, como todas las cadenas de puerto, se define independientemente de la especificación de IDL. El compilador realiza alguna comprobación de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta. Algunos errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

> [!Note]  
> Esta familia de protocolos no se admite en Windows XP.

 

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

[**Extremo**](endpoint.md)
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

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[enlace de cadena](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 