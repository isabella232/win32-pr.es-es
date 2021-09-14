---
description: Vista previa de la Project
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Vista previa de la Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254205"
---
# <a name="previewing-the-project"></a>Vista previa de la Project

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Para obtener una vista previa del proyecto, necesita un componente denominado motor de representación *,* que compila un DirectShow gráfico de filtros a partir de una escala de tiempo. El gráfico de filtro es lo que representa realmente el proyecto. Puede usar el motor de representación para obtener una vista previa de un proyecto o para escribir el archivo de salida final.

En este artículo no se detalla el motor de representación. Para la versión preliminar, solo necesita algunas llamadas de método. Puede encontrar una explicación más exhaustiva, incluido cómo escribir archivos de salida, en [Representación de un Project](rendering-a-project.md). En el ejemplo de código siguiente se muestra cómo construir un gráfico de vista previa.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



Cree el motor de representación mediante la **función CoCreateInstance.** A continuación, llame a los métodos siguientes en la [**interfaz IRenderEngine**](irenderengine.md) del motor de representación:

-   [**SetTimelineObject**](irenderengine-settimelineobject.md). Especifica la escala de tiempo que se usará.
-   [**ConnectFrontEnd**](irenderengine-connectfrontend.md). Crea un gráfico de filtro parcial, con un pin de salida para cada grupo de la escala de tiempo.
-   [**RenderOutputPins**](irenderengine-renderoutputpins.md). Completa el gráfico de vista previa conectando cada pin de salida a un representador de vídeo o audio.

Una vez creado el gráfico, puede obtener una vista previa del proyecto mediante la ejecución del gráfico, como haría con cualquier gráfico DirectShow filtro. En primer lugar, obtenga un puntero al gráfico de filtro llamando al [**método IRenderEngine::GetFilterGraph.**](irenderengine-getfiltergraph.md)


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



Consulte el gráfico de filtros para las [**interfaces IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) [**e IMediaEvent.**](/windows/desktop/api/Control/nn-control-imediaevent) Use estas dos interfaces para ejecutar el gráfico y esperar a que se complete la reproducción. Para obtener una explicación de cómo usar estas interfaces, vea Cómo reproducir [un archivo](how-to-play-a-file.md) y Responder a [eventos](responding-to-events.md). El código siguiente muestra una manera de usar estas interfaces.


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



El código de este ejemplo bloquea la ejecución del programa hasta que se completa la reproducción, debido al parámetro INFINITE en la llamada al método [**IMediaEvent::WaitForCompletion.**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) Sin embargo, si algo sale mal durante la reproducción, podría hacer que el programa dejara de responder. En una aplicación real, use un bucle de mensajes para esperar a que se complete la reproducción. También se recomienda proporcionar al usuario una manera de interrumpir la reproducción.

Cuando termine de usar el motor de representación, llame siempre al [**método IRenderEngine::ScrapIt.**](irenderengine-scrapit.md) Este método elimina el gráfico de filtros y libera los recursos que mantiene el motor de representación.


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Carga y vista previa de un Project](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



