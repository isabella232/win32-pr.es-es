---
description: Implementación de IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implementación de IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b49e3636f5d81202b1060d868ecb40bb99d095dd9f26b6afd0d40c5f5fd0d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205769"
---
# <a name="implementing-iwicbitmapframedecode"></a>Implementación de IWICBitmapFrameDecode

## <a name="iwicbitmapframedecode"></a>IWICBitmapFrameDecode

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) es la interfaz de nivel de fotograma que proporciona acceso a los bits de imagen reales. Esta interfaz se implementa en la clase decoding de nivel de marco. Dado que se deriva de [**IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)la implementación de **IWICBitmapFrameDecode** incluirá una implementación de los métodos **IWICBitmapSource.** Los métodos adicionales de **IWICBitmapFrameDecode** proporcionan acceso a la miniatura de nivel de fotograma, a los contextos de color de la imagen y al lector de consultas de metadatos del marco.

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
-   [GetSize, GetPixelFormat y GetResolution](#getsize-getpixelformat-and-getresolution)
-   [CopyPixels](#copypixels)
-   [CopyPalette](#copypalette)

### <a name="getthumbnail"></a>GetThumbnail

[**GetThumbnail devuelve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) la miniatura del marco actual. Por motivos de rendimiento, las miniaturas se codifican normalmente en formato JPEG. Al igual que con la versión preliminar del descodificador, no es necesario ni recomendado proporcionar su propio descodificador JPEG para las miniaturas. En su lugar, debe delegar en el descodificador JPEG proporcionado por Windows Imaging Component (WIC).

Para obtener más información sobre las miniaturas, vea el [método SetThumbnail](-wic-imp-iwicbitmapframeencode.md) en [Implementación de IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).

### <a name="getcolorcontexts"></a>GetColorContexts

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) devuelve los contextos de color válidos (también conocidos como perfiles de color) asociados a la imagen en este marco. En la mayoría de los casos, esto solo será uno, pero podría haber casos en los que haya dos o, rara vez, más. El autor de la llamada pasará uno o varios objetos [**IWICColorContext,**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) estableciendo el *parámetro cCount* para indicar cuántos pasan. Este método rellena los objetos **IWICColorContext** con los datos de contexto de color reales para los perfiles de color asociados a la imagen. Establezca el *parámetro pcActualCount en* el número real de contextos de color asociados a la imagen, aunque sea mayor que el número que puede devolver. (En el caso de que haya más contextos de color disponibles que el número de objetos **IWICColorContext** pasados por el autor de la llamada, esto indica al autor de la llamada que hay uno o varios otros disponibles).

### <a name="getmetadataqueryreader"></a>GetMetadataQueryReader

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) devuelve un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) que una aplicación puede usar para recuperar metadatos del marco de imagen. Esta interfaz se implementa mediante un controlador de metadatos y permite a una aplicación consultar propiedades de metadatos específicas que pertenecen a un formato de metadatos determinado. Para obtener más información, [vea Implementar IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).

Para crear una instancia de [**IWICMetadataQueryReader,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)llame a [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) en [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a>GetSize, GetPixelFormat y GetResolution

[**GetSize,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)y [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) son autoexplicativos y devuelven las propiedades solicitadas de la imagen.

### <a name="copypixels"></a>CopyPixels

[**CopyPixels es**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) el método al que llama una aplicación cuando desea crear un mapa de bits en memoria que se puede representar en la pantalla o impresora. Este es el método que realiza la decodificación real de los bits de imagen. Los parámetros son un rectángulo, que representa la región de interés en la imagen de origen que se va a copiar en la memoria; el stride, que especifica el número de bytes en una línea de examen; el tamaño del búfer en memoria asignado por la aplicación; y un puntero al búfer en el que se deben copiar los bits de imagen solicitados. (Para evitar que las posibles saturaciones del búfer introduzcan vulnerabilidades de seguridad, asegúrese de copiar solo tantos datos de imagen en el búfer como especifique el *parámetro cbBufferSize).*

### <a name="copypalette"></a>CopyPalette

Solo los códecs que tienen formatos de píxel indexados deben implementar [**el método CopyPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) Si una imagen usa un formato indexado, use este método para devolver la paleta de colores utilizada en la imagen. Si el códec no tiene un formato indexado, devuelva WINCODEC \_ ERR \_ PALETTEUNAVAILABLE.

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

**Conceptual**
</dt> <dt>

[Implementación de IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Implementación de IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



