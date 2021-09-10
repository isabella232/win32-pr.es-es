---
title: Agregar User-Controlled reproducción
description: Agregar User-Controlled reproducción
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- Función MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371942"
---
# <a name="adding-user-controlled-playback"></a>Agregar User-Controlled reproducción

Puede agregar la reproducción controlada por el usuario a una aplicación existente llamando a la [**función MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) como se muestra a continuación:


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



Los [**parámetros MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identifican los identificadores de la ventana primaria y de la instancia del módulo asociada a la ventana de MCIWnd. También especifican estilos de ventana y el nombre de archivo (o nombre del dispositivo) que se asociará a la ventana de MCIWnd.

**MCIWndCreate** realiza automáticamente los pasos siguientes que, para otras clases de ventana, implementaría en el código usted mismo:

1.  Registre la clase de ventana MCIWnd.
2.  Cree la ventana MCIWnd.
3.  Cargue el contenido especificado.
4.  Establezca la posición de reproducción actual al principio del contenido.
5.  Mostrar el control de dispositivo.
6.  Muestra el área de reproducción de la ventana, si es necesario.

 

 




