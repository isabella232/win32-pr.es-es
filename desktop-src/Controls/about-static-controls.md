---
title: Acerca de los controles estáticos
description: En este tema se describe cómo se usan los controles estáticos.
ms.assetid: 155904e1-a963-496d-9b22-6e95ed0ebd47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064c1814b4f4ed6283b2fe22af06aed107e2c4d2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995671"
---
# <a name="about-static-controls"></a>Acerca de los controles estáticos

Las aplicaciones a menudo usan controles estáticos para etiquetar otros controles o para separar un grupo de controles. Aunque los controles estáticos son ventanas secundarias, no se pueden seleccionar. Por lo tanto, no pueden recibir el foco de teclado y no pueden tener una interfaz de teclado. Un control estático que tiene el \_ estilo SS Notify recibe la entrada del mouse y notifica a la ventana primaria cuando el usuario hace clic en el control o hace doble clic en él. Los controles estáticos pertenecen a la clase de ventana estática.

Aunque los controles estáticos se pueden usar en ventanas superpuestas, emergentes y secundarias, están diseñados para usarse en cuadros de diálogo, en los que el sistema normaliza su comportamiento. Mediante el uso de controles estáticos fuera de los cuadros de diálogo, un desarrollador aumenta el riesgo de que la aplicación se comporte de manera no estándar. Normalmente, un desarrollador usa controles estáticos en cuadros de diálogo o usa el \_ estilo de OWNERDRAW SS para crear controles estáticos personalizados.

Los temas siguientes se describen en esta sección.

