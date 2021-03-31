---
description: El intercambio de multimedia accesible sincronizado (SAMI) es un formato para agregar leyendas a medios digitales.
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: Origen de medios SAMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340b51815b130cb41061478358b2ab9dcf68f60
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104083568"
---
# <a name="sami-media-source"></a><span data-ttu-id="f0c37-103">Origen de medios SAMI</span><span class="sxs-lookup"><span data-stu-id="f0c37-103">SAMI Media Source</span></span>

<span data-ttu-id="f0c37-104">El intercambio de multimedia accesible sincronizado (SAMI) es un formato para agregar leyendas a medios digitales.</span><span class="sxs-lookup"><span data-stu-id="f0c37-104">Synchronized Accessible Media Interchange (SAMI) is a format for adding captions to digital media.</span></span> <span data-ttu-id="f0c37-105">Los subtítulos se almacenan en un archivo de texto independiente con la extensión de nombre de archivo. SMI o. Sami.</span><span class="sxs-lookup"><span data-stu-id="f0c37-105">The captions are stored in a separate text file with the file name extension .smi or .sami.</span></span>

<span data-ttu-id="f0c37-106">En Media Foundation, los archivos de subtítulos SAMI se admiten a través del origen de medios SAMI.</span><span class="sxs-lookup"><span data-stu-id="f0c37-106">In Media Foundation, SAMI caption files are supported through the SAMI media source.</span></span> <span data-ttu-id="f0c37-107">Utilice el [solucionador de origen](source-resolver.md) para crear una instancia del origen de medios Sami a partir de una dirección URL o un flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="f0c37-107">Use the [Source Resolver](source-resolver.md) to create an instance of the SAMI media source from a URL or byte stream.</span></span> <span data-ttu-id="f0c37-108">Media Foundation no proporciona un componente que muestre los subtítulos SAMI.</span><span class="sxs-lookup"><span data-stu-id="f0c37-108">Media Foundation does not provide a component that displays SAMI captions.</span></span> <span data-ttu-id="f0c37-109">La aplicación debe interpretar los datos de los títulos que recibe del origen de medios SAMI.</span><span class="sxs-lookup"><span data-stu-id="f0c37-109">The application must interpret the caption data that it receives from the SAMI media source.</span></span>

<span data-ttu-id="f0c37-110">A continuación se muestra un ejemplo de archivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="f0c37-110">The following shows an example SAMI file.</span></span>

``` syntax
<SAMI>
<HEAD>
    <STYLE TYPE="text/css">
    <!--
    P {
        font-family: Arial;
        background: #000000;
        text-align: center;
        }

#standard {Name: Standard; color: #FFFFFF; font-size: 14pt; } 
#hilite {Name: Youth; color: greenyellow; font-size: 18pt;}

    .ENUSCC { Name: English; lang: EN-US-CC; }
    .FRFRCC { Name: French; lang: fr-FR; } 

    -->
    </STYLE>
</HEAD>
<BODY>
    <SYNC Start="0">
        <P Class="ENUSCC">The <I>first</I> caption.</P>
        <P Class="FRFRCC">Un</P>
    </SYNC>
    <SYNC Start="3000">
        <P Class="ENUSCC">The <I>second</I> caption.</P>
        <P Class="FRFRCC">Deux</P>
    </SYNC>
    <SYNC Start="5000">
        <P Class="ENUSCC">The <I>third</I> caption.</P>
        <P Class="FRFRCC">Trois</P>
    </SYNC>
</BODY>
</SAMI>
```

<span data-ttu-id="f0c37-111">El `<STYLE>` elemento contiene información de estilo.</span><span class="sxs-lookup"><span data-stu-id="f0c37-111">The `<STYLE>` element contains style information.</span></span> <span data-ttu-id="f0c37-112">Este ejemplo contiene un estilo base para `<P>` los elementos, junto con dos estilos con nombre, "Standard" y "HiLite".</span><span class="sxs-lookup"><span data-stu-id="f0c37-112">This example contains a base style for `<P>` elements, along with two named styles, "standard" and "hilite".</span></span> <span data-ttu-id="f0c37-113">Los estilos con nombre se usan para modificar el estilo base.</span><span class="sxs-lookup"><span data-stu-id="f0c37-113">The named styles are used to modify the base style.</span></span> <span data-ttu-id="f0c37-114">Los títulos se colocan dentro de `<SYNC>` los elementos.</span><span class="sxs-lookup"><span data-stu-id="f0c37-114">Captions are placed within `<SYNC>` elements.</span></span> <span data-ttu-id="f0c37-115">El atributo Start proporciona el tiempo de presentación en milisegundos para ese título.</span><span class="sxs-lookup"><span data-stu-id="f0c37-115">The start attribute gives the presentation time in milliseconds for that caption.</span></span> <span data-ttu-id="f0c37-116">Los títulos de este ejemplo se proporcionan en dos idiomas, especificados por las etiquetas de idioma RFC-1766, "en-US" y "fr-FR".</span><span class="sxs-lookup"><span data-stu-id="f0c37-116">The captions in this example are given in two languages, specified by their RFC-1766 language tags, "en-US" and "fr -FR".</span></span> <span data-ttu-id="f0c37-117">Dentro de los títulos, los idiomas se identifican por sus nombres de clase; en este caso, "ENUSCC" y "FRFRCC".</span><span class="sxs-lookup"><span data-stu-id="f0c37-117">Within the captions, languages are identified by their class names; in this case, "ENUSCC" and "FRFRCC".</span></span>

