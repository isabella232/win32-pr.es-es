---
title: Características agregadas en el SDK Windows Media Format 9 Series
description: Características agregadas en el SDK Windows Media Format 9 Series
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows SDK de formato multimedia, características
- Windows SDK de formato multimedia, nuevas características
- Windows SDK de formato multimedia, lectores sincrónicos
- Windows SDK de formato multimedia, indexación basada en fotogramas
- Windows SDK de formato multimedia, códigos de tiempo de SMPTE
- Windows SDK de formato multimedia, DirectShow filtros
- Windows SDK de formato multimedia, funcionalidad de escritura de DRM
- Windows SDK de formato multimedia, receptores de archivos
- Windows SDK de formato multimedia, aceleración de vídeo directX (DXVA)
- Windows SDK de formato multimedia, audio multicanal
- Windows SDK de formato multimedia, marca de agua
- Windows SDK de formato multimedia, compatibilidad con varios lenguajes
- Windows SDK de formato multimedia, plantillas de conformidad de dispositivos
- Windows SDK de formato multimedia, enumeraciones de códec
- Windows SDK de formato multimedia, exclusión mutua
- Windows SDK de formato multimedia, velocidad de bits múltiple (MBR)
- Windows SDK de formato multimedia, transcodificación con recompresión inteligente
- Windows SDK de formato multimedia, recompresión inteligente
- Windows SDK de formato multimedia, recompresión
- Windows SDK de formato multimedia, metadatos
- Windows SDK de formato multimedia, relación de aspecto dinámico de píxeles
- Windows SDK de formato multimedia, secuencias de vídeo entrelazadas
- Windows SDK de formato multimedia, codificación de dos pases
- Windows SDK de formato multimedia,WMStub.lib
- lectores sincrónicos, acerca de
- Indexación basada en fotogramas
- Códigos de tiempo de SMPTE, acerca de
- DirectShow filtros
- receptores de archivos, mejoras
- audio multicanal, acerca de
- marca de agua, acerca de
- codecs,enumerations
- exclusión mutua, acerca de
- administración de derechos digitales (DRM), funcionalidad de escritura
- DRM (administración de derechos digitales), funcionalidad de escritura
- Aceleración de vídeo de DirectX (DXVA), acerca de
- DXVA (aceleración de vídeo de DirectX), acerca de
- Formato de sistemas avanzados (ASF), compatibilidad con varios lenguajes
- ASF (formato de sistemas avanzados), compatibilidad con varios idiomas
- velocidad de bits múltiple (MBR), acerca de
- MBR (velocidad de bits múltiple),acerca de
- transcodificación con recompresión inteligente
- recompresión inteligente
- Recompresión
- metadata,Windows SDK de formato multimedia
- relación de aspecto de píxeles dinámicos
- secuencias de vídeo entrelazadas
- codificación de dos pases, acerca de
- Codificación de 2 pases, acerca de
- WMStub.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76dc0f4a8c0b23ba33409039ae7f1d46ada1b3299790ef82fb98b8714f616117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547455"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a>Características agregadas en el SDK Windows Media Format 9 Series

El SDK Windows de la serie Media Format 9 introdujo muchas mejoras y características. En esta sección se proporciona información general sobre esas características para beneficio de los usuarios que migran desde una versión anterior del SDK.

## <a name="synchronous-reading"></a>Lectura sincrónica

Puede leer archivos ASF con llamadas sincrónicas. Al leer un archivo de forma sincrónica, puede cambiar la configuración del lector mientras está leyendo. Las operaciones de lectura sincrónicas del SDK no proporcionan compatibilidad para leer archivos a través de Internet, pero puede usar la interfaz COM estándar, **IStream**, para leer desde orígenes personalizados.

## <a name="frame-based-indexing"></a>Indexación basada en fotogramas

Puede indexar archivos ASF en función de fotogramas de vídeo. Tanto el lector como el lector sincrónico pueden buscar en un fotograma de una secuencia de vídeo y sincronizar las demás secuencias con ese fotograma.

## <a name="indexing-and-seeking-with-smpte-time-code"></a>Indexación y búsqueda con código de tiempo de SMPTE

El SDK Windows media format le permite almacenar códigos de tiempo SMPTE en archivos ASF. Los archivos se pueden indexar mediante código de tiempo SMPTE y tanto el lector asincrónico como el lector sincrónico pueden buscar entradas de índice de código de tiempo SMPTE.

## <a name="directshow-filters"></a>DirectShow Filtros

