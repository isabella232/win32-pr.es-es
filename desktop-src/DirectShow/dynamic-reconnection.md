---
description: Reconexión dinámica
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Reconexión dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b558a2e00ee2577cf1d31dda7aaebb15b5bd740c6dad5689e70b950c02d4d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966165"
---
# <a name="dynamic-reconnection"></a>Reconexión dinámica

En la mayoría DirectShow filtros, los pines no se pueden volver a conectar mientras el gráfico transmite datos activamente. La aplicación debe detener el gráfico antes de volver a conectar los pines. Sin embargo, algunos filtros admiten reconexiones de pin mientras se ejecuta el grafo, un proceso conocido como reconexión dinámica. Esto se puede hacer mediante la aplicación o mediante un filtro en el gráfico.

Por ejemplo, considere el gráfico de la ilustración siguiente.

![diagrama dinámico de creación de gráficos](images/dyngraph.png)

Un escenario para la reconexión dinámica podría ser quitar el filtro 2 del gráfico mientras se ejecuta el gráfico y reemplazarlo por otro filtro. Para que este escenario funcione, debe cumplirse lo siguiente:

-   El pin de entrada del filtro 3 (pin D) debe admitir la [**interfaz IPinConnection.**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) Esta interfaz permite volver a conectar el pin sin detener el filtro.
-   El pin de salida del filtro 1 (anclar A) debe ser capaz de bloquear el flujo de datos multimedia mientras se produce la reconexión. Ningún dato puede desplazarse entre el pin A y el pin D durante la reconexión. Por lo general, esto significa que el pin de salida debe admitir la [**interfaz IPinFlowControl.**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) Sin embargo, si el filtro 1 es el filtro que inicia la reconexión, podría tener algún mecanismo interno para bloquear su propio flujo de datos.

La reconexión dinámica implicará los pasos siguientes:

1.  Bloquee el flujo de datos del pin A.
2.  Vuelva a conectar el pin A al pin D, posiblemente a través de un nuevo filtro intermedio.
3.  Desbloquee el pin A para que los datos empiecen a fluir de nuevo.

**Paso 1. Bloquear el flujo de datos**

Para bloquear el flujo de datos, llame [**a IPinFlowControl::Block en**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) el pin A. Se puede llamar a este método de forma asincrónica o sincrónica. Para llamar al método *de forma asincrónica,* cree un objeto de evento Win32 y pase el identificador de evento al **método Block.** El método devolverá inmediatamente. Espere a que se señale el evento mediante una función como **WaitForSingleObject**. El pin señala el evento cuando ha bloqueado el flujo de datos. Por ejemplo:


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



Para llamar al método *de forma sincrónica,* simplemente pase el valor **NULL** en lugar del identificador de evento. Ahora el método se bloqueará hasta que se complete la operación. Esto puede no ocurrir hasta que el pin esté listo para entregar un nuevo ejemplo. Si el filtro está en pausa, puede tardar un tiempo arbitrario. Por lo tanto, no realice la llamada sincrónica desde el subproceso de aplicación principal. Use un subproceso de trabajo o llame al método de forma asincrónica.

**Paso 2. Volver a conectar los pines**

Para volver a conectar los pines, consulte el Administrador de filtros Graph para la interfaz **IGraphConfig** y llame a [**IGraphConfig::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) o [**IGraphConfig::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure). El **método Reconnect** es más sencillo de usar; hace lo siguiente:

-   Detiene los filtros intermedios (filtro 2 en el ejemplo) y los quita del gráfico.
-   Agrega nuevos filtros intermedios, si es necesario.
-   Conecta todos los pines.
-   Pausa o ejecuta los nuevos filtros para que coincidan con el estado del gráfico.

El **método Reconnect** tiene varios parámetros opcionales que se pueden usar para especificar el tipo de medio para la conexión de pin y el filtro intermedio que se va a usar. Por ejemplo:


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



Para más información, consulte la página de referencia. Si el **método Reconnect** no es lo suficientemente flexible, puede usar el método **Reconfigure,** que llama a un método de devolución de llamada definido por la aplicación para volver a conectar los pines. Para usar este método, implemente la [**interfaz IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) en la aplicación.

Antes de llamar **a Reconfigure**, bloquee el flujo de datos del pin de salida, como se describió anteriormente. A continuación, inserta los datos que todavía están pendientes en la sección del gráfico que estás volviendo a conectar, como se muestra a continuación:

1.  Llame [**a IPinConnection::NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) en el pin de entrada más abajo de la cadena de reconexión (anclar D en el ejemplo). Pase un identificador a un evento Win32.
2.  Llame [**a IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el pin de entrada que está inmediatamente de bajada desde el pin de salida donde bloqueó el flujo de datos. (En este ejemplo, el flujo de datos se bloqueó en el pin A, por lo que llamaría a **EndOfStream** en el pin B).
3.  Espere a que se señale el evento. El pin de entrada (pin D) señala el evento cuando recibe la notificación de fin de flujo. Esto indica que no hay datos que viajen entre los pines y que el autor de la llamada puede volver a conectarlos de forma segura.

Tenga en cuenta que **el método IGraphConfig::Reconnect** controla automáticamente los pasos anteriores. Solo tiene que realizar estos pasos si usa el **método Reconfigure.**

Después de insertar los datos a través del gráfico, llame a **Reconfigure** y pase un puntero a la interfaz de devolución de llamada **IGraphConfigCallback.** Filter Graph Manager llamará al [**método IGraphConfigCallback::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) que ha proporcionado.

**Paso 3. Desbloqueo de la cuenta de Flow**

Después de volver a conectar los pines, desbloquee el flujo de datos mediante una llamada a **IPinFlowControl::Block** con un valor de cero para el primer parámetro.

> [!Note]  
> Si un filtro realiza una reconexión dinámica, hay algunos problemas de subprocesos que debe tener en cuenta. Si filter Graph Manager intenta detener el filtro, puede interbloqueo, ya que el gráfico espera a que se detenga el filtro, mientras que al mismo tiempo el filtro puede estar esperando a que los datos se insertan a través del gráfico. Para evitar el posible interbloqueo, algunos de los métodos descritos en esta sección toman un identificador para un evento Win32. El filtro debe indicar el evento si el administrador de Graph intenta detener el filtro. Para obtener más información, [**vea IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e [**IPinConnection.**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación Graph dinámica](dynamic-graph-building.md)
</dt> </dl>

 

 