<span data-ttu-id="f0c37-118">El origen de medios SAMI crea un flujo de medios para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="f0c37-118">The SAMI media source creates one media stream for each language.</span></span> <span data-ttu-id="f0c37-119">De forma predeterminada, se selecciona la primera secuencia y se anula la selección de los flujos restantes.</span><span class="sxs-lookup"><span data-stu-id="f0c37-119">By default, the first stream is selected and the remaining streams are deselected.</span></span> <span data-ttu-id="f0c37-120">La aplicación puede cambiar la selección de flujo mediante una llamada a [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) y [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span><span class="sxs-lookup"><span data-stu-id="f0c37-120">The application can change the stream selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span> <span data-ttu-id="f0c37-121">Cada descriptor de flujo contiene los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="f0c37-121">Each stream descriptor contains the following attributes.</span></span>



| <span data-ttu-id="f0c37-122">Atributo</span><span class="sxs-lookup"><span data-stu-id="f0c37-122">Attribute</span></span>                                                       | <span data-ttu-id="f0c37-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0c37-123">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="f0c37-124">**\_idioma MF SD \_**</span><span class="sxs-lookup"><span data-stu-id="f0c37-124">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)            | <span data-ttu-id="f0c37-125">Etiqueta de idioma, tal y como se especifica en el `lang` atributo.</span><span class="sxs-lookup"><span data-stu-id="f0c37-125">Language tag, as given by the `lang` attribute.</span></span>  |
| [<span data-ttu-id="f0c37-126">**\_ \_ idioma sami MF \_ SD**</span><span class="sxs-lookup"><span data-stu-id="f0c37-126">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="f0c37-127">Nombre del idioma, tal y como lo especifica el `Name` atributo.</span><span class="sxs-lookup"><span data-stu-id="f0c37-127">Language name, as given by the `Name` attribute.</span></span> |



 

<span data-ttu-id="f0c37-128">Cada flujo tiene el siguiente tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="f0c37-128">Each stream has the following media type:</span></span>



| <span data-ttu-id="f0c37-129">Atributo</span><span class="sxs-lookup"><span data-stu-id="f0c37-129">Attribute</span></span>                                                                            | <span data-ttu-id="f0c37-130">Value</span><span class="sxs-lookup"><span data-stu-id="f0c37-130">Value</span></span>                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [<span data-ttu-id="f0c37-131">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="f0c37-131">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="f0c37-132">**MFMediaType \_ Sami**</span><span class="sxs-lookup"><span data-stu-id="f0c37-132">**MFMediaType\_SAMI**</span></span> |
| [<span data-ttu-id="f0c37-133">**MF \_ MT \_ All \_ Samples \_ independiente**</span><span class="sxs-lookup"><span data-stu-id="f0c37-133">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="f0c37-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="f0c37-134">**TRUE**</span></span>              |



 

<span data-ttu-id="f0c37-135">El origen SAMI entrega cada título en un ejemplo multimedia independiente.</span><span class="sxs-lookup"><span data-stu-id="f0c37-135">The SAMI source delivers each caption in a separate media sample.</span></span> <span data-ttu-id="f0c37-136">La marca de tiempo y la duración de ejemplo se derivan del `<SYNC>` elemento.</span><span class="sxs-lookup"><span data-stu-id="f0c37-136">The sample time stamp and duration are derived from the `<SYNC>` element.</span></span> <span data-ttu-id="f0c37-137">El búfer multimedia contenido en el ejemplo contiene el título como texto ASCII.</span><span class="sxs-lookup"><span data-stu-id="f0c37-137">The media buffer contained in the sample holds the caption as ASCII text.</span></span> <span data-ttu-id="f0c37-138">El estilo de título se incrusta en el título como un atributo en línea `STYLE` .</span><span class="sxs-lookup"><span data-stu-id="f0c37-138">The caption style is embedded in the caption as an inline `STYLE` attribute.</span></span> <span data-ttu-id="f0c37-139">Por ejemplo, dado el archivo SAMI anterior y el uso de la secuencia en inglés con los estilos predeterminados, el primer búfer multimedia contendría los datos siguientes.</span><span class="sxs-lookup"><span data-stu-id="f0c37-139">For example, given the previous SAMI file, and using the English-language stream with the default styles, the first media buffer would contain the following data.</span></span> <span data-ttu-id="f0c37-140">(Los saltos de línea pueden diferir de lo que se muestra aquí).</span><span class="sxs-lookup"><span data-stu-id="f0c37-140">(The line breaks might differ from what is shown here.)</span></span>

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a><span data-ttu-id="f0c37-141">Estilos SAMI</span><span class="sxs-lookup"><span data-stu-id="f0c37-141">SAMI Styles</span></span>

<span data-ttu-id="f0c37-142">Para cambiar el estilo actual, use la interfaz [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .</span><span class="sxs-lookup"><span data-stu-id="f0c37-142">To change the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span> <span data-ttu-id="f0c37-143">Esta interfaz se obtiene llamando a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el origen de medios Sami.</span><span class="sxs-lookup"><span data-stu-id="f0c37-143">This interface is obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the SAMI media source.</span></span> <span data-ttu-id="f0c37-144">(Si usa el origen de medios SAMI con la sesión multimedia, llame a **GetService** en la sesión multimedia). El identificador de servicio es **MF \_ Sami \_ Service**.</span><span class="sxs-lookup"><span data-stu-id="f0c37-144">(If you are using the SAMI media source with the Media Session, call **GetService** on the Media Session.) The service identifier is **MF\_SAMI\_SERVICE**.</span></span>

<span data-ttu-id="f0c37-145">En el ejemplo siguiente se establece el estilo SAMI actual, especificado por index.</span><span class="sxs-lookup"><span data-stu-id="f0c37-145">The following example sets the current SAMI style, specified by index.</span></span>


```C++
HRESULT SetSAMIStyleByIndex(IMFMediaSource *pSource, DWORD index)
{
    IMFSAMIStyle *pSami = NULL;

    DWORD cStyles;
    PROPVARIANT varStyles;

    HRESULT hr = MFGetService(pSource, MF_SAMI_SERVICE, IID_PPV_ARGS(&pSami));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->GetStyleCount(&cStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    if (index >= cStyles)
    {
        hr = E_INVALIDARG;
        goto done;
    }

    hr = pSami->GetStyles(&varStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->SetSelectedStyle(varStyles.calpwstr.pElems[index]);

done:
    PropVariantClear(&varStyles);
    SafeRelease(&pSami);
    return hr;
}
```



<span data-ttu-id="f0c37-146">En este ejemplo se llama a los métodos siguientes en el origen de medios SAMI:</span><span class="sxs-lookup"><span data-stu-id="f0c37-146">This example calls the following methods on the SAMI media source:</span></span>

-   <span data-ttu-id="f0c37-147">[**IMFSAMIStyle:: GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) obtiene el número de estilos.</span><span class="sxs-lookup"><span data-stu-id="f0c37-147">[**IMFSAMIStyle::GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) gets the number of styles.</span></span>
-   <span data-ttu-id="f0c37-148">[**IMFSAMIStyle:: GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) obtiene una lista de los nombres de estilo, almacenados en una **PROPVARIANT**.</span><span class="sxs-lookup"><span data-stu-id="f0c37-148">[**IMFSAMIStyle::GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) gets a list of the style names, stored in a **PROPVARIANT**.</span></span>
-   <span data-ttu-id="f0c37-149">[**IMFSAMIStyle:: SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) establece un estilo por nombre.</span><span class="sxs-lookup"><span data-stu-id="f0c37-149">[**IMFSAMIStyle::SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) sets a style by name.</span></span>

<span data-ttu-id="f0c37-150">La lista de nombres de estilo también se almacena en el descriptor de presentación, en el atributo [**\_ \_ \_ STYLELIST de MF PD**](mf-pd-sami-stylelist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="f0c37-150">The list of style names is also stored on the presentation descriptor, in the [**MF\_PD\_SAMI\_STYLELIST**](mf-pd-sami-stylelist-attribute.md) attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0c37-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f0c37-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0c37-152">Orígenes y receptores de medios</span><span class="sxs-lookup"><span data-stu-id="f0c37-152">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="f0c37-153">Formatos de medios admitidos en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0c37-153">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



