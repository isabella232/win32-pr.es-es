---
title: Crear una ventana
description: Crear una ventana
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea5ec39187b389405d3c6d8eca475944278a3d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103973"
---
# <a name="creating-a-window"></a><span data-ttu-id="df620-103">Crear una ventana</span><span class="sxs-lookup"><span data-stu-id="df620-103">Creating a Window</span></span>

## <a name="window-classes"></a><span data-ttu-id="df620-104">Clases de ventanas</span><span class="sxs-lookup"><span data-stu-id="df620-104">Window Classes</span></span>

<span data-ttu-id="df620-105">Una *clase de* ventana define un conjunto de comportamientos que varias ventanas pueden tener en común.</span><span class="sxs-lookup"><span data-stu-id="df620-105">A *window class* defines a set of behaviors that several windows might have in common.</span></span> <span data-ttu-id="df620-106">Por ejemplo, en un grupo de botones, cada botón tiene un comportamiento similar cuando el usuario hace clic en él.</span><span class="sxs-lookup"><span data-stu-id="df620-106">For example, in a group of buttons, each button has a similar behavior when the user clicks the button.</span></span> <span data-ttu-id="df620-107">Por supuesto, los botones no son completamente idénticos; cada botón muestra su propia cadena de texto y tiene sus propias coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="df620-107">Of course, buttons are not completely identical; each button displays its own text string and has its own screen coordinates.</span></span> <span data-ttu-id="df620-108">Los datos que son únicos para cada ventana se denominan *datos de instancia.*</span><span class="sxs-lookup"><span data-stu-id="df620-108">Data that is unique for each window is called *instance data*.</span></span>

<span data-ttu-id="df620-109">Cada ventana debe estar asociada a una clase de ventana, incluso si el programa solo crea una instancia de esa clase.</span><span class="sxs-lookup"><span data-stu-id="df620-109">Every window must be associated with a window class, even if your program only ever creates one instance of that class.</span></span> <span data-ttu-id="df620-110">Es importante comprender que una clase de ventana no es una "clase" en el sentido de C++.</span><span class="sxs-lookup"><span data-stu-id="df620-110">It is important to understand that a window class is not a "class" in the C++ sense.</span></span> <span data-ttu-id="df620-111">En su lugar, es una estructura de datos utilizada internamente por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="df620-111">Rather, it is a data structure used internally by the operating system.</span></span> <span data-ttu-id="df620-112">Las clases de ventana se registran con el sistema en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="df620-112">Window classes are registered with the system at run time.</span></span> <span data-ttu-id="df620-113">Para registrar una nueva clase de ventana, comience rellenando una [**estructura WNDCLASS:**](/windows/win32/api/winuser/ns-winuser-wndclassa)</span><span class="sxs-lookup"><span data-stu-id="df620-113">To register a new window class, start by filling in a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure:</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

<span data-ttu-id="df620-114">Debe establecer los siguientes miembros de estructura:</span><span class="sxs-lookup"><span data-stu-id="df620-114">You must set the following structure members:</span></span>

- <span data-ttu-id="df620-115">**lpfnWndProc es** un puntero a una función definida por la aplicación denominada procedimiento *de* ventana o "procedimiento de ventana".</span><span class="sxs-lookup"><span data-stu-id="df620-115">**lpfnWndProc** is a pointer to an application-defined function called the *window procedure* or "window proc."</span></span> <span data-ttu-id="df620-116">El procedimiento de ventana define la mayor parte del comportamiento de la ventana.</span><span class="sxs-lookup"><span data-stu-id="df620-116">The window procedure defines most of the behavior of the window.</span></span> <span data-ttu-id="df620-117">Examinaremos el procedimiento de ventana con detalle más adelante.</span><span class="sxs-lookup"><span data-stu-id="df620-117">We'll examine the window procedure in detail later.</span></span> <span data-ttu-id="df620-118">Por ahora, solo tiene que tratar esto como una referencia hacia delante.</span><span class="sxs-lookup"><span data-stu-id="df620-118">For now, just treat this as a forward reference.</span></span>
- <span data-ttu-id="df620-119">**hInstance** es el identificador de la instancia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="df620-119">**hInstance** is the handle to the application instance.</span></span> <span data-ttu-id="df620-120">Obtenga este valor del *parámetro hInstance* de **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="df620-120">Get this value from the *hInstance* parameter of **wWinMain**.</span></span>
- <span data-ttu-id="df620-121">**lpszClassName es** una cadena que identifica la clase window.</span><span class="sxs-lookup"><span data-stu-id="df620-121">**lpszClassName** is a string that identifies the window class.</span></span>

