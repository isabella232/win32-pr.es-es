---
description: Modo sin ventanas de VMR
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Modo sin ventanas de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193f672e0fc1e3dced4bdff16da0e85123079eb94f2ac3c5fdb302b67c9432b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830594"
---
# <a name="vmr-windowless-mode"></a>Modo sin ventanas de VMR

El modo sin ventanas es la manera preferida para que las aplicaciones representen vídeo dentro de una ventana de aplicación. En el modo sin ventanas, el representador de mezcla de vídeo no carga su componente Administrador de ventanas y, por tanto, no admite las interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) o [**IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) En su lugar, la aplicación proporciona la ventana de reproducción y establece un rectángulo de destino en el área cliente para que vmr dibuje el vídeo. VmR usa un objeto de recorte DirectDraw para asegurarse de que el vídeo se recorta en la ventana de la aplicación y no aparece en ninguna otra ventana. El VMR no crea subclases de la ventana de la aplicación ni instala ningún enlace de sistema o proceso.

En modo sin ventanas, la secuencia de eventos durante la conexión y la transición al estado de ejecución es la siguiente:

-   El filtro ascendente propone un tipo de medio, que el VMR acepta o rechaza.
-   Si se acepta el tipo de medio, vmr llama al asignador-presentador para obtener una superficie de DirectDraw. Si la superficie se crea correctamente, los pines se conectan y el VMR está listo para la transición al estado de ejecución.
-   Cuando se ejecuta el gráfico de filtros, el descodificador llama a **GetBuffer** para obtener un ejemplo multimedia del asignador. El VMR consulta al asignador-presentador para asegurarse de que la profundidad de píxeles, el tamaño del rectángulo y otros parámetros de su superficie de DirectDraw son compatibles con el vídeo entrante. Si son compatibles, el VMR devuelve la superficie de DirectDraw al descodificador. Una vez descodificado el descodificador en la superficie, la unidad de sincronización principal de VMR valida las marcas de tiempo. Esta unidad bloquea la **llamada Receive** hasta que llega el tiempo de presentación. En ese momento, el VMR llama a **PresentImage** en el asignador-presentador, que presenta la superficie a la tarjeta gráfica.

En la ilustración siguiente se muestra vmr en modo sin ventanas con varios flujos de entrada.

![vmr en modo sin ventanas](images/vmr-windowless-mult-streams.png)

**Configuración de VMR-7 para el modo sin ventanas**

Para configurar VMR-7 para el modo sin ventanas, realice todos los pasos siguientes antes de conectar cualquiera de los pines de entrada del VMR:

1.  Cree el filtro y agrégrélo al gráfico.
2.  Llame al [**método IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) con la marca sin ventanas VMRMode. \_
3.  Opcionalmente, configure vmr para varios flujos de entrada mediante una llamada [**a IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). VmR crea un pin de entrada para cada secuencia. Use la [**interfaz IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) para establecer el orden Z y otros parámetros para la secuencia. Para obtener más información, [consulte VMR con varias Secuencias (modo de combinación).](vmr-with-multiple-streams--mixing-mode.md)

    Si no llama a **SetNumberOfStreams,** el valor predeterminado de VMR-7 es un pin de entrada. Una vez conectadas las clavijas de entrada, no se puede cambiar el número de pines.

4.  Llame [**a IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) para especificar la ventana en la que aparecerá el vídeo representado.

Una vez completados estos pasos, puede conectar los pines de entrada del filtro de VMR. Hay varias maneras de compilar el grafo, como conectar los pines directamente, usar métodos de Intelligent Conectar como [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)o usar el método [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) de Capture Graph Builder. Para obtener más información, [vea General Graph-Building Techniques](general-graph-building-techniques.md).

Para establecer la posición del vídeo en la ventana de la aplicación, llame al método [**IVMRWindowlessControl::SetVideoPosition.**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) El [**método IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) devuelve el tamaño del vídeo nativo. Durante la reproducción, la aplicación debe notificar al VMR los siguientes Windows mensajes:

-   WM \_ PAINT: llame [**a IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) para volver a dibujar la imagen.
-   WM \_ DISPLAYCHANGE: llame [**a IVMRWindowlessControl::D isplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). VmR realiza las acciones necesarias para mostrar el vídeo con la nueva resolución o profundidad de color.
-   WM \_ SIZE: vuelva a calcular la posición del vídeo y llame a [**SetVideoPosition de**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) nuevo si es necesario.

> [!Note]  
> Las aplicaciones MFC deben definir un controlador de mensajes WM ERASEBNDND vacío o el área de presentación del vídeo no se \_ volverá a dibujar correctamente.

 

**Configuración de VMR-9 para el modo sin ventanas**

Para configurar VMR-9 para el modo sin ventanas, siga los pasos descritos para VMR-7 para el modo sin ventanas, pero use las interfaces [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) e [**IVMRWindowlessControl9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) La única diferencia significativa es que VMR-9 crea cuatro pines de entrada de forma predeterminada, en lugar de un pin de entrada. Por lo tanto, solo tiene que llamar a **SetNumberOfStreams** si va a mezclar más de cuatro secuencias de vídeo.

**Código de ejemplo**

El código siguiente muestra cómo crear un filtro VMR-7, agregarlo al gráfico de filtros DirectShow y, a continuación, poner vmr en modo sin ventanas. Para VMR-9, use CLSID \_ VideoMixingRenderer9 en **CoCreateInstance** y las interfaces VMR-9 correspondientes.


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del modo sin ventanas](using-windowless-mode.md)
</dt> </dl>

 

 



