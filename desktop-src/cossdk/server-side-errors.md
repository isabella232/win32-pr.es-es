---
description: Server-Side errores
ms.assetid: ce8ddb52-237c-4d46-a088-9f592afadcd2
title: Server-Side errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1522f1e4ca07a1a2bfc17273b331a7beb3efc67a8c3f9a90e925161949f694ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793435"
---
# <a name="server-side-errors"></a>Server-Side errores

El agente de escucha y el reproductor trabajan juntos para tratar los mensajes dudosos. Si se produce un error en una transacción que se está reproduciendo, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) vuelve a mover el mensaje de entrada a la cola de entrada. El reproductor anula la transacción si recibe un HRESULT con error del componente de servidor o si detecta una excepción. Si el problema persiste, el agente de escucha podría recorrer continuamente el siguiente patrón:

-   Quita de la cola el mensaje.
-   Crea instancias del objeto
-   Sufre una reversión
-   Vuelve a poner el mensaje en la parte superior de la cola.

El servicio de componentes en cola controla este error mediante una serie de colas de reintento específicas de la aplicación. Cuando se instala el componente, hay siete colas para cada aplicación, como se muestra a continuación:

1.  Cola de entrada normal. El nombre de esta cola es el nombre de la aplicación COM+. Se trata de una cola pública de Message Queuing.

2.  Primera cola de reintentos. Los mensajes se mueven aquí si se produce un error repetidamente en la transacción al procesar mensajes de la cola de entrada normal. Los mensajes de esta cola se procesan después de un minuto. Un mensaje se puede reintentar tres veces en esta cola antes de moverse a la parte posterior de la segunda cola de reintentos. Esta cola se denomina *ApplicationName* \_ 0. Esta cola es una cola privada de Message Queuing.

3.  Segunda cola de reintentos. Los mensajes se mueven aquí si se produce un error repetidamente en la transacción al procesar los mensajes de la primera cola de reintentos. Los mensajes de esta cola se procesan después de dos minutos. Un mensaje se puede reintentar tres veces en esta cola antes de moverse a la parte posterior de la tercera cola de reintentos. Esta cola se denomina *ApplicationName* \_ 1. Esta cola es una cola privada de Message Queuing.

4.  Tercera cola de reintentos. Los mensajes se mueven aquí si se produce un error repetidamente en la transacción al procesar los mensajes de la segunda cola de reintentos. Los mensajes de esta cola se procesan después de cuatro minutos. Un mensaje se puede reintentar tres veces en esta cola antes de moverse a la parte posterior de la cuarta cola de reintentos. Esta cola se denomina *ApplicationName* \_ 2. Esta cola es una cola privada de Message Queuing.

5.  Cuarta cola de reintentos. Los mensajes se mueven aquí si se produce un error repetidamente en la transacción al procesar los mensajes de la tercera cola de reintentos. Los mensajes de esta cola se procesan después de ocho minutos. Un mensaje se puede reintentar tres veces en esta cola antes de moverse a la quinta cola de reintentos. Esta cola se denomina *ApplicationName* \_ 3. Esta cola es una cola privada de Message Queuing.

6.  La quinta cola de reintentos. Los mensajes se mueven aquí si se produce un error repetidamente en la transacción al procesar los mensajes de la cuarta cola de reintentos. Los mensajes de esta cola se procesan después de 16 minutos. Un mensaje se puede reintriste tres veces en esta cola antes de moverse a la cola de reposo final. Esta cola se denomina *ApplicationName* \_ 4. Se trata de una cola privada de Message Queuing.

7.  Una cola de reposo final específica de la aplicación. Los mensajes se mueven aquí si la transacción se anula repetidamente cuando se intenta en la quinta cola de reintentos. Esta cola se denomina *ApplicationName* \_ DeadQueue. Se trata de una cola privada de Message Queuing. La cola de reposo final no es atendida por un agente de escucha de cola. Los mensajes permanecen aquí hasta que se mueven manualmente (quizás mediante la utilidad de mover mensajes de componentes en cola) o se purgan mediante el Explorador de Message Queue Server.

Mensajes que no se pueden reproducir porque está claro que se producirá un error en todos los reintentos se pueden mover directamente a la cola de reposo final específica de la aplicación sin avanzar a través de todos los niveles de reintento.

