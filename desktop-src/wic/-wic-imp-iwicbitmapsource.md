---
description: Implementación de IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Implementación de IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7ffd73271e8e159eea825ed40c24347ec2af98f0edbfa9ecc0d5ac584df23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965024"
---
# <a name="implementing-iwicbitmapsource"></a>Implementación de IWICBitmapSource

## <a name="iwicbitmapsource"></a>IWICBitmapSource

[**IWICBitmapSource es**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) importante para trabajar con imágenes desde la perspectiva de la aplicación. Representa la abstracción de nivel más alto para un origen de imagen y todas las interfaces del componente de creación de imágenes (WIC) de Windows que representan una imagen, incluidos [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) [**IWICBitmap y**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)todas las interfaces de transformación [**(IWICBitmapScaler,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) [**IWICBitmapClipper,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter)**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)se derivan de ella. En cualquier momento específico, un **objeto IWICBitmapSource** puede estar o no con el respaldo de un mapa de bits real en la memoria. Esto permite un procesamiento muy eficaz por parte de una aplicación, ya que una imagen se puede tratar como una abstracción. Las operaciones de transformación se pueden encadenar en una canalización de transformación sin consumir recursos de memoria hasta que la aplicación esté lista para representar o imprimir la imagen, momento en el que invoca el [**método CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) en la transformación final para obtener un mapa de bits en la memoria de la imagen con las transformaciones seleccionadas aplicadas.

``` syntax
interface IWICBitmapSource : IUnknown
{
   // Required methods
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

Desde la perspectiva del códec, los [**métodos IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) se implementan en el objeto descodificador de fotogramas. Estos métodos se describen en Implementación de IWICBitmapSource, junto con los otros métodos en [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), que se deriva de **IWICBitmapSource**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Implementación de IWICBitmapCodecProgressNotification (Descodificador)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Implementación de IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



