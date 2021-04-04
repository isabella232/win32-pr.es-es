---
title: Usar aceleradores de teclado
description: En esta sección se describen las tareas que están asociadas a los aceleradores de teclado.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- entrada de usuario, aceleradores de teclado
- captura de entradas de usuario, aceleradores de teclado
- aceleradores de teclado
- aceleradores
- tablas de aceleradores
- 'Acelerador: recursos de tabla'
- translate (función de acelerador)
- Mensaje WM_COMMAND
- WM_SYS mensaje de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077739"
---
# <a name="using-keyboard-accelerators"></a><span data-ttu-id="eb5aa-112">Usar aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="eb5aa-112">Using Keyboard Accelerators</span></span>

<span data-ttu-id="eb5aa-113">En esta sección se describen las tareas que están asociadas a los aceleradores de teclado.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-113">This section covers tasks that are associated with keyboard accelerators.</span></span>

-   [<span data-ttu-id="eb5aa-114">Uso de un recurso de tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="eb5aa-114">Using an Accelerator Table Resource</span></span>](#using-an-accelerator-table-resource)
    -   [<span data-ttu-id="eb5aa-115">Crear el recurso de tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="eb5aa-115">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
    -   [<span data-ttu-id="eb5aa-116">Cargar el recurso de tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="eb5aa-116">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
    -   [<span data-ttu-id="eb5aa-117">Llamar a la función de acelerador translate</span><span class="sxs-lookup"><span data-stu-id="eb5aa-117">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
    -   [<span data-ttu-id="eb5aa-118">Procesamiento de \_ mensajes de comandos de WM</span><span class="sxs-lookup"><span data-stu-id="eb5aa-118">Processing WM\_COMMAND Messages</span></span>](/windows)
    -   [<span data-ttu-id="eb5aa-119">Destruir el recurso de tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="eb5aa-119">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
    -   [<span data-ttu-id="eb5aa-120">Crear aceleradores para atributos de fuente</span><span class="sxs-lookup"><span data-stu-id="eb5aa-120">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)
-   [<span data-ttu-id="eb5aa-121">Usar una tabla de aceleradores creada en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="eb5aa-121">Using an Accelerator Table Created at Run Time</span></span>](#using-an-accelerator-table-created-at-run-time)
    -   [<span data-ttu-id="eb5aa-122">Creación de una tabla de aceleradores de Run-Time</span><span class="sxs-lookup"><span data-stu-id="eb5aa-122">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
    -   [<span data-ttu-id="eb5aa-123">Aceleradores de procesamiento</span><span class="sxs-lookup"><span data-stu-id="eb5aa-123">Processing Accelerators</span></span>](#processing-accelerators)
    -   [<span data-ttu-id="eb5aa-124">Destruir una tabla de aceleradores de Run-Time</span><span class="sxs-lookup"><span data-stu-id="eb5aa-124">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
    -   [<span data-ttu-id="eb5aa-125">Creación de aceleradores editables por el usuario</span><span class="sxs-lookup"><span data-stu-id="eb5aa-125">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a><span data-ttu-id="eb5aa-126">Uso de un recurso de tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="eb5aa-126">Using an Accelerator Table Resource</span></span>

<span data-ttu-id="eb5aa-127">La forma más común de agregar compatibilidad con el acelerador a una aplicación consiste en incluir un recurso de tabla de aceleradores con el archivo ejecutable de la aplicación y, a continuación, cargar el recurso en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-127">The most common way to add accelerator support to an application is to include an accelerator-table resource with the application's executable file and then load the resource at run time.</span></span>

<span data-ttu-id="eb5aa-128">En esta sección se tratan los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-128">This section covers the following topics.</span></span>

-   [<span data-ttu-id="eb5aa-129">Crear el recurso de tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="eb5aa-129">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
-   [<span data-ttu-id="eb5aa-130">Cargar el recurso de tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="eb5aa-130">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
-   [<span data-ttu-id="eb5aa-131">Llamar a la función de acelerador translate</span><span class="sxs-lookup"><span data-stu-id="eb5aa-131">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
-   [<span data-ttu-id="eb5aa-132">Procesamiento de \_ mensajes de comandos de WM</span><span class="sxs-lookup"><span data-stu-id="eb5aa-132">Processing WM\_COMMAND Messages</span></span>](/windows)
-   [<span data-ttu-id="eb5aa-133">Destruir el recurso de tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="eb5aa-133">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
-   [<span data-ttu-id="eb5aa-134">Crear aceleradores para atributos de fuente</span><span class="sxs-lookup"><span data-stu-id="eb5aa-134">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a><span data-ttu-id="eb5aa-135">Crear el recurso de tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="eb5aa-135">Creating the Accelerator Table Resource</span></span>

<span data-ttu-id="eb5aa-136">Cree un recurso de tabla de aceleradores mediante la instrucción [Accelerators](./accelerators-resource.md) en el archivo de definición de recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-136">You create an accelerator-table resource by using the [ACCELERATORS](./accelerators-resource.md) statement in your application's resource-definition file.</span></span> <span data-ttu-id="eb5aa-137">Debe asignar un nombre o un identificador de recurso a la tabla de aceleradores, preferiblemente a diferencia de la de cualquier otro recurso.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-137">You must assign a name or resource identifier to the accelerator table, preferably unlike that of any other resource.</span></span> <span data-ttu-id="eb5aa-138">El sistema utiliza este identificador para cargar el recurso en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-138">The system uses this identifier to load the resource at run time.</span></span>

<span data-ttu-id="eb5aa-139">Cada acelerador que defina requiere una entrada independiente en la tabla de aceleradores.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-139">Each accelerator you define requires a separate entry in the accelerator table.</span></span> <span data-ttu-id="eb5aa-140">En cada entrada, se define la pulsación de tecla (un código de carácter ASCII o un código de tecla virtual) que genera el acelerador y el identificador del acelerador.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-140">In each entry, you define the keystroke (either an ASCII character code or virtual-key code) that generates the accelerator and the accelerator's identifier.</span></span> <span data-ttu-id="eb5aa-141">También debe especificar si se debe utilizar la pulsación de tecla en alguna combinación con las teclas ALT, Mayús o CTRL.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-141">You must also specify whether the keystroke must be used in some combination with the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="eb5aa-142">Para obtener más información acerca de las claves virtuales, consulte [entrada de teclado](/windows/desktop/inputdev/keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="eb5aa-142">For more information about virtual keys, see [Keyboard Input](/windows/desktop/inputdev/keyboard-input).</span></span>

<span data-ttu-id="eb5aa-143">Una pulsación de tecla ASCII se especifica mediante la inclusión del carácter ASCII entre comillas dobles o mediante el valor entero del carácter en combinación con la marca ASCII.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-143">An ASCII keystroke is specified either by enclosing the ASCII character in double quotation marks or by using the integer value of the character in combination with the ASCII flag.</span></span> <span data-ttu-id="eb5aa-144">En los siguientes ejemplos se muestra cómo definir aceleradores ASCII.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-144">The following examples show how to define ASCII accelerators.</span></span>

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

<span data-ttu-id="eb5aa-145">Una pulsación de tecla de código de tecla virtual se especifica de manera diferente en función de si la pulsación de tecla es una clave alfanumérica o una clave no alfanumérica.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-145">A virtual-key code keystroke is specified differently depending on whether the keystroke is an alphanumeric key or a non-alphanumeric key.</span></span> <span data-ttu-id="eb5aa-146">En el caso de una clave alfanumérica, la letra o el número de la clave, entre comillas dobles, se combina con la marca **VIRTKEY** .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-146">For an alphanumeric key, the key's letter or number, enclosed in double quotation marks, is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="eb5aa-147">En el caso de una clave no alfanumérica, el código de la clave virtual para la clave específica se combina con la marca **VIRTKEY** .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-147">For a non-alphanumeric key, the virtual-key code for the specific key is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="eb5aa-148">En los siguientes ejemplos se muestra cómo definir aceleradores de código de clave virtual.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-148">The following examples show how to define virtual-key code accelerators.</span></span>

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

<span data-ttu-id="eb5aa-149">En el ejemplo siguiente se muestra un recurso de tabla de aceleradores que define los aceleradores para las operaciones de archivos.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-149">The following example shows an accelerator-table resource that defines accelerators for file operations.</span></span> <span data-ttu-id="eb5aa-150">El nombre del recurso es *FileAccel*.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-150">The name of the resource is *FileAccel*.</span></span>

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

<span data-ttu-id="eb5aa-151">Si desea que el usuario presione las teclas ALT, Mayús o CTRL en alguna combinación con la pulsación de tecla del acelerador, especifique las marcas ALT, Mayús y CONTROL en la definición del acelerador.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-151">If you want the user to press the ALT, SHIFT, or CTRL keys in some combination with the accelerator keystroke, specify the ALT, SHIFT, and CONTROL flags in the accelerator's definition.</span></span> <span data-ttu-id="eb5aa-152">A continuación se muestran algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-152">Following are some examples.</span></span>

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

<span data-ttu-id="eb5aa-153">De forma predeterminada, cuando una tecla de aceleración corresponde a un elemento de menú, el sistema resalta el elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-153">By default, when an accelerator key corresponds to a menu item, the system highlights the menu item.</span></span> <span data-ttu-id="eb5aa-154">Puede usar la marca **noinvertir** para evitar el resaltado de un acelerador individual.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-154">You can use the **NOINVERT** flag to prevent highlighting for an individual accelerator.</span></span> <span data-ttu-id="eb5aa-155">En el ejemplo siguiente se muestra cómo usar la marca **Invert** :</span><span class="sxs-lookup"><span data-stu-id="eb5aa-155">The following example shows how to use the **NOINVERT** flag:</span></span>

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

<span data-ttu-id="eb5aa-156">Para definir los aceleradores que corresponden a los elementos de menú de la aplicación, incluya los aceleradores en el texto de los elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-156">To define accelerators that correspond to menu items in your application, include the accelerators in the text of the menu items.</span></span> <span data-ttu-id="eb5aa-157">En el ejemplo siguiente se muestra cómo incluir los aceleradores en el texto de elementos de menú en un archivo de definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-157">The following example shows how to include accelerators in menu-item text in a resource-definition file.</span></span>

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a><span data-ttu-id="eb5aa-158">Cargar el recurso de tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="eb5aa-158">Loading the Accelerator Table Resource</span></span>

<span data-ttu-id="eb5aa-159">Una aplicación carga un recurso de tabla de aceleradores mediante una llamada a la función [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) y especificando el identificador de instancia de la aplicación cuyo archivo ejecutable contiene el recurso y el nombre o el identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-159">An application loads an accelerator-table resource by calling the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function and specifying the instance handle to the application whose executable file contains the resource and the name or identifier of the resource.</span></span> <span data-ttu-id="eb5aa-160">**LoadAccelerators** carga la tabla de aceleradores especificada en la memoria y devuelve el identificador a la tabla de aceleradores.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-160">**LoadAccelerators** loads the specified accelerator table into memory and returns the handle to the accelerator table.</span></span>

<span data-ttu-id="eb5aa-161">Una aplicación puede cargar un recurso de tabla de aceleradores en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-161">An application can load an accelerator-table resource at any time.</span></span> <span data-ttu-id="eb5aa-162">Normalmente, una aplicación de un solo subproceso carga su tabla de aceleradores antes de escribir su bucle de mensajes principal.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-162">Usually, a single-threaded application loads its accelerator table before entering its main message loop.</span></span> <span data-ttu-id="eb5aa-163">Una aplicación que usa varios subprocesos normalmente carga el recurso de tabla de aceleradores para un subproceso antes de escribir el bucle de mensajes para el subproceso.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-163">An application that uses multiple threads typically loads the accelerator-table resource for a thread before entering the message loop for the thread.</span></span> <span data-ttu-id="eb5aa-164">Una aplicación o un subproceso también puede usar varias tablas de aceleradores, cada una de las cuales está asociada a una ventana determinada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-164">An application or thread might also use multiple accelerator tables, each associated with a particular window in the application.</span></span> <span data-ttu-id="eb5aa-165">Este tipo de aplicación cargaría la tabla de aceleradores para la ventana cada vez que el usuario activara la ventana.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-165">Such an application would load the accelerator table for the window each time the user activated the window.</span></span> <span data-ttu-id="eb5aa-166">Para obtener más información sobre los subprocesos, vea [procesos y subprocesos](/windows/desktop/ProcThread/processes-and-threads).</span><span class="sxs-lookup"><span data-stu-id="eb5aa-166">For more information about threads, see [Processes and Threads](/windows/desktop/ProcThread/processes-and-threads).</span></span>

### <a name="calling-the-translate-accelerator-function"></a><span data-ttu-id="eb5aa-167">Llamar a la función de acelerador translate</span><span class="sxs-lookup"><span data-stu-id="eb5aa-167">Calling the Translate Accelerator Function</span></span>

<span data-ttu-id="eb5aa-168">Para procesar aceleradores, el bucle de mensajes de una aplicación (o del subproceso) debe contener una llamada a la función [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-168">To process accelerators, an application's (or thread's) message loop must contain a call to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function.</span></span> <span data-ttu-id="eb5aa-169">**TranslateAccelerator** compara las pulsaciones de teclas con una tabla de aceleradores y, si encuentra una coincidencia, traduce las pulsaciones de teclas en un mensaje de [**\_ comando WM**](wm-command.md) (o [**WM \_ SYSCOMMAND**](wm-syscommand.md)).</span><span class="sxs-lookup"><span data-stu-id="eb5aa-169">**TranslateAccelerator** compares keystrokes to an accelerator table and, if it finds a match, translates the keystrokes into a [**WM\_COMMAND**](wm-command.md) (or [**WM\_SYSCOMMAND**](wm-syscommand.md)) message.</span></span> <span data-ttu-id="eb5aa-170">A continuación, la función envía el mensaje a un procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-170">The function then sends the message to a window procedure.</span></span> <span data-ttu-id="eb5aa-171">Los parámetros de la función **TranslateAccelerator** incluyen el identificador de la ventana que va a recibir los mensajes de **\_ comandos de WM** , el identificador de la tabla de aceleradores que se usa para traducir los aceleradores y un puntero a una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) que contiene un mensaje de la cola.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-171">The parameters of the **TranslateAccelerator** function include the handle to the window that is to receive the **WM\_COMMAND** messages, the handle to the accelerator table used to translate accelerators, and a pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure containing a message from the queue.</span></span> <span data-ttu-id="eb5aa-172">En el ejemplo siguiente se muestra cómo llamar a **TranslateAccelerator** desde dentro de un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-172">The following example shows how to call **TranslateAccelerator** from within a message loop.</span></span>


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a><span data-ttu-id="eb5aa-173">Procesamiento de \_ mensajes de comandos de WM</span><span class="sxs-lookup"><span data-stu-id="eb5aa-173">Processing WM\_COMMAND Messages</span></span>

<span data-ttu-id="eb5aa-174">Cuando se utiliza un acelerador, la ventana especificada en la función [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) recibe [**un \_ comando de WM**](wm-command.md) o un mensaje de [**\_ SYSCOMMAND de WM**](wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-174">When an accelerator is used, the window specified in the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function receives a [**WM\_COMMAND**](wm-command.md) or [**WM\_SYSCOMMAND**](wm-syscommand.md) message.</span></span> <span data-ttu-id="eb5aa-175">La palabra de orden inferior del parámetro *wParam* contiene el identificador del acelerador.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-175">The low-order word of the *wParam* parameter contains the identifier of the accelerator.</span></span> <span data-ttu-id="eb5aa-176">El procedimiento de ventana examina el identificador para determinar el origen del mensaje de **\_ comando de WM** y procesar el mensaje en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-176">The window procedure examines the identifier to determine the source of the **WM\_COMMAND** message and process the message accordingly.</span></span>

<span data-ttu-id="eb5aa-177">Normalmente, si un acelerador corresponde a un elemento de menú de la aplicación, se asigna el mismo identificador al acelerador y al elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-177">Typically, if an accelerator corresponds to a menu item in the application, the accelerator and menu item are assigned the same identifier.</span></span> <span data-ttu-id="eb5aa-178">Si necesita saber si un mensaje de [**\_ comando de WM**](wm-command.md) se generó mediante un acelerador o un elemento de menú, puede examinar la palabra de orden superior del parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-178">If you need to know whether a [**WM\_COMMAND**](wm-command.md) message was generated by an accelerator or by a menu item, you can examine the high-order word of the *wParam* parameter.</span></span> <span data-ttu-id="eb5aa-179">Si un acelerador generó el mensaje, la palabra de orden superior es 1; Si un elemento de menú ha generado el mensaje, la palabra de orden superior es 0.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-179">If an accelerator generated the message, the high-order word is 1; if a menu item generated the message, the high-order word is 0.</span></span>

### <a name="destroying-the-accelerator-table-resource"></a><span data-ttu-id="eb5aa-180">Destruir el recurso de tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="eb5aa-180">Destroying the Accelerator Table Resource</span></span>

<span data-ttu-id="eb5aa-181">El sistema destruye automáticamente los recursos de la tabla de aceleradores cargados por la función [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , quitando el recurso de la memoria después de que se cierre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-181">The system automatically destroys accelerator-table resources loaded by the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function, removing the resource from memory after the application closes.</span></span>

### <a name="creating-accelerators-for-font-attributes"></a><span data-ttu-id="eb5aa-182">Crear aceleradores para atributos de fuente</span><span class="sxs-lookup"><span data-stu-id="eb5aa-182">Creating Accelerators for Font Attributes</span></span>

<span data-ttu-id="eb5aa-183">En el ejemplo de esta sección se muestra cómo realizar las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="eb5aa-183">The example in this section shows how to perform the following tasks:</span></span>

-   <span data-ttu-id="eb5aa-184">Cree un recurso de tabla de aceleradores.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-184">Create an accelerator-table resource.</span></span>
-   <span data-ttu-id="eb5aa-185">Cargue la tabla de aceleradores en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-185">Load the accelerator table at run time.</span></span>
-   <span data-ttu-id="eb5aa-186">Traduzca los aceleradores en un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-186">Translate accelerators in a message loop.</span></span>
-   <span data-ttu-id="eb5aa-187">Procese los mensajes de [**\_ comandos de WM**](wm-command.md) generados por los aceleradores.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-187">Process [**WM\_COMMAND**](wm-command.md) messages generated by the accelerators.</span></span>

<span data-ttu-id="eb5aa-188">Estas tareas se muestran en el contexto de una aplicación que incluye un menú de **caracteres** y los aceleradores correspondientes que permiten al usuario seleccionar atributos de la fuente actual.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-188">These tasks are demonstrated in the context of an application that includes a **Character** menu and corresponding accelerators that allow the user to select attributes of the current font.</span></span>

<span data-ttu-id="eb5aa-189">La siguiente parte de un archivo de definición de recursos define el menú de **caracteres** y la tabla de aceleradores asociada.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-189">The following portion of a resource-definition file defines the **Character** menu and the associated accelerator table.</span></span> <span data-ttu-id="eb5aa-190">Tenga en cuenta que los elementos de menú muestran las pulsaciones de teclas de aceleración y que cada acelerador tiene el mismo identificador que el elemento de menú asociado.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-190">Note that the menu items show the accelerator keystrokes and that each accelerator has the same identifier as its associated menu item.</span></span>


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



<span data-ttu-id="eb5aa-191">En las secciones siguientes del archivo de código fuente de la aplicación se muestra cómo implementar los aceleradores.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-191">The following sections from the application's source file show how to implement the accelerators.</span></span>


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a><span data-ttu-id="eb5aa-192">Usar una tabla de aceleradores creada en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="eb5aa-192">Using an Accelerator Table Created at Run Time</span></span>

<span data-ttu-id="eb5aa-193">En este tema se describe cómo usar las tablas de aceleradores creadas en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-193">This topic discusses how to use accelerator tables created at run time.</span></span>

-   [<span data-ttu-id="eb5aa-194">Creación de una tabla de aceleradores de Run-Time</span><span class="sxs-lookup"><span data-stu-id="eb5aa-194">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
-   [<span data-ttu-id="eb5aa-195">Aceleradores de procesamiento</span><span class="sxs-lookup"><span data-stu-id="eb5aa-195">Processing Accelerators</span></span>](#processing-accelerators)
-   [<span data-ttu-id="eb5aa-196">Destruir una tabla de aceleradores de Run-Time</span><span class="sxs-lookup"><span data-stu-id="eb5aa-196">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
-   [<span data-ttu-id="eb5aa-197">Creación de aceleradores editables por el usuario</span><span class="sxs-lookup"><span data-stu-id="eb5aa-197">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a><span data-ttu-id="eb5aa-198">Creación de una tabla de aceleradores de Run-Time</span><span class="sxs-lookup"><span data-stu-id="eb5aa-198">Creating a Run-Time Accelerator Table</span></span>

<span data-ttu-id="eb5aa-199">El primer paso para crear una tabla de aceleradores en tiempo de ejecución es llenar una matriz de estructuras de [**aceleración**](/windows/win32/api/winuser/ns-winuser-accel) .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-199">The first step in creating an accelerator table at run time is filling an array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures.</span></span> <span data-ttu-id="eb5aa-200">Cada estructura de la matriz define un acelerador en la tabla.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-200">Each structure in the array defines an accelerator in the table.</span></span> <span data-ttu-id="eb5aa-201">La definición de un acelerador incluye sus marcas, su clave y su identificador.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-201">An accelerator's definition includes its flags, its key, and its identifier.</span></span> <span data-ttu-id="eb5aa-202">La estructura de **aceleración** tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-202">The **ACCEL** structure has the following form.</span></span>

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

<span data-ttu-id="eb5aa-203">Para definir la pulsación de tecla del acelerador, especifique un código de carácter ASCII o un código de clave virtual en el miembro **clave** de la estructura de [**aceleración**](/windows/win32/api/winuser/ns-winuser-accel) .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-203">You define an accelerator's keystroke by specifying an ASCII character code or a virtual-key code in the **key** member of the [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structure.</span></span> <span data-ttu-id="eb5aa-204">Si especifica un código de tecla virtual, primero debe incluir la marca **FVIRTKEY** en el miembro **fVirt** ; de lo contrario, el sistema interpreta el código como un código de carácter ASCII.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-204">If you specify a virtual-key code, you must first include the **FVIRTKEY** flag in the **fVirt** member; otherwise, the system interprets the code as an ASCII character code.</span></span> <span data-ttu-id="eb5aa-205">Puede incluir las marcas **FCONTROL**, **FALT** o **FSHIFT** , o las tres, para combinar las teclas Ctrl, Alt o Mayús con la pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-205">You can include the **FCONTROL**, **FALT**, or **FSHIFT** flag, or all three, to combine the CTRL, ALT, or SHIFT key with the keystroke.</span></span>

<span data-ttu-id="eb5aa-206">Para crear la tabla de aceleradores, pase un puntero a la matriz de estructuras de [**aceleración**](/windows/win32/api/winuser/ns-winuser-accel) a la función [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-206">To create the accelerator table, pass a pointer to the array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures to the [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) function.</span></span> <span data-ttu-id="eb5aa-207">**CreateAcceleratorTable** crea la tabla de aceleradores y devuelve el identificador de la tabla.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-207">**CreateAcceleratorTable** creates the accelerator table and returns the handle to the table.</span></span>

### <a name="processing-accelerators"></a><span data-ttu-id="eb5aa-208">Aceleradores de procesamiento</span><span class="sxs-lookup"><span data-stu-id="eb5aa-208">Processing Accelerators</span></span>

<span data-ttu-id="eb5aa-209">El proceso de cargar y llamar a los aceleradores proporcionados por una tabla de aceleradores creada en tiempo de ejecución es igual que el procesamiento de los proporcionados por un recurso de tabla de aceleradores.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-209">The process of loading and calling accelerators provided by an accelerator table created at run time is the same as processing those provided by an accelerator-table resource.</span></span> <span data-ttu-id="eb5aa-210">Para obtener más información, vea [cargar el recurso de tabla de aceleradores](#loading-the-accelerator-table-resource) mediante el [procesamiento de mensajes de \_ comandos de WM](/windows).</span><span class="sxs-lookup"><span data-stu-id="eb5aa-210">For more information, see [Loading the Accelerator Table Resource](#loading-the-accelerator-table-resource) through [Processing WM\_COMMAND Messages](/windows).</span></span>

### <a name="destroying-a-run-time-accelerator-table"></a><span data-ttu-id="eb5aa-211">Destruir una tabla de aceleradores de Run-Time</span><span class="sxs-lookup"><span data-stu-id="eb5aa-211">Destroying a Run-Time Accelerator Table</span></span>

<span data-ttu-id="eb5aa-212">El sistema destruye automáticamente las tablas de acelerador creadas en tiempo de ejecución y quita los recursos de la memoria después de que se cierre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-212">The system automatically destroys accelerator tables created at run time, removing the resources from memory after the application closes.</span></span> <span data-ttu-id="eb5aa-213">Puede destruir una tabla de aceleradores y quitarla de la memoria antes si pasa el identificador de la tabla a la función [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-213">You can destroy an accelerator table and remove it from memory earlier by passing the table's handle to the [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) function.</span></span>

### <a name="creating-user-editable-accelerators"></a><span data-ttu-id="eb5aa-214">Creación de aceleradores editables por el usuario</span><span class="sxs-lookup"><span data-stu-id="eb5aa-214">Creating User Editable Accelerators</span></span>

<span data-ttu-id="eb5aa-215">En este ejemplo se muestra cómo crear un cuadro de diálogo que permite al usuario cambiar el acelerador asociado a un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-215">This example shows how to construct a dialog box that allows the user to change the accelerator associated with a menu item.</span></span> <span data-ttu-id="eb5aa-216">El cuadro de diálogo se compone de un cuadro combinado que contiene elementos de menú, un cuadro combinado que contiene los nombres de las teclas y casillas para seleccionar las teclas CTRL, ALT y Mayús.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-216">The dialog box consists of a combo box containing menu items, a combo box containing the names of keys, and check boxes for selecting the CTRL, ALT, and SHIFT keys.</span></span> <span data-ttu-id="eb5aa-217">En la ilustración siguiente se muestra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-217">The following illustration shows the dialog box.</span></span>

![cuadro de diálogo con cuadros combinados y casillas](images/useredit.gif)

<span data-ttu-id="eb5aa-219">En el ejemplo siguiente se muestra cómo se define el cuadro de diálogo en el archivo de definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-219">The following example shows how the dialog box is defined in the resource-definition file.</span></span>

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

<span data-ttu-id="eb5aa-220">La barra de menús de la aplicación contiene un submenú de **caracteres** cuyos elementos tienen aceleradores asociados.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-220">The application's menu bar contains a **Character** submenu whose items have accelerators associated with them.</span></span>

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

<span data-ttu-id="eb5aa-221">Los valores de elemento de menú de la plantilla de menú son constantes que se definen como se indica a continuación en el archivo de encabezado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-221">The menu item values for the menu template are constants defined as follows in the application's header file.</span></span>

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

<span data-ttu-id="eb5aa-222">El cuadro de diálogo utiliza una matriz de estructuras VKEY definidas por la aplicación, cada una de las cuales contiene una cadena de texto de pulsación de tecla y una cadena de texto acelerador.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-222">The dialog box uses an array of application-defined VKEY structures, each containing a keystroke-text string and an accelerator-text string.</span></span> <span data-ttu-id="eb5aa-223">Cuando se crea el cuadro de diálogo, analiza la matriz y agrega cada cadena de texto de pulsación de tecla al cuadro combinado de **pulsación de tecla** .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-223">When the dialog box is created, it parses the array and adds each keystroke-text string to the **Select Keystroke** combo box.</span></span> <span data-ttu-id="eb5aa-224">Cuando el usuario hace clic en el botón **Aceptar** , el cuadro de diálogo busca la cadena de texto de pulsación de tecla seleccionada y recupera la cadena de texto de acelerador correspondiente.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-224">When the user clicks the **OK** button, the dialog box looks up the selected keystroke-text string and retrieves the corresponding accelerator-text string.</span></span> <span data-ttu-id="eb5aa-225">El cuadro de diálogo anexa la cadena de texto del acelerador al texto del elemento de menú seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-225">The dialog box appends the accelerator-text string to the text of the menu item that the user selected.</span></span> <span data-ttu-id="eb5aa-226">En el ejemplo siguiente se muestra la matriz de estructuras VKEY:</span><span class="sxs-lookup"><span data-stu-id="eb5aa-226">The following example shows the array of VKEY structures:</span></span>


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



<span data-ttu-id="eb5aa-227">El procedimiento de inicialización del cuadro de diálogo rellena los cuadros de la combinación **Seleccionar elemento** y **seleccionar pulsación de tecla** .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-227">The dialog box's initialization procedure fills the **Select Item** and **Select Keystroke** combo boxes.</span></span> <span data-ttu-id="eb5aa-228">Una vez que el usuario selecciona un elemento de menú y el acelerador asociado, el cuadro de diálogo examina los controles del cuadro de diálogo para obtener la selección del usuario, actualiza el texto del elemento de menú y, a continuación, crea una nueva tabla de aceleradores que contiene el nuevo acelerador definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-228">After the user selects a menu item and associated accelerator, the dialog box examines the controls in the dialog box to get the user's selection, updates the text of the menu item, and then creates a new accelerator table that contains the user-defined new accelerator.</span></span> <span data-ttu-id="eb5aa-229">En el ejemplo siguiente se muestra el procedimiento de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-229">The following example shows the dialog-box procedure.</span></span> <span data-ttu-id="eb5aa-230">Tenga en cuenta que debe inicializar en el procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-230">Note that you must initialize in your window procedure.</span></span>


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 