El reproductor emite un evento COM+ para notificar a las partes interesadas que los mensajes no se pueden reproducir. Los eventos COM+ se emiten en las situaciones siguientes:

-   Cuando se anula una transacción
-   Cuando un mensaje se mueve de una cola a otra
-   Cuando un mensaje se deposita en la cola de reposo final

Los mensajes se pueden modificar antes de pasar de una cola a otra. El mecanismo de seguridad de componentes en cola de COM+ permite mover un mensaje para reintentar las colas y, a continuación, reinsertar en la cola de entrada inicial de la aplicación. Para obtener más información sobre la seguridad de los componentes en cola, vea [Queued Components Security](queued-components-security.md).

Las colas de reintento se crean junto con la cola de aplicación principal cuando la aplicación se marca como en cola mediante la herramienta de administración de servicios de componentes o mediante las funciones del SDK administrativo de COM+. El servicio de componentes en cola permite flexibilidad en el mecanismo de reintento al permitir que se eliminen las colas de reintentos. Por ejemplo, si se eliminan todas las colas de reintento, un mensaje que se anula de forma persistente se mueve directamente de la cola de la aplicación a la cola de reposo final específica de la aplicación. Al quitar una o varias de las colas de reintentos, se puede reducir el número y la longitud de los reintentos. Si las colas se quitan de la secuencia de reintentos, el tiempo de las colas restantes corresponde a la posición en la secuencia de colas de reintento. Por ejemplo, si quita la cola de reintentos *ApplicationName* \_ 1, *ApplicationName* 2 y \_ *ApplicationName* 3, los mensajes de \_ *ApplicationName* 4 se procesarían como si la cola fuera la segunda cola de \_ reintentos.

El mecanismo de reintento está diseñado para completar un mensaje si es posible. En algunos casos, puede que no sea posible que el mensaje se haga correctamente. Por ejemplo, un cliente puede estar intentando retirar dinero de una cuenta que no tiene fondos suficientes. En estas circunstancias, puede controlar el error de varias maneras, incluidas las siguientes:

-   Generación de un diagnóstico y emisión de una advertencia
-   Creación de una transacción de compensación
-   Omitir el problema y descartar el mensaje

Al igual que los errores persistentes del lado cliente, el servicio de componentes en cola permite asociar una clase de excepción a un componente. La clase de excepción está  asociada al componente mediante la pestaña Avanzadas de la página de propiedades del componente de la herramienta de administración Servicios de componentes o mediante las funciones administrativas de COM+. La clase de excepción permite al desarrollador tener control después de que se haya reintetido un mensaje y antes de que ese mensaje se haya movido a la cola de reposo final específica de la aplicación. Para obtener más información sobre la clase de excepción, vea [Persistent Client-Side Failures](persistent-client-side-failures.md).

A continuación se muestra la secuencia de eventos para el control de excepciones del lado servidor:

1.  El mensaje se mueve a través de las colas de reintento específicas de la aplicación disponibles.
2.  Se produce un error en el reintento final de la última cola de reintentos.
3.  El servicio de componentes en cola en tiempo de ejecución recupera el componente de destino del mensaje y comprueba si hay una clase de excepción.
4.  El tiempo de ejecución crea una instancia de la clase de excepción.
5.  El tiempo de ejecución consulta [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) en la clase de excepción.
6.  El tiempo de ejecución llama [**a IPlaybackControl::FinalServerRetry en**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalserverretry) la clase de excepción.
7.  El tiempo de ejecución reproduce todas las llamadas de propiedad y método del mensaje a la clase de excepción.
8.  Si los pasos del 4 al 6 no se ejecutan correctamente, el tiempo de ejecución mueve el mensaje a la cola de reposo final específica de la aplicación.

Si necesita intervención en el proceso descrito anteriormente o necesita sacar un mensaje dudoso de su cola de reposo final, use la utilidad de mover mensajes. Para obtener más información sobre la utilidad de mover mensajes, vea [Control de errores.](handling-errors-in-queued-components.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores del lado cliente](client-side-errors.md)
</dt> <dt>

[Errores Client-Side persistentes](persistent-client-side-failures.md)
</dt> </dl>

 

 



