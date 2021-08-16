---
description: Windows Imaging Component (WIC) se ha actualizado con nuevas versiones de Windows. En este tema se proporciona una introducción rápida a estas nuevas características.
ms.assetid: 710B71CE-6FCC-46DA-A65C-6E4FC6A04275
title: Novedades de WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420d501dd495081764a7fba89f73d21077c04b05d92e7c2b47c3c2c2d51d7d10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204020"
---
# <a name="whats-new-in-wic"></a>Novedades de WIC

Windows Imaging Component (WIC) se ha actualizado con nuevas versiones de Windows. En este tema se proporciona una introducción rápida a estas nuevas características.

## <a name="whats-new-for-windows-10-version-1507"></a>Novedades de Windows 10, versión 1507

### <a name="access-to-low-level-jpeg-data-for-wic-decoding-and-encoding"></a>Acceso a datos JPEG de bajo nivel para la codificación y la codificación de WIC

A partir Windows 10, versión 1507, WIC proporciona acceso a estructuras de datos JPEG de bajo nivel, incluidas las tablas de cuantificación y Huffman. Para obtener más información, vea los temas siguientes:

-   [**IWICPlantegFrameDecode (interfaz)**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframedecode)
-   [**IWICPlantegFrameEncode (interfaz)**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframeencode)

### <a name="jpeg-indexing"></a>Indexación JPEG

La indexación JPEG es una técnica que mejora significativamente el rendimiento del acceso aleatorio a pequeñas subrecciones de una imagen JPEG grande, a costa de un uso adicional de memoria. Cualquier llamador de WIC puede aprovechar la indexación JPEG.

La [**interfaz ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) está diseñada para aprovechar la indexación JPEG si está activada. Por ejemplo, la API ID2D1ImageSource solo solicitará las secciones necesarias de la imagen en un escenario como el desplazamiento panorámico y el zoom para una imagen de resolución grande. Para obtener más información, vea los temas siguientes:

-   [**IWICPlantegFrameDecode::SetIndexing (Método)**](/windows/win32/api/Wincodec/nf-wincodec-iwicjpegframedecode-setindexing)
-   [**Interfaz ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)

## <a name="whats-new-for-windows-81"></a>Novedades de Windows 8.1

### <a name="support-for-jpeg-ycbcr-images"></a>Compatibilidad con imágenes JPEG YCbCr

A partir Windows 8.1, WIC proporciona compatibilidad para la codificación, transformación y codificación de datos de imagen JPEG Y'CbCr en su formato nativo. Esto permite a las aplicaciones reducir significativamente el tiempo de procesamiento y el consumo de memoria para determinadas operaciones de creación de imágenes cuando se trabaja con JPEG codificados por Y'CbCr. Para obtener más información, vea los temas siguientes:

