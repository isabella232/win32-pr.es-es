---
description: Errores de Server-Side
ms.assetid: ce8ddb52-237c-4d46-a088-9f592afadcd2
title: Errores de Server-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7946b8197553874b8da22d35f8fab5b83f14862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714837"
---
# <a name="server-side-errors"></a>Errores de Server-Side

El agente de escucha y el reproductor trabajan juntos para tratar los mensajes dudosos. Si se produce un error en una transacción que se reproduce, [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) vuelve a mover el mensaje de entrada a la cola de entrada. El reproductor Anula la transacción si recibe un error HRESULT en el componente del servidor o si detecta una excepción. Si el problema persiste, el agente de escucha podría repetirse continuamente en el siguiente patrón:

-   Quitar de la cola el mensaje
-   Crea una instancia del objeto.
-   Experimenta una reversión
-   Vuelve a colocar el mensaje en la parte superior de la cola.

El servicio de componentes en cola controla este error mediante el uso de una serie de colas de reintento específicas de la aplicación. Creado cuando se instala el componente, hay siete colas para cada aplicación, como se indica a continuación:

1.  La cola de entrada normal. El nombre de esta cola es el nombre de la aplicación COM+. Se trata de una cola pública de Message Queue Server.

2.  La primera cola de reintentos. Los mensajes se mueven aquí si se produce un error repetidamente en la transacción al procesar los mensajes de la cola de entrada normal. Los mensajes de esta cola se procesan después de un minuto. Un mensaje se puede reintentar tres veces en esta cola antes de moverse a la parte posterior de la segunda cola de reintento. Esta cola se denomina *applicationName* \_ 0. Esta cola es una cola privada de Message Queue Server.

3.  Segunda cola de reintentos. Los mensajes se mueven aquí si se produce un error repetidamente en la transacción al procesar los mensajes de la primera cola de reintento. Los mensajes de esta cola se procesan después de dos minutos. Un mensaje se puede reintentar tres veces en esta cola antes de moverse a la parte posterior de la tercera cola de reintento. Esta cola se denomina *applicationName* \_ 1. Esta cola es una cola privada de Message Queue Server.

4.  La tercera cola de reintentos. Los mensajes se mueven aquí si se produce un error repetidamente en la transacción al procesar los mensajes de la segunda cola de reintento. Los mensajes de esta cola se procesan después de cuatro minutos. Un mensaje se puede reintentar tres veces en esta cola antes de moverse a la parte posterior de la cuarta cola de reintento. Esta cola se denomina *applicationName* \_ 2. Esta cola es una cola privada de Message Queue Server.

5.  Cuarta cola de reintentos. Los mensajes se mueven aquí si se produce un error repetidamente en la transacción al procesar los mensajes de la tercera cola de reintento. Los mensajes de esta cola se procesan después de ocho minutos. Un mensaje se puede reintentar tres veces en esta cola antes de pasarse a la quinta cola de reintentos. Esta cola se denomina *applicationName* \_ 3. Esta cola es una cola privada de Message Queue Server.

6.  La quinta cola de reintentos. Los mensajes se mueven aquí si se produce un error repetidamente en la transacción al procesar los mensajes de la cuarta cola de reintento. Los mensajes de esta cola se procesan después de dieciséis minutos. Un mensaje se puede reintentar tres veces en esta cola antes de que se mueva a la cola final. Esta cola se denomina *applicationName* \_ 4. Se trata de una cola privada de Message Queue Server.

7.  Una cola de finalización específica de la aplicación. Los mensajes se mueven aquí si la transacción se anula repetidamente cuando se intenta en la quinta cola de reintentos. Esta cola se denomina *applicationName* \_ DeadQueue. Se trata de una cola privada de Message Queue Server. El agente de escucha de la cola no atiende la cola de mantenimiento final. Los mensajes permanecen aquí hasta que se mueven manualmente (quizás por la utilidad del Movedor de mensajes de componentes en cola) o se purgan mediante el explorador de Message Queue Server.

Los mensajes que no se pueden reproducir porque están claros que cada intento de reintento no se puede migrar directamente a la cola de finalización específica de la aplicación sin ser avanzado a través de todos los niveles de reintento.

