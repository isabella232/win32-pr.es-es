---
title: atributo ncalrpc
description: La palabra clave ncalrpc identifica la comunicación entre procesos locales como la familia de protocolos para el punto de conexión. Esta palabra clave es uno de los nombres de familia de protocolos válidos que se deben usar con el atributo \ Endpoint \.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- ncalrpc (atributo) MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f20ae9e347303288868eeb16758736047fecc1b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995221"
---
# <a name="ncalrpc-attribute"></a>atributo ncalrpc

La palabra clave **ncalrpc** identifica la comunicación entre procesos locales como la familia de protocolos para el punto de conexión. Esta palabra clave es uno de los nombres de familia de protocolos válidos que se deben usar con el atributo de **\[** [**extremo**](endpoint.md) **\]** .

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre del puerto* 
</dt> <dd>

Cadena de caracteres que especifica el puerto de comunicación (una aplicación, un servicio o una instancia de un servicio) que un cliente usa para realizar llamadas entre procesos a un servidor. La cadena puede contener hasta 53 caracteres y no debe contener ninguna barra diagonal inversa ( \) caracteres). El nombre del equipo no se debe utilizar con la palabra clave **ncalrpc** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

La sintaxis de la cadena de puerto de comunicación entre procesos local, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación de IDL. El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta. Es posible que se notifiquen algunas clases de errores en tiempo de ejecución en lugar de en tiempo de compilación.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
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

[**ncacn \_ redes virtuales \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[Enlace de cadenas](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 