---
title: Windows Touch Scratchpad con el ejemplo de lápiz en tiempo real (C++)
description: Revise un ejemplo de C++ de Windows Touch Scratchpad (MTScratchpadRTStylus), que muestra cómo usar mensajes de Windows Touch para dibujar seguimientos de los puntos táctiles en una ventana.
ms.assetid: c72ddc71-48b7-4c26-af2b-10919038eaf8
keywords:
- Windows Touch, ejemplos de código
- Windows Touch, código de ejemplo
- Ejemplos de Windows Touch y Scratchpad
- Ejemplos de Scratchpad
- Objeto Windows Touch,Real-Time Stylus (RTS)
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 42e32e66942f3dcfad11b8b777e846e0cee6c0b3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406298"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="032db-108">Windows Touch Scratchpad con el ejemplo de lápiz en tiempo real (C++)</span><span class="sxs-lookup"><span data-stu-id="032db-108">Windows Touch Scratchpad using the Real-time Stylus Sample (C++)</span></span>

<span data-ttu-id="032db-109">El ejemplo de Windows Touch Scratchpad[(MTScratchpadRTStylus)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)muestra cómo usar mensajes de Windows Touch para dibujar seguimientos de los puntos táctiles en una ventana.</span><span class="sxs-lookup"><span data-stu-id="032db-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="032db-110">El seguimiento del dedo principal, el que se ha puesto primero en el digitalizador, se dibuja en negro.</span><span class="sxs-lookup"><span data-stu-id="032db-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="032db-111">Los dedos secundarios se dibujan en otros seis colores: rojo, verde, azul, aguaz, rojo y amarillo.</span><span class="sxs-lookup"><span data-stu-id="032db-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta, and yellow.</span></span> <span data-ttu-id="032db-112">En la siguiente captura de pantalla se muestra el aspecto de la aplicación mientras se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="032db-112">The following screen shot shows how the application could look while running.</span></span>

![captura de pantalla que muestra el ejemplo de scratchpad táctil de Windows con el lápiz óptico en tiempo real, con una línea verde, roja, tres negra y una línea azul en la pantalla](images/mtscratchpadrtstylus.png)

<span data-ttu-id="032db-114">En este ejemplo, se crea el objeto Lápiz en tiempo real (RTS) y se habilita la compatibilidad con varios puntos de contacto.</span><span class="sxs-lookup"><span data-stu-id="032db-114">For this sample, the Real-time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="032db-115">Se agrega un complemento DynamicRenderer al RTS para representar el contenido.</span><span class="sxs-lookup"><span data-stu-id="032db-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="032db-116">Se implementa un complemento, **CSyncEventHandlerRTS,** para realizar un seguimiento del número de dedos y cambiar el color que está dibujando el representador dinámico.</span><span class="sxs-lookup"><span data-stu-id="032db-116">A plug-in, **CSyncEventHandlerRTS**, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="032db-117">Con ambos complementos en la pila del complemento RTS, la aplicación Windows Touch Scratchpad representará el contacto principal en negro y el resto de los contactos en los distintos colores.</span><span class="sxs-lookup"><span data-stu-id="032db-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="032db-118">El código siguiente muestra cómo se crea el objeto RTS con compatibilidad con varios puntos de contacto.</span><span class="sxs-lookup"><span data-stu-id="032db-118">The following code shows how the RTS object is created with support for multiple contact points.</span></span>

```C++
IRealTimeStylus* CreateRealTimeStylus(HWND hWnd)
{
    // Check input argument
    if (hWnd == NULL)
    {
        ASSERT(hWnd && L"CreateRealTimeStylus: invalid argument hWnd");
        return NULL;
    }

    // Create RTS object
    IRealTimeStylus* pRealTimeStylus = NULL;
    HRESULT hr = CoCreateInstance(CLSID_RealTimeStylus, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pRealTimeStylus));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to CoCreateInstance of RealTimeStylus");
        return NULL;
    }

    // Attach RTS object to a window
    hr = pRealTimeStylus->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to set window handle");
        pRealTimeStylus->Release();
        return NULL;
    }

    // Register RTS object for receiving multi-touch input.
    IRealTimeStylus3* pRealTimeStylus3 = NULL;
    hr = pRealTimeStylus->QueryInterface(&pRealTimeStylus3);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: cannot access IRealTimeStylus3");
        pRealTimeStylus->Release();
        return NULL;
    }
    hr = pRealTimeStylus3->put_MultiTouchEnabled(TRUE);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to enable multi-touch");
        pRealTimeStylus->Release();
        pRealTimeStylus3->Release();
        return NULL;
    }
    pRealTimeStylus3->Release();

    return pRealTimeStylus;
}
```

