---
description: El sistema cambia el tamaño de una ventana cuando el usuario elige comandos de menú de ventana, como Tamaño y Maximizar, o cuando la aplicación llama a funciones, como la función SetWindowPos.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Cambio de tamaño Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f740191f8b85038f17a687ebc547305f882383
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072463"
---
# <a name="resized-windows"></a>Cambio de tamaño Windows

El sistema cambia el tamaño de una ventana cuando el usuario elige comandos de menú de ventana, como Tamaño y Maximizar, o cuando la aplicación llama a funciones, como la [**función SetWindowPos.**](/windows/win32/api/winuser/nf-winuser-setwindowpos) Cuando una ventana cambia de tamaño, el sistema asume que el contenido de la parte expuesta anteriormente de la ventana no se ve afectado y no es necesario volver a dibujarlo. El sistema invalida solo la parte recién expuesta de la ventana, lo que ahorra tiempo cuando la aplicación procesa el mensaje [**WM \_ PAINT**](wm-paint.md) final. En este caso, **WM \_ PAINT** no se genera cuando se reduce el tamaño de la ventana.

En algunas ventanas, cualquier cambio en el tamaño de la ventana invalida el contenido. Por ejemplo, una aplicación de reloj que adapte la cara del reloj para que quepa perfectamente dentro de su ventana debe volver a dibujar el reloj cada vez que la ventana cambie de tamaño. Para forzar que el sistema invalide todo el área cliente de la ventana cuando se realiza un cambio vertical, horizontal o vertical y horizontal, una aplicación debe especificar el estilo \_ CS DRAWDRAW o CS HREDRAW, o ambos, al registrar la clase de \_ ventana. Cualquier ventana que pertenezca a una clase de ventana que tenga estos estilos se invalida cada vez que el usuario o la aplicación cambian el tamaño de la ventana.

 

 
