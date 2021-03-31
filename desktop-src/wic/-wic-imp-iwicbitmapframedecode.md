---
description: Implementación de IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implementación de IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394b5858ec5eee37ef1c7f52b766806c4a0c1a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816094"
---
# <a name="implementing-iwicbitmapframedecode"></a>Implementación de IWICBitmapFrameDecode

## <a name="iwicbitmapframedecode"></a>IWICBitmapFrameDecode

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) es la interfaz de nivel de marco que proporciona acceso a los bits de imagen reales. Esta interfaz se implementa en la clase de descodificación de nivel de marco. Dado que se deriva de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), la implementación de **IWICBitmapFrameDecode** incluirá una implementación de los métodos de **IWICBitmapSource** . Los métodos adicionales en **IWICBitmapFrameDecode** proporcionan acceso a la miniatura de nivel de marco, a los contextos de color de la imagen y al lector de consultas de metadatos para el marco.

``` syntax
interface IWICBitmapFrameDecode : IWICBitmapSource
{
// Required methods
HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
HRESULT GetColorContexts ( UINT cCount, 
IWICColorContext **ppIColorContexts, UINT *pcActualCount );
HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader );

// Methods inherited from IWICBitmapSource
HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
HRESULT GetResolution ( double *pDpiX, double *pDpiY );
HRESULT CopyPixels ( const WICRect *prc, 
   UINT cbStride,
   UINT cbBufferSize, 
   BYTE *pbBuffer );
// Optional method
HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

-   [GetThumbnail](#getthumbnail)
-   [GetColorContexts](#getcolorcontexts)
-   [GetMetadataQueryReader](#getmetadataqueryreader)
-   [GetPixelFormat, y GetResolution](#getsize-getpixelformat-and-getresolution)
-   [CopyPixels](#copypixels)
-   [CopyPalette](#copypalette)

### <a name="getthumbnail"></a>GetThumbnail

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) devuelve la miniatura del fotograma actual. Por motivos de rendimiento, las miniaturas se codifican normalmente en formato JPEG. Del mismo modo que con la vista previa en el descodificador, no es necesario ni se recomienda proporcionar su propio descodificador JPEG para las miniaturas. En su lugar, debe delegar en el descodificador JPEG proporcionado por el componente de creación de imágenes de Windows (WIC).

Para obtener más información sobre las miniaturas, vea el método [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) en [implementar IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).

### <a name="getcolorcontexts"></a>GetColorContexts

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) devuelve los contextos de color válidos (también conocidos como perfiles de color) asociados a la imagen de este marco. En la mayoría de los casos, esto solo será uno, pero puede haber casos en los que haya dos o, en raras ocasiones, más. El autor de la llamada pasará uno o más objetos [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) , estableciendo el parámetro *enta* para indicar cuántos pasan. Este método rellena los objetos **IWICColorContext** con los datos de contexto de color reales de los perfiles de color asociados a la imagen. Establezca el parámetro *pcActualCount* en el número real de contextos de color asociado a la imagen, incluso si es mayor que el número que se puede devolver. (En caso de que haya más contextos de color disponibles que el número de objetos **IWICColorContext** pasados por el autor de la llamada, esto indica al llamador que hay uno o más usuarios disponibles).

### <a name="getmetadataqueryreader"></a>GetMetadataQueryReader

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) devuelve un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) que una aplicación puede usar para recuperar metadatos del marco de imagen. Esta interfaz se implementa mediante un controlador de metadatos y permite que una aplicación consulte propiedades de metadatos específicas pertenecientes a un formato de metadatos determinado. Para obtener más información, vea [implementar IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).

Para crear una instancia de [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), llame a [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) en [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a>GetPixelFormat, y GetResolution

Se explican por sí solos, [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)y [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) [**, y**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)se devuelven las propiedades solicitadas de la imagen.

### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) es el método al que llama una aplicación cuando desea crear un mapa de bits en memoria que se puede representar en la pantalla o la impresora. Este es el método que realiza la descodificación real de los bits de la imagen. Los parámetros son un rectángulo, que representa la región de interés de la imagen de origen que se va a copiar en la memoria; STRIDE, que especifica el número de bytes en una línea de recorrido; tamaño del búfer en memoria asignado por la aplicación; y un puntero al búfer en el que se deben copiar los bits de imagen solicitados. (Para evitar que las saturaciones de búfer potenciales introduzcan vulnerabilidades de seguridad, asegúrese de copiar solo los datos de imagen en el búfer que especifica el parámetro *cbBufferSize* ).

### <a name="copypalette"></a>CopyPalette

Solo los códecs que tienen formatos de píxel indexados deben implementar el método [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) . Si una imagen usa un formato indizado, use este método para devolver la paleta de colores utilizada en la imagen. Si el códec no tiene un formato indizado, devuelva WINCODEC \_ Err \_ PALETTEUNAVAILABLE.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Vista**
</dt> <dt>

[Implementación de IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Implementar IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



