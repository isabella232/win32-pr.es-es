---
description: Implementación de IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementación de IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361036"
---
# <a name="implementing-iwicbitmapsourcetransform"></a>Implementación de IWICBitmapSourceTransform

## <a name="iwicbitmapsourcetransform"></a>IWICBitmapSourceTransform

Aunque es opcional, se recomienda encarecidamente que cada descodificador implemente esta interfaz en la clase de descodificación de nivel de marco, ya que puede proporcionar ventajas de rendimiento importantes. Cuando una aplicación solicita una región específica de interés, tamaño, orientación o formato de píxeles, en lugar de simplemente descodificar toda la imagen a resolución completa y, a continuación, aplicar las transformaciones solicitadas, Windows Imaging Component (WIC) llama a [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para esta interfaz en el objeto [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) . Si el descodificador de fotogramas lo admite, WIC llama al método o métodos adecuados para determinar si el descodificador de fotogramas puede realizar la transformación solicitada o determinar el tamaño o el formato de píxel más cercano que el descodificador puede proporcionar al solicitado. Si el descodificador puede realizar la transformación o transformaciones solicitadas, WIC invoca [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con los parámetros adecuados. Si el descodificador puede realizar algunas, pero no todas las transformaciones solicitadas, WIC pide al descodificador que realice las transformaciones que se pueden realizar y usa los objetos de transformación de WIC ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)y [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) para realizar las transformaciones restantes que el descodificador de marcos no pudo realizar en el resultado de la llamada de **copyPixels** . Si el descodificador no admite [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), WIC debe utilizar los objetos de transformación para realizar todas las transformaciones. Normalmente, es mucho más eficaz para el descodificador realizar transformaciones durante el proceso de descodificación que descodificar toda la imagen y, a continuación, realizar las transformaciones. Esto es especialmente cierto para las operaciones como el escalado a un tamaño mucho menor o a las conversiones de formato de píxel.


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

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) pregunta si el descodificador admite la rotación solicitada o la operación de volteo. Los [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) que se pueden solicitar son:


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

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) realiza el trabajo real de descodificar los bits de imagen, como el método [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) en la interfaz [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , pero el método [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) en [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) es mucho más eficaz y puede mejorar significativamente el rendimiento del procesamiento de imágenes.

Cuando se solicitan varias operaciones de transformación, el resultado depende del orden en el que se realizan las operaciones. Para garantizar la previsibilidad y la coherencia entre los códecs, es importante que todos los códecs realicen estas operaciones en el mismo orden. Este es el orden canónico para realizar estas operaciones.

1.  Escala
2.  Recortar
3.  Girar

La conversión de formato de píxeles se puede realizar en cualquier momento, ya que no tiene ningún efecto en las otras transformaciones.

El primer parámetro, *prcSrc*, se usa para especificar la región de interés para recortar la imagen. Dado que el escalado se realiza antes del recorte por Convención, si la imagen se va a escalar y recortar, la región de interés debe determinarse después de que la imagen se haya escalado.

Los parámetros segundo y tercero indican el tamaño al que se va a escalar la imagen.

El parámetro *pguidDstFormat* indica el formato de píxel solicitado para la imagen descodificada. Dado que WIC ya ha llamado a [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), debe ser un formato de píxel que el descodificador haya indicado que admite.

El parámetro *dstTransform* indica el ángulo de giro solicitado y si se va a voltear la imagen verticalmente, horizontalmente o ambos. De nuevo, dado que WIC ya habrá llamado a [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), la transformación solicitada debe ser una que el descodificador ya haya indicado que admite. Recuerde que el giro siempre debe realizarse después de ajustar el tamaño y el recorte.

### <a name="getclosestsize"></a>GetClosestSize

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) toma dos parámetros in/out. El autor de la llamada utiliza los parámetros *puiWidth* y *puiHeight* para especificar el tamaño en el que el llamador prefiere la descodificación de la imagen. Sin embargo, un descodificador puede descodificar una imagen solo en un tamaño que es múltiplo de su tamaño DCT y distintos formatos de imagen pueden tener distintos tamaños DCT. El descodificador debe determinar, en función de su propio tamaño DCT, el más cercano puede ser el tamaño solicitado y establecer *puiWidth* y *puiHeight* en esas dimensiones en la devolución. Si se solicita un tamaño mayor, pero el códec no admite el escalado, se debe devolver el original.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) se usa para determinar el formato de píxel más cercano al formato de píxel solicitado que el descodificador puede proporcionar sin pérdida de datos. Siempre es preferible convertir a un formato de píxel más ancho que un más estrecho, aunque aumente el tamaño de la imagen, ya que siempre se puede volver a convertir a un formato más restrictivo si es necesario. Sin embargo, después de que se pierdan los datos, no se pueden recuperar.

## <a name="continued-reading"></a>Lectura continua

Para obtener más información sobre cómo crear un códec habilitado para WIC, consulte [implementación de IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Vista**
</dt> <dt>

[Implementar IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Implementación de IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
