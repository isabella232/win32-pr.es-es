---
title: Características agregadas en el SDK de Windows Media Format 9 series
description: Características agregadas en el SDK de Windows Media Format 9 series
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows Media Format SDK, características
- SDK de Windows Media Format, nuevas características
- SDK de Windows Media Format, lectores sincrónicos
- Windows Media Format SDK, indexación basada en marcos
- SDK de Windows Media Format, códigos de tiempo SMPTE
- SDK de Windows Media Format, filtros de DirectShow
- SDK de Windows Media Format, funcionalidad de escritura de DRM
- SDK de Windows Media Format, receptores de archivo
- Windows Media Format SDK, DirectX video Acceleration (DXVA)
- SDK de Windows Media Format, audio multicanal
- Windows Media Format SDK, marca de agua
- SDK de Windows Media Format, compatibilidad con varios idiomas
- SDK de Windows Media Format, plantillas de conformidad de dispositivos
- SDK de Windows Media Format, enumeraciones de códecs
- SDK de Windows Media Format, exclusión mutua
- Windows Media Format SDK, velocidad de bits múltiple (MBR)
- SDK de Windows Media Format, transcodificación con recompresión inteligente
- SDK de Windows Media Format, recompresión inteligente
- SDK de Windows Media Format, recompresión
- SDK de Windows Media Format, metadatos
- SDK de Windows Media Format, relación de aspecto de píxeles dinámicos
- SDK de Windows Media Format, secuencias de vídeo entrelazadas
- Windows Media Format SDK, codificación de dos pasos
- Windows Media Format SDK, WMStub. lib
- lectores sincrónicos, acerca de
- indexación basada en marcos
- Códigos de tiempo SMPTE, acerca de
- Filtros de DirectShow
- receptores de archivos, mejoras
- audio multicanal, acerca de
- marcas de agua, acerca de
- códecs, enumeraciones
- exclusión mutua, acerca de
- Administración de derechos digitales (DRM), funcionalidad de escritura
- DRM (administración de derechos digitales), funcionalidad de escritura
- Aceleración de vídeo de DirectX (DXVA), acerca de
- DXVA (aceleración de vídeo de DirectX), acerca de
- Advanced Systems Format (ASF), compatibilidad con varios idiomas
- ASF (formato de sistemas avanzados), compatibilidad con varios idiomas
- velocidad de bits múltiple (MBR), acerca de
- MBR (velocidad de varios bits), acerca de
- transcodificación con recompresión inteligente
- recompresión inteligente
- recompresión
- metadatos, SDK de Windows Media Format
- relación de aspecto de píxeles dinámicos
- secuencias de vídeo entrelazadas
- codificación de dos pasos, acerca de
- 2-paso de codificación, acerca de
- WMStub. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca7e39c89220c2c8c4cac6af354eefb77257aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268836"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a>Características agregadas en el SDK de Windows Media Format 9 series

El SDK de Windows Media Format 9 series incorporó muchas mejoras y características. En esta sección se proporciona información general sobre estas características para la ventaja de que los usuarios migran desde una versión anterior del SDK.

## <a name="synchronous-reading"></a>Lectura sincrónica

Puede leer archivos ASF con llamadas sincrónicas. Al leer un archivo sincrónicamente, puede cambiar la configuración del lector mientras lee. Las operaciones sincrónicas de lectura del SDK no proporcionan compatibilidad para leer archivos a través de Internet, pero puede usar la interfaz COM estándar, **IStream**, para leer de orígenes personalizados.

## <a name="frame-based-indexing"></a>Indexación basada en marcos

Puede indexar archivos ASF basados en fotogramas de vídeo. Tanto el lector como el lector sincrónico pueden buscar un fotograma de una secuencia de vídeo y sincronizar el resto de flujos con ese marco.

## <a name="indexing-and-seeking-with-smpte-time-code"></a>Indexación y búsqueda con código de tiempo SMPTE

El SDK de Windows Media Format permite almacenar códigos de tiempo SMPTE en archivos ASF. Los archivos pueden ser indexados por código de tiempo SMPTE, y el lector asincrónico y el lector sincrónico pueden buscar entradas de índice de código de tiempo SMPTE.

## <a name="directshow-filters"></a>Filtros de DirectShow

El SDK de Windows Media Format incluye dos filtros de® de Microsoft DirectShow que permiten a las aplicaciones basadas en DirectShow leer y escribir archivos ASF. DirectShow también permite que las aplicaciones capturen datos de dispositivos de vídeo de audio y descompriman datos de diversos formatos antes de volver a codificarlos como contenido basado en Windows Media.

