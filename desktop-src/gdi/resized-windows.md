---
description: El sistema cambia el tamaño de una ventana cuando el usuario elige comandos de menú de la ventana, como size y Maximize, o cuando la aplicación llama a funciones, como la función SetWindowPos.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Ventanas cambiadas de tamaño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f740191f8b85038f17a687ebc547305f882383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908479"
---
# <a name="resized-windows"></a>Ventanas cambiadas de tamaño

El sistema cambia el tamaño de una ventana cuando el usuario elige comandos de menú de la ventana, como size y Maximize, o cuando la aplicación llama a funciones, como la función [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) . Cuando una ventana cambia de tamaño, el sistema supone que el contenido de la parte expuesta anteriormente de la ventana no se ve afectado y no es necesario volver a dibujarlo. El sistema solo invalida la parte recién expuesta de la ventana, lo que ahorra tiempo cuando la aplicación procesa el mensaje de [**\_ pintura de WM**](wm-paint.md) eventual. En este caso, **la \_ pintura de WM** no se genera cuando se reduce el tamaño de la ventana.

En algunas ventanas, cualquier cambio en el tamaño de la ventana invalida el contenido. Por ejemplo, una aplicación de reloj que adapte la superficie del reloj para ajustarse perfectamente dentro de su ventana debe volver a dibujar el reloj cada vez que la ventana cambie de tamaño. Para obligar al sistema a invalidar todo el área cliente de la ventana cuando se realiza un cambio vertical, horizontal o vertical y horizontal, una aplicación debe especificar el estilo CS \_ VREDRAW o CS \_ HREDRAW, o ambos, al registrar la clase de ventana. Cualquier ventana que pertenezca a una clase de ventana que tenga estos estilos se invalida cada vez que el usuario o la aplicación cambia el tamaño de la ventana.

 

 
