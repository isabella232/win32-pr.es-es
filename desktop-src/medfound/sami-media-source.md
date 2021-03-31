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
# <a name="sami-media-source"></a>Origen de medios SAMI

El intercambio de multimedia accesible sincronizado (SAMI) es un formato para agregar leyendas a medios digitales. Los subtítulos se almacenan en un archivo de texto independiente con la extensión de nombre de archivo. SMI o. Sami.

En Media Foundation, los archivos de subtítulos SAMI se admiten a través del origen de medios SAMI. Utilice el [solucionador de origen](source-resolver.md) para crear una instancia del origen de medios Sami a partir de una dirección URL o un flujo de bytes. Media Foundation no proporciona un componente que muestre los subtítulos SAMI. La aplicación debe interpretar los datos de los títulos que recibe del origen de medios SAMI.

A continuación se muestra un ejemplo de archivo SAMI.

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

El `<STYLE>` elemento contiene información de estilo. Este ejemplo contiene un estilo base para `<P>` los elementos, junto con dos estilos con nombre, "Standard" y "HiLite". Los estilos con nombre se usan para modificar el estilo base. Los títulos se colocan dentro de `<SYNC>` los elementos. El atributo Start proporciona el tiempo de presentación en milisegundos para ese título. Los títulos de este ejemplo se proporcionan en dos idiomas, especificados por las etiquetas de idioma RFC-1766, "en-US" y "fr-FR". Dentro de los títulos, los idiomas se identifican por sus nombres de clase; en este caso, "ENUSCC" y "FRFRCC".

El origen de medios SAMI crea un flujo de medios para cada idioma. De forma predeterminada, se selecciona la primera secuencia y se anula la selección de los flujos restantes. La aplicación puede cambiar la selección de flujo mediante una llamada a [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) y [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream). Cada descriptor de flujo contiene los siguientes atributos.



| Atributo                                                       | Descripción                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [**\_idioma MF SD \_**](mf-sd-language-attribute.md)            | Etiqueta de idioma, tal y como se especifica en el `lang` atributo.  |
| [**\_ \_ idioma sami MF \_ SD**](mf-sd-sami-language-attribute.md) | Nombre del idioma, tal y como lo especifica el `Name` atributo. |



 

Cada flujo tiene el siguiente tipo de medio:



| Atributo                                                                            | Value                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                            | **MFMediaType \_ Sami** |
| [**MF \_ MT \_ All \_ Samples \_ independiente**](mf-mt-all-samples-independent-attribute.md) | **TRUE**              |



 

El origen SAMI entrega cada título en un ejemplo multimedia independiente. La marca de tiempo y la duración de ejemplo se derivan del `<SYNC>` elemento. El búfer multimedia contenido en el ejemplo contiene el título como texto ASCII. El estilo de título se incrusta en el título como un atributo en línea `STYLE` . Por ejemplo, dado el archivo SAMI anterior y el uso de la secuencia en inglés con los estilos predeterminados, el primer búfer multimedia contendría los datos siguientes. (Los saltos de línea pueden diferir de lo que se muestra aquí).

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

Para cambiar el estilo actual, use la interfaz [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) . Esta interfaz se obtiene llamando a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el origen de medios Sami. (Si usa el origen de medios SAMI con la sesión multimedia, llame a **GetService** en la sesión multimedia). El identificador de servicio es **MF \_ Sami \_ Service**.

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



En este ejemplo se llama a los métodos siguientes en el origen de medios SAMI:

-   [**IMFSAMIStyle:: GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) obtiene el número de estilos.
-   [**IMFSAMIStyle:: GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) obtiene una lista de los nombres de estilo, almacenados en una **PROPVARIANT**.
-   [**IMFSAMIStyle:: SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) establece un estilo por nombre.

La lista de nombres de estilo también se almacena en el descriptor de presentación, en el atributo [**\_ \_ \_ STYLELIST de MF PD**](mf-pd-sami-stylelist-attribute.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes y receptores de medios](media-sources-and-sinks.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



