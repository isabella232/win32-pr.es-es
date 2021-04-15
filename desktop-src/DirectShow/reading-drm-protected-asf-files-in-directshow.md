---
description: En este tema se describe cómo usar DirectShow para reproducir archivos multimedia que están protegidos con Rights Management digitales (DRM) de Windows Media.
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Leer DRM-Protected archivos ASF en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a90b61982d6c7c444ddcf53948c225b6fc685
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689686"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a>Leer DRM-Protected archivos ASF en DirectShow

En este tema se describe cómo usar DirectShow para reproducir archivos multimedia que están protegidos con Rights Management digitales (DRM) de Windows Media.

## <a name="drm-concepts"></a>Conceptos de DRM

La protección de un archivo multimedia con DRM de Windows Media implica dos pasos distintos:

-   El proveedor de contenido empaqueta el archivo, es decir, cifra el archivo y adjunta la información de licencia al encabezado del archivo ASF. La información de licencia incluye una dirección URL en la que el cliente puede obtener la licencia.
-   La aplicación cliente adquiere una licencia para el contenido.

El empaquetado se produce antes de distribuir el archivo. La adquisición de licencias se produce cuando el usuario intenta reproducir o copiar el archivo. La adquisición de licencias puede ser *silenciosa* o *no silenciosa*. La adquisición silenciosa no requiere ninguna interacción con el usuario. La adquisición no silenciosa requiere que la aplicación abra una ventana del explorador y muestre una página web al usuario. En ese momento, es posible que el usuario tenga que proporcionar algún tipo de información al proveedor de contenido. Sin embargo, ambos tipos de adquisición de licencias requieren que el cliente envíe una solicitud HTTP a un servidor de licencias.

### <a name="drm-versions"></a>Versiones de DRM

Existen varias versiones de DRM de Windows Media. Desde la perspectiva de una aplicación cliente, se pueden agrupar en dos categorías: DRM versión 1 y DRM versión 7 o posterior. (La segunda categoría incluye las versiones de DRM 9 y 10, así como la versión 7). La razón para clasificar las versiones DRM de este modo es que las licencias de la versión 1 se controlan de forma ligeramente diferente que las licencias de la versión 7 o posterior. En esta documentación, la licencia del término *versión 7* significa la versión 7 o posterior.

También es importante distinguir el empaquetado de DRM de la licencia de DRM. Si el archivo está empaquetado con Windows Media Rights Manager versión 7 o posterior, el encabezado DRM puede contener una dirección URL de licencia de la versión 1, además de la dirección URL de la licencia de la versión 7. La dirección URL de la licencia de la versión 1 permite a reproductores antiguos que no admiten la versión 7 para obtener una licencia para el contenido. Sin embargo, el contrario no es cierto, por lo que un archivo con empaquetado de la versión 1 no puede tener una dirección URL de la licencia de la versión 7.

### <a name="application-security-level"></a>Nivel de seguridad de la aplicación

Para reproducir archivos protegidos con DRM, la aplicación cliente debe estar vinculada a una biblioteca estática que Microsoft proporcione en formato binario. Esta biblioteca, que identifica de forma única la aplicación, a veces se denomina biblioteca de código auxiliar. La biblioteca de código auxiliar tiene un nivel de seguridad asignado, cuyo valor viene determinado por el contrato de licencia que firmó al obtener la biblioteca de código auxiliar.

El proveedor de contenido establece un nivel de seguridad mínimo necesario para adquirir la licencia. Si el nivel de seguridad de la biblioteca de código auxiliar es menor que el nivel de seguridad mínimo que requiere el servidor de licencias, la aplicación no puede obtener la licencia.

### <a name="individualization"></a>Individualización

Para aumentar la seguridad, una aplicación puede actualizar los componentes de DRM en el equipo del cliente. Esta actualización, denominada individualización, diferencia la copia del usuario de la aplicación de todas las demás copias de la misma aplicación. El encabezado DRM de un archivo protegido puede especificar un nivel de individualización mínimo. (Para obtener más información, consulte la documentación de WMRMHeader. IndividualizedVersion en el SDK de Windows Media Rights Manager).

