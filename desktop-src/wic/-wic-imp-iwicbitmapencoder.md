---
description: Implementación de IWICBitmapEncoder
ms.assetid: b671e941-ded6-4bde-bc4d-461f13feade0
title: Implementación de IWICBitmapEncoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590dffcf762d22155a89a8143994d9a4d8bcab02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911953"
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

Esta interfaz es el homólogo de la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) y es el punto de partida para codificar un archivo de imagen. Al igual que **IWICBitmapDecoder** se usa para recuperar las propiedades de nivel de contenedor y los marcos individuales del contenedor de imágenes, [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) se usa para establecer las propiedades de nivel de contenedor y serializar los fotogramas de imagen individuales en el contenedor. Esta interfaz se implementa en la clase de codificador de nivel de contenedor.

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

Como se explicó en [implementación de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md), algunos formatos de imagen tienen miniaturas globales, contextos de color o metadatos, mientras que muchos formatos de imagen solo los proporcionan en cada fotograma. Por lo tanto, los métodos para establecer estos valores son opcionales en [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder), pero son necesarios en [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). Hablaremos sobre los métodos opcionales en **IWICBitmapEncoder** en la sección de **IWICBitmapFrameEncode**, donde se implementan con mayor frecuencia.

Si no admite miniaturas globales, devuelva WINCODEC \_ Err \_ CODECNOTHUMBNAIL desde el método SetThumbnail en [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder). Si no admite una paleta de nivel de contenedor, o si la imagen que está codificando no tiene un formato indexado, devuelva WINCODEC \_ Err \_ PALETTEUNAVAILABLE desde el método SetPalette. Para cualquier otro método no admitido, devuelve WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

### <a name="initialize"></a>Inicialización

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) es el primer método invocado en un [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) una vez que se ha creado una instancia. Se pasa una secuencia de imágenes al codificador y, opcionalmente, un llamador puede especificar una opción de caché. En el caso del descodificador, el flujo es de solo lectura, pero el flujo que se pasa a un codificador es una secuencia grabable, en la que el codificador serializará todos los datos y metadatos de la imagen. Las opciones de caché del codificador también son diferentes.

``` syntax
enum WICBitmapEncoderCacheOption
{
   WICBitmapEncoderCacheInMemory,
   WICBitmapEncoderCacheTempFile,
   WICBitmapEncoderNoCache
}
```

La aplicación tiene la opción de solicitar al codificador que almacene en memoria caché los datos de la imagen, los almacene en memoria caché en un archivo temporal o que los escriba directamente en el archivo de disco sin almacenamiento en caché. Cuando se le pide almacenar en caché los datos en un archivo temporal, el codificador debe crear un archivo temporal en el disco y escribir directamente en ese archivo sin almacenar en caché en memoria. Cuando el autor de la llamada selecciona la opción sin caché, cada fotograma se debe confirmar en orden antes de que se pueda crear el fotograma siguiente.

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat) se implementa de la misma manera que el método [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) en la [implementación de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getencoderinfo"></a>GetEncoderInfo

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) devuelve un objeto [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) . Para obtener el objeto **IWICBitmapEncoderInfo** , solo tiene que pasar el GUID del codificador al método [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) en [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)y, a continuación, solicitar la interfaz **IWICBitmapEncoderInfo** en él.

Vea el ejemplo de [implementación de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) en [GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md).

### <a name="createnewframe"></a>CreateNewFrame

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) es el homólogo del codificador de [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) en [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder). Este método devuelve un objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) , que es el objeto que serializa realmente los datos de imagen para un marco específico dentro del contenedor.

