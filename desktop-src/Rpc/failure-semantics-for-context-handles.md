---
title: Semántica de errores para identificadores de contexto
description: En este tema se describe la semántica de errores para los identificadores de contexto.
ms.assetid: fcf28519-39ad-4823-bc27-f3502e4d540c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4528b3f5160b92a4e6f10dbcf877e9fec59f81b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361953"
---
# <a name="failure-semantics-for-context-handles"></a>Semántica de errores para identificadores de contexto

En este tema se describe la semántica de errores para los identificadores de contexto.

## <a name="failure-semantics-when-closing-the-context-handle-fails"></a>Se produce un error en la semántica cuando se produce un error al cerrar el identificador de contexto

Imagine una aplicación cliente está intentando cerrar un identificador de contexto que se abre en el servidor, sin cerrar el proceso de cliente. Además, suponga que se produce un error en la llamada al servidor para cerrar el identificador de contexto (por ejemplo, el cliente está sin memoria). La manera adecuada de controlar esta situación es llamar a la [**función RpcSsDestroyClientContext.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) En tal caso, el cliente limpia su lado del identificador de contexto y cierra abortivamente la conexión al servidor. Puesto que la conexión es realmente un grupo de conexiones (vea [RPC](rpc-and-the-network.md)y la red ), que se cuenta con una referencia para cada enlace abierto o identificador de contexto, destruir el identificador de contexto mediante una llamada a la función **RpcSsDestroyClientContext** no destruye realmente la conexión. En su lugar, disminuye el recuento de referencias para el grupo de conexiones. Para que se cierren las conexiones del grupo, el cliente debe cerrar todos los identificadores de enlace y de contexto a ese servidor desde el proceso de cliente. A continuación, se cierran todas las conexiones del grupo y se inicia y limpia el mecanismo de ejecución del servidor.

## <a name="failure-semantics-during-change-of-state-of-the-context-handle"></a>Semántica de errores durante el cambio de estado del identificador de contexto

La información de esta sección hace referencia a Windows XP y plataformas posteriores.

Los identificadores de contexto son simplemente parámetros de una función. Todos los cambios en el estado de un identificador de contexto se suceden cuando se serializan o desmarshaled los parámetros. Por ejemplo, si un cliente abre un identificador de contexto (lo cambia de **NULL** a no **NULL),** el tiempo de ejecución de RPC no abre realmente la parte RPC del identificador hasta que se serializan los argumentos para enviarlos al cliente. Los errores pueden producirse durante el período de tiempo. Debido a una variedad de posibles condiciones de red o de recursos bajos, la transmisión del paquete al cliente podría producir un error. O bien, la rutina de servidor puede producir una excepción al intentar cambiar un identificador de contexto. En estas u otras situaciones de error, el cliente y el servidor pueden obtener vistas incoherentes del identificador de contexto. En esta sección se explica la regla para el estado del identificador de contexto y la responsabilidad del código de cliente y servidor durante varias condiciones de error.

-   Llega **un** identificador de contexto NULL, pero la rutina de servidor encuentra un error y produce una excepción.

    Es responsabilidad de la rutina del servidor limpiar cualquier estado relacionado con el identificador de contexto que pueda haber creado. El tiempo de ejecución de RPC limpia su estado.

-   Llega un identificador de contexto que no es **NULL,** pero la rutina de servidor encuentra un error y produce una excepción.

    Si la rutina de servidor cerró el identificador de contexto, el cliente no lo sabrá, ya que la llamada no se realizará correctamente. El uso adicional del identificador de contexto dará lugar a un error DE COINCIDENCIA DE CONTEXTO de SS DE RPC \_ X \_ en el \_ \_ cliente. Si la rutina de servidor no modifica el identificador de contexto, el cliente todavía puede usarlo. Si la rutina del servidor cambia la información almacenada en el contexto del servidor, las nuevas llamadas del cliente usarán esa información.

-   Llega un identificador de contexto que no es **NULL** y la rutina de servidor cierra el identificador, pero no se pudo calcular la serialización después de calcular las referencias del identificador de contexto, o bien el procesamiento después del error de serialización.

    El identificador de contexto está cerrado y las llamadas lejos de este cliente que usan este identificador de contexto producirán un error DE MISMATCH DE CONTEXTO de SS de RPC \_ X \_ en el \_ \_ cliente.

-   Llega **un identificador** de contexto NULL y el servidor crea su contexto para este identificador, pero no se pudo calcular la serialización después de calcular las referencias del identificador de contexto, o bien el procesamiento después de un error de serialización.

    En este caso, el tiempo de ejecución de RPC invoca la ejecución para este identificador de contexto y limpia el estado rpc para este identificador de contexto. El identificador de contexto no se creará en el lado cliente.

-   Llega un identificador de contexto que no es **NULL** y el servidor no cambia el identificador de contexto o cambia la información almacenada en el contexto del servidor y se produce un error en la serialización después de serializar el identificador de contexto.

    Las nuevas llamadas del cliente usarán el identificador de contexto que tiene el servidor.

-   Llega **un** identificador de contexto NULL y el servidor no lo establece en nada distinto de **NULL,** pero se produce un error en la llamada antes de serializar el identificador de contexto.

    En este caso, no se crea ningún identificador de contexto en el cliente.

-   Llega un **identificador de** contexto que no es NULL y el servidor lo establece en **NULL,** pero se produce un error en la serialización antes de serializar el identificador de contexto.

    En este caso, el identificador de contexto permanece cerrado en el servidor y el cliente obtiene errores DE MISMATCH DE CONTEXTO de SS de RPC X cuando intenta usar \_ \_ el identificador de \_ \_ contexto.

-   Un **identificador** de contexto NULL llega al servidor y el servidor lo establece en distinto de **NULL,** pero se produce un error en la serialización antes de serializar el identificador de contexto.

    El controlador de contexto se debe invocar para que el servidor pueda limpiarse y no se creará ningún identificador de contexto en el cliente.

-   Llega un identificador de contexto que no es **NULL** y el servidor no cambia el identificador de contexto o cambia la información almacenada en el contexto del servidor y se produce un error en la serialización antes de serializar el identificador de contexto.

    Las nuevas llamadas del cliente usarán el estado en el servidor.

-   Un identificador de contexto se declara como un valor devuelto y la rutina de servidor devuelve **NULL** para el identificador de contexto y se produce un error de serialización antes de serializar el identificador de contexto.

    En este caso, no se crea ningún contexto nuevo en el cliente.

-   Un identificador de contexto se declara como un valor devuelto y la rutina de servidor devuelve un valor distinto de **NULL** para el identificador de contexto y se produce un error de serialización antes de serializar el identificador de contexto.

    El tiempo de ejecución de RPC llama a la rutina de ejecución del identificador de contexto para darle la oportunidad de limpiar y no se crea ningún contexto nuevo en el cliente.

 

 




