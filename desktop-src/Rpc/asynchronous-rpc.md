---
title: RPC asincrónica
description: Llamada a procedimiento remoto asincrónico (RPC) es una extensión de Microsoft que aborda varias limitaciones del modelo RPC tradicional, tal como se define en Open Software Foundation \ 8211;Distributed Computing Environment (OSF-DCE).
ms.assetid: 2586c10e-8284-419f-a200-4f6b11953688
keywords:
- Llamada a procedimiento remoto RPC , descrita, RPC asincrónica
- RPC asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f4a5f160054f78f0a5737993d1a030957af930ab036e73dbcea0a039125964
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023545"
---
# <a name="asynchronous-rpc"></a>RPC asincrónica

Llamada a procedimiento remoto asincrónico (RPC) es una extensión de Microsoft que aborda varias limitaciones del modelo RPC tradicional, tal como se define en Open Software Foundation–Distributed Computing Environment (OSF-DCE). RPC asincrónica separa una llamada a procedimiento remoto de su valor devuelto, que resuelve las siguientes limitaciones de RPC tradicional y sincrónica:

-   **Varias llamadas pendientes desde un cliente de un solo subproceso.** En el modelo RPC tradicional, un cliente se bloquea en una llamada a procedimiento remoto hasta que se devuelve la llamada. Esto evita que un cliente tenga varias llamadas pendientes, mientras sigue teniendo su subproceso disponible para realizar otro trabajo.
-   **Clientes lentos o retrasados.** Es posible que un cliente con lentitud en la generación de datos quiera realizar una llamada a procedimiento remoto con datos iniciales y, a continuación, proporcionar datos adicionales a medida que se generan. Esto no es posible con RPC convencional (sincrónico).
-   **Servidores lentos o retrasados.** Una llamada a procedimiento remoto que tarda mucho tiempo en completarse vinculará el subproceso de distribución mientras dure la tarea. Con RPC asincrónico, el servidor puede iniciar una operación independiente (asincrónica) para procesar la solicitud y devolver la respuesta cuando esté disponible. El servidor también puede enviar la respuesta de forma incremental a medida que los resultados estén disponibles sin tener que vincular un subproceso de distribución mientras dure la llamada remota. Al hacer que la aplicación cliente sea asincrónica, puede evitar que un servidor lento acote innecesariamente una aplicación cliente.
-   **Transferencia de grandes cantidades de datos.** La transferencia de grandes cantidades de datos entre el cliente y el servidor, especialmente a través de vínculos lentos, vincula tanto el subproceso de cliente como el subproceso del administrador del servidor durante la transferencia. Con RPC y canalizaciones asincrónicas, la transferencia de datos puede realizarse de forma incremental y sin bloquear al cliente o servidor para que realice otras tareas.

Para aprovechar los mecanismos RPC asincrónicos, declare funciones con el \[ [**atributo asincrónico.**](/windows/desktop/Midl/async) \] Dado que realiza esta declaración en un archivo de configuración de atributos (ACF), no tiene que realizar ningún cambio en el archivo del lenguaje de definición de interfaz (IDL); RPC asincrónica no tiene ningún efecto en el protocolo de conexión (cómo se transmiten los datos entre el cliente y el servidor). Esto significa que los clientes sincrónicos y asincrónicos pueden comunicarse con una aplicación de servidor asincrónica.

En esta sección se presenta información general sobre cómo desarrollar aplicaciones distribuidas mediante RPC asincrónica. La información general se presenta en las secciones siguientes:

-   [Declarar funciones asincrónicas](declaring-asynchronous-functions.md)
-   [RPC asincrónica del lado cliente](client-side-asynchronous-rpc.md)
-   [RPC asincrónica del lado servidor](server-side-asynchronous-rpc.md)
-   [Orden causal de las llamadas asincrónicas](causal-ordering-of-asynchronous-calls.md)
-   [Tratamiento de errores](error-handling.md)
-   [RPC asincrónica sobre el protocolo de canalización con nombre](asynchronous-rpc-over-the-named-pipe-protocol.md)
-   [Uso de RPC asincrónico con canalizaciones DCE](using-asynchronous-rpc-with-dce-pipes.md)
-   [DCOM asincrónico](asynchronous-dcom.md)

 

 