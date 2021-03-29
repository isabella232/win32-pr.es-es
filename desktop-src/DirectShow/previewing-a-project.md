---
description: Obtener una vista previa de un proyecto
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Obtener una vista previa de un proyecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd9d299a99a0a7315cec986fbc044d427385647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359945"
---
# <a name="previewing-a-project"></a>Obtener una vista previa de un proyecto

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Para obtener una vista previa de un proyecto, llame primero a **CoCreateInstance** para crear una instancia del motor de representación básico. El identificador de clase es CLSID \_ RenderEngine. A continuación, llame al método [**IRenderEngine:: SetTimelineObject**](irenderengine-settimelineobject.md) para especificar la escala de tiempo que está representando.

La primera vez que obtenga una vista previa de la escala de tiempo, realice las siguientes llamadas en el orden indicado:

1.  Llame a [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md) para especificar qué parte de la escala de tiempo se va a mostrar en la vista previa. (Opcional)
2.  Llame a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para compilar el front-end del gráfico.
3.  Llame a [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md). Este método conecta cada pin de salida a un representador de vídeo o representador de audio y completa el gráfico.

En el ejemplo de código siguiente se muestran estos pasos:


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



Ahora, ejecute el gráfico de filtro. En primer lugar, llame al método [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) para recuperar un puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del administrador de gráficos de filtro. A continuación, consulte el administrador de gráficos de filtro para la interfaz [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) y llame a [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), tal como se muestra en el código siguiente:


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



Use la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) del administrador de gráficos de filtro para esperar a que se complete la vista previa. También puede buscar el gráfico mediante la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del administrador de gráficos de filtro, tal como lo haría con un gráfico de reproducción de archivos.

Para volver a obtener una vista previa del proyecto, busque el gráfico de nuevo en el tiempo cero y vuelva a llamar a **Ejecutar** . Si cambia el contenido de la escala de tiempo, haga lo siguiente:

1.  Llame a **SetRenderRange**. (Opcional)
2.  Llame a **ConnectFrontEnd**.
3.  Si el método **ConnectFrontEnd** devuelve S \_ WARN \_ OUTPUTRESET, llame a **RenderOutputPins**. (Si **ConnectFrontEnd** devuelve S \_ Bien, puede omitir este paso).
4.  Vuelva a buscar el gráfico en el tiempo cero.
5.  Ejecute el gráfico.

En el ejemplo siguiente se muestran estos pasos:


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



Para obtener un ejemplo completo en el que se carga y se muestra una vista previa de un archivo de proyecto, vea [cargar y obtener una vista previa de un proyecto](loading-and-previewing-a-project.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrar proyectos de edición de vídeo](managing-video-editing-projects.md)
</dt> <dt>

[Representar un proyecto](rendering-a-project.md)
</dt> </dl>

 

 



