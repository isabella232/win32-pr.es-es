---
title: ncacn_np atributo)
description: La \_ palabra clave ncacn NP identifica las canalizaciones con nombre como la familia de protocolos para el punto de conexión.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84634e6bb5d2b634439be767ad44749291cffe11
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791200"
---
# <a name="ncacn_np-attribute"></a>\_atributo ncacn NP

La palabra clave **ncacn \_ NP** identifica las canalizaciones con nombre como la familia de protocolos para el punto de conexión.

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre del servidor* 
</dt> <dd>

Opcional. Especifica el nombre del servidor. Los caracteres de barra diagonal inversa son opcionales.

</dd> <dt>

*nombre de canalización* 
</dt> <dd>

Especifica un nombre de canalización válido. Un nombre de canalización válido es una cadena que contiene identificadores separados por caracteres de barra diagonal inversa. El primer identificador debe ser una [**canalización**](pipe.md). Cada identificador debe estar separado por dos caracteres de barra diagonal inversa.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un servidor crea una instancia de una canalización con nombre que, a continuación, está disponible para cualquier cliente. Cuando un cliente intenta conectarse, la instancia existente se asocia con ese cliente. Antes de que otro cliente pueda conectarse, el servidor debe crear otra instancia de la canalización con nombre. Si un cliente intenta enlazarse al servidor antes de que se cree la nueva instancia, la llamada de enlace, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), puede generar un error con el mensaje de error RPC \_ S \_ Server \_ Too \_ busy. Por lo tanto, debe asegurarse de que la aplicación cliente controla el caso en el que el servidor está demasiado ocupado para aceptar una conexión. El cliente debe volver a intentarlo automáticamente, preguntar al usuario sobre una acción o producir un error.

La sintaxis de la cadena de puerto de la canalización con nombre, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación de IDL. El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta. Es posible que se notifiquen algunas clases de errores en tiempo de ejecución en lugar de en tiempo de compilación.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
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

[**ncacn \_ redes virtuales \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[**enlace de cadenas**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 