---
description: Modo sin ventana de VMR
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Modo sin ventana de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b137fbc1351f2bbe5ed38673b681e45558675d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360473"
---
# <a name="vmr-windowless-mode"></a>Modo sin ventana de VMR

El modo sin ventanas es la forma preferida para que las aplicaciones representen vídeo en una ventana de la aplicación. En el modo sin ventanas, el representador de mezcla de vídeo no carga su componente de administrador de Windows y, por lo tanto, no es compatible con las interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) o [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . En su lugar, la aplicación proporciona la ventana de reproducción y establece un rectángulo de destino en el área cliente para que la VMR dibuje el vídeo. VMR usa un objeto Clipper de DirectDraw para asegurarse de que el vídeo se recorta en la ventana de la aplicación y no aparece en otras ventanas. VMR no realiza la subclase de la ventana de la aplicación ni instala ningún enlace del sistema o proceso.

En el modo sin ventanas, la secuencia de eventos durante la conexión y la transición al estado de ejecución es la siguiente:

-   El filtro de nivel superior propone un tipo de medio, que la VMR acepta o rechaza.
-   Si se acepta el tipo de medio, el archivo VMR llama al presentador del asignador para obtener una superficie DirectDraw. Si la superficie se crea correctamente, las clavijas Connect y la VMR están listas para realizar la transición al estado de ejecución.
-   Cuando se ejecuta el gráfico de filtros, el descodificador llama a **getBuffer** para obtener un ejemplo multimedia del asignador. VMR consulta al presentador del asignador para asegurarse de que la profundidad de píxeles, el tamaño del rectángulo y otros parámetros de su superficie de DirectDraw son compatibles con el vídeo entrante. Si son compatibles, el VMR devuelve la superficie de DirectDraw al descodificador. Una vez que el descodificador ha descodificado en la superficie, la unidad de sincronización principal de VMR valida las marcas de tiempo. Esta unidad bloquea la llamada de **recepción** hasta que llega el momento de la presentación. En ese momento, la VMR llama a **PresentImage** en el presentador del asignador, que presenta la superficie a la tarjeta gráfica.

En la ilustración siguiente se muestra el VMR en modo sin ventanas con varios flujos de entrada.

![VMR en modo sin ventanas](images/vmr-windowless-mult-streams.png)

**Configuración de VMR-7 para el modo sin ventanas**

Para configurar VMR-7 para el modo sin ventanas, realice todos los pasos siguientes antes de conectar cualquiera de los pin de entrada de VMR:

1.  Cree el filtro y agréguelo al gráfico.
2.  Llame al método [**IVMRFilterConfig:: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) con la \_ marca sin ventana de VMRMode.
3.  Opcionalmente, configure la VMR para varios flujos de entrada mediante una llamada a [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). VMR crea un PIN de entrada para cada flujo. Use la interfaz [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) para establecer el orden Z y otros parámetros para la secuencia. Para obtener más información, consulte [VMR con varias secuencias (modo de combinación)](vmr-with-multiple-streams--mixing-mode.md).

    Si no llama a **SetNumberOfStreams**, el valor predeterminado de VMR-7 es un PIN de entrada. Una vez conectadas las clavijas de entrada, no se puede cambiar el número de clavijas.

4.  Llame a [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) para especificar la ventana en la que aparecerá el vídeo representado.

Una vez completados estos pasos, puede conectar los pin de entrada del filtro VMR. Hay varias maneras de compilar el gráfico, como la conexión directa de los pin, el uso de métodos de conexión inteligentes como [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)o el uso del método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) del generador de gráficos de captura. Para obtener más información, vea [técnicas de Graph-Building generales](general-graph-building-techniques.md).

Para establecer la posición del vídeo dentro de la ventana de la aplicación, llame al método [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) . El método [**IVMRWindowlessControl:: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) devuelve el tamaño de vídeo nativo. Durante la reproducción, la aplicación debe notificar a la VMR los siguientes mensajes de Windows:

-   WM \_ Paint: llame a [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) para volver a dibujar la imagen.
-   WM \_ DISPLAYCHANGE: llame a [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). La VMR toma las medidas necesarias para mostrar el vídeo con la nueva resolución o profundidad de color.
-   \_Tamaño de WM: vuelva a calcular la posición del vídeo y llame de nuevo a [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) si es necesario.

> [!Note]  
> Las aplicaciones MFC deben definir un controlador de mensajes ERASEBKGND de WM vacío \_ o el área de presentación de vídeo no volverá a dibujarse correctamente.

 

**Configuración de VMR-9 para el modo sin ventanas**

Para configurar VMR-9 para el modo sin ventanas, siga los pasos descritos en VMR-7 para el modo sin ventanas, pero use las interfaces [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) y [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) . La única diferencia significativa es que VMR-9 crea cuatro clavijas de entrada de forma predeterminada, en lugar de un PIN de entrada. Por lo tanto, solo tiene que llamar a **SetNumberOfStreams** si está mezclando más de cuatro secuencias de vídeo.

**Código de ejemplo**

En el código siguiente se muestra cómo crear un filtro VMR-7, agregarlo al gráfico de filtros de DirectShow y, a continuación, colocar el VMR en el modo sin ventanas. En el caso de VMR-9, use CLSID \_ VideoMixingRenderer9 en **CoCreateInstance** y las interfaces de VMR-9 correspondientes.


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

[Usar el modo sin ventanas](using-windowless-mode.md)
</dt> </dl>

 

 



