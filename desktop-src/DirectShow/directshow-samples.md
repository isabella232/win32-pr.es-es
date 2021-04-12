---
description: Ejemplos de DirectShow
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: Ejemplos de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f58c10615aaaa4305a30934e32ef9b11efb18c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538061"
---
# <a name="directshow-samples"></a>Ejemplos de DirectShow

Los ejemplos de DirectShow se incluyen con el [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx). Se encuentran en la ruta de acceso de \[ ejemplo raíz de SDK \] \\ \\ DirectShow de multimedia \\ .

En la tabla siguiente se enumeran todos los ejemplos de DirectShow que se proporcionan en el Windows SDK. Para obtener instrucciones sobre cómo compilar los ejemplos, consulte la documentación proporcionada en el Windows SDK.

Si hay documentación adicional para un ejemplo, la primera columna de esta tabla se vincula a ella.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Muestra</th>
<th>Área</th>
<th>Descripción</th>
<th>Dependencias adicionales</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="directshow-base-classes.md">Clases base de DirectShow</a></td>
<td>Biblioteca de clases base</td>
<td>Clases de C++ y funciones de utilidad diseñadas para implementar filtros de DirectShow.</td>

</tr>
<tr class="even">
<td><a href="amcap-sample.md">Ejemplo de AmCap</a></td>
<td>Capturar</td>
<td>Aplicación de captura de vídeo.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="dvapp-sample.md">Ejemplo de DVApp</a></td>
<td>Capturar</td>
<td>Aplicación de captura de vídeo digital (DV).</td>

</tr>
<tr class="even">
<td><a href="playcap-sample.md">Ejemplo de PlayCap</a></td>
<td>Capturar</td>
<td>Aplicación de captura simple.</td>

</tr>
<tr class="odd">
<td><a href="dmo-demo-sample.md">Ejemplo de demostración de DMO</a></td>
<td>DMO</td>
<td>Transmite datos de audio de un archivo WAV a través de un efecto de audio DMO.</td>
<td>SDK de DirectX</td>
</tr>
<tr class="even">
<td>Ejemplo de DVD</td>
<td>DVD</td>
<td>Muestra la reproducción y la navegación básicas de DVD, además de características avanzadas como la administración de nivel parental, marcadores, karaoke y sincronización de comandos.</td>

</tr>
<tr class="odd">
<td><a href="inftee-filter-sample.md">Ejemplo de filtro InfTee</a></td>
<td>Filtros, varios</td>
<td>Implementación de ejemplo del filtro <a href="infinite-pin-tee-filter.md">tee de anclaje infinito</a> .</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="metronome-filter-sample.md">Ejemplo de filtro de metrónomo</a></td>
<td>Filtros, varios</td>
<td>Muestra cómo implementar un reloj de referencia.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="psi-parser-filter-sample.md">Ejemplo de filtro de analizador de PSI</a></td>
<td>Filtros, varios</td>
<td>Recibe tablas de información específica del programa (PSI) de una secuencia de transporte MPEG-2 y extrae información del programa.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="dump-filter-sample.md">Ejemplo de filtro de volcado de memoria</a></td>
<td>Filtros, representador</td>
<td>Escribe los ejemplos de medios recibidos en un archivo de texto.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td>Filtro de SampVid</td>
<td>Filtros, representador</td>
<td>Filtro de representador de vídeo.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="scope-filter-sample.md">Ejemplo de filtro de ámbito</a></td>
<td>Filtros, representador</td>
<td>Muestra datos de sonido como formas de onda.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="async-filter-sample.md">Ejemplo de filtro Async</a></td>
<td>Filtros, origen</td>
<td>Filtro de lector de archivos que admite la descarga progresiva.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="ball-filter-sample.md">Ejemplo de filtro de bola</a></td>
<td>Filtros, origen</td>
<td>Filtro de origen de vídeo que genera una imagen de una bola de rebote.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="push-source-filters-sample.md">Ejemplo de filtros de origen de la instalación</a></td>
<td>Filtros, origen</td>
<td>Filtros de origen que proporcionan los datos siguientes como una secuencia de vídeo: un único mapa de bits, un conjunto de mapas de bits, una copia de la imagen de escritorio actual.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="synth-filter-sample.md">Ejemplo de filtro de sintetizador</a></td>
<td>Filtros, origen</td>
<td>Filtro de origen que genera las ondas de onda de audio. Este ejemplo muestra la generación dinámica de gráficos.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="ezrgb24-filter-sample.md">Ejemplo de filtro EZRGB24</a></td>
<td>Filtros, transformación</td>
<td>Filtro de procesamiento de imágenes.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="gargle-filter-sample.md">Ejemplo de filtro gargle</a></td>
<td>Filtros, transformación</td>
<td>Filtro de efecto de audio.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="wavdest-filter-sample.md">Ejemplo de filtro WavDest</a></td>
<td>Filtros, transformación</td>
<td>Escribe una secuencia de audio en un archivo WAV.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="dmoenum-sample.md">Ejemplo de DMOEnum</a></td>
<td>Varios</td>
<td>Muestra cómo enumerar <a href="directx-media-objects.md">objetos multimedia de DirectX</a> (DMOs).</td>

