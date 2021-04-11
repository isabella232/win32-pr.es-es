---
title: Controlar eventos en C++
description: Controlar eventos en C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Windows Media Player, C++
- Modelo de objetos de Windows Media Player, C++
- modelo de objetos, C++
- Windows Media Player Mobile, C++
- Control ActiveX de Windows Media Player, C++
- Control ActiveX móvil de Windows Media Player, C++
- Control ActiveX, C++
- Incrustación de programas de C++
- incrustación, programas de C++
- Control ActiveX de Windows Media Player, control de eventos
- Control ActiveX de Windows Media Player Mobile, control de eventos
- Control ActiveX, control de eventos
- eventos, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cbef547ab2604244c5c204707a08eb87a6b70a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148825"
---
# <a name="handling-events-in-c"></a><span data-ttu-id="94b7b-116">Controlar eventos en C++</span><span class="sxs-lookup"><span data-stu-id="94b7b-116">Handling Events in C++</span></span>

<span data-ttu-id="94b7b-117">Puede recibir eventos de Windows Media Player de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="94b7b-117">You can receive events from Windows Media Player in two ways.</span></span>

-   <span data-ttu-id="94b7b-118">A **IDispatch** mediante la interfaz **\_ WMPOCXEvents** .</span><span class="sxs-lookup"><span data-stu-id="94b7b-118">Through **IDispatch** by using the **\_WMPOCXEvents** interface.</span></span> <span data-ttu-id="94b7b-119">Esta es la interfaz que se usa para la mayoría de los escenarios de inserción.</span><span class="sxs-lookup"><span data-stu-id="94b7b-119">This is the interface to use for most embedding scenarios.</span></span>
-   <span data-ttu-id="94b7b-120">A través de la interfaz **IWMPEvents** .</span><span class="sxs-lookup"><span data-stu-id="94b7b-120">Through the **IWMPEvents** interface.</span></span> <span data-ttu-id="94b7b-121">Esta interfaz está disponible cuando el código está conectado al reproductor en modo completo, por ejemplo, cuando la comunicación remota de Windows Media Player control o en un complemento de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="94b7b-121">This interface is available when your code is connected to the full mode Player, such as when remoting the Windows Media Player control or in a UI plug-in.</span></span>

<span data-ttu-id="94b7b-122">En cada escenario, empieza a escuchar eventos mediante puntos de conexión COM.</span><span class="sxs-lookup"><span data-stu-id="94b7b-122">In each scenario, you start listening to events by using COM connection points.</span></span>

<span data-ttu-id="94b7b-123">En el ejemplo de código siguiente se usan tres variables miembro:</span><span class="sxs-lookup"><span data-stu-id="94b7b-123">The following example code uses three member variables:</span></span>


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



<span data-ttu-id="94b7b-124">Para recuperar un punto de conexión, primero debe **QueryInterface** para el contenedor de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="94b7b-124">To retrieve a connection point, you first **QueryInterface** for the connection point container.</span></span>


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



<span data-ttu-id="94b7b-125">A continuación, solicite el punto de conexión para la interfaz de eventos que desea usar.</span><span class="sxs-lookup"><span data-stu-id="94b7b-125">Next, request the connection point for the event interface you want to use.</span></span> <span data-ttu-id="94b7b-126">El siguiente código de ejemplo intenta usar primero **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="94b7b-126">The following example code first attempts to use **IWMPEvents**.</span></span> <span data-ttu-id="94b7b-127">Si esa interfaz no está disponible, utiliza **\_ WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="94b7b-127">If that interface isn't available, it uses **\_WMPOCXEvents**.</span></span>


```C++
// Test whether the control supports the IWMPEvents interface.
if(SUCCEEDED(hr))
{
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(IWMPEvents), &m_spConnectionPoint);
    if (FAILED(hr))
    {
        // If not, try the _WMPOCXEvents interface, which uses IDispatch.
        hr = spConnectionContainer->FindConnectionPoint(__uuidof(_WMPOCXEvents), &m_spConnectionPoint);
    }
}

```



<span data-ttu-id="94b7b-128">Por último, llame a **IConnectionPoint:: Advise** para solicitar eventos.</span><span class="sxs-lookup"><span data-stu-id="94b7b-128">Finally, call **IConnectionPoint::Advise** to request events.</span></span>


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



<span data-ttu-id="94b7b-129">En el ejemplo anterior, el primer parámetro supone que la clase que realiza la llamada implementa **IWMPEvents** y **\_ WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="94b7b-129">In the preceding example, the first parameter assumes that the calling class implements both **IWMPEvents** and **\_WMPOCXEvents**.</span></span> <span data-ttu-id="94b7b-130">El segundo parámetro es un valor devuelto que se usa para dejar de escuchar eventos, como cuando el programa se cierra, mediante código similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="94b7b-130">The second parameter is a return value that you use to stop listening to events, such as when your program exits, using code similar to the following:</span></span>


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



