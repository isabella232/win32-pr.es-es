---
description: DirectShow Muestras
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: DirectShow Muestras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87687905d53f91339202af2b08bffa79902e100d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062334"
---
# <a name="directshow-samples"></a>DirectShow Muestras

Los DirectShow se incluyen con el [SDK Windows](https://msdn.microsoft.com/windows/aa904949.aspx). Se encuentran en la ruta de acceso \[ SDK Root Samples Multimedia \] \\ \\ \\ DirectShow.

En la tabla siguiente se enumeran todos los DirectShow ejemplos proporcionados en el SDK Windows. Para obtener instrucciones sobre cómo compilar los ejemplos, consulte la documentación proporcionada en el SDK de Windows.

Si hay documentación adicional para un ejemplo, la primera columna de esta tabla se vincula a ella.




| Muestra | Área | Descripción | Dependencias adicionales | 
|--------|------|-------------|-------------------------|
| <a href="directshow-base-classes.md">DirectShow Clases base</a> | Biblioteca de clases base | Clases y funciones de utilidad de C++ diseñadas para implementar DirectShow filtros. | 
| <a href="amcap-sample.md">Ejemplo de AmCap</a> | Capturar | Aplicación de captura de vídeo. | strmbase.lib | 
| <a href="dvapp-sample.md">Ejemplo de DVApp</a> | Capturar | Aplicación de captura de Vídeo digital (DV). | 
| <a href="playcap-sample.md">Ejemplo de PlayCap</a> | Capturar | Aplicación de captura simple. | 
| <a href="dmo-demo-sample.md">DMO Ejemplo de demostración</a> | DMO | Secuencias datos de audio de un archivo WAV a través de un efecto de audio DMO. | SDK de DirectX | 
| Ejemplo de DVD | DVD | Muestra la reproducción y navegación básicas de DVD, además de características avanzadas como la administración de nivel parental, marcadores, comandos y sincronización de comandos. | 
| <a href="inftee-filter-sample.md">Ejemplo de filtro inftee</a> | Filtros, varios | Implementación de ejemplo del <a href="infinite-pin-tee-filter.md">filtro Infinite Pin Tee.</a> | strmbase.lib | 
| <a href="metronome-filter-sample.md">Ejemplo de filtro de metrónoma</a> | Filtros, varios | Muestra cómo implementar un reloj de referencia. | strmbase.lib | 
| <a href="psi-parser-filter-sample.md">Ejemplo de filtro del analizador de PSI</a> | Filtros, varios | Recibe tablas de información específica del programa (PSI) de un flujo de transporte MPEG-2 y extrae información del programa. | strmbase.lib | 
| <a href="dump-filter-sample.md">Ejemplo de filtro de volcado</a> | Filtros, representador | Escribe muestras de medios que recibe en un archivo de texto. | strmbase.lib | 
| Filtro deVid deVid | Filtros, representador | Filtro de representador de vídeo. | strmbase.lib | 
| <a href="scope-filter-sample.md">Ejemplo de filtro de ámbito</a> | Filtros, representador | Muestra datos de sonido como formas de onda. | strmbase.lib | 
| <a href="async-filter-sample.md">Ejemplo de filtro asincrónico</a> | Filtros, origen | Filtro de lector de archivos que admite la descarga progresiva. | strmbase.lib | 
| <a href="ball-filter-sample.md">Ejemplo de filtro de bola</a> | Filtros, origen | Filtro de origen de vídeo que genera una imagen de una bola de contrabando. | strmbase.lib | 
| <a href="push-source-filters-sample.md">Ejemplo de filtros de origen de inserción</a> | Filtros, origen | Filtros de origen que proporcionan los datos siguientes como secuencia de vídeo: un solo mapa de bits, un conjunto de mapas de bits y una copia de la imagen de escritorio actual. | strmbase.lib | 
| <a href="synth-filter-sample.md">Ejemplo de filtro de Synth</a> | Filtros, origen | Filtro de origen que genera formas de onda de audio. En este ejemplo se muestra la creación de gráficos dinámicos. | strmbase.lib | 
| <a href="ezrgb24-filter-sample.md">Ejemplo de filtro EZRGB24</a> | Filtros, transformación | Filtro de procesamiento de imágenes. | strmbase.lib | 
| <a href="gargle-filter-sample.md">Ejemplo de filtro de Gargle</a> | Filtros, transformación | Filtro de efecto de audio. | strmbase.lib | 
| <a href="wavdest-filter-sample.md">Ejemplo de filtro WavDest</a> | Filtros, transformación | Escribe una secuencia de audio en un archivo WAV. | strmbase.lib | 
| <a href="dmoenum-sample.md">DMOEnum Sample</a> | Varios | Muestra cómo enumerar objetos <a href="directx-media-objects.md">multimedia (DMO) de DirectX.</a> | 
| <a href="mapper-sample.md">Ejemplo del asignador</a> | Varios | Muestra cómo usar el <a href="filter-mapper.md">Asignador de filtros</a> para buscar filtros en el Registro. | 
| Ejemplo de SysEnum | Varios | Muestra cómo usar el <a href="system-device-enumerator.md">enumerador de dispositivos del sistema</a> para enumerar dispositivos y filtros. | 
| <a href="cutscene-sample.md">Ejemplo de CutScene</a> | Reproducción | Reproduce un archivo de vídeo en modo de pantalla completa. | 
| Ejemplo DDrawXCL | Reproducción | Reproduce vídeo en el modo de pantalla completa exclusivo de DirectDraw, mediante la <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>interfaz IDDrawExclModeVideo</strong></a> en el filtro <a href="overlay-mixer-filter.md">Mixer</a> superposición. | 
| Ejemplo de DShowPlayer | Reproducción | Aplicación de reproducción de vídeo. | 
| Ejemplo EVRPlayer | Reproducción | Muestra cómo usar el filtro DirectShow EVR.<blockquote>[!Note]<br />Requiere Windows Vista o posterior.</blockquote><br /><br /> Este ejemplo está disponible en el SDK Windows para Windows Server 2008 o posterior.<br /> | strmbase.lib | 
| Ejemplo texture3D9 | Reproducción | Dibuja vídeo en una superficie de textura de Microsoft DirectX 9.0. | strmbase.lib, SDK de DirectX | 
| <a href="ticker-sample.md">Ejemplo de ticker</a> | VMR-9 | Usa VMR-9 para combinar vídeo y texto. | 
| Ejemplo VMR9Allocator | VMR-9 | Implementa un asignador-presentador personalizado para VMR-9. | strmbase.lib | 
| Ejemplo VMR9Compositor | VMR-9 | Implementa un mezclador personalizado para VMR-9. | 
| <a href="vmrplayer-sample.md">Ejemplo de VMRPlayer</a> | VMR-9 | Usa VMR-9 para combinar uno o dos vídeos en ejecución y una imagen estática. | 
| Ejemplo de marca de agua | VMR-9 | Combina un mapa de bits estático en un vídeo durante la reproducción, mediante VMR-9. | 
| <a href="windowless-sample.md">Ejemplo sin ventanas</a> | VMR-9 | Muestra el modo sin ventanas en VMR-9. | 




 

## <a name="additional-dependencies"></a>Dependencias adicionales

Algunos de los ejemplos se vinculan a DirectShow biblioteca de clases base. Para compilar estos ejemplos, primero debe compilar la biblioteca de clases base. Para obtener más información, [vea DirectShow Base Classes](directshow-base-classes.md). La biblioteca de clases base es necesaria para todos los filtros de ejemplo.

Algunos de los ejemplos también requieren el SDK de DirectX, además del SDK Windows SDK. Para compilar estos ejemplos, debe instalar el SDK de DirectX y establecer la variable de entorno %DXSDK DIR% igual a la ruta \_ de instalación del SDK de DirectX.

Muchos de los ejemplos DirectShow usan un conjunto de encabezados comunes y archivos de código fuente ubicados en el sdk de Directrory \[ Root Samples Multimedia DirectShow \] \\ \\ \\ \\ Common. Si copia una carpeta de ejemplo en otro directorio, asegúrese de copiar también la carpeta Común.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del entorno de compilación](setting-up-the-build-environment.md)
</dt> </dl>

 

 




