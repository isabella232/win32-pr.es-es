---
title: Aplicaciones de ejemplo del SDK de Windows Media Format
description: Aplicaciones de ejemplo del SDK de Windows Media Format
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- SDK de Windows Media Format, aplicaciones de ejemplo
- Administración de derechos digitales (DRM), aplicaciones de ejemplo
- DRM (administración de derechos digitales), aplicaciones de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ce7a9baf53c289e9420cf3c226bf21a3c6bd16
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488759"
---
# <a name="windows-media-format-sdk-sample-applications"></a>Aplicaciones de ejemplo del SDK de Windows Media Format

El código de ejemplo proporcionado con este SDK está en forma de proyectos para Microsoft Visual Studio 2005. La mayoría de los ejemplos se encuentran en C++, pero ManagedWMFSDKWrapper y ManagedMetadataEdit requieren C#.

Estos ejemplos no funcionarán a menos que se haya instalado el SDK de Windows Media Format o el SDK de Windows Player.

La información de uso de cada ejemplo se encuentra en un archivo readme.txt en cada directorio de ejemplo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Samle</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AudioPlayer</td>
<td>Reproduce archivos de Windows Media, incluidos los archivos protegidos con DRM. Se controla a través de una GUI y los comandos incluyen reproducir, pausar, buscar y detener. Puede reproducir archivos o archivos locales leídos de Internet (incluidos los resultados en Internet mediante el ejemplo WMVNetWrite).
<blockquote>
[!Note]<br />
Las partes DRM de este ejemplo no se admiten en las versiones basadas en x64 de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>DRMHeader</td>
<td>DRMHeader es una aplicación de consola que usa la interfaz <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> del editor de metadatos para leer atributos DRM de archivos sin vincular a la biblioteca estática de DRM.
<blockquote>
[!Note]<br />
Este ejemplo no se admite en las versiones basadas en x64 de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>DRMShow</td>
<td>DRMShow es una aplicación de consola que muestra cómo leer las propiedades <a href="wmformat-glossary.md"><em>DRM</em></a> de un archivo de Windows Media mediante el método <strong>IWMDRMReader:: GetDRMProperty</strong> . En este ejemplo se muestra el uso del método <strong>IWMDRMReader:: GetDRMProperty</strong> y las propiedades que se pueden recuperar del lector DRM. No muestra cómo adquirir una licencia para contenido protegido con DRM. Este ejemplo requiere la compilación de la biblioteca de rutas de DRM WMStubDRM. lib.<br/>
<blockquote>
[!Note]<br />
Este ejemplo no se admite en las versiones basadas en x64 de Windows.
</blockquote>
<br/> Al adquirir WMStubDRM. lib de Microsoft, se asigna a la biblioteca un nivel de seguridad de la aplicación. Si el nivel de seguridad de la biblioteca que recibe no es suficiente para reproducir un archivo protegido, este ejemplo mostrará un error.<br/></td>
</tr>
<tr class="even">
<td>DirectShowInterop/DSCopy</td>
<td>Transcodificar uno o más archivos en un archivo ASF mediante el filtro de escritor ASF de DirectShow. El archivo de entrada puede ser cualquier formato comprimido o sin comprimir compatible con DirectShow.</td>
</tr>
<tr class="odd">
<td>DirectShowInterop/DSPlay</td>
<td>Este ejemplo es un reproductor de archivos multimedia de audio/vídeo interactivo con compatibilidad con <a href="wmformat-glossary.md"><em>DRM</em></a> . Usa el filtro de lector ASF de WM de DirectShow para reproducir archivos de Windows Media (ASF, WMA, WMV) sin protección DRM y archivos que usan DRM en un nivel de 100 o inferior. Consulte readme.txt en el directorio del ejemplo para obtener más información.</td>
</tr>
<tr class="even">
<td>DirectShowInterop/DSSeekFm</td>
<td>En este ejemplo se muestra cómo usar el filtro de lector ASF de DirectShow para reproducir el contenido ASF en un gráfico de filtros de DirectShow y también cómo usar la compatibilidad para buscar fotogramas en el SDK de Windows Media Format.</td>
</tr>
<tr class="odd">
<td>Administrados/WMFSDKWrapper</td>
<td>Este ensamblado administrado actúa como un contenedor que usan los ejemplos de código administrado para tener acceso a algunas interfaces de metadatos de este SDK.</td>
</tr>
<tr class="even">
<td>Administrados/MetadataEdit</td>
<td>Esta aplicación de C# se puede usar para ver y editar metadatos de archivos de Windows Media.</td>
</tr>
<tr class="odd">
<td>MetaDataEdit</td>
<td>Se trata de una versión de C++ de la aplicación MetadataEdit administrada.</td>
</tr>
<tr class="even">
<td>ReadFromStream</td>
<td>Este ejemplo de aplicación de consola muestra cómo leer datos de <strong>IStream</strong> con WMReader. El origen de <strong>IStream</strong> se ha implementado para usar un archivo en el formato de Windows Media (WMA/WMV/ASF).
<blockquote>
[!Note]<br />
En este ejemplo no se muestra cómo procesar los ejemplos de medios que salen de WMReader. Para obtener ejemplos sobre cómo procesar audio y vídeo u otros tipos de muestras multimedia, consulte otros ejemplos, por ejemplo, AudioPlayer, que se incluyen con el SDK de Windows Media Format.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>UncompAVIToWMV</td>
<td>Este ejemplo de aplicación de consola muestra el código necesario para comprimir un archivo AVI en un archivo WMV. Muestra cómo fusionar mediante combinación ejemplos de secuencias de audio y vídeo de varios archivos AVI y combinarlos en secuencias similares o crear una nueva secuencia basada en el perfil de flujo de origen. También se muestra cómo crear un flujo arbitrario, realizar una codificación Multipass, agregar código de tiempo SMPTE y aplicar la protección DRM versión 1.</td>
</tr>
<tr class="even">
<td>WMGenProfile/exe</td>
<td>Este ejemplo se ha actualizado a partir de la versión 7,1. Ahora es una aplicación de diálogo de MFC. En el ejemplo WMGenProfile se muestra el uso de la biblioteca estática WMGenProfile. También sirve como herramienta para la creación de perfiles. Esta herramienta está diseñada para los desarrolladores familiarizados con el formato de Windows Media. La interfaz de usuario no se ha probado para la experiencia del usuario y no está pensada como recomendación sobre cómo presentar esta información a un usuario.</td>
</tr>
<tr class="odd">
<td>WMGenProfile/lib</td>
<td>El ejemplo de biblioteca GenProfile muestra la creación de perfiles. Muestra cómo crear tipos de medios y secuencias para varios tipos de secuencias (audio, vídeo, script, imagen, transferencia de archivos y Web). No se muestra cómo trabajar con perfiles del sistema o cómo convertir perfiles del sistema en perfiles que especifican los códecs de la serie de Windows Media Audio y vídeo 9.</td>
</tr>
<tr class="even">
<td>WMProp</td>
<td>Esta aplicación de consola muestra cómo recuperar atributos mediante el objeto de editor de metadatos y la información de perfil del lector.</td>
</tr>
<tr class="odd">
<td>WMStats</td>
<td>Esta aplicación de consola muestra las estadísticas de lector y escritor. También se pueden usar varias instancias de WMStats simultáneamente en un equipo. Inicie una instancia como servidor para enviar la secuencia a la red y, a continuación, ejecute una segunda instancia como cliente para comprobar que el servidor se está transmitiendo correctamente.</td>
</tr>
<tr class="even">
<td>WMSyncReader</td>
<td>Este ejemplo de aplicación de consola muestra cómo leer un archivo multimedia mediante <strong>IWMSyncReader</strong> sin crear ningún subproceso adicional ni usar devoluciones de llamada. Se han implementado las siguientes características: leer ejemplos comprimidos o descomprimidos<br/> Búsqueda basada en el tiempo<br/> Búsqueda basada en marcos<br/> Origen derivado de <strong>IStream</strong><br/></td>
</tr>
<tr class="odd">
<td>WMVAppend</td>
<td>Esta aplicación de consola toma dos archivos de Windows Media para la entrada e intenta crear un archivo de salida con el contenido de la primera seguido del segundo. En el ejemplo se comparan los perfiles de los dos archivos de entrada para asegurarse de que son lo suficientemente similares para ser anexados. Si no es así, aparece un mensaje de error. Por ejemplo, un mensaje de error se produce cuando un archivo es de solo audio y el segundo es un archivo de audio o vídeo, o cuando dos archivos de audio tienen velocidades de bits diferentes. El ejemplo acepta orígenes de velocidad de bits variable (VBR). Sin embargo, cuando se comparan los perfiles de los dos orígenes de VBR, el ejemplo omite la diferencia de velocidad de bits media porque dos flujos VBR tendrán velocidades de bits medias diferentes aunque se hayan creado con el mismo perfil. WMVAppend no puede comparar la velocidad de bits máxima de las secuencias VBR basadas en la tasa de bits sin restricciones o el nivel de calidad de las secuencias VBR basadas en la calidad, ya que esta información no existe en los archivos de código fuente. Por lo tanto, es responsabilidad del usuario asegurarse de que se crean dos archivos de origen con el mismo perfil. De lo contrario, se puede crear contenido no válido.<br/></td>
</tr>
<tr class="even">
<td>WMVCopy</td>
<td>En este ejemplo se muestra el código necesario para copiar un archivo WMV. Muestra cómo leer y escribir ejemplos comprimidos, leer atributos y scripts de encabezado y modificar atributos de encabezado.</td>
</tr>
<tr class="odd">
<td>WMVNetWrite</td>
<td>Esta aplicación de consola muestra cómo se transmite un archivo de Windows Media a través de Internet. El ejemplo requiere que se especifique un puerto y, a continuación, se puede reproducir el archivo mediante un reproductor.</td>
</tr>
<tr class="even">
<td>WMVRecompress</td>
<td>Esta aplicación de consola muestra cómo volver a comprimir un archivo WMV. Muestra cómo leer ejemplos sin comprimir, escribir ejemplos sin comprimir y realizar la codificación de múltiples pasadas, la salida de varios canales y la recompresión inteligente.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK de Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 