El SDK Windows Media Format incluye dos filtros de Microsoft DirectShow® que permiten a las DirectShow basadas en aplicaciones leer y escribir archivos ASF. DirectShow permite a las aplicaciones capturar datos de dispositivos de audio y vídeo y descomprimir datos de diversos formatos antes de volver a codificar como contenido basado en Windows multimedia.

## <a name="enhanced-profiles"></a>Perfiles mejorados

Los perfiles pueden contener información de uso compartido de ancho de banda e información de priorización de flujos. El uso compartido de ancho de banda permite especificar que dos o más secuencias, independientemente de sus velocidades de bits individuales, nunca usarán más de una cantidad especificada de ancho de banda. Los datos de uso compartido de ancho de banda en un perfil son meramente informativos. no se aplica por ninguna lógica en el SDK. La priorización de secuencias permite especificar un orden de prioridad para las secuencias de un perfil. Si no hay suficiente ancho de banda en la reproducción para transmitir el archivo correctamente, se pueden omitir las secuencias de prioridad más baja para mejorar el rendimiento.

## <a name="drm-writing-capability"></a>Funcionalidad de escritura de DRM

Además de la compatibilidad existente con la lectura de DRM, el SDK de la serie Windows Media Format 9 agregó compatibilidad para escribir archivos ASF con la versión 1 de DRM o la versión 7 de DRM. Esta nueva funcionalidad permite escenarios de "DRM en directo", como la difusión web de pago por vista de eventos deportivos en directo o conciertos.

## <a name="enhanced-file-sink"></a>Receptor de archivos mejorado

Se agregaron varias nuevas funcionalidades de receptor de archivos a la versión de la serie 9 del SDK. Puede configurar el receptor de archivos para deshabilitar la indexación automática de los archivos ASF recién creados. También tiene la opción de configurarlo para la entrada y salida sin búfer.

## <a name="directx-video-acceleration"></a>Aceleración de vídeo de DirectX

DirectX Video Acceleration (DXVA) es una tecnología que permite la reproducción de vídeo de alta velocidad de bits (calidad de DVD o superior) en máquinas menos eficaces con tarjetas gráficas habilitadas para DXVA. Puede usar el objeto lector de este SDK para habilitar la aceleración de vídeo de DirectX, si el hardware lo admite, al reproducir archivos ASF.

## <a name="multichannel-audio"></a>Audio multicanal

Puede codificar y reproducir audio multicanal. El códec Windows media audio Professional 9 admite formatos con 6 canales y 8 canales, así como estéreo de alta definición.

## <a name="watermarking"></a>Marca de agua

Puede codificar archivos ASF con marcas de agua digitales por motivos de seguridad. Todos los sistemas de marca de agua son diferentes en su enfoque, pero todos insertan la identificación en el contenido codificado. La marca de agua se realiza mediante objetos multimedia especiales de DirectX® (DDO) de terceros.

## <a name="support-for-multiple-languages-in-asf-files"></a>Compatibilidad con varios idiomas en archivos ASF

Puede admitir varios lenguajes en archivos ASF, tanto en secuencias como en metadatos. Por ejemplo, puede crear un archivo de vídeo con secuencias de audio en varios idiomas. En la reproducción, el usuario puede seleccionar el idioma que se va a usar o la aplicación puede consultar la información del sistema en el equipo que se está reproduciendo y seleccionar automáticamente un idioma. Los atributos de metadatos también se pueden especificar varias veces, con los valores en distintos idiomas.

## <a name="device-conformance-templates"></a>Plantillas de conformidad de dispositivos

Para ayudar a dirigir el contenido a dispositivos cliente específicos, los códecs Windows media ahora admiten plantillas de conformidad de dispositivos. Cada plantilla contiene un intervalo definido de configuraciones y características de códec que se deben usar para medios destinados a una categoría determinada de plataformas. Los perfiles del sistema ya no se admiten con las versiones más recientes de los códecs Windows media. Todos los perfiles deben personalizarse para satisfacer sus necesidades. Puede usar plantillas de conformidad de dispositivos para ayudarle a diseñar los perfiles.

## <a name="expanded-codec-enumeration"></a>Enumeración de códec expandida

El objeto del administrador de perfiles puede consultar Windows códecs de audio y vídeo multimedia para ver los formatos admitidos. Puede establecer parámetros para los formatos recuperados. Por ejemplo, puede recuperar todos los formatos de velocidad de bits variable basados en calidad admitidos por el códec Windows Media Audio 9.

## <a name="improved-mutual-exclusion"></a>Exclusión mutua mejorada

