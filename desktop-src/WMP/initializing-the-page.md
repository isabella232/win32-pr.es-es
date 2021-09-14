---
title: Inicialización de la página
description: Inicialización de la página
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Reproductor de Windows Media en línea,Download Manager
- online stores,Download Manager
- tipo 2 tiendas en línea, Administrador de descarga
- Reproductor de Windows Media en línea, inicializar páginas
- tiendas en línea, inicialización de páginas
- tiendas en línea de tipo 2, inicialización de páginas
- Reproductor de Windows Media,Download Manager
- Reproductor de Windows Media Administrador de descarga
- Administrador de descarga
- inicialización de páginas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249608"
---
# <a name="initializing-the-page"></a>Inicialización de la página

Cuando se carga la página web, se ejecuta la función **Init.** Este código recupera primero los datos almacenados en una sesión anterior. Para obtener más información, vea [Mantenimiento de la información de sesión.](maintaining-session-information.md) A continuación, crea **el objeto DownloadManager** y lo almacena en la variable global denominada g \_ oManager.


```C++
g_oManager = external.DownloadManager;

```



A continuación, la función conecta el evento **OnColorChange** a la función denominada **OnAppColor** y, a continuación, llama a la función directamente para inicializar el color de fondo. Vea [Matching the Reproductor de Windows Media Colors](matching-the-windows-media-player-colors.md)(Coincidencia de Reproductor de Windows Media colores).

Por último, la función inicia un temporizador con un intervalo de un segundo e inicializa los cuadros de lista que muestran las colecciones de descarga y los elementos de descarga pendientes. Esto es importante porque es posible que haya habido sesiones en curso la última vez que se cerró la tienda en línea y esta información debe mostrarse de nuevo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del Administrador de descargas**](using-the-download-manager.md)
</dt> </dl>

 

 




