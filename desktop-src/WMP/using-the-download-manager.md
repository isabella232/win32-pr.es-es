---
title: Uso del Administrador de descargas
description: Uso del Administrador de descargas
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Reproductor de Windows Media en línea,Download Manager
- online stores,Download Manager
- tipo 2 tiendas en línea, Administrador de descarga
- Reproductor de Windows Media,Download Manager
- Reproductor de Windows Media Administrador de descarga
- Administrador de descarga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476162"
---
# <a name="using-the-download-manager"></a>Uso del Administrador de descargas

El SDK Reproductor de Windows Media incluye una página web de ejemplo que muestra cómo usar el Administrador de descarga para descargar archivos en el equipo del usuario. Puede encontrar el ejemplo en la carpeta denominada WebPage donde instaló el SDK. El nombre del archivo es sample.asp. El ejemplo proporciona la siguiente funcionalidad:

-   Crea el **objeto DownloadManager.**
-   Crea un **objeto DownloadCollection.**
-   Inicia la descarga de cinco archivos cuando el usuario hace clic en **Descargar.** Las rutas de acceso de archivo predeterminadas se proporcionan en el ejemplo. Debe reemplazar estas rutas de acceso predeterminadas por las ubicaciones de los archivos en su propio servidor. Puede cambiar las rutas de acceso cambiando los valores asignados a la matriz global denominada g \_ sFiles.
-   Muestra la información de estado de una descarga cuando el usuario la selecciona.
-   Proporciona controles para pausar, reanudar, cancelar y quitar un elemento de descarga.
-   Mantiene información sobre la descarga de colecciones entre sesiones mediante cookies. Esto es importante porque el usuario puede cerrar el reproductor en cualquier momento. Además, si el usuario cambia los paneles de tareas en el Reproductor, finaliza la sesión de la tienda en línea.
-   Usa la descarga en tiempo real de forma predeterminada. Puede cambiar el comportamiento a la descarga en segundo plano cambiando el valor de la variable denominada g \_ sDLType. La descarga en segundo plano está disponible para su uso con el sistema operativo Microsoft Windows XP.
-   Sincroniza el color de fondo con el color player. Puede usar esta característica para que la tienda en línea cambie de apariencia cuando el usuario elija cambiar el color del reproductor.

En las secciones siguientes se proporciona más información:

-   [Inicialización de la página](initializing-the-page.md)
-   [Iniciar las descargas](starting-the-downloads.md)
-   [Recuperar información de estado](retrieving-status-information.md)
-   [Mantenimiento de la información de sesión](maintaining-session-information.md)
-   [Depuración de la página](debugging-the-page.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para almacenes en línea de tipo 2**](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




