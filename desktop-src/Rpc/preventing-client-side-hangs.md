---
title: Impedir bloqueos del cliente
description: Hay dos maneras en las que el cliente puede bloquear la conectividad de red puede provocar que se pierdan las solicitudes del servidor o que el propio servidor pueda bloquearse. Con las opciones predeterminadas, RPC nunca agotará el tiempo de espera de una llamada y el subproceso de cliente esperará indefinidamente una respuesta.
ms.assetid: 2c201e29-9d9c-48e6-b0b5-68e4b25c3fb7
keywords:
- RPC llamada a procedimiento remoto, procedimientos recomendados, impedir bloqueos del cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d4b5fc92ca18b575d081cd7b5abf90929e7df5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791991"
---
# <a name="preventing-client-side-hangs"></a>Impedir bloqueos del cliente

Hay dos maneras en las que el cliente puede bloquearse: la conectividad de red puede provocar que se pierdan las solicitudes del servidor o que el propio servidor pueda bloquearse. Con las opciones predeterminadas, RPC nunca agotará el tiempo de espera de una llamada y el subproceso de cliente esperará indefinidamente una respuesta.

Hay dos métodos para evitar esto: mantener las conexiones activas y tiempos de espera.

## <a name="tcp-keep-alives"></a>Mantenimiento de conexiones TCP

El cliente puede configurarse para hacer ping periódicamente en el servidor para asegurarse de que el servidor está activo y en ejecución. Los pings son conexiones TCP persistentes para las secuencias de protocolo [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) y [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http) y, por tanto, son eficientes en el uso de CPU y el ancho de banda de red. Para habilitar Keep alives en una llamada a procedimiento remoto determinada, use la función [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) antes de que se inicie la llamada. Esta función toma un identificador de enlace y un tiempo de espera como argumentos. Cada llamada a procedimiento remoto en este identificador de enlace después de **RpcMgmtSetComTimeout** utiliza el tiempo de espera proporcionado.

El parámetro timeout de la función [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) especifica cuánto tiempo espera el tiempo de ejecución de RPC antes de activar Keep alives. El tiempo de espera es un valor comprendido entre 0 y 10, donde 0 es el tiempo de espera mínimo y 10 es el tiempo de espera infinito (sin tiempo de espera). El tiempo de espera no está en segundos; la conversión del valor de tiempo de espera proporcionado a la función **RpcMgmtSetComTimeout** en segundos se realiza en el tiempo de ejecución de RPC y es específica de la implementación.

En la tabla siguiente se proporciona la traducción a segundos para Windows 2000 y Windows XP. Las versiones futuras de Windows pueden cambiar la asignación entre el parámetro timeout y el valor de tiempo de espera en segundos:

| Parámetro timeout                       | Tiempo de espera real en segundos |
|-----------------------------------------|----------------------------|
| 0 ( \_ tiempo de \_ espera mínimo de enlace de RPC C \_ \_ )       | 120                        |
| 1                                       | 240                        |
| 2                                       | 360                        |
| 3                                       | 480                        |
| 4                                       | 600                        |
| 5 ( \_ tiempo de \_ espera predeterminado de enlace de RPC C \_ \_ )   | 720                        |
| 6                                       | 840                        |
| 7                                       | 960                        |
| 8                                       | 1080                       |
| 9 ( \_ tiempo de \_ espera máximo de enlace de RPC C \_ \_ )       | 1200                       |
| 10 ( \_ tiempo de \_ espera infinito de enlace de RPC C \_ \_ ) | Tiempo de espera infinito          |



 

Una vez que se activan las conexiones de mantenimiento, el cliente envía un paquete de mantenimiento de conexión cada segundo. Si no hay ninguna confirmación del servidor durante tres o más conexiones Keep Alive, el cliente declara la conexión muerta y produce un error en la llamada a procedimiento remoto. Si el servidor envía una respuesta dentro del tiempo de espera especificado, las conexiones Keep Alive no se activarán. Si el servidor responde a Keep alives, pero no responde a la llamada a procedimiento remoto, el cliente continúa enviando las conexiones de mantenimiento. Una vez que el servidor responde a la llamada RPC, las conexiones persistentes están desactivadas. En Windows 2000, Keep alives solo se activa para las llamadas RPC sincrónicas. En Windows XP, mantener las conexiones activas también se activan para las llamadas RPC asincrónicas.

