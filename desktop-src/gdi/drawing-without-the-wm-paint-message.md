---
description: Aunque las aplicaciones llevan a cabo la mayoría de las operaciones de dibujo mientras el \_ mensaje de Paint se está procesando, a veces es más eficaz para una aplicación dibujar directamente en una ventana sin depender del mensaje de dibujo de WM \_ .
ms.assetid: 2d015879-58d2-4cbe-b1cc-445f2e8fd316
title: Dibujo sin el mensaje WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66695e85b700de6f62366dedb6fe082f410d4385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908489"
---
# <a name="drawing-without-the-wm_paint-message"></a>Dibujo sin el mensaje de pintura de WM \_

Aunque las aplicaciones llevan a cabo la mayoría de las operaciones de dibujo mientras el mensaje de [**\_ Paint**](wm-paint.md) se está procesando, a veces es más eficaz para una aplicación dibujar directamente en una ventana sin depender del mensaje de **\_ dibujo de WM** . Esto puede ser útil cuando el usuario necesita comentarios inmediatos, como al seleccionar texto y arrastrar o cambiar el tamaño de un objeto. En tales casos, la aplicación normalmente dibuja mientras se procesan los mensajes del mouse o del teclado.

Para dibujar en una ventana sin usar un mensaje de [**\_ dibujo de WM**](wm-paint.md) , la aplicación usa la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para recuperar un contexto de dispositivo de pantalla para la ventana. Con el contexto de dispositivo de pantalla, la aplicación puede dibujar en la ventana y evitar la intrusión en otras ventanas. Cuando la aplicación ha terminado de dibujar, llama a la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) para liberar el contexto de dispositivo de pantalla para que lo usen otras aplicaciones.

Al dibujar sin usar un mensaje de [**\_ dibujo de WM**](wm-paint.md) , la aplicación no suele invalidar la ventana. En su lugar, se dibuja de tal manera que puede restaurar fácilmente la ventana y quitar el dibujo. Por ejemplo, cuando el usuario selecciona texto o un objeto, la aplicación normalmente dibuja la selección invirtiendo lo que ya está en la ventana. La aplicación puede quitar la selección y restaurar el contenido original de la ventana simplemente invirtiendo de nuevo.

La aplicación es responsable de administrar cuidadosamente cualquier cambio que realice en la ventana. En concreto, si una aplicación dibuja una selección y se produce un mensaje de dibujo de [**WM \_**](wm-paint.md) intermedio, la aplicación debe asegurarse de que los dibujos realizados durante el mensaje no dañen la selección. Para evitar esto, muchas aplicaciones quitan la selección, llevan a cabo las operaciones de dibujo habituales y, a continuación, restauran la selección cuando se completa el dibujo.

 

 



