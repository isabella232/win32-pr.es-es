---
description: Implementar IWICBitmapFrameEncode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Implementar IWICBitmapFrameEncode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278190"
---
# <a name="implementing-iwicbitmapframeencode"></a>Implementar IWICBitmapFrameEncode

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) es el homólogo del codificador de la interfaz [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) . Puede implementar esta interfaz en la clase de codificación de nivel de marco, que es la clase que realiza la codificación real de los bits de imagen para cada fotograma.


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [Inicialización](#initialize)
-   [SetSize y SetResolution](#setsize-and-setresolution)
-   [SetPixelFormat](#setpixelformat)
-   [SetColorContexts](#setcolorcontexts)
-   [GetMetadataQueryWriter](#getmetadataquerywriter)
-   [SetThumbnail](#setthumbnail)
-   [WritePixels](#writepixels)
-   [WriteSource](#writesource)
-   [Confirmar](#commit)
-   [SetPalette](#setpalette)

### <a name="initialize"></a>Inicialización

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) es el primer método invocado en un objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) después del que se ha creado una instancia. Este método tiene un parámetro, que se puede establecer en **null**. Este parámetro representa las opciones del codificador y es la misma instancia de [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que se creó en el método [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) en el descodificador de nivel de contenedor y se devuelve al llamador en el parámetro pIEncoderOptions de ese método. En ese momento, ha rellenado el struct IPropertyBag2 con propiedades que representan las opciones de codificación que admite el codificador de nivel de marco. Ahora, el autor de la llamada ha proporcionado valores para esas propiedades para indicar determinados parámetros de opción de codificación y está pasando el mismo objeto a usted para inicializar el objeto **IWICBitmapFrameEncode** . Debe aplicar las opciones especificadas al codificar los bits de la imagen.

### <a name="setsize-and-setresolution"></a>SetSize y SetResolution

[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) y [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) se explican por sí solos. El autor de la llamada utiliza estos métodos para especificar el tamaño y la resolución de la imagen codificada.

### <a name="setpixelformat"></a>SetPixelFormat

[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) se usa para solicitar un formato de píxel en el que codificar la imagen. Si el formato de píxel solicitado no es compatible, debe devolver el GUID del formato de píxel más cercano que se admite en *pPixelFormat*, que es un parámetro in/out.

### <a name="setcolorcontexts"></a>SetColorContexts

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) se usa para especificar uno o más contextos de color válidos (también conocidos como perfiles de color) para esta imagen. Es importante especificar los contextos de color, de modo que una aplicación que descodifica la imagen más tarde puede convertir el perfil de color de origen en el perfil de destino del dispositivo que se usa para mostrar o imprimir la imagen. Sin un perfil de color, no es posible obtener colores coherentes en distintos dispositivos. Esto puede resultar frustrante para los usuarios finales cuando sus fotografías tienen un aspecto diferente en diferentes monitores y no pueden hacer que las copias coincidan con lo que ven en la pantalla.

### <a name="getmetadataquerywriter"></a>GetMetadataQueryWriter

[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) devuelve un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) que una aplicación puede usar para insertar o editar propiedades de metadatos específicas en un bloque de metadatos en el marco de imagen.

Puede crear instancias de un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) desde [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) de varias maneras. Puede crearlo desde el [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), de la misma manera que [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) se creó a partir de un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) en el método [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) de la interfaz [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



También se puede crear a partir de un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)existente, como el obtenido con el método anterior.


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



El parámetro *pguidVendor* permite especificar un proveedor determinado para que lo use el escritor de consultas al crear instancias de un escritor de metadatos. Por ejemplo, si proporciona sus propios escritores de metadatos, puede especificar su propio GUID de proveedor. Puede pasar **null** a este parámetro si no tiene ninguna preferencia.

### <a name="setthumbnail"></a>SetThumbnail

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) se usa para proporcionar una miniatura. Todas las imágenes deben proporcionar una miniatura, ya sea globalmente, en cada fotograma o en ambas. Los métodos **GetThumbnail** y **SetThumbnail** son opcionales en el nivel de contenedor pero, si un códec devuelve WINCODEC \_ Err \_ CODECNOTHUMBNAIL del método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) , Windows Imaging Component (WIC) invocará el método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) para el marco 0. Si no se encuentra ninguna miniatura en ningún lugar, WIC debe descodificar la imagen completa y escalarla a un tamaño de miniatura, lo que podría suponer una gran penalización del rendimiento para imágenes más grandes.

La miniatura debe tener un tamaño y una resolución que permita descodificar y mostrar rápidamente. Por este motivo, las miniaturas suelen ser imágenes JPEG. Tenga en cuenta que, si usa JPEG para las miniaturas, no tiene que escribir un codificador JPEG para codificarlos o un descodificador JPEG para descodificarlos. Siempre debe delegar en el códec JPEG que se suministra con la plataforma WIC para codificar y descodificar las miniaturas.

### <a name="writepixels"></a>WritePixels

[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) es el método que se usa para pasar líneas de análisis de un mapa de bits en memoria para la codificación. Se llamará al método varias veces hasta que se hayan pasado todas las líneas de recorrido. El parámetro *lineCount* indica el número de líneas de análisis que se van a escribir en esta llamada. El parámetro *cbStride* indica el número de bytes por línea de examen. *cbBufferSize* indica el tamaño del búfer pasado en el parámetro pbPixels, que contiene los bits de imagen reales que se van a codificar. Si el alto combinado de las líneas de análisis de las llamadas acumulativas es mayor que el alto especificado en el método [**setSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) , se devuelve WINCODEC \_ Err \_ TOOMANYSCANLINES.

Cuando [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) es **WICBitmapEncoderCacheInMemory**, las líneas de análisis deben almacenarse en la memoria caché hasta que se hayan pasado todas las líneas de examen. Si la opción de caché del codificador es **WICBitmapEncoderCacheTempFile**, las líneas de análisis deben almacenarse en caché en un archivo temporal, que se crea al inicializar el objeto. En cualquiera de estos casos, la imagen no se debe codificar hasta que el autor de la llamada llame a [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit). En el caso de que la opción de caché sea **WICBitmapEncoderNoCache**, el codificador debe codificar las líneas de análisis a medida que se reciben, si es posible. (En algunos formatos, esto no es posible y las líneas de recorrido deben almacenarse en caché hasta que se llame a commit).

La mayoría de los códecs sin formato no implementarán [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), ya que no admiten la modificación de los bits de imagen en el archivo sin formato. Sin embargo, los códecs sin formato deben implementar **WritePixels**, porque cuando se agregan metadatos, puede aumentar el tamaño del archivo, lo que requiere que el archivo se vuelva a escribir en el disco. En ese caso, es necesario poder copiar los bits de imagen existentes, que es lo que hace el método **WritePixels** .

### <a name="writesource"></a>WriteSource

[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) se usa para codificar un objeto [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) . El primer parámetro es un puntero a un objeto **IWICBitmapSource** . El segundo parámetro es un WICRect que especifica la región de interés que se va a codificar. Se puede llamar a este método varias veces consecutivas, siempre que el ancho de cada rectángulo tenga el mismo ancho que la imagen final que se va a codificar. Si el ancho del rectángulo pasado en el parámetro PRC es diferente del ancho especificado en el método setSize, devuelva WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS. Si el alto combinado de las líneas de análisis de las llamadas acumulativas es mayor que el alto especificado en el método setSize, se devuelve WINCODEC \_ Err \_ TOOMANYSCANLINES.

Las opciones de caché funcionan de la misma manera con este método que con el método [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) descrito anteriormente.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) es el método que serializa los bits de imagen codificados en la secuencia de archivos y recorre en iteración todos los escritores de metadatos para el marco que los solicita para serializar los metadatos en la secuencia. En el caso de que la opción de caché del codificador sea WICBitmapEncoderCacheInMemory o WICBitmapEncoderCacheTempFile, este método también es responsable de codificar la imagen y, cuando la opción de caché es WICBitmapEncoderCacheTempFile, el método **commit** también debe eliminar el archivo temporal que se usa para almacenar en caché los datos de la imagen antes de la codificación.

Este método siempre se invoca después de que se hayan pasado todas las líneas de recorrido o rectángulos que componen la imagen mediante el método [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) o [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) . El tamaño del rectángulo final que se compone a través de las llamadas acumuladas a WritePixels o WriteSource debe tener el mismo tamaño que el que se especificó en el método setSize. Si el tamaño no coincide con el tamaño esperado, este método debe devolver WINCODECERROR \_ UNEXPECTEDSIZE.

Para recorrer en iteración los escritores de metadatos e indicar a cada escritor de metadatos que serialice sus metadatos, vaya a la secuencia, invoque GetWriterByIndex para recorrer en iteración los escritores de cada bloque e invoque IWICPersistStream. Save en cada escritor de metadatos.


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a>SetPalette

Solo los códecs con formatos indexados deben implementar el método [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) . Si una imagen usa un formato indizado, use este método para especificar la paleta de colores utilizada en la imagen. Si el códec no tiene un formato indizado, devuelva WINCODEC \_ Err \_ PALETTEUNAVAILABLE desde este método.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Implementación de IWICBitmapCodecProgressNotification (encoder)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Implementación de IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
