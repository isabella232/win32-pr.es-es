---
description: Windows Sockets 2 introduce e/s superpuestas y requiere que todos los proveedores de transporte admitan esta funcionalidad.
ms.assetid: 90d49171-e211-4426-aa56-88aaeac7c578
title: Entrada/salida superpuestas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8caa13dd3d50e4f0fdaa1b92fa8e99afd8e2e1
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "103914238"
---
# <a name="overlapped-inputoutput"></a>Entrada/salida superpuestas

Windows Sockets 2 introduce e/s superpuestas y requiere que todos los proveedores de transporte admitan esta funcionalidad. La e/s superpuesta solo se puede realizar en sockets creados a través de la función [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) con el indicador de la marca \_ \_ OVERLAPPED superpuesta, y seguir el modelo establecido en Windows.

Para recibir, un cliente usa [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) o [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) para proporcionar búferes en los que se van a recibir los datos. Si se exponen uno o más búferes antes del momento en que la red ha recibido los datos, es posible que los datos se colocan en los búferes del usuario inmediatamente a medida que llegan y, por tanto, evitan la operación de copia que, de lo contrario, se produciría. Si los datos llegan cuando los búferes de recepción ya se han publicado, se copian inmediatamente en los búferes del usuario. Si los datos llegan cuando la aplicación no ha publicado ningún búfer de recepción, el proveedor de servicios recurre al estilo sincrónico de operación en el que los datos entrantes se almacenan en búfer internamente hasta el momento en que el cliente emite una llamada de recepción y, por tanto, proporciona un búfer en el que se pueden copiar los datos. Una excepción a esto sería si la aplicación usa [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) para establecer el tamaño del búfer de recepción en cero. En esta instancia, los protocolos confiables solo permitirán que se reciban los datos cuando se hayan publicado los búferes de la aplicación, y los datos de protocolos no confiables se perderían.

En el lado de envío, los clientes usan [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) o [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) para proporcionar punteros a búferes rellenos y, después, acuerdan no molestar los búferes de ningún modo hasta que la red haya consumido el contenido del búfer.

Las llamadas de envío y recepción superpuestas se devuelven inmediatamente. Un valor devuelto de cero indica que la operación de e/s se completó inmediatamente y que ya se ha producido la indicación de finalización correspondiente. Es decir, se ha señalado el objeto de evento asociado o la rutina de finalización se ha puesto en cola a través de [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc). Un valor devuelto de \_ error de socket junto con un código de error de la \_ e/s de WSA \_ pendiente indica que la operación superpuesta se ha iniciado correctamente y que se proporcionará una indicación posterior cuando se hayan consumido los búferes de envío o cuando se rellenen los búferes de recepción. Cualquier otro código de error indica que la operación superpuesta no se ha iniciado correctamente y que no habrá ninguna indicación de finalización próxima.

Las operaciones de envío y recepción se pueden superponer. Las funciones Receive se pueden invocar varias veces para publicar búferes de recepción como preparación para los datos entrantes, y las funciones send se pueden invocar varias veces para poner en cola varios búferes que se van a enviar. Tenga en cuenta que, aunque se enviará una serie de búferes de envío superpuestos en el orden proporcionado, se pueden producir las indicaciones de finalización correspondientes en un orden diferente. Del mismo modo, en el lado receptor, los búferes se rellenarán en el orden en que se proporcionan, pero las indicaciones de finalización pueden aparecer en un orden diferente.

La característica de finalización aplazada de e/s superpuesta también está disponible para [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)).

## <a name="delivering-completion-indications"></a>Entrega de indicaciones de finalización

Los proveedores de servicios tienen dos maneras de indicar la finalización superpuesta: establecimiento de un objeto de evento especificado por el cliente o invocación de una rutina de finalización especificada por el cliente. En ambos casos, una estructura de datos, [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped), se asocia a cada operación superpuesta. Esta estructura la asigna el cliente y la usa para indicar qué objeto de evento (si existe) se debe establecer cuando se complete. El proveedor de servicios puede usar la estructura **WSAOVERLAPPED** como un lugar para almacenar un identificador en los resultados (por ejemplo, el número de bytes transferidos, marcas actualizadas, códigos de error, etc.) para una operación superpuesta determinada. Para obtener estos resultados, los clientes deben invocar [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult), pasando un puntero a la estructura superpuesta correspondiente.