<span data-ttu-id="94b7b-131">La implementación de los controladores de eventos para **IWMPEvents** y **\_ WMPOCXEvents** es diferente.</span><span class="sxs-lookup"><span data-stu-id="94b7b-131">Implementing the event handlers for **IWMPEvents** and **\_WMPOCXEvents** differs.</span></span> <span data-ttu-id="94b7b-132">En el caso de **IWMPEvents**, debe implementar una función que controle todos los eventos definidos por la interfaz, incluso si no pretende utilizar el evento.</span><span class="sxs-lookup"><span data-stu-id="94b7b-132">For **IWMPEvents**, you must implement a function to handle every event defined by the interface, even if you don't intend to use the event.</span></span>


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



<span data-ttu-id="94b7b-133">Para implementar controladores **\_ WMPOCXEvents** , debe usar **IDispatch:: Invoke**, que es una implementación de un solo controlador de eventos para todos los eventos que se producen en la interfaz **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="94b7b-133">To implement **\_WMPOCXEvents** handlers, you must use **IDispatch::Invoke**, which is a single event handler implementation for all the events happening on the **IDispatch** interface.</span></span> <span data-ttu-id="94b7b-134">Esto significa que puede elegir controlar solo determinados eventos y omitir otros.</span><span class="sxs-lookup"><span data-stu-id="94b7b-134">This means that you can choose to handle only certain events and ignore others.</span></span> <span data-ttu-id="94b7b-135">En el ejemplo de código siguiente se muestra un controlador de **\_ WMPOCXEvents** , mediante **Invoke**, que solo controla los eventos **OpenStateChange** y **PlayStateChange** :</span><span class="sxs-lookup"><span data-stu-id="94b7b-135">The following example code shows a **\_WMPOCXEvents** handler, using **Invoke**, that handles only the **OpenStateChange** and **PlayStateChange** events:</span></span>


```C++
HRESULT CMyClass::Invoke(
    DISPID  dispIdMember,      
    REFIID  riid,              
    LCID  lcid,                
    WORD  wFlags,              
    DISPPARAMS FAR*  pDispParams,  
    VARIANT FAR*  pVarResult,  
    EXCEPINFO FAR*  pExcepInfo,  
    unsigned int FAR*  puArgErr )
{
    if (!pDispParams)
        return E_POINTER;

    if (pDispParams->cNamedArgs != 0)
        return DISP_E_NONAMEDARGS;

    HRESULT hr = DISP_E_MEMBERNOTFOUND;

    switch (dispIdMember)
    {
        case DISPID_WMPCOREEVENT_OPENSTATECHANGE:
            OpenStateChange(pDispParams->rgvarg[0].lVal /* NewState */ );
            break;

        case DISPID_WMPCOREEVENT_PLAYSTATECHANGE:
            PlayStateChange(pDispParams->rgvarg[0].lVal /* NewState */);
            break;

        // Other cases can handle additional events by using DISPIDs.
    }

    return( hr );
}

```



<span data-ttu-id="94b7b-136">En el código de ejemplo anterior, cada caso simplemente llama a a través del controlador **IWMPEvents** para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="94b7b-136">In the preceding example code, each case simply calls through to the **IWMPEvents** handler for the corresponding event.</span></span> <span data-ttu-id="94b7b-137">Si el código solo controla **\_ WMPOCXEvents**, puede llamar a una función personalizada o controlar el evento en línea después de la instrucción **Case** .</span><span class="sxs-lookup"><span data-stu-id="94b7b-137">If your code only handles **\_WMPOCXEvents**, you can simply call a custom function or handle the event inline after the **case** statement.</span></span>

## <a name="receiving-events-from-windows-media-player-10-mobile"></a><span data-ttu-id="94b7b-138">Recibir eventos de Windows Media Player 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="94b7b-138">Receiving Events from Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="94b7b-139">El control móvil de Windows Media Player 10 solo admite la recepción de ciertos eventos a través de **\_ WMPOCXEvents** y **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="94b7b-139">The Windows Media Player 10 Mobile control only supports receiving certain events through **\_WMPOCXEvents** and **IWMPEvents**.</span></span> <span data-ttu-id="94b7b-140">Para obtener más información, consulte la documentación de **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="94b7b-140">For more information, please see the documentation for **IWMPEvents**.</span></span>

## <a name="samples"></a><span data-ttu-id="94b7b-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="94b7b-141">Samples</span></span>

<span data-ttu-id="94b7b-142">El paquete de instalación de Windows Media Player instala un ejemplo que muestra el control de eventos.</span><span class="sxs-lookup"><span data-stu-id="94b7b-142">The Windows Media Player setup package installs a sample that demonstrates event handling.</span></span> <span data-ttu-id="94b7b-143">Vea el ejemplo WMPHost para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="94b7b-143">See the WMPHost sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94b7b-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94b7b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94b7b-145">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="94b7b-145">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="94b7b-146">**Usar el control Media Player de Windows en un programa de C++**</span><span class="sxs-lookup"><span data-stu-id="94b7b-146">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




