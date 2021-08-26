---
title: Búsqueda de puntos de conexión
description: Los programas de servidor escuchan los puntos de conexión de las solicitudes de cliente. La sintaxis de la cadena de punto de conexión depende de la secuencia de protocolo que use. Por ejemplo, el punto de conexión para TCP/IP es un número de puerto y la sintaxis del punto de conexión para las canalizaciones con nombre es un nombre de canalización válido.
ms.assetid: 330bbe9f-b7e9-4a5b-86d8-824edec960d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024a85704287db7e5f78bb67eee9b64a7c6dc84ce5724623450d36f743e5fa9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021285"
---
# <a name="finding-endpoints"></a>Búsqueda de puntos de conexión

Los programas de servidor escuchan los puntos de conexión de las solicitudes de cliente. La sintaxis de la cadena de punto de conexión depende de la secuencia de protocolo que use. Por ejemplo, el punto de conexión para TCP/IP es un número de puerto y la sintaxis del punto de conexión para las canalizaciones con nombre es un nombre de canalización válido.

Hay dos tipos de puntos de conexión: conocidos y dinámicos. La elección del tipo de punto de conexión que usa el programa determina si la aplicación distribuida o la biblioteca en tiempo de ejecución especifica el punto de conexión.

En esta sección se analizan los puntos de conexión y se presenta información sobre cómo encontrarlos. Se organiza en los temas siguientes:

-   [Uso de Well-Known de conexión](#using-well-known-endpoints)
-   [Uso de puntos de conexión dinámicos](#using-dynamic-endpoints)
-   [Exportación de puntos Well-Known de conexión a la base de datos del mapa de puntos de conexión](#exporting-well-known-endpoints-into-the-endpoint-map-database)

> [!Note]  
> Los *términos puntos de conexión estáticos* y puntos de conexión conocidos son *equivalentes* y se usan indistintamente.

 

Es posible que la aplicación cliente use la asignación de punto de conexión para determinar si un programa de servidor se está ejecutando actualmente o no. El cliente puede llamar a [**RpcMgmtInqIfIds,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids) [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)y [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) para ver si el servidor ha registrado la interfaz concreta que requiere en la asignación del punto de conexión.

## <a name="using-well-known-endpoints"></a>Uso de puntos de conexión conocidos

Los puntos de conexión conocidos son puntos de conexión asignados previamente que el programa de servidor usa cada vez que se ejecuta. Dado que el servidor siempre escucha a ese punto de conexión determinado, el cliente siempre intenta conectarse a él. Normalmente, la autoridad responsable del protocolo de transporte asigna los puntos de conexión conocidos. Dado que los equipos host de servidor tienen un número finito de puntos de conexión disponibles, se desaconseja encarecidamente a los desarrolladores de aplicaciones el uso de puntos de conexión conocidos. Otra ventaja de los puntos de conexión dinámicos es que simplifican la administración y el mantenimiento a largo plazo del sistema.

Una aplicación distribuida puede especificar un punto de conexión conocido en una cadena y pasar esa cadena como parámetro a la [**función RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep). Como alternativa, la cadena de punto de conexión puede aparecer en el encabezado de interfaz de archivo IDL como parte del atributo de interfaz \[ [](/windows/desktop/Midl/endpoint) \] de punto de conexión.

Puede usar dos enfoques para implementar el punto de conexión conocido:

-   Especificar toda la información en un enlace de cadena
-   Almacenar el punto de conexión conocido en la base de datos de servicio de nombres

Puede escribir toda la información necesaria para establecer un enlace en una aplicación distribuida al desarrollarlo. El cliente puede especificar el punto de conexión conocido directamente en una cadena, llamar a [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) para crear una cadena que contenga toda la información de enlace y proporcionar esta cadena a la [**función RpcBindingFromStringBinding para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) obtener un identificador. El cliente y el servidor se pueden codificar de forma automática para usar un punto de conexión conocido o escribirse para que la información del punto de conexión procede de la línea de comandos, un archivo de datos, un archivo de configuración o el archivo IDL.

La aplicación cliente también puede consultar una base de datos de servicio de nombres para obtener información de punto de conexión conocida.

## <a name="using-dynamic-endpoints"></a>Uso de puntos de conexión dinámicos

El número de puntos de conexión para un servidor determinado y una secuencia de protocolo determinada suelen ser limitados. Por ejemplo, cuando se usa la secuencia del protocolo [ \_ ncacn ip \_ tcp,](/windows/desktop/Midl/ncacn-ip-tcp) lo que indica que la comunicación de red RPC se produce mediante TCP/IP, solo hay un número limitado de puertos disponibles (la mayoría de los sistemas solo tienen abierto el intervalo de 1025 a 5000). Las bibliotecas en tiempo de ejecución de RPC permiten asignar puntos de conexión dinámicamente, según sea necesario. Dado que el número de UUID de interfaz posibles es prácticamente ilimitado, el uso del UUID de la interfaz para dirigir la llamada ofrece más espacio para la expansión y más flexibilidad.

De forma predeterminada, las funciones de la biblioteca en tiempo de ejecución de RPC buscan información de punto de conexión cuando consultan una base de datos de servicio de nombres. Si el punto de conexión es dinámico, la base de datos de servicio de nombres no contendrá información de punto de conexión. Sin embargo, la consulta dará al programa cliente el nombre de un servidor. A continuación, puede buscar en el mapa de puntos de conexión del servidor.

Si el cliente necesita realizar una llamada a procedimiento remoto mediante un punto de conexión dinámico, el método preferido es realizar la llamada en un identificador de enlace enlazado parcialmente. El tiempo de ejecución de RPC resuelve el punto de conexión de forma transparente. Este método es superior al uso de la [**función RpcEpResolveBinding,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding) ya que permite mecanismos de almacenamiento en caché avanzados en tiempo de ejecución de RPC.

Si se requiere un control más específico sobre la selección de puntos de conexión, los clientes pueden buscar una entrada en el mapa de punto de conexión llamando a las funciones [**RpcMgmtEpEltInqBegin,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin) [**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)y [**RpcMgmtEpEltInqDone.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)

## <a name="exporting-well-known-endpoints-into-the-endpoint-map-database"></a>Exportación de puntos de conexión conocidos a la base de datos de mapa de puntos de conexión

Es posible combinar los dos enfoques para buscar puntos de conexión, especialmente cuando un sistema distribuido está haciendo la transición de un modelo de punto de conexión conocido a un modelo de punto de conexión dinámico. En estas transiciones, una versión intermedia del servidor usará un punto de conexión conocido, pero también registrará el punto de conexión conocido con la base de datos de asignación de puntos de conexión. Este enfoque permite a los clientes que usan un punto de conexión conocido y a los clientes que usan un punto de conexión dinámico conectarse. Una vez actualizados todos los servidores, se puede implementar una nueva versión de cliente que use solo puntos de conexión dinámicos. Una vez actualizados todos los clientes, una versión final del servidor puede dejar de usar puntos de conexión conocidos y empezar a usar solo puntos de conexión dinámicos.

Este enfoque permite una ruta de transición para las aplicaciones que se han iniciado con un punto de conexión conocido pero que desean migrar a un punto de conexión dinámico sin necesidad de una actualización simultánea de todos los servidores y clientes.

 

 