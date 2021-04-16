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
# <a name="dynamic-reconnection"></a><span data-ttu-id="9b075-103">Reconexión dinámica</span><span class="sxs-lookup"><span data-stu-id="9b075-103">Dynamic Reconnection</span></span>

<span data-ttu-id="9b075-104">En la mayoría de los filtros de DirectShow, los PIN no se pueden volver a conectar mientras el gráfico está transmitiendo datos de forma activa.</span><span class="sxs-lookup"><span data-stu-id="9b075-104">In most DirectShow filters, pins cannot be reconnected while the graph is actively streaming data.</span></span> <span data-ttu-id="9b075-105">La aplicación debe detener el gráfico antes de volver a conectar los pin.</span><span class="sxs-lookup"><span data-stu-id="9b075-105">The application must stop the graph before reconnecting the pins.</span></span> <span data-ttu-id="9b075-106">Sin embargo, algunos filtros admiten las reconexiones de PIN mientras se ejecuta el gráfico, un proceso conocido como reconexión dinámica.</span><span class="sxs-lookup"><span data-stu-id="9b075-106">However, some filters do support pin reconnections while the graph is running, a process known as dynamic reconnection.</span></span> <span data-ttu-id="9b075-107">Esto puede realizarse mediante la aplicación o mediante un filtro en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="9b075-107">This can be done either by the application, or by a filter in the graph.</span></span>

<span data-ttu-id="9b075-108">Como ejemplo, considere el gráfico de la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="9b075-108">As an example, consider the graph in the following illustration.</span></span>

![gráfico dinámico: Diagrama de creación](images/dyngraph.png)

<span data-ttu-id="9b075-110">Un escenario de reconexión dinámica podría ser quitar el filtro 2 del gráfico, mientras que el gráfico se está ejecutando y reemplazarlo por otro filtro.</span><span class="sxs-lookup"><span data-stu-id="9b075-110">One scenario for dynamic reconnection might be to remove Filter 2 from the graph, while the graph is running, and replace it with another filter.</span></span> <span data-ttu-id="9b075-111">Para que este escenario funcione, debe cumplirse lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9b075-111">For this scenario to work, the following must be true:</span></span>

-   <span data-ttu-id="9b075-112">El PIN de entrada del filtro 3 (pin D) debe admitir la interfaz [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) .</span><span class="sxs-lookup"><span data-stu-id="9b075-112">The input pin on Filter 3 (pin D) must support the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="9b075-113">Esta interfaz permite que el PIN se vuelva a conectar sin detener el filtro.</span><span class="sxs-lookup"><span data-stu-id="9b075-113">This interface enables the pin to be reconnected without stopping the filter.</span></span>
-   <span data-ttu-id="9b075-114">El PIN de salida del filtro 1 (PIN A) debe ser capaz de bloquear el flujo de datos multimedia mientras se produce la reconexión.</span><span class="sxs-lookup"><span data-stu-id="9b075-114">The output pin on Filter 1 (pin A) must be able to block the flow of media data while the reconnection occurs.</span></span> <span data-ttu-id="9b075-115">No se pueden viajar datos entre el PIN A y el pin D durante la reconexión.</span><span class="sxs-lookup"><span data-stu-id="9b075-115">No data can travel between pin A and pin D during the reconnection.</span></span> <span data-ttu-id="9b075-116">Por lo general, esto significa que el PIN de salida debe admitir la interfaz [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) .</span><span class="sxs-lookup"><span data-stu-id="9b075-116">Generally, this means the output pin must support the [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) interface.</span></span> <span data-ttu-id="9b075-117">Sin embargo, si el filtro 1 es el filtro que inicia la reconexión, es posible que tenga algún mecanismo interno para bloquear su propio flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="9b075-117">However, if Filter 1 is the filter that initiates the reconnection, it might have some internal mechanism to block its own data flow.</span></span>

<span data-ttu-id="9b075-118">La reconexión dinámica implicará los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="9b075-118">The dynamic reconnection will involve the following steps:</span></span>