Dado que el servicio de individualización de Microsoft controla la información del usuario, debe mostrar la Directiva de privacidad de Microsoft o proporcionar un vínculo a esa página en el sitio web de Microsoft antes de que la aplicación individualizes: <https://go.microsoft.com/fwlink/p/?linkid=10240> .

## <a name="provide-the-software-certificate"></a>Proporcionar el certificado de software

Para permitir que la aplicación use la licencia DRM, la aplicación debe proporcionar un certificado de software o una *clave* para el administrador de gráficos de filtro. Esta clave está contenida en una biblioteca estática que es individualizada para la aplicación. Para obtener información sobre cómo obtener la biblioteca individualizada, consulte [obtención de la biblioteca DRM necesaria](../wmformat/obtaining-the-required-drm-library.md) en la documentación del SDK de Windows Media Format.

Para proporcionar la clave de software, realice los pasos siguientes:

1.  Vínculo a la biblioteca estática.
2.  Implemente la interfaz **IServiceProvider** .
3.  Consulte el administrador de gráficos de filtro para la interfaz [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) .
4.  Llame a [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) con un puntero a la implementación de **IServiceProvider**.
5.  Filter Graph Manager llamará a **IServiceProvider:: QueryService** y especificará el **IID \_ IWMReader** para el identificador de servicio.
6.  En la implementación de **QueryService**, llame a [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) para crear la clave de software.

En el código siguiente se muestra cómo implementar el método **QueryService** :


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



En el código siguiente se muestra cómo llamar a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) en Filter Graph Manager:


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





## <a name="building-the-playback-graph"></a>Compilar el gráfico de reproducción

Para reproducir un archivo ASF protegido con DRM, realice los pasos siguientes:

1.  Cree el [Administrador de gráficos de filtro](filter-graph-manager.md) y use la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para registrar eventos de grafos.
2.  Llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una nueva instancia del filtro de [lector ASF de WM](wm-asf-reader-filter.md) .
3.  Llame a [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el filtro al gráfico de filtro.
4.  Consulte el filtro para la interfaz [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .
5.  Llame a [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) con la dirección URL del archivo.
6.  Controlar eventos de [**\_ \_ evento WMT de EC**](ec-wmt-event.md) .
7.  En el primer evento de [**\_ \_ evento WMT EC**](ec-wmt-event.md) , consulte el filtro de [lector ASF de WM](wm-asf-reader-filter.md) para la interfaz **IServiceProvider** .
8.  Llame a **IServiceProvider:: QueryService** para obtener un puntero a la interfaz [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .
9.  Llame a [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para representar los pines de salida del filtro del [lector ASF de WM](wm-asf-reader-filter.md) .

> [!Note]  
> Al abrir un archivo protegido con DRM, no llame a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) para crear el gráfico de filtro. El filtro lector ASF de WM no puede conectarse a ningún otro filtro hasta que se adquiera la licencia DRM. Este paso requiere que la aplicación use la interfaz [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) , que se debe obtener del filtro, tal y como se describe en los pasos 7 a 8. Por lo tanto, debe crear el filtro y agregarlo al gráfico.

 

> [!Note]  
> Es importante registrarse para los eventos de gráfico (paso 1) antes de agregar el filtro de [lector ASF de WM](wm-asf-reader-filter.md) al gráfico (paso 3), ya que la aplicación debe controlar los eventos de [**\_ \_ evento WMT de EC**](ec-wmt-event.md) . Los eventos se envían cuando se llama a [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) (paso 5).

 

En el código siguiente se muestra cómo compilar el gráfico:


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

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            if (FAILED(hr))
            {
                goto done;
            }
            hr = RenderOutputPins(pGraph, m_pReader);
    }
    else
    {
        // Not a Windows Media file, so just render the standard way.
        hr = pGraph->RenderFile(pwszFile, NULL);
    }

done:
    return hr;
}</code></pre></td>
</tr>
</tbody>
</table>



En el código anterior, la `RenderOutputPins` función enumera los terminales de salida en el filtro de [lector ASF de WM](wm-asf-reader-filter.md) y llama a [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para cada pin.


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



En el código siguiente se muestra cómo obtener un puntero a la interfaz [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) desde el [lector ASF de WM](wm-asf-reader-filter.md):


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

 

 
