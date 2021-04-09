---
title: Responder a clics del mouse
description: Responder a clics del mouse
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149263"
---
# <a name="responding-to-mouse-clicks"></a>Responder a clics del mouse

Si el usuario hace clic en un botón del mouse mientras el cursor está sobre el área cliente de una ventana, la ventana recibe uno de los mensajes siguientes.



| Mensaje                                        | Significado                   |
|------------------------------------------------|---------------------------|
| [**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown) | Botón primario abajo          |
| [**LBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-lbuttonup)     | Botón primario arriba            |
| [**MBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-mbuttondown) | Botón central abajo        |
| [**MBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-mbuttonup)     | Botón central arriba          |
| [**RBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-rbuttondown) | Botón derecho abajo         |
| [**RBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-rbuttonup)     | Botón derecho arriba           |
| [**XBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-xbuttondown) | XBUTTON1 o XBUTTON2 abajo |
| [**XBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-xbuttonup)     | XBUTTON1 o XBUTTON2 up   |



 

Recuerde que el área cliente es la parte de la ventana que excluye el marco. Para obtener más información acerca de las áreas de cliente, consulte [¿Qué es una ventana?](what-is-a-window-.md)

### <a name="mouse-coordinates"></a>Coordenadas del mouse

En todos estos mensajes, el parámetro *lParam* contiene las coordenadas x e y del puntero del mouse. Los 16 bits más bajos de *lParam* contienen la coordenada x y los 16 bits siguientes contienen la coordenada y. Use las macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para desempaquetar las coordenadas de *lParam*.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Estas macros se definen en el archivo de encabezado WindowsX. h.

En Windows de 64 bits, *lParam* es un valor de 64 bits. No se usan los 32 superiores de *lParam* . La documentación de MSDN menciona la "palabra de orden inferior" y la "palabra de orden superior" de *lParam*. En el caso de 64 bits, esto significa que las palabras de orden inferior y superior de los 32 bits inferiores. Las macros extraen los valores correctos, por lo que, si los usa, estará seguro.

Las coordenadas del mouse se proporcionan en píxeles, no en píxeles independientes del dispositivo (DIP) y se miden en relación con el área cliente de la ventana. Las coordenadas son valores con signo. Las posiciones situadas encima y a la izquierda del área cliente tienen coordenadas negativas, lo que es importante si realiza el seguimiento de la posición del mouse fuera de la ventana. Veremos cómo hacerlo en un tema posterior, [capturando el movimiento del mouse fuera de la ventana](mouse-movement.md).

### <a name="additional-flags"></a>Marcas adicionales

El parámetro *wParam* contiene **una operación OR bit a bit** de marcas, que indica el estado de los demás botones del mouse más las teclas Mayús y Ctrl.



| Marca             | Significado                          |
|------------------|----------------------------------|
| **MK ( \_ control)**  | La tecla CTRL está presionada.            |
| **MK \_ LBUTTON**  | El botón primario del mouse está inactivo.   |
| **MK \_ MBUTTON**  | El botón central del mouse está presionado. |
| **MK \_ RBUTTON**  | El botón secundario del mouse está inactivo.  |
| **\_MAYÚS MK**    | La tecla Mayús está presionada.           |
| **MK \_ XBUTTON1** | El botón XBUTTON1 está inactivo.     |
| **MK \_ XBUTTON2** | El botón XBUTTON2 está inactivo.     |



 

La ausencia de una marca significa que no se presionó el botón o la tecla correspondiente. Por ejemplo, para comprobar si la tecla CTRL está presionada:


```C++
if (wParam & MK_CONTROL) { ...
```



Si necesita buscar el estado de otras teclas además de CTRL y Mayús, use la función [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) , que se describe en [entrada de teclado](keyboard-input.md).

Los mensajes de la ventana de [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) y [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) se aplican tanto a XBUTTON1 como a XBUTTON2. El parámetro *wParam* indica en qué botón se hizo clic.


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a>Doble clics

De forma predeterminada, una ventana no recibe notificaciones de doble clic. Para recibir doble clic, establezca la marca **CS \_ DBLCLKS** en la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) al registrar la clase de ventana.


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



Si establece la marca **CS \_ DBLCLKS** como se muestra, la ventana recibirá notificaciones de doble clic. Un clic doble se indica mediante un mensaje de ventana con "DBLCLK" en el nombre. Por ejemplo, al hacer doble clic en el botón primario del mouse, se genera la siguiente secuencia de mensajes:

<dl>

[**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown)  
[**LBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-lbuttonup)  
[**LBUTTONDBLCLK de WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk)  
[**LBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

En efecto, el segundo mensaje de [**\_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown) que se generaría normalmente se convierte en un mensaje de [**\_ LBUTTONDBLCLK de WM**](/windows/desktop/inputdev/wm-lbuttondblclk) . Los mensajes equivalentes se definen para los botones derecho, medio y botón XBUTTON.

Hasta que obtenga el mensaje de doble clic, no hay ninguna manera de indicar que el primer clic del mouse es el inicio de un doble clic. Por lo tanto, una acción de doble clic debe continuar una acción que comience con el primer clic del mouse. Por ejemplo, en el shell de Windows, un solo clic selecciona una carpeta, mientras que un doble clic abre la carpeta.

## <a name="non-client-mouse-messages"></a>Mensajes de mouse que no son de cliente

Se define un conjunto independiente de mensajes para los eventos del mouse que se producen dentro del área no cliente de la ventana. Estos mensajes tienen las letras "NC" en el nombre. Por ejemplo, [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) es el equivalente no cliente de [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown). Una aplicación típica no interceptará estos mensajes, porque la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) controla estos mensajes correctamente. Sin embargo, pueden ser útiles para ciertas funciones avanzadas. Por ejemplo, podría utilizar estos mensajes para implementar el comportamiento personalizado en la barra de título. Si administra estos mensajes, normalmente debe pasarlos a **DefWindowProc** después. De lo contrario, la aplicación interrumpirá la funcionalidad estándar, como arrastrar o minimizar la ventana.

## <a name="next"></a>Siguientes

[Movimiento del mouse](mouse-movement.md)

 

 