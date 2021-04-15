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
# <a name="sami-cc-parser-filter"></a><span data-ttu-id="c493b-103">Filtro de analizador SAMI (CC)</span><span class="sxs-lookup"><span data-stu-id="c493b-103">SAMI (CC) Parser Filter</span></span>

<span data-ttu-id="c493b-104">Analiza los datos de subtítulos de los archivos de intercambio de medios accesibles (SAMI) sincronizados.</span><span class="sxs-lookup"><span data-stu-id="c493b-104">Parses captioning data from Synchronized Accessible Media Interchange (SAMI) files.</span></span>

<span data-ttu-id="c493b-105">SAMI es un formato de texto similar a HTML y se usa para codificar títulos basados en tiempo.</span><span class="sxs-lookup"><span data-stu-id="c493b-105">SAMI is a text format similar to HTML, and is used for encoding time-based captions.</span></span> <span data-ttu-id="c493b-106">Este filtro convierte los datos SAMI en una secuencia de texto.</span><span class="sxs-lookup"><span data-stu-id="c493b-106">This filter converts SAMI data into a text stream.</span></span> <span data-ttu-id="c493b-107">Cada ejemplo de la secuencia contiene una entrada de título, junto con información de formato.</span><span class="sxs-lookup"><span data-stu-id="c493b-107">Each sample in the stream contains one caption entry, along with format information.</span></span> <span data-ttu-id="c493b-108">Las marcas de tiempo de los ejemplos se generan a partir de la información de hora en el archivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="c493b-108">The time stamps on the samples are generated from the time information in the SAMI file.</span></span>

