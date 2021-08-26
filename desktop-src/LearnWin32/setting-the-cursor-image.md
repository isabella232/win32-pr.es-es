---
title: Establecimiento de la imagen de cursor
description: Establecimiento de la imagen de cursor
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4723289155bc7898f6f49e188ad972ca152332c82994b57c79af493c8fe6b572
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896915"
---
# <a name="setting-the-cursor-image"></a>Establecimiento de la imagen de cursor

El *cursor* es la imagen pequeña que muestra la ubicación del mouse u otro dispositivo que apunta. Muchas aplicaciones cambian la imagen del cursor para proporcionar comentarios al usuario. Aunque no es necesario, agrega un buen poco de pulir a la aplicación.

Windows proporciona un conjunto de imágenes de cursor estándar, *denominadas cursores del sistema*. Estos incluyen la flecha, la mano, el haz de I, el reloj de reloj (que ahora es un círculo de giro) y otros. En esta sección se describe cómo usar los cursores del sistema. Para tareas más avanzadas, como la creación de cursores personalizados, vea [Cursores](/windows/desktop/menurc/cursors).

Puede asociar un cursor a una clase de ventana estableciendo el **miembro hCursor** de la [**estructura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) o [**WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) De lo contrario, el cursor predeterminado es la flecha. Cuando el mouse se mueve sobre una ventana, la ventana recibe un mensaje [**\_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) de WM (a menos que otra ventana haya capturado el mouse). En este momento, se produce uno de los siguientes eventos:

-   La aplicación establece el cursor y el procedimiento de ventana devuelve **TRUE.**
-   La aplicación no hace nada y pasa [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Para establecer el cursor, un programa hace lo siguiente:

1.  Llama [**a LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) para cargar el cursor en la memoria. Esta función devuelve un identificador al cursor.
2.  Llama [**a SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) y pasa el identificador del cursor.

De lo contrario, si la aplicación pasa [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) [**a DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)la función **DefWindowProc** usa el algoritmo siguiente para establecer la imagen del cursor:

1.  Si la ventana tiene un elemento primario, reenvía [**el mensaje \_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) al elemento primario que se debe controlar.
2.  De lo contrario, si la ventana tiene un cursor de clase, establezca el cursor en el cursor de clase.
3.  Si no hay ningún cursor de clase, establezca el cursor en el cursor de flecha.

La [**función LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) puede cargar un cursor personalizado desde un recurso o uno de los cursores del sistema. En el ejemplo siguiente se muestra cómo establecer el cursor en el cursor de la mano del sistema.


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



Si cambia el cursor, la imagen del cursor se restablece en el siguiente movimiento del mouse, a menos que intercepte el [**mensaje \_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) y vuelva a establecer el cursor. El código siguiente muestra cómo controlar **WM \_ SETCURSOR**.


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



Este código comprueba primero los 16 bits inferiores *de lParam*. Si `LOWORD(lParam)` es igual a **HTCLIENT**, significa que el cursor está sobre el área de cliente de la ventana. De lo contrario, el cursor se encuentra sobre el área no cliente. Normalmente, solo debe establecer el cursor para el área de cliente y dejar que Windows el cursor para el área no cliente.

## <a name="next"></a>Siguientes

[Entrada del usuario: ejemplo extendido](user-input--extended-example.md)

 

 