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
# <a name="sami-cc-parser-filter"></a><span data-ttu-id="94eac-103">Filtro de analizador SAMI (CC)</span><span class="sxs-lookup"><span data-stu-id="94eac-103">SAMI (CC) Parser Filter</span></span>

<span data-ttu-id="94eac-104">Analiza los datos de subtítulos de archivos de intercambio multimedia accesible sincronizado (SAMI).</span><span class="sxs-lookup"><span data-stu-id="94eac-104">Parses captioning data from Synchronized Accessible Media Interchange (SAMI) files.</span></span>

<span data-ttu-id="94eac-105">SAMI es un formato de texto similar a HTML y se usa para codificar títulos basados en tiempo.</span><span class="sxs-lookup"><span data-stu-id="94eac-105">SAMI is a text format similar to HTML, and is used for encoding time-based captions.</span></span> <span data-ttu-id="94eac-106">Este filtro convierte los datos SAMI en una secuencia de texto.</span><span class="sxs-lookup"><span data-stu-id="94eac-106">This filter converts SAMI data into a text stream.</span></span> <span data-ttu-id="94eac-107">Cada ejemplo de la secuencia contiene una entrada de título, junto con información de formato.</span><span class="sxs-lookup"><span data-stu-id="94eac-107">Each sample in the stream contains one caption entry, along with format information.</span></span> <span data-ttu-id="94eac-108">Las marcas de tiempo de los ejemplos se generan a partir de la información de hora del archivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="94eac-108">The time stamps on the samples are generated from the time information in the SAMI file.</span></span>

<span data-ttu-id="94eac-109">Este filtro está diseñado para usarse con el filtro [Representador](internal-script-command-renderer-filter.md) de comandos de script interno.</span><span class="sxs-lookup"><span data-stu-id="94eac-109">This filter is designed to be used with the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="94eac-110">El representador de comandos de script interno recibe los ejemplos de texto y los envía a la aplicación, en forma de notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="94eac-110">The Internal Script Command Renderer receives the text samples and sends them to the application, in the form of event notifications.</span></span> <span data-ttu-id="94eac-111">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="94eac-111">For more information, see the Remarks section.</span></span>



| <span data-ttu-id="94eac-112">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="94eac-112">Label</span></span> | <span data-ttu-id="94eac-113">Value</span><span class="sxs-lookup"><span data-stu-id="94eac-113">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94eac-114">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="94eac-114">Filter Interfaces</span></span>                        | <span data-ttu-id="94eac-115">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="94eac-115">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="94eac-116">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="94eac-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="94eac-117">Secuencia \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="94eac-117">MEDIATYPE\_Stream</span></span>                                                                                        |
| <span data-ttu-id="94eac-118">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="94eac-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="94eac-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="94eac-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="94eac-120">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="94eac-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="94eac-121">TEXTO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="94eac-121">MEDIATYPE\_Text, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="94eac-122">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="94eac-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="94eac-123">[**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="94eac-123">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="94eac-124">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="94eac-124">Filter CLSID</span></span>                             | <span data-ttu-id="94eac-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span><span class="sxs-lookup"><span data-stu-id="94eac-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span></span>                                                                   |
| <span data-ttu-id="94eac-126">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="94eac-126">Property Page CLSID</span></span>                      | <span data-ttu-id="94eac-127">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="94eac-127">No property page</span></span>                                                                                         |
| <span data-ttu-id="94eac-128">Executable</span><span class="sxs-lookup"><span data-stu-id="94eac-128">Executable</span></span>                               | <span data-ttu-id="94eac-129">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="94eac-129">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="94eac-130">Mérito</span><span class="sxs-lookup"><span data-stu-id="94eac-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="94eac-131">NO ES \_ PROBABLE QUE SE PRODUZCAN</span><span class="sxs-lookup"><span data-stu-id="94eac-131">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="94eac-132">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="94eac-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="94eac-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="94eac-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="94eac-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94eac-134">Remarks</span></span>

<span data-ttu-id="94eac-135">A continuación se muestra un archivo SAMI simple:</span><span class="sxs-lookup"><span data-stu-id="94eac-135">The following is a simple SAMI file:</span></span>


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