<span data-ttu-id="c493b-109">Este filtro está diseñado para usarse con el filtro de [representador del comando de script interno](internal-script-command-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="c493b-109">This filter is designed to be used with the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="c493b-110">El representador del comando de script interno recibe los ejemplos de texto y los envía a la aplicación, en forma de notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="c493b-110">The Internal Script Command Renderer receives the text samples and sends them to the application, in the form of event notifications.</span></span> <span data-ttu-id="c493b-111">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="c493b-111">For more information, see the Remarks section.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c493b-112">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="c493b-112">Filter Interfaces</span></span>                        | <span data-ttu-id="c493b-113">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="c493b-113">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="c493b-114">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="c493b-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="c493b-115">\_Secuencia MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="c493b-115">MEDIATYPE\_Stream</span></span>                                                                                        |
| <span data-ttu-id="c493b-116">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="c493b-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="c493b-117">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c493b-117">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="c493b-118">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="c493b-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="c493b-119">\_Texto MEDIATYPE, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="c493b-119">MEDIATYPE\_Text, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="c493b-120">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="c493b-120">Output Pin Interfaces</span></span>                    | <span data-ttu-id="c493b-121">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c493b-121">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="c493b-122">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="c493b-122">Filter CLSID</span></span>                             | <span data-ttu-id="c493b-123">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span><span class="sxs-lookup"><span data-stu-id="c493b-123">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span></span>                                                                   |
| <span data-ttu-id="c493b-124">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="c493b-124">Property Page CLSID</span></span>                      | <span data-ttu-id="c493b-125">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="c493b-125">No property page</span></span>                                                                                         |
| <span data-ttu-id="c493b-126">Executable</span><span class="sxs-lookup"><span data-stu-id="c493b-126">Executable</span></span>                               | <span data-ttu-id="c493b-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="c493b-127">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="c493b-128">Fundament</span><span class="sxs-lookup"><span data-stu-id="c493b-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="c493b-129">MÉRITO \_ improbable</span><span class="sxs-lookup"><span data-stu-id="c493b-129">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="c493b-130">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="c493b-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="c493b-131">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c493b-131">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="c493b-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c493b-132">Remarks</span></span>

<span data-ttu-id="c493b-133">A continuación se facilita un archivo SAMI simple:</span><span class="sxs-lookup"><span data-stu-id="c493b-133">The following is a simple SAMI file:</span></span>


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



<span data-ttu-id="c493b-134">La etiqueta de **estilo** define dos configuraciones de idioma: Inglés (. ENCC) y francés (. FRCC).</span><span class="sxs-lookup"><span data-stu-id="c493b-134">The **STYLE** tag defines two language settings, English (.ENCC) and French (.FRCC).</span></span> <span data-ttu-id="c493b-135">También define dos estilos, \# normal y \# GREENTEXT.</span><span class="sxs-lookup"><span data-stu-id="c493b-135">It also defines two styles, \#NORMAL and \#GREENTEXT.</span></span> <span data-ttu-id="c493b-136">Cada etiqueta **Sync** define la hora de inicio de un título, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="c493b-136">Each **SYNC** tag defines the start time for a caption, in milliseconds.</span></span> <span data-ttu-id="c493b-137">Las etiquetas **P** contienen el texto del título, mientras que el atributo de **clase** especifica la configuración de idioma a la que se aplica el título.</span><span class="sxs-lookup"><span data-stu-id="c493b-137">The **P** tags contain the caption text, while the **CLASS** attribute specifies the language setting to which the caption applies.</span></span>

<span data-ttu-id="c493b-138">Para cada lenguaje y estilo, el filtro crea una secuencia lógica.</span><span class="sxs-lookup"><span data-stu-id="c493b-138">For each language and style, the filter creates a logical stream.</span></span> <span data-ttu-id="c493b-139">En cualquier momento, se habilitan exactamente una secuencia de idioma y una secuencia de estilo.</span><span class="sxs-lookup"><span data-stu-id="c493b-139">At any time, exactly one language stream and one style stream are enabled.</span></span> <span data-ttu-id="c493b-140">Cuando el filtro genera un ejemplo, selecciona el título para el idioma actual y aplica el estilo actual.</span><span class="sxs-lookup"><span data-stu-id="c493b-140">When the filter generates a sample, it selects the caption for the current language and applies the current style.</span></span> <span data-ttu-id="c493b-141">De forma predeterminada, se habilita el primer idioma y estilo declarados en el archivo.</span><span class="sxs-lookup"><span data-stu-id="c493b-141">By default, the first language and style declared in the file are enabled.</span></span> <span data-ttu-id="c493b-142">Una aplicación puede usar el método [**IAMStreamSelect:: enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) para habilitar una secuencia diferente.</span><span class="sxs-lookup"><span data-stu-id="c493b-142">An application can use the [**IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) method to enable a different stream.</span></span>

<span data-ttu-id="c493b-143">Con la configuración predeterminada, el primer título del archivo de ejemplo genera el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="c493b-143">With the default settings, the first caption in the example file produces the following output:</span></span>


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



<span data-ttu-id="c493b-144">Si la salida va al representador del comando de script interno, ese filtro envía una notificación de evento de evento [**\_ \_ OLE de EC**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="c493b-144">If the output goes to the Internal Script Command Renderer, that filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="c493b-145">El segundo parámetro de evento es un BSTR con el texto de título.</span><span class="sxs-lookup"><span data-stu-id="c493b-145">The second event parameter is a BSTR with the caption text.</span></span> <span data-ttu-id="c493b-146">La aplicación puede recuperar el evento y mostrar el título.</span><span class="sxs-lookup"><span data-stu-id="c493b-146">The application can retrieve the event and display the caption.</span></span>

<span data-ttu-id="c493b-147">En el ejemplo siguiente se muestra cómo representar un archivo SAMI, recuperar la información de la secuencia, habilitar secuencias y mostrar el texto de la leyenda.</span><span class="sxs-lookup"><span data-stu-id="c493b-147">The following example shows how to render a SAMI file, retrieve stream information, enable streams, and display caption text.</span></span> <span data-ttu-id="c493b-148">En el ejemplo se da por supuesto que el archivo SAMI anterior se guarda como C: \\ Sami \_ Test \_ file. Sami.</span><span class="sxs-lookup"><span data-stu-id="c493b-148">The example assumes that the previous SAMI file is saved as C:\\Sami\_test\_file.sami.</span></span>

<span data-ttu-id="c493b-149">Por motivos de brevedad, en este ejemplo se usan índices de secuencias codificados de forma rígida al llamar al método **IAMStreamSelect:: enable** .</span><span class="sxs-lookup"><span data-stu-id="c493b-149">For brevity, this example used hard-coded stream indexes when it calls the **IAMStreamSelect::Enable** method.</span></span> <span data-ttu-id="c493b-150">También realiza una comprobación de errores mínima.</span><span class="sxs-lookup"><span data-stu-id="c493b-150">It also performs minimal error checking.</span></span>


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



<span data-ttu-id="c493b-151">Este filtro usa la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) para extraer ejemplos del filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="c493b-151">This filter uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface to pull samples from the source filter.</span></span> <span data-ttu-id="c493b-152">Por lo tanto, no admite la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) en su PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="c493b-152">Therefore, it does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on its input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c493b-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c493b-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c493b-154">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="c493b-154">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



