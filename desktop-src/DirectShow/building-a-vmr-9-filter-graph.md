---
description: Creación de un filtro VMR-9 Graph
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Creación de un filtro VMR-9 Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161676"
---
# <a name="building-a-vmr-9-filter-graph"></a>Creación de un filtro VMR-9 Graph

Dado que el filtro del representador de mezcla de vídeo 9 (VMR-9) no es el representador de vídeo predeterminado, una aplicación que usa VMR-9 debe agregarlo explícitamente al gráfico y conectarlo. En esta sección se presentan dos enfoques diferentes para crear gráficos de filtro con VMR-9.

Uso de Capture Graph Builder

Capture Graph Builder es un objeto auxiliar para crear gráficos de filtro personalizados. Puede usarlo para compilar gráficos de VMR-9 como se muestra a continuación:

1.  Cree e inicialice capture Graph Builder, como se describe en el tema Acerca de la captura [Graph Builder](about-the-capture-graph-builder.md).
2.  Llame a CoCreateInstance para crear vmr-9:
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  Llame [**a IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) en filter Graph Manager para agregar VMR-9 al gráfico de filtros:
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  Llame [**a IGraphBuilder::AddSourceFilter para**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) agregar un filtro de código fuente para el archivo de vídeo:
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  Llame al [**método ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para representar la secuencia de vídeo en vmr:
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  Opcionalmente, llame a RenderStream de nuevo para representar la secuencia de audio:
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

Puede mezclar varias secuencias de vídeo llamando a AddSourceFilter y RenderStream para cada archivo de código fuente.

Uso del Administrador de Graph filtros

Si prefiere no usar Capture Graph Builder, puede crear un gráfico VMR-9 con solo usar métodos en filter Graph Manager, como se muestra a continuación:

1.  Cree el VMR-9 y agrégrélo al gráfico, como se muestra en el procedimiento anterior.
2.  Use AddSourceFilter para agregar un filtro de origen para el archivo de vídeo, como se muestra en el procedimiento anterior.
3.  Si desea representar el audio, cree una instancia del filtro [Representador de Direct Sound](directsound-renderer-filter.md) y agrétrelo al gráfico de filtros.
4.  Use el método IBaseFilter::EnumPins para buscar un pin de salida en el filtro de origen. Consulte [Enumeración de pins](enumerating-pins.md) para obtener más información.
5.  Consulte el Administrador de Graph filtros para la interfaz IFilterGraph2.
6.  Llame [**a IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) con la marca \_ AM RENDEREX \_ RENDERTOEXISTINGRENDERERS. Esta llamada representa el pin de salida, usando solo los filtros de representador que ya están en el gráfico, en este caso, VMR-9 y Direct Sound Renderer. Esto evita que la lógica de Conectar inteligente agregue el representador de vídeo predeterminado al gráfico, lo que dejaría el VMR-9 sin conectar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de gráficos con capture Graph Builder](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



