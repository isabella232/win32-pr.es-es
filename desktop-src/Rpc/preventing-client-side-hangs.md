---
title: Evitar que se resalte el lado cliente
description: Hay dos maneras en que el cliente puede bloquear la conectividad de red puede hacer que se pierdan las solicitudes del servidor o que el propio servidor se pueda bloquear. Con las opciones predeterminadas, RPC nunca tiempo de espera de una llamada y el subproceso de cliente esperará indefinidamente una respuesta.
ms.assetid: 2c201e29-9d9c-48e6-b0b5-68e4b25c3fb7
keywords:
- Llamada a procedimiento remoto RPC, procedimientos recomendados, evitar que el cliente se ahorca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da79573e59e30c58a7c236b35293b678c93dde6bf999b477de054d6f3c62971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927301"
---
# <a name="preventing-client-side-hangs"></a>Evitar que se resalte el lado cliente

Hay dos maneras en que el cliente puede bloquearse: la conectividad de red puede hacer que se pierdan las solicitudes del servidor o que el propio servidor se pueda bloquear. Con las opciones predeterminadas, RPC nunca tiempo de espera de una llamada y el subproceso de cliente esperará indefinidamente una respuesta.

Hay dos métodos para evitarlo: mantener los tiempos de vida y los tiempos de espera.

## <a name="tcp-keep-alives"></a>TCP Keep Alives

El cliente se puede configurar para hacer ping periódicamente al servidor para asegurarse de que el servidor está activo y en ejecución. Los pings son secuencias tcp keep-alive para las secuencias de protocolo http [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) y [**ncacn \_**](/windows/desktop/Midl/ncacn-http) y, por lo tanto, son eficaces en el uso de la CPU y el ancho de banda de red. Para habilitar keep alives en una llamada de procedimiento remoto determinada, use la [**función RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) antes de iniciar la llamada. Esta función toma un identificador de enlace y un tiempo de espera como argumentos. Cada llamada a procedimiento remoto en este identificador de enlace después **de RpcMgmtSetComTimeout** usa el tiempo de espera proporcionado.

El parámetro Timeout de la [**función RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) especifica cuánto tiempo espera el tiempo de ejecución de RPC antes de que se activa keep alives. El tiempo de espera es un valor entre 0 y 10, donde 0 es el tiempo de espera mínimo y 10 es tiempo de espera infinito (sin tiempo de espera). El tiempo de espera en sí no es en segundos; La traducción del valor de tiempo de espera proporcionado a la función **RpcMgmtSetComTimeout** en segundos la realiza el tiempo de ejecución de RPC y es específica de la implementación.

En la tabla siguiente se proporciona la traducción a segundos para Windows 2000 y Windows XP. Las versiones futuras Windows pueden cambiar la asignación entre el parámetro Timeout y el valor de tiempo de espera en segundos:

| Parámetro timeout                       | Tiempo de espera real en segundos |
|-----------------------------------------|----------------------------|
| 0 (TIEMPO DE \_ ESPERA MÍNIMO DE ENLACE RPC \_ \_ \_ C)       | 120                        |
| 1                                       | 240                        |
| 2                                       | 360                        |
| 3                                       | 480                        |
| 4                                       | 600                        |
| 5 (TIEMPO DE \_ ESPERA PREDETERMINADO DEL ENLACE RPC \_ \_ \_ C)   | 720                        |
| 6                                       | 840                        |
| 7                                       | 960                        |
| 8                                       | 1080                       |
| 9 (TIEMPO DE \_ ESPERA MÁXIMO DEL ENLACE RPC \_ \_ \_ C)       | 1200                       |
| 10 (TIEMPO DE \_ ESPERA INFINITO DE ENLACE RPC \_ \_ \_ C) | Tiempo de espera infinito          |



 

Una vez que se han activado las conexiones continuas, el cliente envía un paquete keep alive cada segundo. Si no hay ninguna confirmación del servidor para tres o más keep alives, el cliente declara la conexión fallada y produce un error en la llamada al procedimiento remoto. Si el servidor envía una respuesta dentro del tiempo de espera especificado, no se activa keep alives. Si el servidor responde a las conexiones continuas, pero no responde a la llamada a procedimiento remoto, el cliente continúa enviando mensajes keep alives. Una vez que el servidor responde a la llamada RPC, se desactivarán las conexiones continuas. Para Windows 2000, las operaciones keep alive solo se activadas para las llamadas RPC sincrónicas. Para Windows XP, las llamadas RPC asincrónicas también están activadas.