Es tentador establecer Keep alives en el valor más bajo para asegurarse de que la aplicación cliente responde a los problemas de la red de manera puntual. Se debe tener en cuenta el cuidado y el escrutinio aplicados a si se garantiza un valor agresivo. Un servidor que pierde temporalmente la conectividad se puede desbordar con mantener conexiones de varios clientes una vez que se restaure la conectividad. Además, las tareas de cálculo largas pueden tardar más de dos minutos, y el servidor puede que se encuentre en un tiempo mayor que la respuesta a la espera de tiempo de CPU que la realización de un trabajo útil. Por lo tanto, las conexiones Keep Alive deben usarse con moderación. Si el cliente no puede tolerar que el subproceso se esté enlazando durante períodos largos, se debe tener en cuenta la RPC asincrónica.

Otras secuencias de protocolos pueden implementar mecanismos diferentes para detectar servidores que no responden, en función del transporte que se utilice. El transporte [**ncalrpc**](/windows/desktop/Midl/ncalrpc) no usa Keep alives. Dado que todas las comunicaciones de **ncalrpc** son locales, si el servidor deja de responder mientras se está realizando una llamada, el tiempo de ejecución de RPC en el cliente produce un error inmediato en la llamada.

## <a name="call-time-outs"></a>Tiempo de espera de llamadas

TCP Keep alives está bien si se pierde la conectividad de red o si se bloquea el servidor. Pero si el servidor se bloquea en modo de usuario, TCP Keep alives se devuelve correctamente, pero la llamada nunca devolverá. Para tratar este escenario, se ha agregado una nueva opción en tiempo de ejecución para Windows XP: \_ tiempo de espera de llamada de RPC C \_ OPT \_ \_ . Esta opción indica al tiempo de ejecución de RPC que configure un temporizador cada vez que envíe una solicitud al servidor. Si el temporizador expira, la llamada se cancela automáticamente y se completa con la llamada de \_ RPC \_ S \_ cancelada. Siempre que el servidor responda dentro del límite de tiempo especificado, el cliente no cancelará la llamada. Esto significa que una llamada de varios fragmentos puede tardar más que el tiempo de espera para completarse, ya que cada respuesta del servidor se recibe dentro del período de tiempo de espera, aunque el período de tiempo para que lleguen todas las respuestas supera el período de tiempo de espera.

Además, cuando se cancela una llamada, el servidor no recibe una notificación de la cancelación. Por lo tanto, el servidor probablemente ejecutará la llamada en algún momento y el cliente simplemente omitirá la respuesta del servidor.

La dificultad más peligrosa con el tiempo de espera de la llamada es establecer un tiempo de espera corto y volver a intentar la llamada en el mismo servidor. En el escenario siguiente se muestran los peligros de este enfoque:

Imagine un servidor que funciona cerca de su capacidad. Tiene varios clientes con tiempos de espera muy cortos, como cinco segundos. Una pérdida temporal de la conectividad de red o la congestión en un enrutador produce una interrupción en las respuestas del servidor durante unos segundos. En redes Ethernet, esta situación se puede deber fácilmente a una ráfaga de actividad en un vínculo que el servidor comparte con otro equipo. El servidor no administra para enviar todas las respuestas antes de que se agote el tiempo de espera de cinco segundos. Los clientes obtienen sus llamadas canceladas e intentan de inmediato. El servidor no es consciente de que las llamadas son reintentos y las ejecuta también. Por lo tanto, en lugar de ejecutar su carga de trabajo normal de llamadas, ejecuta 30-50% más llamadas, dependiendo de cuántos clientes hayan agotado el tiempo de espera. Si esto supera su capacidad y el servidor no puede responder a todos los clientes en un plazo de cinco segundos, se envía otra ronda de llamadas al servidor. Los clientes siguen reemitiendo las mismas llamadas y, dado que el servidor está sobrecargado en el procesamiento de llamadas anteriores, no puede responder dentro del tiempo de espera. Una vez que responde, los clientes han alcanzado el tiempo de espera, ha emitido una nueva llamada y descartado la respuesta. En el peor de los casos, el servidor no se recuperará hasta que se reinicie y, según el patrón de acceso de cliente, no se pueda recuperar hasta que se detenga un número suficiente de clientes.

> [!Note]  
> Los tiempos de espera de la llamada solo funcionan en las secuencias de protocolo [**\_ \_ TCP IP ncacn**](/windows/desktop/Midl/ncacn-ip-tcp) y [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http) .

 

 

 