Si se selecciona la indicación de finalización basada en eventos para una solicitud de e/s superpuesta determinada, los clientes pueden usar la rutina [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) para sondear o esperar a que se complete la operación superpuesta. Si se selecciona la indicación de finalización basada en rutinas de finalización para una solicitud de e/s superpuesta en particular, solo está disponible la opción de sondeo de **WSPGetOverlappedResult** . Un cliente también puede utilizar otros medios para esperar (como el uso de [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)) hasta que el objeto de evento correspondiente se ha señalado o el proveedor de servicios ha invocado la rutina de finalización especificada. Una vez que se ha indicado la finalización, el cliente puede invocar a **WSPGetOverlappedResult**, con la expectativa de que la llamada se complete inmediatamente.

## <a name="invoking-socket-io-completion-routines"></a>Invocar rutinas de finalización de e/s de socket

Si el parámetro *lpCompletionRoutine* de una operación superpuesta no es **null**, es responsabilidad del proveedor de servicios organizar la invocación de la rutina de finalización especificada por el cliente cuando se complete la operación superpuesta. Dado que la rutina de finalización se debe ejecutar en el contexto del mismo subproceso que inició la operación superpuesta, no se puede invocar directamente desde el proveedor de servicios. El \_32.DLL Ws2 ofrece un mecanismo de llamada a procedimiento asincrónico (APC) para facilitar la invocación de rutinas de finalización.

Un proveedor de servicios organiza una función para que se ejecute en el subproceso adecuado mediante una llamada a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc). Se puede llamar a esta función desde cualquier proceso y contexto de subproceso, incluso un contexto diferente del subproceso y el proceso que se usó para iniciar la operación superpuesta.

[**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) toma como parámetros de entrada un puntero a una estructura [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) , un puntero a una función APC que se va a invocar y un valor de contexto de 32 bits que se pasa posteriormente a la función APC. Los proveedores de servicios siempre se suministran con un puntero a la estructura **WSATHREADID** adecuada mediante el parámetro *lpThreadId* a la función superpuesta. El proveedor debe almacenar la estructura **WSATHREADID** localmente y proporcionar un puntero a esta copia de la estructura **WSATHREADID** como parámetro de entrada a **WPUQueueApc**. Una vez que la función **WPUQueueApc** devuelve, el proveedor puede desechar su copia de **WSATHREADID**.

El procedimiento [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) simplemente pone en cola la información suficiente para llamar a la función APC indicada con los parámetros especificados, pero no lo llama. Cuando el subproceso de destino entra en un estado de espera de alerta, esta información se quita de la cola y se realiza una llamada a la función APC en ese subproceso de destino y contexto de proceso. Dado que el mecanismo APC solo admite un único valor de contexto de 32 bits, la función APC no puede ser la rutina de finalización especificada por el cliente, lo que implica más parámetros. En su lugar, el proveedor de servicios debe proporcionar un puntero a su propia función de APC que use el valor de contexto proporcionado para tener acceso a la información de los resultados necesarios para la operación superpuesta y, a continuación, invoca la rutina de finalización especificada por el cliente.

En el caso de los proveedores de servicios en los que un componente de modo de usuario implementa la e/s superpuesta, un uso típico del mecanismo APC es el siguiente:

-   Cuando se completa la operación de e/s, el proveedor asigna un búfer pequeño y lo empaqueta con un puntero al procedimiento de finalización proporcionado por el cliente y los valores de parámetro que se van a pasar al procedimiento.
-   Pone en cola un APC, especificando el puntero al búfer como el valor de contexto y su propio procedimiento intermedio como el procedimiento de destino.
-   Cuando el subproceso de destino entra en el estado de espera de alerta, se llama al procedimiento intermedio del proveedor de servicios en el contexto de subproceso adecuado.
-   El procedimiento intermedio simplemente desempaqueta los parámetros, desasigna el búfer y llama al procedimiento de finalización proporcionado por el cliente.
-   En el caso de los proveedores de servicios en los que un componente de modo kernel implementa la e/s superpuesta, una implementación típica es similar, salvo que la implementación usaría interfaces de kernel estándar para poner en cola el APC.

La descripción de las interfaces de kernel relevantes está fuera del ámbito de la especificación de Windows Sockets 2.

> [!Note]  
> Los proveedores de servicios deben permitir a los clientes de Windows Sockets 2 invocar las operaciones de envío y recepción desde dentro del contexto de la rutina de finalización de e/s de socket y garantizar que para un socket determinado, las rutinas de finalización de e/s no se anidarán.

 

En algunas circunstancias, un proveedor de servicios por niveles puede necesitar iniciar y completar las operaciones superpuestas desde dentro de un subproceso de trabajo interno. En este caso, [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) no estará disponible desde una llamada de función entrante. La interfaz del proveedor de servicios proporciona una llamada a, [**WPUOpenCurrentThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuopencurrentthread), para obtener un **WSATHREADID** para el subproceso actual. Cuando ya no se necesita este **WSATHREADID** , se deben devolver sus recursos llamando a [**WPUCloseThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosethread).

 

 