1.  <span data-ttu-id="9b075-119">Bloquee el flujo de datos del PIN A.</span><span class="sxs-lookup"><span data-stu-id="9b075-119">Block the data stream from pin A.</span></span>
2.  <span data-ttu-id="9b075-120">Vuelva a conectar el PIN a al pin D, posiblemente a través de un nuevo filtro intermedio.</span><span class="sxs-lookup"><span data-stu-id="9b075-120">Reconnect pin A to pin D, possibly through a new intermediate filter.</span></span>
3.  <span data-ttu-id="9b075-121">Desbloquee el PIN A para que los datos empiecen a fluir de nuevo.</span><span class="sxs-lookup"><span data-stu-id="9b075-121">Unblock pin A so that data starts to flow again.</span></span>

<span data-ttu-id="9b075-122">**Paso 1. Bloquear el flujo de datos**</span><span class="sxs-lookup"><span data-stu-id="9b075-122">**Step 1. Block the Data Stream**</span></span>

<span data-ttu-id="9b075-123">Para bloquear el flujo de datos, llame a [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) en el PIN a. Se puede llamar a este método de forma asincrónica o sincrónica.</span><span class="sxs-lookup"><span data-stu-id="9b075-123">To block the data stream, call [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) on pin A. This method can be called either asynchronously or synchronously.</span></span> <span data-ttu-id="9b075-124">Para llamar al método de *forma asincrónica*, cree un objeto de evento de Win32 y pase el identificador de evento al método de **bloque** .</span><span class="sxs-lookup"><span data-stu-id="9b075-124">To call the method *asynchronously*, create a Win32 event object and pass the event handle to the **Block** method.</span></span> <span data-ttu-id="9b075-125">El método se devolverá inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="9b075-125">The method will return immediately.</span></span> <span data-ttu-id="9b075-126">Espere a que se Señalice el evento con una función como **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="9b075-126">Wait for the event to be signaled, using a function such as **WaitForSingleObject**.</span></span> <span data-ttu-id="9b075-127">El PIN señala el evento cuando ha bloqueado el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="9b075-127">The pin signals the event when it has blocked the data flow.</span></span> <span data-ttu-id="9b075-128">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9b075-128">For example:</span></span>


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



<span data-ttu-id="9b075-129">Para llamar al método *sincrónicamente*, solo tiene que pasar el valor **null** en lugar del identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="9b075-129">To call the method *synchronously*, simply pass the value **NULL** instead of the event handle.</span></span> <span data-ttu-id="9b075-130">Ahora el método se bloqueará hasta que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="9b075-130">Now the method will block until the operation completes.</span></span> <span data-ttu-id="9b075-131">Esto puede no ocurrir hasta que el PIN esté listo para entregar un nuevo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9b075-131">This may not happen until the pin is ready to deliver a new sample.</span></span> <span data-ttu-id="9b075-132">Si el filtro está en pausa, puede tardar un período de tiempo arbitrario.</span><span class="sxs-lookup"><span data-stu-id="9b075-132">If the filter is paused, this can take an arbitrary length of time.</span></span> <span data-ttu-id="9b075-133">Por lo tanto, no realice la llamada sincrónica desde el subproceso de la aplicación principal.</span><span class="sxs-lookup"><span data-stu-id="9b075-133">Therefore, do not make the synchronous call from your main application thread.</span></span> <span data-ttu-id="9b075-134">Usar un subproceso de trabajo o llamar al método de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9b075-134">Use a worker thread, or else call the method asynchronously.</span></span>

<span data-ttu-id="9b075-135">**Paso 2. Volver a conectar los pin**</span><span class="sxs-lookup"><span data-stu-id="9b075-135">**Step 2. Reconnect the Pins**</span></span>

