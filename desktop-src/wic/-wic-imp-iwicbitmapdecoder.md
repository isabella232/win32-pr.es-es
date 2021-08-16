---
description: Implementación de IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementación de IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0088b756a7a30134224e32fa67ee891f2c48339f9af70447cb760915ad420619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711152"
---
# <a name="implementing-iwicbitmapdecoder"></a>Implementación de IWICBitmapDecoder

## <a name="iwicbitmapdecoder"></a>IWICBitmapDecoder

Cuando una aplicación solicita un descodificador, el primer punto de interacción con el códec es a través de la [**interfaz IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) Se trata de la interfaz de nivel de contenedor que proporciona acceso a las propiedades de nivel superior del contenedor y, lo que es más importante, a los marcos que contiene. Esta es la interfaz principal de la clase descodificador de nivel de contenedor.

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

Algunos formatos de imagen tienen miniaturas globales, contextos de color o metadatos, mientras que muchos formatos de imagen solo los proporcionan por fotograma. Los métodos para acceder a estos elementos son opcionales en [**IWICBitmapDecoder,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)pero son necesarios en [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Del mismo modo, algunos códecs no usan formatos de píxel indexados, por lo que no es necesario implementar los [métodos CopyPalette](-wic-imp-iwicbitmapframedecode.md) en ninguna de las interfaces. Para obtener más información sobre los métodos **opcionales de IWICBitmapDecoder,** vea [Implementing IWICBitmapFrameDecode ( Implementación de IWICBitmapFrameDecode),](-wic-imp-iwicbitmapframedecode.md)donde se implementan más comúnmente.

### <a name="querycapability"></a>QueryCapability

[**QueryCapability es**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) el método que se usa para el arbitraje de códecs. (Vea [Discovery and Arbitration en](-wic-howwicworks.md) el tema How The Windows Imaging Component [Works](-wic-howwicworks.md) ). Si dos códecs son capaces de decodificar el mismo formato de imagen, o si se produce una colisión de patrones en la que dos códecs usan el mismo patrón de identificación, este método le permite seleccionar el códec que mejor puede controlar cualquier imagen específica.

Al invocar este método, Windows Imaging Component (WIC) le pasa la secuencia real que contiene la imagen. Debe comprobar si puede descodificar cada fotograma dentro de la imagen y enumerar a través de los bloques de metadatos para declarar con precisión qué funcionalidades tiene este descodificador con respecto a la secuencia de archivos específica que se le pasa. Esto es importante para todos los descodificadores, pero especialmente importante para los formatos de imagen basados en contenedores Tagged Image File Format (TIFF). El proceso de detección funciona haciendo coincidir los patrones asociados con los descodificadores del registro con los patrones del archivo de imagen real. Declarar el patrón de identificación en el registro garantiza que el descodificador siempre se detectará para las imágenes en formato de imagen. Sin embargo, el descodificador todavía podría detectarse para imágenes en otros formatos. Por ejemplo, todos los contenedores TIFF incluyen el patrón TIFF, que es un patrón de identificación válido para el formato de imagen TIFF. Esto significa que, durante la detección, se encontrarán al menos dos patrones de identificación en los archivos de imagen para cualquier formato de imagen basado en un contenedor de estilo TIFF. Uno será el patrón TIFF y el otro será el patrón de formato de imagen real. Aunque es menos probable, también podría haber colisiones de patrones entre otros formatos de imagen no relacionados. Este es el motivo por el que la detección y el arbitraje son un proceso en dos fases. Compruebe siempre que el flujo de imagen pasado a [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) es realmente una instancia válida de su propio formato de imagen. Además, si el códec descodifica un formato de imagen para el que no es propietario de la especificación, la implementación de **QueryCapability** debe comprobar la presencia de cualquier característica que pueda ser válida en la especificación de formato de imagen que el códec no implementa. Esto garantizará que los usuarios no experimenten errores de decodificación innecesarios ni obtengan resultados inesperados con el códec.

Antes de realizar cualquier operación en la imagen, debe guardar la posición actual de la secuencia para poder restaurarla a su posición original antes de volver del método . La [**enumeración WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que especifica las funcionalidades se define de la siguiente manera:

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

Debe declarar **WICBitmapDecoderCapabilitySameEncoder** solo si el codificador fue el que codifica la imagen. Después de comprobar si puede descodificar cada fotograma del contenedor, declare **WICBitmapDecoderCapabilityCanDecodeSomeImages** si puede descodificar algunos fotogramas, pero no todos, **WICBitmapDecoderCapabilityCanDecodeAllImages** si puede descodificar todos los fotogramas o ninguno si no puede descodificar ninguno de ellos. (Estas dos enumeraciones son mutuamente excluyentes; si devuelve **WICBitmapDecoderCapabilityCanDecodeAllImages,** se omitirá **WICBitmapDecoderCapabilityCanDecodeSomeImages).** Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** después de comprobar que puede enumerar a través de los bloques de metadatos del contenedor de imágenes. No tiene que buscar una miniatura en cada fotograma. Si hay una miniatura global y se puede descodificar, puede declarar **WICBitmapDecoderCapabilityCanDecodeThumbnail**. Si no hay ninguna miniatura global, intente descodificar la miniatura del fotograma 0. Si no hay ninguna miniatura en ninguno de estos lugares, no declare esta funcionalidad.

Después de determinar las funcionalidades del descodificador con respecto al flujo de imagen pasado a este método, realice una operación OR con [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que haya comprobado que este descodificador puede realizar en esta imagen y devuelva el resultado. Recuerde restaurar la secuencia a su posición original antes de volver.

### <a name="initialize"></a>Inicialización

[**Una**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) aplicación invoca initialize después de que se haya seleccionado un descodificador para descodificar una imagen específica. El flujo de imagen se pasa al descodificador y un autor de la llamada puede especificar opcionalmente la opción de caché [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) para tratar con los metadatos del archivo.

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

Algunas aplicaciones usan metadatos más que otras. La mayoría de las aplicaciones no necesitan acceder a todos los metadatos de un archivo de imagen y solicitarán metadatos específicos cuando lo necesiten. Otras aplicaciones prefieren almacenar en caché todos los metadatos por adelantado que mantener abierta la secuencia de archivos y realizar E/S de disco cada vez que necesiten acceder a los metadatos. Si el autor de la llamada no especifica una opción de caché de metadatos, el comportamiento predeterminado del almacenamiento en caché debe ser la caché a petición. Esto significa que no se debe cargar ningún metadato en la memoria hasta que la aplicación realiza una solicitud específica para los metadatos. Si la aplicación especifica **WICDecodeMetadataCacheOnLoad,** los metadatos deben cargarse inmediatamente en la memoria y almacenarse en caché. Cuando los metadatos se almacenan en caché durante la carga, la secuencia de archivos se puede liberar después de que los metadatos se hayan almacenado en caché.

### <a name="getcontainerformat"></a>GetContainerFormat

Para implementar [**GetContainerFormat,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)solo tiene que devolver el GUID del formato de imagen de la imagen para la que se crea una instancia del descodificador. Este método también se implementa en [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) e [**IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)

### <a name="getdecoderinfo"></a>GetDecoderInfo

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) devuelve un [**objeto IWICBitmapDecoderInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) Para obtener el objeto **IWICBitmapDecoderInfo,** simplemente pase el GUID del descodificador al [**método CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) en [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)y, a continuación, solicite la interfaz **IWICBitmapDecoderInfo** en él, como se muestra en el ejemplo siguiente.


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a>GetFrameCount

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) simplemente devuelve el número de fotogramas del contenedor. Algunos formatos de contenedor admiten varios fotogramas y otros solo admiten un fotograma por contenedor.

### <a name="getframe"></a>GetFrame

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) es un método importante en la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) porque el marco contiene los bits de imagen reales y el objeto descodificador de marco devuelto por este método es el objeto que realiza la descodificación real de la imagen solicitada. Ese es el otro objeto que debe implementar al escribir un descodificador. Para obtener más información sobre los descodificadores de marco, [vea Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).

### <a name="getpreview"></a>GetPreview

[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) devuelve una vista previa de la imagen. Para obtener una explicación detallada de las versiones preliminares, vea el método [Implementing IWICBitmapEncoder (Implementación de IWICBitmapEncoder)](-wic-imp-iwicbitmapencoder.md) en la interfaz [Implementing IWICBitmapEncoder (Implementación de IWICBitmapEncoder).](-wic-imp-iwicbitmapencoder.md)

Si el formato de imagen contiene una vista previa JPEG incrustada, se recomienda encarecidamente que, en lugar de escribir un descodificador JPEG para descodificarlo, delegue en el descodificador JPEG que se incluye con la plataforma WIC para descodificar vistas previas y miniaturas. Para ello, busque el principio de los datos de la imagen de vista previa en la secuencia e invoque el [**método CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) en [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaces de descodificador](-wic-decoderinterfaces.md)
</dt> <dt>

[Implementación de IWICBitmapCodecProgressNotification (descodificador)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



