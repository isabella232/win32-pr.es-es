---
description: DirectShow Muestras
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: DirectShow Muestras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb99271821fcef80b66b379b29bd42de0505011fd47c8dfee208e6f00b007208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821170"
---
# <a name="directshow-samples"></a>DirectShow Muestras

Los DirectShow se incluyen con el [SDK Windows](https://msdn.microsoft.com/windows/aa904949.aspx). Se encuentran en la ruta de acceso \[ SDK Root Samples Multimedia \] \\ \\ \\ DirectShow.

En la tabla siguiente se enumeran todos los DirectShow ejemplos proporcionados en Windows SDK. Para obtener instrucciones sobre cómo compilar los ejemplos, consulte la documentación proporcionada en el SDK de Windows.

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
<td><a href="directshow-base-classes.md">DirectShow Clases base</a></td>
<td>Biblioteca de clases base</td>
<td>Clases y funciones de utilidad de C++ diseñadas para implementar DirectShow filtros.</td>

</tr>
<tr class="even">
<td><a href="amcap-sample.md">Ejemplo de AmCap</a></td>
<td>Capturar</td>
<td>Aplicación de captura de vídeo.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="dvapp-sample.md">Ejemplo de DVApp</a></td>
<td>Capturar</td>
<td>Aplicación de captura de Vídeo digital (DV).</td>

</tr>
<tr class="even">
<td><a href="playcap-sample.md">Ejemplo de PlayCap</a></td>
<td>Capturar</td>
<td>Aplicación de captura simple.</td>

</tr>
<tr class="odd">
<td><a href="dmo-demo-sample.md">DMO Ejemplo de demostración</a></td>
<td>DMO</td>
<td>Secuencias datos de audio de un archivo WAV a través de un efecto de audio DMO.</td>
<td>SDK de DirectX</td>
</tr>
<tr class="even">
<td>Ejemplo de DVD</td>
<td>DVD</td>
<td>Muestra la reproducción y navegación básicas de DVD, además de características avanzadas, como la administración de nivel parental, los marcadores, los comandos y la sincronización de comandos.</td>

</tr>
<tr class="odd">
<td><a href="inftee-filter-sample.md">Ejemplo de filtro inftee</a></td>
<td>Filtros, varios</td>
<td>Implementación de ejemplo del filtro <a href="infinite-pin-tee-filter.md">Tee de pin infinito.</a></td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="metronome-filter-sample.md">Ejemplo de filtro de metrónoma</a></td>
<td>Filtros, varios</td>
<td>Muestra cómo implementar un reloj de referencia.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="psi-parser-filter-sample.md">Ejemplo de filtro del analizador de PSI</a></td>
<td>Filtros, varios</td>
<td>Recibe tablas de información específica del programa (PSI) de un flujo de transporte MPEG-2 y extrae información del programa.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="dump-filter-sample.md">Ejemplo de filtro de volcado</a></td>
<td>Filtros, representador</td>
<td>Escribe los ejemplos multimedia que recibe en un archivo de texto.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td>Filtro DeVid</td>
<td>Filtros, representador</td>
<td>Filtro de representador de vídeo.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="scope-filter-sample.md">Ejemplo de filtro de ámbito</a></td>
<td>Filtros, representador</td>
<td>Muestra los datos de sonido como formas de onda.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="async-filter-sample.md">Ejemplo de filtro asincrónico</a></td>
<td>Filtros, origen</td>
<td>Filtro del lector de archivos que admite la descarga progresiva.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="ball-filter-sample.md">Ejemplo de filtro de bola</a></td>
<td>Filtros, origen</td>
<td>Filtro de origen de vídeo que genera una imagen de una bola de sobresaliendo.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="push-source-filters-sample.md">Ejemplo de filtros de origen de inserción</a></td>
<td>Filtros, origen</td>
<td>Filtros de origen que proporcionan los datos siguientes como secuencia de vídeo: un solo mapa de bits, un conjunto de mapas de bits y una copia de la imagen de escritorio actual.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="synth-filter-sample.md">Ejemplo de filtro de síntesis</a></td>
<td>Filtros, origen</td>
<td>Filtro de origen que genera formas de onda de audio. En este ejemplo se muestra la creación de gráficos dinámicos.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="ezrgb24-filter-sample.md">Ejemplo de filtro EZRGB24</a></td>
<td>Filtros, transformación</td>
<td>Filtro de procesamiento de imágenes.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="gargle-filter-sample.md">Ejemplo de filtro de Gargle</a></td>
<td>Filtros, transformación</td>
<td>Filtro de efecto de audio.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="wavdest-filter-sample.md">Ejemplo de filtro WavDest</a></td>
<td>Filtros, transformación</td>
<td>Escribe una secuencia de audio en un archivo WAV.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="dmoenum-sample.md">DMOEnum Sample</a></td>
<td>Varios</td>
<td>Muestra cómo enumerar objetos <a href="directx-media-objects.md">multimedia DirectX</a> (DDO).</td>

</tr>
<tr class="odd">
<td><a href="mapper-sample.md">Ejemplo del asignador</a></td>
<td>Varios</td>
<td>Muestra cómo usar el <a href="filter-mapper.md">Asignador de filtros</a> para buscar filtros en el Registro.</td>

</tr>
<tr class="even">
<td>Ejemplo de SysEnum</td>
<td>Varios</td>
<td>Muestra cómo usar el <a href="system-device-enumerator.md">enumerador de dispositivos del sistema</a> para enumerar dispositivos y filtros.</td>

</tr>
<tr class="odd">
<td><a href="cutscene-sample.md">Ejemplo de CutScene</a></td>
<td>Reproducción</td>
<td>Reproduce un archivo de vídeo en modo de pantalla completa.</td>

</tr>
<tr class="even">
<td>Ejemplo de DDrawXCL</td>
<td>Reproducción</td>
<td>Reproduce vídeo en el modo de pantalla completa exclusivo de DirectDraw, mediante la interfaz <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a> en el filtro <a href="overlay-mixer-filter.md">overlay Mixer.</a></td>

</tr>
<tr class="odd">
<td>Ejemplo de DShowPlayer</td>
<td>Reproducción</td>
<td>Aplicación de reproducción de vídeo.</td>

</tr>
<tr class="even">
<td>Ejemplo de EVRPlayer</td>
<td>Reproducción</td>
<td>Muestra cómo usar el filtro DirectShow EVR.
<blockquote>
[!Note]<br />
Requiere Windows Vista o posterior.
</blockquote>
<br/> <br/> Este ejemplo está disponible en el SDK Windows para Windows Server 2008 o posterior.<br/></td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td>Ejemplo de Texture3D9</td>
<td>Reproducción</td>
<td>Dibuja vídeo en una superficie de textura de Microsoft DirectX 9.0.</td>
<td>strmbase.lib, SDK de DirectX</td>
</tr>
<tr class="even">
<td><a href="ticker-sample.md">Ejemplo de ticker</a></td>
<td>VMR-9</td>
<td>Usa VMR-9 para combinar vídeo y texto.</td>

</tr>
<tr class="odd">
<td>Ejemplo VMR9Allocator</td>
<td>VMR-9</td>
<td>Implementa un asignador-presentador personalizado para VMR-9.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td>Ejemplo VMR9Compositor</td>
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
<td>Combina un mapa de bits estático en un vídeo durante la reproducción, mediante VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="windowless-sample.md">Ejemplo sin ventanas</a></td>
<td>VMR-9</td>
<td>Muestra el modo sin ventana en VMR-9.</td>

</tr>
</tbody>
</table>



 

## <a name="additional-dependencies"></a>Dependencias adicionales

Algunos de los ejemplos se vinculan a la biblioteca de DirectShow base. Para compilar estos ejemplos, primero debe compilar la biblioteca de clases base. Para obtener más información, [vea DirectShow clases base](directshow-base-classes.md). La biblioteca de clases base es necesaria para todos los filtros de ejemplo.

Algunos de los ejemplos también requieren el SDK de DirectX, además del SDK Windows sdk. Para compilar estos ejemplos, debe instalar el SDK de DirectX y establecer la variable de entorno %DXSDK DIR% igual a la ruta de \_ instalación del SDK de DirectX.

Muchos de los ejemplos DirectShow usan un conjunto de encabezados y archivos de código fuente comunes ubicados en el SDK de Directrory \[ Root Samples Multimedia DirectShow \] \\ \\ \\ \\ Common. Si copia una carpeta de ejemplo en otro directorio, asegúrese de copiar también la carpeta Común.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del entorno de compilación](setting-up-the-build-environment.md)
</dt> </dl>

 

 




