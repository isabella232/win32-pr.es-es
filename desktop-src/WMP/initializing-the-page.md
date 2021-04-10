---
title: Inicialización de la página
description: Inicialización de la página
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player tiendas en línea, inicializar páginas
- tiendas en línea, inicializar páginas
- tipo 2 tiendas en línea, inicializando páginas
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
- inicializar páginas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269077"
---
# <a name="initializing-the-page"></a>Inicialización de la página

Cuando se carga la página web, se ejecuta la función **init** . Este código recupera primero los datos almacenados en una sesión anterior. Para obtener más información, consulte mantenimiento de la [información de sesión](maintaining-session-information.md). Después crea el objeto **Downloadmanager** y lo almacena en la variable global denominada g \_ oManager.


```C++
g_oManager = external.DownloadManager;

```



A continuación, la función conecta el evento **OnColorChange** a la función denominada **OnAppColor** y, a continuación, llama directamente a la función para inicializar el color de fondo. Vea [buscar coincidencias con los colores de Media Player de Windows](matching-the-windows-media-player-colors.md).

Por último, la función inicia un temporizador con un intervalo de un segundo e inicializa los cuadros de lista que muestran las colecciones de descarga pendientes y los elementos de descarga. Esto es importante porque puede haber sesiones en curso la última vez que se cerró la tienda en línea y es necesario volver a mostrar esta información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del administrador de descargas**](using-the-download-manager.md)
</dt> </dl>

 

 




