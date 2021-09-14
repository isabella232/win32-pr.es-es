---
description: 'Más información sobre: Funcionamiento del componente Windows creación de imágenes'
ms.assetid: c233e25b-bec6-4e67-8fbf-2bf9b70c7522
title: Funcionamiento del componente Windows imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc9fe31ae4346f2c2d1f0b273e78ed10a0ec7e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362790"
---
# <a name="how-the-windows-imaging-component-works"></a>Funcionamiento del componente Windows imaging

Este tema contiene las siguientes secciones:

-   [Detección y arbitraje](#discovery-and-arbitration)
-   [Descodificación](#decoding)
-   [Encoding](#encoding)
-   [Duración de un códec](#the-lifetime-of-a-codec)
-   [Cómo habilitar un códec con WIC](#how-to-wic-enabled-a-codec)
-   [Compatibilidad con el apartamento multiproceso en WIC](#multi-threaded-apartment-support-in-wic)
-   [Temas relacionados](#related-topics)

## <a name="discovery-and-arbitration"></a>Detección y arbitraje

Para poder descodificar una imagen, se debe encontrar un códec adecuado que pueda descodificar ese formato de imagen. En la mayoría de los sistemas, dado que los formatos de imagen admitidos están codificados de forma automática, no se requiere ningún proceso de detección. Dado que la plataforma Windows Imaging Component (WIC) es extensible, es necesario poder identificar el formato de una imagen y hacer coincidirla con un códec adecuado.

Para admitir la detección en tiempo de ejecución, cada formato de imagen debe tener un patrón de identificación que se pueda usar para identificar el descodificador adecuado para ese formato. (Se recomienda encarecidamente que, para los nuevos formatos de archivo, use un GUID para el patrón de identificación, ya que se garantiza que sea único). El patrón de identificación debe incrustarse en cada archivo de imagen que se ajuste a ese formato de imagen. Cada descodificador tiene una entrada del Registro que especifica el patrón de identificación o los patrones de los formatos de imagen que puede descodificar. Cuando una aplicación necesita abrir una imagen, solicita un descodificador de WIC. WIC busca los descodificadores disponibles en el registro y comprueba si cada entrada del Registro tiene un patrón de identificación que coincida con el patrón insertado en el archivo de imagen. Para obtener más información sobre las entradas del Registro de descodificación, vea [Entradas del Registro específicas del codificador.](-wic-decoderregentries.md)

Cuando WIC encuentra un único descodificador que coincide con el patrón de identificación de la imagen, crea una instancia del descodificador y le pasa el archivo de imagen. Si WIC encuentra más de una coincidencia, invoca un método denominado [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) en cada descodificador correspondiente para emparejarse entre ellos y encontrar la mejor coincidencia. Para obtener más información, vea la [sección QueryCapabilities](-wic-imp-iwicbitmapdecoder.md) de [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

## <a name="decoding"></a>Descodificación

Después de seleccionar y crear instancias del descodificador adecuado, la aplicación se pone en contacto directamente con el descodificador. El descodificador tiene varias responsabilidades, que implementa a través de varias interfaces. Estos servicios se pueden clasificar como:

-   Servicios de nivel de contenedor
-   Servicios de nivel de marco
-   Servicios de enumeración de metadatos
-   Transformaciones de descodificador nativo
-   Notificaciones de progreso y soporte técnico de cancelación
-   Servicios de procesamiento sin procesar

Los servicios de nivel de contenedor incluyen recuperar la miniatura de nivel superior (si se admite), la vista previa, los contextos de color, la paleta (si procede) y el formato del contenedor, así como proporcionar acceso a los fotogramas de imagen individuales dentro del contenedor. (Algunos contenedores contienen solo un fotograma, mientras que otros, como Tagged Image File Format (TIFF), pueden contener varios fotogramas). Este conjunto de servicios también incluye proporcionar información sobre el propio descodificador y sus funcionalidades con respecto a un archivo de imagen específico.

Los fotogramas individuales tienen sus propias miniaturas y también pueden tener sus propios contextos de color, paletas y otras propiedades, que se exponen en el nivel de fotograma. Sin embargo, la operación más importante realizada en el nivel de fotograma es la decodificación real de los bits de imagen para ese fotograma.

WIC proporciona lectores de metadatos para los formatos de metadatos más comunes (IFD, EXIF, IPTC, XMP, APP0, APP1 y otros formatos) y también admite la extensibilidad para formatos de metadatos de terceros. Esto libera el códec de la responsabilidad de analizar los metadatos. Sin embargo, el códec es responsable de enumerar los bloques de metadatos y solicitar un lector de metadatos para cada bloque. WIC realiza la detección de controladores de metadatos de la misma manera que lo hace con los códecs, en función de un patrón en el encabezado de bloque que coincide con un patrón en la entrada del Registro del controlador de metadatos. Para obtener más información, vea las entradas [del Registro específicas del codificador.](-wic-decoderregentries.md)

Los descodificadores no son necesarios para admitir de forma nativa las operaciones de transformación, pero esto permite optimizaciones de rendimiento significativas que proporcionan una mejor experiencia del usuario final. Por ejemplo, una aplicación puede crear una canalización de varias transformaciones (escalado, recorte, rotación y conversión de formato de píxel) para realizar en una imagen antes de representar la imagen. Para obtener más información sobre las canalizaciones de transformación, [vea IWICBitmapSource](-wic-imp-iwicbitmapsource.md). Después de crear una canalización de transformación, la aplicación solicita la transformación final en la canalización para generar el mapa de bits que resulta de aplicar todas las transformaciones al origen de la imagen. En ese momento, si el propio descodificador puede realizar operaciones de transformación, WIC pregunta cuál de las transformaciones solicitadas puede realizar. WiC realizará las transformaciones solicitadas que el descodificador no pueda realizar en la imagen descodificada antes de devolverla al autor de la llamada. Esta canalización de transformación optimizada proporciona un mejor rendimiento que realizar cada transformación secuencialmente en memoria, especialmente cuando se pueden realizar algunas o todas las transformaciones durante el proceso de descodización.

Las notificaciones de progreso y la compatibilidad con la cancelación permiten a una aplicación solicitar notificaciones de progreso para operaciones largas y también permitir que la aplicación dé al usuario la oportunidad de cancelar una operación que está tardando demasiado tiempo. Esto es importante porque si un usuario no puede cancelar una operación, puede parecer que el proceso se ha cerrado e intentar cancelarla cerrando la aplicación.

Estas interfaces se describen en detalle en la sección [Sobre la implementación de un descodificador WIC-Enabled .](-wic-implementingwicdecoder.md)

Los servicios de procesamiento sin procesar incluyen el ajuste de la configuración de la cámara, como la exposición, el contraste y el ajuste, o el cambio del espacio de color antes de procesar los bits sin procesar.

## <a name="encoding"></a>Encoding

Al igual que los descodificadores, los codificadores tienen responsabilidades que implementan a través de interfaces. Los servicios que proporcionan los codificadores son complementarios a los servicios proporcionados por los descodificadores, salvo que escriben datos de imagen en lugar de leerlo. Los codificadores también proporcionan servicios en las siguientes categorías:

-   Servicios de nivel de contenedor
-   Servicios de nivel de marco
-   Enumeración de metadatos y servicios de actualización
-   Soporte técnico de cancelación y notificación de progreso

Los servicios de nivel de contenedor para un codificador incluyen establecer la miniatura de nivel superior (si se admite), la vista previa y la paleta (si procede) e iterar por los fotogramas de imagen individuales para que se puedan serializar en el contenedor.

Los servicios de nivel de marco para un codificador reflejan los del descodificador, salvo que escriben los datos de la imagen, la miniatura y cualquier paleta asociada u otro componente, en lugar de leerlos.

Además, los servicios de enumeración de metadatos para un codificador incluyen la iteración a través de los bloques de metadatos que se escribirán e invocación de los escritores de metadatos adecuados para serializar los metadatos en el disco.

Estas interfaces se describen en detalle en la sección [Sobre la implementación de un WIC-Enabled Encoder.](-wic-implementingwicencoder.md)

## <a name="the-lifetime-of-a-codec"></a>Duración de un códec

Se crea una instancia de un códec WIC para controlar una sola imagen y normalmente tiene una corta duración. Se crea cuando se carga una imagen y se libera cuando se cierra la imagen. Una aplicación puede usar un gran número de códecs simultáneamente con duraciones superpuestas (piense en desplazarse por un directorio que contiene cientos de imágenes) y varias aplicaciones pueden estar haciendo esto al mismo tiempo.

Aunque algunos códecs tienen una duración que está limitada a la duración del proceso en el que se encuentra, no es el caso de los códecs WIC. Los Windows Vista Galería de fotos, Windows Explorer y Visualizador de fotos, así como muchas otras aplicaciones, se han creado en WIC y usarán el códec para mostrar imágenes y miniaturas. Si el ámbito de la duración del códec es la duración del proceso, cada vez que se muestra una imagen o miniatura en el Explorador de vista de Windows, el códec del que se crea una instancia para descodificar esa imagen permanecerá en memoria hasta la próxima vez que el usuario reinicie su equipo. Si el códec nunca se descarga, sus recursos se "pierden" porque ningún otro componente del sistema los puede usar.

## <a name="how-to-wic-enabled-a-codec"></a>Cómo habilitar un códec con WIC

1.  Implemente una clase descodificadora de nivel de contenedor y una clase descodificadora de nivel de marco que exponga las interfaces WIC necesarias para descodificar imágenes e iterar por bloques de metadatos. Esto permite que todas las aplicaciones basadas en WIC interactúen con el códec de la misma manera que interactúan con los formatos de imagen estándar.
2.  Implemente una clase de codificador de nivel de contenedor y una clase de codificador de nivel de fotograma que exponga las interfaces WIC necesarias para codificar imágenes y serializar bloques de metadatos en un archivo de imagen.
3.  Si el formato del contenedor no se basa en un contenedor TIFF o JPEG, es posible que tenga que escribir controladores de metadatos para los formatos de metadatos comunes (EXIF, XMP). Sin embargo, si usa un formato de contenedor basado en TIFF o JPEG, esto no es necesario porque puede delegar en los controladores de metadatos proporcionados por el sistema.
4.  Inserte un patrón de identificación único (se recomienda un GUID) en todos los archivos de imagen. Esto permite que el formato de la imagen coincida con el códec durante la detección. Si va a escribir un contenedor de WIC para un formato de imagen existente, debe encontrar un patrón de bits que el codificador siempre escribe en sus archivos de imagen que es único para ese formato de imagen y usarlo como patrón de identificación).
5.  Registre el códec en el momento de la instalación. Esto permite detectar el códec en tiempo de ejecución mediante la coincidencia del patrón de identificación en el Registro con el patrón incrustado en el archivo de imagen.
6.  A partir Windows 7, WIC requiere que los códecs sean del tipo de apartamento COM "Both". Esto significa que debe realizar el bloqueo adecuado para controlar los autores de llamadas entre departamentos y los llamadores en escenarios multiproceso. Para obtener más información, consulte la siguiente sección sobre la compatibilidad con los departamentos multiproceso.
7.  Compatibilidad con plataformas de 64 bits: para Windows 7, WIC requerirá que se entreguen códecs WIC de terceros como binarios nativos de 32 y 64 bits. Además, el formulario de 32 bits debe instalarse y ejecutarse en sistemas de 64 bits, y el instalador de códecs de Windows 7 de terceros debe instalar los archivos binarios de 32 y 64 bits en sistemas de 64 bits.

## <a name="multi-threaded-apartment-support-in-wic"></a>Compatibilidad con el apartamento multiproceso en WIC

Cualquier número de subprocesos dentro del MTA puede llamar simultáneamente a los objetos dentro de un apartamento multiproceso (MTA). Esto permite un mejor rendimiento en sistemas de varios núcleos y determinados escenarios de servidor. Además, los códecs WIC de un MTA pueden llamar a otros objetos del MTA sin el costo de cálculo de valores asociado a la llamada entre subprocesos en diferentes departamentos sta. En Windows 7, todos los códecs WIC integrados se han actualizado para admitir MTA, incluidos JPEG, TIFF, PNG, GIF, ICO y BMP. Se recomienda encarecidamente que se escriban códecs de terceros para admitir MTA. Los códecs de terceros que no admiten MTA provocan costos de rendimiento significativos en aplicaciones multiproceso debido a la serialización. La habilitación de la compatibilidad con MTA requiere que se implemente la sincronización adecuada en el códec de terceros. La implementación exacta de estas técnicas de sincronización está fuera del ámbito de este documento. Para obtener más información sobre la sincronización de objetos COM, vea [Understanding and Using COM Threading Models](/previous-versions/ms809971(v=msdn.10)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Introducción (Cómo escribir un códec de WIC-Enabled)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Implementación de un descodificador de WIC-Enabled](-wic-implementingwicdecoder.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Introducción a los metadatos de WIC](-wic-about-metadata.md)
</dt> </dl>

 

 



