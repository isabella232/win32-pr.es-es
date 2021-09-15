---
description: Implementación de IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementación de IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247575"
---
# <a name="implementing-iwicbitmapsourcetransform"></a>Implementación de IWICBitmapSourceTransform

## <a name="iwicbitmapsourcetransform"></a>IWICBitmapSourceTransform

Aunque es opcional, se recomienda encarecidamente que cada descodificador implemente esta interfaz en la clase de descodificación de nivel de marco, ya que puede proporcionar importantes ventajas de rendimiento. Cuando una aplicación solicita una región específica de interés, tamaño, orientación o formato de píxel, en lugar de descodificar toda la imagen a una resolución completa y, a continuación, aplicar las transformaciones solicitadas, Windows Imaging Component (WIC) llama a [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para esta interfaz en el objeto [**IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) Si el descodificador de fotogramas lo admite, WIC llama al método o métodos adecuados para determinar si el descodificador de fotogramas puede realizar la transformación solicitada o determinar el formato de píxel o tamaño más cercano que el descodificador puede proporcionar al solicitado. Si el descodificador puede realizar la transformación o las transformaciones solicitadas, WIC invoca [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con los parámetros adecuados. Si el descodificador puede realizar algunas, pero no todas las transformaciones solicitadas, WIC pide al descodificador que realice los objetos de transformación de WIC [**(IWICBitmapScaler,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) [**IWICBitmapClipper,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)y [**IWICFormatConverter)**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)para realizar las transformaciones restantes que el descodificador de fotogramas no pudo realizar en el resultado de la llamada **a CopyPixels.** Si el descodificador no admite [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)WIC debe usar los objetos de transformación para realizar todas las transformaciones. Normalmente, el descodificador suele ser mucho más eficaz para realizar transformaciones durante el proceso de descodificación que descodificar toda la imagen y, a continuación, realizar las transformaciones. Esto es especialmente cierto para operaciones como el escalado a un tamaño mucho menor o conversiones de formato de píxel.


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [DoesSupportTransform](#doessupporttransform)
-   [CopyPixels](#copypixels)
-   [GetClosestSize](#getclosestsize)
-   [GetClosestPixelFormat](#getclosestpixelformat)

### <a name="doessupporttransform"></a>DoesSupportTransform

[**DoesSupportTransform pregunta**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) si el descodificador admite la operación de rotación o volteo solicitada. Las [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) que se pueden solicitar son:


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) realiza el trabajo real de lacodización de los bits de imagen, como el [**método CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) en la interfaz [**IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) pero el método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) en [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) es mucho más eficaz y puede mejorar significativamente el rendimiento del procesamiento de imágenes.

Cuando se solicitan varias operaciones de transformación, el resultado depende del orden en que se realizan las operaciones. Para garantizar la predictibilidad y la coherencia entre códecs, es importante que todos los códecs realicen estas operaciones en el mismo orden. Este es el orden canónico para realizar estas operaciones.

1.  Escala
2.  Recortar
3.  Girar

La conversión de formato de píxel se puede realizar en cualquier momento, porque no tiene ningún efecto en las otras transformaciones.

El primer parámetro, *prcSrc*, se usa para especificar la región de interés para recortar la imagen. Dado que el escalado se realiza antes del recorte por convención, si la imagen se va a escalar y recortar, la región de interés debe determinarse después de que se haya escalado la imagen.

El segundo y tercer parámetro indican el tamaño al que se va a escalar la imagen.

El *parámetro pguidDstFormat* indica el formato de píxel solicitado para la imagen descodificada. Dado que WIC ya ha llamado a [**GetClosestPixelFormat,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)debe ser un formato de píxel que el descodificador haya indicado que admite.

El *parámetro dstTransform* indica el ángulo de rotación solicitado y si se va a voltear la imagen vertical, horizontalmente o ambos. De nuevo, dado que WIC ya habrá llamado [**a DoesSupportTransform,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)la transformación solicitada debe ser una que el descodificador ya haya indicado que admite. Recuerde que la rotación siempre debe realizarse después del escalado y el recorte.

### <a name="getclosestsize"></a>GetClosestSize

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) toma dos parámetros de entrada y salida. El autor de la llamada usa los parámetros *puiWidth* y *puiHeight* para especificar el tamaño con el que el autor de la llamada prefiere descodificar la imagen. Sin embargo, un descodificador puede descodificar una imagen solo a un tamaño que sea un múltiplo de su tamaño DCT, y los distintos formatos de imagen pueden tener diferentes tamaños de DCT. El descodificador debe determinar, en función de su propio tamaño DCT, lo más cercano que pueda llegar al tamaño solicitado y establecer *puiWidth* y *puiHeight* en esas dimensiones en la devolución. Si se solicita un tamaño mayor, pero el códec no admite el escalado superior, se debe devolver el original.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) se usa para determinar el formato de píxel más cercano al formato de píxel solicitado que el descodificador puede proporcionar sin pérdida de datos. Siempre es preferible convertir a un formato de píxel más ancho que uno más estrecho, aunque aumente el tamaño de la imagen, ya que siempre se puede reconvertir a un formato más restrictivo si es necesario. Sin embargo, una vez perdidos los datos, no se pueden recuperar.

## <a name="continued-reading"></a>Lectura continua

Para más información sobre cómo crear un códec habilitado para WIC, consulte [Implementación de IWICDevelopRaw.](-wic-imp-iwicdevelopraw.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Implementación de IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Implementación de IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
