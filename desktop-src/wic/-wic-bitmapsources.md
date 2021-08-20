---
description: En este tema se presentan los orígenes de mapa de bits, un componente Windows imaging component (WIC) principal que representa los píxeles de mapa de bits de una imagen.
ms.assetid: cff0c088-ca22-4d55-9cf0-9cbe9803923e
title: Información general sobre orígenes de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a72558458787c69af8440eb08d956e0670835954886144a5d19f06c13b5fb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668661"
---
# <a name="bitmap-sources-overview"></a>Información general sobre orígenes de mapa de bits

En este tema se presentan los orígenes de mapa de bits, un componente Windows imaging component (WIC) principal que representa los píxeles de mapa de bits de una imagen.

En este tema se incluyen las siguientes secciones.

-   [Orígenes de mapa de bits](#bitmap-sources-overview)
-   [Fotogramas de mapa de bits](#bitmap-frames)
-   [Mapas de bits](#bitmap-sources-overview)
-   [Transformar orígenes de mapa de bits](#transform-bitmap-sources)
-   [Convertidores de formato de píxel y contexto de color](#pixel-format-and-color-context-converters)
-   [Dibujar orígenes de mapa de bits](#drawing-bitmap-sources)
-   [Temas relacionados](#related-topics)

## <a name="bitmap-sources"></a>Orígenes de mapa de bits

El [**componente IWICBitmapSource es**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) el bloque de creación básico de WIC y representa un único conjunto de píxeles. Un origen de mapa de bits puede ser un marco individual de una imagen de varias tramas o puede ser el resultado de una transformación realizada en un origen de mapa de bits. La interfaz **IWICBitmapSource** es la base de muchas de las interfaces WIC principales, como el marco descodificador [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) y los orígenes de mapa de bits de transformación, como [**IWICBitmapFlipRotator.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)

En la tabla siguiente se describen los distintos componentes de origen de mapa de bits proporcionados por WIC.



| Orígenes de mapa de bits                                                    | Descripción                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) | Representa un marco de imagen descodificador.                                    |
| [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                       | Proporciona capacidad de escritura y representación en memoria para orígenes de mapa de bits. |
| [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)         | Recorta un origen de mapa de bits a un rectángulo deseado.                        |
| [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) | Invierte o gira un origen de mapa de bits a una orientación deseada.       |
| [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)           | Escala un origen de mapa de bits a un tamaño deseado.                            |
| [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)       | Transforma el contexto de color de un origen de mapa de bits.                     |
| [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)     | Convierte el formato de píxel de un origen de mapa de bits.                        |



 

## <a name="bitmap-frames"></a>Fotogramas de mapa de bits

El [**IWICBitmapSource más**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) común es [**IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) Esta interfaz se usa para acceder a los datos de mapa de bits reales de un formato de imagen. Muchos formatos de imagen solo admiten un único fotograma de mapa de bits, mientras que otros formatos como GIF y TIFF admiten varios fotogramas por imagen.

Para obtener un ejemplo sobre cómo obtener fotogramas de mapa de bits de una imagen, vea el tema [Cómo recuperar los fotogramas de una imagen](https://www.bing.com/search?q=How+to+Retrieve+the+Frames+of+an+Image) .

## <a name="bitmaps"></a>Mapas de bits

Un [**IWICBitmap agrega**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) los conceptos de escritura y estática en memoria a los orígenes de mapa de bits. Los mapas de bits de WIC permiten a los usuarios acceder directamente a los píxeles de un origen de mapa de bits. Este acceso directo lo proporciona el [**método Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) y admite cualquier combinación de acceso de lectura o escritura a los píxeles de mapa de bits. **El** método Lock bloquea el rectángulo de mapa de bits especificado y proporciona un [**objeto IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) para acceder a los píxeles.

Para obtener un ejemplo [**con objetos IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) e [**IWICBitmapLock,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) vea el tema [How to Modify the Pixels of a Bitmap Source](-wic-bitmapsources-howto-modifypixels.md) .

## <a name="transform-bitmap-sources"></a>Transformar orígenes de mapa de bits

WIC proporciona varias [**interfaces IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que transforman los datos de píxeles. En concreto, WIC proporciona transformaciones de origen de mapa de bits para escalar, recortar, girar y voltear datos de píxeles. Estas transformaciones de origen de mapa de bits son [**IWICBitmapClipper,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)e [**IWICBitmapFlipRotator.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) Cada uno de estos orígenes de mapa de bits tiene un método para inicializar y crear un nuevo origen de mapa de bits transformado. Por ejemplo, **IWICBitmapClipper incluye** el [**método Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) Este método inicializa el origen de mapa de bits del clipper con los datos de píxel recortados del origen de mapa de bits de entrada en el [**WICRect especificado.**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)

En los siguientes temas de procedimientos se muestran los distintos usos de los orígenes de mapa de bits de transformación.

-   [Cómo escalar un origen de mapa de bits](-wic-bitmapsources-howto-scale.md)
-   [Cómo recortar un origen de mapa de bits](-wic-bitmapsources-howto-clip.md)
-   [Cómo voltear y girar un origen de mapa de bits](-wic-bitmapsources-howto-flipandrotate.md)

## <a name="pixel-format-and-color-context-converters"></a>Convertidores de formato de píxel y contexto de color

WIC también proporciona orígenes de mapa de bits que convierten el formato de píxel y el contexto de color de un origen de mapa de bits. WIC proporciona [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) e [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) para estas operaciones.

[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) convierte un origen de mapa de bits determinado de un formato de píxel a otro.

Para obtener un ejemplo con [**IWICFormatConverter,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)vea el tema How to Draw a Bitmap Source Using Direct2D (Cómo dibujar un origen de mapa de [bits mediante Direct2D).](-wic-bitmapsources-howto-drawusingd2d.md)

## <a name="drawing-bitmap-sources"></a>Dibujar orígenes de mapa de bits

WIC es una tecnología de códec de imágenes fijas que se usa para administrar metadatos y datos de imágenes y no proporciona de forma inherente una manera de representar imágenes. Sin embargo, los orígenes de mapa de bits se pueden dibujar mediante varias tecnologías Windows gráficos como Direct2D, Windows Interfaz de dispositivo gráfico (GDI) y Windows GDI+. Cada una de estas tecnologías tiene un nivel diferente de interoperabilidad con WIC. Direct2D proporciona interoperabilidad directa a través de la interfaz [ID2D1Bitmap](../direct2d/render-targets-overview.md) y el método [ID2D1RenderTarget::CreateBitmapFromWicBitmap,](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) mientras que GDI y GDI+ requieren que los usuarios copien los píxeles de origen del mapa de bits en un mapa [de bits](../gdi/bitmaps.md).

En el ejemplo siguiente se muestra cómo dibujar orígenes de mapa de bits mediante Direct2D.

-   [Cómo dibujar un origen de mapa de bits mediante Direct2D](-wic-bitmapsources-howto-drawusingd2d.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre codificación](-wic-creating-encoder.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
