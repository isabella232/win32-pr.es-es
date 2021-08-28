---
title: Especificar puntos de conexión
description: Especificar puntos de conexión conocidos y dinámicos en llamada a procedimiento remoto (RPC).
ms.assetid: fc39b527-11e6-45a7-b3b5-8bcf469633d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff73f13f752e42917353a217f5a2fcfa8d1fcfa9dc60edf585c42d72b0d306e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017615"
---
# <a name="specifying-endpoints"></a>Especificar puntos de conexión

Un punto de conexión es una dirección específica de la red de un proceso de servidor para las llamadas a procedimiento remoto. El nombre real del punto de conexión depende de la secuencia de protocolo usada. Por ejemplo, TCP, UDP y HTTP usan puertos. Las canalizaciones con nombre usan un nombre de canalización con nombre. Las aplicaciones cliente/servidor pueden usar un punto de conexión conocido o un punto de conexión dinámico. En esta sección se presentan las técnicas que usan los programas de servidor para especificar puntos de conexión conocidos y dinámicos. La información se describe en los temas siguientes:

-   [Especificar puntos de conexión conocidos](#specifying-well-known-endpoints)
-   [Especificar puntos de conexión dinámicos](#specifying-dynamic-endpoints)

## <a name="specifying-well-known-endpoints"></a>Especificar puntos de conexión conocidos

Cuando el servidor usa un punto de conexión conocido, puede incluir los datos del punto de conexión como parte de su entrada de base de datos de servicio de nombre. Si lo hace, el identificador de enlace del cliente contiene una dirección de servidor completa que incluye el punto de conexión conocido cuando el cliente importa el identificador de enlace de la entrada del servidor.

El programa de servidor también puede especificar puntos de conexión conocidos al mismo tiempo que especifica secuencias de protocolo. Invoque [**la función RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) o [**RpcServerUseProtseqEpEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) La diferencia entre ambos es que la última función tiene un parámetro adicional que el servidor puede usar para controlar la asignación dinámica de puertos.

Si el programa de servidor especifica su información de punto de conexión de esta manera, también debe llamar a la [**función RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) para registrar el punto de conexión en la asignación del punto de conexión. Aunque el punto de conexión siempre es el mismo, el cliente puede usar la asignación de punto de conexión para buscar el servidor.

Al igual que las secuencias de protocolo, una aplicación puede especificar información de punto de conexión en su archivo IDL. Cuando lo haga, debe registrar las secuencias de protocolo y los puntos de conexión al mismo tiempo invocando la función [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) o [**RpcServerUseAllProtseqsIfEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) En este caso, el cliente tiene acceso a la información del punto de conexión a través de la especificación de interfaz en el archivo IDL. Por lo tanto, no es necesario llamar a la [**función RpcEpRegister.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)

## <a name="specifying-dynamic-endpoints"></a>Especificar puntos de conexión dinámicos

Un punto de conexión dinámico es un punto de conexión que el equipo host del servidor asigna cuando el servidor comienza la ejecución. La mayoría de las aplicaciones de servidor usan puntos de conexión dinámicos para evitar conflictos con otros programas a través del número limitado de puertos que están disponibles en el sistema del equipo host del servidor. Sin embargo, los programas que usan canalizaciones con nombre o la secuencia del protocolo [**ncalrpc**](/windows/desktop/Midl/ncalrpc) tienen un espacio de nombres de punto de conexión muy grande. Se benefician menos de los puntos de conexión dinámicos que los programas que usan otros transportes.

Los programas de servidor registran puntos de conexión dinámicos en una base de datos de mapa de puntos de conexión. Si desea que el servidor use cualquier punto de conexión disponible, llame a [**RpcServerUseAllProtSeqs,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) [**RpcServerUseAllProtseqsEx,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex) [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) o [**RpcServerUseProtseqEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) Esto establece la biblioteca en tiempo de ejecución de RPC para usar todas o una secuencias de protocolo válidas con puntos de conexión dinámicos. A continuación, el servidor debe llamar a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) para obtener un conjunto de identificadores de enlace válidos. El servidor pasa el conjunto de identificadores de enlace, o vector de enlace, a la función [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) para registrar todos los puntos de conexión adecuados en el mapa de puntos de conexión. Para cada llamada que el servidor realiza a **RpcEpRegister**, debe haber una llamada correspondiente a [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) para liberar la memoria que usa el vector de enlace.

Tenga en cuenta que los programas de servidor pueden usar [**la función RpcEpRegisterNoReplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace) en lugar [**de RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister). Los programas suelen **usar RpcEpRegisterNoReplace** cuando se deben ejecutar varias copias de un programa de servidor en un sistema host de servidor.

Las [**funciones RpcEpRegister y**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) [**RpcEpRegisterNoReplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace) agregan las interfaces del servidor y los identificadores de enlace a la base de datos del asignador de puntos de conexión. Cuando el cliente realiza una llamada a procedimiento remoto mediante un identificador enlazado parcialmente, la biblioteca en tiempo de ejecución del cliente solicita al asignador de puntos de conexión del equipo servidor el punto de conexión de una instancia de servidor compatible. La biblioteca cliente proporciona el UUID de interfaz, la secuencia de protocolo y, si está presente, el UUID del objeto en el identificador de enlace de cliente. El asignador de puntos de conexión busca una entrada de base de datos que coincida con la información del cliente. El UUID de la interfaz cliente/servidor, la versión principal de la interfaz y la secuencia de protocolo deben coincidir exactamente. Además, la versión secundaria de la interfaz del servidor debe ser mayor o igual que la versión secundaria del cliente.

Si todas las pruebas se realizan correctamente, el asignador de puntos de conexión devuelve el punto de conexión válido y la biblioteca en tiempo de ejecución del cliente actualiza el punto de conexión en el identificador de enlace.

Los puntos de conexión dinámicos se purgan automáticamente de la base de datos del asignador de puntos de conexión cuando el proceso de servidor deja de ejecutarse. Puede quitar el punto de conexión de la base de datos del asignador de puntos de conexión antes de que el programa de servidor salga mediante la [**función RpcEpUnregister,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepunregister) o bien puede permitir la limpieza automática para administrar la eliminación del punto de conexión.

 

 