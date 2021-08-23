---
title: ncacn_np atributo
description: La palabra clave np \_ ncacn identifica las canalizaciones con nombre como la familia de protocolos para el punto de conexión.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7acf294241c1d38b2067ba54e315fc3240e5bb6eca81a6b12012f8dec457a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013763"
---
# <a name="ncacn_np-attribute"></a>atributo \_ np ncacn

La **palabra clave np \_ ncacn** identifica las canalizaciones con nombre como la familia de protocolos para el punto de conexión.

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*server-name* 
</dt> <dd>

Opcional. Especifica el nombre del servidor. Los caracteres de barra diagonal inversa son opcionales.

</dd> <dt>

*pipe-name* 
</dt> <dd>

Especifica un nombre de canalización válido. Un nombre de canalización válido es una cadena que contiene identificadores separados por caracteres de barra diagonal inversa. El primer identificador debe ser [**la canalización**](pipe.md). Cada identificador debe estar separado por dos caracteres de barra diagonal inversa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Un servidor crea una instancia de una canalización con nombre que, a continuación, está disponible para cualquier cliente. Cuando un cliente intenta conectarse, la instancia existente está asociada a ese cliente. Antes de que otro cliente pueda conectarse, el servidor debe crear otra instancia de la canalización con nombre. Si un cliente intenta enlazar con el servidor antes de crear la nueva instancia, la llamada de enlace, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), puede producir un error con el mensaje de error RPC \_ S SERVER TOO \_ \_ \_ BUSY. Por lo tanto, debe asegurarse de que la aplicación cliente controla el caso en el que el servidor está demasiado ocupado para aceptar una conexión. El cliente debe reintentar automáticamente, solicitar al usuario un curso de acción o producir un error correctamente.

La sintaxis de la cadena de puerto de canalización con nombre, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación de IDL. El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta. Algunas clases de errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

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

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**enlace de cadena**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 