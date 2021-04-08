---
title: Administración del estado de la aplicación
description: Un procedimiento de ventana es simplemente una función que se invoca para cada mensaje, por lo que es intrínsecamente sin estado. Por lo tanto, necesita una forma de realizar un seguimiento del estado de la aplicación desde una llamada de función a la siguiente.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e275833c30c612b5b40ab29d089d07ed7794b429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077727"
---
# <a name="managing-application-state"></a><span data-ttu-id="83729-104">Administración del estado de la aplicación</span><span class="sxs-lookup"><span data-stu-id="83729-104">Managing Application State</span></span>

<span data-ttu-id="83729-105">Un procedimiento de ventana es simplemente una función que se invoca para cada mensaje, por lo que es intrínsecamente sin estado.</span><span class="sxs-lookup"><span data-stu-id="83729-105">A window procedure is just a function that gets invoked for every message, so it is inherently stateless.</span></span> <span data-ttu-id="83729-106">Por lo tanto, necesita una forma de realizar un seguimiento del estado de la aplicación desde una llamada de función a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="83729-106">Therefore, you need a way to track the state of your application from one function call to the next.</span></span>

<span data-ttu-id="83729-107">El enfoque más sencillo es simplemente colocar todo en las variables globales.</span><span class="sxs-lookup"><span data-stu-id="83729-107">The simplest approach is simply to put everything in global variables.</span></span> <span data-ttu-id="83729-108">Esto funciona bien lo suficiente para programas pequeños y muchos de los ejemplos del SDK usan este enfoque.</span><span class="sxs-lookup"><span data-stu-id="83729-108">This works well enough for small programs, and many of the SDK samples use this approach.</span></span> <span data-ttu-id="83729-109">En un programa grande, sin embargo, conduce a la proliferación de variables globales.</span><span class="sxs-lookup"><span data-stu-id="83729-109">In a large program, however, it leads to a proliferation of global variables.</span></span> <span data-ttu-id="83729-110">Además, es posible que tenga varias ventanas, cada una con su propio procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="83729-110">Also, you might have several windows, each with its own window procedure.</span></span> <span data-ttu-id="83729-111">Seguimiento de la ventana que debería tener acceso a las variables que son confusas y propensas a errores.</span><span class="sxs-lookup"><span data-stu-id="83729-111">Keeping track of which window should access which variables becomes confusing and error-prone.</span></span>

<span data-ttu-id="83729-112">La función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) proporciona una manera de pasar cualquier estructura de datos a una ventana.</span><span class="sxs-lookup"><span data-stu-id="83729-112">The [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function provides a way to pass any data structure to a window.</span></span> <span data-ttu-id="83729-113">Cuando se llama a esta función, envía los dos mensajes siguientes al procedimiento de ventana:</span><span class="sxs-lookup"><span data-stu-id="83729-113">When this function is called, it sends the following two messages to your window procedure:</span></span>

- [<span data-ttu-id="83729-114">**NCCREATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="83729-114">**WM\_NCCREATE**</span></span>](/windows/desktop/winmsg/wm-nccreate)
- [<span data-ttu-id="83729-115">**creación de WM \_**</span><span class="sxs-lookup"><span data-stu-id="83729-115">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)

<span data-ttu-id="83729-116">Estos mensajes se envían en el orden mostrado.</span><span class="sxs-lookup"><span data-stu-id="83729-116">These messages are sent in the order listed.</span></span> <span data-ttu-id="83729-117">(Estos no son los únicos dos mensajes que se envían durante [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), pero se pueden omitir los demás para este debate).</span><span class="sxs-lookup"><span data-stu-id="83729-117">(These are not the only two messages sent during [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), but we can ignore the others for this discussion.)</span></span>

<span data-ttu-id="83729-118">Los mensajes de [**\_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) y de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) se envían antes de que la ventana se vuelva visible.</span><span class="sxs-lookup"><span data-stu-id="83729-118">The [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message are sent before the window becomes visible.</span></span> <span data-ttu-id="83729-119">Esto los convierte en un buen lugar para inicializar la interfaz de usuario, por ejemplo, para determinar el diseño inicial de la ventana.</span><span class="sxs-lookup"><span data-stu-id="83729-119">That makes them a good place to initialize your UI—for example, to determine the initial layout of the window.</span></span>

<span data-ttu-id="83729-120">El último parámetro de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) es un puntero de tipo **void \***.</span><span class="sxs-lookup"><span data-stu-id="83729-120">The last parameter of [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) is a pointer of type **void\***.</span></span> <span data-ttu-id="83729-121">Puede pasar cualquier valor de puntero que desee en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="83729-121">You can pass any pointer value that you want in this parameter.</span></span> <span data-ttu-id="83729-122">Cuando el procedimiento de ventana controla el mensaje de [**\_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) o [**WM \_ Create**](/windows/desktop/winmsg/wm-create) de WM, puede extraer este valor de los datos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="83729-122">When the window procedure handles the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) or [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, it can extract this value from the message data.</span></span>

<span data-ttu-id="83729-123">Veamos cómo usaría este parámetro para pasar datos de la aplicación a la ventana.</span><span class="sxs-lookup"><span data-stu-id="83729-123">Let's see how you would use this parameter to pass application data to your window.</span></span> <span data-ttu-id="83729-124">En primer lugar, defina una clase o estructura que contenga información de estado.</span><span class="sxs-lookup"><span data-stu-id="83729-124">First, define a class or structure that holds state information.</span></span>

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

<span data-ttu-id="83729-125">Cuando llame a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), pase un puntero a esta estructura en el parámetro **void \*** final.</span><span class="sxs-lookup"><span data-stu-id="83729-125">When you call [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), pass a pointer to this structure in the final **void\*** parameter.</span></span>

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