<span data-ttu-id="94eac-136">La **etiqueta STYLE** define dos configuraciones de idioma, inglés (. ENCC) y francés (. FRCC).</span><span class="sxs-lookup"><span data-stu-id="94eac-136">The **STYLE** tag defines two language settings, English (.ENCC) and French (.FRCC).</span></span> <span data-ttu-id="94eac-137">También define dos estilos, \# NORMAL y \# GREENTEXT.</span><span class="sxs-lookup"><span data-stu-id="94eac-137">It also defines two styles, \#NORMAL and \#GREENTEXT.</span></span> <span data-ttu-id="94eac-138">Cada **etiqueta SYNC** define la hora de inicio de un título, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="94eac-138">Each **SYNC** tag defines the start time for a caption, in milliseconds.</span></span> <span data-ttu-id="94eac-139">Las **etiquetas P** contienen el texto del título, mientras que el atributo **CLASS** especifica la configuración de idioma a la que se aplica el título.</span><span class="sxs-lookup"><span data-stu-id="94eac-139">The **P** tags contain the caption text, while the **CLASS** attribute specifies the language setting to which the caption applies.</span></span>

<span data-ttu-id="94eac-140">Para cada idioma y estilo, el filtro crea una secuencia lógica.</span><span class="sxs-lookup"><span data-stu-id="94eac-140">For each language and style, the filter creates a logical stream.</span></span> <span data-ttu-id="94eac-141">En cualquier momento, se habilitan exactamente una secuencia de idioma y una secuencia de estilo.</span><span class="sxs-lookup"><span data-stu-id="94eac-141">At any time, exactly one language stream and one style stream are enabled.</span></span> <span data-ttu-id="94eac-142">Cuando el filtro genera un ejemplo, selecciona el título del idioma actual y aplica el estilo actual.</span><span class="sxs-lookup"><span data-stu-id="94eac-142">When the filter generates a sample, it selects the caption for the current language and applies the current style.</span></span> <span data-ttu-id="94eac-143">De forma predeterminada, el primer idioma y estilo declarados en el archivo están habilitados.</span><span class="sxs-lookup"><span data-stu-id="94eac-143">By default, the first language and style declared in the file are enabled.</span></span> <span data-ttu-id="94eac-144">Una aplicación puede usar el [**método IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) para habilitar una secuencia diferente.</span><span class="sxs-lookup"><span data-stu-id="94eac-144">An application can use the [**IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) method to enable a different stream.</span></span>

<span data-ttu-id="94eac-145">Con la configuración predeterminada, el primer título del archivo de ejemplo genera la siguiente salida:</span><span class="sxs-lookup"><span data-stu-id="94eac-145">With the default settings, the first caption in the example file produces the following output:</span></span>


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



<span data-ttu-id="94eac-146">Si la salida va al representador de comandos de script interno, ese filtro envía una notificación [**de eventos OLE EVENT \_ \_ de EC.**](ec-ole-event.md)</span><span class="sxs-lookup"><span data-stu-id="94eac-146">If the output goes to the Internal Script Command Renderer, that filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="94eac-147">El segundo parámetro de evento es un BSTR con el texto del título.</span><span class="sxs-lookup"><span data-stu-id="94eac-147">The second event parameter is a BSTR with the caption text.</span></span> <span data-ttu-id="94eac-148">La aplicación puede recuperar el evento y mostrar el título.</span><span class="sxs-lookup"><span data-stu-id="94eac-148">The application can retrieve the event and display the caption.</span></span>

<span data-ttu-id="94eac-149">En el ejemplo siguiente se muestra cómo representar un archivo SAMI, recuperar información de secuencias, habilitar secuencias y mostrar texto de título.</span><span class="sxs-lookup"><span data-stu-id="94eac-149">The following example shows how to render a SAMI file, retrieve stream information, enable streams, and display caption text.</span></span> <span data-ttu-id="94eac-150">En el ejemplo se supone que el archivo SAMI anterior se guarda como C: \\ Sami \_ test \_ file.sami.</span><span class="sxs-lookup"><span data-stu-id="94eac-150">The example assumes that the previous SAMI file is saved as C:\\Sami\_test\_file.sami.</span></span>

<span data-ttu-id="94eac-151">Por brevedad, en este ejemplo se usaron índices de flujo codificados de forma fuerte cuando llama al **método IAMStreamSelect::Enable.**</span><span class="sxs-lookup"><span data-stu-id="94eac-151">For brevity, this example used hard-coded stream indexes when it calls the **IAMStreamSelect::Enable** method.</span></span> <span data-ttu-id="94eac-152">También realiza una comprobación de errores mínima.</span><span class="sxs-lookup"><span data-stu-id="94eac-152">It also performs minimal error checking.</span></span>


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



<span data-ttu-id="94eac-153">Este filtro usa la [**interfaz IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) para extraer ejemplos del filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="94eac-153">This filter uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface to pull samples from the source filter.</span></span> <span data-ttu-id="94eac-154">Por lo tanto, no admite la [**interfaz IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) en su pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="94eac-154">Therefore, it does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on its input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94eac-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94eac-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94eac-156">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="94eac-156">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



