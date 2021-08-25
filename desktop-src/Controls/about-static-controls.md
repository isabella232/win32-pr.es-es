---
title: Acerca de los controles estáticos
description: En este tema se describe cómo se usan los controles estáticos.
ms.assetid: 155904e1-a963-496d-9b22-6e95ed0ebd47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa9b77ff7c1357cede494f60c1d345d0eb4b8f5f8cf63ace13176179d385794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922305"
---
# <a name="about-static-controls"></a>Acerca de los controles estáticos

Las aplicaciones suelen usar controles estáticos para etiquetar otros controles o para separar un grupo de controles. Aunque los controles estáticos son ventanas secundarias, no se pueden seleccionar. Por lo tanto, no pueden recibir el foco del teclado y no pueden tener una interfaz de teclado. Un control estático que tiene el estilo SS NOTIFY recibe la entrada del mouse, notificando a la ventana primaria cuando el usuario hace clic o \_ hace doble clic en el control. Los controles estáticos pertenecen a la clase de ventana STATIC.

Aunque los controles estáticos se pueden usar en ventanas superpuestas, emergentes y secundarias, están diseñados para su uso en cuadros de diálogo, donde el sistema normaliza su comportamiento. Al usar controles estáticos fuera de los cuadros de diálogo, un desarrollador aumenta el riesgo de que la aplicación se comporte de forma no estándar. Normalmente, un desarrollador usa controles estáticos en cuadros de diálogo o usa el estilo SS \_ OWNERDRAW para crear controles estáticos personalizados.

En esta sección se tratan los temas siguientes.

