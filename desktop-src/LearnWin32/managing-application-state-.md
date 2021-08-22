---
title: Administración del estado de la aplicación
description: Un procedimiento de ventana es simplemente una función que se invoca para cada mensaje, por lo que es intrínsecamente sin estado. Por lo tanto, necesita una manera de realizar un seguimiento del estado de la aplicación desde una llamada de función a la siguiente.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0cde27195ba0dfc16668da11beac243821902995a9d01daa337f8962944343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068074"
---
# <a name="managing-application-state"></a>Administración del estado de la aplicación

Un procedimiento de ventana es simplemente una función que se invoca para cada mensaje, por lo que es intrínsecamente sin estado. Por lo tanto, necesita una manera de realizar un seguimiento del estado de la aplicación desde una llamada de función a la siguiente.

El enfoque más sencillo es simplemente colocar todo en variables globales. Esto funciona lo suficientemente bien para programas pequeños y muchos de los ejemplos del SDK usan este enfoque. En un programa grande, sin embargo, conduce a una proliferación de variables globales. Además, es posible que tenga varias ventanas, cada una con su propio procedimiento de ventana. Realizar un seguimiento de qué ventana debe tener acceso a las variables que se vuelven confusas y propensas a errores.

La [**función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) proporciona una manera de pasar cualquier estructura de datos a una ventana. Cuando se llama a esta función, envía los dos mensajes siguientes al procedimiento de ventana:

- [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)
- [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)

Estos mensajes se envían en el orden indicado. (Estos no son los únicos dos mensajes enviados durante [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)pero podemos omitir los demás para esta explicación).

Los [**mensajes WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) [**y WM \_ CREATE**](/windows/desktop/winmsg/wm-create) se envían antes de que la ventana se vuelva visible. Esto los convierte en un buen lugar para inicializar la interfaz de usuario, por ejemplo, para determinar el diseño inicial de la ventana.

El último parámetro de [**CreateWindowEx es**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) un puntero de tipo **\* void* _. Puede pasar cualquier valor de puntero que desee en este parámetro. Cuando el procedimiento de ventana controla [el mensaje _ WM *\_ NCCREATE* *](/windows/desktop/winmsg/wm-nccreate) o [**WM \_ CREATE,**](/windows/desktop/winmsg/wm-create) puede extraer este valor de los datos del mensaje.

Veamos cómo usaría este parámetro para pasar datos de aplicación a la ventana. En primer lugar, defina una clase o estructura que contiene información de estado.

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

Al llamar a [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)pase un puntero a esta estructura en el parámetro **void \*** final.

```C++
StateInfo *pState = new (std::nothrow) StateInfo;

if (pState == NULL)
{
    return 0;
}

// Initialize the structure members (not shown).

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
    pState      // Additional application data
    );
```

Cuando recibe los mensajes [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) y [**WM \_ CREATE,**](/windows/desktop/winmsg/wm-create) el parámetro *lParam* de cada mensaje es un puntero a una [**estructura CREATESTRUCT.**](/windows/win32/api/winuser/ns-winuser-createstructa) La **estructura CREATESTRUCT,** a su vez, contiene el puntero que pasó a [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)

![diagrama que muestra el diseño de la estructura createstruct](images/appstate01.png)

Aquí se muestra cómo extraer el puntero a la estructura de datos. En primer lugar, obtenga [**la estructura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) mediante la conversión *del parámetro lParam.*

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

El **miembro lpCreateParams** de la [**estructura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) es el puntero void original que especificó en [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Obtenga un puntero a su propia estructura de datos mediante la conversión **de lpCreateParams**.

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

A continuación, llame [**a la función SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) y pase el puntero a la estructura de datos.

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

El propósito de esta última llamada de función es almacenar el puntero *StateInfo* en los datos de instancia de la ventana. Una vez hecho esto, siempre puede obtener el puntero desde la ventana llamando a [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

Cada ventana tiene sus propios datos de instancia, por lo que puede crear varias ventanas y proporcionar a cada ventana su propia instancia de la estructura de datos. Este enfoque es especialmente útil si define una clase de ventanas y crea más de una ventana de esa clase, por ejemplo, si crea una clase de control personalizada. Es conveniente encapsular la [**llamada GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) en una pequeña función auxiliar.

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

Ahora puede escribir el procedimiento de ventana como se muestra a continuación.

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;
    if (uMsg == WM_CREATE)
    {
        CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
        pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
        SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
    }
    else
    {
        pState = GetAppState(hwnd);
    }

    switch (uMsg)
    {


    // Remainder of the window procedure not shown ...

    }
    return TRUE;
}
```

## <a name="an-object-oriented-approach"></a>Un enfoque Object-Oriented de datos

Podemos ampliar este enfoque aún más. Ya hemos definido una estructura de datos para contener información de estado sobre la ventana. Tiene sentido proporcionar a esta estructura de datos funciones miembro (métodos) que funcionan en los datos. Esto conduce de forma natural a un diseño en el que la estructura (o clase) es responsable de todas las operaciones en la ventana. A continuación, el procedimiento de ventana formaría parte de la clase .

En otras palabras, nos gustaría pasar de esto:

```C++
// pseudocode

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;

    /* Get pState from the HWND. */

    switch (uMsg)
    {
        case WM_SIZE:
            HandleResize(pState, ...);
            break;

        case WM_PAINT:
            HandlePaint(pState, ...);
            break;

       // And so forth.
    }
}
```

Por esta otra:

```C++
// pseudocode

