---
description: Obtenga información sobre los tipos de medios Microsoft Media Foundation. Un tipo de medio describe el formato de una secuencia multimedia.
ms.assetid: 169cdb00-0c1a-4530-90b7-bc89c71d1d04
title: Acerca de los tipos de medios (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263c2b473e378e6ae5dc75453b20d02dce61818f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269428"
---
# <a name="about-media-types-microsoft-media-foundation"></a>Acerca de los tipos de medios (Microsoft Media Foundation)

Un *tipo de medio* describe el formato de una secuencia multimedia. En Microsoft Media Foundation, los tipos de medios se representan mediante la [**interfaz IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) Esta interfaz hereda la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Los detalles de un tipo de medio se especifican como atributos.

Para crear un nuevo tipo de medio, llame a [**la función MFCreateMediaType.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) Esta función devuelve un puntero a la [**interfaz IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) El tipo de medio inicialmente no tiene atributos. Para establecer los detalles del formato, establezca los atributos pertinentes.

Para obtener una lista de atributos de tipo de medio, vea [Atributos de tipo de medio](media-type-attributes.md).

## <a name="major-types-and-subtypes"></a>Tipos principales y subtipos

Dos elementos importantes de información para cualquier tipo de medio son el tipo principal y el subtipo.

-   El *tipo principal* es un GUID que define la categoría general de los datos en un flujo multimedia. Los tipos principales incluyen vídeo y audio. Para especificar el tipo principal, establezca el atributo [MF \_ MT MAJOR \_ \_ TYPE.](mf-mt-major-type-attribute.md) El [**método IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) devuelve el valor de este atributo.
-   El *subtipo define* aún más el formato. Por ejemplo, dentro del tipo principal de vídeo, hay subtipos para RGB-24, RGB-32, YUY2, etc. Dentro del audio, hay audio PCM, audio de punto flotante IEEE y otros. El subtipo proporciona más información que el tipo principal, pero no define todo sobre el formato. Por ejemplo, los subtipos de vídeo no definen el tamaño de la imagen ni la velocidad de fotogramas. Para especificar el subtipo, establezca el atributo [MF \_ MT \_ SUBTYPE.](mf-mt-subtype-attribute.md)

Todos los tipos de medios deben tener un GUID de tipo principal y un GUID de subtipo. Para obtener una lista de GUID de tipo principal y subtipo, vea [GUID de tipo multimedia](media-type-guids.md).

## <a name="why-attributes"></a>¿Por qué atributos?

Los atributos tienen varias ventajas con respecto a las estructuras de formato que se han usado en tecnologías anteriores, como DirectShow y el SDK Windows Media Format.

-   Es más fácil representar los valores "don't know" o "don't care". Por ejemplo, si está escribiendo una transformación de vídeo, es posible que sepa de antemano qué formatos RGB y YUV admite la transformación, pero no las dimensiones del fotograma de vídeo, hasta que las obtenga del origen del vídeo. De forma similar, es posible que no le preocupa ciertos detalles, como los vídeos principal. Con una estructura de formato, cada miembro debe rellenarse con *algún* valor. Como resultado, es habitual usar cero para indicar un valor desconocido o predeterminado. Esta práctica puede producir errores si otro componente trata cero como un valor legítimo. Con los atributos, simplemente se omiten los atributos que son desconocidos o no son relevantes para el componente.

-   A medida que los requisitos han cambiado con el tiempo, las estructuras de formato se ampliaron agregando datos adicionales al final de la estructura. Por ejemplo, **ESTANDOATEXTENSIBLE** extiende la **estructura DE LA FORMADETEATEX.** Esta práctica es propensa a errores, ya que los componentes deben convertir punteros de estructura a otros tipos de estructura. Los atributos se pueden extender de forma segura.
-   Se han definido estructuras de formato incompatibles mutuamente. Por ejemplo, DirectShow define las **estructuras VIDEOINFOHEADER** y **VIDEOINFOHEADER2.** Los atributos se establecen de forma independiente entre sí, por lo que este problema no surge.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 



