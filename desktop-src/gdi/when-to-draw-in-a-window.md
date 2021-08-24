---
description: 'Una aplicación se dibuja en una ventana en varias ocasiones: al crear por primera vez una ventana, al cambiar el tamaño de la ventana, al mover la ventana desde detrás de otra ventana, al minimizar o maximizar la ventana, al mostrar los datos de un archivo abierto y al desplazarse, cambiar o seleccionar una parte de los datos mostrados.'
ms.assetid: 4b5d6842-5707-4884-a55a-e09e342cea46
title: Cuándo dibujar en una ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832f219ad15fa919715b0f6892b73686237e1c3681e298106db3cefc4a8c3ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468095"
---
# <a name="when-to-draw-in-a-window"></a>Cuándo dibujar en una ventana

Una aplicación se dibuja en una ventana en varias ocasiones: al crear por primera vez una ventana, al cambiar el tamaño de la ventana, al mover la ventana desde detrás de otra ventana, al minimizar o maximizar la ventana, al mostrar los datos de un archivo abierto y al desplazarse, cambiar o seleccionar una parte de los datos mostrados.

El sistema administra acciones como mover y cambiar el tamaño de una ventana. Si una acción afecta al contenido de la ventana, el sistema marca la parte afectada de la ventana como lista para actualizarse y, en la siguiente oportunidad, envía un mensaje [**\_ WM PAINT**](wm-paint.md) al procedimiento de ventana de la ventana. El mensaje es una señal a la aplicación para determinar lo que se debe actualizar y para llevar a cabo el dibujo necesario.

La aplicación administra algunas acciones, como mostrar archivos abiertos y seleccionar los datos mostrados. Para estas acciones, una aplicación puede marcar para actualizar la parte de la ventana afectada por la acción, lo que hace que se envíe un [**mensaje DE WM \_ PAINT**](wm-paint.md) en la siguiente oportunidad. Si una acción requiere comentarios inmediatos, la aplicación puede dibujar mientras se realiza la acción, sin esperar a **WM \_ PAINT**. Por ejemplo, una aplicación típica resalta el área que el usuario selecciona en lugar de esperar al siguiente **mensaje \_ WM PAINT** para actualizar el área.

En todos los casos, una aplicación puede dibujarse en una ventana en cuanto se crea. Para dibujar en la ventana, la aplicación debe recuperar primero un identificador en un contexto de dispositivo de presentación para la ventana. Lo ideal es que una aplicación lleve a cabo la mayoría de sus operaciones de dibujo durante el procesamiento de [**mensajes \_ WM PAINT.**](wm-paint.md) En este caso, la aplicación recupera un contexto de dispositivo para mostrar llamando a la [**función BeginPaint.**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) Si una aplicación se dibuja en cualquier otro momento, como desde [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) o durante el procesamiento de mensajes de teclado o mouse, llama a la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para recuperar el controlador de dominio de pantalla.

 

 
