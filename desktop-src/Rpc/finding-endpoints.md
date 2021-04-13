---
title: Búsqueda de puntos de conexión
description: Los programas de servidor escuchan los puntos de conexión para las solicitudes de cliente. La sintaxis de la cadena de punto de conexión depende de la secuencia de protocolo que se use. Por ejemplo, el extremo de TCP/IP es un número de puerto y la sintaxis de extremo para canalizaciones con nombre es un nombre de canalización válido.
ms.assetid: 330bbe9f-b7e9-4a5b-86d8-824edec960d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0a97df3408a4d3c24dff9de28553f9e4b2210d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359051"
---
# <a name="finding-endpoints"></a>Búsqueda de puntos de conexión

Los programas de servidor escuchan los puntos de conexión para las solicitudes de cliente. La sintaxis de la cadena de punto de conexión depende de la secuencia de protocolo que se use. Por ejemplo, el extremo de TCP/IP es un número de puerto y la sintaxis de extremo para canalizaciones con nombre es un nombre de canalización válido.

Hay dos tipos de extremos: Well-Known y Dynamic. La elección del tipo de punto de conexión que utiliza el programa determina si la aplicación distribuida o la biblioteca en tiempo de ejecución especifica el extremo.

En esta sección se describen los puntos de conexión y se ofrece información sobre cómo encontrarlos. Se organiza en los temas siguientes:

-   [Uso de puntos de conexión de Well-Known](#using-well-known-endpoints)
-   [Uso de puntos de conexión dinámicos](#using-dynamic-endpoints)
-   [Exportar Well-Known puntos de conexión en la base de datos de asignación de puntos de conexión](#exporting-well-known-endpoints-into-the-endpoint-map-database)

> [!Note]  
> Los términos *puntos de conexión estáticos* y puntos *de conexión conocidos* son equivalentes y se usan indistintamente.

 

Es posible que la aplicación cliente use la asignación de punto de conexión para determinar si un programa de servidor se está ejecutando actualmente o no. El cliente puede llamar a [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)y [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) para ver si el servidor ha registrado la interfaz concreta que requiere en la asignación de punto de conexión.

## <a name="using-well-known-endpoints"></a>Uso de puntos de conexión conocidos

Los puntos de conexión conocidos son extremos asignados previamente que el programa de servidor usa cada vez que se ejecuta. Dado que el servidor siempre escucha a ese extremo concreto, el cliente siempre intenta conectarse a él. Los puntos de conexión conocidos suelen estar asignados por la autoridad responsable del Protocolo de transporte. Dado que los equipos host de servidor tienen un número finito de puntos de conexión disponibles, se recomienda encarecidamente que los desarrolladores de aplicaciones usen puntos de conexión conocidos. Otra ventaja de los puntos de conexión dinámicos es que simplifican la administración y el mantenimiento a largo plazo del sistema.

Una aplicación distribuida puede especificar un punto de conexión conocido en una cadena y pasar esa cadena como un parámetro a la función [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep). Como alternativa, la cadena de punto de conexión puede aparecer en el encabezado de la interfaz de archivo IDL como parte del atributo de interfaz de \[ [extremo](/windows/desktop/Midl/endpoint) \] .

Puede usar dos enfoques para implementar el punto de conexión conocido:

-   Especificar toda la información en un enlace de cadena
-   Almacenar el punto de conexión conocido en la base de datos del servicio de nombres

Puede escribir toda la información necesaria para establecer un enlace en una aplicación distribuida al desarrollarla. El cliente puede especificar el punto de conexión conocido directamente en una cadena, llamar a [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) para crear una cadena que contenga toda la información de enlace y proporcionar esta cadena a la función [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obtener un identificador. El cliente y el servidor se pueden codificar de forma rígida para usar un punto de conexión bien conocido, o bien escribirse de modo que la información del punto de conexión proceda de la línea de comandos, un archivo de datos, un archivo de configuración o el archivo IDL.

La aplicación cliente también puede consultar una base de datos del servicio de nombres para obtener información de punto de conexión conocida.

## <a name="using-dynamic-endpoints"></a>Uso de puntos de conexión dinámicos

Normalmente, el número de puntos de conexión para un servidor determinado y una secuencia de protocolo determinada es limitado. Por ejemplo, cuando se usa la secuencia de protocolo [ \_ \_ TCP IP ncacn](/windows/desktop/Midl/ncacn-ip-tcp) , que indica que la comunicación de red RPC se produce mediante TCP/IP, solo hay disponible un número limitado de puertos (la mayoría de los sistemas solo tienen abierto el intervalo de 1025 a 5000). Las bibliotecas en tiempo de ejecución de RPC permiten asignar puntos de conexión dinámicamente, según sea necesario. Dado que el número de UUID de interfaz posible es prácticamente ilimitado, el uso de la interfaz UUID para dirigir la llamada ofrece más espacio para la expansión y más flexibilidad.

De forma predeterminada, las funciones de la biblioteca en tiempo de ejecución de RPC buscan información del punto de conexión cuando consultan una base de datos del servicio de nombres. Si el extremo es dinámico, la base de datos del servicio de nombres no contendrá información del punto de conexión. Sin embargo, la consulta proporcionará al programa cliente el nombre de un servidor. Después, puede buscar en la asignación de punto de conexión del servidor.

Si el cliente necesita realizar una llamada a procedimiento remoto mediante un punto de conexión dinámico, el método preferido es realizar la llamada en un identificador de enlace enlazado parcialmente. El tiempo de ejecución de RPC resuelve el punto de conexión de forma transparente. Este método es superior al uso de la función [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding) , ya que permite mecanismos de almacenamiento en caché avanzados en el tiempo de ejecución de RPC.

Si se requiere un control más específico sobre la selección del punto de conexión, los clientes pueden buscar en la asignación de punto de conexión una entrada cada vez llamando a las funciones [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin), [**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)y [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) .

## <a name="exporting-well-known-endpoints-into-the-endpoint-map-database"></a>Exportar puntos de conexión conocidos en la base de datos de asignación de puntos de conexión

Es posible mezclar los dos enfoques para buscar puntos de conexión, especialmente cuando un sistema distribuido está pasando de un modelo de punto de conexión conocido a un modelo de punto de conexión dinámico. En tales transiciones, una versión intermedia del servidor usará un punto de conexión conocido, pero también registrará el punto de conexión conocido con la base de datos de asignación de puntos de conexión. Este enfoque permite a los clientes que usan puntos de conexión conocidos y clientes que usan un extremo dinámico conectarse. Una vez que se han actualizado todos los servidores, se puede implementar una nueva versión de cliente que solo use puntos de conexión dinámicos. Una vez que se actualizan todos los clientes, una versión final del servidor puede dejar de usar puntos de conexión conocidos y comenzar a usar solo puntos de conexión dinámicos.

Este enfoque permite una ruta de transición para las aplicaciones que se han iniciado con un punto de conexión conocido pero que desean migrar a un punto de conexión dinámico sin necesidad de una actualización simultánea de todos los servidores y clientes.

 

 