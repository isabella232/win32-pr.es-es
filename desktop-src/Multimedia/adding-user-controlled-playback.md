---
title: Agregar User-Controlled reproducción
description: Agregar User-Controlled reproducción
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- Función MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62d4e4af43be9877ec5bf3fae452e44ae415bc47047448cb65b64ad3446e0b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941823"
---
# <a name="adding-user-controlled-playback"></a>Agregar User-Controlled reproducción

Puede agregar la reproducción controlada por el usuario a una aplicación existente mediante una llamada a la [**función MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) como se muestra a continuación:


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



Los [**parámetros MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identifican los identificadores de la ventana primaria y de la instancia del módulo asociada a la ventana de MCIWnd. También especifican estilos de ventana y el nombre de archivo (o nombre del dispositivo) que se asociará a la ventana MCIWnd.

**MCIWndCreate** realiza automáticamente los pasos siguientes que, para otras clases de ventana, implementaría en el código usted mismo:

1.  Registre la clase de ventana MCIWnd.
2.  Cree la ventana MCIWnd.
3.  Cargue el contenido especificado.
4.  Establezca la posición de reproducción actual al principio del contenido.
5.  Muestra el control de dispositivo.
6.  Muestra el área de reproducción de la ventana, si es necesario.

 

 