El reproductor emite un evento COM+ para notificar a las partes interesadas que no se pueden reproducir mensajes. Los eventos COM+ se emiten en las siguientes situaciones:

-   Cuando se anula una transacción
-   Cuando se mueve un mensaje de una cola a otra
-   Cuando se deposita un mensaje en la cola de eliminación final

Los mensajes se pueden modificar antes de pasar de una cola a otra. El mecanismo de seguridad de componentes en cola de COM+ permite que un mensaje se mueva a las colas de reintento y, a continuación, se vuelva a insertar en la cola de entrada inicial de la aplicación. Para obtener más información sobre la seguridad de los componentes en cola, vea [seguridad de componentes en cola](queued-components-security.md).

Las colas de reintento se crean junto con la cola de la aplicación principal cuando la aplicación está marcada como en cola por la herramienta de administración de servicios de componentes o mediante las funciones del SDK administrativo de COM+. El servicio de componentes en cola permite la flexibilidad en el mecanismo de reintento, ya que permite eliminar las colas de reintento. Por ejemplo, si se eliminan todas las colas de reintentos, los mensajes que se anulen de forma persistente se moverán directamente de la cola de la aplicación a la cola de finalización específica de la aplicación. Al quitar una o varias colas de reintentos, se puede reducir el número y la longitud de los reintentos. Si las colas se quitan de la secuencia de reintentos, la temporización de las colas restantes corresponde a la posición en la secuencia de colas de reintento. Por ejemplo, si quita la cola de reintentos *applicationName* \_ 1, *applicationName* \_ 2 y *applicationName* \_ 3, los mensajes en *applicationName* \_ 4 se procesarán como si la cola fuera la segunda cola de reintento.

El mecanismo de reintento está diseñado para completar un mensaje si es posible. En algunos casos, puede que no sea posible que el mensaje se lleve a cabo correctamente. Por ejemplo, un cliente puede estar intentando retirar dinero de una cuenta que no tiene fondos suficientes. En estas circunstancias, puede controlar el error de varias maneras, incluidas las siguientes:

-   Generar un diagnóstico y emitir una advertencia
-   Crear una transacción de compensación
-   Omitir el problema y descartar el mensaje

Al igual que los errores persistentes del lado cliente, el servicio de componentes en cola permite asociar una clase de excepción a un componente. La clase de excepción está asociada al componente mediante la ficha **Opciones avanzadas** de la página Propiedades de componente de la herramienta de administración de servicios de componentes o mediante las funciones administrativas de com+. La clase de excepción permite que el desarrollador tenga el control después de que se haya reintentado un mensaje y antes de que el mensaje se mueva a la cola de finalización específica de la aplicación. Para obtener más información sobre la clase de excepción, vea [errores de Client-Side persistentes](persistent-client-side-failures.md).

A continuación se encuentra la secuencia de eventos para el control de excepciones del servidor:

1.  El mensaje se mueve a través de las colas de reintento específicas de la aplicación disponibles.
2.  Se produce un error en el reintento final de la última cola de reintento.
3.  El tiempo de ejecución del servicio de componentes en cola recupera el componente de destino del mensaje y comprueba una clase de excepción.
4.  El tiempo de ejecución crea una instancia de la clase de excepción.
5.  Las consultas en tiempo de ejecución [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) en la clase de excepción.
6.  El tiempo de ejecución llama a [**IPlaybackControl:: FinalServerRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalserverretry) en la clase de excepción.
7.  El tiempo de ejecución reproduce todas las llamadas a propiedades y métodos desde el mensaje a la clase de excepción.
8.  Si los pasos del 4 al 6 no se realizan correctamente, el tiempo de ejecución mueve el mensaje a la cola de finalización específica de la aplicación.

Si necesita intervenir en el proceso descrito anteriormente o necesita mover un mensaje dudoso fuera de la cola de salida final, use la utilidad del Movedor de mensajes. Para obtener más información sobre la utilidad del Movedor de mensajes, vea [control de errores](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores del lado cliente](client-side-errors.md)
</dt> <dt>

[Errores de Client-Side persistentes](persistent-client-side-failures.md)
</dt> </dl>

 

 



