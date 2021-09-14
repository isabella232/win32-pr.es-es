---
description: Uso del modo sin ventanas
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Uso del modo sin ventanas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160107"
---
# <a name="using-windowless-mode"></a>Uso del modo sin ventanas

Tanto el filtro de representador de mezcla de vídeo [7](video-mixing-renderer-filter-7.md) (VMR-7) como el filtro de representador de mezcla de vídeo [9](video-mixing-renderer-filter-9.md) (VMR-9) admiten el modo sin *ventanas,* lo que representa una mejora importante sobre la interfaz [**IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) En este tema se describen las diferencias entre el modo sin ventana y el modo de ventana, y cómo usar el modo sin ventana.

Para mantener la compatibilidad con versiones anteriores con las aplicaciones existentes, vmr tiene como valor predeterminado el modo de ventana. En modo de ventana, el representador crea su propia ventana para mostrar el vídeo. Normalmente, la aplicación establece la ventana de vídeo como un elemento secundario de la ventana de la aplicación. Sin embargo, la existencia de una ventana de vídeo independiente provoca algunos problemas:

-   Lo más importante es que existe la posibilidad de interbloqueos si se envían mensajes de ventana entre subprocesos.
-   El Administrador Graph filtros debe reenviar determinados mensajes de ventana, como WM \_ PAINT, al representador de vídeo. La aplicación debe usar la implementación del Administrador de filtros Graph de [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (y no la del representador de vídeo), de modo que el Administrador de filtros Graph mantenga el estado interno correcto.
-   Para recibir eventos de mouse o teclado desde la ventana de vídeo, la aplicación debe establecer una purga de *mensajes,* lo que hace que la ventana de vídeo reenvía estos mensajes a la aplicación.
-   Para evitar problemas de recorte, la ventana de vídeo debe tener los estilos de ventana adecuados.

El modo sin ventanas evita estos problemas al hacer que el VMR se dibuje directamente en el área cliente de la ventana de la aplicación, mediante DirectDraw para recortar el rectángulo de vídeo. El modo sin ventanas reduce significativamente la posibilidad de interbloqueos. Además, la aplicación no tiene que establecer la ventana de propietario ni los estilos de ventana. De hecho, cuando vmr está en modo sin ventanas, ni siquiera expone la [**interfaz IVideoWindow,**](/windows/desktop/api/Control/nn-control-ivideowindow) que ya no es necesaria.

Para usar el modo sin ventanas, debe configurar explícitamente el VMR. Sin embargo, encontrará que es más flexible y fácil de usar que el modo con ventanas.

El filtro VMR-7 y el filtro VMR-9 exponen interfaces diferentes, pero los pasos son equivalentes para cada una.

## <a name="configure-the-vmr-for-windowless-mode"></a>Configuración de VMR para el modo sin ventanas

Para invalidar el comportamiento predeterminado de vmr, configure el VMR antes de compilar el gráfico de filtros:

**VMR-7**

1.  Cree el Administrador de Graph filtros.
2.  Cree vmr-7 y agrégrelo al gráfico de filtros.
3.  Llame [**a IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) en VMR-7 con la marca sin ventanas **VMRMode. \_**
4.  Consulte vmr-7 para la [**interfaz IVMRWindowlessControl.**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol)
5.  Llame [**a IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) en VMR-7. Especifique un identificador en la ventana donde debe aparecer el vídeo.

**VMR-9**

1.  Cree el Administrador de Graph filtros.
2.  Cree el VMR-9 y agrégrélo al gráfico de filtros.
3.  Llame [**a IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) en VMR-9 con la marca sin ventanas **VMR9Mode. \_**
4.  Consulte vmr-9 para la [**interfaz IVMRWindowlessControl9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9)
5.  Llame [**a IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) en VMR-9. Especifique un identificador en la ventana donde debe aparecer el vídeo.

Ahora compile el resto del gráfico de filtro mediante una llamada [**a IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) u otros métodos de creación de grafos. Filter Graph Manager usa automáticamente la instancia de la VMR que agregó al gráfico. (Para obtener más información sobre por qué ocurre esto, vea [Intelligent Conectar).](intelligent-connect.md)

En el código siguiente se muestra una función auxiliar que crea VMR-7, la agrega al gráfico y configura el modo sin ventanas.


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



Esta función supone que solo se muestra una secuencia de vídeo y no se mezcla un mapa de bits estático en el vídeo. Para más información, consulte [Modo sin ventanas de VMR.](vmr-windowless-mode.md) Llamaría a esta función como se muestra a continuación:


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a>Posición del vídeo

Después de configurar vmr, el siguiente paso es establecer la posición del vídeo. Hay dos rectángulos a tener en cuenta: el *rectángulo de origen* y el rectángulo *de* destino. El rectángulo de origen define qué parte del vídeo se va a mostrar. El rectángulo de destino especifica la región en el área cliente de la ventana que contendrá el vídeo. El VMR recorta la imagen de vídeo al rectángulo de origen y ajusta la imagen recortada para ajustarla al rectángulo de destino.

**VMR-7**

1.  Llame al [**método IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) para especificar ambos rectángulos.
2.  El rectángulo de origen debe ser igual o menor que el tamaño del vídeo nativo; Puede usar el [**método IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) para obtener el tamaño del vídeo nativo.

**VMR-9**

1.  Llame al [**método IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) para especificar ambos rectángulos.
2.  El rectángulo de origen debe ser igual o menor que el tamaño del vídeo nativo; Puede usar el [**método IVMRWindowlessControl9::GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) para obtener el tamaño del vídeo nativo.

Por ejemplo, el código siguiente establece los rectángulos de origen y destino para VMR-7. Establece el rectángulo de origen igual a toda la imagen de vídeo y el rectángulo de destino igual al área cliente de la ventana completa:


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



Si desea grabar para ocupar una parte más pequeña del área de cliente, modifique el *parámetro rcDest.* Si desea recortar la imagen de vídeo, modifique el *parámetro rcSrc.*

## <a name="handle-window-messages"></a>Controlar mensajes de ventana

Dado que vmr no tiene su propia ventana, se le debe notificar si necesita volver a dibujar o cambiar el tamaño del vídeo. Responda a los siguientes mensajes de ventana mediante una llamada a los métodos de VMR enumerados.

**VMR-7**

1.  [**WM \_ PAINT**](../gdi/wm-paint.md). Llame [**a IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo). Este método hace que VMR-7 vuelva a dibujar el fotograma de vídeo más reciente.
2.  [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): llame [**a IVMRWindowlessControl::D isplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). Este método notifica al VMR-7 que el vídeo debe mostrarse con una nueva resolución o profundidad de color.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) o [**WM \_ WINDOWPOSCHANGED:**](../winmsg/wm-windowposchanged.md)recalcula la posición del vídeo y llama a [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) para actualizar la posición, si es necesario.