Es tentador establecer keep alives en el valor más bajo para asegurarse de que la aplicación cliente responde a los problemas de red de forma oportuna. Se debe tener en cuenta detenidamente este tipo de tentación y aplicar el examen a si se garantiza un valor agresivo. Un servidor que pierde temporalmente la conectividad puede encontrarse desbordado por las alertas de varios clientes una vez restaurada la conectividad. Además, las tareas de cálculo largas pueden tardar más de dos minutos y es posible que el servidor deba dedicar más tiempo a la CPU a responder a las operaciones de mantenimiento que a realizar un trabajo útil. Por lo tanto, se debe usar keep alives con moderación. Si el cliente no puede tolerar que su subproceso esté vinculado durante largos períodos, se debe tener en cuenta rpc asincrónica.

Otras secuencias de protocolo pueden implementar diferentes mecanismos para detectar servidores que no responden, en función del transporte que se utilice. El [**transporte ncalrpc**](/windows/desktop/Midl/ncalrpc) no usa keep alives. Puesto que todas las comunicaciones de **ncalrpc** son locales, si el servidor deja de responder mientras hay una llamada en curso, el tiempo de ejecución rpc en el cliente produce un error inmediato en la llamada.

## <a name="call-time-outs"></a>Tiempos de espera de llamada

Las conexiones TCP están bien si se pierde la conectividad de red o si el servidor se bloquea. Sin embargo, si el servidor se interbloquea en modo de usuario, los tcps mantienen activo el resultado correctamente, pero la llamada nunca se devolverá. Para tratar con este escenario, se agregó una nueva opción en tiempo de ejecución para Windows XP: RPC \_ C \_ OPT CALL \_ \_ TIMEOUT. Esta opción indica al tiempo de ejecución de RPC que configure un temporizador cada vez que envía una solicitud al servidor. Si el temporizador expira, la llamada se cancela automáticamente y se completa con RPC \_ S \_ CALL \_ CANCELLED. Siempre que el servidor responda dentro del límite de tiempo especificado, el cliente no cancelará la llamada. Esto significa que una llamada a variosfragmentos puede tardar más que el período de tiempo de espera en completarse, ya que cada respuesta del servidor se recibe dentro del período de tiempo de espera, aunque el período de tiempo de espera para que todas las respuestas lleguen sea superior al período de tiempo de espera.

Además, cuando se cancela una llamada, el servidor no se notifica de la cancelación. Por lo tanto, el servidor probablemente ejecutará la llamada en algún momento y el cliente simplemente omitirá la respuesta del servidor.

El problema más peligroso con tiempos de espera de llamada es establecer un tiempo de espera corto y volver a intentar la llamada en el mismo servidor. En el siguiente escenario se ilustran los riesgos de este enfoque:

Imagine un servidor que funciona cerca de la capacidad. Tiene una serie de clientes con tiempos de espera muy cortos, como cinco segundos. Una pérdida temporal de conectividad de red o congestión en un enrutador provoca un error en las respuestas del servidor durante unos segundos. En redes Ethernet, esta situación puede deberse fácilmente a una ráfaga de actividad en un vínculo que el servidor comparte con otra máquina. El servidor no consigue enviar todas las respuestas antes del tiempo de espera de cinco segundos. Los clientes cancelan sus llamadas y lo reintenten inmediatamente. El servidor no es consciente de que las llamadas son reintentos y también las ejecuta. Por lo tanto, en lugar de ejecutar su carga de trabajo normal de llamadas, ejecuta entre un 30 y un 50 % más de llamadas, en función del número de clientes que se han pasado por alto. Si esto supera su capacidad y el servidor no puede responder a todos los clientes en un plazo de cinco segundos, se envía otra ronda de llamadas al servidor. Los clientes siguen reeditando las mismas llamadas y, dado que el servidor está sobrecargado procesando llamadas anteriores, no puede responder dentro del tiempo de espera. Una vez que responde, los clientes han alcanzado el tiempo de espera, han emitido una nueva llamada y han descartado la respuesta. En el peor de los casos, el servidor no se recuperará hasta el reinicio y, según el patrón de acceso de cliente, puede que no se recupere hasta que se detenga un número suficiente de clientes.

> [!Note]  
> Los tiempos de espera de llamada solo funcionan en las secuencias de [**protocolo http ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) y [**ncacn. \_**](/windows/desktop/Midl/ncacn-http)

 

 

 