<span data-ttu-id="9b075-136">Para volver a conectar los pin, consulte el administrador de gráficos de filtro para la interfaz **IGraphConfig** y llame a [**IGraphConfig:: reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) o [**IGraphConfig:: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span><span class="sxs-lookup"><span data-stu-id="9b075-136">To reconnect the pins, query the Filter Graph Manager for the **IGraphConfig** interface and call either [**IGraphConfig::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) or [**IGraphConfig::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span></span> <span data-ttu-id="9b075-137">El método de **reconexión** es más fácil de usar; hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9b075-137">The **Reconnect** method is simpler to use; it does the following:</span></span>

-   <span data-ttu-id="9b075-138">Detiene los filtros intermedios (filtro 2 en el ejemplo) y los quita del gráfico.</span><span class="sxs-lookup"><span data-stu-id="9b075-138">Stops the intermediate filters (Filter 2 in the example) and removes them from the graph.</span></span>
-   <span data-ttu-id="9b075-139">Agrega nuevos filtros intermedios, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="9b075-139">Adds new intermediate filters, if needed.</span></span>
-   <span data-ttu-id="9b075-140">Conecta todos los pin.</span><span class="sxs-lookup"><span data-stu-id="9b075-140">Connects all the pins.</span></span>
-   <span data-ttu-id="9b075-141">Pausa o ejecuta cualquier filtro nuevo para que coincida con el estado del gráfico.</span><span class="sxs-lookup"><span data-stu-id="9b075-141">Pauses or runs any new filters, to match the state of the graph.</span></span>

<span data-ttu-id="9b075-142">El método de **reconexión** tiene varios parámetros opcionales que se pueden usar para especificar el tipo de medio para la conexión del PIN y el filtro intermedio que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="9b075-142">The **Reconnect** method has several optional parameters that can be used to specify the media type for the pin connection and the intermediate filter to use.</span></span> <span data-ttu-id="9b075-143">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9b075-143">For example:</span></span>


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



<span data-ttu-id="9b075-144">Para obtener más información, consulte la página de referencia.</span><span class="sxs-lookup"><span data-stu-id="9b075-144">For details, consult the reference page.</span></span> <span data-ttu-id="9b075-145">Si el método de **reconexión** no es lo suficientemente flexible, puede usar el método **reconfigure** , que llama a un método de devolución de llamada definido por la aplicación para volver a conectar los pin.</span><span class="sxs-lookup"><span data-stu-id="9b075-145">If the **Reconnect** method is not flexible enough, you can use the **Reconfigure** method, which calls an application-defined callback method to reconnect the pins.</span></span> <span data-ttu-id="9b075-146">Para usar este método, implemente la interfaz [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9b075-146">To use this method, implement the [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) interface in your application.</span></span>

<span data-ttu-id="9b075-147">Antes de llamar a **reconfigure**, bloquee el flujo de datos desde el terminal de salida, tal y como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9b075-147">Before calling **Reconfigure**, block the data flow from the output pin, as described previously.</span></span> <span data-ttu-id="9b075-148">A continuación, inserte los datos que aún estén pendientes en la sección del gráfico que está reconectando, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="9b075-148">Then push any data that is still pending in the section of the graph that you are reconnecting, as follows:</span></span>

1.  <span data-ttu-id="9b075-149">Llame a [**IPinConnection:: NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) en el PIN de entrada más abajo en la cadena de reconexión (pin D en el ejemplo).</span><span class="sxs-lookup"><span data-stu-id="9b075-149">Call [**IPinConnection::NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) on the input pin furthest downstream in the reconnection chain (pin D in the example).</span></span> <span data-ttu-id="9b075-150">Pase un identificador a un evento de Win32.</span><span class="sxs-lookup"><span data-stu-id="9b075-150">Pass in a handle to a Win32 event.</span></span>
2.  <span data-ttu-id="9b075-151">Llame a [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el PIN de entrada que es inmediatamente inferior al pin de salida donde bloqueó el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="9b075-151">Call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the input pin that is immediately downstream from the output pin where you blocked the data flow.</span></span> <span data-ttu-id="9b075-152">(En este ejemplo, el flujo de datos se bloqueó en el PIN A, por lo que llamaría a **EndOfStream** en el pin B).</span><span class="sxs-lookup"><span data-stu-id="9b075-152">(In this example, the data flow was blocked at pin A, so you would call **EndOfStream** on pin B.)</span></span>
3.  <span data-ttu-id="9b075-153">Espere a que se señale el evento.</span><span class="sxs-lookup"><span data-stu-id="9b075-153">Wait for the event to be signaled.</span></span> <span data-ttu-id="9b075-154">El PIN de entrada (pin D) indica el evento cuando recibe la notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="9b075-154">The input pin (pin D) signals the event when it receives the end-of-stream notification.</span></span> <span data-ttu-id="9b075-155">Esto indica que no hay datos que se desplazan entre los pin y que el autor de la llamada puede volver a conectar los pin de forma segura.</span><span class="sxs-lookup"><span data-stu-id="9b075-155">This indicates that no data is traveling between the pins, and that the caller can safely reconnect the pins.</span></span>

<span data-ttu-id="9b075-156">Tenga en cuenta que el método **IGraphConfig:: reconnect** controla automáticamente los pasos anteriores.</span><span class="sxs-lookup"><span data-stu-id="9b075-156">Note that the **IGraphConfig::Reconnect** method automatically handles the previous steps.</span></span> <span data-ttu-id="9b075-157">Solo tiene que realizar estos pasos si usa el método **reconfigure** .</span><span class="sxs-lookup"><span data-stu-id="9b075-157">You only need to perform these steps if you are using the **Reconfigure** method.</span></span>

<span data-ttu-id="9b075-158">Una vez que los datos se hayan insertado a través del gráfico, llame a **reconfigure** y pase un puntero a la interfaz de devolución de llamada **IGraphConfigCallback** .</span><span class="sxs-lookup"><span data-stu-id="9b075-158">After the data is pushed through the graph, call **Reconfigure** and pass a pointer to your **IGraphConfigCallback** callback interface.</span></span> <span data-ttu-id="9b075-159">Filter Graph Manager llamará al método [**IGraphConfigCallback:: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) que ha proporcionado.</span><span class="sxs-lookup"><span data-stu-id="9b075-159">The Filter Graph Manager will call the [**IGraphConfigCallback::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) method that you have provided.</span></span>

<span data-ttu-id="9b075-160">**Paso 3. Desbloquear el flujo de datos**</span><span class="sxs-lookup"><span data-stu-id="9b075-160">**Step 3. Unblock the Data Flow**</span></span>

<span data-ttu-id="9b075-161">Una vez que haya reconectado los pin, desbloquee el flujo de datos mediante una llamada a **IPinFlowControl:: Block** con un valor de cero para el primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="9b075-161">After you have reconnected the pins, unblock the data flow by calling **IPinFlowControl::Block** with a value of zero for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="9b075-162">Si un filtro realiza una reconexión dinámica, hay algunos problemas de subprocesamiento que debe tener en cuenta.</span><span class="sxs-lookup"><span data-stu-id="9b075-162">If a dynamic reconnection is performed by a filter, there are some threading issues that you must be aware of.</span></span> <span data-ttu-id="9b075-163">Si Filter Graph Manager intenta detener el filtro, puede interbloquearse porque el gráfico espera a que se detenga el filtro, al mismo tiempo que el filtro puede estar esperando a que los datos se inserten en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="9b075-163">If the Filter Graph Manager tries to stop the filter, it can deadlock, because the graph waits for the filter to stop, while at the same time the filter may be waiting for data to be pushed through the graph.</span></span> <span data-ttu-id="9b075-164">Para evitar el posible interbloqueo, algunos de los métodos descritos en esta sección toman un identificador de un evento de Win32.</span><span class="sxs-lookup"><span data-stu-id="9b075-164">To prevent the possible deadlock, some of the methods described in this section take a handle to a Win32 event.</span></span> <span data-ttu-id="9b075-165">El filtro debe indicar el evento si el administrador de gráficos de filtros intenta detener el filtro.</span><span class="sxs-lookup"><span data-stu-id="9b075-165">The filter should signal the event if the Filter Graph Manager attempts to stop the filter.</span></span> <span data-ttu-id="9b075-166">Para obtener más información, vea [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) y [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span><span class="sxs-lookup"><span data-stu-id="9b075-166">For more information, see [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) and [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9b075-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b075-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b075-168">Creación de gráficos dinámicos</span><span class="sxs-lookup"><span data-stu-id="9b075-168">Dynamic Graph Building</span></span>](dynamic-graph-building.md)
</dt> </dl>

 

 



