---
title: Acerca de los controles de animación
description: Un control de animación es una ventana que muestra un Audio-Video clip intercalado (AVI). Un clip AVI es una serie de fotogramas de mapa de bits como una película. Los controles de animación solo pueden mostrar clips AVI que no contienen audio.
ms.assetid: 6be69d1a-5b2c-41d5-b6d7-e86ddac2cb0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625828e5f4febce7314da365c9db93ce3a07136
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656431"
---
# <a name="about-animation-controls"></a>Acerca de los controles de animación

Un *control de animación* es una ventana que muestra un Audio-Video clip intercalado (AVI). Un clip AVI es una serie de fotogramas de mapa de bits como una película. Los controles de animación solo pueden mostrar clips AVI que no contienen audio.

Un uso común de un control de animación es indicar la actividad del sistema durante una operación larga. Esto es posible porque el subproceso de la operación continúa ejecutándose mientras se muestra el clip AVI. Por ejemplo, el cuadro de diálogo Buscar del explorador de Windows muestra una lupa en movimiento mientras el sistema busca un archivo.

> [!Note]  
> Si usa ComCtl32.dll versión 6, no se admite el subproceso; Asegúrese de que la aplicación no bloquea la interfaz de usuario o de lo contrario, no se producirá la animación.

 

Un control de animación puede mostrar un clip AVI procedente de un archivo AVI sin comprimir o de un archivo AVI comprimido mediante la codificación de longitud de ejecución ( \_ RLE8 de BI). Puede Agregar el clip AVI a la aplicación como un recurso AVI, o bien el clip puede acompañar a la aplicación como un archivo AVI independiente.

> [!Note]  
> El archivo AVI o el recurso no deben tener un canal de sonido. Las capacidades del control de animación son muy limitadas y están sujetas a cambios. Si necesita un control para proporcionar funciones de reproducción y grabación multimedia para su aplicación, puede usar el control MCIWnd. Para obtener más información, vea [clase de ventana MCIWnd](/windows/desktop/Multimedia/mciwnd-window-class).

 

En esta sección se tratan los temas siguientes.

-   [Creación de controles de animación](#animation-control-creation)
-   [Acerca de los mensajes de control de animación](#about-animation-control-messages)
-   [Procesamiento de mensajes predeterminado](#default-message-processing)

## <a name="animation-control-creation"></a>Creación de controles de animación

Un control de animación pertenece a la clase de ventana [**animar \_ clase**](common-control-window-classes.md) . Puede crear un control de animación mediante las funciones [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , o bien [**animar \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro. La macro coloca el control de animación en la esquina superior izquierda de la ventana primaria y, si no se especifica el estilo del [**\_ centro de ACS**](animation-control-styles.md) , establece el ancho y el alto del control en función de las dimensiones de un fotograma en el clip AVI. Si se especifica **ACS \_ Center** , **animar \_ crear** establece el ancho y el alto del control en cero. Puede utilizar la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para establecer la posición y el tamaño del control.

Si crea un control de animación dentro de un cuadro de diálogo o de un recurso de cuadro de diálogo, el control se destruye automáticamente cuando el usuario cierra el cuadro de diálogo. Si crea un control de animación dentro de una ventana, debe destruir explícitamente el control.

## <a name="about-animation-control-messages"></a>Acerca de los mensajes de control de animación

Una aplicación envía mensajes a un control de animación para abrir, reproducir, detener y cerrar el clip AVI correspondiente. Cada mensaje tiene una o varias macros que puede usar en lugar de enviar el mensaje explícitamente.

Después de crear un control de animación, una aplicación envía el mensaje [**\_ Open de ACM**](acm-open.md) para abrir un clip AVI y cargarlo en la memoria. El mensaje especifica la ruta de acceso de un archivo AVI o el nombre de un recurso AVI. El sistema carga el recurso AVI desde el módulo que creó el control Animation.

Si el control de animación tiene el estilo de [**\_ reproducción automática de ACS**](animation-control-styles.md) , el control comienza a reproducir el clip AVI inmediatamente después de que se abra el archivo AVI o el recurso AVI. De lo contrario, una aplicación puede usar el mensaje [**ACM \_ Play**](acm-play.md) para iniciar el clip AVI. Una aplicación puede detener el clip en cualquier momento enviando el mensaje [**de \_ detención de ACM**](acm-stop.md) . El último fotograma jugado sigue mostrándose cuando el control termina de reproducir el clip AVI o cuando se envía la **\_ detención de ACM** .

Un control de animación puede enviar dos códigos de notificación a su ventana primaria: [ACN \_ Start](acn-start.md) y [ACN \_ Stop](acn-stop.md). La mayoría de las aplicaciones no controlan ninguna notificación.

Para cerrar el archivo AVI o el recurso AVI y quitarlo de la memoria, una aplicación puede usar la macro de [**animación de \_ cierre**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) , que envía [**ACM \_ Open**](acm-open.md) con el nombre de archivo o el nombre de recurso establecido en **null**.

## <a name="default-message-processing"></a>Procesamiento de mensajes predeterminado

En esta sección se describen los mensajes de ventana que se controlan mediante el procedimiento de ventana de la clase de ventana [**Animate \_ Class**](common-control-window-classes.md) .



| Message                                    | Procesamiento realizado                                                                                                                                                                                                                                                                        |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**cierre de WM \_**](/windows/desktop/winmsg/wm-close)           | Libera el archivo AVI o el recurso AVI asociado al control Animation.                                                                                                                                                                                                                   |
| [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)       | Libera el archivo AVI o el recurso AVI, libera una estructura de datos interna y, a continuación, llama a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .                                                                                                                                                |
| [**ERASEBKGND de WM \_**](/windows/desktop/winmsg/wm-erasebkgnd) | Borra el fondo de la ventana utilizando el color de fondo actual para los controles estáticos.                                                                                                                                                                                                        |
| [**NCCREATE de WM \_**](/windows/desktop/winmsg/wm-nccreate)     | Asigna e inicializa una estructura de datos interna y, a continuación, llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).                                                                                                                                                                              |
| [**NCHITTEST de WM \_**](/windows/desktop/inputdev/wm-nchittest) | Devuelve el valor de la prueba de posicionamiento de HTTRANSPARENT.                                                                                                                                                                                                                                                   |
| [**pintura de WM \_**](/windows/desktop/gdi/wm-paint)              | Dibuja un marco AVI en el control de animación.                                                                                                                                                                                                                                                |
| [**tamaño de WM \_**](/windows/desktop/winmsg/wm-size)             | Comprueba si el control tiene el estilo de [**\_ centro de ACS**](animation-control-styles.md) . Si el control no lo hace, llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). De lo contrario, centra la animación en el control, invalida el control y, a continuación, llama a **DefWindowProc**. |



 

 

 