---
description: Escribir un archivo Windows multimedia en DES
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Escribir un archivo Windows multimedia en DES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05b954ae6046bb61027bd3e7f63bcd2fcaafa35020bc0a8a1bed278b99731ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650495"
---
# <a name="writing-a-windows-media-file-in-des"></a>Escribir un archivo Windows multimedia en DES

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En esta sección se describe cómo escribir un archivo Windows multimedia mediante [DirectShow Editing Services](directshow-editing-services.md) (DES).

> [!IMPORTANT]
> No use el motor de representación inteligente para escribir Windows archivos multimedia. Use siempre el motor de representación básico (CLSID \_ RenderEngine).

 

Para escribir un Windows multimedia, haga lo siguiente:

1.  Llame **a SetSite** en el motor de representación, con un puntero al proveedor de claves.
2.  Cree el front-end del gráfico. (Vea [Representación de un Project](rendering-a-project.md)).
3.  Cree el [filtro WM ASF Writer](wm-asf-writer-filter.md) y agrégrélo al gráfico.
4.  Use la [**interfaz IFileSinkFilter en**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) el filtro WM ASF Writer para establecer el nombre de archivo.
5.  Configure WM ASF Writer para usar un perfil Windows media. Cada perfil tiene un número predefinido de secuencias. Debe elegir un perfil que coincida con los grupos del proyecto.

    La [**interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) contiene algunos métodos diferentes para establecer el perfil. Por ejemplo, el **método ConfigureFilterUsingProfileGuid** especifica un perfil de sistema como GUID. O bien, puede usar Windows media format para obtener un puntero **IWMProfile** y, a continuación, llamar a [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile). Para obtener más información, [vea Configuring the ASF Writer](configuring-the-asf-writer.md).

6.  Conectar el front-end a ASF Writer. El front-end del gráfico contiene un pin de salida para cada grupo. Suponiendo que especificó un perfil compatible, ASF Writer debe tener un conjunto de pines de entrada correspondientes. Conectar cada pin de salida al pin de entrada correspondiente. La manera más fácil de hacerlo es usar el [**método ICaptureGraphBuilder2::RenderStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) En primer lugar, cree una nueva instancia de [Capture Graph Builder](capture-graph-builder.md) e inicialíctela con un puntero al Administrador de Graph filtros:

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    A continuación, recupere el pin de salida de cada grupo mediante una llamada [**al método IRenderEngine::GetGroupOutputPin.**](irenderengine-getgroupoutputpin.md) Llame **a RenderStream** para conectar el pin a ASF Writer:

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

[Uso de Windows multimedia con DirectShow Editing Services](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