-   [Tipos de control estáticos](#static-control-types)
    -   [Control estático de gráficos simples](#simple-graphics-static-control)
    -   [Control estático de texto](#text-static-control)
    -   [Control estático de imagen](#image-static-control)
    -   [Control estático dibujado por el propietario](#owner-drawn-static-control)
-   [Procesamiento de mensajes predeterminado de control estático](#static-control-default-message-processing)

## <a name="static-control-types"></a>Tipos de control estáticos

Hay cuatro tipos de controles estáticos. Cada tipo tiene uno o varios estilos [de control estáticos.](static-control-styles.md)

-   [Control estático de gráficos simples](#simple-graphics-static-control)
-   [Control estático de texto](#text-static-control)
-   [Control estático de imagen](#image-static-control)
-   [Control estático dibujado por el propietario](#owner-drawn-static-control)

### <a name="simple-graphics-static-control"></a>Control estático de gráficos simples

Un control estático gráfico simple muestra un marco o un rectángulo relleno. Un marco se puede dibujar en una serie de estilos, incluidos negro, gris o blanco. Además, se puede dibujar un marco con un estilo grabado para darle una apariencia tridimensional. Los estilos de fotograma incluyen SS \_ BLACKFRAME, SS \_ GRAYFRAME, SS \_ WHITEFRAME, SS \_ ETCHEDHORZ, SS \_ ETCHEDVERT y SS \_ ETCHEDFRAME.

Un rectángulo se puede rellenar con color en uno de los tres estilos: negro, gris o blanco. Estos estilos se definen mediante las constantes SS \_ BLACKRECT, SS \_ GRAYRECT y SS \_ WHITERECT.

Los estilos gráficos no se pueden combinar.

### <a name="text-static-control"></a>Control estático de texto

Un control estático de texto muestra el texto de un rectángulo en uno de los cinco estilos:

-   alineado a la izquierda sin ajuste de línea
-   alineado a la izquierda con ajuste de línea
-   centrado
-   alineado a la derecha
-   simple

Estos estilos se definen mediante las constantes SS \_ LEFTNOWORDWRAP, SS \_ LEFT, SS \_ CENTER, SS RIGHT y \_ SS \_ SIMPLE, respectivamente. El sistema reorganiza el texto de estos controles de maneras predefinidas, excepto el texto "simple", que no se reorganiza.

Una aplicación puede cambiar el texto de un control estático de texto en cualquier momento mediante la [**función SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) o el [**mensaje \_ SETTEXT de WM.**](/windows/desktop/winmsg/wm-settext)

El sistema muestra tanto texto como sea posible en el control estático y recorta lo que no cabe. Para calcular un tamaño adecuado para el control, recupere las métricas de fuente del texto. Para obtener más información sobre las fuentes y las métricas de fuente, vea [Fuentes y texto.](/windows/desktop/gdi/fonts-and-text)

De forma predeterminada, el texto de ventana de un control estático, como para otros controles, puede contener una yand que define el carácter siguiente como tecla de método abreviado para el control (o, en el caso de la mayoría de los controles estáticos, para el control que etiqueta, que es el siguiente control en el orden de tabulación). Si desea mostrar yerras en el texto en lugar de usarlos para definir accesos directos, incluya el estilo \_ NOPREFIX de SS.

### <a name="image-static-control"></a>Control estático de imagen

Un control estático de imagen puede mostrar mapas de bits, iconos (incluidos iconos animados) o metarchivos mejorados. El tipo de gráfico que muestra un control estático determinado depende del estilo del control: SS \_ BITMAP, SS ICON o \_ SS \_ ENHMETAFILE. Una aplicación especifica el estilo cuando crea el control y también especifica un identificador para el mapa de bits, el icono o el metarchivo para que se muestre el control. Una vez creado el control, una aplicación puede asociar un gráfico diferente al control enviándole un mensaje [**\_ SETIMAGE de STM,**](stm-setimage.md) especificando un identificador para el nuevo objeto gráfico. Una aplicación puede recuperar un identificador para el objeto gráfico asociado actualmente a un control estático mediante el envío de un [**mensaje \_ GETIMAGE de STM.**](stm-getimage.md) Una aplicación envía mensajes a un control estático mediante la [**función SendDlgItemMessage.**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea)

### <a name="owner-drawn-static-control"></a>Owner-Drawn static control

Mediante el estilo SS \_ OWNERDRAW, una aplicación puede asumir la responsabilidad de pintar un control estático. La ventana primaria de un control estático dibujado por el propietario (su propietario) recibe un mensaje [**\_ DRAWITEM**](wm-drawitem.md) de WM cada vez que es necesario pintar el control estático. El mensaje incluye un puntero a una [**estructura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contiene información que la ventana de propietario utiliza al dibujar el control.

## <a name="static-control-default-message-processing"></a>Procesamiento de mensajes predeterminado de control estático

El procedimiento de ventana de la clase de ventana de control estático predefinida realiza el procesamiento predeterminado para todos los mensajes que el procedimiento de control estático no procesa. Cuando el control estático devuelve **FALSE para** cualquier mensaje, el procedimiento de ventana predefinido comprueba los mensajes y lleva a cabo la acción predeterminada descrita en la tabla siguiente. En la tabla, un control estático de texto es un control estático con el estilo SS \_ LEFTNOWORDWRAP, SS \_ LEFT, SS \_ CENTER, SS RIGHT o \_ SS \_ SIMPLE.



| Message                                                | Acción predeterminada                                                                                                                              |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                     | Carga el objeto gráfico y tamaños de la ventana según el tamaño del objeto, para los controles estáticos gráficos. No realiza ninguna acción para otros controles estáticos. |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)                   | Libera y destruye cualquier objeto gráfico para los controles estáticos gráficos. No realiza ninguna acción para otros controles estáticos.                              |
| [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)                     | Vuelve a dibujar los controles estáticos visibles.                                                                                                           |
| [**WM \_ ERASEBNDAND**](/windows/desktop/winmsg/wm-erasebkgnd)             | Devuelve **TRUE**, lo que indica que el control borra el fondo.                                                                             |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)             | Devuelve DLGC \_ STATIC.                                                                                                                       |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)                   | Devuelve un identificador a la fuente para los controles estáticos de texto.                                                                                      |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)                   | Devuelve el número de caracteres copiados.                                                                                                    |
| [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength)       | Devuelve la longitud, en caracteres, del texto de un control estático de texto.                                                                   |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)     | Envía a la ventana primaria un [código de notificación \_ DBLCLK de STN](stn-dblclk.md) si el estilo de control es SS \_ NOTIFY.                              |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)         | Envía a la ventana primaria un [código de notificación DE \_ STN CLICKED](stn-clicked.md) si el estilo de control es SS \_ NOTIFY.                            |
| [**WM \_ NCLBUTTONDBLCLK**](/windows/desktop/inputdev/wm-nclbuttondblclk) | Envía a la ventana primaria un [código de notificación \_ DBLCLK de STN](stn-dblclk.md) si el estilo de control es SS \_ NOTIFY.                              |
| [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown)     | Envía a la ventana primaria un [código de notificación DE \_ STN CLICKED](stn-clicked.md) si el estilo de control es SS \_ NOTIFY.                            |
| [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest)             | Devuelve HTCLIENT si el estilo de control es SS \_ NOTIFY; de lo contrario, devuelve HTTRANSPARENT.                                                      |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                          | Vuelve a dibujar el control.                                                                                                                       |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)                   | Establece la fuente y vuelve a dibujar para los controles estáticos de texto.                                                                                        |
| [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)                   | Establece el texto y vuelve a dibujar para los controles estáticos de texto.                                                                                        |



 

El procedimiento de ventana predefinido pasa todos los demás mensajes [**a DefWindowProc para**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) el procesamiento predeterminado.

 

 