<span data-ttu-id="df620-122">Los nombres de clase son locales para el proceso actual, por lo que el nombre solo debe ser único dentro del proceso.</span><span class="sxs-lookup"><span data-stu-id="df620-122">Class names are local to the current process, so the name only needs to be unique within the process.</span></span> <span data-ttu-id="df620-123">Sin embargo, los controles estándar de Windows también tienen clases.</span><span class="sxs-lookup"><span data-stu-id="df620-123">However, the standard Windows controls also have classes.</span></span> <span data-ttu-id="df620-124">Si usa cualquiera de esos controles, debe elegir nombres de clase que no entren en conflicto con los nombres de clase de control.</span><span class="sxs-lookup"><span data-stu-id="df620-124">If you use any of those controls, you must pick class names that do not conflict with the control class names.</span></span> <span data-ttu-id="df620-125">Por ejemplo, la clase de ventana para el control de botón se denomina "Button".</span><span class="sxs-lookup"><span data-stu-id="df620-125">For example, the window class for the button control is named "Button".</span></span>

<span data-ttu-id="df620-126">La [**estructura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) tiene otros miembros que no se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="df620-126">The [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure has other members not shown here.</span></span> <span data-ttu-id="df620-127">Puede establecerlos en cero, como se muestra en este ejemplo, o rellenarlos.</span><span class="sxs-lookup"><span data-stu-id="df620-127">You can set them to zero, as shown in this example, or fill them in.</span></span> <span data-ttu-id="df620-128">En la documentación de MSDN se describe la estructura en detalle.</span><span class="sxs-lookup"><span data-stu-id="df620-128">The MSDN documentation describes the structure in detail.</span></span>

<span data-ttu-id="df620-129">A continuación, pase la dirección de la [**estructura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) a [**la función RegisterClass.**](/windows/desktop/api/winuser/nf-winuser-registerclassa)</span><span class="sxs-lookup"><span data-stu-id="df620-129">Next, pass the address of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="df620-130">Esta función registra la clase de ventana con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="df620-130">This function registers the window class with the operating system.</span></span>

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a><span data-ttu-id="df620-131">Creación de la ventana</span><span class="sxs-lookup"><span data-stu-id="df620-131">Creating the Window</span></span>

<span data-ttu-id="df620-132">Para crear una nueva instancia de una ventana, llame a la [**función CreateWindowEx:**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)</span><span class="sxs-lookup"><span data-stu-id="df620-132">To create a new instance of a window, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function:</span></span>

```C++
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

<span data-ttu-id="df620-133">Puede leer descripciones detalladas de parámetros en MSDN, pero este es un resumen rápido:</span><span class="sxs-lookup"><span data-stu-id="df620-133">You can read detailed parameter descriptions on MSDN, but here is a quick summary:</span></span>

- <span data-ttu-id="df620-134">El primer parámetro le permite especificar algunos comportamientos opcionales para la ventana (por ejemplo, ventanas transparentes).</span><span class="sxs-lookup"><span data-stu-id="df620-134">The first parameter lets you specify some optional behaviors for the window (for example, transparent windows).</span></span> <span data-ttu-id="df620-135">Establezca este parámetro en cero para los comportamientos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="df620-135">Set this parameter to zero for the default behaviors.</span></span>
- <span data-ttu-id="df620-136">`CLASS_NAME` es el nombre de la clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="df620-136">`CLASS_NAME` is the name of the window class.</span></span> <span data-ttu-id="df620-137">Esto define el tipo de ventana que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="df620-137">This defines the type of window you are creating.</span></span>
- <span data-ttu-id="df620-138">Los distintos tipos de ventanas usan el texto de la ventana de maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="df620-138">The window text is used in different ways by different types of windows.</span></span> <span data-ttu-id="df620-139">Si la ventana tiene una barra de título, el texto se muestra en la barra de título.</span><span class="sxs-lookup"><span data-stu-id="df620-139">If the window has a title bar, the text is displayed in the title bar.</span></span>
- <span data-ttu-id="df620-140">El estilo de ventana es un conjunto de marcas que definen parte del aspecto de una ventana.</span><span class="sxs-lookup"><span data-stu-id="df620-140">The window style is a set of flags that define some of the look and feel of a window.</span></span> <span data-ttu-id="df620-141">La constante **WS \_ OVERLAPPEDWINDOW es** en realidad varias marcas combinadas con un OR bit a **bit.**</span><span class="sxs-lookup"><span data-stu-id="df620-141">The constant **WS\_OVERLAPPEDWINDOW** is actually several flags combined with a bitwise **OR**.</span></span> <span data-ttu-id="df620-142">Juntas, estas marcas dan a la ventana una barra de título, un borde, un menú del sistema y **los botones Minimizar** **y Maximizar.**</span><span class="sxs-lookup"><span data-stu-id="df620-142">Together these flags give the window a title bar, a border, a system menu, and **Minimize** and **Maximize** buttons.</span></span> <span data-ttu-id="df620-143">Este conjunto de marcas es el estilo más común para una ventana de aplicación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="df620-143">This set of flags is the most common style for a top-level application window.</span></span>
- <span data-ttu-id="df620-144">Para la posición y el tamaño, **la constante CW \_ USEDEFAULT** significa usar valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="df620-144">For position and size, the constant **CW\_USEDEFAULT** means to use default values.</span></span>
- <span data-ttu-id="df620-145">El parámetro siguiente establece una ventana primaria o una ventana de propietario para la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="df620-145">The next parameter sets a parent window or owner window for the new window.</span></span> <span data-ttu-id="df620-146">Establezca el elemento primario si va a crear una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="df620-146">Set the parent if you are creating a child window.</span></span> <span data-ttu-id="df620-147">Para una ventana de nivel superior, establezca esta opción en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="df620-147">For a top-level window, set this to **NULL**.</span></span>
- <span data-ttu-id="df620-148">Para una ventana de aplicación, el parámetro siguiente define el menú de la ventana.</span><span class="sxs-lookup"><span data-stu-id="df620-148">For an application window, the next parameter defines the menu for the window.</span></span> <span data-ttu-id="df620-149">En este ejemplo no se usa un menú, por lo que el valor es **NULL.**</span><span class="sxs-lookup"><span data-stu-id="df620-149">This example does not use a menu, so the value is **NULL**.</span></span>
- <span data-ttu-id="df620-150">*hInstance* es el identificador de instancia, descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="df620-150">*hInstance* is the instance handle, described previously.</span></span> <span data-ttu-id="df620-151">(Vea [WinMain: el punto de entrada de la aplicación).](winmain--the-application-entry-point.md)</span><span class="sxs-lookup"><span data-stu-id="df620-151">(See [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).)</span></span>
- <span data-ttu-id="df620-152">El último parámetro es un puntero a datos arbitrarios de tipo **void. \***</span><span class="sxs-lookup"><span data-stu-id="df620-152">The last parameter is a pointer to arbitrary data of type **void\***.</span></span> <span data-ttu-id="df620-153">Puede usar este valor para pasar una estructura de datos al procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="df620-153">You can use this value to pass a data structure to your window procedure.</span></span> <span data-ttu-id="df620-154">Mostraremos una posible manera de usar este parámetro en la sección [Administración del estado de la aplicación](managing-application-state-.md).</span><span class="sxs-lookup"><span data-stu-id="df620-154">We'll show one possible way to use this parameter in the section [Managing Application State](managing-application-state-.md).</span></span>

<span data-ttu-id="df620-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) devuelve un identificador a la nueva ventana o cero si se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="df620-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) returns a handle to the new window, or zero if the function fails.</span></span> <span data-ttu-id="df620-156">Para mostrar la ventana, es decir, hacer que la ventana sea visible, pase el identificador de ventana a la [**función ShowWindow:**](/windows/desktop/api/winuser/nf-winuser-showwindow)</span><span class="sxs-lookup"><span data-stu-id="df620-156">To show the window—that is, make the window visible —pass the window handle to the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function:</span></span>

```C++
ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="df620-157">El *parámetro hwnd* es el identificador de ventana devuelto [**por CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)</span><span class="sxs-lookup"><span data-stu-id="df620-157">The *hwnd* parameter is the window handle returned by [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="df620-158">El *parámetro nCmdShow* se puede usar para minimizar o maximizar una ventana.</span><span class="sxs-lookup"><span data-stu-id="df620-158">The *nCmdShow* parameter can be used to minimize or maximize a window.</span></span> <span data-ttu-id="df620-159">El sistema operativo pasa este valor al programa a través de la **función wWinMain.**</span><span class="sxs-lookup"><span data-stu-id="df620-159">The operating system passes this value to the program through the **wWinMain** function.</span></span>

<span data-ttu-id="df620-160">Este es el código completo para crear la ventana.</span><span class="sxs-lookup"><span data-stu-id="df620-160">Here is the complete code to create the window.</span></span> <span data-ttu-id="df620-161">Recuerde que `WindowProc` sigue siendo simplemente una declaración adelantada de una función.</span><span class="sxs-lookup"><span data-stu-id="df620-161">Remember that `WindowProc` is still just a forward declaration of a function.</span></span>

```C++
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

<span data-ttu-id="df620-162">Enhorabuena, ha creado una ventana.</span><span class="sxs-lookup"><span data-stu-id="df620-162">Congratulations, you've created a window!</span></span> <span data-ttu-id="df620-163">En este momento, la ventana no contiene ningún contenido ni interactúa con el usuario.</span><span class="sxs-lookup"><span data-stu-id="df620-163">Right now, the window does not contain any content or interact with the user.</span></span> <span data-ttu-id="df620-164">En una aplicación de GUI real, la ventana respondería a eventos del usuario y del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="df620-164">In a real GUI application, the window would respond to events from the user and the operating system.</span></span> <span data-ttu-id="df620-165">En la sección siguiente se describe cómo los mensajes de ventana proporcionan este tipo de interactividad.</span><span class="sxs-lookup"><span data-stu-id="df620-165">The next section describes how window messages provide this sort of interactivity.</span></span>

### <a name="next"></a><span data-ttu-id="df620-166">Siguientes</span><span class="sxs-lookup"><span data-stu-id="df620-166">Next</span></span>

[<span data-ttu-id="df620-167">Mensajes de ventana</span><span class="sxs-lookup"><span data-stu-id="df620-167">Window Messages</span></span>](window-messages.md)
