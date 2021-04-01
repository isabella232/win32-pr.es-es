---
title: Semántica de errores para los identificadores de contexto
description: En este tema se describe la semántica de errores para los identificadores de contexto.
ms.assetid: fcf28519-39ad-4823-bc27-f3502e4d540c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4528b3f5160b92a4e6f10dbcf877e9fec59f81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075785"
---
# <a name="failure-semantics-for-context-handles"></a>Semántica de errores para los identificadores de contexto

En este tema se describe la semántica de errores para los identificadores de contexto.

## <a name="failure-semantics-when-closing-the-context-handle-fails"></a>Se produce un error en la semántica de errores al cerrar el identificador de contexto

Imagine que una aplicación cliente está intentando cerrar un identificador de contexto abierto en el servidor sin cerrar el proceso de cliente. Además, supongamos que se produce un error en la llamada al servidor para cerrar el identificador de contexto (por ejemplo, el cliente no tiene memoria suficiente). La manera adecuada de controlar esta situación es llamar a la función [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) . En tal caso, el cliente limpia su lado del identificador de contexto y abortively cierra la conexión al servidor. Dado que la conexión es realmente un grupo de conexiones (vea [RPC y la red](rpc-and-the-network.md)), que se cuenta con una referencia para cada identificador de enlace o contexto abierto, la destrucción del identificador de contexto mediante una llamada a la función **RpcSsDestroyClientContext** no destruye realmente la conexión. En su lugar, disminuye el recuento de referencias del grupo de conexiones. En el caso de las conexiones del grupo que se van a cerrar, el cliente debe cerrar todos los identificadores de enlace y los identificadores de contexto para ese servidor desde el proceso del cliente. A continuación, se cierran todas las conexiones del grupo y se inicia el mecanismo de ejecución del servidor y se limpia.

## <a name="failure-semantics-during-change-of-state-of-the-context-handle"></a>Semántica de errores durante el cambio de estado del identificador de contexto

La información de esta sección se refiere a Windows XP y plataformas posteriores.

Los identificadores de contexto son simplemente parámetros para una función. Todos los cambios en el estado de un identificador de contexto se producen cuando se calculan las referencias de los parámetros o se anula su serialización. Por ejemplo, si un cliente abre un identificador de contexto (lo cambia de **null** a un **valor** distinto de NULL), el tiempo de ejecución de RPC no abre realmente la parte de RPC del identificador hasta que se calculan las referencias de los argumentos para enviarlos al cliente. Los errores se pueden producir durante el tiempo provisional. Debido a una serie de condiciones de red o de recursos insuficientes posibles, se podría producir un error en la transmisión del paquete al cliente. O la rutina del servidor puede producir una excepción al intentar cambiar un identificador de contexto. En estas situaciones de error, el cliente y el servidor pueden obtener vistas incoherentes del identificador de contexto. En esta sección se explica la regla para el estado del identificador de contexto y la responsabilidad del código de cliente y servidor durante varias condiciones de error.

-   Llega un identificador de contexto **nulo** , pero la rutina de servidor encuentra un error y produce una excepción.

    Es responsabilidad de la rutina del servidor limpiar cualquier estado relacionado con el identificador de contexto que haya creado. El tiempo de ejecución de RPC limpia su estado.

-   Los identificadores de contexto que no son **null** llegan, pero la rutina de servidor encuentra un error y produce una excepción.

    Si la rutina de servidor cerró el identificador de contexto, el cliente no lo sabrá, ya que la llamada no se realizará correctamente. el uso adicional del identificador de contexto producirá un error de falta de coincidencia de contexto de RPC \_ X \_ SS \_ \_ en el cliente. Si la rutina del servidor no modifica el identificador de contexto, el cliente todavía puede usarlo. Si la rutina del servidor cambia la información almacenada en el contexto del servidor, las nuevas llamadas del cliente usarán esa información.

-   Llega un identificador de contexto que no **es null** y la rutina de servidor cierra el identificador, pero se ha producido un error en el cálculo de referencias después del identificador de contexto, o bien el procesamiento después del cálculo de referencias.

    El identificador de contexto está cerrado y otras llamadas realizadas por este cliente con este identificador de contexto provocan \_ un \_ error de falta de coincidencia de contexto de RPC X SS \_ \_ en el cliente.

-   Llega un identificador de contexto **nulo** y el servidor crea su contexto para este identificador, pero se ha producido un error en el cálculo de referencias después del identificador de contexto o el procesamiento después del cálculo de referencias.

    En este caso, el tiempo de ejecución de RPC invoca el estado de ejecución para este identificador de contexto y limpia el estado de RPC para este identificador de contexto. El identificador de contexto no se creará en el lado cliente.

-   Llega un identificador de contexto que no **es null** y el servidor no cambia el identificador de contexto, o bien cambia la información almacenada en el contexto del servidor y se produce un error en el cálculo de referencias después de calcular las referencias del identificador de contexto.

    Las nuevas llamadas del cliente usarán el identificador de contexto que tenga el servidor.

-   Llega un identificador de contexto **nulo** y el servidor no lo establece en un valor distinto de **null**, pero se produce un error en la llamada antes de que se calculen las referencias del identificador de contexto.

    En este caso, no se crea ningún identificador de contexto en el cliente.

-   Llega un identificador de contexto que no **es null** y el servidor lo establece en **null**, pero se produce un error en el cálculo de referencias antes de que se calculen las referencias del identificador de contexto.

    En este caso, el identificador de contexto permanece cerrado en el servidor y el cliente obtiene errores de falta de coincidencia de contexto de RPC \_ X \_ SS \_ \_ al intentar usar el identificador de contexto.

-   Un identificador de contexto **nulo** llega al servidor y el servidor lo establece en un valor distinto de **null**, pero se produce un error en el cálculo de referencias antes de que se calculen las referencias del identificador de contexto.

    Se debe invocar la ejecución del identificador de contexto para que el servidor pueda realizar la limpieza, y no se creará ningún identificador de contexto en el cliente.

-   Llega un identificador de contexto que no **es null** y el servidor no cambia el identificador de contexto, o bien cambia la información almacenada en el contexto del servidor, y se produce un error en el cálculo de referencias antes de que se calculen las referencias del identificador de contexto.

    Las nuevas llamadas del cliente usarán el estado en el servidor.

-   Un identificador de contexto se declara como un valor devuelto y la rutina del servidor devuelve **null** para el identificador de contexto y se produce un error en el cálculo de referencias antes de que se calculen las referencias del identificador de contexto.

    En este caso, no se crea ningún contexto nuevo en el cliente.

-   Un identificador de contexto se declara como un valor devuelto y la rutina del servidor devuelve un valor distinto de **null** para el identificador de contexto y se produce un error en el cálculo de referencias antes de que se calculen las referencias del identificador de contexto.

    El tiempo de ejecución de RPC llama a la rutina de ejecución del identificador de contexto para darle la oportunidad de limpiar y no se crea ningún contexto nuevo en el cliente.

 

 




