---
description: Aplicaciones de DVD
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: Aplicaciones de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d601fdbf94ef2a2d9a70d1f28f68854200b58f9fb44d23c3738994f3001e3a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102965"
---
# <a name="dvd-applications"></a>Aplicaciones de DVD

DirectShow proporciona un componente denominado filtro de origen [DVD Navigator](dvd-navigator-filter.md) que simplifica las tareas de navegación de DVD en C++. DVD Navigator tiene todas las funcionalidades que se encuentran en un reproductor de DVD independiente completo, además de funcionalidades adicionales específicas para reproducir DVD en equipos personales. Con el navegador de DVD, C++ y los desarrolladores de scripting pueden crear aplicaciones de DVD con todas las características sin hacer referencia a la especificación de DVD. DVD Navigator, en coordinación con los filtros de descodificador, también controla la administración regional y la protección de copyright (CSS y protección de copia análoga), aislando a los desarrolladores de aplicaciones de estos detalles.

El filtro DVD Navigator funciona en todo DVD-Video volumen, que consta de los archivos del directorio VIDEO \_ TS. A diferencia DirectShow la mayoría de los filtros de origen que funcionan con secuencias o archivos individuales, el navegador de DVD usa la estructura DVD-Video de títulos, capítulos y códigos de tiempo. Los desarrolladores que quieran reproducir archivos MPEG-2 individuales en DirectShow deben usar el [demultiplexor MPEG-2](mpeg-2-demultiplexer.md) en lugar del filtro DVD Navigator. Consulte [Compatibilidad con MPEG-2 en DirectShow](mpeg-2-support-in-directshow.md) para obtener más información.

> [!Note]  
> Para reproducir DVD, el usuario debe tener un descodificador MPEG-2.

 

Esta sección contiene los temas siguientes.

-   [Características de compatibilidad de DVD en DirectShow](dvd-support-features-in-directshow.md)
-   [Conceptos básicos de DVD](dvd-basics.md)
-   [Creación del filtro de DVD Graph](building-the-dvd-filter-graph.md)
-   [Obtención de los punteros de interfaz de DVD](obtaining-the-dvd-interface-pointers.md)
-   [Comandos de DVD](dvd-commands.md)
-   [Identificación de operaciones de DVD válidas](identifying-valid-dvd-operations.md)
-   [Sincronizar comandos de DVD](synchronizing-dvd-commands.md)
-   [Data Flow en el navegador de DVD](data-flow-in-the-dvd-navigator.md)
-   [Control de notificaciones de eventos de DVD](handling-dvd-event-notifications.md)
-   [Trabajar con menús de DVD](working-with-dvd-menus.md)
-   [Audio y subpicture Secuencias](audio-and-subpicture-streams.md)
-   [Aplicación de los niveles de administración parental](enforcing-parental-management-levels.md)
-   [Guardar y restaurar objetos DvdState](saving-and-restoring-dvdstate-objects.md)
-   [Trabajar con cadenas de texto de DVD](working-with-dvd-text-strings.md)
-   [Reproducir audio de audio Secuencias](playing-karaoke-audio-streams.md)
-   [Control de las eyección de disco](handling-disc-ejections.md)
-   [Mejoras de reproducción de DVD en Windows Vista](dvd-playback-enhancements-in-windows-vista.md)
-   [Configuración del filtro de DVD Graph DVD](dvd-filter-graph-configuration.md)
-   [Accesos directos a páginas de referencia de DVD de C++](shortcuts-to-c-dvd-reference-pages.md)

Para obtener referencias sobre el desarrollo del descodificador DE DVD/MPEG2, consulte Desarrollo del [descodificador de DVD DirectShow](dvd-decoder-development-in-directshow.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DirectShow](using-directshow.md)
</dt> </dl>

 

 



