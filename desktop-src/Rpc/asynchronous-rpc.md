---
title: RPC asincrónico
description: La llamada a procedimiento remoto (RPC) asincrónica es una extensión de Microsoft que aborda varias limitaciones del modelo RPC tradicional, tal como se define en el entorno de computación distribuida de Open Software Foundation \ 8211; (OSF-DCE).
ms.assetid: 2586c10e-8284-419f-a200-4f6b11953688
keywords:
- RPC llamada a procedimiento remoto, descripción, RPC asincrónico
- RPC asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ac79a30fd01aeba1efb3cbd2b7cc741f26238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149517"
---
# <a name="asynchronous-rpc"></a>RPC asincrónico

La llamada a procedimiento remoto (RPC) asincrónica es una extensión de Microsoft que aborda varias limitaciones del modelo RPC tradicional, tal como se define en Open Software Foundation – Distributed Computing Environment (OSF-DCE). RPC asincrónico separa una llamada a procedimiento remoto de su valor devuelto, que resuelve las siguientes limitaciones del RPC sincrónico tradicional:

-   **Varias llamadas pendientes desde un cliente de un solo subproceso.** En el modelo RPC tradicional, un cliente se bloquea en una llamada a procedimiento remoto hasta que se devuelve la llamada. Esto impide que un cliente tenga varias llamadas pendientes, mientras que el subproceso sigue estando disponible para realizar otro trabajo.
-   **Clientes lentos o retrasados.** Un cliente que es lento para generar datos puede querer realizar una llamada a procedimiento remoto con los datos iniciales y, a continuación, proporcionar datos adicionales a medida que se generan. Esto no es posible con RPC (sincrónico) convencional.
-   **Servidores lentos o retrasados.** Una llamada a procedimiento remoto que tarda mucho tiempo en completarse enlazará el subproceso de envío mientras dure la tarea. Con RPC asincrónico, el servidor puede iniciar una operación independiente (asincrónica) para procesar la solicitud y devolver la respuesta cuando esté disponible. El servidor también puede enviar la respuesta de forma incremental a medida que los resultados estén disponibles sin tener que asociar un subproceso de envío mientras dure la llamada remota. Al hacer que la aplicación cliente sea asincrónica, puede evitar que un servidor lento se quede innecesariamente a través de una aplicación cliente.
-   **Transferencia de grandes cantidades de datos.** La transferencia de grandes cantidades de datos entre el cliente y el servidor, especialmente a través de vínculos de baja velocidad, une el subproceso de cliente y el subproceso del administrador del servidor durante la transferencia. Con RPC y canalizaciones asincrónicas, la transferencia de datos se puede realizar de forma incremental y sin impedir que el cliente o el servidor realice otras tareas.

Puede aprovechar los mecanismos RPC asincrónicos mediante la declaración de funciones con el \[ atributo [**Async**](/windows/desktop/Midl/async) \] . Dado que esta declaración se realiza en un archivo de configuración de atributos (ACF), no es necesario realizar ningún cambio en el archivo de lenguaje de definición de interfaz (IDL); RPC asincrónico no tiene ningún efecto en el protocolo de conexión (cómo se transmiten los datos entre el cliente y el servidor). Esto significa que los clientes sincrónicos y asincrónicos pueden comunicarse con una aplicación de servidor asincrónica.

En esta sección se ofrece información general sobre cómo desarrollar aplicaciones distribuidas mediante RPC asincrónico. La información general se presenta en las siguientes secciones:

-   [Declarar funciones asincrónicas](declaring-asynchronous-functions.md)
-   [RPC asincrónica del lado cliente](client-side-asynchronous-rpc.md)
-   [RPC asincrónica del lado servidor](server-side-asynchronous-rpc.md)
-   [Ordenación causal de llamadas asincrónicas](causal-ordering-of-asynchronous-calls.md)
-   [Tratamiento de errores](error-handling.md)
-   [RPC asincrónico a través del Protocolo de canalización con nombre](asynchronous-rpc-over-the-named-pipe-protocol.md)
-   [Usar RPC asincrónico con canalizaciones de DCE](using-asynchronous-rpc-with-dce-pipes.md)
-   [DCOM asincrónico](asynchronous-dcom.md)

 

 