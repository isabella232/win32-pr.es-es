---
description: Filtro de analizador SAMI (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Filtro de analizador SAMI (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0449bccd41a09fca952b5d84552ef919055526
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537683"
---
# <a name="sami-cc-parser-filter"></a>Filtro de analizador SAMI (CC)

Analiza los datos de subtítulos de los archivos de intercambio de medios accesibles (SAMI) sincronizados.

SAMI es un formato de texto similar a HTML y se usa para codificar títulos basados en tiempo. Este filtro convierte los datos SAMI en una secuencia de texto. Cada ejemplo de la secuencia contiene una entrada de título, junto con información de formato. Las marcas de tiempo de los ejemplos se generan a partir de la información de hora en el archivo SAMI.

Este filtro está diseñado para usarse con el filtro de [representador del comando de script interno](internal-script-command-renderer-filter.md) . El representador del comando de script interno recibe los ejemplos de texto y los envía a la aplicación, en forma de notificaciones de eventos. Para obtener más información, vea la sección Comentarios.



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Tipos de medios de anclaje de entrada                    | \_Secuencia MEDIATYPE                                                                                        |
| Interfaces de PIN de entrada                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Tipos de medios de anclaje de salida                   | \_Texto MEDIATYPE, MEDIASUBTYPE \_ null                                                                      |
| Interfaces de clavija de salida                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Identificador CLSID                             | {33FACFE0-A9BE-11D0-A520-00A0D10129C0}                                                                   |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                         |
| Executable                               | quartz.dll                                                                                               |
| [Fundament](merit.md)                       | MÉRITO \_ improbable                                                                                          |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>Observaciones

A continuación se facilita un archivo SAMI simple:


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



La etiqueta de **estilo** define dos configuraciones de idioma: Inglés (. ENCC) y francés (. FRCC). También define dos estilos, \# normal y \# GREENTEXT. Cada etiqueta **Sync** define la hora de inicio de un título, en milisegundos. Las etiquetas **P** contienen el texto del título, mientras que el atributo de **clase** especifica la configuración de idioma a la que se aplica el título.

Para cada lenguaje y estilo, el filtro crea una secuencia lógica. En cualquier momento, se habilitan exactamente una secuencia de idioma y una secuencia de estilo. Cuando el filtro genera un ejemplo, selecciona el título para el idioma actual y aplica el estilo actual. De forma predeterminada, se habilita el primer idioma y estilo declarados en el archivo. Una aplicación puede usar el método [**IAMStreamSelect:: enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) para habilitar una secuencia diferente.

Con la configuración predeterminada, el primer título del archivo de ejemplo genera el siguiente resultado:


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



Si la salida va al representador del comando de script interno, ese filtro envía una notificación de evento de evento [**\_ \_ OLE de EC**](ec-ole-event.md) . El segundo parámetro de evento es un BSTR con el texto de título. La aplicación puede recuperar el evento y mostrar el título.

En el ejemplo siguiente se muestra cómo representar un archivo SAMI, recuperar la información de la secuencia, habilitar secuencias y mostrar el texto de la leyenda. En el ejemplo se da por supuesto que el archivo SAMI anterior se guarda como C: \\ Sami \_ Test \_ file. Sami.

Por motivos de brevedad, en este ejemplo se usan índices de secuencias codificados de forma rígida al llamar al método **IAMStreamSelect:: enable** . También realiza una comprobación de errores mínima.


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



Este filtro usa la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) para extraer ejemplos del filtro de origen. Por lo tanto, no admite la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) en su PIN de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



