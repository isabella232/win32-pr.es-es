---
description: Windows Imaging Component (WIC) se ha actualizado con las nuevas versiones de Windows. En este tema se proporciona una introducción rápida a estas nuevas características.
ms.assetid: 710B71CE-6FCC-46DA-A65C-6E4FC6A04275
title: Novedades de WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b8b3783ac2fd8ef6a971f785cec80f868a6b80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707360"
---
# <a name="whats-new-in-wic"></a>Novedades de WIC

Windows Imaging Component (WIC) se ha actualizado con las nuevas versiones de Windows. En este tema se proporciona una introducción rápida a estas nuevas características.

## <a name="whats-new-for-windows-10-version-1507"></a>Novedades de Windows 10, versión 1507

### <a name="access-to-low-level-jpeg-data-for-wic-decoding-and-encoding"></a>Acceso a datos JPEG de bajo nivel para la descodificación y codificación de WIC

A partir de Windows 10, versión 1507, WIC proporciona acceso a las estructuras de datos JPEG de bajo nivel, incluidas las tablas Huffman y de cuantificación. Para obtener más información, vea los temas siguientes:

-   Interfaz [**IWICJpegFrameDecode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframedecode)
-   Interfaz [**IWICJpegFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframeencode)

### <a name="jpeg-indexing"></a>Indexación JPEG

La indexación JPEG es una técnica que mejora significativamente el rendimiento del acceso aleatorio a pequeñas subregiones de una imagen JPEG grande, a costa del uso de memoria adicional. Cualquier llamador de WIC puede aprovechar la indexación JPEG.

La interfaz [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) se ha diseñado para aprovechar la indexación JPEG si está activada. Por ejemplo, la API de ID2D1ImageSource solo solicitará las secciones necesarias de la imagen en un escenario como pan y zoom para una imagen de gran resolución. Para obtener más información, vea los temas siguientes:

-   [**IWICJpegFrameDecode:: SetIndexing**](/windows/win32/api/Wincodec/nf-wincodec-iwicjpegframedecode-setindexing) (método)
-   Interfaz [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)

## <a name="whats-new-for-windows-81"></a>Novedades de Windows 8.1

### <a name="support-for-jpeg-ycbcr-images"></a>Compatibilidad con imágenes de JPEG YCbCr

A partir de Windows 8.1, WIC proporciona compatibilidad para descodificar, transformar y codificar datos de imagen JPEG Y'CbCr en su formato nativo. Esto permite a las aplicaciones reducir significativamente el tiempo de procesamiento y el consumo de memoria para ciertas operaciones de creación de imágenes al trabajar con JPEG codificados con Y'CbCr. Para obtener más información, vea los temas siguientes:

