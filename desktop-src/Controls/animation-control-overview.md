---
title: Acerca de los controles de animación
description: Un control de animación es una ventana que muestra un Audio-Video clip intercalado (AVI). Un clip AVI es una serie de fotogramas de mapa de bits como una película. Los controles de animación solo pueden mostrar clips AVI que no contengan audio.
ms.assetid: 6be69d1a-5b2c-41d5-b6d7-e86ddac2cb0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a2a579334fe266499884ccf40ad1154b3465ffd301c92643f248ff2664ed4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921795"
---
# <a name="about-animation-controls"></a>Acerca de los controles de animación

Un *control de* animación es una ventana que muestra Audio-Video clip intercalado (AVI). Un clip AVI es una serie de fotogramas de mapa de bits como una película. Los controles de animación solo pueden mostrar clips AVI que no contengan audio.

Un uso común de un control de animación es indicar la actividad del sistema durante una operación larga. Esto es posible porque el subproceso de operación continúa ejecutándose mientras se muestra el clip AVI. Por ejemplo, el cuadro de diálogo Buscar de Windows Explorer muestra una lupa móvil a medida que el sistema busca un archivo.

> [!Note]  
> Si usa la versión ComCtl32.dll 6, no se admite el subproceso; Asegúrese de que la aplicación no bloquea la interfaz de usuario o de lo contrario no se producirá la animación.

 

Un control de animación puede mostrar un clip AVI que se origina en un archivo AVI sin comprimir o desde un archivo AVI que se comprimió mediante la codificación de longitud de ejecución (BI \_ RLE8). Puede agregar el clip AVI a la aplicación como un recurso AVI, o bien el clip puede acompaña a la aplicación como un archivo AVI independiente.

> [!Note]  
> El archivo AVI, o recurso, no debe tener un canal de sonido. Las funcionalidades del control de animación son muy limitadas y están sujetas a cambios. Si necesita un control para proporcionar funcionalidades de reproducción y grabación multimedia para la aplicación, puede usar el control MCIWnd. Para obtener más información, vea [Clase de ventana MCIWnd](/windows/desktop/Multimedia/mciwnd-window-class).

 

En esta sección se de tratan los temas siguientes.

-   [Creación de controles de animación](#animation-control-creation)
-   [Acerca de los mensajes de control de animación](#about-animation-control-messages)
-   [Procesamiento de mensajes predeterminado](#default-message-processing)

## <a name="animation-control-creation"></a>Creación de controles de animación

Un control de animación pertenece a la [**clase de ventana ANIMATE \_ CLASS.**](common-control-window-classes.md) Para crear un control de animación, use [**las funciones CreateWindow,**](/windows/desktop/api/winuser/nf-winuser-createwindowa) [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**Animate \_ Create.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) La macro coloca el control de animación en la esquina superior izquierda de la ventana primaria y, si no se especifica el estilo [**ACS \_ CENTER,**](animation-control-styles.md) establece el ancho y alto del control en función de las dimensiones de un marco en el clip AVI. Si **se especifica ACS \_ CENTER,** **Animate \_ Create** establece el ancho y alto del control en cero. Puede usar la [**función SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para establecer la posición y el tamaño del control.

Si crea un control de animación dentro de un cuadro de diálogo o desde un recurso de cuadro de diálogo, el control se destruye automáticamente cuando el usuario cierra el cuadro de diálogo. Si crea un control de animación dentro de una ventana, debe destruirlo explícitamente.

## <a name="about-animation-control-messages"></a>Acerca de los mensajes de control de animación

Una aplicación envía mensajes a un control de animación para abrir, reproducir, detener y cerrar el clip AVI correspondiente. Cada mensaje tiene una o varias macros que puede usar en lugar de enviar el mensaje explícitamente.

Después de crear un control de animación, una aplicación envía el mensaje OPEN de [**ACM \_**](acm-open.md) para abrir un clip AVI y cargarlo en la memoria. El mensaje especifica la ruta de acceso de un archivo AVI o el nombre de un recurso AVI. El sistema carga el recurso AVI desde el módulo que creó el control de animación.

Si el control de animación tiene el estilo [**\_ ACS AUTOPLAY,**](animation-control-styles.md) el control comienza a reproducir el clip AVI inmediatamente después de abrir el archivo AVI o el recurso AVI. De lo contrario, una aplicación puede usar el [**mensaje \_ ACM PLAY**](acm-play.md) para iniciar el clip avi. Una aplicación puede detener el clip en cualquier momento mediante el envío del [**mensaje STOP \_ de ACM.**](acm-stop.md) El último fotograma reproducido permanece mostrado cuando el control termina de reproducir el clip AVI o cuando se envía **ACM \_ STOP.**

Un control de animación puede enviar dos códigos de notificación a su ventana primaria: [ACN \_ START](acn-start.md) y [ACN \_ STOP.](acn-stop.md) La mayoría de las aplicaciones no controlan ninguna notificación.

Para cerrar el archivo AVI o el recurso AVI y quitarlo de la memoria, una aplicación puede usar la macro [**Animar \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) cerrar, que envía [**ACM \_ OPEN**](acm-open.md) con el nombre de archivo o el nombre del recurso establecido en **NULL.**

## <a name="default-message-processing"></a>Procesamiento de mensajes predeterminado

En esta sección se describen los mensajes de ventana que controla el procedimiento de ventana para la [**clase de ventana ANIMATE \_ CLASS.**](common-control-window-classes.md)



| Message                                    | Procesamiento realizado                                                                                                                                                                                                                                                                        |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close)           | Libera el archivo AVI o el recurso AVI asociado al control de animación.                                                                                                                                                                                                                   |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)       | Libera el archivo AVI o el recurso AVI, libera una estructura de datos interna y, a continuación, llama a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)                                                                                                                                                |
| [**WM \_ ERASEBND**](/windows/desktop/winmsg/wm-erasebkgnd) | Borra el fondo de la ventana con el color de fondo actual para los controles estáticos.                                                                                                                                                                                                        |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)     | Asigna e inicializa una estructura de datos interna y, a continuación, llama [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).                                                                                                                                                                              |
| [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) | Devuelve el valor de la prueba de impacto HTTRANSPARENT.                                                                                                                                                                                                                                                   |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)              | Dibuja un marco AVI en el control de animación.                                                                                                                                                                                                                                                |
| [**TAMAÑO \_ DE WM**](/windows/desktop/winmsg/wm-size)             | Comprueba si el control tiene el [**estilo DE ACS \_ CENTER.**](animation-control-styles.md) Si el control no lo hace, llama [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). De lo contrario, centra la animación en el control , invalida el control y, a continuación, llama **a DefWindowProc**. |



 

 

 