-   [Tipos de control estáticos](#static-control-types)
    -   [Control estático de gráficos simple](#simple-graphics-static-control)
    -   [Control estático de texto](#text-static-control)
    -   [Control estático de imagen](#image-static-control)
    -   [Control estático dibujado por el propietario](#owner-drawn-static-control)
-   [Procesamiento de mensajes predeterminados de controles estáticos](#static-control-default-message-processing)

## <a name="static-control-types"></a>Tipos de control estáticos

Hay cuatro tipos de controles estáticos. Cada tipo tiene uno o varios [estilos de control estáticos](static-control-styles.md).

-   [Control estático de gráficos simple](#simple-graphics-static-control)
-   [Control estático de texto](#text-static-control)
-   [Control estático de imagen](#image-static-control)
-   [Control estático dibujado por el propietario](#owner-drawn-static-control)

### <a name="simple-graphics-static-control"></a>Control estático de gráficos simple

Un control estático de gráficos simple muestra un marco o un rectángulo relleno. Un marco puede dibujarse en un número de estilos, incluido negro, gris o blanco. Además, se puede dibujar un marco con un estilo grabado para darle un aspecto tridimensional. Entre los estilos de marco se incluyen SS \_ BLACKFRAME, SS \_ GRAYFRAME, SS \_ WHITEFRAME, SS \_ ETCHEDHORZ, SS \_ ETCHEDVERT y SS \_ ETCHEDFRAME.

Un rectángulo se puede rellenar con color en uno de estos tres estilos: negro, gris o blanco. Estos estilos se definen mediante las constantes SS \_ BLACKRECT, SS \_ GRAYRECT y SS \_ WHITERECT.

Los estilos gráficos no se pueden combinar.

### <a name="text-static-control"></a>Control estático de texto

Un control estático de texto muestra texto en un rectángulo en uno de cinco estilos:

-   alineado a la izquierda sin ajuste de palabra
-   alineado a la izquierda con ajuste de palabra
-   centrado
-   alineado a la derecha
-   simple

Estos estilos se definen mediante las constantes SS \_ LEFTNOWORDWRAP, SS \_ left, SS \_ Center, SS \_ right y SS \_ simple, respectivamente. El sistema reorganiza el texto de estos controles de maneras predefinidas, salvo por el texto "simple", que no se reorganiza.

Una aplicación puede cambiar el texto de un control estático de texto en cualquier momento mediante la función [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) o el mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .

El sistema muestra tanto texto como puede en el control estático y recorta el contenido que no cabe. Para calcular el tamaño adecuado para el control, recupere las métricas de fuente del texto. Para obtener más información sobre fuentes y métricas de fuentes, vea [fuentes y texto](/windows/desktop/gdi/fonts-and-text).

De forma predeterminada, el texto de la ventana de un control estático, como para otros controles, puede contener una y comercial que define el siguiente carácter como tecla de método abreviado para el control (o, en el caso de la mayoría de los controles estáticos, para el control que etiqueta, que es el siguiente control en el orden de tabulación). Si desea mostrar los signos de y comercial en el texto en lugar de usarlos para definir los accesos directos, incluya el \_ estilo SS noprefix.

### <a name="image-static-control"></a>Control estático de imagen

Un control estático de imagen puede mostrar mapas de bits, iconos (incluidos iconos animados) o metaarchivos mejorados. El tipo de gráfico que muestra un control estático determinado depende del estilo del control: SS \_ Bitmap, SS \_ Icon o SS \_ ENHMETAFILE. Una aplicación especifica el estilo cuando crea el control y también especifica un identificador para el mapa de bits, el icono o el metarchivo del control que se va a mostrar. Una vez creado el control, una aplicación puede asociar un gráfico diferente al control mediante el envío de un mensaje [**STM \_ SETIMAGE**](stm-setimage.md) , que especifica un identificador para el nuevo objeto gráfico. Una aplicación puede recuperar un identificador para el objeto gráfico asociado actualmente a un control estático mediante el envío de un mensaje de [**STM \_ GetImage**](stm-getimage.md) . Una aplicación envía mensajes a un control estático mediante la función [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) .

### <a name="owner-drawn-static-control"></a>Owner-Drawn control estático

Al usar el \_ estilo de OWNERDRAW SS, una aplicación puede asumir la responsabilidad de dibujar un control estático. La ventana primaria de un control estático dibujado por el propietario (su propietario) recibe un mensaje de Windows de [**WM \_**](wm-drawitem.md) siempre que es necesario pintar el control estático. El mensaje incluye un puntero a una estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contiene información que la ventana propietaria utiliza al dibujar el control.

## <a name="static-control-default-message-processing"></a>Procesamiento de mensajes predeterminados de controles estáticos

El procedimiento de ventana para la clase de ventana de control estática predefinida realiza el procesamiento predeterminado para todos los mensajes que no procesa el procedimiento de control estático. Cuando el control estático devuelve **false** para cualquier mensaje, el procedimiento de ventana predefinido comprueba los mensajes y realiza la acción predeterminada que se describe en la tabla siguiente. En la tabla, un control estático de texto es un control estático con el estilo SS \_ LEFTNOWORDWRAP, SS \_ left, SS \_ Center, SS \_ right o SS \_ simple.



| Message                                                | Acción predeterminada                                                                                                                              |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**creación de WM \_**](/windows/desktop/winmsg/wm-create)                     | Carga el objeto gráfico y ajusta el tamaño de la ventana al tamaño del objeto, para los controles estáticos gráficos. No realiza ninguna acción para otros controles estáticos. |
| [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)                   | Libera y destruye cualquier objeto gráfico, para los controles estáticos gráficos. No realiza ninguna acción para otros controles estáticos.                              |
| [**\_habilitación de WM**](/windows/desktop/winmsg/wm-enable)                     | Vuelve a dibujar controles estáticos visibles.                                                                                                           |
| [**ERASEBKGND de WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)             | Devuelve **true**, que indica que el control borra el fondo.                                                                             |
| [**GETDLGCODE de WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)             | Devuelve DLGC \_ static.                                                                                                                       |
| [**GETFONT de WM \_**](/windows/desktop/winmsg/wm-getfont)                   | Devuelve un identificador para la fuente de los controles estáticos de texto.                                                                                      |
| [**GETTEXT de WM \_**](/windows/desktop/winmsg/wm-gettext)                   | Devuelve el número de caracteres copiados.                                                                                                    |
| [**GETTEXTLENGTH de WM \_**](/windows/desktop/winmsg/wm-gettextlength)       | Devuelve la longitud, en caracteres, del texto de un control estático de texto.                                                                   |
| [**LBUTTONDBLCLK de WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk)     | Envía a la ventana primaria un código de notificación [STN \_ DBLCLK](stn-dblclk.md) si el estilo de control es SS \_ Notify.                              |
| [**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown)         | Envía a la ventana primaria un código de notificación en el que se [ \_ hizo clic STN](stn-clicked.md) si el estilo de control es SS \_ Notify.                            |
| [**NCLBUTTONDBLCLK de WM \_**](/windows/desktop/inputdev/wm-nclbuttondblclk) | Envía a la ventana primaria un código de notificación [STN \_ DBLCLK](stn-dblclk.md) si el estilo de control es SS \_ Notify.                              |
| [**NCLBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-nclbuttondown)     | Envía a la ventana primaria un código de notificación en el que se [ \_ hizo clic STN](stn-clicked.md) si el estilo de control es SS \_ Notify.                            |
| [**NCHITTEST de WM \_**](/windows/desktop/inputdev/wm-nchittest)             | Devuelve HTCLIENT si el estilo de control es SS \_ NOTIFY; de lo contrario, devuelve HTTRANSPARENT.                                                      |
| [**pintura de WM \_**](/windows/desktop/gdi/wm-paint)                          | Vuelve a dibujar el control.                                                                                                                       |
| [**WM \_**](/windows/desktop/winmsg/wm-setfont)                   | Establece la fuente y los redibujados para los controles estáticos de texto.                                                                                        |
| [**SETTEXT de WM \_**](/windows/desktop/winmsg/wm-settext)                   | Establece el texto y los redibujados para los controles estáticos de texto.                                                                                        |



 

El procedimiento de ventana predefinido pasa todos los demás mensajes a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para el procesamiento predeterminado.

 

 