---
description: Windows Sockets 2 introduce E/S superpuesta y requiere que todos los proveedores de transporte admitan esta funcionalidad.
ms.assetid: 90d49171-e211-4426-aa56-88aaeac7c578
title: Entrada y salida superpuestas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d260cccd13bfb8e872e0ac7346c112efff2f77cf115e3fe2f8dd3d3fb94deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641795"
---
# <a name="overlapped-inputoutput"></a>Entrada y salida superpuestas

Windows Sockets 2 introduce E/S superpuesta y requiere que todos los proveedores de transporte admitan esta funcionalidad. La E/S superpuesta solo se puede realizar en sockets creados a través de la función [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) con la marca OVERLAPPED de WSA FLAG establecida y seguir el modelo \_ establecido en \_ Windows.

Para recibir, un cliente usa [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) o [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) para proporcionar búferes en los que se recibirán los datos. Si uno o varios búferes se publican antes del momento en que la red ha recibido los datos, es posible que los datos se coloquen en los búferes del usuario inmediatamente a medida que llegan y, por tanto, eviten la operación de copia que se produciría de otro modo. Si llegan datos cuando ya se han publicado búferes de recepción, se copian inmediatamente en los búferes del usuario. Si llegan datos cuando la aplicación no ha publicado búferes de recepción, el proveedor de servicios recurre al estilo sincrónico de operación donde los datos entrantes se almacenan en búfer internamente hasta que el cliente emite una llamada de recepción y, por tanto, proporciona un búfer en el que se pueden copiar los datos. Una excepción a esto sería si la aplicación usara [**WSPSetSockOpt para**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) establecer el tamaño del búfer de recepción en cero. En este caso, los protocolos confiables solo permitirían que se recibieran datos cuando se publicaran búferes de aplicación y se perdiera información sobre protocolos no confiables.

En el lado de envío, los clientes usan [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) o [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) para proporcionar punteros a búferes rellenos y, a continuación, aceptan no alterar los búferes de ninguna manera hasta que la red haya consumido el contenido del búfer.

Las llamadas de envío y recepción superpuestas se devuelven inmediatamente. Un valor devuelto de cero indica que la operación de E/S se completó inmediatamente y que ya se ha producido la indicación de finalización correspondiente. Es decir, se ha señalado el objeto de evento asociado o la rutina de finalización se ha puesto en cola a través de [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc). Un valor devuelto de SOCKET ERROR junto con un código de error de WSA IO PENDING indica que la operación superpuesta se ha iniciado correctamente y que se proporciona una indicación posterior cuando se han consumido los búferes de envío o cuando se rellenan los búferes de \_ \_ \_ recepción. Cualquier otro código de error indica que la operación superpuesta no se inició correctamente y que no habrá ninguna indicación de finalización próxima.

Las operaciones de envío y recepción se pueden superponer. Las funciones de recepción se pueden invocar varias veces para publicar búferes de recepción como preparación para los datos entrantes, y las funciones de envío se pueden invocar varias veces para poner en cola varios búferes que se enviarán. Tenga en cuenta que, aunque se enviará una serie de búferes de envío superpuestos en el orden proporcionado, las indicaciones de finalización correspondientes pueden producirse en un orden diferente. Del mismo modo, en el lado receptor, los búferes se rellenarán en el orden en que se proporcionan, pero las indicaciones de finalización pueden producirse en un orden diferente.

La característica de finalización diferida de E/S superpuesta también está disponible para [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)).

## <a name="delivering-completion-indications"></a>Entrega de indicaciones de finalización

Los proveedores de servicios tienen dos maneras de indicar la finalización superpuesta: establecer un objeto de evento especificado por el cliente o invocar una rutina de finalización especificada por el cliente. En ambos casos, una estructura de datos, [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped), está asociada a cada operación superpuesta. El cliente asigna esta estructura y la usa para indicar qué objeto de evento (si existe) se va a establecer cuando se produzca la finalización. El proveedor de servicios puede usar la estructura **WSAOVERLAPPED** como lugar para almacenar un identificador en los resultados (por ejemplo, el número de bytes transferidos, las marcas actualizadas, los códigos de error, etc.) para una operación superpuesta determinada. Para obtener estos resultados, los clientes deben invocar [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult), pasando un puntero a la estructura superpuesta correspondiente.

Si se selecciona la indicación de finalización basada en eventos para una solicitud de E/S superpuesta determinada, los clientes pueden usar la rutina [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) para sondear o esperar a que finalice la operación superpuesta. Si se selecciona la indicación de finalización basada en la rutina de finalización para una solicitud de E/S superpuesta determinada, solo está disponible la opción de sondeo **de WSPGetOverlappedResult.** Un cliente también puede usar otros medios para esperar (como el uso de [**WSAWaitForMultipleEvents)**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)hasta que se ha señalado el objeto de evento correspondiente o el proveedor de servicios ha invocado la rutina de finalización especificada. Una vez que se ha indicado la finalización, el cliente puede invocar **WSPGetOverlappedResult**, con la expectativa de que la llamada se complete inmediatamente.

