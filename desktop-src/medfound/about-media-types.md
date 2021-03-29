---
description: Acerca de los tipos de medios
ms.assetid: 169cdb00-0c1a-4530-90b7-bc89c71d1d04
title: Acerca de los tipos de medios (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca1ee75979c5c382e7e4ea458655efb83435a22d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003309"
---
# <a name="about-media-types-microsoft-media-foundation"></a>Acerca de los tipos de medios (Microsoft Media Foundation)

Un *tipo de medio* describe el formato de un flujo multimedia. En Microsoft Media Foundation, los tipos de medios se representan mediante la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Esta interfaz hereda la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Los detalles de un tipo de medio se especifican como atributos.

Para crear un nuevo tipo de archivo multimedia, llame a la función [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) . Esta función devuelve un puntero a la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . El tipo de medio no tiene inicialmente ningún atributo. Para establecer los detalles del formato, establezca los atributos correspondientes.

Para obtener una lista de los atributos de tipo de medio, consulte [atributos de tipo de medio](media-type-attributes.md).

## <a name="major-types-and-subtypes"></a>Tipos y subtipos principales

Dos partes importantes de la información para cualquier tipo de medio son el tipo principal y el subtipo.

-   El *tipo principal* es un GUID que define la categoría general de los datos en un flujo multimedia. Los tipos principales incluyen vídeo y audio. Para especificar el tipo principal, establezca el atributo de [ \_ \_ \_ tipo principal MF MT](mf-mt-major-type-attribute.md) . El método [**IMFMediaType:: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) devuelve el valor de este atributo.
-   El *subtipo* define el formato. Por ejemplo, en el tipo de vídeo principal, hay subtipos para RGB-24, RGB-32, YUY2, etc. En el audio, hay audio PCM, audio de punto flotante IEEE y otros. El subtipo proporciona más información que el tipo principal, pero no define todo lo relacionado con el formato. Por ejemplo, los subtipos de vídeo no definen el tamaño de la imagen ni la velocidad de fotogramas. Para especificar el subtipo, establezca el atributo de [ \_ \_ subtipo MF MT](mf-mt-subtype-attribute.md) .

Todos los tipos de medios deben tener un GUID de tipo principal y un GUID de subtipo. Para obtener una lista de los GUID de tipo y subtipo principales, consulte [GUID de tipo de medio](media-type-guids.md).

## <a name="why-attributes"></a>¿Por qué atributos?

Los atributos tienen varias ventajas sobre las estructuras de formato que se han usado en tecnologías anteriores como DirectShow y el SDK de Windows Media Format.

-   Es más fácil representar valores "inconscientes" o "que no le interesan". Por ejemplo, si está escribiendo una transformación de vídeo, puede conocer de antemano los formatos de RGB y YUV que admite la transformación, pero no las dimensiones del fotograma de vídeo hasta que los obtenga del origen de vídeo. Del mismo modo, es posible que no le interese algunos detalles, como los principales de vídeo. Con una estructura de formato, cada miembro se debe rellenar con *algún* valor. Como resultado, es habitual utilizar cero para indicar un valor desconocido o predeterminado. Esta práctica puede producir errores si otro componente trata a cero como un valor legítimo. Con los atributos, simplemente omite los atributos desconocidos o que no son relevantes para el componente.

-   A medida que los requisitos han cambiado con el tiempo, las estructuras de formato se extendieron agregando datos adicionales al final de la estructura. Por ejemplo, **WAVEFORMATEXTENSIBLE** extiende la estructura **WAVEFORMATEX** . Esta práctica es propensa a errores, porque los componentes deben convertir punteros de estructura en otros tipos de estructura. Los atributos se pueden extender de forma segura.
-   Se han definido estructuras de formato mutuamente incompatibles. Por ejemplo, DirectShow define las estructuras **VIDEOINFOHEADER** y **VIDEOINFOHEADER2** . Los atributos se establecen de forma independiente entre sí, por lo que este problema no se produce.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 