<span data-ttu-id="032db-119">El código siguiente muestra cómo se crea y agrega el complemento de representador dinámico al RTS.</span><span class="sxs-lookup"><span data-stu-id="032db-119">The following code shows how the dynamic renderer plug-in is created and added to the RTS.</span></span>

```C++
IDynamicRenderer* CreateDynamicRenderer(IRealTimeStylus* pRealTimeStylus)
{
    // Check input argument
    if (pRealTimeStylus == NULL)
    {
        ASSERT(pRealTimeStylus && L"CreateDynamicRenderer: invalid argument RealTimeStylus");
        return NULL;
    }

    // Get window handle from RTS object
    HWND hWnd = NULL;
    HRESULT hr = pRealTimeStylus->get_HWND((HANDLE_PTR*)&hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to get window handle");
        return NULL;
    }

    // Create DynamicRenderer object
    IDynamicRenderer* pDynamicRenderer = NULL;
    hr = CoCreateInstance(CLSID_DynamicRenderer, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pDynamicRenderer));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to CoCreateInstance of DynamicRenderer");
        return NULL;
    }

    // Add DynamicRenderer to the RTS object as a synchronous plugin
    IStylusSyncPlugin* pSyncDynamicRenderer = NULL;
    hr = pDynamicRenderer->QueryInterface(&pSyncDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to access IStylusSyncPlugin of DynamicRenderer");
        pDynamicRenderer->Release();
        return NULL;
    }

    hr = pRealTimeStylus->AddStylusSyncPlugin(
        0,                      // insert plugin at position 0 in the sync plugin list
        pSyncDynamicRenderer);  // plugin to be inserted - DynamicRenderer
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to add DynamicRenderer to the RealTimeStylus plugins");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    // Attach DynamicRenderer to the same window RTS object is attached to
    hr = pDynamicRenderer->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to set window handle");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    pSyncDynamicRenderer->Release();

    return pDynamicRenderer;
}
```

<span data-ttu-id="032db-120">El código siguiente cambia el color del trazo del lápiz óptico para el controlador de eventos **StylusDown** en **CSyncEventHandlerRTS,** un complemento RTS personalizado.</span><span class="sxs-lookup"><span data-stu-id="032db-120">The following code changes the stylus stroke color for the **StylusDown** event handler in the **CSyncEventHandlerRTS**, a custom RTS plug-in.</span></span>

```C++
HRESULT CSyncEventHandlerRTS::StylusDown(
    IRealTimeStylus* /* piRtsSrc */,
    const StylusInfo* /* pStylusInfo */,
    ULONG /* cPropCountPerPkt */,
    LONG* /* pPacket */,
    LONG** /* ppInOutPkt */)
{
    // Get DrawingAttributes of DynamicRenderer
    IInkDrawingAttributes* pDrawingAttributesDynamicRenderer;
    HRESULT hr = g_pDynamicRenderer->get_DrawingAttributes(&pDrawingAttributesDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to get RTS's drawing attributes");
        return hr;
    }

    // Set new stroke color to the DrawingAttributes of the DynamicRenderer
    // If there are no fingers down, this is a primary contact
    hr = pDrawingAttributesDynamicRenderer->put_Color(GetTouchColor(m_nContacts == 0));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to set color");
        pDrawingAttributesDynamicRenderer->Release();
        return hr;
    }

    pDrawingAttributesDynamicRenderer->Release();

    ++m_nContacts;  // Increment finger-down counter

    return S_OK;
}
```

<span data-ttu-id="032db-121">Cuando el *m_nContacts* se incrementa, cambiará el conjunto de colores en el representador dinámico.</span><span class="sxs-lookup"><span data-stu-id="032db-121">When the *m_nContacts* value is incremented, it will change the color set in the dynamic renderer.</span></span> <span data-ttu-id="032db-122">Los trazos que no son el contacto principal se dibujarán con colores diferentes.</span><span class="sxs-lookup"><span data-stu-id="032db-122">Strokes that are not the primary contact will be drawn with different colors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="032db-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="032db-123">Related topics</span></span>

<span data-ttu-id="032db-124">[Aplicación scratchpad multi touch (RTS/C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS) [aplicación de scratchpad multi touch (RTS/C++),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp) [ejemplos de Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="032db-124">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
