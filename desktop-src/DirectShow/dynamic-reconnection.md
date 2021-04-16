---
description: Reconexión dinámica
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Reconexión dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704178a28b91c6f78bea20b9c73c9a61f80be881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495142"
---
# <a name="dynamic-reconnection"></a>Reconexión dinámica

En la mayoría de los filtros de DirectShow, los PIN no se pueden volver a conectar mientras el gráfico está transmitiendo datos de forma activa. La aplicación debe detener el gráfico antes de volver a conectar los pin. Sin embargo, algunos filtros admiten las reconexiones de PIN mientras se ejecuta el gráfico, un proceso conocido como reconexión dinámica. Esto puede realizarse mediante la aplicación o mediante un filtro en el gráfico.

Como ejemplo, considere el gráfico de la ilustración siguiente.

![gráfico dinámico: Diagrama de creación](images/dyngraph.png)

Un escenario de reconexión dinámica podría ser quitar el filtro 2 del gráfico, mientras que el gráfico se está ejecutando y reemplazarlo por otro filtro. Para que este escenario funcione, debe cumplirse lo siguiente:

-   El PIN de entrada del filtro 3 (pin D) debe admitir la interfaz [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) . Esta interfaz permite que el PIN se vuelva a conectar sin detener el filtro.
-   El PIN de salida del filtro 1 (PIN A) debe ser capaz de bloquear el flujo de datos multimedia mientras se produce la reconexión. No se pueden viajar datos entre el PIN A y el pin D durante la reconexión. Por lo general, esto significa que el PIN de salida debe admitir la interfaz [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) . Sin embargo, si el filtro 1 es el filtro que inicia la reconexión, es posible que tenga algún mecanismo interno para bloquear su propio flujo de datos.

La reconexión dinámica implicará los siguientes pasos:

1.  Bloquee el flujo de datos del PIN A.
2.  Vuelva a conectar el PIN a al pin D, posiblemente a través de un nuevo filtro intermedio.
3.  Desbloquee el PIN A para que los datos empiecen a fluir de nuevo.

**Paso 1. Bloquear el flujo de datos**

Para bloquear el flujo de datos, llame a [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) en el PIN a. Se puede llamar a este método de forma asincrónica o sincrónica. Para llamar al método de *forma asincrónica*, cree un objeto de evento de Win32 y pase el identificador de evento al método de **bloque** . El método se devolverá inmediatamente. Espere a que se Señalice el evento con una función como **WaitForSingleObject**. El PIN señala el evento cuando ha bloqueado el flujo de datos. Por ejemplo:


```C++
// Create an event
HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (hEvent != NULL)
{
    // Block the data flow.
    hr = pFlowControl->Block(AM_PIN_FLOW_CONTROL_BLOCK, hEvent); 
    if (SUCCEEDED(hr))
    {
        // Wait for the pin to finish.
        DWORD dwRes = WaitForSingleObject(hEvent, dwMilliseconds);
    }
}
```



Para llamar al método *sincrónicamente*, solo tiene que pasar el valor **null** en lugar del identificador de evento. Ahora el método se bloqueará hasta que se complete la operación. Esto puede no ocurrir hasta que el PIN esté listo para entregar un nuevo ejemplo. Si el filtro está en pausa, puede tardar un período de tiempo arbitrario. Por lo tanto, no realice la llamada sincrónica desde el subproceso de la aplicación principal. Usar un subproceso de trabajo o llamar al método de forma asincrónica.

**Paso 2. Volver a conectar los pin**

Para volver a conectar los pin, consulte el administrador de gráficos de filtro para la interfaz **IGraphConfig** y llame a [**IGraphConfig:: reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) o [**IGraphConfig:: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure). El método de **reconexión** es más fácil de usar; hace lo siguiente:

-   Detiene los filtros intermedios (filtro 2 en el ejemplo) y los quita del gráfico.
-   Agrega nuevos filtros intermedios, si es necesario.
-   Conecta todos los pin.
-   Pausa o ejecuta cualquier filtro nuevo para que coincida con el estado del gráfico.

El método de **reconexión** tiene varios parámetros opcionales que se pueden usar para especificar el tipo de medio para la conexión del PIN y el filtro intermedio que se va a usar. Por ejemplo:


```C++
pGraph->AddFilter(pNewFilter, L"New Filter for the Graph");
pConfig->Reconnect(
    pPinA,      // Reconnect this output pin...
    pPinD,      // ... to this input pin.
    pMediaType, // Use this media type.
    pNewFilter, // Connect them through this filter.
    NULL, 
    0);     
```



Para obtener más información, consulte la página de referencia. Si el método de **reconexión** no es lo suficientemente flexible, puede usar el método **reconfigure** , que llama a un método de devolución de llamada definido por la aplicación para volver a conectar los pin. Para usar este método, implemente la interfaz [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) en la aplicación.

Antes de llamar a **reconfigure**, bloquee el flujo de datos desde el terminal de salida, tal y como se ha descrito anteriormente. A continuación, inserte los datos que aún estén pendientes en la sección del gráfico que está reconectando, como se indica a continuación:

1.  Llame a [**IPinConnection:: NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) en el PIN de entrada más abajo en la cadena de reconexión (pin D en el ejemplo). Pase un identificador a un evento de Win32.
2.  Llame a [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el PIN de entrada que es inmediatamente inferior al pin de salida donde bloqueó el flujo de datos. (En este ejemplo, el flujo de datos se bloqueó en el PIN A, por lo que llamaría a **EndOfStream** en el pin B).
3.  Espere a que se señale el evento. El PIN de entrada (pin D) indica el evento cuando recibe la notificación de final de secuencia. Esto indica que no hay datos que se desplazan entre los pin y que el autor de la llamada puede volver a conectar los pin de forma segura.

Tenga en cuenta que el método **IGraphConfig:: reconnect** controla automáticamente los pasos anteriores. Solo tiene que realizar estos pasos si usa el método **reconfigure** .

Una vez que los datos se hayan insertado a través del gráfico, llame a **reconfigure** y pase un puntero a la interfaz de devolución de llamada **IGraphConfigCallback** . Filter Graph Manager llamará al método [**IGraphConfigCallback:: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) que ha proporcionado.

**Paso 3. Desbloquear el flujo de datos**

Una vez que haya reconectado los pin, desbloquee el flujo de datos mediante una llamada a **IPinFlowControl:: Block** con un valor de cero para el primer parámetro.

> [!Note]  
> Si un filtro realiza una reconexión dinámica, hay algunos problemas de subprocesamiento que debe tener en cuenta. Si Filter Graph Manager intenta detener el filtro, puede interbloquearse porque el gráfico espera a que se detenga el filtro, al mismo tiempo que el filtro puede estar esperando a que los datos se inserten en el gráfico. Para evitar el posible interbloqueo, algunos de los métodos descritos en esta sección toman un identificador de un evento de Win32. El filtro debe indicar el evento si el administrador de gráficos de filtros intenta detener el filtro. Para obtener más información, vea [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) y [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de gráficos dinámicos](dynamic-graph-building.md)
</dt> </dl>

 

 