</tr>
<tr class="odd">
<td><a href="mapper-sample.md">Ejemplo de asignador</a></td>
<td>Varios</td>
<td>Muestra cómo utilizar el <a href="filter-mapper.md">asignador de filtros</a> para buscar filtros en el registro.</td>

</tr>
<tr class="even">
<td>Ejemplo de SysEnum</td>
<td>Varios</td>
<td>Muestra cómo usar el <a href="system-device-enumerator.md">enumerador de dispositivos del sistema</a> para enumerar los dispositivos y los filtros.</td>

</tr>
<tr class="odd">
<td><a href="cutscene-sample.md">Ejemplo de CutScene</a></td>
<td>Reproducción</td>
<td>Reproduce un archivo de vídeo en modo de pantalla completa.</td>

</tr>
<tr class="even">
<td>Ejemplo de DDrawXCL</td>
<td>Reproducción</td>
<td>Reproduce el vídeo en el modo de pantalla completa DirectDraw, mediante la interfaz <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a> en el filtro de <a href="overlay-mixer-filter.md">mezclador de superposición</a> .</td>

</tr>
<tr class="odd">
<td>Ejemplo de DShowPlayer</td>
<td>Reproducción</td>
<td>Aplicación de reproducción de vídeo.</td>

</tr>
<tr class="even">
<td>Ejemplo de EVRPlayer</td>
<td>Reproducción</td>
<td>Muestra cómo usar el filtro EVR de DirectShow.
<blockquote>
[!Note]<br />
Requiere Windows Vista o posterior.
</blockquote>
<br/> <br/> Este ejemplo está disponible en el Windows SDK para Windows Server 2008 o posterior.<br/></td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td>Ejemplo de Texture3D9</td>
<td>Reproducción</td>
<td>Dibuja vídeo en una superficie de textura de Microsoft DirectX 9,0.</td>
<td>strmbase. lib, SDK de DirectX</td>
</tr>
<tr class="even">
<td><a href="ticker-sample.md">Ejemplo de teletipo</a></td>
<td>VMR-9</td>
<td>Usa VMR-9 para mezclar vídeo y texto.</td>

</tr>
<tr class="odd">
<td>Ejemplo de VMR9Allocator</td>
<td>VMR-9</td>
<td>Implementa un asignador personalizado-presentador para la VMR-9.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td>Ejemplo de VMR9Compositor</td>
<td>VMR-9</td>
<td>Implementa un mezclador personalizado para VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="vmrplayer-sample.md">Ejemplo de VMRPlayer</a></td>
<td>VMR-9</td>
<td>Usa VMR-9 para combinar uno o dos vídeos en ejecución y una imagen estática.</td>

</tr>
<tr class="even">
<td>Ejemplo de marca de agua</td>
<td>VMR-9</td>
<td>Combina un mapa de bits estático en un vídeo durante la reproducción mediante la VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="windowless-sample.md">Ejemplo sin ventanas</a></td>
<td>VMR-9</td>
<td>Muestra el modo sin ventanas en VMR-9.</td>

</tr>
</tbody>
</table>



 

## <a name="additional-dependencies"></a>Dependencias adicionales

Algunos de los ejemplos se vinculan a la biblioteca de clases base de DirectShow. Para compilar estos ejemplos, primero debe compilar la biblioteca de clases base. Para obtener más información, vea [clases base de DirectShow](directshow-base-classes.md). La biblioteca de clases base es necesaria para todos los filtros de ejemplo.

Algunos de los ejemplos también requieren el SDK de DirectX, además de los Windows SDK. Para compilar estos ejemplos, debe instalar el SDK de DirectX y establecer la \_ variable de entorno% DXSDK dir% en la ruta de instalación del SDK de DirectX.

Muchos de los ejemplos de DirectShow usan un conjunto de encabezados comunes y archivos de código fuente que se encuentran en el SDK de directrory ejemplos de la \[ raíz de \] \\ \\ multimedia \\ DirectShow \\ Common. Si copia una carpeta de ejemplo en otro directorio, asegúrese de copiar también la carpeta común.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configurar el entorno de compilación](setting-up-the-build-environment.md)
</dt> </dl>

 

 




