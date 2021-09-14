---
title: Crear una ventana
description: Crear una ventana
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: d05536183a2e5a2504a096a22e11bea2098f08ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159997"
---
# <a name="creating-a-window"></a>Crear una ventana

## <a name="window-classes"></a>Clases de ventanas

Una *clase de ventana* define un conjunto de comportamientos que varias ventanas pueden tener en común. Por ejemplo, en un grupo de botones, cada botón tiene un comportamiento similar cuando el usuario hace clic en él. Por supuesto, los botones no son completamente idénticos; cada botón muestra su propia cadena de texto y tiene sus propias coordenadas de pantalla. Los datos que son únicos para cada ventana se denominan *datos de instancia.*

Cada ventana debe estar asociada a una clase de ventana, incluso si el programa solo crea una instancia de esa clase. Es importante comprender que una clase de ventana no es una "clase" en el sentido de C++. En su lugar, es una estructura de datos utilizada internamente por el sistema operativo. Las clases de ventana se registran con el sistema en tiempo de ejecución. Para registrar una nueva clase de ventana, comience rellenando una [**estructura WNDCLASS:**](/windows/win32/api/winuser/ns-winuser-wndclassa)

```cpp
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

Debe establecer los siguientes miembros de estructura:

- **lpfnWndProc es** un puntero a una función definida por la aplicación denominada procedimiento *de* ventana o "procedimiento de ventana". El procedimiento de ventana define la mayor parte del comportamiento de la ventana. Examinaremos el procedimiento de ventana con detalle más adelante. Por ahora, solo tiene que tratar esto como una referencia hacia delante.
- **hInstance** es el identificador de la instancia de la aplicación. Obtenga este valor del *parámetro hInstance* de **wWinMain**.
- **lpszClassName es** una cadena que identifica la clase window.

Los nombres de clase son locales para el proceso actual, por lo que el nombre solo debe ser único dentro del proceso. Sin embargo, los controles Windows estándar también tienen clases. Si usa cualquiera de esos controles, debe elegir nombres de clase que no entren en conflicto con los nombres de clase de control. Por ejemplo, la clase de ventana para el control de botón se denomina "Button".

La [**estructura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) tiene otros miembros que no se muestran aquí. Puede establecerlos en cero, como se muestra en este ejemplo, o rellenarlos. La [**documentación de WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) describe la estructura en detalle.

A continuación, pase la dirección de la [**estructura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) a [**la función RegisterClass.**](/windows/desktop/api/winuser/nf-winuser-registerclassa) Esta función registra la clase window con el sistema operativo.

```cpp
RegisterClass(&wc);
```

## <a name="creating-the-window"></a>Creación de la ventana

Para crear una nueva instancia de una ventana, llame a la [**función CreateWindowEx:**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)

```cpp
HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}
```

Puede leer descripciones detalladas de parámetros en la documentación de la función [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pero este es un resumen rápido:

- El primer parámetro le permite especificar algunos comportamientos opcionales para la ventana (por ejemplo, ventanas transparentes). Establezca este parámetro en cero para los comportamientos predeterminados.
- `CLASS_NAME` es el nombre de la clase de ventana. Esto define el tipo de ventana que está creando.
- Los distintos tipos de ventanas usan el texto de la ventana de maneras diferentes. Si la ventana tiene una barra de título, el texto se muestra en la barra de título.
- El estilo de ventana es un conjunto de marcas que definen parte del aspecto de una ventana. La constante **WS \_ OVERLAPPEDWINDOW es** en realidad varias marcas combinadas con un OR bit a **bit.** Juntas, estas marcas dan a la ventana una barra de título, un borde, un menú del sistema y **los botones Minimizar** **y Maximizar.** Este conjunto de marcas es el estilo más común para una ventana de aplicación de nivel superior.
- Para la posición y el tamaño, **la constante CW \_ USEDEFAULT** significa usar valores predeterminados.
- El parámetro siguiente establece una ventana primaria o una ventana de propietario para la nueva ventana. Establezca el elemento primario si va a crear una ventana secundaria. Para una ventana de nivel superior, establezca esta opción en **NULL.**
- Para una ventana de aplicación, el parámetro siguiente define el menú de la ventana. En este ejemplo no se usa un menú, por lo que el valor es **NULL.**
- *hInstance* es el identificador de instancia, descrito anteriormente. (Vea [WinMain: el punto de entrada de la aplicación).](winmain--the-application-entry-point.md)
- El último parámetro es un puntero a datos arbitrarios de tipo **void. \*** Puede usar este valor para pasar una estructura de datos al procedimiento de ventana. Se mostrará una posible manera de usar este parámetro en la sección [Administración del estado de la aplicación.](managing-application-state-.md)

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) devuelve un identificador a la nueva ventana o cero si se produce un error en la función. Para mostrar la ventana, es decir, hacer que la ventana sea visible, pase el identificador de ventana a la [**función ShowWindow:**](/windows/desktop/api/winuser/nf-winuser-showwindow)

```cpp
ShowWindow(hwnd, nCmdShow);
```

El *parámetro hwnd* es el identificador de ventana devuelto [**por CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) El *parámetro nCmdShow* se puede usar para minimizar o maximizar una ventana. El sistema operativo pasa este valor al programa a través de la **función wWinMain.**

Este es el código completo para crear la ventana. Recuerde que `WindowProc` sigue siendo simplemente una declaración adelantada de una función.

```cpp
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;

RegisterClass(&wc);

// Create the window.

HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}

ShowWindow(hwnd, nCmdShow);
```

Enhorabuena, ha creado una ventana. En este momento, la ventana no contiene contenido ni interactúa con el usuario. En una aplicación de GUI real, la ventana respondería a eventos del usuario y del sistema operativo. En la sección siguiente se describe cómo los mensajes de ventana proporcionan este tipo de interactividad.

### <a name="next"></a>Siguientes

[Mensajes de ventana](window-messages.md)