**VMR-9**

1.  [**WM \_ PAINT**](../gdi/wm-paint.md). Llame [**a IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo). Este método hace que VMR-9 vuelva a dibujar el fotograma de vídeo más reciente.
2.  [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): llame [**a IVMRWindowlessControl9::D isplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged). Este método notifica a VMR-9 que el vídeo debe mostrarse con una nueva resolución o profundidad de color.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) o [**WM \_ WINDOWPOSCHANGED:**](../winmsg/wm-windowposchanged.md)recalcula la posición del vídeo y llama a [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) para actualizar la posición, si es necesario.

> [!Note]  
> El controlador predeterminado para el [**mensaje \_ WM WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) envía un [**mensaje WM \_ SIZE.**](../winmsg/wm-size.md) Pero si la aplicación intercepta **WM \_ WINDOWPOSCHANGED** y no lo pasa a [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)debe llamar a **SetVideoPosition** en el controlador **WM \_ WINDOWPOSCHANGED,** además del controlador **WM \_ SIZE.**

 

En el ejemplo siguiente se muestra un [**controlador de mensajes WM \_ PAINT.**](../gdi/wm-paint.md) Pinta una región definida por el rectángulo de cliente menos el rectángulo de vídeo. No dibuje en el rectángulo de vídeo, ya que el VMR lo pintará, lo que provocará un parpadeo. Por la misma razón, no establezca un pincel de fondo en la clase de ventana.


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



Aunque debe responder a mensajes [**DE WM \_ PAINT,**](../gdi/wm-paint.md) no es necesario hacer nada entre los **mensajes DE WM \_ PAINT** para actualizar el vídeo. Como se muestra en este ejemplo, el modo sin ventanas permite tratar la imagen de vídeo simplemente como una región de dibujo automático en la ventana.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el representador de mezcla de vídeo](using-the-video-mixing-renderer.md)
</dt> <dt>

[Representación de vídeo](video-rendering.md)
</dt> </dl>

 

 
