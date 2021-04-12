---
title: Establecer la imagen del cursor
description: Establecer la imagen del cursor
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487610"
---
# <a name="setting-the-cursor-image"></a>Establecer la imagen del cursor

El *cursor* es la imagen pequeña que muestra la ubicación del mouse u otro dispositivo señalador. Muchas aplicaciones cambian la imagen del cursor para proporcionar comentarios al usuario. Aunque no es necesario, agrega un buen aspecto a la aplicación.

Windows proporciona un conjunto de imágenes de cursores estándar, llamadas *cursores del sistema*. Entre ellas se incluyen la flecha, la mano, el rayo, el reloj de arena (que ahora es un círculo girado) y otros. En esta sección se describe cómo usar los cursores del sistema. Para tareas más avanzadas, como la creación de cursores personalizados, vea [cursores](/windows/desktop/menurc/cursors).

Puede asociar un cursor a una clase de ventana estableciendo el miembro **hCursor** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) o [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . De lo contrario, el cursor predeterminado es la flecha. Cuando el mouse se mueve sobre una ventana, la ventana recibe un mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) (a menos que otra ventana haya capturado el mouse). En este momento, se produce uno de los siguientes eventos:

-   La aplicación establece el cursor y el procedimiento de ventana devuelve **true**.
-   La aplicación no realiza ninguna acción y pasa [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Para establecer el cursor, un programa hace lo siguiente:

1.  Llama a [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) para cargar el cursor en la memoria. Esta función devuelve un identificador al cursor.
2.  Llama a [**setCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) y pasa el identificador del cursor.

De lo contrario, si la aplicación pasa [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), la función **DefWindowProc** usa el siguiente algoritmo para establecer la imagen del cursor:

1.  Si la ventana tiene un elemento primario, reenvíe el mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) al elemento primario para controlar.
2.  De lo contrario, si la ventana tiene un cursor de clase, establezca el cursor en el cursor de clase.
3.  Si no hay ningún cursor de clase, establezca el cursor en el cursor de flecha.

La función [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) puede cargar un cursor personalizado de un recurso, o uno de los cursores del sistema. En el ejemplo siguiente se muestra cómo establecer el cursor en el cursor de mano del sistema.


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



Si cambia el cursor, la imagen del cursor se restablecerá en el siguiente movimiento del mouse, a menos que se intercepte el mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) y se vuelva a establecer el cursor. En el código siguiente se muestra cómo administrar **WM \_ SETCURSOR**.


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



Este código comprueba primero los 16 bits inferiores de *lParam*. Si es `LOWORD(lParam)` igual a **HTCLIENT**, significa que el cursor está sobre el área cliente de la ventana. De lo contrario, el cursor se encuentra sobre el área no cliente. Normalmente, solo debe establecer el cursor para el área cliente y dejar que Windows configure el cursor para el área no cliente.

## <a name="next"></a>Siguientes

[Entrada de usuario: ejemplo extendido](user-input--extended-example.md)

 

 