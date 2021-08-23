---
description: Vista previa de un Project
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Vista previa de un Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159303c175c459b4d5d93ba4c7b4b2622caddac2a35d3474a3059ac703d62645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583565"
---
# <a name="previewing-a-project"></a>Vista previa de un Project

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Para obtener una vista previa de un proyecto, primero **llame a CoCreateInstance** para crear una instancia del motor de representación básico. El identificador de clase es CLSID \_ RenderEngine. A continuación, [**llame al método IRenderEngine::SetTimelineObject**](irenderengine-settimelineobject.md) para especificar la escala de tiempo que está representando.

La primera vez que obtenga una vista previa de la escala de tiempo, realice las siguientes llamadas en el orden indicado:

1.  Llame [**a IRenderEngine::SetRenderRange para**](irenderengine-setrenderrange.md) especificar qué parte de la escala de tiempo se va a obtener en vista previa. (Opcional)
2.  Llame [**a IRenderEngine::ConnectFrontEnd para**](irenderengine-connectfrontend.md) compilar el front-end del gráfico.
3.  Llame [**a IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md). Este método conecta cada pin de salida a un representador de vídeo o representador de audio, completando el gráfico.

En el ejemplo de código siguiente se muestran estos pasos:


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



Ahora ejecute el gráfico de filtro. En primer lugar, llame al [**método IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) para recuperar un puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) de Filter Graph Manager. A continuación, consulte filter Graph Manager para la interfaz [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) y llame a [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), como se muestra en el código siguiente:


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



Use la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) de Filter Graph Manager para esperar a que se complete la versión preliminar. También puede buscar el gráfico mediante la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) de Filter Graph Manager, tal como lo haría con un gráfico de reproducción de archivos.

Para obtener una vista previa del proyecto de nuevo, busque el gráfico de nuevo en el tiempo cero y llame a **Ejecutar de** nuevo. Si cambia el contenido de la escala de tiempo, haga lo siguiente:

1.  Llame **a SetRenderRange.** (Opcional)
2.  Llame **a ConnectFrontEnd.**
3.  Si el **método ConnectFrontEnd** devuelve S \_ WARN \_ OUTPUTRESET, llame a **RenderOutputPins**. (Si **ConnectFrontEnd devuelve** S \_ De acuerdo, puede omitir este paso).
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



Para obtener un ejemplo completo que carga y muestra una vista previa de un archivo de proyecto, vea Carga y vista [previa de un Project](loading-and-previewing-a-project.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de proyectos de edición de vídeo](managing-video-editing-projects.md)
</dt> <dt>

[Representación de un Project](rendering-a-project.md)
</dt> </dl>

 

 



