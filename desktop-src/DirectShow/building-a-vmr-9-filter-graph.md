---
description: Creación de un gráfico de filtros VMR-9
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Creación de un gráfico de filtros VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906741"
---
# <a name="building-a-vmr-9-filter-graph"></a>Creación de un gráfico de filtros VMR-9

Dado que el filtro de representador de mezcla de vídeo 9 (VMR-9) no es el representador de vídeo predeterminado, una aplicación que use VMR-9 debe agregarlo explícitamente al gráfico y conectarlo. En esta sección se presentan dos enfoques diferentes para crear gráficos de filtros con VMR-9.

Usar el generador de gráficos de captura

El generador de gráficos de captura es un objeto auxiliar para crear gráficos de filtros personalizados. Puede usarlo para compilar gráficos VMR-9 como se indica a continuación:

1.  Cree e inicialice el generador de gráficos de captura, tal y como se describe en el tema [sobre el generador de gráficos de captura](about-the-capture-graph-builder.md).
2.  Llame a CoCreateInstance para crear el método VMR-9:
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  Llame a [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) en el administrador de gráficos de filtro para agregar el VMR-9 al gráfico de filtros:
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  Llame a [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para agregar un filtro de origen para el archivo de vídeo:
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  Llame al método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para representar la secuencia de vídeo en la VMR:
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  Opcionalmente, vuelva a llamar a RenderStream para representar la secuencia de audio:
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

Puede mezclar varias secuencias de vídeo llamando a AddSourceFilter y RenderStream para cada archivo de código fuente.

Usar el administrador de gráficos de filtro

Si prefiere no usar el generador de gráficos de captura, puede crear un grafo de VMR-9 simplemente mediante métodos en el administrador de gráficos de filtro, como se indica a continuación:

1.  Cree el VMR-9 y agréguelo al gráfico, tal como se muestra en el procedimiento anterior.
2.  Use AddSourceFilter para agregar un filtro de origen para el archivo de vídeo, tal como se muestra en el procedimiento anterior.
3.  Si desea representar el audio, cree una instancia del filtro de [representador de DirectSound](directsound-renderer-filter.md) y agréguela al gráfico de filtros.
4.  Use el método IBaseFilter:: EnumPins para buscar un PIN de salida en el filtro de origen. Consulte [enumeración de PIN](enumerating-pins.md) para obtener más información.
5.  Consulte el administrador de gráficos de filtro para la interfaz IFilterGraph2.
6.  Llame a [**IFilterGraph2:: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) con la \_ marca AM RenderEx \_ RENDERTOEXISTINGRENDERERS. Esta llamada representa el PIN de salida, usando solo los filtros de representador que ya están en el gráfico, en este caso, VMR-9 y el representador de DirectSound. De esta forma, se evita que la lógica de conexión inteligente agregue el representador de vídeo predeterminado al gráfico, lo que dejaría que VMR-9 estuviera sin conexión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Generar gráficos con el generador de gráficos de captura](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



