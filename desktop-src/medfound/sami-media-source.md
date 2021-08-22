---
description: Synchronized Accessible Media Interchange (SAMI) es un formato para agregar subtítulos a medios digitales.
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: Origen multimedia SAMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7567f7479b6f8d0d2439f89dbf3e6cf273fc7dcae31590ddf9b51a4d66a6940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034823"
---
# <a name="sami-media-source"></a>Origen multimedia SAMI

Synchronized Accessible Media Interchange (SAMI) es un formato para agregar subtítulos a medios digitales. Los subtítulos se almacenan en un archivo de texto independiente con la extensión de nombre de archivo .smi o .sami.

En Media Foundation, los archivos de subtítulos SAMI se admiten a través del origen multimedia SAMI. Use el [solucionador de origen](source-resolver.md) para crear una instancia del origen multimedia SAMI a partir de una dirección URL o secuencia de bytes. Media Foundation no proporciona un componente que muestre los títulos SAMI. La aplicación debe interpretar los datos de título que recibe del origen multimedia SAMI.

A continuación se muestra un archivo SAMI de ejemplo.

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

El `<STYLE>` elemento contiene información de estilo. Este ejemplo contiene un estilo base para `<P>` los elementos, junto con dos estilos con nombre, "standard" y "hilite". Los estilos con nombre se usan para modificar el estilo base. Los títulos se colocan dentro de `<SYNC>` los elementos . El atributo start proporciona el tiempo de presentación en milisegundos para ese título. Los títulos de este ejemplo se dan en dos idiomas, especificados por sus etiquetas de idioma RFC-1766, "en-US" y "fr -FR". Dentro de los subtítulos, los idiomas se identifican por sus nombres de clase; en este caso, "ENUSCC" y "FRFRCC".

El origen multimedia SAMI crea una secuencia multimedia para cada idioma. De forma predeterminada, se selecciona la primera secuencia y se deselecciona el resto de secuencias. La aplicación puede cambiar la selección de secuencias llamando [**a IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) y [**IMFPresentationDescriptor::D eselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream). Cada descriptor de flujo contiene los atributos siguientes.



| Atributo                                                       | Descripción                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [**MF \_ SD \_ LANGUAGE**](mf-sd-language-attribute.md)            | Etiqueta de idioma, según lo especificado por el `lang` atributo .  |
| [**MF \_ SD \_ SAMI \_ LANGUAGE**](mf-sd-sami-language-attribute.md) | Nombre de idioma, tal como lo especifica el `Name` atributo . |



 

Cada secuencia tiene el siguiente tipo de medio:



| Atributo                                                                            | Value                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [**TIPO \_ PRINCIPAL DE MT \_ DE \_ MF**](mf-mt-major-type-attribute.md)                            | **MFMediaType \_ SAMI** |
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) | **TRUE**              |



 

El origen SAMI entrega cada título en un ejemplo multimedia independiente. La marca de tiempo de ejemplo y la duración se derivan del `<SYNC>` elemento . El búfer multimedia contenido en el ejemplo contiene el título como texto ASCII. El estilo de título se incrusta en el título como un atributo `STYLE` insertado. Por ejemplo, dado el archivo SAMI anterior y el uso de la secuencia en inglés con los estilos predeterminados, el primer búfer multimedia contendrá los datos siguientes. (Los saltos de línea pueden diferir de lo que se muestra aquí).

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a>Estilos SAMI

Para cambiar el estilo actual, use la [**interfaz IMFSAMIStyle.**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) Esta interfaz se obtiene mediante una llamada [**a IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el origen multimedia SAMI. (Si usa el origen multimedia SAMI con la sesión multimedia, llame a **GetService** en la sesión multimedia). El identificador de servicio **es MF \_ SAMI \_ SERVICE.**

En el ejemplo siguiente se establece el estilo SAMI actual, especificado por index.


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



Este ejemplo llama a los métodos siguientes en el origen multimedia SAMI:

-   [**IMFSAMIStyle::GetStyleCount obtiene**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) el número de estilos.
-   [**IMFSAMIStyle::GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) obtiene una lista de los nombres de estilo, almacenados en **un elemento PROPVARIANT.**
-   [**IMFSAMIStyle::SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) establece un estilo por nombre.

La lista de nombres de estilo también se almacena en el descriptor de presentación, en el atributo [**MF \_ PD \_ SAMI \_ STYLELIST.**](mf-pd-sami-stylelist-attribute.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes multimedia y receptores](media-sources-and-sinks.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



