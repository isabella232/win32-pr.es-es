---
title: Windows Touch Scratchpad con el ejemplo de lápiz en tiempo real (C++)
description: Revise un ejemplo de C++ de Windows Touch Scratchpad (MTScratchpadRTStylus), que muestra cómo usar los mensajes de Windows Touch para dibujar seguimientos de los puntos táctiles en una ventana.
ms.assetid: c72ddc71-48b7-4c26-af2b-10919038eaf8
keywords:
- Windows Touch,ejemplos de código
- Windows Touch, código de ejemplo
- Windows Ejemplos de Touch y Scratchpad
- Ejemplos de Scratchpad
- Windows Objeto Touch,Real-time Stylus (RTS)
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 8ae407240b939f1afe70a976c995e244521cf51ed9103ac5601fdfa817ddf9e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089815"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Windows Touch Scratchpad con el ejemplo de lápiz en tiempo real (C++)

El ejemplo Windows Touch Scratchpad[(MTScratchpadRTStylus)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)muestra cómo usar los mensajes de Windows Touch para dibujar seguimientos de los puntos táctiles en una ventana. El seguimiento del dedo principal, el que se ha puesto primero en el digitalizador, se dibuja en negro. Los dedos secundarios se dibujan en otros seis colores: rojo, verde, azul, aguaz, rojo y amarillo. En la siguiente captura de pantalla se muestra el aspecto de la aplicación mientras se ejecuta.

![captura de pantalla que muestra el ejemplo de scratchpad táctil de Windows con el lápiz óptico en tiempo real, con una línea verde, roja, tres negra y azul en la pantalla](images/mtscratchpadrtstylus.png)

En este ejemplo, se crea el objeto Lápiz en tiempo real (RTS) y se habilita la compatibilidad con varios puntos de contacto. Se agrega un complemento DynamicRenderer al RTS para representar el contenido. Se implementa un complemento, **CSyncEventHandlerRTS,** para realizar un seguimiento del número de dedos y cambiar el color que está dibujando el representador dinámico. Con ambos complementos en la pila del complemento RTS, la aplicación Windows Touch Scratchpad representará el contacto principal en negro y el resto de los contactos en los distintos colores.

El código siguiente muestra cómo se crea el objeto RTS con compatibilidad con varios puntos de contacto.

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

El código siguiente muestra cómo se crea y agrega el complemento de representador dinámico al RTS.

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

El código siguiente cambia el color del trazo del lápiz óptico para el controlador de eventos **StylusDown** en **CSyncEventHandlerRTS,** un complemento RTS personalizado.

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

Cuando el *m_nContacts* se incrementa, cambiará el conjunto de colores en el representador dinámico. Los trazos que no son el contacto principal se dibujarán con colores diferentes.

## <a name="related-topics"></a>Temas relacionados

Aplicación scratchpad multi touch [(RTS/C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)aplicación de scratchpad multi touch [(RTS/C++),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)Windows [touch samples](windows-touch-samples.md)