## <a name="enhanced-profiles"></a>Perfiles mejorados

Los perfiles pueden contener información de uso compartido de ancho de banda e información de priorización de secuencias. El uso compartido de ancho de banda le permite especificar que dos o más secuencias, independientemente de sus velocidades de bits individuales, nunca usarán más de una cantidad de ancho de banda especificada. El ancho de banda que comparte datos en un perfil es meramente informativo; no se aplica a ninguna lógica del SDK. La priorización de flujo le permite especificar un orden de prioridad para las secuencias de un perfil. Si no hay suficiente ancho de banda en la reproducción para transmitir el archivo correctamente, se pueden omitir los flujos de menor prioridad para mejorar el rendimiento.

## <a name="drm-writing-capability"></a>Funcionalidad de escritura de DRM

Además de la compatibilidad con la lectura de DRM existente, el SDK de Windows Media Format 9 series agregó compatibilidad para escribir archivos ASF con la protección DRM versión 1 o DRM versión 7. Esta nueva capacidad permite escenarios de "DRM dinámica", como la difusión por Web de pago por vista de eventos deportivos en directo o conciertos.

## <a name="enhanced-file-sink"></a>Receptor de archivos mejorado

Se han agregado varias funcionalidades nuevas del receptor de archivos a la versión 9 de la serie del SDK. Puede configurar el receptor de archivos para deshabilitar la indexación automática de archivos ASF recién creados. También tiene la opción de configurarla para la entrada y salida no almacenadas en búfer.

## <a name="directx-video-acceleration"></a>Aceleración de vídeo de DirectX

DirectX video Acceleration (DXVA) es una tecnología que permite la reproducción de vídeo de alta velocidad (calidad del DVD o mejor) en máquinas menos eficaces con tarjetas gráficas habilitadas para DXVA. Puede usar el objeto lector de este SDK para habilitar la aceleración de vídeo de DirectX, si el hardware lo admite, al reproducir archivos ASF.

## <a name="multichannel-audio"></a>Audio multicanal

Puede codificar y reproducir audio multicanal. El códec Windows Media Audio 9 Professional admite formatos con 6 canales y 8 canales, así como estéreo de alta definición.

## <a name="watermarking"></a>Agua

Puede codificar archivos ASF con marcas de agua digitales para la seguridad. Todos los sistemas de marca de agua son diferentes en su enfoque, pero toda la identificación de inserción en el contenido codificado. La marca de agua se realiza mediante el uso de objetos multimedia de DirectX® de terceros (DMOs).

## <a name="support-for-multiple-languages-in-asf-files"></a>Compatibilidad con varios idiomas en archivos ASF

Puede admitir varios idiomas en archivos ASF, tanto en secuencias como en metadatos. Por ejemplo, puede crear un archivo de vídeo con secuencias de audio en varios idiomas. En la reproducción, el usuario puede seleccionar el idioma que desea usar o la aplicación puede consultar la información del sistema en el equipo que se está reproduciendo y seleccionar un idioma automáticamente. Los atributos de metadatos también se pueden especificar varias veces, con los valores en diferentes lenguajes.

## <a name="device-conformance-templates"></a>Plantillas de conformidad de dispositivos

Para ayudar a dirigir el contenido a dispositivos cliente específicos, los códecs de Windows Media ahora admiten plantillas de conformidad de dispositivos. Cada plantilla contiene un intervalo definido de opciones de configuración y códecs que deben usarse para medios destinados a una determinada categoría de plataformas. Los perfiles del sistema ya no son compatibles con las versiones más recientes de los códecs de Windows Media. Todos los perfiles deben personalizarse para adaptarse a sus necesidades. Puede usar plantillas de conformidad de dispositivos para ayudarle a diseñar los perfiles.

## <a name="expanded-codec-enumeration"></a>Enumeración de códec expandida

El objeto de administrador de perfiles puede consultar los códecs de Windows Media Audio y vídeo para obtener los formatos admitidos. Puede establecer parámetros para los formatos recuperados. Por ejemplo, puede recuperar todos los formatos de velocidad de bits variables basados en la calidad admitidos por el códec Windows Media Audio 9.

## <a name="improved-mutual-exclusion"></a>Exclusión mutua mejorada

