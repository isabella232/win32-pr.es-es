---
title: Atributo ncalrpc
description: La palabra clave ncalrpc identifica la comunicación entre procesos local como la familia de protocolos para el punto de conexión. Esta palabra clave es uno de los nombres de familia de protocolo válidos que se deben usar con el atributo \ endpoint\.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- MidL del atributo ncalrpc
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5d22b572eb9ad2f2e46b029ec242b48d5cd684
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159454"
---
# <a name="ncalrpc-attribute"></a>Atributo ncalrpc

La **palabra clave ncalrpc** identifica la comunicación entre procesos local como la familia de protocolos para el punto de conexión. Esta palabra clave es uno de los nombres de familia de protocolo válidos que se deben usar con el atributo **\[** [**de punto de**](endpoint.md) **\]** conexión.

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*port-name* 
</dt> <dd>

Cadena de caracteres que especifica el puerto de comunicación (una aplicación, un servicio o una instancia de un servicio) que un cliente usa para realizar llamadas entre procesos a un servidor. La cadena puede contener hasta 53 caracteres y no debe contener caracteres de barra diagonal inversa ( \\ ). El nombre del equipo no debe usarse con la **palabra clave ncalrpc.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

La sintaxis de la cadena de puerto de interproceso-comunicación local, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación de IDL. El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta. Algunas clases de errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

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

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[Enlace de cadena](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 