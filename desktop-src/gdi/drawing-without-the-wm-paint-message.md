---
description: Aunque las aplicaciones realizan la mayoría de las operaciones de dibujo mientras se procesa el mensaje WM PAINT, a veces es más eficaz que una aplicación dibuje directamente en una ventana sin depender del \_ mensaje WM \_ PAINT.
ms.assetid: 2d015879-58d2-4cbe-b1cc-445f2e8fd316
title: Dibujar sin el WM_PAINT mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66695e85b700de6f62366dedb6fe082f410d4385
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474338"
---
# <a name="drawing-without-the-wm_paint-message"></a>Dibujar sin el mensaje \_ WM PAINT

Aunque las aplicaciones realizan la mayoría de las operaciones de dibujo mientras se procesa el mensaje [**\_ WM PAINT,**](wm-paint.md) a veces es más eficaz que una aplicación dibuje directamente en una ventana sin depender del **mensaje WM \_ PAINT.** Esto puede ser útil cuando el usuario necesita comentarios inmediatos, como al seleccionar texto y arrastrar o cambiar el tamaño de un objeto. En tales casos, la aplicación normalmente se dibuja al procesar los mensajes del teclado o del mouse.

Para dibujar en una ventana sin usar un mensaje [**\_ WM PAINT,**](wm-paint.md) la aplicación usa la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para recuperar un contexto de dispositivo de visualización para la ventana. Con el contexto del dispositivo de presentación, la aplicación puede dibujar en la ventana y evitar la intrusión en otras ventanas. Cuando la aplicación ha terminado de dibujar, llama a la [**función ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) para liberar el contexto del dispositivo de presentación para que lo usen otras aplicaciones.

Al dibujar sin usar un [**mensaje \_ WM PAINT,**](wm-paint.md) la aplicación normalmente no invalida la ventana. En su lugar, dibuja de tal manera que puede restaurar fácilmente la ventana y quitar el dibujo. Por ejemplo, cuando el usuario selecciona texto o un objeto, la aplicación normalmente dibuja la selección al invertir lo que ya está en la ventana. La aplicación puede quitar la selección y restaurar el contenido original de la ventana simplemente invertiendo de nuevo.

La aplicación es responsable de administrar cuidadosamente los cambios que realiza en la ventana. En concreto, si una aplicación dibuja una selección y se produce un mensaje [**\_ WM PAINT**](wm-paint.md) que interviene, la aplicación debe asegurarse de que cualquier dibujo realizado durante el mensaje no da da error a la selección. Para evitar esto, muchas aplicaciones quitan la selección, realizan operaciones de dibujo habituales y, a continuación, restauran la selección cuando se completa el dibujo.

 

 



