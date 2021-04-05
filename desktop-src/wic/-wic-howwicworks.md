---
description: Más información acerca de cómo funciona el componente de creación de imágenes de Windows
ms.assetid: c233e25b-bec6-4e67-8fbf-2bf9b70c7522
title: Cómo funciona el componente de creación de imágenes de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc9fe31ae4346f2c2d1f0b273e78ed10a0ec7e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815470"
---
# <a name="how-the-windows-imaging-component-works"></a>Cómo funciona el componente de creación de imágenes de Windows

Este tema contiene las siguientes secciones:

-   [Detección y arbitraje](#discovery-and-arbitration)
-   [Descodificación](#decoding)
-   [Encoding](#encoding)
-   [La duración de un códec](#the-lifetime-of-a-codec)
-   [Cómo habilitar un códec con WIC](#how-to-wic-enabled-a-codec)
-   [Compatibilidad con apartamento multiproceso en WIC](#multi-threaded-apartment-support-in-wic)
-   [Temas relacionados](#related-topics)

## <a name="discovery-and-arbitration"></a>Detección y arbitraje

Antes de que se pueda descodificar una imagen, se debe encontrar un códec adecuado que pueda descodificar ese formato de imagen. En la mayoría de los sistemas, dado que los formatos de imagen admitidos están codificados de forma rígida, no se requiere ningún proceso de detección. Dado que la plataforma de componentes de imágenes de Windows (WIC) es extensible, es necesario poder identificar el formato de una imagen y hacerla coincidir con un códec adecuado.

Para admitir la detección en tiempo de ejecución, cada formato de imagen debe tener un patrón de identificación que se pueda usar para identificar el descodificador adecuado para ese formato. (Se recomienda encarecidamente que, para los nuevos formatos de archivo, use un GUID para el patrón de identificación, ya que se garantiza que es único). El patrón de identificación debe estar incrustado en cada archivo de imagen que se ajuste a ese formato de imagen. Cada descodificador tiene una entrada del registro que especifica el patrón de identificación o patrones de los formatos de imagen que puede descodificar. Cuando una aplicación necesita abrir una imagen, solicita un descodificador de WIC. WIC busca los descodificadores disponibles en el registro y comprueba cada entrada del registro en busca de un patrón de identificación que coincida con el patrón incrustado en el archivo de imagen. Para obtener más información sobre las entradas del registro del descodificador, consulte [entradas del registro específicas del codificador](-wic-decoderregentries.md) .

Cuando WIC encuentra un único descodificador que coincide con el patrón de identificación de la imagen, crea una instancia del descodificador y le pasa el archivo de imagen. Si WIC encuentra más de una coincidencia, invoca un método denominado [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) en cada descodificador coincidente para arbitrar entre ellos y encontrar la mejor coincidencia. Para obtener más información, vea la sección [QueryCapabilities](-wic-imp-iwicbitmapdecoder.md) en el tema sobre la [implementación de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

## <a name="decoding"></a>Descodificación

Una vez que se ha seleccionado el descodificador adecuado y se ha creado una instancia, la aplicación se comunica directamente con el descodificador. El descodificador tiene varias responsabilidades, que implementa a través de varias interfaces. Estos servicios se pueden clasificar como:

-   Servicios de nivel de contenedor
-   Servicios de nivel de marco
-   Servicios de enumeración de metadatos
-   Transformaciones nativas del descodificador
-   Notificaciones de progreso y compatibilidad de cancelación
-   Servicios de procesamiento sin procesar

Los servicios de nivel de contenedor incluyen la recuperación de la miniatura de nivel superior (si se admite), la vista previa, los contextos de color, la paleta (si es aplicable) y el formato de contenedor, así como proporcionar acceso a los fotogramas de imagen individuales dentro del contenedor. (Algunos contenedores contienen un solo fotograma, mientras que otros, como Tagged Image File Format (TIFF), pueden contener varios fotogramas). Este conjunto de servicios también incluye proporcionar información sobre el propio descodificador y sus capacidades con respecto a un archivo de imagen específico.

Los fotogramas individuales tienen sus propias miniaturas y también pueden tener sus propios contextos de color, paletas y otras propiedades, que se exponen en el nivel de marco. Sin embargo, la operación más importante realizada en el nivel de marco es la descodificación real de los bits de imagen para ese marco.

WIC proporciona a los lectores de metadatos los formatos de metadatos más comunes (IFD, EXIF, IPTC, XMP, APP0, APP1 y otros formatos) y también admite la extensibilidad para formatos de metadatos de terceros. Esto libera el códec de la responsabilidad de analizar los metadatos. Sin embargo, el códec es responsable de enumerar los bloques de metadatos y de solicitar un lector de metadatos para cada bloque. WIC realiza la detección de los controladores de metadatos de la misma manera que lo hace para los códecs, basándose en un patrón del encabezado de bloque que coincide con un patrón en la entrada del registro del controlador de metadatos. Para obtener más información, consulte las [entradas del registro específicas del codificador](-wic-decoderregentries.md) .

No es necesario que los descodificadores admitan de forma nativa las operaciones de transformación, pero esto permite optimizaciones de rendimiento significativas que proporcionan una mejor experiencia de usuario final. Por ejemplo, una aplicación puede crear una canalización de varias transformaciones (escalado, recorte, rotación y conversión de formato de píxeles) para realizar en una imagen antes de que se represente la imagen. Para obtener más información sobre las canalizaciones de transformación, vea [IWICBitmapSource](-wic-imp-iwicbitmapsource.md). Después de crear una canalización de transformación, la aplicación solicita la transformación final de la canalización para generar el mapa de bits que se obtiene al aplicar todas las transformaciones al origen de la imagen. En ese momento, si el propio descodificador puede realizar operaciones de transformación, WIC pregunta cuál de las transformaciones solicitadas puede realizar. Las transformaciones solicitadas que no pueda realizar el descodificador se realizarán mediante WIC en la imagen descodificada antes de devolverla al autor de la llamada. Esta canalización de transformación optimizada proporciona un mejor rendimiento que la realización de cada transformación secuencialmente en la memoria, especialmente cuando algunas o todas las transformaciones se pueden realizar durante el proceso de descodificación.

Las notificaciones de progreso y la compatibilidad con la cancelación permiten que una aplicación solicite notificaciones de progreso para las operaciones largas y también permite a la aplicación ofrecer al usuario la posibilidad de cancelar una operación que está tardando demasiado tiempo. Esto es importante porque si un usuario no puede cancelar una operación, puede sentir que el proceso se ha bloqueado e intentar cancelarlo cerrando la aplicación.

Estas interfaces se describen en detalle en la sección sobre la [implementación de un descodificador de WIC-Enabled](-wic-implementingwicdecoder.md).

Los servicios de procesamiento sin formato incluyen el ajuste de la configuración de la cámara, como la exposición, el contraste y el enfoque, o el cambio del espacio de colores antes de procesar los bits sin formato.

## <a name="encoding"></a>Encoding

Al igual que los descodificadores, los codificadores tienen responsabilidades que implementan a través de interfaces. Los servicios que proporcionan los codificadores son complementarios a los servicios proporcionados por los descodificadores, salvo que escriben datos de imagen en lugar de leerlo. Los codificadores también proporcionan servicios en las siguientes categorías:

-   Servicios de nivel de contenedor
-   Servicios de nivel de marco
-   Enumeración de metadatos y servicios de actualización
-   Compatibilidad con notificaciones de progreso y cancelación

Los servicios de nivel de contenedor para un codificador incluyen el establecimiento de la miniatura de nivel superior (si se admite), la vista previa y la paleta (si es aplicable) y la iteración por los fotogramas de imagen individuales para que se puedan serializar en el contenedor.

Los servicios de nivel de marco de un codificador reflejan los del descodificador, salvo que escriben los datos de imagen, la miniatura y cualquier paleta asociada u otro componente, en lugar de leerlos.

Además, los servicios de enumeración de metadatos para un codificador incluyen la iteración por los bloques de metadatos que se van a escribir y la invocación de los escritores de metadatos adecuados para serializar los metadatos en el disco.

Estas interfaces se describen en detalle en la sección sobre la [implementación de un codificador de WIC-Enabled](-wic-implementingwicencoder.md).

## <a name="the-lifetime-of-a-codec"></a>La duración de un códec

Se crea una instancia de un códec WIC para controlar una sola imagen y, normalmente, tiene una duración breve. Se crea cuando se carga una imagen y se libera cuando se cierra la imagen. Una aplicación puede usar un gran número de códecs simultáneamente con una duración de superposición (es decir, desplazarse a través de un directorio que contenga cientos de imágenes) y varias aplicaciones pueden hacerlo al mismo tiempo.

Aunque algunos códecs tienen una duración cuyo ámbito es la duración del proceso en el que residen, este no es el caso de los códecs WIC. La Galería fotográfica de Windows Vista, el explorador de Windows y el visor fotográfico, así como otras muchas aplicaciones, se basan en WIC y usarán el códec para mostrar imágenes y miniaturas. Si el ámbito de la duración del códec es la duración del proceso, cada vez que se muestra una imagen o una miniatura en el explorador de Windows Vista, el códec del que se ha creado una instancia para descodificar esa imagen permanecerá en memoria hasta la próxima vez que el usuario reinicie su equipo. Si el códec nunca está descargado, sus recursos están, en efecto, "filtrados" porque no se pueden usar en ningún otro componente del sistema.

## <a name="how-to-wic-enabled-a-codec"></a>Cómo habilitar un códec con WIC

1.  Implemente una clase de descodificador de nivel de contenedor y una clase de descodificador de nivel de marco que exponga las interfaces WIC necesarias para descodificar imágenes y recorrer en iteración los bloques de metadatos. Esto permite que todas las aplicaciones basadas en WIC interactúen con el códec de la misma manera que interactúan con los formatos de imagen estándar.
2.  Implemente una clase de codificador de nivel de contenedor y una clase de codificador de nivel de marco que exponga las interfaces WIC necesarias para codificar imágenes y serializar bloques de metadatos en un archivo de imagen.
3.  Si el formato del contenedor no se basa en un contenedor TIFF o JPEG, puede que tenga que escribir controladores de metadatos para los formatos de metadatos comunes (EXIF, XMP). Sin embargo, si usa un formato de contenedor basado en TIFF o JPEG, no es necesario porque puede delegar en los controladores de metadatos proporcionados por el sistema.
4.  Inserte un patrón de identificación único (se recomienda un GUID) en todos los archivos de imagen. Esto permite que el formato de la imagen coincida con el códec durante la detección. Si está escribiendo un contenedor WIC para un formato de imagen existente, debe buscar un patrón de bits que el codificador siempre escribe en los archivos de imagen que son únicos para ese formato de imagen y usarlos como el patrón de identificación).
5.  Registre el códec en el momento de la instalación. Esto permite detectar el códec en tiempo de ejecución haciendo coincidir el patrón de identificación del registro con el patrón incrustado en el archivo de imagen.
6.  A partir de Windows 7, WIC requiere que los códecs tengan el tipo de Apartamento COM "both". Esto significa que debe realizar el bloqueo adecuado para administrar llamadores y llamadores entre apartamentos en escenarios de varios subprocesos. Para obtener más información, consulte la sección siguiente sobre compatibilidad con apartamento multiproceso.
7.  Compatibilidad con las plataformas de 64 bits: para Windows 7, WIC requiere que los códecs WIC de terceros se entreguen como archivos binarios nativos de 32 bits y de 64 bits. Además, el formato de 32 bits debe instalarse y ejecutarse en sistemas de 64 bits, y el instalador de códecs de Windows 7 de terceros debe instalar los archivos binarios de 32 bits y de 64 bits en sistemas de 64 bits.

## <a name="multi-threaded-apartment-support-in-wic"></a>Compatibilidad con apartamento multiproceso en WIC

Se puede llamar a los objetos de un contenedor multiproceso (MTA) simultáneamente en cualquier número de subprocesos del MTA. Esto permite un mejor rendimiento en los sistemas de varios núcleos y en determinados escenarios de servidor. Además, los códecs WIC de un MTA pueden llamar a otros objetos del MTA sin el costo de serialización asociado a la llamada entre subprocesos en distintos apartamentos STA. En Windows 7, todos los códecs WIC integrados se han actualizado para admitir MTA, como JPEG, TIFF, PNG, GIF, ICO y BMP. Se recomienda escribir códecs de terceros para admitir MTA. Los códecs de terceros que no son compatibles con los MTA causan importantes costos de rendimiento en las aplicaciones multiproceso debido a la serialización. La habilitación de la compatibilidad con MTA requiere que se implemente la sincronización adecuada en el códec de terceros. La implementación exacta de estas técnicas de sincronización está fuera del ámbito de este documento. Para obtener más información sobre la sincronización de objetos COM, vea [Descripción y uso de modelos de subprocesos com](/previous-versions/ms809971(v=msdn.10)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Introducción (cómo escribir un códec WIC-Enabled)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Implementar un descodificador de WIC-Enabled](-wic-implementingwicdecoder.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre metadatos de WIC](-wic-about-metadata.md)
</dt> </dl>

 

 



