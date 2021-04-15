---
title: Escribir el procedimiento de ventana
description: .
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f11b22ba5dd0653905ca4e2bdb546d106183fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676359"
---
# <a name="writing-the-window-procedure"></a>Escribir el procedimiento de ventana

La función [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) llama al procedimiento de ventana de la ventana que es el destino del mensaje. El procedimiento de ventana tiene la siguiente firma.

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

Hay cuatro parámetros:

- *hWnd* es un identificador de la ventana.
- *uMsg* es el código del mensaje; por ejemplo, el mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) indica que se ha cambiado el tamaño de la ventana.
- *wParam* y *lParam* contienen datos adicionales relacionados con el mensaje. El significado exacto depende del código del mensaje.

**LRESULT** es un valor entero que el programa devuelve a Windows. Contiene la respuesta del programa a un mensaje determinado. El significado de este valor depende del código del mensaje. **Callback** es la Convención de llamada de la función.

Un procedimiento de ventana típico es simplemente una gran instrucción switch que cambia en el código del mensaje. Agregue casos para cada mensaje que desee controlar.

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

Los datos adicionales para el mensaje se encuentran en los parámetros *lParam* y *wParam* . Ambos parámetros son valores enteros el tamaño de un puntero de ancho (32 bits o 64 bits). El significado de cada depende del código del mensaje (*uMsg*). Para cada mensaje, tendrá que buscar el código de mensaje en MSDN y convertir los parámetros al tipo de datos correcto. Normalmente, los datos son un valor numérico o un puntero a una estructura. Algunos mensajes no tienen datos.

Por ejemplo, la documentación del mensaje [**de \_ tamaño de WM**](/windows/desktop/winmsg/wm-size) indica que:

- *wParam* es una marca que indica si la ventana se ha minimizado, maximizado o cambiado de tamaño.
- *lParam* contiene el nuevo ancho y alto de la ventana como valores de 16 bits empaquetados en un número de 1 32 o 64 bits. Tendrá que realizar algún cambio de bits para obtener estos valores. Afortunadamente, el archivo de encabezado WinDef. h incluye macros auxiliares que lo hacen.

Un procedimiento de ventana típico controla docenas de mensajes, por lo que puede crecer bastante. Una manera de hacer que el código sea más modular es colocar la lógica para controlar cada mensaje en una función independiente. En el procedimiento de ventana, convierta los parámetros *wParam* e *lParam* al tipo de datos correcto y pase esos valores a la función. Por ejemplo, para controlar el mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) , el procedimiento de ventana tendría el siguiente aspecto:

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

Las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) obtienen los valores de ancho y alto de 16 bits de *lParam*. (Puede buscar estos tipos de detalles en la documentación de MSDN para cada código de mensaje). El procedimiento de ventana extrae el ancho y el alto y, a continuación, pasa estos valores a la `OnSize` función.

## <a name="default-message-handling"></a>Control de mensajes predeterminado

Si no controla un mensaje determinado en el procedimiento de ventana, pase los parámetros de mensaje directamente a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Esta función realiza la acción predeterminada para el mensaje, que varía según el tipo de mensaje.

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a>Evitar cuellos de botella en el procedimiento de ventana

Mientras se ejecuta el procedimiento de ventana, se bloquea cualquier otro mensaje para Windows creado en el mismo subproceso. Por lo tanto, evite el procesamiento largo dentro del procedimiento de ventana. Por ejemplo, supongamos que el programa abre una conexión TCP y espera indefinidamente a que el servidor responda. Si lo hace dentro del procedimiento de ventana, la interfaz de usuario no responderá hasta que se complete la solicitud. Durante ese tiempo, la ventana no puede procesar la entrada del mouse o del teclado, volver a dibujarse o incluso cerrarse.

En su lugar, debe trasladar el trabajo a otro subproceso, utilizando uno de los recursos de multitarea integrados en Windows:

- Cree un nuevo subproceso.
- Use un grupo de subprocesos.
- Usar llamadas de e/s asincrónicas.
- Use llamadas a procedimientos asincrónicos.

## <a name="next"></a>Siguientes

[Pintar la ventana](painting-the-window.md)