-   [](-wic-sample-d2d-viewer.md)[Efecto YCbCr](../direct2d/ycbcr-effect.md) de Direct2D
-   Interfaz [**IWICPlanarBitmapSourceTransform**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
-   Interfaz [**IWICPlanarBitmapFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode)

### <a name="support-for-block-compressed-formats-dds-files"></a>Compatibilidad con formatos comprimidos de bloques (archivos DDS)

A partir de Windows 8.1, WIC agrega un nuevo códec que admite imágenes de DDS codificadas en los siguientes formatos: DXGI \_ format \_ BC1 \_ UNORM, dxgi \_ format \_ BC2 \_ UNORM y dxgi \_ format \_ BC3 \_ UNORM. Se puede tener acceso a los datos comprimidos en bloque DDS en un formulario descodificado mediante interfaces WIC estándar o directamente mediante nuevas interfaces específicas de DDS. Para obtener más información, vea los temas siguientes:

-   Interfaz [**IWICDdsDecoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsdecoder)
-   Interfaz [**IWICDdsEncoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsencoder)

## <a name="whats-new-for-windows-8"></a>Novedades de Windows 8

En Windows 8, WIC se ha actualizado con varias características nuevas. La versión actualizada de WIC también está disponible en Windows 7 y Windows Server 2008 R2 a través de la [actualización de la plataforma para Windows 7](../direct3darticles/platform-update-for-windows-7.md), que está disponible a través de la [actualización de la plataforma para Windows 7](https://support.microsoft.com/kb/2670838).

### <a name="improved-direct2d-integration"></a>Integración mejorada de Direct2D

WIC en Windows 8 proporciona estas API para mejorar la integración de Direct2D con WIC:

-   [**IWICImageEncoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicimageencoder) : una nueva interfaz que puede codificar contenido de Direct2D [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) en [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md). Los métodos de esta interfaz toman un puntero a [**WICImageParameters**](/windows/win32/api/Wincodec/ns-wincodec-wicimageparameters), que son parámetros para controlar la codificación.
-   [**IWICImagingFactory2**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory2) : nuevo generador de WIC con el método [**CreateImageEncoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder) . Esta interfaz hereda del generador WIC original, [**IWICImagingFactory**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory), y se crea de la misma manera.

### <a name="changes-to-bmp-codec-alpha-support"></a>Cambios en la compatibilidad con el códec BMP Alpha

WIC en Windows 8 admite la carga de archivos de imagen [**BITMAPV5HEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) como imágenes con formato [WICPixelFormat32bppBGRA](-wic-codec-native-pixel-formats.md). Además, el codificador BMP es compatible con una nueva opción de codificador booleana "EnableV5Header32bppBGRA", que indica al codificador que escriba un **BITMAPV5HEADER** con los datos de imagen de 32bppBGRA.

Para obtener más información sobre los formatos BMP, consulte [información general sobre el formato BMP](bmp-format-overview.md).

### <a name="new-pixel-formats"></a>Nuevos formatos de píxeles

WIC en Windows 8 define estos nuevos formatos de píxel:

-   GUID \_ WICPixelFormat32bppRGB
-   GUID \_ WICPixelFormat64bppRGB
-   GUID \_ WICPixelFormat96bppRGBFloat
-   GUID \_ WICPixelFormat64bppPRGBAHalf

> [!Note]  
> El códec integrado TIFF devolverá los datos de WICPixelFormat96bppRGBFloat de GUID \_ . Los otros tres formatos no se usan en códecs integrados.

 

### <a name="restrictions-to-component-extensibility-in-appcontainer"></a>Restricciones a la extensibilidad de componentes en AppContainer

Cuando se ejecuta en un proceso AppContainer, que incluye todas las aplicaciones de la tienda Windows, WIC solo usará los componentes proporcionados por Windows, independientemente de si hay componentes adicionales instalados en el sistema. La aplicación que no se ejecuta en AppContainer no se ve afectada.

Las aplicaciones no necesitan realizar ningún cambio en el código para que se ejecuten en un AppContainger, pero los parámetros de la marca [**WICComponentEnumerateOptions**](/windows/win32/api/Wincodec/ne-wincodec-wiccomponentenumerateoptions) y del GUID del proveedor no tendrán ningún efecto. WIC no podrá cargar una imagen si no se puede descodificar mediante un códec proporcionado por Windows y, al llamar al método [**CreateComponentEnumerator**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentenumerator) , solo se devolverán los componentes proporcionados por Windows.

### <a name="changes-to-clsid_wicpngdecoder-and-png-decoder-color-context-support"></a>Cambios en la \_ compatibilidad con el contexto de color del descodificador de CLSID WICPngDecoder y PNG

**CLSID \_ de WICPngDecoder1** se ha agregado con el mismo GUID que **CLSID \_ WICPngDecoder** y se ha agregado **CLSID \_ WICPngDecoder2** .

Cuando se compila con el SDK de Windows 8, **CLSID \_ WICPngDecoder** se \# define como **CLSID \_ WICPngDecoder2** para promover aplicaciones recién compiladas con el nuevo comportamiento del descodificador de PNG. Las aplicaciones deben continuar especificando el **CLSID \_ WICPngDecoder**.

Si se especifica **CLSID \_ WICPngDecoder2** , se creará una versión del descodificador de PNG de WIC que generará un [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) a partir de fragmentos de cHRM y gama. Esto permite usar estos metadatos de espacio de colores con otras API de Windows para la administración de color de la imagen de origen. Un **IWICColorContext** no se genera a partir de los fragmentos gama y cHRM si está presente un fragmento ICCP, si hay un fragmento sRGB, o si los fragmentos gama y cHRM indican un espacio de color sRGB.

Una aplicación puede especificar **CLSID \_ WICPngDecoder1** para crear una versión del descodificador de PNG de WIC que no genera un [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) a partir de los fragmentos de gama y cHRM. Esto coincide con el comportamiento del descodificador PNG en versiones anteriores de Windows.

### <a name="changes-to-wincodec_sdk_version"></a>Cambios en la \_ versión del SDK de WINCODEC \_

Cuando se compila con el SDK de Windows 8, la **\_ \_ versión del SDK de WINCODEC** se \# define como **WINCODEC \_ SDK \_ VERSION2** para promover las aplicaciones recién compiladas con el nuevo comportamiento del descodificador de PNG. De lo contrario, se \# define como **WINCODEC \_ SDK \_ VERSION1**. Las aplicaciones deben seguir especificando la **\_ \_ versión del SDK de WINCODEC**.

Si se especifica la **\_ \_ versión del SDK de WINCODEC** al llamar a [**WICCreateImagingFactory \_ proxy**](-wic-codec-wiccreateimagingfactory-proxy.md) para crear el generador de imágenes, se creará **CLSID \_ WICPngDecoder2** en lugar de **CLSID \_ WICPngDecoder1** desde el método [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) y sus variantes. Además, un enumerador de información de componente de descodificador devolverá la información del componente **CLSID \_ WICPngDecoder2** , pero no la información de **CLSID \_ WICPngDecoder1** .

La especificación de **WINCODEC \_ SDK \_ VERSION1** hará que se use **CLSID \_ WICPngDecoder1** en lugar de **CLSID \_ WICPngDecoder2** en los casos anteriores.

### <a name="changes-to-clsid_wicimagingfactory"></a>Cambios en CLSID \_ WICImagingFactory

**CLSID \_ de WICImagingFactory1** se ha agregado con el mismo GUID que **CLSID \_ WICImagingFactory** y se ha agregado **CLSID \_ WICImagingFactory2** .

Cuando se compila con el SDK de Windows 8, **CLSID \_ WICImagingFactory** se \# define como **CLSID \_ WICImagingFactory2** para promover aplicaciones recién compiladas con el nuevo comportamiento del descodificador de PNG. Las aplicaciones deben continuar especificando el **CLSID \_ WICImagingFactory**.

Si se especifica **CLSID \_ WICImagingFactory2** al llamar a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el generador de imágenes, se creará **CLSID \_ WICPngDecoder2** en lugar de **CLSID \_ WICPngDecoder1** desde el método [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) y sus variantes. Además, un enumerador de información de componente de descodificador devolverá la información del componente **CLSID \_ WICPngDecoder2** , pero no la información de **CLSID \_ WICPngDecoder1** .

Si se especifica **CLSID \_ WICImagingFactory1** , se utilizará **CLSID \_ WICPngDecoder1** en lugar de **CLSID \_ WICPngDecoder2** en los casos anteriores.

## <a name="whats-new-for-windows-7"></a>Novedades de Windows 7

En Windows 7, WIC se ha actualizado con varias características nuevas. En este tema se proporciona una introducción rápida a estas nuevas características.

### <a name="updates-to-the-tiff-codec"></a>Actualizaciones del códec TIFF

El códec WIC TIFF se ha actualizado para Windows 7 para admitir varias características no admitidas por la versión anterior de WIC.

-   Compatibilidad con archivos TIFF de gran tamaño.
-   Descodificar imágenes TIFF en mosaico.
-   Descodificar imágenes TIFF (plano).
-   Descodificar imágenes TIFF con codificación JPEG.

### <a name="progressive-decoding"></a>Descodificación progresiva

La descodificación progresiva proporciona la capacidad de descodificar y representar gradualmente partes de una imagen antes de que toda la imagen termine de descargarse. Esta característica mejora en gran medida la experiencia del usuario al ver imágenes desde Internet, ya que el usuario no tiene que esperar a que se descargue toda la imagen antes de que pueda comenzar la descodificación. Con la descodificación progresiva, los usuarios pueden ver una vista previa de la imagen con los datos disponibles durante mucho tiempo antes de descargar la imagen completa. Esta característica es esencial para cualquier aplicación que se use para ver imágenes de Internet o de orígenes de datos con ancho de banda limitado.

Para obtener más información, vea [información general sobre la descodificación progresiva](-wic-progressive-decoding.md).

### <a name="extended-metadata-support-for-jpeg-png-and-gif"></a>Compatibilidad con metadatos extendidos para JPEG, PNG y GIF

En Windows 7, WIC amplió su compatibilidad con metadatos para imágenes JPEG, PNG y GIF.

-   Se ha agregado compatibilidad con las propiedades GIF y gif animadas.
-   Controladores de metadatos JPG expandidos que admiten metadatos de crominancia, luminancia y comentarios.
-   Controladores de metadatos PNG expandidos para admitir los metadatos tIME, sRGB, iCCP, hIST, cHRM, iTXt, bKGD y gAMA.
-   Se han agregado nuevos controladores de metadatos de 8BIM para metadatos de ResolutionInfo y metadatos de compendio de IPTC.
-   Se han agregado nuevos controladores de metadatos para el descriptor de pantalla lógico (LSD), el descriptor de imagen (IMD), las extensiones de control gráfico (GCE) y los metadatos de extensiones de aplicación (APE).
-   Compatibilidad con metadatos que abarcan bloques APPn.

### <a name="multi-threaded-apartment-support"></a>Compatibilidad con apartamento multiproceso

Se puede llamar a los objetos de un contenedor multiproceso (MTA) simultáneamente con cualquier número de subprocesos del MTA, lo que permite un mejor rendimiento en los sistemas de varios núcleos y en determinados escenarios de servidor. Además, los códecs WIC que viven dentro de un MTA pueden llamar a otros objetos que viven dentro del MTA sin el costo de serialización asociado a la llamada entre subprocesos que residen en distintos apartamentos STA. En Windows 7, todos los códecs WIC integrados se han actualizado para admitir MTA, como JPEG, TIFF, PNG, GIF, ICO y BMP. Se recomienda escribir códecs para admitir MTA. Los códecs que no son compatibles con MTA provocarán un degradación del de rendimiento significativo en aplicaciones multiproceso debido a la serialización. La habilitación de la compatibilidad con MTA requiere que se implemente la sincronización adecuada en el códec. La implementación exacta de estas técnicas de sincronización está fuera del ámbito de este documento. A continuación se proporciona una referencia general para la sincronización de objetos del modelo de objetos componentes (COM).

### <a name="metadata-working-group-implementations"></a>Implementaciones de grupos de trabajo de metadatos

Actualmente hay una variedad de formatos de almacenamiento de metadatos que contienen propiedades que se superponen, sin ningún estándar del sector claro ni orientación sobre métodos coherentes para leer y escribir estos formatos de metadatos. Para ayudar con esta variedad de formatos y propiedades, se formó el grupo de trabajo de metadatos (MWG). El objetivo de MWG es proporcionar directrices que garanticen la interoperabilidad entre una amplia variedad de plataformas, aplicaciones y dispositivos. Las instrucciones establecidas por MWG se aplican a los campos de metadatos XMP, EXIF y IPTC y a los formatos de imagen JPEG, TIFF y PSD.

En Windows 7, el controlador de metadatos de la foto y el nivel de directiva de metadatos se han actualizado para leer y escribir metadatos de imagen de acuerdo con las instrucciones establecidas por el MWG. Para obtener más información sobre el grupo de trabajo de metadatos (MWG), vea las [directrices de metadatos establecidas](https://s3.amazonaws.com/software.tagthatphoto.com/docs/mwg_guidance.pdf).

### <a name="windows-7-features-supported-on-windows-vista-and-windows-server-2008"></a>Características de Windows 7 compatibles con Windows Vista y Windows Server 2008

La [actualización de la plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md) es un conjunto de bibliotecas en tiempo de ejecución que permite a los desarrolladores destinar aplicaciones a Windows 7 y Windows Vista. La actualización de la plataforma para Windows Server 2008 es un conjunto de bibliotecas en tiempo de ejecución que permite a los desarrolladores destinar aplicaciones a Windows Server 2008 R2 y Windows Server 2008. La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update. Las aplicaciones de terceros que requieren la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 pueden detectar Windows Update detectar si está instalado el requerido actualizado; en caso contrario, Windows Update lo descargará e instalará en segundo plano. Para obtener más información acerca de ambas actualizaciones, consulte Actualización de la plataforma para Windows Vista.

 

 
