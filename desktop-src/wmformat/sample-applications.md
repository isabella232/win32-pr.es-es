---
title: Windows Aplicaciones de ejemplo del SDK de formato multimedia
description: Windows Aplicaciones de ejemplo del SDK de formato multimedia
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows SDK de formato multimedia, aplicaciones de ejemplo
- administración de derechos digitales (DRM),aplicaciones de ejemplo
- DRM (administración de derechos digitales),aplicaciones de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c778ef1613359f6f3dc6c08d918e32f2f29bade
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475011"
---
# <a name="windows-media-format-sdk-sample-applications"></a>Windows Aplicaciones de ejemplo del SDK de formato multimedia

El código de ejemplo proporcionado con este SDK está en forma de proyectos para Microsoft Visual Studio 2005. La mayoría de los ejemplos están en C++, pero ManagedWMFSDKWrapper y ManagedMetadataEdit requieren C#.

Estos ejemplos no funcionarán a menos que se haya instalado Windows SDK de formato multimedia o Windows Player SDK de Windows Player.

La información de uso de cada ejemplo se encuentra en un archivo readme.txt en cada directorio de ejemplo.




| Samle | Descripción | 
|-------|-------------|
| Audioplayer | Reproduce Windows multimedia, incluidos los archivos protegidos con DRM. Se controla a través de una GUI y los comandos incluyen Reproducir, Pausar, Buscar y Detener. Puede reproducir archivos locales o archivos leídos desde Internet (incluidos los resultados en Internet mediante el ejemplo WMVNetWrite).<blockquote>[!Note]<br />Las partes de DRM de este ejemplo no se admiten en versiones basadas en x64 de Windows.</blockquote><br /> | 
| DRMHeader | DRMHeader es una aplicación de consola que usa la interfaz <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> del editor de metadatos para leer atributos DRM de archivos sin vincular a la biblioteca estática drm.<blockquote>[!Note]<br />Este ejemplo no se admite en versiones basadas en x64 de Windows.</blockquote><br /> | 
| DRMShow | DRMShow es una aplicación de consola que muestra cómo leer las propiedades <a href="wmformat-glossary.md"><em>DRM</em></a> de un archivo Windows Media mediante el método <strong>IWMDRMReader::GetDRMProperty.</strong> En este ejemplo se muestra el uso del método <strong>IWMDRMReader::GetDRMProperty</strong> y las propiedades que se pueden recuperar del lector DRM. No muestra cómo adquirir una licencia para contenido protegido por DRM. Este ejemplo requiere que se compile la biblioteca de códigos auxiliares DE DRM WMStubDRM.lib.<br /><blockquote>[!Note]<br />Este ejemplo no se admite en versiones basadas en x64 de Windows.</blockquote><br /> Cuando adquiere WMStubDRM.lib de Microsoft, a la biblioteca se le asigna un nivel de seguridad de aplicación. Si el nivel de seguridad de la biblioteca que recibe no es suficiente para reproducir un archivo protegido, este ejemplo mostrará un error.<br /> | 
| DirectShowInterop/DSCopy | Transcodifica uno o varios archivos en un archivo ASF mediante el DirectShow WM ASF Writer. El archivo de entrada puede ser cualquier formato comprimido o sin comprimir admitido por DirectShow. | 
| DirectShowInterop/DSPlay | Este ejemplo es un reproductor de archivos multimedia de audio/vídeo interactivo con <a href="wmformat-glossary.md"><em>compatibilidad con DRM.</em></a> Usa el filtro WM ASF Reader de DirectShow para reproducir archivos multimedia de Windows (ASF, WMA, WMV) sin protección DRM y archivos que usan DRM en un nivel de 100 o inferior. Consulte readme.txt en el directorio del ejemplo para obtener más información. | 
| DirectShowInterop/DSSeekFm | En este ejemplo se muestra cómo usar el filtro de lector de ASF de DIRECTSHOW WM para reproducir contenido de ASF en un gráfico de filtros de DirectShow y también cómo usar el marco que busca compatibilidad en el SDK de formato multimedia de Windows. | 
| Managed/WMFSDKWrapper | Este ensamblado administrado actúa como un contenedor que usan los ejemplos de código administrado para acceder a algunas interfaces de metadatos de este SDK. | 
| Managed/MetadataEdit | Esta aplicación de C# se puede usar para ver y editar metadatos desde Windows archivos multimedia. | 
| MetaDataEdit | Se trata de una versión de C++ de la aplicación Managed MetadataEdit. | 
| ReadFromStream | En este ejemplo de aplicación de consola se muestra cómo leer datos de <strong>IStream</strong> con WMReader. El origen de <strong>IStream</strong> se ha implementado para usar un archivo en Windows Media Format (WMA/WMV/ASF).<blockquote>[!Note]<br />En este ejemplo no se muestra cómo procesar los ejemplos multimedia que sale de WMReader. Para obtener ejemplos sobre cómo procesar audio/vídeo u otros tipos de ejemplos multimedia, consulte otros ejemplos, por ejemplo AudioPlayer, que se incluyen con el SDK de formato multimedia de Windows.</blockquote><br /> | 
| UncompAVIToWMV | En este ejemplo de aplicación de consola se muestra el código necesario para comprimir un archivo AVI en un archivo WMV. Muestra cómo combinar ejemplos de secuencias de audio y vídeo de varios archivos AVI y combinar estos en secuencias similares o crear una nueva secuencia basada en el perfil de secuencia de origen. También se muestra cómo crear una secuencia arbitraria, realizar codificación multipass, agregar código de tiempo SMPTE y aplicar protección DRM versión 1. | 
| WMGenProfile/exe | Este ejemplo se ha actualizado desde la versión 7.1. Ahora es una aplicación de cuadro de diálogo MFC. El ejemplo WMGenProfile muestra el uso de la biblioteca estática WMGenProfile. También sirve como herramienta para la creación de perfiles. Esta herramienta está pensada para desarrolladores familiarizados con Windows Media Format. La interfaz de usuario no se ha probado para la experiencia del usuario y no está pensada como una recomendación sobre cómo presentar esta información a un usuario. | 
| WMGenProfile/lib | El ejemplo de biblioteca GenProfile muestra la creación de perfiles. Muestra cómo crear tipos de medios y secuencias para varios tipos de secuencias (audio, vídeo, script, imagen, transferencia de archivos y Web). No muestra cómo trabajar con perfiles del sistema ni cómo convertir perfiles del sistema en perfiles que especifican los códecs de las series Windows Media Audio y Video 9. | 
| WMProp | Esta aplicación de consola muestra cómo recuperar atributos mediante el objeto del editor de metadatos y la información de perfil del lector. | 
| WMStats | Esta aplicación de consola muestra las estadísticas lector y escritor. También se pueden usar varias instancias de WMStats simultáneamente en una máquina. Inicie una instancia como servidor para enviar la secuencia a la red y, a continuación, ejecute una segunda instancia como cliente para comprobar que el servidor está transmitiendo correctamente. | 
| WMSyncReader | En este ejemplo de aplicación de consola se muestra cómo leer un archivo multimedia mediante <strong>IWMSyncReader</strong> sin crear ningún subproceso adicional o usar devoluciones de llamada. Se implementan las siguientes características: Lectura de muestras comprimidas o descomprimidas<br /> Búsqueda basada en tiempo<br /> Búsqueda basada en fotogramas<br />Origen derivado de <strong>IStream</strong><br /> | 
| WMVAppend | Esta aplicación de consola toma dos Windows multimedia para la entrada e intenta crear un archivo de salida con el contenido del primero seguido del segundo. En el ejemplo se comparan los perfiles de los dos archivos de entrada para asegurarse de que son lo suficientemente similares como para anexarse. Si este no es el caso, aparece un mensaje de error. Por ejemplo, se produce un mensaje de error cuando un archivo es solo audio y el segundo es un archivo de audio y vídeo, o cuando dos archivos de audio tienen velocidades de bits diferentes. El ejemplo acepta orígenes de velocidad de bits variable (VBR). Sin embargo, al comparar los perfiles de los dos orígenes de VBR, el ejemplo omite la diferencia de velocidad de bits media porque dos secuencias de VBR tendrán velocidades de bits medias diferentes incluso si se crearon con el mismo perfil. WMVAppend no puede comparar la velocidad de bits máxima de secuencias VBR basadas en velocidad de bits sin restricciones ni el nivel de calidad de las secuencias VBR basadas en calidad, porque esta información no existe en los archivos de origen. Por lo tanto, es responsabilidad del usuario asegurarse de que se crean dos archivos de origen con el mismo perfil. De lo contrario, se puede crear contenido no válido.<br /> | 
| WMVCopy | En este ejemplo se muestra el código necesario para copiar un archivo WMV. Muestra cómo leer y escribir ejemplos comprimidos, leer atributos de encabezado y scripts, y modificar atributos de encabezado. | 
| WMVNetWrite | Esta aplicación de consola muestra cómo se transmite un Windows multimedia a través de Internet. El ejemplo requiere que se especifique un puerto y, a continuación, el archivo se puede reproducir mediante un reproductor. | 
| WMVRecompress | Esta aplicación de consola muestra cómo volver acomprimir un archivo WMV. Muestra la lectura de ejemplos sin comprimir, la escritura de muestras sin comprimir y la codificación de varios pases, la salida de varios canales y la recompresión inteligente. | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 





