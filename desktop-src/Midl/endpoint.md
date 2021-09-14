---
title: atributo de punto de conexión
description: El atributo \endpoint\ especifica un puerto o puertos conocidos (puntos de conexión de comunicación) en los que los servidores de la interfaz escuchan llamadas.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- midl del atributo de punto de conexión
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159601"
---
# <a name="endpoint-attribute"></a>atributo de punto de conexión

El **\[ atributo endpoint \]** especifica un puerto o puertos conocidos (puntos de conexión de comunicación) en los que los servidores de la interfaz escuchan llamadas.

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*secuencia de protocolo* 
</dt> <dd>

Especifica una cadena de caracteres que representa una combinación válida de un protocolo RPC (como "ncacn"), un protocolo de transporte (como "tcp") y un protocolo de red (como "ip"). Para obtener una lista de secuencias de protocolo válidas, vea [Constantes de secuencia de protocolo .](/windows/desktop/Rpc/protocol-sequence-constants)

</dd> <dt>

*endpoint-port* 
</dt> <dd>

Especifica una cadena que representa la designación del extremo para la familia de protocolos especificada. La sintaxis de la cadena de puerto es específica de cada secuencia de protocolo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo \]** de punto de conexión especifica una familia de transporte, como el protocolo orientado a conexiones TCP/IP, un protocolo orientado a conexiones NetBIOS o el protocolo orientado a conexiones de canalización con nombre. El uso del atributo **\[ de \]** punto de conexión es coherente con otros métodos para agregar un punto de conexión y no proporciona servicios adicionales o especiales para el punto de conexión; simplemente proporciona un acceso directo para llamar a la API.

> [!Note]  
> Especificar un punto de conexión en . La definición de la interfaz IDL no restringe el acceso a la interfaz al punto de conexión especificado. Agregar un punto de conexión a . La definición de interfaz IDL permite llamar a la interfaz a través de cualquier punto de conexión de ese proceso y permite que el punto de conexión se utilice para llamar a otras interfaces de ese proceso.

 

El *valor de secuencia de* protocolo determina los valores válidos para el puerto de punto de *conexión.* El compilador MIDL comprueba solo la sintaxis general de la *entrada endpoint-port.* Las bibliotecas en tiempo de ejecución notifican errores de especificación de puerto. Para obtener información sobre los valores permitidos para cada secuencia de protocolo, vea [Constantes de secuencia de protocolo.](/windows/desktop/Rpc/protocol-sequence-constants)

El compilador MIDL proporcionado con RPC de Microsoft no admite las siguientes secuencias de protocolo especificadas por DCE: **ncacn \_ osi \_ dna** y **ncadg \_ dds**.

Asegúrese de que cita correctamente los caracteres de barra diagonal inversa en los puntos de conexión. Este error se produce normalmente cuando el punto de conexión es una canalización con nombre.

Las funciones en tiempo de ejecución RPC [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) y [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)usan la información del punto de conexión especificada en el archivo IDL.

## <a name="examples"></a>Ejemplos

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 