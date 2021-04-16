---
description: En este tema se presentan los orígenes de mapas de bits, un componente básico de Windows Imaging Component (WIC) que representa los píxeles de mapa de bits de una imagen.
ms.assetid: cff0c088-ca22-4d55-9cf0-9cbe9803923e
title: Información general sobre orígenes de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910bfc253798058639b98a1d1beaacec9bd4d1bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497338"
---
# <a name="bitmap-sources-overview"></a>Información general sobre orígenes de mapas de bits

En este tema se presentan los orígenes de mapas de bits, un componente básico de Windows Imaging Component (WIC) que representa los píxeles de mapa de bits de una imagen.

En este tema se incluyen las siguientes secciones.

-   [Orígenes de mapas de bits](#bitmap-sources-overview)
-   [Marcos de mapas de bits](#bitmap-frames)
-   [Mapas de bits](#bitmap-sources-overview)
-   [Transformación de orígenes de mapas de bits](#transform-bitmap-sources)
-   [Formatos de píxel y convertidores de contexto de color](#pixel-format-and-color-context-converters)
-   [Dibujar orígenes de mapas de bits](#drawing-bitmap-sources)
-   [Temas relacionados](#related-topics)

## <a name="bitmap-sources"></a>Orígenes de mapas de bits

El componente [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) es el bloque de creación básico de WIC y representa un único conjunto de píxeles. Un origen de mapa de bits puede ser un marco individual de una imagen de un fotograma o puede ser el resultado de una transformación realizada en un origen de mapa de bits. La interfaz **IWICBitmapSource** es la base de muchas de las interfaces WIC principales, como el marco descodificador [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) y la transformación de orígenes de mapas de bits, como [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).

En la tabla siguiente se describen los diferentes componentes de origen del mapa de bits proporcionados por WIC.



| Orígenes de mapas de bits                                                    | Descripción                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) | Representa un marco de imagen del descodificador.                                    |
| [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                       | Proporciona escritura y representación en memoria a los orígenes de mapa de bits. |
| [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)         | Recorta un origen de mapa de bits a un rectángulo deseado.                        |
| [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) | Voltea o gira una fuente de mapa de bits a una orientación deseada.       |
| [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)           | Escala una fuente de mapa de bits a un tamaño deseado.                            |
| [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)       | Transforma el contexto de color de un origen de mapa de bits.                     |
| [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)     | Convierte el formato de píxel de un origen de mapa de bits.                        |



 

## <a name="bitmap-frames"></a>Marcos de mapas de bits

El más común de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) es el [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Esta interfaz se utiliza para tener acceso a los datos de mapa de bits reales de un formato de imagen. Muchos formatos de imagen solo admiten un único marco de mapa de bits, mientras que otros formatos como GIF y TIFF admiten varios fotogramas por imagen.

Para obtener un ejemplo sobre cómo obtener fotogramas de mapa de bits a partir de una imagen, vea el tema [Cómo recuperar los marcos de una imagen](https://www.bing.com/search?q=How+to+Retrieve+the+Frames+of+an+Image) .

## <a name="bitmaps"></a>Mapas de bits

Un [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) agrega los conceptos de escritura y estático en memoria a los orígenes de mapa de bits. Los mapas de bits de WIC permiten a los usuarios acceder directamente a los píxeles de un origen de mapa de bits. Este acceso directo lo proporciona el método [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) y admite cualquier combinación de acceso de lectura o escritura a los píxeles del mapa de bits. **Lock** Method bloquea el rectángulo de mapa de bits especificado y proporciona un objeto [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) para tener acceso a los píxeles.

Para obtener un ejemplo de uso de los objetos [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) y [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) , vea el tema [modificación de los píxeles de un origen de mapa de bits](-wic-bitmapsources-howto-modifypixels.md) .

## <a name="transform-bitmap-sources"></a>Transformación de orígenes de mapas de bits

WIC proporciona varias interfaces de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que transforman los datos de píxeles. En concreto, WIC proporciona transformaciones de origen de mapas de bits para escalar, recortar, girar y voltear datos de píxeles. Estas transformaciones de origen de mapa de bits son [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)y [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator). Cada uno de estos orígenes de mapa de bits tiene un método para inicializar y crear un nuevo origen de mapa de bits transformado. Por ejemplo, **IWICBitmapClipper** incluye el método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) . Este método inicializa el origen de mapa de bits de Clipper con los datos de píxeles recortados del origen de mapa de bits de entrada en el [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)determinado.

Los siguientes temas de procedimientos muestran diferentes usos de los orígenes de mapas de bits de transformación.

-   [Cómo escalar un origen de mapa de bits](-wic-bitmapsources-howto-scale.md)
-   [Cómo recortar un origen de mapa de bits](-wic-bitmapsources-howto-clip.md)
-   [Cómo voltear y girar un origen de mapa de bits](-wic-bitmapsources-howto-flipandrotate.md)

## <a name="pixel-format-and-color-context-converters"></a>Formatos de píxel y convertidores de contexto de color

WIC también proporciona orígenes de mapas de bits que convierten el formato de píxel y el contexto de color de un origen de mapa de bits. WIC proporciona [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) y [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) para estas operaciones.

[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) convierte un origen de mapa de bits determinado de un formato de píxel a otro.

Para obtener un ejemplo del uso de [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter), consulte el tema [Cómo dibujar un origen de mapa de bits mediante Direct2D](-wic-bitmapsources-howto-drawusingd2d.md) .

## <a name="drawing-bitmap-sources"></a>Dibujar orígenes de mapas de bits

WIC es una tecnología de códec de imagen fija que se usa para administrar datos y metadatos de imágenes y no proporciona de forma inherente una manera de representar imágenes. Sin embargo, los orígenes de mapas de bits se pueden dibujar utilizando varias tecnologías de gráficos de Windows como Direct2D, Windows Interfaz de dispositivo gráfico (GDI) y Windows GDI+. Cada una de estas tecnologías tiene un nivel diferente de interoperabilidad con WIC. Direct2D proporciona interoperabilidad directa a través de la interfaz [ID2D1Bitmap](../direct2d/render-targets-overview.md) y el método [ID2D1RenderTarget:: CREATEBITMAPFROMWICBITMAP](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) mientras que GDI y GDI+ requieren que los usuarios copien los píxeles de origen del mapa de bits en un [mapa de bits](../gdi/bitmaps.md).

En el ejemplo siguiente se muestra cómo dibujar orígenes de mapas de bits mediante Direct2D.

-   [Cómo dibujar un origen de mapa de bits mediante Direct2D](-wic-bitmapsources-howto-drawusingd2d.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre la codificación](-wic-creating-encoder.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
