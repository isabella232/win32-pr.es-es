---
description: Filtro de analizador SAMI (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Filtro de analizador SAMI (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77f0aa2d913b7f0295a078c8174ae483bb1cb62
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909683"
---
# <a name="sami-cc-parser-filter"></a>Filtro de analizador SAMI (CC)

Analiza los datos de subtítulos de archivos de intercambio multimedia accesible sincronizado (SAMI).

SAMI es un formato de texto similar a HTML y se usa para codificar títulos basados en tiempo. Este filtro convierte los datos SAMI en una secuencia de texto. Cada ejemplo de la secuencia contiene una entrada de título, junto con información de formato. Las marcas de tiempo de los ejemplos se generan a partir de la información de hora del archivo SAMI.

Este filtro está diseñado para usarse con el filtro [Representador](internal-script-command-renderer-filter.md) de comandos de script interno. El representador de comandos de script interno recibe los ejemplos de texto y los envía a la aplicación, en forma de notificaciones de eventos. Para obtener más información, vea la sección Comentarios.



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Tipos de medios de pin de entrada                    | Secuencia \_ MEDIATYPE                                                                                        |
| Interfaces de pin de entrada                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Tipos de medios de pin de salida                   | TEXTO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                      |
| Interfaces de pin de salida                    | [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | {33FACFE0-A9BE-11D0-A520-00A0D10129C0}                                                                   |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                         |
| Executable                               | quartz.dll                                                                                               |
| [Mérito](merit.md)                       | NO ES \_ PROBABLE QUE SE PRODUZCAN                                                                                          |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>Comentarios

A continuación se muestra un archivo SAMI simple:


```C++
<SAMI>
<Head>
<STYLE TYPE="text/css"> <!--
    .ENCC {Name: English; lang:en-US; SAMI_TYPE: CC;}
    .FRCC {Name: French; lang:fr-FR; SAMI_TYPE: CC;}
    #NORMAL {Name: Normal; font-family: arial;}
    #GREENTEXT {Name: GreenText; color:green; font-family: verdana;}
-->
</STYLE>
</Head>
<BODY>
<Sync Start=1000>
    <P CLASS="ENCC">One
    <P CLASS="FRCC">Un

<Sync Start=2000>
    <P CLASS="ENCC">Two
    <P CLASS="FRCC">Deux

<Sync Start=3000>
    <P CLASS="ENCC">Three
    <P CLASS="FRCC">Trois
</BODY>
</SAMI>
```



La **etiqueta STYLE** define dos configuraciones de idioma, inglés (. ENCC) y francés (. FRCC). También define dos estilos, \# NORMAL y \# GREENTEXT. Cada **etiqueta SYNC** define la hora de inicio de un título, en milisegundos. Las **etiquetas P** contienen el texto del título, mientras que el atributo **CLASS** especifica la configuración de idioma a la que se aplica el título.

Para cada idioma y estilo, el filtro crea una secuencia lógica. En cualquier momento, se habilitan exactamente una secuencia de idioma y una secuencia de estilo. Cuando el filtro genera un ejemplo, selecciona el título del idioma actual y aplica el estilo actual. De forma predeterminada, el primer idioma y estilo declarados en el archivo están habilitados. Una aplicación puede usar el [**método IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) para habilitar una secuencia diferente.

Con la configuración predeterminada, el primer título del archivo de ejemplo genera la siguiente salida:


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



Si la salida va al representador de comandos de script interno, ese filtro envía una notificación [**de eventos OLE EVENT \_ \_ de EC.**](ec-ole-event.md) El segundo parámetro de evento es un BSTR con el texto del título. La aplicación puede recuperar el evento y mostrar el título.

En el ejemplo siguiente se muestra cómo representar un archivo SAMI, recuperar información de secuencias, habilitar secuencias y mostrar texto de título. En el ejemplo se supone que el archivo SAMI anterior se guarda como C: \\ Sami \_ test \_ file.sami.

Por brevedad, en este ejemplo se usaron índices de flujo codificados de forma fuerte cuando llama al **método IAMStreamSelect::Enable.** También realiza una comprobación de errores mínima.


```C++
void __cdecl main()
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    IMediaControl *pMediaControl;
    IMediaEventEx *pEv;
    IBaseFilter   *pSAMI;

    CoInitialize(NULL);
    
    // Create the filter graph manager.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC, 
                        IID_IGraphBuilder, (void **)&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pMediaControl);
    pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEv);

    // Create the graph and find the SAMI parser.
    pGraph->RenderFile(L"C:\\Sami_test_file.sami", NULL);
    hr = pGraph->FindFilterByName(L"SAMI (CC) Parser", &pSAMI);
    if (SUCCEEDED(hr)) 
    {
        IAMStreamSelect *pStrm = NULL;
        hr = pSAMI->QueryInterface(IID_IAMStreamSelect, (void**)&pStrm);
        if (SUCCEEDED(hr)) 
        {
            DWORD dwStreams = 0;
            pStrm->Count(&dwStreams);
            printf("Stream count: %d\n", dwStreams);

            // Select French and "GreenText"
            hr = pStrm->Enable(1, AMSTREAMSELECTENABLE_ENABLE);
            hr = pStrm->Enable(3, AMSTREAMSELECTENABLE_ENABLE);

            // Print the name of each logical stream.
            for (DWORD index = 0; index < dwStreams; index++)
            {
                DWORD dwFlags;
                WCHAR *wszName;
                hr = pStrm->Info(index, NULL, &dwFlags, NULL, NULL,
                    &wszName, NULL, NULL);
                if (hr == S_OK)
                {
                    wprintf(L"Stream %d: %s [%s]\n", index, wszName, 
                        (dwFlags ?  L"ENABLED" : L"DISABLED"));
                    CoTaskMemFree(wszName);
                }
            }
            pStrm->Release();
        }
        pSAMI->Release();
    }

    // Run the graph and display the captions.
    pMediaControl->Run();
    while (1)
    {
        long evCode, lParam1, lParam2;
        pEv->GetEvent(&evCode, &lParam1, &lParam2, 100);
        
        if (evCode == EC_OLE_EVENT) {
            wprintf(L"%s\n", (BSTR)lParam2);
        }
        pEv->FreeEventParams(evCode, lParam1, lParam2);

        if (evCode == EC_USERABORT || evCode == EC_COMPLETE || evCode == EC_ERRORABORT)
            break;
    }

    // Clean up.
    pMediaControl->Release();
    pEv->Release();
    pGraph->Release();
    CoUninitialize();
}
```



Este filtro usa la [**interfaz IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) para extraer ejemplos del filtro de origen. Por lo tanto, no admite la [**interfaz IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) en su pin de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



