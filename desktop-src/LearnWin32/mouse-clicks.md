---
title: Respuesta a los clics del mouse
description: Respuesta a los clics del mouse
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947b50726e79fbf29c4f013d4ac0a449c009c1817b74b1a8063e63a68c4dd6c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897215"
---
# <a name="responding-to-mouse-clicks"></a>Respuesta a los clics del mouse

Si el usuario hace clic en un botón del mouse mientras el cursor está sobre el área cliente de una ventana, la ventana recibe uno de los mensajes siguientes.



| Mensaje                                        | Significado                   |
|------------------------------------------------|---------------------------|
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) | Botón izquierdo hacia abajo          |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)     | Botón izquierdo hacia arriba            |
| [**WM \_ MBUTTONDOWN**](/windows/desktop/inputdev/wm-mbuttondown) | Botón central hacia abajo        |
| [**WM \_ MBUTTONUP**](/windows/desktop/inputdev/wm-mbuttonup)     | Botón central hacia arriba          |
| [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown) | Botón derecho hacia abajo         |
| [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)     | Botón derecho hacia arriba           |
| [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) | XBUTTON1 o XBUTTON2 hacia abajo |
| [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup)     | XBUTTON1 o XBUTTON2 hacia arriba   |



 

Recuerde que el área de cliente es la parte de la ventana que excluye el marco. Para obtener más información sobre las áreas cliente, vea [¿Qué es una ventana?](what-is-a-window-.md)

### <a name="mouse-coordinates"></a>Coordenadas del mouse

En todos estos mensajes, el *parámetro lParam* contiene las coordenadas x e y del puntero del mouse. Los 16 bits más bajos de *lParam* contienen la coordenada x y los 16 bits siguientes contienen la coordenada y. Use las macros [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) [**y GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para desempaquetar las coordenadas *de lParam*.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Estas macros se definen en el archivo de encabezado WindowsX.h.

En los valores de 64 Windows, *lParam* es un valor de 64 bits. No se usan los 32 bits superiores de *lParam.* La documentación de MSDN menciona la "palabra de orden bajo" y la "palabra de orden superior" *de lParam*. En el caso de 64 bits, esto significa las palabras de orden bajo y alto de los 32 bits inferiores. Las macros extraen los valores correctos, por lo que si los usa, estará seguro.

Las coordenadas del mouse se dan en píxeles, no en píxeles independientes del dispositivo (DIP), y se miden con respecto al área cliente de la ventana. Las coordenadas son valores con firma. Las posiciones encima y a la izquierda del área de cliente tienen coordenadas negativas, lo que es importante si realiza un seguimiento de la posición del mouse fuera de la ventana. Veremos cómo hacerlo en un tema posterior, [Capturar movimiento del mouse fuera de la ventana](mouse-movement.md).

### <a name="additional-flags"></a>Marcas adicionales

El *parámetro wParam* contiene un **OR** bit a bit de marcas, que indica el estado de los demás botones del mouse más las teclas MAYÚS y CTRL.



| Marca             | Significado                          |
|------------------|----------------------------------|
| **MK \_ CONTROL**  | La tecla CTRL está presionada.            |
| **MK \_ LBUTTON**  | El botón izquierdo del mouse está apagado.   |
| **MK \_ MBUTTON**  | El botón central del mouse está apagado. |
| **MK \_ RBUTTON**  | El botón derecho del mouse está apagado.  |
| **MK \_ SHIFT**    | La tecla MAYÚS está abajo.           |
| **MK \_ XBUTTON1** | El botón XBUTTON1 está apagado.     |
| **MK \_ XBUTTON2** | El botón XBUTTON2 está apagado.     |



 

La ausencia de una marca significa que no se presionó el botón o la tecla correspondientes. Por ejemplo, para probar si la tecla CTRL está presionada:


```C++
if (wParam & MK_CONTROL) { ...
```



Si necesita encontrar el estado de otras teclas además de CTRL y MAYÚS, use la función [**GetKeyState,**](/windows/desktop/api/winuser/nf-winuser-getkeystate) que se describe en [Entrada de teclado](keyboard-input.md).

Los [**mensajes de ventana \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) y [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) se aplican a XBUTTON1 y XBUTTON2. El *parámetro wParam* indica qué botón se hizo clic.


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



## <a name="double-clicks"></a>Clics dobles

Una ventana no recibe notificaciones de doble clic de forma predeterminada. Para recibir doble clic, establezca la marca **\_ DBLCLKS** de CS en la [**estructura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) al registrar la clase de ventana.


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



Si establece la marca **\_ DBLCLKS** de CS como se muestra, la ventana recibirá notificaciones de doble clic. Un doble clic se indica mediante un mensaje de ventana con "DBLCLK" en el nombre. Por ejemplo, un doble clic en el botón izquierdo del mouse genera la siguiente secuencia de mensajes:

<dl>

[**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)  
[**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)  
[**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)  
[**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

De hecho, el segundo mensaje [**\_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown) que normalmente se generaría se convierte en un mensaje [**\_ LBUTTONDBLCLK de WM.**](/windows/desktop/inputdev/wm-lbuttondblclk) Los mensajes equivalentes se definen para los botones right, middle y XBUTTON.

Hasta que reciba el mensaje de doble clic, no hay ninguna manera de saber que el primer clic del mouse es el inicio de un doble clic. Por lo tanto, una acción de doble clic debe continuar con una acción que comience con el primer clic del mouse. Por ejemplo, en Windows Shell, un solo clic selecciona una carpeta, mientras que un doble clic abre la carpeta.

## <a name="non-client-mouse-messages"></a>Mensajes del mouse que no son de cliente

Se define un conjunto independiente de mensajes para los eventos del mouse que se producen dentro del área no cliente de la ventana. Estos mensajes tienen las letras "NC" en el nombre. Por ejemplo, [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) es el equivalente no cliente de [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown). Una aplicación típica no interceptará estos mensajes, porque la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) controla estos mensajes correctamente. Sin embargo, pueden ser útiles para determinadas funciones avanzadas. Por ejemplo, puede usar estos mensajes para implementar el comportamiento personalizado en la barra de título. Si controla estos mensajes, generalmente debe pasarlos a **DefWindowProc más** adelante. De lo contrario, la aplicación interrumpirá la funcionalidad estándar, como arrastrar o minimizar la ventana.

## <a name="next"></a>Siguientes

[Movimiento del mouse](mouse-movement.md)

 

 