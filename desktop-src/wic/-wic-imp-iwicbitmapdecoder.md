---
description: Implementar IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementar IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082721"
---
# <a name="implementing-iwicbitmapdecoder"></a>Implementar IWICBitmapDecoder

## <a name="iwicbitmapdecoder"></a>IWICBitmapDecoder

Cuando una aplicación solicita un descodificador, el primer punto de interacción con el códec se realiza a través de la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) . Esta es la interfaz de nivel de contenedor que proporciona acceso a las propiedades de nivel superior del contenedor y, lo que es más importante, los fotogramas que contiene. Esta es la interfaz principal de la clase descodificador de nivel de contenedor.

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

Algunos formatos de imagen tienen miniaturas globales, contextos de color o metadatos, mientras que muchos formatos de imagen solo los proporcionan en cada fotograma. Los métodos para tener acceso a estos elementos son opcionales en [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), pero son necesarios en [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Del mismo modo, algunos códecs no usan formatos de píxeles indizados, por lo que no es necesario implementar los métodos [CopyPalette](-wic-imp-iwicbitmapframedecode.md) en ninguna de las interfaces. Para obtener más información sobre los métodos **IWICBitmapDecoder** opcionales, vea [implementar IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), donde se implementan con mayor frecuencia.

### <a name="querycapability"></a>QueryCapability

[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) es el método que se usa para el arbitraje del códec. (Consulte [detección y arbitraje](-wic-howwicworks.md) en el tema [Cómo funciona el componente de creación de imágenes de Windows](-wic-howwicworks.md) ). Si dos códecs pueden descodificar el mismo formato de imagen o si se produce una colisión de patrón en la que dos códecs usan el mismo patrón de identificación, este método le permite seleccionar el códec que puede controlar mejor cualquier imagen específica.

Al invocar este método, el componente de creación de imágenes de Windows (WIC) le pasa la secuencia real que contiene la imagen. Debe comprobar si puede descodificar cada fotograma de la imagen y enumerar los bloques de metadatos para declarar con precisión qué funcionalidades tiene este descodificador con respecto al flujo de archivo específico que se le ha pasado. Esto es importante para todos los descodificadores, pero especialmente importante para los formatos de imagen basados en contenedores Tagged Image File Format (TIFF). El proceso de detección funciona mediante patrones coincidentes asociados con los descodificadores en el registro con los patrones del archivo de imagen real. Declarar el patrón de identificación en el registro garantiza que el descodificador siempre se detectará para las imágenes en el formato de imagen. Sin embargo, el descodificador todavía podría detectarse para imágenes en otros formatos. Por ejemplo, todos los contenedores TIFF incluyen el patrón TIFF, que es un patrón de identificación válido para el formato de imagen TIFF. Esto significa que, durante la detección, se encontrarán al menos dos patrones de identificación en los archivos de imagen para cualquier formato de imagen que se base en un contenedor de estilo TIFF. Uno será el patrón TIFF y el otro será el patrón de formato de imagen real. Aunque es menos probable, también podría haber colisiones de patrón entre otros formatos de imagen no relacionados. Este es el motivo por el que la detección y el arbitraje son un proceso de dos fases. Compruebe siempre que el flujo de imagen pasado a [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) es realmente una instancia válida de su propio formato de imagen. Además, si el códec descodifica un formato de imagen para el que no posee la especificación, la implementación de **QueryCapability** debe comprobar la presencia de cualquier característica que pueda ser válida en la especificación de formato de imagen que el códec no implementa. Esto garantizará que los usuarios no experimenten errores de descodificación innecesarios u obtengan resultados inesperados con el códec.

Antes de realizar cualquier operación en la imagen, debe guardar la posición actual de la secuencia, por lo que puede restaurarla a su posición original antes de volver del método. La enumeración [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que especifica las capacidades se define de la siguiente manera:

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

Solo debe declarar **WICBitmapDecoderCapabilitySameEncoder** si su codificador era el que codifica la imagen. Después de comprobar si puede descodificar cada fotograma del contenedor, declare **WICBitmapDecoderCapabilityCanDecodeSomeImages** si puede descodificar algunos, pero no todos, **WICBitmapDecoderCapabilityCanDecodeAllImages** si puede descodificar todos los fotogramas, o ninguno si no puede descodificar ninguno de ellos. (Estas dos enumeraciones son mutuamente excluyentes; si devuelve **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** se omitirá). Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** después de comprobar que puede enumerar los bloques de metadatos en el contenedor de imágenes. No tiene que buscar una miniatura en cada fotograma. Si hay una miniatura global y puede descodificarla, puede declarar **WICBitmapDecoderCapabilityCanDecodeThumbnail**. Si no hay ninguna miniatura global, intente descodificar la miniatura del fotograma 0. Si no hay ninguna miniatura en ninguno de estos lugares, no declare esta funcionalidad.

Después de determinar las capacidades del descodificador con respecto al flujo de imagen pasado a este método, realice una operación OR con el [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que ha comprobado que este descodificador puede realizar en esta imagen y devuelva el resultado. Recuerde restaurar el flujo a su posición original antes de volver.

### <a name="initialize"></a>Inicialización

Una aplicación invoca la [**inicialización**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) una vez que se ha seleccionado un descodificador para descodificar una imagen específica. La secuencia de imágenes se pasa al descodificador y un llamador puede especificar opcionalmente la opción de caché [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) para tratar con los metadatos del archivo.

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

Algunas aplicaciones usan metadatos más que otras. La mayoría de las aplicaciones no necesitan tener acceso a todos los metadatos de un archivo de imagen y solicitarán metadatos específicos a medida que lo necesiten. En lugar de ello, otras aplicaciones almacenarán en caché todos los metadatos antes de que mantener la secuencia de archivos abierta y realizar la e/s de disco cada vez que necesiten tener acceso a los metadatos. Si el autor de la llamada no especifica una opción de caché de metadatos, el comportamiento de almacenamiento en caché predeterminado debe ser caché a petición. Esto significa que no se deben cargar metadatos en memoria hasta que la aplicación realice una solicitud específica para esos metadatos. Si la aplicación especifica **WICDecodeMetadataCacheOnLoad**, los metadatos se deben cargar en memoria de inmediato y almacenar en caché. Cuando los metadatos se almacenan en la memoria caché durante la carga, la secuencia de archivos se puede liberar una vez que los metadatos se han almacenado en caché.

### <a name="getcontainerformat"></a>GetContainerFormat

Para implementar [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), solo tiene que devolver el GUID del formato de imagen de la imagen para la que se crea una instancia del descodificador. Este método también se implementa en [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) y [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).

### <a name="getdecoderinfo"></a>GetDecoderInfo

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) devuelve un objeto [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) . Para obtener el objeto **IWICBitmapDecoderInfo** , solo tiene que pasar el GUID del descodificador al método [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) en [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)y, a continuación, solicitar la interfaz **IWICBitmapDecoderInfo** en él, tal como se muestra en el ejemplo siguiente.


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a>GetFrameCount

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) simplemente devuelve el número de marcos del contenedor. Algunos formatos de contenedor admiten varios marcos y otros solo admiten un marco por contenedor.

### <a name="getframe"></a>GetFrame

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) es un método importante en la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) porque el marco contiene los bits de imagen reales y el objeto de descodificador de marco devuelto por este método es el objeto que realiza la descodificación real de la imagen solicitada. Es el otro objeto que debe implementar al escribir un descodificador. Para obtener más información sobre los descodificadores de fotogramas, vea [implementar IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).

### <a name="getpreview"></a>GetPreview

[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) devuelve una vista previa de la imagen. Para obtener una explicación detallada de las versiones preliminares, vea el método de [implementación de IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) en la interfaz de [implementación de IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) .

Si el formato de imagen contiene una vista previa de JPEG incrustada, se recomienda encarecidamente que, en lugar de escribir un descodificador JPEG, delegue en el descodificador JPEG que se suministra con la plataforma WIC para descodificar vistas previas y vistas en miniatura. Para ello, busque el principio de los datos de la imagen de vista previa en la secuencia e invoque el método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) en [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).


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

**Vista**
</dt> <dt>

[Interfaces del descodificador](-wic-decoderinterfaces.md)
</dt> <dt>

[Implementación de IWICBitmapCodecProgressNotification (descodificador)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