Una de las ventajas de Windows Imaging Component (WIC) es que proporciona una capa de abstracción para aplicaciones que les permite trabajar con todos los formatos de imagen de la misma manera. Sin embargo, no todos los formatos de imagen son exactamente iguales. Algunos formatos de imagen tienen funcionalidades que otros no tienen. Para que las aplicaciones puedan aprovechar estas capacidades únicas, es necesario proporcionar una manera de que el códec las exponga. Este es el propósito de las opciones del codificador. Si el códec es compatible con las opciones del codificador, debe crear un objeto [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que exponga las opciones del codificador que admita y devolverlo en el parámetro *ppIEncoderOptions* de este método. A continuación, el autor de la llamada puede usar este objeto IPropertyBag2 para determinar qué opciones del codificador admite el códec. Si el llamador desea especificar valores para cualquiera de las opciones admitidas del codificador, asignará el valor a la propiedad correspondiente en el objeto IPropertyBag2 y lo pasará al objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) recién creado en el método Initialize.

Para crear una instancia de un objeto [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , primero debe crear un struct PROPBAG2 para especificar cada opción de codificador que admita su codificador y su tipo de datos para cada propiedad. A continuación, debe implementar un objeto IPropertyBag2 que aplique los intervalos de valores para cada propiedad en la escritura y reconcilie los valores en conflicto o superpuestos. En el caso de los conjuntos simples de opciones de codificador no conflictivas, puede invocar el método [**CreateEncoderPropertyBag**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) , que creará un objeto IPropertyBag2 simple mediante las propiedades que especifique en el struct PROPBAG2. Todavía debe aplicar los intervalos de valores. En el caso de las opciones más avanzadas del codificador, o si necesita conciliar los valores en conflicto, debe escribir su propia implementación de IPropertyBag2.


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



WIC proporciona un pequeño conjunto de opciones de codificador canónicos que usan algunos de los formatos de imagen comunes. Todas las opciones canónicas del codificador son opcionales y los códecs no son necesarios para admitir ninguno de ellos. La razón por la que se proporcionan como opciones canónicas es que muchas aplicaciones exponen la interfaz de usuario para que los usuarios especifiquen estas opciones al guardar un archivo de imagen en un formato que los admita. Proporcionar una manera canónica de especificar estas opciones facilita a las aplicaciones la comunicación con los codificadores de una manera coherente. En la tabla siguiente se enumeran las opciones de codificador canónicas.



| Opción de codificador     | VARTYPE  | Intervalo de valores               |
|--------------------|----------|---------------------------|
| Lossless           | VT \_ bool | Verdadero/Falso                |
| ImageQuality       | VT \_ R4   | 0.0-1.0                   |
| CompressionQuality | VT \_ R4   | 0.0-1.0                   |
| BitmapTransform    | VT \_ UI1  | WICBitmapTransformOptions |



 

Si el códec admite la codificación sin pérdida, debe exponer la opción de codificador sin pérdida como una manera de que las aplicaciones soliciten que una imagen se codifique sin pérdida. Si un autor de llamada establece esta propiedad en true, debe omitir la opción ImageQuality y codificar la imagen sin pérdida.

La opción ImageQuality permite a una aplicación especificar el grado de fidelidad con el que codificar la imagen. Esta opción permite a un usuario establecer un equilibrio entre la calidad de la imagen y el tamaño del archivo o la velocidad. JPEG es un ejemplo de un formato de imagen que admite este equilibrio. Un valor de 0,0 indica que la fidelidad es de baja importancia y el codificador debe usar su algoritmo más perdido. Un valor de 1,0 indica que la fidelidad es la más importante y el codificador debe conservar la mayor fidelidad posible. (Dependiendo del códec, esto puede ser sinónimo de la opción Lossless. Sin embargo, si el códec admite la codificación sin pérdida y la opción Lossless está establecida en true, se debe pasar por alto la opción ImageQuality).

La opción CompressionQuality permite a una aplicación especificar la eficacia de la compresión que se va a usar al codificar la imagen. Un algoritmo muy eficaz puede generar un archivo de imagen más pequeño con la misma calidad que un algoritmo de compresión menos eficaz, pero puede tardar más tiempo en codificarse. Esta opción permite que un usuario especifique un equilibrio entre el tamaño del archivo y la velocidad de la codificación, a la vez que conserva el mismo nivel de calidad. TIFF es un ejemplo de un formato de imagen que admite este equilibrio. (Tenga en cuenta que un formato como JPEG admite distintos niveles de compresión, pero una mayor tasa de compresión resulta en una calidad de imagen inferior. Por lo tanto, un formato de imagen JPEG expondría la opción ImageQuality en lugar de la opción CompressionQuality). Un valor de 0,0 para esta opción indica que debe comprimir la imagen lo más rápidamente posible, sin reducir la fidelidad, a costa de un tamaño de archivo mayor. Un valor de 1,0 indica que debe crear el tamaño de archivo más pequeño posible (en el mismo nivel de calidad), independientemente del tiempo que pueda tardar en codificarlo. Un códec puede admitir tanto la opción ImageQuality como la opción CompressionQuality, donde la opción ImageQuality especifica el grado de pérdida aceptable y la opción CompressionQuality ofrece un equilibrio entre el tamaño y la velocidad en el nivel de calidad especificado.

La opción BitmapTransform proporciona una manera para que el llamador especifique un ángulo de giro o una orientación horizontal vertical u horizontal al codificar. La enumeración WICBitmapTransformOptions que se usa para especificar la transformación solicitada es la misma enumeración usada al solicitar una transformación durante la descodificación a través de la interfaz IWICBitmapSourceTransform.

Tenga en cuenta que los codificadores no se limitan a las opciones de codificador canónicos. El propósito de las opciones del codificador es permitir que los codificadores expongan sus capacidades y no hay ningún límite en cuanto a los tipos de funcionalidades que puede exponer. Asegúrese de que las opciones del codificador están bien documentadas. Aunque una aplicación puede usar el contenedor de propiedades que se devuelve de este método para detectar los nombres, tipos y rangos de valores de las opciones admitidas, la única forma de averiguar su significado o de exponerlos en la interfaz de usuario es desde la documentación.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) es el método al que se llama después de que todos los datos y metadatos de la imagen se hayan serializado en la secuencia. Debe utilizar este método para serializar los datos de la imagen de vista previa en el flujo y cualquier miniatura global, metadatos, paleta u otros elementos, si procede. Este método no debe cerrar el flujo de archivo, porque se espera que la aplicación que abrió la secuencia lo cierre.