Puede crear registros con nombre que contengan varias secuencias dentro de un objeto de exclusión mutua. También puede asignar nombres a los objetos de exclusión mutua para que sean más fáciles de identificar. Esto le permite crear capas de exclusión mutua. Por ejemplo, un archivo puede contener flujos que se excluyen mutuamente por la velocidad de bits y por lenguaje. La exclusión mutua basada en el lenguaje implicaría grupos de flujos, cada uno de los cuales consta de secuencias en el mismo lenguaje pero que se excluyen mutuamente según la velocidad de bits.

## <a name="expanded-multiple-bit-rate-support"></a>Compatibilidad ampliada con varias velocidades de bits

Se incluye compatibilidad con la exclusión mutua para el audio de velocidad de bits múltiple (MBR) y para vídeo con secuencias de distintos tamaños de imagen.

## <a name="attributes-for-streams"></a>Atributos para secuencias

Puede asignar atributos a flujos individuales en archivos ASF. Todavía debe usar atributos de nivel de archivo para archivos MP3. Esta característica no agrega ningún método al SDK, pero los métodos existentes aceptarán ahora números de secuencia distintos de cero.

## <a name="transcoding-with-smart-recompression"></a>Transcodificación con recompresión inteligente

La recompresión inteligente le permite transcodificar archivos de audio de Windows Media de una velocidad de bits alta a una velocidad de bits más baja con una calidad mejor que la que se podía conseguir.

## <a name="expanded-metadata-support"></a>Compatibilidad ampliada con metadatos

El SDK de Windows Media Format proporciona las siguientes características de metadatos nuevas:

-   Etiquetas de metadatos basadas en índices, que permiten varias etiquetas con el mismo nombre.
-   Capacidad de leer atributos de encabezado DRM sin un archivo WMStubDRM. lib.
-   Atributos con más de 64 kilobytes de datos asociados.
-   Atributos en varios idiomas.
-   Docenas de nuevos atributos predefinidos.

## <a name="dynamic-pixel-aspect-ratio"></a>Relación de aspecto de píxeles dinámicos

Las secuencias de vídeo que se componen de varios tipos de contenido se pueden acomodar mediante la identificación de la relación de aspecto de píxeles de las muestras dispares del flujo. Esto permite que la aplicación de reproducción proporcione una mejor reproducción de dicho contenido.

## <a name="interlaced-video-streams"></a>Secuencias de vídeo entrelazadas

Las versiones anteriores del SDK de Windows Media Format proporcionan la capacidad de codificar contenido [*entrelazado*](wmformat-glossary.md) en una secuencia de vídeo de recorrido progresivo. A partir del SDK de Windows Media Format 9 series, puede codificar vídeo entrelazado a la vez que conserva su formato entrelazado. Esto puede dar lugar a una reproducción mejorada, especialmente en dispositivos entrelazados, como los conjuntos de televisión.

## <a name="two-pass-encoding"></a>Codificación de Two-Pass

Los nuevos códecs de Windows Media permiten la codificación de dos pasos. El contenido codificado en dos pasos puede lograr una salida de mayor calidad.

## <a name="new-speech-codec"></a>Nuevo códec de voz

Este SDK incluye el nuevo códec de voz de Windows Media Audio 9, que está optimizado para codificar la voz humana mientras usa una velocidad de bits baja. Este códec también proporciona un rendimiento superior para el contenido de voz de música mixta.

## <a name="accessible-video-frame-duration"></a>Duración del fotograma de vídeo accesible

Puede hacer que el objeto escritor de este SDK proporcione la duración de los fotogramas de vídeo al lector.

## <a name="streaming-html"></a>Transmisión por secuencias de HTML

Con la versión anterior de este SDK, podía usar un comando de script para indicar a la aplicación que abrira una página web. A partir del SDK de Windows Media Format 9 series, puede almacenar los componentes de las páginas web en los archivos ASF para asegurarse de que no haya ningún retraso en las presentaciones.

## <a name="wmstublib-no-longer-required-for-build-environment"></a>WMStub. lib ya no es necesario para el entorno de compilación

La configuración del entorno de compilación del SDK de Windows Media Format ha cambiado a partir del SDK de Windows Media Format 9 series. Ya no es necesario incluir WMStub. lib para las aplicaciones que usan este SDK. Sin embargo, las aplicaciones habilitadas para DRM todavía deben obtener y firmar un contrato de licencia independiente y obtener una biblioteca estática única de Microsoft. Póngase en contacto con wmla@microsoft.com para obtener más información sobre la biblioteca DRM y el contrato de licencia. Para obtener más información sobre cómo compilar proyectos con este SDK, vea [archivos de biblioteca y configuración del compilador](library-files-and-compiler-settings.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK de Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




