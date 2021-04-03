---
description: Obtener una vista previa del proyecto
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Obtener una vista previa del proyecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997943"
---
# <a name="previewing-the-project"></a>Obtener una vista previa del proyecto

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Para obtener una vista previa del proyecto, necesita un componente denominado *motor de representación*, que genera un gráfico de filtros de DirectShow a partir de una escala de tiempo. El gráfico de filtros es lo que realmente representa el proyecto. Puede usar el motor de representación para obtener una vista previa de un proyecto o para escribir el archivo de salida final.

En este artículo no se explica con detalle el motor de representación. Para la versión preliminar, solo necesita algunas llamadas a métodos. Puede encontrar una explicación más completa, incluida la forma de escribir archivos de salida, en la [representación de un proyecto](rendering-a-project.md). En el ejemplo de código siguiente se muestra cómo crear un gráfico de vista previa.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



Cree el motor de representación mediante la función **CoCreateInstance** . A continuación, llame a los métodos siguientes en la interfaz [**IRenderEngine**](irenderengine.md) del motor de representación:

-   [**SetTimelineObject**](irenderengine-settimelineobject.md). Especifica la escala de tiempo que se va a usar.
-   [**ConnectFrontEnd**](irenderengine-connectfrontend.md). Crea un gráfico de filtro parcial, con un PIN de salida para cada grupo de la escala de tiempo.
-   [**RenderOutputPins**](irenderengine-renderoutputpins.md). Completa el gráfico de vista previa conectando cada pin de salida a un representador de vídeo o audio.

Una vez creado el gráfico, puede obtener una vista previa del mismo ejecutando el gráfico, como haría con cualquier gráfico de filtros de DirectShow. En primer lugar, obtenga un puntero al gráfico de filtros llamando al método [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) .


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



Consulte el gráfico de filtro para las interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) . Use estas dos interfaces para ejecutar el gráfico y esperar a que se complete la reproducción. Para obtener una explicación de cómo utilizar estas interfaces, vea [Cómo reproducir un archivo](how-to-play-a-file.md) y [responder a eventos](responding-to-events.md). En el código siguiente se muestra una manera de utilizar estas interfaces.


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



El código de este ejemplo bloquea la ejecución del programa hasta que se completa la reproducción, debido al parámetro infinito en la llamada al método [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) . Sin embargo, si se produce algún problema durante la reproducción, podría provocar que el programa dejara de responder. En una aplicación real, use un bucle de mensajes para esperar a que se complete la reproducción. También se recomienda proporcionar al usuario una manera de interrumpir la reproducción.

Cuando termine de usar el motor de representación, llame siempre al método [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) . Este método elimina el gráfico de filtro y libera todos los recursos mantenidos por el motor de representación.


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cargar y obtener una vista previa de un proyecto](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



