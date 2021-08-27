---
description: En este tema se describe cómo usar DirectShow para reproducir archivos multimedia que están protegidos con Windows Media Digital Rights Management (DRM).
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Leer DRM-Protected asf en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46eaafe96b00019e7c4e69741c251bc0079c459d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466582"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a>Leer DRM-Protected asf en DirectShow

En este tema se describe cómo usar DirectShow para reproducir archivos multimedia que están protegidos con Windows Media Digital Rights Management (DRM).

## <a name="drm-concepts"></a>Conceptos de DRM

La protección de un archivo multimedia Windows DRM multimedia implica dos pasos distintos:

-   El proveedor de contenido empaqueta el archivo, es decir, cifra el archivo y adjunta la información de licencia al encabezado del archivo ASF. La información de licencia incluye una dirección URL donde el cliente puede obtener la licencia.
-   La aplicación cliente adquiere una licencia para el contenido.

El empaquetado se produce antes de distribuir el archivo. La adquisición de licencias se produce cuando el usuario intenta reproducir o copiar el archivo. La adquisición de licencias *puede ser silenciosa* o no *silenciosa.* La adquisición silenciosa no requiere ninguna interacción con el usuario. La adquisición no silenciosa requiere que la aplicación abra una ventana del explorador y muestre una página web al usuario. En ese momento, es posible que el usuario tenga que proporcionar algún tipo de información al proveedor de contenido. Sin embargo, ambos tipos de adquisición de licencias requieren que el cliente envíe una solicitud HTTP a un servidor de licencias.

### <a name="drm-versions"></a>Versiones de DRM

Existen varias versiones Windows DRM multimedia. Desde la perspectiva de una aplicación cliente, se pueden agrupar en dos categorías: DRM versión 1 y DRM versión 7 o posterior. (La segunda categoría incluye las versiones 9 y 10 de DRM, así como la versión 7). La razón para categorizar las versiones de DRM de esta manera es que las licencias de la versión 1 se administran de forma ligeramente diferente a las licencias de la versión 7 o posteriores. En esta documentación, el término licencia *de la versión 7* significa la versión 7 o posterior.

También es importante distinguir el empaquetado drm de la licencia DRM. Si el archivo se empaqueta mediante Windows Media Rights Manager versión 7 o posterior, el encabezado DRM puede contener una dirección URL de licencia de la versión 1 además de la dirección URL de licencia de la versión 7. La dirección URL de licencia de la versión 1 permite a los reproductores más antiguos que no admiten la versión 7 obtener una licencia para el contenido. Sin embargo, lo contrario no es cierto, por lo que un archivo con empaquetado de la versión 1 no puede tener una dirección URL de licencia de la versión 7.

### <a name="application-security-level"></a>Nivel de seguridad de la aplicación

Para reproducir archivos protegidos con DRM, la aplicación cliente debe estar vinculada a una biblioteca estática proporcionada en formato binario por Microsoft. Esta biblioteca, que identifica de forma única la aplicación, a veces se denomina biblioteca de código auxiliar. La biblioteca de código auxiliar tiene un nivel de seguridad asignado, cuyo valor viene determinado por el contrato de licencia que firmó al obtener la biblioteca de código auxiliar.

El proveedor de contenido establece un nivel de seguridad mínimo necesario para adquirir la licencia. Si el nivel de seguridad de la biblioteca de código auxiliar es menor que el nivel de seguridad mínimo requerido por el servidor de licencias, la aplicación no puede obtener la licencia.

### <a name="individualization"></a>Individualización

Para aumentar la seguridad, una aplicación puede actualizar los componentes de DRM en el equipo del cliente. Esta actualización, denominada individualización, diferencia la copia del usuario de la aplicación de todas las demás copias de la misma aplicación. El encabezado DRM de un archivo protegido puede especificar un nivel de individualización mínimo. (Para obtener más información, vea la documentación de WMRMHeader.IndividualizedVersion en Windows SDK de Media Rights Manager).

