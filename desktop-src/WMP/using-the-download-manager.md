---
title: Uso del administrador de descargas
description: Uso del administrador de descargas
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419153"
---
# <a name="using-the-download-manager"></a>Uso del administrador de descargas

El SDK de Windows Media Player incluye una página web de ejemplo que muestra cómo usar el administrador de descargas para descargar archivos en el equipo del usuario. Puede encontrar el ejemplo en la carpeta denominada página web en la que instaló el SDK. El nombre del archivo es sample. asp. El ejemplo proporciona la funcionalidad siguiente:

-   Crea el objeto **Downloadmanager** .
-   Crea un objeto **DownloadCollection** .
-   Comienza a descargar cinco archivos cuando el usuario hace clic en **Descargar**. En el ejemplo se proporcionan rutas de acceso de archivo predeterminadas. Debe reemplazar estas rutas de acceso predeterminadas por las ubicaciones de los archivos de su propio servidor. Puede cambiar las rutas de acceso cambiando los valores asignados a la matriz global denominada g \_ sFiles.
-   Muestra información de estado de una descarga cuando el usuario la selecciona.
-   Proporciona controles para pausar, reanudar, cancelar y quitar un elemento de descarga.
-   Mantiene información acerca de las colecciones de descarga entre sesiones mediante cookies. Esto es importante porque el usuario puede cerrar el reproductor en cualquier momento. Además, si el usuario cambia los paneles de tareas en el reproductor, finaliza la sesión de la tienda en línea.
-   Usa la descarga en tiempo real de forma predeterminada. Puede cambiar el comportamiento a la descarga en segundo plano cambiando el valor de la variable denominada g \_ sDLType. La descarga en segundo plano está disponible para su uso con el sistema operativo Microsoft Windows XP.
-   Sincroniza el color de fondo con el color del reproductor. Puede usar esta característica para que la tienda en línea cambie de apariencia cuando el usuario decida cambiar el color del reproductor.

En las secciones siguientes se proporciona más información:

-   [Inicialización de la página](initializing-the-page.md)
-   [Iniciar las descargas](starting-the-downloads.md)
-   [Recuperando información de estado](retrieving-status-information.md)
-   [Mantenimiento de la información de sesión](maintaining-session-information.md)
-   [Depurar la página](debugging-the-page.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para las tiendas en línea de tipo 2**](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




