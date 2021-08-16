---
description: Implementación de IWICBitmapEncoder
ms.assetid: b671e941-ded6-4bde-bc4d-461f13feade0
title: Implementación de IWICBitmapEncoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d02105470f837dba0689b665473c01c42f6cd6497a85424ea6eea3371696f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088017"
---
# <a name="implementing-iwicbitmapencoder"></a>Implementación de IWICBitmapEncoder

-   [IWICBitmapEncoder](#implementing-iwicbitmapencoder)
    -   [Inicialización](#initialize)
    -   [GetContainerFormat](#getcontainerformat)
    -   [GetEncoderInfo](#getencoderinfo)
    -   [CreateNewFrame](#createnewframe)
    -   [Confirmar](#commit)
    -   [SetPreview](#setpreview)
-   [Temas relacionados](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

-   [Inicialización](#initialize)
-   [GetContainerFormat](#getcontainerformat)
-   [GetEncoderInfo](#getencoderinfo)
-   [CreateNewFrame](#createnewframe)
-   [Confirmar](#commit)
-   [SetPreview](#setpreview)

Esta interfaz es la equivalente a la [**interfaz IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) y es el punto de partida para codificar un archivo de imagen. Del mismo modo que se usa **IWICBitmapDecoder** para recuperar propiedades de nivel de contenedor y fotogramas individuales del contenedor de imágenes, [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) se usa para establecer propiedades de nivel de contenedor y serializar fotogramas de imagen individuales en el contenedor. Esta interfaz se implementa en la clase de codificador de nivel de contenedor.

``` syntax
interface IWICBitmapEncoder : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IStream *pIStream,
              WICBitmapEncoderCacheOption cacheOption );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetEncoderInfo ( IWICBitmapEncoderInfo **pIEncoderInfo );
   HRESULT CreateNewFrame ( IWICBitmapFrameEncode **ppIFrameEncode,
              IPropertyBag2 **ppIEncoderOptions );
   HRESULT Commit ( void );

   // Optional methods
   HRESULT SetPreview ( IWICBitmapSource *pIPreview );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT SetColorContexts ( UINT cCount,
              IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
              **ppIMetadataQueryWriter );
   HRESULT SetPalette ( IWICPalette *pIPalette);
};
```

Como se describe en Implementación de [IWICBitmapDecoder,](-wic-imp-iwicbitmapdecoder.md)algunos formatos de imagen tienen miniaturas globales, contextos de color o metadatos, mientras que muchos formatos de imagen solo los proporcionan por fotograma. Por lo tanto, los métodos para establecer estos son opcionales en [**IWICBitmapEncoder,**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)pero son necesarios en [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). Trataremos los métodos que son opcionales en **IWICBitmapEncoder** en la sección **sobre IWICBitmapFrameEncode,** donde se implementan normalmente.

Si no admite miniaturas globales, devuelva EL CÓDEC DE ERROR DE WINCODECNOTHUMBNAIL desde el \_ \_ método SetThumbnail en [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder). Si no admite una paleta de nivel de contenedor o si la imagen que está codificando no tiene un formato indexado, devuelva WINCODEC ERR PALETTEUNAVAILABLE desde el método \_ \_ SetPalette. Para cualquier otro método no admitido, devuelva WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION.

### <a name="initialize"></a>Inicialización

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) es el primer método invocado en [**un IWICBitmapEncoder después**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) de crear una instancia. Se pasa una secuencia de imagen al codificador y, opcionalmente, un autor de la llamada puede especificar una opción de caché. En el caso del descodificador, la secuencia es de solo lectura, pero la secuencia que se pasa a un codificador es una secuencia que se puede escribir, en la que el codificador serializará todos los datos y metadatos de la imagen. Las opciones de caché en el codificador también son diferentes.

``` syntax
enum WICBitmapEncoderCacheOption
{
   WICBitmapEncoderCacheInMemory,
   WICBitmapEncoderCacheTempFile,
   WICBitmapEncoderNoCache
}
```

La aplicación tiene la opción de solicitar al codificador que almacena en caché los datos de imagen en memoria, almacenar en caché en un archivo temporal o escribirlo directamente en el archivo de disco sin almacenamiento en caché. Cuando se le pide que almacena en caché los datos en un archivo temporal, el codificador debe crear un archivo temporal en el disco y escribir directamente en ese archivo sin almacenar en caché en la memoria. Cuando el autor de la llamada selecciona la opción sin caché, cada fotograma debe estar confirmado en orden antes de que se pueda crear el fotograma siguiente.

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat se**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat) implementa de la misma manera que el [método GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) en [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getencoderinfo"></a>GetEncoderInfo

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) devuelve un [**objeto IWICBitmapEncoderInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) Para obtener el objeto **IWICBitmapEncoderInfo,** simplemente pase el GUID del codificador al [**método CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) en [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)y, a continuación, solicite la interfaz **IWICBitmapEncoderInfo** en él.

Vea el ejemplo de [Implementación de IWICBitmapDecoder en](-wic-imp-iwicbitmapdecoder.md) [GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md).

### <a name="createnewframe"></a>CreateNewFrame

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) es el homólogo del codificador [**de GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) en [**IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) Este método devuelve un [**objeto IWICBitmapFrameEncode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) que es el objeto que serializa realmente los datos de imagen de un marco específico dentro del contenedor.

Una de las ventajas de Windows Imaging Component (WIC) es que proporciona una capa de abstracción para las aplicaciones que les permite trabajar con todos los formatos de imagen de la misma manera. Sin embargo, no todos los formatos de imagen son exactamente iguales. Algunos formatos de imagen tienen funcionalidades que otros no tienen. Para que las aplicaciones puedan aprovechar esas funcionalidades únicas, es necesario proporcionar una manera de que el códec las exponga. Este es el propósito de las opciones del codificador. Si el códec admite cualquier opción de codificador, debe crear un objeto [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que exponga las opciones de codificador que admite y devolverlo en el parámetro *ppIEncoderOptions* de este método. A continuación, el autor de la llamada puede usar este objeto IPropertyBag2 para determinar qué opciones de codificador admite el códec. Si el autor de la llamada quiere especificar valores para cualquiera de las opciones de codificador admitidas, asignará el valor a la propiedad correspondiente en el objeto IPropertyBag2 y lo pasará al objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) recién creado en su método Initialize.

Para crear una instancia de un [objeto IPropertyBag2,](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) primero debe crear una estructura PROPBAG2 para especificar cada opción de codificador que admite el codificador y su tipo de datos para cada propiedad. A continuación, debe implementar un objeto IPropertyBag2 que aplique los intervalos de valores para cada propiedad en la escritura y concilia los valores en conflicto o superpuestos. Para conjuntos sencillos de opciones de codificador que no están en conflicto, puede invocar el método [**CreateEncoderPropertyBag,**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) que creará un objeto IPropertyBag2 simple mediante las propiedades que especifique en la estructura PROPBAG2. Todavía debe aplicar los intervalos de valores. Para obtener opciones de codificador más avanzadas, o si necesita conciliar valores en conflicto, debe escribir su propia implementación de IPropertyBag2.


```C++
UINT cuiPropertyCount = 0;
IPropertyBag2* pPropertyBag = NULL;
PROPBAG2* pPropBagOptions;
HRESULT hr;

// Insert code here to initialize piPropertyBag with the 
// supported options for your encoder, and to initialize 
// cuiPropertyCount to the number of encoder option properties
// you are exposing.
...

hr = pComponentFactory->CreateEncoderPropertyBag( 
   pPropBagOptions, cuiPropertyCount, &pPropertyBag);
```



WIC proporciona un pequeño conjunto de opciones de codificador canónico que usan algunos de los formatos de imagen comunes. Todas las opciones de codificador canónico son opcionales y los códecs no son necesarios para admitir ninguna de ellas. La razón por la que se proporcionan como opciones canónicas es porque muchas aplicaciones exponen la interfaz de usuario para que los usuarios especifiquen estas opciones al guardar un archivo de imagen en un formato que las admita. Proporcionar una manera canónica de especificar estas opciones facilita que las aplicaciones las comuniquen a los codificadores de forma coherente. Las opciones de codificador canónico se enumeran en la tabla siguiente.



| Opción de codificador     | VARTYPE  | Intervalo de valores               |
|--------------------|----------|---------------------------|
| Lossless           | VT \_ BOOL | Verdadero/Falso                |
| ImageQuality       | VT \_ R4   | 0.0-1.0                   |
| CompressionQuality | VT \_ R4   | 0.0-1.0                   |
| BitmapTransform    | VT \_ UI1  | WICBitmapTransformOptions |



 

Si el códec admite la codificación sin pérdida, debe exponer la opción Codificador sin pérdida como una manera de que las aplicaciones soliciten que una imagen se encodifice sin pérdida de datos. Si un autor de la llamada establece esta propiedad en True, debe omitir la opción ImageQuality y codificar la imagen sin pérdida de datos.

La opción ImageQuality permite a una aplicación especificar el grado de fidelidad con el que codificar la imagen. Esta opción permite a un usuario realizar un equilibrio entre la calidad de la imagen y la velocidad o el tamaño del archivo. JPEG es un ejemplo de un formato de imagen que admite este intercambio. Un valor de 0,0 indica que la fidelidad es de baja importancia y el codificador debe usar su algoritmo con mayor pérdida. Un valor de 1,0 indica que la fidelidad es la más importante y el codificador debe conservar la máxima fidelidad posible. (Dependiendo del códec, esto puede ser sinónimo de la opción Sin pérdida. Sin embargo, si el códec admite la codificación sin pérdida y la opción Sin pérdida se establece en True, se debe omitir la opción ImageQuality.

La opción CompressionQuality permite que una aplicación especifique la eficacia de la compresión que se usará al codificar la imagen. Un algoritmo muy eficaz puede generar un archivo de imagen más pequeño con la misma calidad que un algoritmo de compresión menos eficaz, pero puede tardar más tiempo en codificar. Esta opción permite a un usuario especificar un equilibrio entre el tamaño del archivo y la velocidad de codificación, a la vez que se conserva el mismo nivel de calidad. TIFF es un ejemplo de un formato de imagen que admite este intercambio. (Tenga en cuenta que un formato como JPEG admite diferentes niveles de compresión, pero una mayor tasa de compresión da como resultado una calidad de imagen inferior. Por lo tanto, un formato de imagen JPEG expondría la opción ImageQuality en lugar de la opción CompressionQuality). Un valor de 0,0 para esta opción indica que debe comprimir la imagen lo antes posible, sin reducir la fidelidad, a costa de un tamaño de archivo mayor. Un valor de 1,0 indica que debe crear el tamaño de archivo más pequeño posible (con el mismo nivel de calidad), independientemente del tiempo que se pueda tardar en codificarlo. Un códec puede admitir tanto la opción ImageQuality como la opción CompressionQuality, donde la opción ImageQuality especifica el grado aceptable de pérdida y la opción CompressionQuality ofrece un ajuste de tamaño y velocidad en el nivel de calidad especificado.

La opción BitmapTransform proporciona una manera de que el autor de la llamada especifique un ángulo de rotación o una orientación vertical u horizontal al codificar. La enumeración WICBitmapTransformOptions usada para especificar la transformación solicitada es la misma enumeración que se usa al solicitar una transformación durante la codificación a través de la interfaz IWICBitmapSourceTransform.

Tenga en cuenta que los codificadores no se limitan a las opciones de codificador canónico. El propósito de las opciones del codificador es permitir que los codificadores exponan sus funcionalidades, y no hay ningún límite para los tipos de funcionalidades que puede exponer. Asegúrese de que las opciones del codificador están bien documentadas. Aunque una aplicación puede usar el bolsa de propiedades que devuelve de este método para detectar los nombres, los tipos y los intervalos de valores de las opciones que admite, la única manera de averiguar sus significados o cómo exponerlos en la interfaz de usuario es en la documentación.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) es el método al que se llama después de que todos los datos y metadatos de la imagen se hayan serializado en la secuencia. Debe usar este método para serializar los datos de la imagen de vista previa en la secuencia y cualquier miniatura global, metadatos, paleta u otros elementos, si procede. Este método no debe cerrar la secuencia de archivos, porque se espera que la aplicación que abrió la secuencia la cierre.

La sección del método IWICBitmapFrameEncode:Commit contiene detalles sobre cómo IWICBitmapEncoderCacheOptions afecta al comportamiento de este método.

### <a name="setpreview"></a>SetPreview

[**SetPreview se**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) usa para crear una vista previa de la imagen. Aunque no es estrictamente necesario que todas las imágenes tengan una versión preliminar, se recomienda encarecidamente. Las cámaras digitales y los escáneres modernos generan imágenes de muy alta resolución, que tienden a ser muy grandes y, por tanto, se necesita un tiempo de procesamiento significativo para descodificar. Las imágenes de la próxima generación de cámaras serán incluso más grandes. Es una buena idea proporcionar una versión de menor resolución de una imagen, normalmente en formato JPEG, que se puede descodificar rápidamente y mostrarse "al instante" cuando un usuario la solicita. Una aplicación puede solicitar una versión preliminar antes de solicitar la descodificación de la imagen real para proporcionar una mejor experiencia a los usuarios y mostrarles una representación de tamaño de pantalla de la imagen mientras esperan a descodificar la imagen real. Aunque los códecs deben proporcionar vistas previas, los códecs que no admiten [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) deberían hacerlo definitivamente.

Si proporciona una versión preliminar JPEG, no tiene que escribir un codificador JPEG para codificarlo. Debe delegar en el codificador JPEG que se distribuye con la plataforma WIC para codificar vistas previas y miniaturas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaces de codificador](-wic-encoderinterfaces.md)
</dt> <dt>

[Implementación de IWICBitmapCodecProgressNotification (Codificador)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