<span data-ttu-id="83729-126">Cuando recibe los mensajes [**de \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) y [**WM \_**](/windows/desktop/winmsg/wm-create) de WM, el parámetro *lParam* de cada mensaje es un puntero a una estructura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) .</span><span class="sxs-lookup"><span data-stu-id="83729-126">When you receive the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) messages, the *lParam* parameter of each message is a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="83729-127">La estructura **CREATESTRUCT** , a su vez, contiene el puntero que pasó a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="83729-127">The **CREATESTRUCT** structure, in turn, contains the pointer that you passed into [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>

![diagrama que muestra el diseño de la estructura createstruct](images/appstate01.png)

<span data-ttu-id="83729-129">Aquí se muestra cómo extraer el puntero a la estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="83729-129">Here is how you extract the pointer to your data structure.</span></span> <span data-ttu-id="83729-130">En primer lugar, obtenga la estructura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) mediante la conversión del parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="83729-130">First, get the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure by casting the *lParam* parameter.</span></span>

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

<span data-ttu-id="83729-131">El miembro **lpCreateParams** de la estructura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) es el puntero void original que especificó en [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="83729-131">The **lpCreateParams** member of the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure is the original void pointer that you specified in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="83729-132">Obtenga un puntero a su propia estructura de datos mediante la conversión de **lpCreateParams**.</span><span class="sxs-lookup"><span data-stu-id="83729-132">Get a pointer to your own data structure by casting **lpCreateParams**.</span></span>

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

<span data-ttu-id="83729-133">A continuación, llame a la función [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) y pase el puntero a la estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="83729-133">Next, call the [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function and pass in the pointer to your data structure.</span></span>

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

<span data-ttu-id="83729-134">El propósito de esta última llamada de función es almacenar el puntero *StateInfo* en los datos de instancia para la ventana.</span><span class="sxs-lookup"><span data-stu-id="83729-134">The purpose of this last function call is to store the *StateInfo* pointer in the instance data for the window.</span></span> <span data-ttu-id="83729-135">Una vez hecho esto, siempre puede volver a obtener el puntero desde la ventana llamando a [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span><span class="sxs-lookup"><span data-stu-id="83729-135">Once you do this, you can always get the pointer back from the window by calling [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span></span>

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

<span data-ttu-id="83729-136">Cada ventana tiene sus propios datos de instancia, por lo que puede crear varias ventanas y asignar a cada ventana su propia instancia de la estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="83729-136">Each window has its own instance data, so you can create multiple windows and give each window its own instance of the data structure.</span></span> <span data-ttu-id="83729-137">Este enfoque es especialmente útil si define una clase de ventanas y crea más de una ventana de esa clase; por ejemplo, si crea una clase de control personalizada.</span><span class="sxs-lookup"><span data-stu-id="83729-137">This approach is especially useful if you define a class of windows and create more than one window of that class—for example, if you create a custom control class.</span></span> <span data-ttu-id="83729-138">Es conveniente encapsular la llamada a [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) en una pequeña función auxiliar.</span><span class="sxs-lookup"><span data-stu-id="83729-138">It is convenient to wrap the [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) call in a small helper function.</span></span>

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

<span data-ttu-id="83729-139">Ahora puede escribir el procedimiento de ventana como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="83729-139">Now you can write your window procedure as follows.</span></span>

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

## <a name="an-object-oriented-approach"></a><span data-ttu-id="83729-140">Un enfoque Object-Oriented</span><span class="sxs-lookup"><span data-stu-id="83729-140">An Object-Oriented Approach</span></span>

<span data-ttu-id="83729-141">Podemos ampliar este enfoque aún más.</span><span class="sxs-lookup"><span data-stu-id="83729-141">We can extend this approach further.</span></span> <span data-ttu-id="83729-142">Ya hemos definido una estructura de datos para contener información de estado sobre la ventana.</span><span class="sxs-lookup"><span data-stu-id="83729-142">We have already defined a data structure to hold state information about the window.</span></span> <span data-ttu-id="83729-143">Tiene sentido proporcionar esta estructura de datos con funciones miembro (métodos) que operan en los datos.</span><span class="sxs-lookup"><span data-stu-id="83729-143">It makes sense to provide this data structure with member functions (methods) that operate on the data.</span></span> <span data-ttu-id="83729-144">Esto conduce de forma natural a un diseño en el que la estructura (o clase) es responsable de todas las operaciones en la ventana.</span><span class="sxs-lookup"><span data-stu-id="83729-144">This naturally leads to a design where the structure (or class) is responsible for all of the operations on the window.</span></span> <span data-ttu-id="83729-145">El procedimiento de ventana se convertirá entonces en parte de la clase.</span><span class="sxs-lookup"><span data-stu-id="83729-145">The window procedure would then become part of the class.</span></span>

<span data-ttu-id="83729-146">En otras palabras, nos gustaría pasar de esto:</span><span class="sxs-lookup"><span data-stu-id="83729-146">In other words, we would like to go from this:</span></span>

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

<span data-ttu-id="83729-147">Por esta otra:</span><span class="sxs-lookup"><span data-stu-id="83729-147">To this:</span></span>

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

<span data-ttu-id="83729-148">El único problema es cómo enlazar el `MyWindow::WindowProc` método.</span><span class="sxs-lookup"><span data-stu-id="83729-148">The only problem is how to hook up the `MyWindow::WindowProc` method.</span></span> <span data-ttu-id="83729-149">La función [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) espera que el procedimiento de ventana sea un puntero a función.</span><span class="sxs-lookup"><span data-stu-id="83729-149">The [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function expects the window procedure to be a function pointer.</span></span> <span data-ttu-id="83729-150">No se puede pasar un puntero a una función miembro (no estática) en este contexto.</span><span class="sxs-lookup"><span data-stu-id="83729-150">You can't pass a pointer to a (non-static) member function in this context.</span></span> <span data-ttu-id="83729-151">Sin embargo, puede pasar un puntero a una función miembro *estática* y, a continuación, delegar a la función miembro.</span><span class="sxs-lookup"><span data-stu-id="83729-151">However, you can pass a pointer to a *static* member function and then delegate to the member function.</span></span> <span data-ttu-id="83729-152">Esta es una plantilla de clase que muestra este enfoque:</span><span class="sxs-lookup"><span data-stu-id="83729-152">Here is a class template that shows this approach:</span></span>

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

<span data-ttu-id="83729-153">La `BaseWindow` clase es una clase base abstracta, de la que se derivan las clases de ventana específicas.</span><span class="sxs-lookup"><span data-stu-id="83729-153">The `BaseWindow` class is an abstract base class, from which specific window classes are derived.</span></span> <span data-ttu-id="83729-154">Por ejemplo, a continuación se muestra la declaración de una clase simple derivada de `BaseWindow` :</span><span class="sxs-lookup"><span data-stu-id="83729-154">For example, here is the declaration of a simple class derived from `BaseWindow`:</span></span>

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

<span data-ttu-id="83729-155">Para crear la ventana, llame a `BaseWindow::Create` :</span><span class="sxs-lookup"><span data-stu-id="83729-155">To create the window, call `BaseWindow::Create`:</span></span>

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

<span data-ttu-id="83729-156">El método virtual puro `BaseWindow::HandleMessage` se usa para implementar el procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="83729-156">The pure-virtual `BaseWindow::HandleMessage` method is used to implement the window procedure.</span></span> <span data-ttu-id="83729-157">Por ejemplo, la siguiente implementación es equivalente al procedimiento de ventana que se muestra al principio del [módulo 1](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="83729-157">For example, the following implementation is equivalent to the window procedure shown at the start of [Module 1](your-first-windows-program.md).</span></span>

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

<span data-ttu-id="83729-158">Observe que el identificador de ventana se almacena en una variable miembro (*m \_ hWnd*), por lo que no es necesario pasarlo como un parámetro a `HandleMessage` .</span><span class="sxs-lookup"><span data-stu-id="83729-158">Notice that the window handle is stored in a member variable (*m\_hwnd*), so we do not need to pass it as a parameter to `HandleMessage`.</span></span>

<span data-ttu-id="83729-159">Muchos de los marcos de programación de Windows existentes, como Microsoft Foundation Classes (MFC) y Active Template Library (ATL), utilizan enfoques que son básicamente similares a los que se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="83729-159">Many of the existing Windows programming frameworks, such as Microsoft Foundation Classes (MFC) and Active Template Library (ATL), use approaches that are basically similar to the one shown here.</span></span> <span data-ttu-id="83729-160">Por supuesto, un marco totalmente generalizado como MFC es más complejo que este ejemplo relativamente simplista.</span><span class="sxs-lookup"><span data-stu-id="83729-160">Of course, a fully generalized framework such as MFC is more complex than this relatively simplistic example.</span></span>

## <a name="next"></a><span data-ttu-id="83729-161">Siguientes</span><span class="sxs-lookup"><span data-stu-id="83729-161">Next</span></span>

[<span data-ttu-id="83729-162">Módulo 2: usar COM en el programa de Windows</span><span class="sxs-lookup"><span data-stu-id="83729-162">Module 2: Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a><span data-ttu-id="83729-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83729-163">Related topics</span></span>

[<span data-ttu-id="83729-164">Ejemplo de BaseWindow</span><span class="sxs-lookup"><span data-stu-id="83729-164">BaseWindow Sample</span></span>](basewindow-sample.md)