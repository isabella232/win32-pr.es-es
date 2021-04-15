---
description: Escritura de un archivo de Windows Media en DES
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Escritura de un archivo de Windows Media en DES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689668"
---
# <a name="writing-a-windows-media-file-in-des"></a>Escritura de un archivo de Windows Media en DES

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En esta sección se describe cómo escribir un archivo de Windows Media mediante los [servicios de edición de DirectShow](directshow-editing-services.md) (des).

> [!IMPORTANT]
> No utilice el motor de representación inteligente para escribir archivos de Windows Media. Use siempre el motor de representación básico (CLSID \_ RenderEngine).

 

Para escribir un archivo de Windows Media, haga lo siguiente:

1.  Llame a **SetSite** en el motor de representación con un puntero al proveedor de claves.
2.  Cree el front-end del gráfico. (Vea [representar un proyecto](rendering-a-project.md)).
3.  Cree el filtro del [escritor ASF de WM](wm-asf-writer-filter.md) y agréguelo al gráfico.
4.  Use la interfaz [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) en el filtro de escritor ASF de WM para establecer el nombre de archivo.
5.  Configure el escritor ASF de WM para que use un perfil de Windows Media. Cada perfil tiene un número predefinido de secuencias. Debe elegir un perfil que coincida con los grupos del proyecto.

    La interfaz [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) contiene algunos métodos diferentes para configurar el perfil. Por ejemplo, el método **ConfigureFilterUsingProfileGuid** especifica un perfil de sistema como un GUID. O bien, puede usar los métodos de formato de Windows Media para obtener un puntero **IWMProfile** y, a continuación, llamar a [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile). Para obtener más información, consulte [configuración del escritor ASF](configuring-the-asf-writer.md).

6.  Conecte el front-end al escritor ASF. El front-end del gráfico contiene un PIN de salida para cada grupo. Suponiendo que haya especificado un perfil compatible, el escritor ASF debe tener un conjunto coincidente de clavijas de entrada. Conecte cada pin de salida al pin de entrada correspondiente. La forma más fácil de hacerlo es usar el método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) . En primer lugar, cree una nueva instancia del [generador de gráficos de captura](capture-graph-builder.md) e inicialícela con un puntero al administrador de gráficos de filtro:

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    A continuación, recupere el PIN de salida para cada grupo mediante una llamada al método [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) . Llame a **RenderStream** para conectar el PIN al escritor ASF:

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Windows Media con los servicios de edición de DirectShow](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



