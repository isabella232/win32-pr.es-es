---
description: 'Una aplicación se dibuja en una ventana en varias ocasiones: cuando se crea una ventana por primera vez, cuando se cambia el tamaño de la ventana, al mover la ventana detrás de otra ventana, al minimizar o maximizar la ventana, cuando se muestran datos de un archivo abierto y al desplazarse, cambiar o seleccionar una parte de los datos mostrados.'
ms.assetid: 4b5d6842-5707-4884-a55a-e09e342cea46
title: Cuándo dibujar en una ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42c8c157de5a591be5ad1a6ad3e319cf83220e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360626"
---
# <a name="when-to-draw-in-a-window"></a>Cuándo dibujar en una ventana

Una aplicación se dibuja en una ventana en varias ocasiones: cuando se crea una ventana por primera vez, cuando se cambia el tamaño de la ventana, al mover la ventana detrás de otra ventana, al minimizar o maximizar la ventana, cuando se muestran datos de un archivo abierto y al desplazarse, cambiar o seleccionar una parte de los datos mostrados.

El sistema administra acciones como mover y cambiar el tamaño de una ventana. Si una acción afecta al contenido de la ventana, el sistema marca la parte afectada de la ventana como lista para actualizar y, en la siguiente oportunidad, envía un mensaje de [**\_ dibujo de WM**](wm-paint.md) al procedimiento de ventana de la ventana de. El mensaje es una señal a la aplicación para determinar qué debe actualizarse y realizar el dibujo necesario.

Algunas acciones son administradas por la aplicación, como Mostrar archivos abiertos y seleccionar los datos mostrados. Para estas acciones, una aplicación puede marcar para actualizar la parte de la ventana afectada por la acción, lo que provoca que se envíe un mensaje de [**\_ pintura de WM**](wm-paint.md) en la siguiente oportunidad. Si una acción requiere comentarios inmediatos, la aplicación puede dibujar mientras se realiza la acción, sin tener que esperar a **WM \_ Paint**. Por ejemplo, una aplicación típica resalta el área que el usuario selecciona en lugar de esperar a que el siguiente mensaje de **\_ dibujo de WM** actualice el área.

En todos los casos, una aplicación puede dibujar en una ventana en cuanto se crea. Para dibujar en la ventana, la aplicación debe recuperar primero un identificador de un contexto de dispositivo de pantalla para la ventana. Idealmente, una aplicación lleva a cabo la mayoría de sus operaciones de dibujo durante el procesamiento de mensajes de la [**\_ pintura de WM**](wm-paint.md) . En este caso, la aplicación recupera un contexto de dispositivo de pantalla mediante una llamada a la función [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) . Si una aplicación se dibuja en cualquier otro momento, por ejemplo, desde [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) o durante el procesamiento de mensajes de teclado o de mouse, llama a la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para recuperar el controlador de dominio de pantalla.

 

 
