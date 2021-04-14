---
description: Aplicaciones de DVD
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: Aplicaciones de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acaddc683078acff84b7c90689f82becfb7b1d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359969"
---
# <a name="dvd-applications"></a>Aplicaciones de DVD

DirectShow proporciona un componente denominado filtro de origen de [DVD Navigator](dvd-navigator-filter.md) que simplifica las tareas de navegación por DVD en C++. El navegador de DVD tiene todas las capacidades que se encuentran en un reproductor de DVD independiente, además de otras funciones específicas para la reproducción de DVD en equipos personales. Con el explorador de DVD, los desarrolladores de C++ y de scripting pueden crear aplicaciones de DVD completas sin hacer referencia a la especificación de DVD. El navegador del DVD, en coordinación con los filtros del descodificador, también controla la administración regional y la protección de los derechos de autor (CSS y la protección de la copia analógica), aislando a los desarrolladores de aplicaciones de estos detalles.

El filtro del explorador de DVD funciona en todo un volumen de DVD-Video, que consta de los archivos del directorio de vídeo de \_ TS. A diferencia de la mayoría de los filtros de origen de DirectShow que funcionan con secuencias o archivos individuales, el navegador de DVD utiliza la estructura de DVD-Video de títulos, capítulos y códigos de hora. Los desarrolladores que deseen reproducir archivos MPEG-2 individuales en DirectShow deben usar el [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) en lugar del filtro del navegador de DVD. Para obtener más información [, consulte compatibilidad con MPEG-2 en DirectShow](mpeg-2-support-in-directshow.md) .

> [!Note]  
> Para reproducir DVDs, el usuario debe tener un descodificador MPEG-2.

 

Esta sección contiene los temas siguientes.

-   [Características de compatibilidad con DVD en DirectShow](dvd-support-features-in-directshow.md)
-   [Conceptos básicos de DVD](dvd-basics.md)
-   [Creación del gráfico de filtros de DVD](building-the-dvd-filter-graph.md)
-   [Obtener los punteros de interfaz de DVD](obtaining-the-dvd-interface-pointers.md)
-   [Comandos de DVD](dvd-commands.md)
-   [Identificación de las operaciones de DVD válidas](identifying-valid-dvd-operations.md)
-   [Sincronizar comandos de DVD](synchronizing-dvd-commands.md)
-   [Flujo de datos en el navegador de DVD](data-flow-in-the-dvd-navigator.md)
-   [Control de las notificaciones de eventos de DVD](handling-dvd-event-notifications.md)
-   [Trabajar con menús de DVD](working-with-dvd-menus.md)
-   [Secuencias de audio y subimagen](audio-and-subpicture-streams.md)
-   [Aplicar niveles de administración parental](enforcing-parental-management-levels.md)
-   [Guardar y restaurar objetos DvdState](saving-and-restoring-dvdstate-objects.md)
-   [Trabajar con cadenas de texto de DVD](working-with-dvd-text-strings.md)
-   [Reproducir flujos de audio de karaoke](playing-karaoke-audio-streams.md)
-   [Control de expulsaciones de disco](handling-disc-ejections.md)
-   [Mejoras en la reproducción de DVD en Windows Vista](dvd-playback-enhancements-in-windows-vista.md)
-   [Configuración del gráfico de filtros de DVD](dvd-filter-graph-configuration.md)
-   [Accesos directos a páginas de referencia de DVD de C++](shortcuts-to-c-dvd-reference-pages.md)

Para obtener referencias sobre el desarrollo de descodificadores de DVD/MPEG2, consulte [desarrollo de descodificadores de DVD en DirectShow](dvd-decoder-development-in-directshow.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar DirectShow](using-directshow.md)
</dt> </dl>

 

 