Puede crear registros con nombre que contengan varias secuencias dentro de un objeto de exclusión mutua. También puede nombrar objetos de exclusión mutua para que sean más fáciles de identificar. Esto le permite crear capas de exclusión mutua. Por ejemplo, un archivo puede contener secuencias que se excluyen mutuamente por velocidad de bits y por idioma. La exclusión mutua basada en lenguaje implicaría grupos de secuencias, cada grupo compuesto por secuencias en el mismo idioma, pero mutuamente excluyente por velocidad de bits.

## <a name="expanded-multiple-bit-rate-support"></a>Compatibilidad expandida con varias velocidades de bits

La compatibilidad con la exclusión mutua se incluye para el audio de velocidad de bits múltiple (MBR) y para el vídeo con secuencias de distintos tamaños de imagen.

## <a name="attributes-for-streams"></a>Atributos para Secuencias

Puede asignar atributos a secuencias individuales en archivos ASF. Debe seguir utilizando atributos de nivel de archivo para archivos MP3. Esta característica no agrega ningún método al SDK, pero los métodos existentes ahora aceptarán números de secuencia distintos de cero.

## <a name="transcoding-with-smart-recompression"></a>Transcodificación con recompresión inteligente

La recompresión inteligente le permite transcodificar archivos de audio multimedia Windows de una velocidad de bits alta a una velocidad de bits inferior con una mejor calidad de la que se lograba anteriormente.

## <a name="expanded-metadata-support"></a>Compatibilidad con metadatos expandido

El SDK Windows Media Format proporciona las siguientes nuevas características de metadatos:

-   Etiquetas de metadatos basadas en índices, habilitando varias etiquetas con el mismo nombre.
-   Capacidad de leer atributos de encabezado DRM sin un archivo WMStubDRM.lib.
-   Atributos con más de 64 kilobytes de datos asociados.
-   Atributos en varios idiomas.
-   Docenas de atributos predefinidos nuevos.

## <a name="dynamic-pixel-aspect-ratio"></a>Relación de aspecto dinámico de píxeles

Las secuencias de vídeo que se componen de varios tipos de contenido se pueden alojar mediante la identificación de la relación de aspecto de píxeles de las muestras dispares de la secuencia. Esto permite que la aplicación de reproducción proporcione una mejor reproducción de dicho contenido.

## <a name="interlaced-video-streams"></a>Vídeo entrelazado Secuencias

Las versiones anteriores del SDK Windows Media Format han [](wmformat-glossary.md) proporcionado la capacidad de codificar contenido entrelazado en una secuencia de vídeo de examen progresiva. A partir del SDK Windows Media Format 9, puede codificar vídeo entrelazado y conservar su formato entrelazado. Esto puede dar lugar a una reproducción mejorada, especialmente en dispositivos entrelazados, como los conjuntos de televisión.

## <a name="two-pass-encoding"></a>Two-Pass codificación

Los nuevos códecs Windows media habilitan la codificación de dos pases. El contenido codificado en dos pases puede lograr una salida de mayor calidad.

## <a name="new-speech-codec"></a>Nuevo códec de voz

Este SDK incluye el nuevo códec Windows Media Audio 9 Voice, que está optimizado para codificar la voz humana mientras se usa una velocidad de bits baja. Este códec también proporciona un rendimiento superior para el contenido mixto de música y voz.

## <a name="accessible-video-frame-duration"></a>Duración del fotograma de vídeo accesible

Puede hacer que el objeto de escritor de este SDK proporcione al lector la duración de los fotogramas de vídeo.

## <a name="streaming-html"></a>Streaming HTML

Con la versión anterior de este SDK, podía usar un comando de script para indicar a la aplicación que abra una página web. A partir del SDK Windows Media Format 9, puede almacenar los componentes de las páginas web en los archivos ASF para asegurarse de que no haya ningún retraso en las presentaciones.

## <a name="wmstublib-no-longer-required-for-build-environment"></a>WMStub.lib ya no es necesario para el entorno de compilación

La configuración del entorno de compilación para el SDK Windows Media Format ha cambiado a partir del SDK de la serie Windows Media Format 9. Ya no es necesario incluir WMStub.lib para las aplicaciones que usan este SDK. Sin embargo, las aplicaciones habilitadas para DRM todavía deben obtener y firmar un contrato de licencia independiente y obtener una biblioteca estática única de Microsoft. Póngase en wmla@microsoft.com contacto con para obtener más información sobre la biblioteca DRM y el contrato de licencia. Para obtener más información sobre cómo compilar proyectos con este SDK, vea [Archivos de biblioteca y compilador Configuración](library-files-and-compiler-settings.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