## <a name="invoking-socket-io-completion-routines"></a>Invocar rutinas de finalización de E/S de socket

Si el parámetro *lpCompletionRoutine* de una operación superpuesta no es **NULL,** es responsabilidad del proveedor de servicios organizar la invocación de la rutina de finalización especificada por el cliente cuando se complete la operación superpuesta. Puesto que la rutina de finalización debe ejecutarse en el contexto del mismo subproceso que inició la operación superpuesta, no se puede invocar directamente desde el proveedor de servicios. El32.DLL Ws2 ofrece un mecanismo de llamada a procedimiento asincrónico (APC) para facilitar la invocación de \_ rutinas de finalización.

Un proveedor de servicios organiza la ejecución de una función en el subproceso adecuado mediante una llamada a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc). Se puede llamar a esta función desde cualquier contexto de proceso y subproceso, incluso desde un contexto diferente del subproceso y el proceso que se usó para iniciar la operación superpuesta.

[**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) toma como parámetros de entrada un puntero a una estructura [**WSATHREADID,**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) un puntero a una función de APC que se va a invocar y un valor de contexto de 32 bits que se pasa posteriormente a la función APC. Los proveedores de servicios siempre se proporcionan con un puntero a la estructura **WSATHREADID** adecuada a través del parámetro *lpThreadId* a la función superpuesta. El proveedor debe almacenar la estructura **WSATHREADID** localmente y proporcionar un puntero a esta copia de la estructura **WSATHREADID** como un parámetro de entrada a **WPUQueueApc**. Una vez que se devuelve la función **WPUQueueApc,** el proveedor puede eliminar su copia de **WSATHREADID**.

El procedimiento [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) simplemente coloca en cola información suficiente para llamar a la función de APC indicada con los parámetros especificados, pero no la llama. Cuando el subproceso de destino entra en un estado de espera que se puede alertar, esta información se quita de la cola y se realiza una llamada a la función APC en ese subproceso de destino y contexto de proceso. Dado que el mecanismo de APC solo admite un único valor de contexto de 32 bits, la función APC no puede ser la rutina de finalización especificada por el cliente, lo que implica más parámetros. En su lugar, el proveedor de servicios debe proporcionar un puntero a su propia función de APC que usa el valor de contexto proporcionado para tener acceso a la información de resultado necesaria para la operación superpuesta y, a continuación, invoca la rutina de finalización especificada por el cliente.

Para los proveedores de servicios en los que un componente de modo de usuario implementa E/S superpuesta, un uso típico del mecanismo de APC es el siguiente:

-   Cuando se completa la operación de E/S, el proveedor asigna un búfer pequeño y lo empaqueta con un puntero al procedimiento de finalización proporcionado por el cliente y a los valores de parámetro que se pasan al procedimiento.
-   Pone en cola un APC, especificando el puntero al búfer como valor de contexto y su propio procedimiento intermedio como procedimiento de destino.
-   Cuando el subproceso de destino entra finalmente en el estado de espera que se puede alertar, se llama al procedimiento intermedio del proveedor de servicios en el contexto de subproceso adecuado.
-   El procedimiento intermedio simplemente desempaqueta los parámetros, desasigna el búfer y llama al procedimiento de finalización proporcionado por el cliente.
-   En el caso de los proveedores de servicios en los que un componente de modo kernel implementa E/S superpuesta, una implementación típica es similar, salvo que la implementación usaría interfaces de kernel estándar para poner en cola el APC.

La descripción de las interfaces de kernel pertinentes está fuera del ámbito de la especificación Windows Sockets 2.

> [!Note]  
> Los proveedores de servicios deben permitir que los clientes de Windows Sockets 2 invoque operaciones de envío y recepción desde dentro del contexto de la rutina de finalización de E/S de socket y garantizar que para un socket determinado, las rutinas de finalización de E/S no se anidarán.

 

En algunas circunstancias, es posible que un proveedor de servicios por capas necesite iniciar y completar operaciones superpuestas desde dentro de un subproceso de trabajo interno. En este caso, un [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) no estaría disponible desde una llamada de función entrante. La interfaz del proveedor de servicios proporciona una llamada de llamada, [**WPUOpenCurrentThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuopencurrentthread), para obtener un **WSATHREADID** para el subproceso actual. Cuando ya no se necesite este **WSATHREADID,** se deben devolver sus recursos mediante una llamada a [**WPUCloseThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosethread).

 

 