Dado que el servicio de individualización de Microsoft controla la información del usuario, debe mostrar la directiva de privacidad de Microsoft o proporcionar un vínculo a esa página en el sitio web de Microsoft antes de que la aplicación individualice: <https://go.microsoft.com/fwlink/p/?linkid=10240> .

## <a name="provide-the-software-certificate"></a>Proporcionar el certificado de software

Para permitir que la aplicación use la licencia DRM,  la aplicación debe proporcionar un certificado de software o una clave al Administrador de Graph filtros. Esta clave está contenida en una biblioteca estática que se individualiza para la aplicación. Para obtener información sobre cómo obtener la biblioteca individualizada, consulte [Obtención](../wmformat/obtaining-the-required-drm-library.md) de la biblioteca DRM necesaria en la documentación Windows SDK de formato multimedia.

Para proporcionar la clave de software, realice los pasos siguientes:

1.  Vínculo a la biblioteca estática.
2.  Implemente **la interfaz IServiceProvider.**
3.  Consulte el Administrador de Graph filtro para la [**interfaz IObjectWithSite.**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
4.  Llame [**a IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) con un puntero a la implementación de **IServiceProvider**.
5.  El Administrador Graph filtro llamará **a IServiceProvider::QueryService** y especificará **\_ IID IWMReader** como identificador de servicio.
6.  En la implementación de **QueryService**, llame a [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) para crear la clave de software.

El código siguiente muestra cómo implementar el **método QueryService:**


```C++
STDMETHODIMP Player::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (ppv == NULL ) 
    { 
        return E_POINTER; 
    }

    if (siid == __uuidof(IWMReader) && riid == __uuidof(IUnknown))
    {
        IUnknown *punkCert;

        HRESULT hr = WMCreateCertificate(&punkCert);

        if (SUCCEEDED(hr))
        {
            *ppv = (void *) punkCert;
        }

        return hr;
    }
    return E_NOINTERFACE;
}
```



En el código siguiente se muestra cómo llamar [**a SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) en filter Graph Manager:


```C++
HRESULT Player::CreateFilterGraph()
{
    CComPtr<IObjectWithSite> pSite;

    HRESULT hr = pGraph.CoCreateInstance(CLSID_FilterGraph);

    if (FAILED(hr))
    {
        goto done;
    }

    // Register the application as a site (service).
    hr = pGraph->QueryInterface(&pSite);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSite->SetSite(this);


done:
    return hr;
}
```





## <a name="building-the-playback-graph"></a>Creación de la ventana de reproducción Graph

Para reproducir un archivo ASF protegido con DRM, realice los pasos siguientes:

1.  Cree el [Administrador Graph filtro](filter-graph-manager.md) y use la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para registrarse para eventos de grafo.
2.  Llame [**a CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una nueva instancia del filtro [WM ASF Reader.](wm-asf-reader-filter.md)
3.  Llame [**a IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el filtro al gráfico de filtros.
4.  Consulte el filtro para la [**interfaz IFileSourceFilter.**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)
5.  Llame [**a IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) con la dirección URL del archivo.
6.  Controlar [**eventos \_ EC WMT \_ EVENT.**](ec-wmt-event.md)
7.  En el primer [**evento EC \_ WMT \_ EVENT,**](ec-wmt-event.md) consulte el filtro [WM ASF Reader](wm-asf-reader-filter.md) para la interfaz **IServiceProvider.**
8.  Llame **a IServiceProvider::QueryService** para obtener un puntero a la [**interfaz IWMDRMReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
9.  Llame [**a IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para representar los pines de salida del filtro [wm ASF Reader.](wm-asf-reader-filter.md)

> [!Note]  
> Al abrir un archivo protegido con DRM, no llame a [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) para crear el gráfico de filtros. El filtro WM ASF Reader no se puede conectar a ningún otro filtro hasta que se adquiera la licencia DRM. Este paso requiere que la aplicación use la interfaz [**IWMDRMReader,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) que se debe obtener del filtro, como se describe en los pasos 7 a 8. Por lo tanto, debe crear el filtro y agregarlo al gráfico.

 

> [!Note]  
> Es importante registrarse para eventos de grafo (paso 1) antes de agregar el filtro [lector de ASF wm](wm-asf-reader-filter.md) al gráfico (paso 3), ya que la aplicación debe controlar los eventos EC [**\_ WMT \_ EVENT.**](ec-wmt-event.md) Los eventos se envían cuando [**se llama a Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) (paso 5).

 

El código siguiente muestra cómo compilar el gráfico:


```C++
HRESULT Player::LoadMediaFile(PCWSTR pwszFile)
{


    BOOL bIsWindowsMediaFile = IsWindowsMediaFile(pwszFile);

    HRESULT hr = S_OK;

    // If this is the first time opening the file, create the
    // filter graph and add the WM ASF Reader filter.

    if (m_DRM.State() == DRM_INITIAL)
    {
        hr = CreateFilterGraph();
        if (FAILED(hr))
        {
            goto done;
        }

        // Use special handling for Windows Media files.
        if (bIsWindowsMediaFile)
        {
            // Add the ASF Reader filter to the graph.
            hr = m_pReader.CoCreateInstance(CLSID_WMAsfReader);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pGraph->AddFilter(m_pReader, NULL);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = m_pReader->QueryInterface(&m_pFileSource);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    }

    if (bIsWindowsMediaFile)
    {
            hr = m_pFileSource->Load(pwszFile, NULL);
```

<span codelanguage="ManagedCPlusPlus"></span>


| C++ | 
|-----|
| <pre><code>            if (FAILED(hr))            {                goto done;            }            hr = RenderOutputPins(pGraph, m_pReader);    }    else    {        // Not a Windows Media file, so just render the standard way.        hr = pGraph-&gt;RenderFile(pwszFile, NULL);    }done:    return hr;}</code></pre> | 




En el código anterior, la función enumera los pines de salida en el filtro WM ASF Reader y llama a `RenderOutputPins` [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para cada pin. [](wm-asf-reader-filter.md)


```C++
HRESULT RenderOutputPins(IGraphBuilder *pGraph, IBaseFilter *pFilter)
{
    CComPtr<IEnumPins>  pEnumPin = NULL;
    CComPtr<IPin>       pConnectedPin;
    CComPtr<IPin>       pPin;

    // Enumerate all pins on the filter
    HRESULT hr = pFilter->EnumPins(&pEnumPin);
    if (FAILED(hr))
    {
        goto done;
    }

    // Step through every pin, looking for the output pins.
    while (S_OK == (hr = pEnumPin->Next(1, &pPin, NULL)))
    {
        // Skip connected pins.
        hr = pPin->ConnectedTo(&pConnectedPin);
        if (hr == VFW_E_NOT_CONNECTED)
        {
            PIN_DIRECTION PinDirection;
            hr = pPin->QueryDirection(&PinDirection);

            if ((S_OK == hr) && (PinDirection == PINDIR_OUTPUT))
            {
                hr = pGraph->Render(pPin);
            }
        }

        pConnectedPin.Release();
        pPin.Release();

        // If there was an error, stop enumerating.
        if (FAILED(hr))
        {
            break;
        }
    }

done:
    return hr;
}
```



En el código siguiente se muestra cómo obtener un puntero a la [**interfaz IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) desde el [lector de ASF de WM](wm-asf-reader-filter.md):


```C++
HRESULT DrmManager::Initialize(IBaseFilter *pFilter)
{


    CComPtr<IServiceProvider> pService;
    CComPtr<IWMDRMReader> pDrmReader;

    HRESULT hr = pFilter->QueryInterface(&pService);
    if (SUCCEEDED(hr))
    {
        hr = pService->QueryService(
            __uuidof(IWMDRMReader), IID_PPV_ARGS(&m_pDrmReader));
    }
    return hr;
}
```





## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