-   Efecto[YCbCr de](../direct2d/ycbcr-effect.md) [Direct2D](-wic-sample-d2d-viewer.md)
-   [**IWICPlanarBitmapSourceTransform (interfaz)**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
-   [**IWICPlanarBitmapFrameEncode (interfaz)**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode)

### <a name="support-for-block-compressed-formats-dds-files"></a>Compatibilidad con formatos comprimidos en bloques (archivos DDS)

A partir de Windows 8.1, WIC agrega un nuevo códec que admite imágenes DDS codificadas en los siguientes formatos: DXGI \_ FORMAT \_ BC1 \_ UNORM, DXGI \_ FORMAT BC2 UNORM y \_ \_ DXGI FORMAT \_ \_ BC3 \_ UNORM. Se puede acceder a los datos comprimidos de bloques DDS en un formato descodificado mediante interfaces WIC estándar, o bien se puede acceder directamente a ellos mediante nuevas interfaces específicas de DDS. Para obtener más información, vea los temas siguientes:

-   [**IWICDdsDecoder (interfaz)**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsdecoder)
-   [**IWICDdsEncoder (interfaz)**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsencoder)

## <a name="whats-new-for-windows-8"></a>Novedades de Windows 8

En Windows 8, WIC se ha actualizado con varias características nuevas. La versión actualizada de WIC también está disponible en Windows 7 y Windows Server 2008 R2 a través de la actualización de plataforma para [Windows 7](../direct3darticles/platform-update-for-windows-7.md), que está disponible a través de la actualización de plataforma [para Windows 7](https://support.microsoft.com/kb/2670838).

### <a name="improved-direct2d-integration"></a>Integración mejorada de Direct2D

WIC en Windows 8 proporciona estas API para mejorar la integración de Direct2D con WIC:

-   [**IWICImageEncoder:**](/windows/win32/api/Wincodec/nn-wincodec-iwicimageencoder) una nueva interfaz que puede codificar el contenido de [**Direct2D ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) en [un IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md). Los métodos de esta interfaz toman un puntero a [**WICImageParameters**](/windows/win32/api/Wincodec/ns-wincodec-wicimageparameters), que son parámetros para controlar la codificación.
-   [**IWICImagingFactory2:**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory2) nuevo generador de WIC con [**el método CreateImageEncoder.**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder) Esta interfaz hereda del generador de WIC original, [**IWICImagingFactory,**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory)y se crea de la misma manera.

### <a name="changes-to-bmp-codec-alpha-support"></a>Cambios en la compatibilidad alfa de códec BMP

WIC en Windows 8 archivos de [**imagen BITMAPV5HEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) como imágenes con formato [WICPixelFormat32bppBGRA.](-wic-codec-native-pixel-formats.md) Además, el codificador BMP admite una nueva opción booleana de codificador "EnableV5Header32bppBGRA", que indica al codificador que escriba un **BITMAPV5HEADER** con los datos de imagen 32bppBGRA.

Para obtener más información sobre los formatos BMP, vea [Información general sobre el formato BMP.](bmp-format-overview.md)

### <a name="new-pixel-formats"></a>Nuevos formatos de píxel

WIC en Windows 8 define estos nuevos formatos de píxel:

-   GUID \_ WICPixelFormat32bppRGB
-   GUID \_ WICPixelFormat64bppRGB
-   GUID \_ WICPixelFormat96bppRGBFloat
-   GUID \_ WICPixelFormat64bppPRGBAHalf

> [!Note]  
> El códec integrado TIFF devolverá datos \_ GUID WICPixelFormat96bppRGBFloat. Los otros tres formatos no los usan los códecs integrados.

 

### <a name="restrictions-to-component-extensibility-in-appcontainer"></a>Restricciones a la extensibilidad de componentes en AppContainer

Cuando se ejecuta en un proceso AppContainer, que incluye todas las aplicaciones de Windows Store, WIC solo usará componentes proporcionados por Windows, independientemente de si hay componentes adicionales instalados en el sistema. La aplicación que no se ejecuta en AppContainer no se ve afectada.

Las aplicaciones no necesitan realizar ningún cambio en el código para ejecutarse en appContainger, pero la marca [**WICComponentEnumerateOptions**](/windows/win32/api/Wincodec/ne-wincodec-wiccomponentenumerateoptions) y los parámetros GUID del proveedor no tendrán ningún efecto. WIC no podrá cargar una imagen si no se puede descodificar mediante un códec proporcionado por Windows y llamar al método [**CreateComponentEnumerator**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentenumerator) solo devolverá Windows componentes proporcionados.

### <a name="changes-to-clsid_wicpngdecoder-and-png-decoder-color-context-support"></a>Cambios en CLSID \_ WICPngDecoder y compatibilidad con el contexto de color del descodificador PNG

**CLSID \_ WICPngDecoder1** se ha agregado con el mismo GUID que **CLSID \_ WICPngDecoder** y se ha agregado **CLSID \_ WICPngDecoder2.**

Cuando se compila con el SDK de Windows 8, **CLSID \_ WICPngDecoder** se define en \# **CLSID \_ WICPngDecoder2** para promover las aplicaciones recién compiladas mediante el nuevo comportamiento del descodificador PNG. Las aplicaciones deben seguir **especificando CLSID \_ WICPngDecoder**.

Si se especifica **CLSID \_ WICPngDecoder2,** se creará una versión del descodificador PNG de WIC que generará un [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) a partir de fragmentos cHRM y gAMA. Esto permite que estos metadatos de espacio de color se utilicen con otras API de Windows api para administrar el color de la imagen de origen. No se genera un **IWICColorContext** a partir de los fragmentos gAMA y cHRM si hay un fragmento de iCCP, si hay un fragmento de sRGB, o si los fragmentos gAMA y cHRM indican un espacio de colores sRGB.

Una aplicación puede especificar **CLSID \_ WICPngDecoder1** para crear una versión del descodificador PNG de WIC que no genere un [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) a partir de los fragmentos gAMA y cHRM. Esto coincide con el comportamiento del descodificador PNG en versiones anteriores de Windows.

### <a name="changes-to-wincodec_sdk_version"></a>Cambios en la VERSIÓN DEL SDK de WINCODEC \_ \_

Cuando se compila con el SDK de Windows 8, LA VERSIÓN DEL SDK de **WINCODEC \_ \_** se define en \# **WINCODEC \_ SDK \_ VERSION2** para promover las aplicaciones recién compiladas mediante el nuevo comportamiento del descodificador PNG. De lo contrario, \# se define en **WINCODEC \_ SDK \_ VERSION1**. Las aplicaciones deben seguir especificando **LA VERSIÓN DEL \_ SDK \_ de WINCODEC.**

Si se especifica LA VERSIÓN del SDK de **WINCODEC \_ \_** al llamar a [**WICCreateImagingFactory \_ Proxy**](-wic-codec-wiccreateimagingfactory-proxy.md) para crear el generador de imágenes, se crea **CLSID \_ WICPngDecoder2** en lugar de **CLSID \_ WICPngDecoder1** desde el [**método CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) y sus variantes. Además, un enumerador de información del componente descodificador devolverá la información del componente **\_ CLSID WICPngDecoder2,** pero no la información de **\_ CLSID WICPngDecoder1.**

Si se especifica **WINCODEC \_ SDK \_ VERSION1,** se usará **CLSID \_ WICPngDecoder1** en lugar de **CLSID \_ WICPngDecoder2** en los casos anteriores.

### <a name="changes-to-clsid_wicimagingfactory"></a>Cambios en CLSID \_ WICImagingFactory

**CLSID \_ WICImagingFactory1** se ha agregado con el mismo GUID que **CLSID \_ WICImagingFactory** y se ha agregado **CLSID \_ WICImagingFactory2.**

Cuando se compila con el SDK de Windows 8, **CLSID \_ WICImagingFactory** se define en \# **CLSID \_ WICImagingFactory2** para promover las aplicaciones recién compiladas mediante el nuevo comportamiento del descodificador PNG. Las aplicaciones deben seguir **especificando CLSID \_ WICImagingFactory**.

Si se especifica **CLSID \_ WICImagingFactory2** al llamar a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el generador de imágenes, se crea **CLSID \_ WICPngDecoder2** en lugar de **CLSID \_ WICPngDecoder1** desde el [**método CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) y sus variantes. Además, un enumerador de información del componente descodificador devolverá la información del componente **\_ CLSID WICPngDecoder2,** pero no la información de **\_ CLSID WICPngDecoder1.**

Si se especifica **CLSID \_ WICImagingFactory1,** se usará **CLSID \_ WICPngDecoder1 en** lugar de **CLSID \_ WICPngDecoder2** en los casos anteriores.

## <a name="whats-new-for-windows-7"></a>Novedades de Windows 7

En Windows 7, WIC se ha actualizado con varias características nuevas. En este tema se proporciona una introducción rápida a estas nuevas características.

### <a name="updates-to-the-tiff-codec"></a>Actualizaciones del códec TIFF

El códec WIC TIFF se ha actualizado para Windows 7 para admitir varias características no compatibles con la versión anterior de WIC.

-   Compatibilidad con archivos TIFF grandes.
-   Descodificar imágenes TIFF en mosaico.
-   Descodificar imágenes TIFF planas( planas).
-   Descodificar imágenes TIFF codificadas en JPEG.

### <a name="progressive-decoding"></a>Decoding progresiva

La descodificación progresiva proporciona la capacidad de descodificar y representar incrementalmente partes de una imagen antes de que toda la imagen haya terminado de descargarse. Esta característica mejora considerablemente la experiencia del usuario al ver imágenes desde Internet, ya que el usuario no tiene que esperar a que toda la imagen se descargue antes de que pueda comenzar la descodación. Con la decodificación progresiva, los usuarios pueden ver una vista previa de la imagen con los datos disponibles mucho antes de que se descargue toda la imagen. Esta característica es esencial para cualquier aplicación que se usa para ver imágenes desde Internet o desde orígenes de datos con ancho de banda limitado.

Para obtener más información, vea [Información general sobre la decodación progresiva.](-wic-progressive-decoding.md)

### <a name="extended-metadata-support-for-jpeg-png-and-gif"></a>Compatibilidad con metadatos extendidos para JPEG, PNG y GIF

En Windows 7, WIC ha ampliado su compatibilidad con metadatos para imágenes JPEG, PNG y GIF.

-   Se ha agregado compatibilidad con las propiedades GIF y GIF animadas.
-   Controladores de metadatos JPG expandido para admitir metadatos de chrominance, luminance y comment.
-   Controladores de metadatos PNG expandidos para admitir los metadatos tIME, sRGB, iCCP, hIST, cHRM, iTXt, bHRD y gXT.
-   Se han agregado nuevos controladores de metadatos de 8BIM para metadatos ResolutionInfo y metadatos de resumen de IPTC.
-   Se han agregado nuevos controladores de metadatos para los metadatos de Descriptor de pantalla lógica (LSD), Descriptor de imagen (IMD), Extensiones de control gráfico (GCE) y Extensiones de aplicación (APE).
-   Compatibilidad con metadatos que abarcan bloques APPn.

### <a name="multi-threaded-apartment-support"></a>Compatibilidad con apartamento multiproceso

Cualquier número de subprocesos dentro del MTA puede llamar simultáneamente a los objetos dentro de un apartamento multiproceso (MTA), lo que permite un mejor rendimiento en sistemas de varios núcleos y determinados escenarios de servidor. Además, los códecs WIC que se encuentran dentro de un MTA pueden llamar a otros objetos que se encuentran dentro del MTA sin el costo de serialización asociado a la llamada entre subprocesos que se encuentran en diferentes departamentos STA. En Windows 7, todos los códecs WIC integrados se han actualizado para admitir MTA, incluidos JPEG, TIFF, PNG, GIF, ICO y BMP. Se recomienda encarecidamente escribir códecs para admitir MTA. Los códecs que no admiten MTA provocarán una reducción significativa del rendimiento en las aplicaciones multiproceso debido a la serialización. La habilitación de la compatibilidad con MTA requiere que se implemente la sincronización adecuada en el códec. La implementación exacta de estas técnicas de sincronización está fuera del ámbito de este documento. A continuación se proporciona una referencia general para sincronizar objetos del Modelo de objetos componentes (COM).

### <a name="metadata-working-group-implementations"></a>Implementaciones de grupos de trabajo de metadatos

Actualmente hay una variedad de formatos de almacenamiento de metadatos que contienen propiedades superpuestas, sin ningún estándar del sector claro ni instrucciones sobre métodos coherentes para leer y escribir estos formatos de metadatos. Para ayudar con esta variedad de formatos y propiedades, se ha formado el grupo de trabajo de metadatos (MWG). El objetivo de MWG es proporcionar directrices que garanticen la interoperabilidad entre una amplia variedad de plataformas, aplicaciones y dispositivos. Las directrices establecidas por MWG se aplican a los campos de metadatos XMP, Exif e IPTC, y a los formatos de imagen JPEG, TIFF y PSD.

En Windows 7, el controlador de metadatos de fotos y la capa de directiva de metadatos se han actualizado para leer y escribir metadatos de imagen según las directrices establecidas por MWG. Para obtener más información sobre el grupo de trabajo de metadatos (MWG), vea las [directrices de metadatos establecidas.](https://s3.amazonaws.com/software.tagthatphoto.com/docs/mwg_guidance.pdf)

### <a name="windows-7-features-supported-on-windows-vista-and-windows-server-2008"></a>Windows 7 características admitidas en Windows Vista y Windows Server 2008

La [actualización de plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md) es un conjunto de bibliotecas en tiempo de ejecución que permite a los desarrolladores dirigir aplicaciones a Windows 7 y Windows Vista. La actualización de plataforma para Windows Server 2008 es un conjunto de bibliotecas en tiempo de ejecución que permite a los desarrolladores dirigir las aplicaciones a Windows Server 2008 R2 y Windows Server 2008. La actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update. Las aplicaciones de terceros que requieren actualización de plataforma para Windows Vista o actualización de plataforma para Windows Server 2008 pueden hacer que Windows Update detecte si está instalada la actualización necesaria; Si no es así, Windows Update lo descargará e instalará en segundo plano. Para obtener más información sobre ambas actualizaciones, vea Actualización de plataforma para Windows Vista.

 

 
