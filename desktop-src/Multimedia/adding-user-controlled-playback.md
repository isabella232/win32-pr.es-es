---
title: Agregar User-Controlled reproducción
description: Agregar User-Controlled reproducción
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- MCIWndCreate función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651300"
---
# <a name="adding-user-controlled-playback"></a>Agregar User-Controlled reproducción

Puede Agregar la reproducción controlada por el usuario a una aplicación existente llamando a la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) de la siguiente manera:


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



Los parámetros de [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identifican los identificadores de la ventana primaria y la instancia de módulo asociada a la ventana MCIWnd. También especifican los estilos de ventana y el nombre de archivo (o nombre de dispositivo) que se asociarán a la ventana de MCIWnd.

**MCIWndCreate** realiza automáticamente los pasos siguientes que, para otras clases de ventana, implementaría en el código usted mismo:

1.  Registre la clase de ventana MCIWnd.
2.  Cree la ventana de MCIWnd.
3.  Cargar el contenido especificado.
4.  Establecer la posición de reproducción actual al principio del contenido.
5.  Muestra el control de dispositivo.
6.  Muestra el área de reproducción de la ventana, si es necesario.

 

 