LRESULT MyWindow::WindowProc(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_SIZE:
            this->HandleResize(...);
            break;

        case WM_PAINT:
            this->HandlePaint(...);
            break;
    }
}
```

El único problema es cómo enlazar el `MyWindow::WindowProc` método. La [**función RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) espera que el procedimiento de ventana sea un puntero de función. No se puede pasar un puntero a una función miembro (no estática) en este contexto. Sin embargo, puede pasar un puntero a una *función miembro* estática y, a continuación, delegar en la función miembro. Esta es una plantilla de clase que muestra este enfoque:

```C++
template <class DERIVED_TYPE> 
class BaseWindow
{
public:
    static LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
    {
        DERIVED_TYPE *pThis = NULL;

        if (uMsg == WM_NCCREATE)
        {
            CREATESTRUCT* pCreate = (CREATESTRUCT*)lParam;
            pThis = (DERIVED_TYPE*)pCreate->lpCreateParams;
            SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pThis);

            pThis->m_hwnd = hwnd;
        }
        else
        {
            pThis = (DERIVED_TYPE*)GetWindowLongPtr(hwnd, GWLP_USERDATA);
        }
        if (pThis)
        {
            return pThis->HandleMessage(uMsg, wParam, lParam);
        }
        else
        {
            return DefWindowProc(hwnd, uMsg, wParam, lParam);
        }
    }

    BaseWindow() : m_hwnd(NULL) { }

    BOOL Create(
        PCWSTR lpWindowName,
        DWORD dwStyle,
        DWORD dwExStyle = 0,
        int x = CW_USEDEFAULT,
        int y = CW_USEDEFAULT,
        int nWidth = CW_USEDEFAULT,
        int nHeight = CW_USEDEFAULT,
        HWND hWndParent = 0,
        HMENU hMenu = 0
        )
    {
        WNDCLASS wc = {0};

        wc.lpfnWndProc   = DERIVED_TYPE::WindowProc;
        wc.hInstance     = GetModuleHandle(NULL);
        wc.lpszClassName = ClassName();

        RegisterClass(&wc);

        m_hwnd = CreateWindowEx(
            dwExStyle, ClassName(), lpWindowName, dwStyle, x, y,
            nWidth, nHeight, hWndParent, hMenu, GetModuleHandle(NULL), this
            );

        return (m_hwnd ? TRUE : FALSE);
    }

    HWND Window() const { return m_hwnd; }

protected:

    virtual PCWSTR  ClassName() const = 0;
    virtual LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam) = 0;

    HWND m_hwnd;
};
```

La `BaseWindow` clase es una clase base abstracta, de la que se derivan clases de ventana específicas. Por ejemplo, esta es la declaración de una clase simple derivada de `BaseWindow` :

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

Para crear la ventana, llame a `BaseWindow::Create` :

```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    MainWindow win;

    if (!win.Create(L"Learn to Program Windows", WS_OVERLAPPEDWINDOW))
    {
        return 0;
    }

    ShowWindow(win.Window(), nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}
```

El método virtual `BaseWindow::HandleMessage` puro se usa para implementar el procedimiento de ventana. Por ejemplo, la siguiente implementación es equivalente al procedimiento de ventana que se muestra al principio del [módulo 1](your-first-windows-program.md).

```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(m_hwnd, &ps);
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(m_hwnd, &ps);
        }
        return 0;

    default:
        return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
    }
    return TRUE;
}
```

Observe que el identificador de ventana se almacena en una variable miembro (*m \_ hwnd*), por lo que no es necesario pasarlo como parámetro a `HandleMessage` .

Muchos de los marcos de programación de Windows existentes, como Microsoft Foundation Classes (MFC) y Active Template Library (ATL), usan enfoques que son básicamente similares al que se muestra aquí. Por supuesto, un marco totalmente generalizado como MFC es más complejo que este ejemplo relativamente simplista.

## <a name="next"></a>Siguientes

[Módulo 2: Uso de COM en el Windows programa](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a>Temas relacionados

[Ejemplo baseWindow](basewindow-sample.md)