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
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159463"
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

Especifica un puerto SPP de Banyan Sarras. El intervalo válido para los puntos de conexión estáticos es de 250 a 511.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar el protocolo de transporte **ncacn \_ vns \_ spp** en aplicaciones distribuidas que se ejecutan en Windows 2000, se debe instalar el software cliente de Enterprise de Banyan adecuado. Después de la instalación, **abra Panel de control**, elija **Configuración y** Agregar y, a continuación, seleccione Servicios RPC de **\| Banyan de servicio para \| Banyan.** La compatibilidad con los clientes de 16 bits requiere el software adecuado de Trass. Para obtener más información sobre el producto Enterprise cliente de Banyan y el software de 16 bits de Banyan, póngase en contacto con Banyan.

La sintaxis de la cadena de puerto de transporte de SPP de Banyan Queryan, al igual que todas las cadenas de puerto, se define independientemente de la especificación de IDL. El compilador realiza alguna comprobación de sintaxis, pero no garantiza que la especificación del extremo sea correcta. Algunos errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

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

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[enlace de cadena](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 