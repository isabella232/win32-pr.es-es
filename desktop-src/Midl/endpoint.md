---
title: atributo de extremo
description: El atributo \ Endpoint \ especifica un puerto o puertos conocidos (puntos de conexión de comunicación) en los que los servidores de la interfaz escuchan las llamadas.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- atributo de extremo MIDL
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904525"
---
# <a name="endpoint-attribute"></a>atributo de extremo

El atributo de **\[ extremo \]** especifica un puerto o puertos conocidos (puntos de conexión de comunicación) en los que los servidores de la interfaz escuchan las llamadas.

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Protocolo: secuencia* 
</dt> <dd>

Especifica una cadena de caracteres que representa una combinación válida de un protocolo RPC (como "ncacn"), un protocolo de transporte (por ejemplo, "TCP") y un protocolo de red (como "IP"). Para obtener una lista de secuencias de protocolo válidas, vea [constantes de secuencia de protocolos](/windows/desktop/Rpc/protocol-sequence-constants).

</dd> <dt>

*Puerto de extremo* 
</dt> <dd>

Especifica una cadena que representa la designación del extremo para la familia de protocolos especificada. La sintaxis de la cadena de puerto es específica de cada secuencia de protocolos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo de **\[ extremo \]** especifica una familia de transporte como el protocolo orientado a la conexión TCP/IP, un protocolo orientado a la conexión NetBIOS o el protocolo orientado a la conexión de canalización con nombre. El uso del atributo de **\[ punto de conexión \]** es coherente con otros métodos para agregar un punto de conexión y no proporciona servicios adicionales o especiales para el punto de conexión; simplemente proporciona un acceso directo para llamar a la API.

> [!Note]  
> Especificar un extremo en. La definición de la interfaz IDL no restringe el acceso a la interfaz al punto de conexión especificado. Agregar un punto de conexión a. La definición de la interfaz IDL permite llamar a la interfaz a través de cualquier punto de conexión de ese proceso y permite usar el punto de conexión para llamar a otras interfaces en ese proceso.

 

El valor de la *secuencia de protocolos* determina los valores válidos para el *Puerto del extremo*. El compilador MIDL comprueba únicamente la sintaxis general de la entrada del *Puerto de extremo* . Las bibliotecas en tiempo de ejecución informan de los errores de especificación de puerto. Para obtener información sobre los valores permitidos para cada secuencia de protocolo, vea las [constantes de secuencia de protocolo](/windows/desktop/Rpc/protocol-sequence-constants).

Las siguientes secuencias de protocolo especificadas por DCE no son compatibles con el compilador MIDL proporcionado con Microsoft RPC: **ncacn \_ OSI \_ DNA** y **ncadg \_ DDS**.

Asegúrese de que ha comillas correctamente los caracteres de barra diagonal inversa en los extremos. Este error suele producirse cuando el punto de conexión es una canalización con nombre.

La información del punto de conexión especificada en el archivo IDL se usa en las funciones de tiempo de ejecución de RPC [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) y [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).

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

 

 