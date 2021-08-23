---
description: El sistema cambia el tamaño de una ventana cuando el usuario elige comandos de menú de ventana, como Tamaño y Maximizar, o cuando la aplicación llama a funciones, como la función SetWindowPos.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Cambio de tamaño Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efd6f71d1657c0d01b3df9101fc15fa35f54ecfc01b1588b696cd9110dad317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602725"
---
# <a name="resized-windows"></a>Cambio de tamaño Windows

El sistema cambia el tamaño de una ventana cuando el usuario elige comandos de menú de ventana, como Tamaño y Maximizar, o cuando la aplicación llama a funciones, como la [**función SetWindowPos.**](/windows/win32/api/winuser/nf-winuser-setwindowpos) Cuando una ventana cambia de tamaño, el sistema asume que el contenido de la parte expuesta anteriormente de la ventana no se ve afectado y no es necesario volver a dibujarlo. El sistema invalida solo la parte recién expuesta de la ventana, lo que ahorra tiempo cuando la aplicación procesa el mensaje [**WM \_ PAINT**](wm-paint.md) final. En este caso, **WM \_ PAINT** no se genera cuando se reduce el tamaño de la ventana.

En algunas ventanas, cualquier cambio en el tamaño de la ventana invalida el contenido. Por ejemplo, una aplicación de reloj que adapte la cara del reloj para que quepa perfectamente dentro de su ventana debe volver a dibujar el reloj cada vez que la ventana cambie de tamaño. Para forzar que el sistema invalide todo el área cliente de la ventana cuando se realiza un cambio vertical, horizontal o vertical y horizontal, una aplicación debe especificar el estilo CS DRAWDRAW o HREDRAW de CS, o ambos, al registrar la clase de \_ \_ ventana. Cualquier ventana que pertenezca a una clase de ventana que tenga estos estilos se invalida cada vez que el usuario o la aplicación cambian el tamaño de la ventana.

 

 