La sección sobre el método IWICBitmapFrameEncode: commit tiene detalles sobre cómo el IWICBitmapEncoderCacheOptions afecta al comportamiento de este método.

### <a name="setpreview"></a>SetPreview

[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) se usa para crear una vista previa de la imagen. Aunque no es estrictamente necesario que todas las imágenes tengan una vista previa, es muy recomendable. Las cámaras digitales y los escáneres modernos generan imágenes de alta resolución, que suelen ser muy grandes y, por consiguiente, tardan mucho tiempo en descodificarse. Las imágenes de la próxima generación de cámaras serán incluso mayores. Es una buena idea proporcionar una versión más pequeña y de menor resolución de una imagen, normalmente en formato JPEG, que se puede descodificar rápidamente y mostrar "al instante" cuando un usuario lo solicita. Una aplicación puede solicitar una vista previa antes de solicitar la descodificación de la imagen real para proporcionar una mejor experiencia a los usuarios y mostrarles una representación de tamaño de pantalla de la imagen mientras theyare esperando descodificar la imagen real. Aunque los códecs deben proporcionar versiones preliminares, los códecs que no son compatibles con [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) deben hacerlo.

Si proporciona una vista previa JPEG, no tiene que escribir un codificador JPEG para codificarla. Debe delegar al codificador JPEG que se suministra con la plataforma WIC para codificar vistas previas y vistas en miniatura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaces del codificador](-wic-encoderinterfaces.md)
</dt> <dt>

[Implementación de IWICBitmapCodecProgressNotification (encoder)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
