---
title: Uso de los menús
description: En esta sección se proporcionan ejemplos de código para tareas relacionadas con menús.
ms.assetid: b1391e37-a146-46ec-a329-aa57cfcfd351
keywords:
- recursos, menús
- menús, crear
- recursos de plantilla de menú
- recursos, menú-plantilla
- formato de plantilla de menú extendido
- formato de plantilla de menú anterior
- cargar recursos de plantilla de menú
- menús, clase
- menús, acceso directo
- crear menús
- menús de clase
- menús contextuales
- mapas de bits de elementos de menú
- menús, dibujado por el propietario
- menús dibujados por el propietario
- mapas de bits de marcas de verificación personalizadas
- menús, casillas
- menús, fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d216b5fe5e6c25a98b5bdf3abe9d55b4bb0b34f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791212"
---
# <a name="using-menus"></a><span data-ttu-id="2ae81-121">Uso de los menús</span><span class="sxs-lookup"><span data-stu-id="2ae81-121">Using Menus</span></span>

<span data-ttu-id="2ae81-122">En esta sección se describen las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="2ae81-122">This section describes the following tasks:</span></span>

-   [<span data-ttu-id="2ae81-123">Uso de un recurso de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="2ae81-123">Using a Menu-Template Resource</span></span>](#using-a-menu-template-resource)
    -   [<span data-ttu-id="2ae81-124">Formato de Menu-Template extendido</span><span class="sxs-lookup"><span data-stu-id="2ae81-124">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
    -   [<span data-ttu-id="2ae81-125">Formato de Menu-Template anterior</span><span class="sxs-lookup"><span data-stu-id="2ae81-125">Old Menu-Template Format</span></span>](#old-menu-template-format)
    -   [<span data-ttu-id="2ae81-126">Cargar un recurso de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="2ae81-126">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
    -   [<span data-ttu-id="2ae81-127">Crear un menú de clase</span><span class="sxs-lookup"><span data-stu-id="2ae81-127">Creating a Class Menu</span></span>](#creating-a-class-menu)
-   [<span data-ttu-id="2ae81-128">Crear un menú contextual</span><span class="sxs-lookup"><span data-stu-id="2ae81-128">Creating a Shortcut Menu</span></span>](#creating-a-shortcut-menu)
    -   [<span data-ttu-id="2ae81-129">Procesamiento del mensaje de CONTEXTMENU de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-129">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
    -   [<span data-ttu-id="2ae81-130">Crear un menú contextual Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="2ae81-130">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
    -   [<span data-ttu-id="2ae81-131">Mostrar un menú contextual</span><span class="sxs-lookup"><span data-stu-id="2ae81-131">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)
-   [<span data-ttu-id="2ae81-132">Usar mapas de bits de Menu-Item</span><span class="sxs-lookup"><span data-stu-id="2ae81-132">Using Menu-Item Bitmaps</span></span>](#using-menu-item-bitmaps)
    -   [<span data-ttu-id="2ae81-133">Establecer la marca de tipo de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="2ae81-133">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
    -   [<span data-ttu-id="2ae81-134">Crear el mapa de bits</span><span class="sxs-lookup"><span data-stu-id="2ae81-134">Creating the Bitmap</span></span>](#creating-the-bitmap)
    -   [<span data-ttu-id="2ae81-135">Agregar líneas y gráficos a un menú</span><span class="sxs-lookup"><span data-stu-id="2ae81-135">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
    -   [<span data-ttu-id="2ae81-136">Ejemplo de mapas de bits de Menu-Item</span><span class="sxs-lookup"><span data-stu-id="2ae81-136">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)
-   [<span data-ttu-id="2ae81-137">Crear Owner-Drawn elementos de menú</span><span class="sxs-lookup"><span data-stu-id="2ae81-137">Creating Owner-Drawn Menu Items</span></span>](#creating-owner-drawn-menu-items)
    -   [<span data-ttu-id="2ae81-138">Establecer la marca de Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="2ae81-138">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
    -   [<span data-ttu-id="2ae81-139">Menús dibujados por el propietario y el mensaje de MEASUREITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-139">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="2ae81-140">Menús dibujados por el propietario y el mensaje de la DRAWITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-140">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="2ae81-141">Menús dibujados por el propietario y el mensaje de MENUCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-141">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
    -   [<span data-ttu-id="2ae81-142">Establecer fuentes para Menu-Item cadenas de texto</span><span class="sxs-lookup"><span data-stu-id="2ae81-142">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
    -   [<span data-ttu-id="2ae81-143">Ejemplo de elementos de menú de Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="2ae81-143">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)
-   [<span data-ttu-id="2ae81-144">Usar mapas de bits de marca de verificación personalizada</span><span class="sxs-lookup"><span data-stu-id="2ae81-144">Using Custom Check Mark Bitmaps</span></span>](#using-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="2ae81-145">Crear mapas de bits de marcas de verificación personalizadas</span><span class="sxs-lookup"><span data-stu-id="2ae81-145">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="2ae81-146">Asociar mapas de bits a un elemento de menú</span><span class="sxs-lookup"><span data-stu-id="2ae81-146">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
    -   [<span data-ttu-id="2ae81-147">Establecer el atributo de marca de verificación</span><span class="sxs-lookup"><span data-stu-id="2ae81-147">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
    -   [<span data-ttu-id="2ae81-148">Simular casillas en un menú</span><span class="sxs-lookup"><span data-stu-id="2ae81-148">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
    -   [<span data-ttu-id="2ae81-149">Ejemplo de uso de mapas de bits de marcas de verificación personalizadas</span><span class="sxs-lookup"><span data-stu-id="2ae81-149">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a><span data-ttu-id="2ae81-150">Uso de un recurso de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="2ae81-150">Using a Menu-Template Resource</span></span>

<span data-ttu-id="2ae81-151">Normalmente se incluye un menú en una aplicación mediante la creación de un recurso de plantilla de menú y, a continuación, la carga del menú en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2ae81-151">You typically include a menu in an application by creating a menu-template resource and then loading the menu at run time.</span></span> <span data-ttu-id="2ae81-152">En esta sección se describe el formato de una plantilla de menú y se explica cómo cargar un recurso de plantilla de menú y usarlo en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-152">This section describes the format of a menu template, and explains how to load a menu-template resource and use it in your application.</span></span> <span data-ttu-id="2ae81-153">Para obtener información sobre cómo crear un recurso de plantilla de menú, vea la documentación que se incluye con las herramientas de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="2ae81-153">For information about creating a menu-template resource, see the documentation included with your development tools.</span></span>

-   [<span data-ttu-id="2ae81-154">Formato de Menu-Template extendido</span><span class="sxs-lookup"><span data-stu-id="2ae81-154">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
-   [<span data-ttu-id="2ae81-155">Formato de Menu-Template anterior</span><span class="sxs-lookup"><span data-stu-id="2ae81-155">Old Menu-Template Format</span></span>](#old-menu-template-format)
-   [<span data-ttu-id="2ae81-156">Cargar un recurso de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="2ae81-156">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
-   [<span data-ttu-id="2ae81-157">Crear un menú de clase</span><span class="sxs-lookup"><span data-stu-id="2ae81-157">Creating a Class Menu</span></span>](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a><span data-ttu-id="2ae81-158">Formato de Menu-Template extendido</span><span class="sxs-lookup"><span data-stu-id="2ae81-158">Extended Menu-Template Format</span></span>

<span data-ttu-id="2ae81-159">El formato de plantilla de menú extendido admite funcionalidad de menú adicional.</span><span class="sxs-lookup"><span data-stu-id="2ae81-159">The extended menu-template format supports additional menu functionality.</span></span> <span data-ttu-id="2ae81-160">Al igual que los recursos de plantilla de menú estándar, los recursos de plantilla de menú extendido tienen el tipo de recurso de **\_ menú RT** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-160">Like standard menu-template resources, extended menu-template resources have the **RT\_MENU** resource type.</span></span> <span data-ttu-id="2ae81-161">El sistema distingue los dos formatos de recursos por el número de versión, que es el primer miembro del encabezado de recurso.</span><span class="sxs-lookup"><span data-stu-id="2ae81-161">The system distinguishes the two resource formats by the version number, which is the first member of the resource header.</span></span>

<span data-ttu-id="2ae81-162">Una plantilla de menú extendida está formada por una estructura de [**\_ \_ encabezado de plantilla de MENUEX**](menuex-template-header.md) , seguida de una o más estructuras de definición de elementos de [**\_ \_ elemento de plantilla MENUEX**](menuex-template-item.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-162">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one more [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) item definition structures.</span></span>

### <a name="old-menu-template-format"></a><span data-ttu-id="2ae81-163">Formato de Menu-Template anterior</span><span class="sxs-lookup"><span data-stu-id="2ae81-163">Old Menu-Template Format</span></span>

<span data-ttu-id="2ae81-164">Una plantilla de menú antigua (Microsoft Windows NT 3,51 y versiones anteriores) define un menú, pero no admite la nueva funcionalidad de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-164">An old menu template (Microsoft Windows NT 3.51 and earlier) defines a menu, but does not support the new menu functionality.</span></span> <span data-ttu-id="2ae81-165">Un recurso de plantilla de menú antiguo tiene el tipo de recurso de **\_ menú RT** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-165">An old menu-template resource has the **RT\_MENU** resource type.</span></span>

<span data-ttu-id="2ae81-166">Una plantilla de menú antigua está formada por una estructura [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) seguida de una o más estructuras [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-166">An old menu template consists of a [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) structure followed by one or more [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) structures.</span></span>

### <a name="loading-a-menu-template-resource"></a><span data-ttu-id="2ae81-167">Cargar un recurso de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="2ae81-167">Loading a Menu-Template Resource</span></span>

<span data-ttu-id="2ae81-168">Para cargar un recurso de plantilla de menú, use la función [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) , especificando un identificador para el módulo que contiene el recurso y el identificador de la plantilla de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-168">To load a menu-template resource, use the [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) function, specifying a handle to the module that contains the resource and the menu template's identifier.</span></span> <span data-ttu-id="2ae81-169">La función **LoadMenu** devuelve un identificador de menú que puede usar para asignar el menú a una ventana.</span><span class="sxs-lookup"><span data-stu-id="2ae81-169">The **LoadMenu** function returns a menu handle that you can use to assign the menu to a window.</span></span> <span data-ttu-id="2ae81-170">Esta ventana se convierte en la ventana propietaria del menú y recibe todos los mensajes generados por el menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-170">This window becomes the menu's owner window, receiving all the messages generated by the menu.</span></span>

<span data-ttu-id="2ae81-171">Para crear un menú a partir de una plantilla de menú que ya está en la memoria, use la función [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-171">To create a menu from a menu template that is already in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span> <span data-ttu-id="2ae81-172">Esto resulta útil si la aplicación genera plantillas de menú dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="2ae81-172">This is useful if your application generates menu templates dynamically.</span></span>

<span data-ttu-id="2ae81-173">Para asignar un menú a una ventana, use la función [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) o especifique el identificador del menú en el parámetro *hMenu* de la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) al crear una ventana.</span><span class="sxs-lookup"><span data-stu-id="2ae81-173">To assign a menu to a window, use the [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) function or specify the menu's handle in the *hMenu* parameter of the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function when creating a window.</span></span> <span data-ttu-id="2ae81-174">Otra forma de asignar un menú a una ventana es especificar una plantilla de menú al registrar una clase de ventana. la plantilla identifica el menú especificado como el menú clase para esa clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="2ae81-174">Another way you can assign a menu to a window is to specify a menu template when you register a window class; the template identifies the specified menu as the class menu for that window class.</span></span>

<span data-ttu-id="2ae81-175">Para que el sistema asigne automáticamente un menú específico a una ventana, especifique la plantilla del menú al registrar la clase de la ventana.</span><span class="sxs-lookup"><span data-stu-id="2ae81-175">To have the system automatically assign a specific menu to a window, specify the menu's template when you register the window's class.</span></span> <span data-ttu-id="2ae81-176">La plantilla identifica el menú especificado como el menú clase para esa clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="2ae81-176">The template identifies the specified menu as the class menu for that window class.</span></span> <span data-ttu-id="2ae81-177">A continuación, cuando se crea una ventana de la clase especificada, el sistema asigna automáticamente el menú especificado a la ventana.</span><span class="sxs-lookup"><span data-stu-id="2ae81-177">Then, when you create a window of the specified class, the system automatically assigns the specified menu to the window.</span></span>

<span data-ttu-id="2ae81-178">No se puede asignar un menú a una ventana que sea una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="2ae81-178">You cannot assign a menu to a window that is a child window.</span></span>

<span data-ttu-id="2ae81-179">Para crear un menú de clase, incluya el identificador del recurso de plantilla de menú como el miembro **lpszMenuName** de una estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) y, a continuación, pase un puntero a la estructura a la función [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-179">To create a class menu, include the identifier of the menu-template resource as the **lpszMenuName** member of a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure and then pass a pointer to the structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span>

### <a name="creating-a-class-menu"></a><span data-ttu-id="2ae81-180">Crear un menú de clase</span><span class="sxs-lookup"><span data-stu-id="2ae81-180">Creating a Class Menu</span></span>

<span data-ttu-id="2ae81-181">En el ejemplo siguiente se muestra cómo crear un menú de clase para una aplicación, crear una ventana que use el menú clase y comandos de menú procesar en el procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="2ae81-181">The following example shows how to create a class menu for an application, create a window that uses the class menu, and process menu commands in the window procedure.</span></span>

<span data-ttu-id="2ae81-182">A continuación se encuentra la parte pertinente del archivo de encabezado de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="2ae81-182">Following is the relevant portion of the application's header file:</span></span>


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



<span data-ttu-id="2ae81-183">A continuación se muestran las partes relevantes de la propia aplicación:</span><span class="sxs-lookup"><span data-stu-id="2ae81-183">Following are the relevant portions of the application itself:</span></span>


```
HINSTANCE hinst; 
 
int APIENTRY WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg = { };  // message 
    WNDCLASS wc;    // windowclass data 
    HWND hwnd;      // handle to the main window 
 
    // Create the window class for the main window. Specify 
    // the identifier of the menu-template resource as the 
    // lpszMenuName member of the WNDCLASS structure to create 
    // the class menu. 
 
    wc.style = 0; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  MAKEINTRESOURCE(IDM_MYMENURESOURCE); 
    wc.lpszClassName = "MainWClass"; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    hinst = hinstance; 
 
    // Create the main window. Set the hmenu parameter to NULL so 
    // that the system uses the class menu for the window. 
 
    hwnd = CreateWindow("MainWClass", "Sample Application", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, hinstance, 
        NULL); 
 
    if (hwnd == NULL) 
        return FALSE; 
 
    // Make the window visible and send a WM_PAINT message to the 
    // window procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
 
    // Start the main message loop. 
 
    while (GetMessage(&msg, NULL, 0, 0)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(hPrevInstance); 
} 
 
 
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    switch (uMsg) 
    { 
        // Process other window messages. 
 
        case WM_COMMAND: 
 
            // Test for the identifier of a command item. 
 
            switch(LOWORD(wParam)) 
            { 
                case IDM_FI_OPEN: 
                    DoFileOpen();   // application-defined 
                    break; 
 
                case IDM_FI_CLOSE: 
                    DoFileClose();  // application-defined 
                    break; 
                // Process other menu commands. 
 
                default: 
                    break; 
 
            } 
            return 0; 
 
        // Process other window messages. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="creating-a-shortcut-menu"></a><span data-ttu-id="2ae81-184">Crear un menú contextual</span><span class="sxs-lookup"><span data-stu-id="2ae81-184">Creating a Shortcut Menu</span></span>

<span data-ttu-id="2ae81-185">Para usar un menú contextual en una aplicación, pase su identificador a la función [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-185">To use a shortcut menu in an application, pass its handle to the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="2ae81-186">Una aplicación normalmente llama a **TrackPopupMenuEx** en un procedimiento de ventana en respuesta a un mensaje generado por el usuario, como [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) o [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown).</span><span class="sxs-lookup"><span data-stu-id="2ae81-186">An application typically calls **TrackPopupMenuEx** in a window procedure in response to a user-generated message, such as [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown).</span></span>

<span data-ttu-id="2ae81-187">Además del controlador de menú emergente, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) requiere que se especifique un identificador para la ventana propietaria, la posición del menú contextual (en coordenadas de pantalla) y el botón del mouse que el usuario puede usar para elegir un elemento.</span><span class="sxs-lookup"><span data-stu-id="2ae81-187">In addition to the pop-up menu handle, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) requires that you specify a handle to the owner window, the position of the shortcut menu (in screen coordinates), and the mouse button that the user can use to choose an item.</span></span>

<span data-ttu-id="2ae81-188">Todavía se admite la función [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) anterior, pero las nuevas aplicaciones deben usar la función [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-188">The older [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function is still supported, but new applications should use the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="2ae81-189">La función **TrackPopupMenuEx** requiere los mismos parámetros que **TrackPopupMenu**, pero también permite especificar una parte de la pantalla que el menú no debe ocultar.</span><span class="sxs-lookup"><span data-stu-id="2ae81-189">The **TrackPopupMenuEx** function requires the same parameters as **TrackPopupMenu**, but also lets you specify a portion of the screen that the menu should not obscure.</span></span> <span data-ttu-id="2ae81-190">Una aplicación normalmente llama a estas funciones en un procedimiento de ventana al procesar el mensaje de [**\_ CONTEXTMENU de WM**](wm-contextmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-190">An application typically calls these functions in a window procedure when processing the [**WM\_CONTEXTMENU**](wm-contextmenu.md) message.</span></span>

<span data-ttu-id="2ae81-191">Puede especificar la posición de un menú contextual proporcionando coordenadas x e y junto con la marca **\_ CENTERALIGN** de TPM, **\_ LEFTALIGN TPM** o **\_ RIGHTALIGN** de TPM.</span><span class="sxs-lookup"><span data-stu-id="2ae81-191">You can specify the position of a shortcut menu by providing x- and y-coordinates along with the **TPM\_CENTERALIGN**, **TPM\_LEFTALIGN**, or **TPM\_RIGHTALIGN** flag.</span></span> <span data-ttu-id="2ae81-192">La marca especifica la posición del menú contextual con respecto a las coordenadas x e y.</span><span class="sxs-lookup"><span data-stu-id="2ae81-192">The flag specifies the position of the shortcut menu relative to the x- and y-coordinates.</span></span>

<span data-ttu-id="2ae81-193">Debe permitir que el usuario elija un elemento en un menú contextual con el mismo botón del mouse que se usa para mostrar el menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-193">You should permit the user to choose an item from a shortcut menu by using the same mouse button used to display the menu.</span></span> <span data-ttu-id="2ae81-194">Para ello, especifique la marca **\_ LEFTBUTTON** o **TPM \_ RIGHTBUTTON** para indicar qué botón del mouse puede usar el usuario para elegir un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-194">To do this, specify either **TPM\_LEFTBUTTON** or **TPM\_RIGHTBUTTON** flag to indicate which mouse button the user can use to choose a menu item.</span></span>

-   [<span data-ttu-id="2ae81-195">Procesamiento del mensaje de CONTEXTMENU de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-195">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
-   [<span data-ttu-id="2ae81-196">Crear un menú contextual Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="2ae81-196">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
-   [<span data-ttu-id="2ae81-197">Mostrar un menú contextual</span><span class="sxs-lookup"><span data-stu-id="2ae81-197">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a><span data-ttu-id="2ae81-198">Procesamiento del mensaje de CONTEXTMENU de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-198">Processing the WM\_CONTEXTMENU Message</span></span>

<span data-ttu-id="2ae81-199">El mensaje de [**\_ CONTEXTMENU de WM**](wm-contextmenu.md) se genera cuando el procedimiento de ventana de la aplicación pasa el mensaje de [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) o [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-199">The [**WM\_CONTEXTMENU**](wm-contextmenu.md) message is generated when an application's window procedure passes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="2ae81-200">La aplicación puede procesar este mensaje para mostrar un menú contextual apropiado para una parte específica de su pantalla.</span><span class="sxs-lookup"><span data-stu-id="2ae81-200">The application can process this message to display a shortcut menu appropriate to a specific portion of its screen.</span></span> <span data-ttu-id="2ae81-201">Si la aplicación no muestra un menú contextual, debe pasar el mensaje a **DefWindowProc** para el control predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2ae81-201">If the application does not display a shortcut menu, it should pass the message to **DefWindowProc** for default handling.</span></span>

<span data-ttu-id="2ae81-202">A continuación se muestra un ejemplo del procesamiento de mensajes de [**\_ CONTEXTMENU de WM**](wm-contextmenu.md) tal y como podría aparecer en el procedimiento de ventana de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-202">Following is an example of [**WM\_CONTEXTMENU**](wm-contextmenu.md) message processing as it might appear in an application's window procedure.</span></span> <span data-ttu-id="2ae81-203">Las palabras de orden inferior y de orden superior del parámetro *lParam* especifican las coordenadas de pantalla del mouse cuando se suelta el botón secundario del mouse (tenga en cuenta que estas coordenadas pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="2ae81-203">The low-order and high-order words of the *lParam* parameter specify the screen coordinates of the mouse when the right mouse button is released (note that these coordinates can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="2ae81-204">La función **OnContextMenu** definida por la aplicación devuelve **true** si muestra un menú contextual, o bien **false** si no lo hace.</span><span class="sxs-lookup"><span data-stu-id="2ae81-204">The application-defined **OnContextMenu** function returns **TRUE** if it displays a context menu, or **FALSE** if it does not.</span></span>


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



<span data-ttu-id="2ae81-205">La siguiente función OnContextMenu definida por la aplicación muestra un menú contextual si la posición del mouse especificado está dentro del área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="2ae81-205">The following application-defined OnContextMenu function displays a shortcut menu if the specified mouse position is within the window's client area.</span></span> <span data-ttu-id="2ae81-206">Una función más sofisticada podría mostrar uno de varios menús diferentes, en función de la parte del área de cliente que se especifique.</span><span class="sxs-lookup"><span data-stu-id="2ae81-206">A more sophisticated function might display one of several different menus, depending on which portion of the client area is specified.</span></span> <span data-ttu-id="2ae81-207">Para mostrar realmente el menú contextual, en este ejemplo se llama a una función definida por la aplicación denominada DisplayContextMenu.</span><span class="sxs-lookup"><span data-stu-id="2ae81-207">To actually display the shortcut menu, this example calls an application-defined function called DisplayContextMenu.</span></span> <span data-ttu-id="2ae81-208">Para obtener una descripción de esta función, vea [Mostrar un menú contextual](#displaying-a-shortcut-menu).</span><span class="sxs-lookup"><span data-stu-id="2ae81-208">For a description of this function, see [Displaying a Shortcut Menu](#displaying-a-shortcut-menu).</span></span>


```
BOOL WINAPI OnContextMenu(HWND hwnd, int x, int y) 
{ 
    RECT rc;                    // client area of window 
    POINT pt = { x, y };        // location of mouse click 
 
    // Get the bounding rectangle of the client area. 
 
    GetClientRect(hwnd, &rc); 
 
    // Convert the mouse position to client coordinates. 
 
    ScreenToClient(hwnd, &pt); 
 
    // If the position is in the client area, display a  
    // shortcut menu. 
 
    if (PtInRect(&rc, pt)) 
    { 
        ClientToScreen(hwnd, &pt); 
        DisplayContextMenu(hwnd, pt); 
        return TRUE; 
    } 
 
    // Return FALSE if no menu is displayed. 
 
    return FALSE; 
} 
```



### <a name="creating-a-shortcut-font-attributes-menu"></a><span data-ttu-id="2ae81-209">Crear un menú contextual Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="2ae81-209">Creating a Shortcut Font-Attributes Menu</span></span>

<span data-ttu-id="2ae81-210">El ejemplo de esta sección contiene partes de código de una aplicación que crea y muestra un menú contextual que permite al usuario establecer fuentes y atributos de fuente.</span><span class="sxs-lookup"><span data-stu-id="2ae81-210">The example in this section contains portions of code from an application that creates and displays a shortcut menu that enables the user to set fonts and font attributes.</span></span> <span data-ttu-id="2ae81-211">La aplicación muestra el menú en el área cliente de la ventana principal cada vez que el usuario hace clic en el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="2ae81-211">The application displays the menu in the client area of its main window whenever the user clicks the left mouse button.</span></span>

<span data-ttu-id="2ae81-212">Esta es la plantilla de menú del menú contextual que se proporciona en el archivo de definición de recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-212">Here is the menu template for the shortcut menu that is provided in the application's resource-definition file.</span></span>


```
PopupMenu MENU 
BEGIN 
  POPUP "Dummy Popup" 
    BEGIN 
      POPUP "Fonts" 
        BEGIN 
          MENUITEM "Courier",     IDM_FONT_COURIER 
          MENUITEM "Times Roman", IDM_FONT_TMSRMN 
          MENUITEM "Swiss",       IDM_FONT_SWISS 
          MENUITEM "Helvetica",   IDM_FONT_HELV 
          MENUITEM "Old English", IDM_FONT_OLDENG 
        END 
      POPUP "Sizes" 
        BEGIN 
          MENUITEM "7",  IDM_SIZE_7 
          MENUITEM "8",  IDM_SIZE_8 
          MENUITEM "9",  IDM_SIZE_9 
          MENUITEM "10", IDM_SIZE_10 
          MENUITEM "11", IDM_SIZE_11 
          MENUITEM "12", IDM_SIZE_12 
          MENUITEM "14", IDM_SIZE_14 
        END 
      POPUP "Styles" 
        BEGIN 
          MENUITEM "Bold",        IDM_STYLE_BOLD 
          MENUITEM "Italic",      IDM_STYLE_ITALIC 
          MENUITEM "Strike Out",  IDM_STYLE_SO 
          MENUITEM "Superscript", IDM_STYLE_SUPER 
          MENUITEM "Subscript",   IDM_STYLE_SUB 
        END 
    END 
 
END 
```



<span data-ttu-id="2ae81-213">En el ejemplo siguiente se proporciona el procedimiento de ventana y las funciones auxiliares que se usan para crear y mostrar el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="2ae81-213">The following example gives the window procedure and supporting functions used to create and display the shortcut menu.</span></span>


```
LRESULT APIENTRY MenuWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rc;    // client area             
    POINT pt;   // location of mouse click  
 
    switch (uMsg) 
    { 
        case WM_LBUTTONDOWN: 
 
            // Get the bounding rectangle of the client area. 
 
            GetClientRect(hwnd, (LPRECT) &rc); 
 
            // Get the client coordinates for the mouse click.  
 
            pt.x = GET_X_LPARAM(lParam); 
            pt.y = GET_Y_LPARAM(lParam); 
 
            // If the mouse click took place inside the client 
            // area, execute the application-defined function 
            // that displays the shortcut menu. 
 
            if (PtInRect((LPRECT) &rc, pt)) 
                HandlePopupMenu(hwnd, pt); 
            break; 
        // Process other window messages.  
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
 
VOID APIENTRY HandlePopupMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // menu template          
    HMENU hmenuTrackPopup;  // shortcut menu   
 
    //  Load the menu template containing the shortcut menu from the 
    //  application's resources. 
 
    hmenu = LoadMenu(hinst, "PopupMenu"); 
    if (hmenu == NULL) 
        return; 
 
    // Get the first shortcut menu in the menu template. This is the 
    // menu that TrackPopupMenu displays. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // TrackPopup uses screen coordinates, so convert the 
    // coordinates of the mouse click to screen coordinates. 
 
    ClientToScreen(hwnd, (LPPOINT) &pt); 
 
    // Draw and track the shortcut menu.  
 
    TrackPopupMenu(hmenuTrackPopup, TPM_LEFTALIGN | TPM_LEFTBUTTON, 
        pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



### <a name="displaying-a-shortcut-menu"></a><span data-ttu-id="2ae81-214">Mostrar un menú contextual</span><span class="sxs-lookup"><span data-stu-id="2ae81-214">Displaying a Shortcut Menu</span></span>

<span data-ttu-id="2ae81-215">La función que se muestra en el ejemplo siguiente muestra un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="2ae81-215">The function shown in the following example displays a shortcut menu.</span></span>

<span data-ttu-id="2ae81-216">La aplicación incluye un recurso de menú identificado por la cadena "ShortcutExample".</span><span class="sxs-lookup"><span data-stu-id="2ae81-216">The application includes a menu resource identified by the string "ShortcutExample."</span></span> <span data-ttu-id="2ae81-217">La barra de menús contiene simplemente un nombre de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-217">The menu bar simply contains a menu name.</span></span> <span data-ttu-id="2ae81-218">La aplicación utiliza la función [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) para mostrar el menú asociado a este elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-218">The application uses the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function to display the menu associated with this menu item.</span></span> <span data-ttu-id="2ae81-219">(La barra de menús no se muestra porque **TrackPopupMenu** requiere un identificador para un menú, un submenú o un menú contextual).</span><span class="sxs-lookup"><span data-stu-id="2ae81-219">(The menu bar itself is not displayed because **TrackPopupMenu** requires a handle to a menu, submenu, or shortcut menu.)</span></span>


```
VOID APIENTRY DisplayContextMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // top-level menu 
    HMENU hmenuTrackPopup;  // shortcut menu 
 
    // Load the menu resource. 
 
    if ((hmenu = LoadMenu(hinst, "ShortcutExample")) == NULL) 
        return; 
 
    // TrackPopupMenu cannot display the menu bar so get 
    // a handle to the first shortcut menu. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // Display the shortcut menu. Track the right mouse 
    // button. 
 
    TrackPopupMenu(hmenuTrackPopup, 
            TPM_LEFTALIGN | TPM_RIGHTBUTTON, 
            pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



## <a name="using-menu-item-bitmaps"></a><span data-ttu-id="2ae81-220">Usar mapas de bits de Menu-Item</span><span class="sxs-lookup"><span data-stu-id="2ae81-220">Using Menu-Item Bitmaps</span></span>

<span data-ttu-id="2ae81-221">El sistema puede usar un mapa de bits en lugar de una cadena de texto para mostrar un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-221">The system can use a bitmap instead of a text string to display a menu item.</span></span> <span data-ttu-id="2ae81-222">Para usar un mapa de bits, debe establecer la marca de **\_ mapa de bits Miim** para el elemento de menú y especificar un identificador para el mapa de bits que el sistema debe mostrar para el elemento de menú en el miembro **HbmpItem** de la estructura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-222">To use a bitmap, you must set the **MIIM\_BITMAP** flag for the menu item and specify a handle to the bitmap that the system should display for the menu item in the **hbmpItem** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="2ae81-223">En esta sección se describe cómo usar mapas de bits para los elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-223">This section describes how to use bitmaps for menu items.</span></span>

-   [<span data-ttu-id="2ae81-224">Establecer la marca de tipo de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="2ae81-224">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
-   [<span data-ttu-id="2ae81-225">Crear el mapa de bits</span><span class="sxs-lookup"><span data-stu-id="2ae81-225">Creating the Bitmap</span></span>](#creating-the-bitmap)
-   [<span data-ttu-id="2ae81-226">Agregar líneas y gráficos a un menú</span><span class="sxs-lookup"><span data-stu-id="2ae81-226">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
-   [<span data-ttu-id="2ae81-227">Ejemplo de mapas de bits de Menu-Item</span><span class="sxs-lookup"><span data-stu-id="2ae81-227">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a><span data-ttu-id="2ae81-228">Establecer la marca de tipo de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="2ae81-228">Setting the Bitmap Type Flag</span></span>

<span data-ttu-id="2ae81-229">La marca de mapa de bits **Miim \_** o **MF \_** indica al sistema que use un mapa de bits en lugar de una cadena de texto para mostrar un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-229">The **MIIM\_BITMAP** or **MF\_BITMAP** flag tells the system to use a bitmap rather than a text string to display a menu item.</span></span> <span data-ttu-id="2ae81-230">La marca de mapa de **\_ bits** **Miim \_** o MF de un elemento de menú debe establecerse en tiempo de ejecución; no se puede establecer en el archivo de definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ae81-230">A menu item's **MIIM\_BITMAP** or **MF\_BITMAP** flag must be set at run time; you cannot set it in the resource-definition file.</span></span>

<span data-ttu-id="2ae81-231">En el caso de las aplicaciones nuevas, puede usar la función [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) o [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) para establecer la marca de tipo de **mapa de \_ bits Miim** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-231">For new applications, you can use the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) or [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) function to set the **MIIM\_BITMAP** type flag.</span></span> <span data-ttu-id="2ae81-232">Para cambiar un elemento de menú de un elemento de texto a un elemento de mapa de bits, use **SetMenuItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="2ae81-232">To change a menu item from a text item to a bitmap item, use **SetMenuItemInfo**.</span></span> <span data-ttu-id="2ae81-233">Para agregar un nuevo elemento de mapa de bits a un menú, utilice la función **InsertMenuItem** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-233">To add a new bitmap item to a menu, use the **InsertMenuItem** function.</span></span>

<span data-ttu-id="2ae81-234">Las aplicaciones escritas para versiones anteriores del sistema pueden seguir usando las funciones [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) para establecer la marca de **mapa de \_ bits MF** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-234">Applications written for earlier versions of the system can continue to use the [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to set the **MF\_BITMAP** flag.</span></span> <span data-ttu-id="2ae81-235">Para cambiar un elemento de menú de un elemento de cadena de texto a un elemento de mapa de bits, use **ModifyMenu**.</span><span class="sxs-lookup"><span data-stu-id="2ae81-235">To change a menu item from a text string item to a bitmap item, use **ModifyMenu**.</span></span> <span data-ttu-id="2ae81-236">Para agregar un nuevo elemento de mapa de bits a un menú, use la marca de **\_ mapa de bits MF** con la función **InsertMenu** o **AppendMenu** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-236">To add a new bitmap item to a menu, use the **MF\_BITMAP** flag with the **InsertMenu** or **AppendMenu** function.</span></span>

### <a name="creating-the-bitmap"></a><span data-ttu-id="2ae81-237">Crear el mapa de bits</span><span class="sxs-lookup"><span data-stu-id="2ae81-237">Creating the Bitmap</span></span>

<span data-ttu-id="2ae81-238">Al establecer el **\_ mapa** de bits Miim o el indicador de tipo de **\_ mapa de bits MF** para un elemento de menú, también debe especificar un identificador para el mapa de bits que el sistema debe mostrar para el elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-238">When you set the **MIIM\_BITMAP** or **MF\_BITMAP** type flag for a menu item, you must also specify a handle to the bitmap that the system should display for the menu item.</span></span> <span data-ttu-id="2ae81-239">Puede proporcionar el mapa de bits como un recurso de mapa de bits o crear el mapa de bits en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2ae81-239">You can provide the bitmap as a bitmap resource or create the bitmap at run time.</span></span> <span data-ttu-id="2ae81-240">Si usa un recurso de mapa de bits, puede utilizar la función [**loadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) para cargar el mapa de bits y obtener su identificador.</span><span class="sxs-lookup"><span data-stu-id="2ae81-240">If you use a bitmap resource, you can use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap and obtain its handle.</span></span>

<span data-ttu-id="2ae81-241">Para crear el mapa de bits en tiempo de ejecución, utilice las funciones de Windows Interfaz de dispositivo gráfico (GDI).</span><span class="sxs-lookup"><span data-stu-id="2ae81-241">To create the bitmap at run time, use Windows Graphics Device Interface (GDI) functions.</span></span> <span data-ttu-id="2ae81-242">GDI proporciona varias maneras de crear un mapa de bits en tiempo de ejecución, pero los desarrolladores normalmente usan el método siguiente:</span><span class="sxs-lookup"><span data-stu-id="2ae81-242">GDI provides several ways to create a bitmap at run time, but developers typically use the following method:</span></span>

1.  <span data-ttu-id="2ae81-243">Use la función [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) para crear un contexto de dispositivo compatible con el contexto de dispositivo que usa la ventana principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-243">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the device context used by the application's main window.</span></span>
2.  <span data-ttu-id="2ae81-244">Use la función [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) para crear un mapa de bits compatible con la ventana principal de la aplicación o use la función [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) para crear un mapa de bits monocromo.</span><span class="sxs-lookup"><span data-stu-id="2ae81-244">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window or use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>
3.  <span data-ttu-id="2ae81-245">Use la función [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para seleccionar el mapa de bits en el contexto de dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="2ae81-245">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="2ae81-246">Use funciones de dibujo de GDI, como [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) y [**lineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), para dibujar una imagen en el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="2ae81-246">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap.</span></span>

<span data-ttu-id="2ae81-247">Para obtener más información, vea [mapas de bits](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="2ae81-247">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="adding-lines-and-graphs-to-a-menu"></a><span data-ttu-id="2ae81-248">Agregar líneas y gráficos a un menú</span><span class="sxs-lookup"><span data-stu-id="2ae81-248">Adding Lines and Graphs to a Menu</span></span>

<span data-ttu-id="2ae81-249">En el ejemplo de código siguiente se muestra cómo crear un menú que contiene los mapas de bits del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-249">The following code sample shows how to create a menu that contains menu-item bitmaps.</span></span> <span data-ttu-id="2ae81-250">Crea dos menús.</span><span class="sxs-lookup"><span data-stu-id="2ae81-250">It creates two menus.</span></span> <span data-ttu-id="2ae81-251">El primero es un menú gráfico que contiene tres mapas de bits de elementos de menú: un gráfico circular, un gráfico de líneas y un gráfico de barras.</span><span class="sxs-lookup"><span data-stu-id="2ae81-251">The first is a Chart menu that contains three menu-item bitmaps: a pie chart, a line chart, and a bar chart.</span></span> <span data-ttu-id="2ae81-252">En el ejemplo se muestra cómo cargar estos mapas de bits desde el archivo de recursos de la aplicación y, a continuación, usar las funciones [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) y [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) para crear los elementos de menú y menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-252">The example demonstrates how to load these bitmaps from the application's resource file, and then use the [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) and [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to create the menu and menu items.</span></span>

<span data-ttu-id="2ae81-253">El segundo menú es un menú líneas.</span><span class="sxs-lookup"><span data-stu-id="2ae81-253">The second menu is a Lines menu.</span></span> <span data-ttu-id="2ae81-254">Contiene mapas de bits que muestran los estilos de línea proporcionados por el lápiz predefinido en el sistema.</span><span class="sxs-lookup"><span data-stu-id="2ae81-254">It contains bitmaps showing the line styles provided by the predefined pen in the system.</span></span> <span data-ttu-id="2ae81-255">Los mapas de bits de estilo de línea se crean en tiempo de ejecución mediante las funciones GDI.</span><span class="sxs-lookup"><span data-stu-id="2ae81-255">The line-style bitmaps are created at run time by using GDI functions.</span></span>

<span data-ttu-id="2ae81-256">Estas son las definiciones de los recursos de mapa de bits en el archivo de definición de recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-256">Here are the definitions of the bitmap resources in the application's resource-definition file.</span></span>


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



<span data-ttu-id="2ae81-257">Estas son las partes relevantes del archivo de encabezado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-257">Here are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_SOLID       PS_SOLID 
#define IDM_DASH        PS_DASH 
#define IDM_DASHDOT     PS_DASHDOT 
#define IDM_DASHDOTDOT  PS_DASHDOTDOT 
 
#define IDM_PIE  1 
#define IDM_LINE 2 
#define IDM_BAR  3 
 
// Line-type flags  
 
#define SOLID       0 
#define DOT         1 
#define DASH        2 
#define DASHDOT     3 
#define DASHDOTDOT  4 
 
// Count of pens  
 
#define CPENS 5 
 
// Chart-type flags  
 
#define PIE  1 
#define LINE 2 
#define BAR  3 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
VOID MakeChartMenu(HWND); 
VOID MakeLineMenu(HWND, HPEN, HBITMAP); 
```



<span data-ttu-id="2ae81-258">En el ejemplo siguiente se muestra cómo se crean los menús y los mapas de bits de elementos de menú en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-258">The following example shows how menus and menu-item bitmaps are created in an application.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HPEN hpen[CPENS]; 
    static HBITMAP hbmp[CPENS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create the Chart and Line menus.  
 
            MakeChartMenu(hwnd); 
            MakeLineMenu(hwnd, hpen, hbmp); 
            return 0; 
 
        // Process other window messages. 
 
        case WM_DESTROY: 
 
            for (i = 0; i < CPENS; i++) 
            { 
                DeleteObject(hbmp[i]); 
                DeleteObject(hpen[i]); 
            } 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
VOID MakeChartMenu(HWND hwnd) 
{ 
    HBITMAP hbmpPie;    // handle to pie chart bitmap   
    HBITMAP hbmpLine;   // handle to line chart bitmap  
    HBITMAP hbmpBar;    // handle to bar chart bitmap   
    HMENU hmenuMain;    // handle to main menu          
    HMENU hmenuChart;   // handle to Chart menu  
 
    // Load the pie, line, and bar chart bitmaps from the 
    // resource-definition file. 
 
    hbmpPie = LoadBitmap(hinst, MAKEINTRESOURCE(PIE)); 
    hbmpLine = LoadBitmap(hinst, MAKEINTRESOURCE(LINE)); 
    hbmpBar = LoadBitmap(hinst, MAKEINTRESOURCE(BAR)); 
 
    // Create the Chart menu and add it to the menu bar. 
    // Append the Pie, Line, and Bar menu items to the Chart 
    // menu. 
 
    hmenuMain = GetMenu(hwnd); 
    hmenuChart = CreatePopupMenu(); 
    AppendMenu(hmenuMain, MF_STRING | MF_POPUP, (UINT) hmenuChart, 
        "Chart"); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_PIE, (LPCTSTR) hbmpPie); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_LINE, 
        (LPCTSTR) hbmpLine); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_BAR, (LPCTSTR) hbmpBar); 
 
    return; 
} 
 
VOID MakeLineMenu(HWND hwnd, HPEN phpen, HBITMAP phbmp) 
{ 
    HMENU hmenuLines;       // handle to Lines menu      
    HMENU hmenu;            // handle to main menu              
    COLORREF crMenuClr;     // menu-item background color       
    HBRUSH hbrBackground;   // handle to background brush       
    HBRUSH hbrOld;          // handle to previous brush         
    WORD wLineX;            // width of line bitmaps            
    WORD wLineY;            // height of line bitmaps           
    HDC hdcMain;            // handle to main window's DC       
    HDC hdcLines;           // handle to compatible DC          
    HBITMAP hbmpOld;        // handle to previous bitmap        
    int i;                  // loop counter                     
 
    // Create the Lines menu. Add it to the menu bar.  
 
    hmenu = GetMenu(hwnd); 
    hmenuLines = CreatePopupMenu(); 
    AppendMenu(hmenu, MF_STRING | MF_POPUP, 
        (UINT) hmenuLines, "&Lines"); 
 
    // Create a brush for the menu-item background color.  
 
    crMenuClr = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crMenuClr); 
 
    // Create a compatible device context for the line bitmaps, 
    // and then select the background brush into it. 
 
    hdcMain = GetDC(hwnd); 
    hdcLines = CreateCompatibleDC(hdcMain); 
    hbrOld = SelectObject(hdcLines, hbrBackground); 
 
    // Get the dimensions of the check-mark bitmap. The width of 
    // the line bitmaps will be five times the width of the 
    // check-mark bitmap. 
 
    wLineX = GetSystemMetrics(SM_CXMENUCHECK) * (WORD) 5; 
    wLineY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    // Create the bitmaps and select them, one at a time, into the 
    // compatible device context. Initialize each bitmap by 
    // filling it with the menu-item background color. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        phbmp[i] = CreateCompatibleBitmap(hdcMain, wLineX, wLineY); 
        if (i == 0) 
            hbmpOld = SelectObject(hdcLines, phbmp[i]); 
        else 
            SelectObject(hdcLines, phbmp[i]); 
        ExtFloodFill(hdcLines, 0, 0, crMenuClr, FLOODFILLBORDER); 
    } 
 
    // Create the pens.  
 
    phpen[0] = CreatePen(PS_SOLID, 1, RGB(0, 0, 0)); 
    phpen[1] = CreatePen(PS_DOT, 1, RGB(0, 0, 0)); 
    phpen[2] = CreatePen(PS_DASH, 1, RGB(0, 0, 0)); 
    phpen[3] = CreatePen(PS_DASHDOT, 1, RGB(0, 0, 0)); 
    phpen[4] = CreatePen(PS_DASHDOTDOT, 1, RGB(0, 0, 0)); 
 
    // Select a pen and a bitmap into the compatible device 
    // context, draw a line into the bitmap, and then append 
    // the bitmap as an item in the Lines menu. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        SelectObject(hdcLines, phbmp[i]); 
        SelectObject(hdcLines, phpen[i]); 
        MoveToEx(hdcLines, 0, wLineY / 2, NULL); 
        LineTo(hdcLines, wLineX, wLineY / 2); 
        AppendMenu(hmenuLines, MF_BITMAP, i + 1, 
            (LPCTSTR) phbmp[i]); 
    } 
 
    // Release the main window's device context and destroy the 
    // compatible device context. Also, destroy the background 
    // brush. 
 
    ReleaseDC(hwnd, hdcMain); 
    SelectObject(hdcLines, hbrOld); 
    DeleteObject(hbrBackground); 
    SelectObject(hdcLines, hbmpOld); 
    DeleteDC(hdcLines); 
 
    return; 
} 
```



### <a name="example-of-menu-item-bitmaps"></a><span data-ttu-id="2ae81-259">Ejemplo de mapas de bits de Menu-Item</span><span class="sxs-lookup"><span data-stu-id="2ae81-259">Example of Menu-Item Bitmaps</span></span>

<span data-ttu-id="2ae81-260">En el ejemplo de este tema se crean dos menús, cada uno con varios elementos de menú de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="2ae81-260">The example in this topic creates two menus, each containing several bitmap menu items.</span></span> <span data-ttu-id="2ae81-261">Para cada menú, la aplicación agrega un nombre de menú correspondiente a la barra de menús de la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="2ae81-261">For each menu, the application adds a corresponding menu name to the main window's menu bar.</span></span>

<span data-ttu-id="2ae81-262">El primer menú contiene elementos de menú que muestran cada uno de los tres tipos de gráficos: circular, línea y barra.</span><span class="sxs-lookup"><span data-stu-id="2ae81-262">The first menu contains menu items showing each of three chart types: pie, line, and bar.</span></span> <span data-ttu-id="2ae81-263">Los mapas de bits de estos elementos de menú se definen como recursos y se cargan mediante la función [**loadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-263">The bitmaps for these menu items are defined as resources and are loaded by using the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function.</span></span> <span data-ttu-id="2ae81-264">Asociado con este menú es un nombre de menú de "gráfico" en la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="2ae81-264">Associated with this menu is a "Chart" menu name on the menu bar.</span></span>

<span data-ttu-id="2ae81-265">El segundo menú contiene elementos de menú que muestran cada uno de los cinco estilos de línea que se usan con la función [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) : **PS \_ Solid**, **PS \_ Dash**, **PS \_ DOT**, **PS \_ DASHDOT** y **PS \_ DASHDOTDOT**.</span><span class="sxs-lookup"><span data-stu-id="2ae81-265">The second menu contains menu items showing each of the five line styles used with the [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) function: **PS\_SOLID**, **PS\_DASH**, **PS\_DOT**, **PS\_DASHDOT**, and **PS\_DASHDOTDOT**.</span></span> <span data-ttu-id="2ae81-266">La aplicación crea los mapas de bits para estos elementos de menú en tiempo de ejecución mediante las funciones de dibujo de GDI.</span><span class="sxs-lookup"><span data-stu-id="2ae81-266">The application creates the bitmaps for these menu items at run time using GDI drawing functions.</span></span> <span data-ttu-id="2ae81-267">Asociado a este menú es el nombre del menú **líneas** en la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="2ae81-267">Associated with this menu is a **Lines** menu name on the menu bar.</span></span>

<span data-ttu-id="2ae81-268">Definido en el procedimiento de ventana de la aplicación hay dos matrices estáticas de identificadores de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="2ae81-268">Defined in the application's window procedure are two static arrays of bitmap handles.</span></span> <span data-ttu-id="2ae81-269">Una matriz contiene los identificadores de los tres mapas de bits utilizados para el menú **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-269">One array contains the handles of the three bitmaps used for the **Chart** menu.</span></span> <span data-ttu-id="2ae81-270">La otra contiene los identificadores de los cinco mapas de bits utilizados para el menú **líneas** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-270">The other contains the handles of the five bitmaps used for the **Lines** menu.</span></span> <span data-ttu-id="2ae81-271">Al procesar el mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) , el procedimiento de ventana carga los mapas de bits del gráfico, crea los mapas de bits de línea y, a continuación, agrega los elementos de menú correspondientes.</span><span class="sxs-lookup"><span data-stu-id="2ae81-271">When processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, the window procedure loads the chart bitmaps, creates the line bitmaps, and then adds the corresponding menu items.</span></span> <span data-ttu-id="2ae81-272">Al procesar el mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) , el procedimiento de ventana elimina todos los mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="2ae81-272">When processing the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the window procedure deletes all of the bitmaps.</span></span>

<span data-ttu-id="2ae81-273">A continuación se muestran las partes relevantes del archivo de encabezado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-273">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_PIE         1 
#define IDM_LINE        2 
#define IDM_BAR         3 
 
#define IDM_SOLID       4 
#define IDM_DASH        5 
#define IDM_DASHDOT     6 
#define IDM_DASHDOTDOT  7 
 
// Number of items on the Chart and Lines menus 
 
#define C_LINES         5 
#define C_CHARTS        3 
 
// Bitmap resource identifiers 
 
#define IDB_PIE         1 
#define IDB_LINE        2 
#define IDB_BAR         3 
 
// Dimensions of the line bitmaps 
 
#define CX_LINEBMP      40 
#define CY_LINEBMP      10 
```



<span data-ttu-id="2ae81-274">A continuación se muestran las partes relevantes del procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="2ae81-274">Following are the relevant portions of the window procedure.</span></span> <span data-ttu-id="2ae81-275">El procedimiento de ventana realiza la mayor parte de su inicialización mediante una llamada a las funciones definidas por la aplicación LoadChartBitmaps, CreateLineBitmaps y AddBitmapMenu, que se describen más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="2ae81-275">The window procedure performs most of its initialization by calling the application-defined LoadChartBitmaps, CreateLineBitmaps, and AddBitmapMenu functions, described later in this topic.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    static HBITMAP aHbmLines[C_LINES]; 
    static HBITMAP aHbmChart[C_CHARTS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
             // Call application-defined functions to load the 
             // bitmaps for the Chart menu and create those for 
             // the Lines menu. 
 
            LoadChartBitmaps(aHbmChart); 
            CreateLineBitmaps(aHbmLines); 
 
             // Call an application-defined function to create 
             // menus containing the bitmap menu items. The function 
             // also adds a menu name to the window's menu bar. 
 
            AddBitmapMenu( 
                    hwnd,      // menu bar's owner window 
                    "&Chart",  // text of menu name on menu bar 
                    IDM_PIE,   // ID of first item on menu 
                    aHbmChart, // array of bitmap handles 
                    C_CHARTS   // number of items on menu 
                    ); 
            AddBitmapMenu(hwnd, "&Lines", IDM_SOLID, 
                    aHbmLines, C_LINES); 
            break; 
 
        case WM_DESTROY: 
            for (i = 0; i < C_LINES; i++) 
                DeleteObject(aHbmLines[i]); 
            for (i = 0; i < C_CHARTS; i++) 
                DeleteObject(aHbmChart[i]); 
            PostQuitMessage(0); 
            break; 
 
        // Process additional messages here. 
 
        default: 
            return (DefWindowProc(hwnd, uMsg, wParam, lParam)); 
    } 
    return 0; 
} 
```



<span data-ttu-id="2ae81-276">La función LoadChartBitmaps definida por la aplicación carga los recursos de mapa de bits para el menú gráfico mediante una llamada a la función [**loadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-276">The application-defined LoadChartBitmaps function loads the bitmap resources for the chart menu by calling the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, as follows.</span></span>


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



<span data-ttu-id="2ae81-277">La función CreateLineBitmaps definida por la aplicación crea los mapas de bits para el menú líneas mediante las funciones de dibujo de GDI.</span><span class="sxs-lookup"><span data-stu-id="2ae81-277">The application-defined CreateLineBitmaps function creates the bitmaps for the Lines menu by using GDI drawing functions.</span></span> <span data-ttu-id="2ae81-278">La función crea un contexto de dispositivo de memoria (DC) con las mismas propiedades que el controlador de dominio de la ventana de escritorio.</span><span class="sxs-lookup"><span data-stu-id="2ae81-278">The function creates a memory device context (DC) with the same properties as the desktop window's DC.</span></span> <span data-ttu-id="2ae81-279">Para cada estilo de línea, la función crea un mapa de bits, lo selecciona en el controlador de dominio de memoria y lo dibuja en él.</span><span class="sxs-lookup"><span data-stu-id="2ae81-279">For each line style, the function creates a bitmap, selects it into the memory DC, and draws in it.</span></span>


```
VOID WINAPI CreateLineBitmaps(HBITMAP *paHbm) 
{ 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
    COLORREF clrMenu = GetSysColor(COLOR_MENU); 
    HBRUSH hbrOld; 
    HPEN hpenOld; 
    HBITMAP hbmOld; 
    int fnDrawMode; 
    int i; 
 
     // Create a brush using the menu background color, 
     // and select it into the memory DC. 
 
    hbrOld = SelectObject(hdcMem, CreateSolidBrush(clrMenu)); 
 
     // Create the bitmaps. Select each one into the memory 
     // DC that was created and draw in it. 
 
    for (i = 0; i < C_LINES; i++) 
    { 
        // Create the bitmap and select it into the DC. 
 
        paHbm[i] = CreateCompatibleBitmap(hdcDesktop, 
                CX_LINEBMP, CY_LINEBMP); 
        hbmOld = SelectObject(hdcMem, paHbm[i]); 
 
        // Fill the background using the brush. 
 
        PatBlt(hdcMem, 0, 0, CX_LINEBMP, CY_LINEBMP, PATCOPY); 
 
        // Create the pen and select it into the DC. 
 
        hpenOld = SelectObject(hdcMem, 
                CreatePen(PS_SOLID + i, 1, RGB(0, 0, 0))); 
 
         // Draw the line. To preserve the background color where 
         // the pen is white, use the R2_MASKPEN drawing mode. 
 
        fnDrawMode = SetROP2(hdcMem, R2_MASKPEN); 
        MoveToEx(hdcMem, 0, CY_LINEBMP / 2, NULL); 
        LineTo(hdcMem, CX_LINEBMP, CY_LINEBMP / 2); 
        SetROP2(hdcMem, fnDrawMode); 
 
        // Delete the pen, and select the old pen and bitmap. 
 
        DeleteObject(SelectObject(hdcMem, hpenOld)); 
        SelectObject(hdcMem, hbmOld); 
    } 
 
    // Delete the brush and select the original brush. 
 
    DeleteObject(SelectObject(hdcMem, hbrOld)); 
 
    // Delete the memory DC and release the desktop DC. 
 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
} 
```



<span data-ttu-id="2ae81-280">La función AddBitmapMenu definida por la aplicación crea un menú y le agrega el número especificado de elementos de menú de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="2ae81-280">The application-defined AddBitmapMenu function creates a menu and adds the specified number of bitmap menu items to it.</span></span> <span data-ttu-id="2ae81-281">A continuación, agrega un nombre de menú correspondiente a la barra de menús de la ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="2ae81-281">Then it adds a corresponding menu name to the specified window's menu bar.</span></span>


```
VOID WINAPI AddBitmapMenu( 
        HWND hwnd,          // window that owned the menu bar 
        LPSTR lpszText,     // text of menu name on menu bar 
        UINT uID,           // ID of first bitmap menu item 
        HBITMAP *paHbm,     // bitmaps for the menu items 
        int cItems)         // number bitmap menu items 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup = CreatePopupMenu(); 
    MENUITEMINFO mii; 
    int i; 
 
    // Add the bitmap menu items to the menu. 
 
    for (i = 0; i < cItems; i++) 
    { 
        mii.fMask = MIIM_ID | MIIM_BITMAP | MIIM_DATA; 
        mii.wID = uID + i; 
        mii.hbmpItem = &paHbm[i]; 
        InsertMenuItem(hmenuPopup, i, TRUE, &mii); 
    } 
 
    // Add a menu name to the menu bar. 
 
    mii.fMask = MIIM_STRING | MIIM_DATA | MIIM_SUBMENU; 
    mii.fType = MFT_STRING; 
    mii.hSubMenu = hmenuPopup; 
    mii.dwTypeData = lpszText; 
    InsertMenuItem(hmenuBar, 
        GetMenuItemCount(hmenuBar), TRUE, &mii); 
} 
```



## <a name="creating-owner-drawn-menu-items"></a><span data-ttu-id="2ae81-282">Crear Owner-Drawn elementos de menú</span><span class="sxs-lookup"><span data-stu-id="2ae81-282">Creating Owner-Drawn Menu Items</span></span>

<span data-ttu-id="2ae81-283">Si necesita tener un control completo sobre la apariencia de un elemento de menú, puede usar un elemento de menú dibujado por el propietario en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-283">If you need complete control over the appearance of a menu item, you can use an owner-drawn menu item in your application.</span></span> <span data-ttu-id="2ae81-284">En esta sección se describen los pasos necesarios para crear y usar un elemento de menú dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="2ae81-284">This section describes the steps involved in creating and using an owner-drawn menu item.</span></span>

-   [<span data-ttu-id="2ae81-285">Establecer la marca de Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="2ae81-285">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
-   [<span data-ttu-id="2ae81-286">Menús dibujados por el propietario y el mensaje de MEASUREITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-286">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
-   [<span data-ttu-id="2ae81-287">Menús dibujados por el propietario y el mensaje de la DRAWITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-287">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
-   [<span data-ttu-id="2ae81-288">Menús dibujados por el propietario y el mensaje de MENUCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-288">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
-   [<span data-ttu-id="2ae81-289">Establecer fuentes para Menu-Item cadenas de texto</span><span class="sxs-lookup"><span data-stu-id="2ae81-289">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
-   [<span data-ttu-id="2ae81-290">Ejemplo de elementos de menú de Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="2ae81-290">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a><span data-ttu-id="2ae81-291">Establecer la marca de Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="2ae81-291">Setting the Owner-Drawn Flag</span></span>

<span data-ttu-id="2ae81-292">No se puede definir un elemento de menú dibujado por el propietario en el archivo de definición de recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-292">You cannot define an owner-drawn menu item in your application's resource-definition file.</span></span> <span data-ttu-id="2ae81-293">En su lugar, debe crear un nuevo elemento de menú o modificar uno existente mediante el uso de la marca de menú de **\_ OWNERDRAW de MFT** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-293">Instead, you must create a new menu item or modify an existing one by using the **MFT\_OWNERDRAW** menu flag.</span></span>

<span data-ttu-id="2ae81-294">Puede usar la función [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) o [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) para especificar un elemento de menú dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="2ae81-294">You can use the [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) or [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function to specify an owner-drawn menu item.</span></span> <span data-ttu-id="2ae81-295">Use **InsertMenuItem** para insertar un nuevo elemento de menú en la posición especificada de un menú o una barra de menús.</span><span class="sxs-lookup"><span data-stu-id="2ae81-295">Use **InsertMenuItem** to insert a new menu item at the specified position in a menu bar or menu.</span></span> <span data-ttu-id="2ae81-296">Use **SetMenuItemInfo** para cambiar el contenido de un menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-296">Use **SetMenuItemInfo** to change the contents of a menu.</span></span>

<span data-ttu-id="2ae81-297">Al llamar a estas dos funciones, debe especificar un puntero a una estructura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , que especifica las propiedades del nuevo elemento de menú o las propiedades que desea cambiar para un elemento de menú existente.</span><span class="sxs-lookup"><span data-stu-id="2ae81-297">When calling these two functions, you must specify a pointer to a [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, which specifies the properties of the new menu item or the properties you want to change for an existing menu item.</span></span> <span data-ttu-id="2ae81-298">Para convertir un elemento en un elemento dibujado por el propietario, especifique el valor de **Miim \_ ftype** para el miembro **fMask** y el valor de **\_ OWNERDRAW de MFT** para el miembro **ftype** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-298">To make an item an owner-drawn item, specify the **MIIM\_FTYPE** value for the **fMask** member and the **MFT\_OWNERDRAW** value for the **fType** member.</span></span>

<span data-ttu-id="2ae81-299">Al establecer los miembros adecuados de la estructura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , puede asociar un valor definido por la aplicación, que se denomina **datos del elemento**, con cada elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-299">By setting the appropriate members of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, you can associate an application-defined value, which is called **item data**, with each menu item.</span></span> <span data-ttu-id="2ae81-300">Para ello, especifique el valor **de \_ datos Miim** para el miembro **fMask** y el valor definido por la aplicación para el miembro **dwItemData** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-300">To do so, specify the **MIIM\_DATA** value for the **fMask** member and the application-defined value for the **dwItemData** member.</span></span>

<span data-ttu-id="2ae81-301">Puede usar datos de elementos con cualquier tipo de elemento de menú, pero es especialmente útil para los elementos dibujados por el propietario.</span><span class="sxs-lookup"><span data-stu-id="2ae81-301">You can use item data with any type of menu item, but it is particularly useful for owner-drawn items.</span></span> <span data-ttu-id="2ae81-302">Por ejemplo, supongamos que una estructura contiene información que se usa para dibujar un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-302">For example, suppose a structure contains information used to draw a menu item.</span></span> <span data-ttu-id="2ae81-303">Una aplicación podría usar los datos del elemento para un elemento de menú para almacenar un puntero a la estructura.</span><span class="sxs-lookup"><span data-stu-id="2ae81-303">An application might use the item data for a menu item to store a pointer to the structure.</span></span> <span data-ttu-id="2ae81-304">Los datos del elemento se envían a la ventana propietaria del menú con los mensajes [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) y [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-304">The item data is sent to the menu's owner window with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages.</span></span> <span data-ttu-id="2ae81-305">Para recuperar los datos de los elementos de un menú en cualquier momento, utilice la función [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-305">To retrieve the item data for a menu at any time, use the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function.</span></span>

<span data-ttu-id="2ae81-306">Las aplicaciones escritas para versiones anteriores del sistema pueden seguir llamando a [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) para asignar la marca de **\_ OWNERDRAW MF** a un elemento de menú dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="2ae81-306">Applications written for earlier versions of the system can continue to call [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) to assign the **MF\_OWNERDRAW** flag to an owner-drawn menu item.</span></span>

<span data-ttu-id="2ae81-307">Cuando se llama a cualquiera de estas tres funciones, se puede pasar un valor como el parámetro *lpNewItem* .</span><span class="sxs-lookup"><span data-stu-id="2ae81-307">When you call any of these three functions, you can pass a value as the *lpNewItem* parameter.</span></span> <span data-ttu-id="2ae81-308">Este valor puede representar cualquier información que sea significativa para su aplicación y que estará disponible para la aplicación cuando se muestre el elemento.</span><span class="sxs-lookup"><span data-stu-id="2ae81-308">This value can represent any information that is meaningful to your application, and that will be available to your application when the item is to be displayed.</span></span> <span data-ttu-id="2ae81-309">Por ejemplo, el valor podría contener un puntero a una estructura; la estructura, a su vez, puede contener una cadena de texto y un identificador de la fuente lógica que utilizará la aplicación para dibujar la cadena.</span><span class="sxs-lookup"><span data-stu-id="2ae81-309">For example, the value could contain a pointer to a structure; the structure, in turn, might contain a text string and a handle to the logical font your application will use to draw the string.</span></span>

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a><span data-ttu-id="2ae81-310">Menús Owner-Drawn y el mensaje de MEASUREITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-310">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>

<span data-ttu-id="2ae81-311">Antes de que el sistema muestre un elemento de menú dibujado por el propietario por primera vez, envía el mensaje de [**\_ MEASUREITEM de WM**](../controls/wm-measureitem.md) al procedimiento de ventana de la ventana que posee el menú del elemento.</span><span class="sxs-lookup"><span data-stu-id="2ae81-311">Before the system displays an owner-drawn menu item for the first time, it sends the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message to the window procedure of the window that owns the item's menu.</span></span> <span data-ttu-id="2ae81-312">Este mensaje contiene un puntero a una estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que identifica el elemento y contiene los datos de elemento que una aplicación puede haber asignado a él.</span><span class="sxs-lookup"><span data-stu-id="2ae81-312">This message contains a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the item and contains the item data that an application may have assigned to it.</span></span> <span data-ttu-id="2ae81-313">El procedimiento de ventana debe rellenar los miembros **itemWidth** y **ItemHeight** de la estructura antes de volver a procesar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="2ae81-313">The window procedure must fill the **itemWidth** and **itemHeight** members of the structure before returning from processing the message.</span></span> <span data-ttu-id="2ae81-314">El sistema utiliza la información de estos miembros al crear el rectángulo delimitador en el que una aplicación dibuja el elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-314">The system uses the information in these members when creating the bounding rectangle in which an application draws the menu item.</span></span> <span data-ttu-id="2ae81-315">También utiliza la información para detectar cuándo el usuario elige el elemento.</span><span class="sxs-lookup"><span data-stu-id="2ae81-315">It also uses the information to detect when the user chooses the item.</span></span>

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a><span data-ttu-id="2ae81-316">Menús Owner-Drawn y el mensaje de la DRAWITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-316">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>

<span data-ttu-id="2ae81-317">Siempre que se debe dibujar el elemento (por ejemplo, cuando se muestra por primera vez o cuando el usuario lo selecciona), el sistema envía el mensaje de Windows de [**WM \_**](../controls/wm-drawitem.md) al procedimiento de ventana de la ventana propietaria del menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-317">Whenever the item must be drawn (for example, when it is first displayed or when the user selects it), the system sends the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message to the window procedure of the menu's owner window.</span></span> <span data-ttu-id="2ae81-318">Este mensaje contiene un puntero a una estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , que contiene información sobre el elemento, incluidos los datos de los elementos que puede haber asignado una aplicación a él.</span><span class="sxs-lookup"><span data-stu-id="2ae81-318">This message contains a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure, which contains information about the item, including the item data that an application may have assigned to it.</span></span> <span data-ttu-id="2ae81-319">Además, **drawitemstruct (** contiene marcas que indican el estado del elemento (por ejemplo, si está atenuado o seleccionado), así como un rectángulo delimitador y un contexto de dispositivo que la aplicación utiliza para dibujar el elemento.</span><span class="sxs-lookup"><span data-stu-id="2ae81-319">In addition, **DRAWITEMSTRUCT** contains flags that indicate the state of the item (such as whether it is grayed or selected) as well as a bounding rectangle and a device context that the application uses to draw the item.</span></span>

<span data-ttu-id="2ae81-320">Una aplicación debe hacer lo siguiente mientras se procesa el mensaje de [**\_ DRAWITEM de WM**](../controls/wm-drawitem.md) :</span><span class="sxs-lookup"><span data-stu-id="2ae81-320">An application must do the following while processing the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message:</span></span>

-   <span data-ttu-id="2ae81-321">Determine el tipo de dibujo necesario.</span><span class="sxs-lookup"><span data-stu-id="2ae81-321">Determine the type of drawing that is necessary.</span></span> <span data-ttu-id="2ae81-322">Para ello, compruebe el miembro **del itemaction** de la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-322">To do so, check the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span>
-   <span data-ttu-id="2ae81-323">Dibuje el elemento de menú de manera adecuada, utilizando el rectángulo delimitador y el contexto de dispositivo obtenidos de la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-323">Draw the menu item appropriately, using the bounding rectangle and device context obtained from the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="2ae81-324">La aplicación solo debe dibujar dentro del rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="2ae81-324">The application must draw only within the bounding rectangle.</span></span> <span data-ttu-id="2ae81-325">Por motivos de rendimiento, el sistema no recorta las partes de la imagen que se dibujan fuera del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="2ae81-325">For performance reasons, the system does not clip portions of the image that are drawn outside the rectangle.</span></span>
-   <span data-ttu-id="2ae81-326">Restaure todos los objetos GDI seleccionados para el contexto de dispositivo del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-326">Restore all GDI objects selected for the menu item's device context.</span></span>

<span data-ttu-id="2ae81-327">Si el usuario selecciona el elemento de menú, el sistema establece el miembro **del itemaction** de la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) en el valor **\_ SELECT de Oda** y establece el valor **\_ seleccionado de ODS** en el miembro **ItemState** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-327">If the user selects the menu item, the system sets the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure to the **ODA\_SELECT** value and sets the **ODS\_SELECTED** value in the **itemState** member.</span></span> <span data-ttu-id="2ae81-328">Esta es la indicación de la aplicación para volver a dibujar el elemento de menú para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="2ae81-328">This is an application's cue to redraw the menu item to indicate that it is selected.</span></span>

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a><span data-ttu-id="2ae81-329">Menús Owner-Drawn y el mensaje de MENUCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ae81-329">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>

<span data-ttu-id="2ae81-330">Los menús que no sean menús dibujados por el propietario pueden especificar una tecla de menú insertando un carácter de subrayado junto a un carácter en la cadena de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-330">Menus other than owner-drawn menus can specify a menu mnemonic by inserting an underscore next to a character in the menu string.</span></span> <span data-ttu-id="2ae81-331">Esto permite al usuario seleccionar el menú presionando la tecla ALT y presionando el carácter de la tecla de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-331">This allows the user to select the menu by pressing ALT and pressing the menu mnemonic character.</span></span> <span data-ttu-id="2ae81-332">Sin embargo, en los menús dibujados por el propietario, no se puede especificar una tecla de tecla de menú de esta manera.</span><span class="sxs-lookup"><span data-stu-id="2ae81-332">In owner-drawn menus, however, you cannot specify a menu mnemonic in this manner.</span></span> <span data-ttu-id="2ae81-333">En su lugar, la aplicación debe procesar el mensaje de [**\_ MENUCHAR de WM**](wm-menuchar.md) para proporcionar menús dibujados por el propietario con teclas de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-333">Instead, your application must process the [**WM\_MENUCHAR**](wm-menuchar.md) message to provide owner-drawn menus with menu mnemonics.</span></span>

<span data-ttu-id="2ae81-334">El mensaje de [**\_ MENUCHAR de WM**](wm-menuchar.md) se envía cuando el usuario escribe una tecla de menú que no coincide con ninguno de los códigos mnemónicos predefinidos del menú actual.</span><span class="sxs-lookup"><span data-stu-id="2ae81-334">The [**WM\_MENUCHAR**](wm-menuchar.md) message is sent when the user types a menu mnemonic that does not match any of the predefined mnemonics of the current menu.</span></span> <span data-ttu-id="2ae81-335">El valor contenido en *wParam* especifica el carácter ASCII que corresponde a la tecla que el usuario presionó con la tecla Alt.</span><span class="sxs-lookup"><span data-stu-id="2ae81-335">The value contained in *wParam* specifies the ASCII character that corresponds to the key the user pressed with the ALT key.</span></span> <span data-ttu-id="2ae81-336">La palabra de orden inferior de *wParam* especifica el tipo del menú seleccionado y puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="2ae81-336">The low-order word of *wParam* specifies the type of the selected menu and can be one of the following values:</span></span>

-   <span data-ttu-id="2ae81-337">**MF \_ Elemento emergente** si el menú actual es un submenú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-337">**MF\_POPUP** if the current menu is a submenu.</span></span>
-   <span data-ttu-id="2ae81-338">**MF \_ SYSMENU** si el menú es el menú del sistema.</span><span class="sxs-lookup"><span data-stu-id="2ae81-338">**MF\_SYSMENU** if the menu is the system menu.</span></span>

<span data-ttu-id="2ae81-339">La palabra de orden superior de *wParam* contiene el identificador de menú del menú actual.</span><span class="sxs-lookup"><span data-stu-id="2ae81-339">The high-order word of *wParam* contains the menu handle to the current menu.</span></span> <span data-ttu-id="2ae81-340">La ventana con los menús dibujados por el propietario puede procesar [**WM \_ MENUCHAR**](wm-menuchar.md) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="2ae81-340">The window with the owner-drawn menus can process [**WM\_MENUCHAR**](wm-menuchar.md) as follows:</span></span>


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



<span data-ttu-id="2ae81-341">Los dos de la palabra de orden superior del valor devuelto informa al sistema de que la palabra de orden inferior del valor devuelto contiene el índice de base cero del elemento de menú que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="2ae81-341">The two in the high-order word of the return value informs the system that the low-order word of the return value contains the zero-based index of the menu item to be selected.</span></span>

<span data-ttu-id="2ae81-342">Las constantes siguientes corresponden a los posibles valores devueltos del mensaje de [**\_ MENUCHAR de WM**](wm-menuchar.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-342">The following constants correspond to the possible return values from the [**WM\_MENUCHAR**](wm-menuchar.md) message.</span></span>



| <span data-ttu-id="2ae81-343">Constante</span><span class="sxs-lookup"><span data-stu-id="2ae81-343">Constant</span></span>         | <span data-ttu-id="2ae81-344">Value</span><span class="sxs-lookup"><span data-stu-id="2ae81-344">Value</span></span> | <span data-ttu-id="2ae81-345">Significado</span><span class="sxs-lookup"><span data-stu-id="2ae81-345">Meaning</span></span>                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae81-346">**MNC \_ omitir**</span><span class="sxs-lookup"><span data-stu-id="2ae81-346">**MNC\_IGNORE**</span></span>  | <span data-ttu-id="2ae81-347">0</span><span class="sxs-lookup"><span data-stu-id="2ae81-347">0</span></span>     | <span data-ttu-id="2ae81-348">El sistema debe descartar el carácter que el usuario presionó y crear un pitido corto en el altavoz del sistema.</span><span class="sxs-lookup"><span data-stu-id="2ae81-348">The system should discard the character the user pressed and create a short beep on the system speaker.</span></span>                                                       |
| <span data-ttu-id="2ae81-349">**MNC \_ cerrar**</span><span class="sxs-lookup"><span data-stu-id="2ae81-349">**MNC\_CLOSE**</span></span>   | <span data-ttu-id="2ae81-350">1</span><span class="sxs-lookup"><span data-stu-id="2ae81-350">1</span></span>     | <span data-ttu-id="2ae81-351">El sistema debe cerrar el menú activo.</span><span class="sxs-lookup"><span data-stu-id="2ae81-351">The system should close the active menu.</span></span>                                                                                                                      |
| <span data-ttu-id="2ae81-352">**\_Ejecutar MNC**</span><span class="sxs-lookup"><span data-stu-id="2ae81-352">**MNC\_EXECUTE**</span></span> | <span data-ttu-id="2ae81-353">2</span><span class="sxs-lookup"><span data-stu-id="2ae81-353">2</span></span>     | <span data-ttu-id="2ae81-354">El sistema debe elegir el elemento especificado en la palabra de orden inferior del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="2ae81-354">The system should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="2ae81-355">La ventana propietaria recibe un mensaje de [**\_ comando de WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-355">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span> |
| <span data-ttu-id="2ae81-356">**MNC \_ seleccionar**</span><span class="sxs-lookup"><span data-stu-id="2ae81-356">**MNC\_SELECT**</span></span>  | <span data-ttu-id="2ae81-357">3</span><span class="sxs-lookup"><span data-stu-id="2ae81-357">3</span></span>     | <span data-ttu-id="2ae81-358">El sistema debe seleccionar el elemento especificado en la palabra de orden inferior del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="2ae81-358">The system should select the item specified in the low-order word of the return value.</span></span>                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a><span data-ttu-id="2ae81-359">Establecer fuentes para Menu-Item cadenas de texto</span><span class="sxs-lookup"><span data-stu-id="2ae81-359">Setting Fonts for Menu-Item Text Strings</span></span>

<span data-ttu-id="2ae81-360">Este tema contiene un ejemplo de una aplicación que usa elementos de menú dibujados por el propietario en un menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-360">This topic contains an example from an application that uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="2ae81-361">El menú contiene elementos que establecen los atributos de la fuente actual y los elementos se muestran con el atributo de fuente adecuado.</span><span class="sxs-lookup"><span data-stu-id="2ae81-361">The menu contains items that set the attributes of the current font, and the items are displayed using the appropriate font attribute.</span></span>

<span data-ttu-id="2ae81-362">Aquí se muestra cómo se define el menú en el archivo de definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ae81-362">Here is how the menu is defined in the resource-definition file.</span></span> <span data-ttu-id="2ae81-363">Tenga en cuenta que las cadenas de los elementos de menú normal, negrita, cursiva y subrayado se asignan en tiempo de ejecución, por lo que sus cadenas están vacías en el archivo de definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ae81-363">Note that the strings for the Regular, Bold, Italic, and Underline menu items are assigned at run time, so their strings are empty in the resource-definition file.</span></span>


```
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "",    IDM_REGULAR 
        MENUITEM SEPARATOR 
        MENUITEM    "",    IDM_BOLD 
        MENUITEM    "",    IDM_ITALIC 
        MENUITEM    "",    IDM_ULINE 
    END 
END 
```



<span data-ttu-id="2ae81-364">El procedimiento de ventana de la aplicación procesa los mensajes implicados en el uso de elementos de menú dibujados por el propietario.</span><span class="sxs-lookup"><span data-stu-id="2ae81-364">The application's window procedure processes the messages involved in using owner-drawn menu items.</span></span> <span data-ttu-id="2ae81-365">La aplicación utiliza el mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2ae81-365">The application uses the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to do the following:</span></span>

-   <span data-ttu-id="2ae81-366">Establezca la marca **MF \_ OWNERDRAW** para los elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-366">Set the **MF\_OWNERDRAW** flag for the menu items.</span></span>
-   <span data-ttu-id="2ae81-367">Establezca las cadenas de texto para los elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-367">Set the text strings for the menu items.</span></span>
-   <span data-ttu-id="2ae81-368">Obtiene los identificadores de las fuentes que se usan para dibujar los elementos.</span><span class="sxs-lookup"><span data-stu-id="2ae81-368">Obtain handles of the fonts used to draw the items.</span></span>
-   <span data-ttu-id="2ae81-369">Obtener los valores de color de fondo y de texto para los elementos de menú seleccionados.</span><span class="sxs-lookup"><span data-stu-id="2ae81-369">Obtain the text and background color values for selected menu items.</span></span>

<span data-ttu-id="2ae81-370">Las cadenas de texto y los identificadores de fuente se almacenan en una matriz de estructuras de elementos definidas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-370">The text strings and font handles are stored in an array of application-defined MYITEM structures.</span></span> <span data-ttu-id="2ae81-371">La función GetAFont definida por la aplicación crea una fuente que corresponde al atributo de fuente especificado y devuelve un identificador a la fuente.</span><span class="sxs-lookup"><span data-stu-id="2ae81-371">The application-defined GetAFont function creates a font that corresponds to the specified font attribute and returns a handle to the font.</span></span> <span data-ttu-id="2ae81-372">Los identificadores se destruyen durante el procesamiento del mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-372">The handles are destroyed during the processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>

<span data-ttu-id="2ae81-373">Durante el procesamiento del mensaje [**de \_ MEASUREITEM de WM**](../controls/wm-measureitem.md) , el ejemplo obtiene el ancho y el alto de una cadena de elemento de menú y copia estos valores en la estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-373">During the processing of the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message, the example gets the width and height of a menu-item string and copies these values into the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure.</span></span> <span data-ttu-id="2ae81-374">El sistema utiliza los valores de ancho y alto para calcular el tamaño del menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-374">The system uses the width and height values to calculate the size of the menu.</span></span>

<span data-ttu-id="2ae81-375">Durante el procesamiento del mensaje de la secuencia de mensajes de [**WM \_**](../controls/wm-drawitem.md) , la cadena del elemento de menú se dibuja con la habitación izquierda junto a la cadena para el mapa de bits de la marca de verificación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-375">During the processing of the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message, the menu item's string is drawn with room left next to the string for the check-mark bitmap.</span></span> <span data-ttu-id="2ae81-376">Si el usuario selecciona el elemento, el texto seleccionado y los colores de fondo se usan para dibujar el elemento.</span><span class="sxs-lookup"><span data-stu-id="2ae81-376">If the user selects the item, the selected text and background colors are used to draw the item.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    typedef struct _MYITEM 
    { 
        HFONT hfont; 
        LPSTR psz; 
    } MYITEM;             // structure for item font and string  
 
    MYITEM *pmyitem;      // pointer to item's font and string        
    static MYITEM myitem[CITEMS];   // array of MYITEMS               
    static HMENU hmenu;             // handle to main menu            
    static COLORREF crSelText;  // text color of selected item        
    static COLORREF crSelBkgnd; // background color of selected item  
    COLORREF crText;            // text color of unselected item      
    COLORREF crBkgnd;           // background color unselected item   
    LPMEASUREITEMSTRUCT lpmis;  // pointer to item of data             
    LPDRAWITEMSTRUCT lpdis;     // pointer to item drawing data        
    HDC hdc;                    // handle to screen DC                
    SIZE size;                  // menu-item text extents             
    WORD wCheckX;               // check-mark width                   
    int nTextX;                 // width of menu item                 
    int nTextY;                 // height of menu item                
    int i;                      // loop counter                       
    HFONT hfontOld;             // handle to old font                 
    BOOL fSelected = FALSE;     // menu-item selection flag
    size_t * pcch;
    HRESULT hResult;           
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Modify the Regular, Bold, Italic, and Underline 
            // menu items to make them owner-drawn items. Associate 
            // a MYITEM structure with each item to contain the 
            // string for and font handle to each item. 
 
            hmenu = GetMenu(hwnd); 
            ModifyMenu(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED | MF_OWNERDRAW, IDM_REGULAR, 
                (LPTSTR) &myitem[REGULAR]); 
            ModifyMenu(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_BOLD, (LPTSTR) &myitem[BOLD]); 
            ModifyMenu(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ITALIC, 
                (LPTSTR) &myitem[ITALIC]); 
            ModifyMenu(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ULINE, (LPTSTR) &myitem[ULINE]); 
 
            // Retrieve each item's font handle and copy it into 
            // the hfont member of each item's MYITEM structure. 
            // Also, copy each item's string into the structures. 
 
            myitem[REGULAR].hfont = GetAFont(REGULAR); 
            myitem[REGULAR].psz = "Regular"; 
            myitem[BOLD].hfont = GetAFont(BOLD); 
            myitem[BOLD].psz = "Bold"; 
            myitem[ITALIC].hfont = GetAFont(ITALIC); 
            myitem[ITALIC].psz = "Italic"; 
            myitem[ULINE].hfont = GetAFont(ULINE); 
            myitem[ULINE].psz = "Underline"; 
 
            // Retrieve the text and background colors of the 
            // selected menu text. 
 
            crSelText = GetSysColor(COLOR_HIGHLIGHTTEXT); 
            crSelBkgnd = GetSysColor(COLOR_HIGHLIGHT); 
 
            return 0; 
 
        case WM_MEASUREITEM: 
 
            // Retrieve a device context for the main window.  
 
            hdc = GetDC(hwnd); 
 
            // Retrieve pointers to the menu item's 
            // MEASUREITEMSTRUCT structure and MYITEM structure. 
 
            lpmis = (LPMEASUREITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpmis->itemData; 
 
            // Select the font associated with the item into 
            // the main window's device context. 
 
            hfontOld = SelectObject(hdc, pmyitem->hfont); 
 
            // Retrieve the width and height of the item's string, 
            // and then copy the width and height into the 
            // MEASUREITEMSTRUCT structure's itemWidth and 
            // itemHeight members.
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            GetTextExtentPoint32(hdc, pmyitem->psz, 
                *pcch, &size); 
            lpmis->itemWidth = size.cx; 
            lpmis->itemHeight = size.cy; 
 
            // Select the old font back into the device context, 
            // and then release the device context. 
 
            SelectObject(hdc, hfontOld); 
            ReleaseDC(hwnd, hdc); 
 
            return TRUE; 
 
            break; 
 
        case WM_DRAWITEM: 
 
            // Get pointers to the menu item's DRAWITEMSTRUCT 
            // structure and MYITEM structure. 
 
            lpdis = (LPDRAWITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpdis->itemData; 
 
            // If the user has selected the item, use the selected 
            // text and background colors to display the item. 
 
            if (lpdis->itemState & ODS_SELECTED) 
            { 
                crText = SetTextColor(lpdis->hDC, crSelText); 
                crBkgnd = SetBkColor(lpdis->hDC, crSelBkgnd); 
                fSelected = TRUE; 
            } 
 
            // Remember to leave space in the menu item for the 
            // check-mark bitmap. Retrieve the width of the bitmap 
            // and add it to the width of the menu item. 
 
            wCheckX = GetSystemMetrics(SM_CXMENUCHECK); 
            nTextX = wCheckX + lpdis->rcItem.left; 
            nTextY = lpdis->rcItem.top; 
 
            // Select the font associated with the item into the 
            // item's device context, and then draw the string. 
 
            hfontOld = SelectObject(lpdis->hDC, pmyitem->hfont);
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            ExtTextOut(lpdis->hDC, nTextX, nTextY, ETO_OPAQUE, 
                &lpdis->rcItem, pmyitem->psz, 
                *pcch, NULL); 
 
            // Select the previous font back into the device 
            // context. 
 
            SelectObject(lpdis->hDC, hfontOld); 
 
            // Return the text and background colors to their 
            // normal state (not selected). 
 
            if (fSelected) 
            { 
                SetTextColor(lpdis->hDC, crText); 
                SetBkColor(lpdis->hDC, crBkgnd); 
            } 
 
            return TRUE; 
 
        // Process other messages.  
 
        case WM_DESTROY: 
 
            // Destroy the menu items' font handles.  
 
            for (i = 0; i < CITEMS; i++) 
                DeleteObject(myitem[i].hfont); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HFONT GetAFont(int fnFont) 
{ 
    static LOGFONT lf;  // structure for font information  
 
    // Get a handle to the ANSI fixed-pitch font, and copy 
    // information about the font to a LOGFONT structure. 
 
    GetObject(GetStockObject(ANSI_FIXED_FONT), sizeof(LOGFONT), 
        &lf); 
 
    // Set the font attributes, as appropriate.  
 
    if (fnFont == BOLD) 
        lf.lfWeight = FW_BOLD; 
    else 
        lf.lfWeight = FW_NORMAL; 
 
    lf.lfItalic = (fnFont == ITALIC); 
    lf.lfItalic = (fnFont == ULINE); 
 
    // Create the font, and then return its handle.  
 
    return CreateFont(lf.lfHeight, lf.lfWidth, 
        lf.lfEscapement, lf.lfOrientation, lf.lfWeight, 
        lf.lfItalic, lf.lfUnderline, lf.lfStrikeOut, lf.lfCharSet, 
        lf.lfOutPrecision, lf.lfClipPrecision, lf.lfQuality, 
        lf.lfPitchAndFamily, lf.lfFaceName); 
} 
```



### <a name="example-of-owner-drawn-menu-items"></a><span data-ttu-id="2ae81-377">Ejemplo de elementos de menú de Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="2ae81-377">Example of Owner-Drawn Menu Items</span></span>

<span data-ttu-id="2ae81-378">En el ejemplo de este tema se usan elementos de menú dibujados por el propietario en un menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-378">The example in this topic uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="2ae81-379">Los elementos de menú seleccionan atributos de fuente específicos y la aplicación muestra cada elemento de menú mediante una fuente que tiene el atributo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2ae81-379">The menu items select specific font attributes, and the application displays each menu item using a font that has the corresponding attribute.</span></span> <span data-ttu-id="2ae81-380">Por ejemplo, el elemento de menú **cursiva** se muestra en una fuente en cursiva.</span><span class="sxs-lookup"><span data-stu-id="2ae81-380">For example, the **Italic** menu item is displayed in an italic font.</span></span> <span data-ttu-id="2ae81-381">El nombre del menú de **caracteres** en la barra de menús abre el menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-381">The **Character** menu name on the menu bar opens the menu.</span></span>

<span data-ttu-id="2ae81-382">La barra de menús y el menú desplegable se definen inicialmente mediante un recurso de plantilla de menú extendido.</span><span class="sxs-lookup"><span data-stu-id="2ae81-382">The menu bar and drop-down menu are defined initially by an extended menu-template resource.</span></span> <span data-ttu-id="2ae81-383">Dado que una plantilla de menú no puede especificar elementos dibujados por el propietario, el menú contiene inicialmente cuatro elementos de menú de texto con las siguientes cadenas: "normal", "Bold", "Italic" y "underline".</span><span class="sxs-lookup"><span data-stu-id="2ae81-383">Because a menu template cannot specify owner-drawn items, the menu initially contains four text menu items with the following strings: "Regular," "Bold," "Italic," and "Underline."</span></span> <span data-ttu-id="2ae81-384">El procedimiento de ventana de la aplicación los cambia a elementos dibujados por el propietario cuando procesa el mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-384">The application's window procedure changes these to owner-drawn items when it processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="2ae81-385">Cuando recibe el mensaje **de \_ creación de WM** , el procedimiento de ventana llama a la función de creación definida por la aplicación, que realiza los pasos siguientes para cada elemento de menú:</span><span class="sxs-lookup"><span data-stu-id="2ae81-385">When it receives the **WM\_CREATE** message, the window procedure calls the application-defined OnCreate function, which performs the following steps for each menu item:</span></span>

-   <span data-ttu-id="2ae81-386">Asigna una estructura de elemento definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-386">Allocates an application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="2ae81-387">Obtiene el texto del elemento de menú y lo guarda en la estructura de elemento definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-387">Gets the text of the menu item and saves it in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="2ae81-388">Crea la fuente usada para mostrar el elemento de menú y guarda su identificador en la estructura de elementos definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-388">Creates the font used to display the menu item and saves its handle in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="2ae81-389">Cambia el tipo de elemento de menú a **\_ OWNERDRAW de MFT** y guarda un puntero a la estructura de elemento definida por la aplicación como datos de elemento.</span><span class="sxs-lookup"><span data-stu-id="2ae81-389">Changes the menu item type to **MFT\_OWNERDRAW** and saves a pointer to the application-defined MYITEM structure as item data.</span></span>

<span data-ttu-id="2ae81-390">Dado que un puntero a cada estructura de elemento definida por la aplicación se guarda como datos de elemento, se pasa al procedimiento de ventana junto con los mensajes de [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) y [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) para el elemento de menú correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2ae81-390">Because a pointer to each application-defined MYITEM structure is saved as item data, it is passed to the window procedure in conjunction with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages for the corresponding menu item.</span></span> <span data-ttu-id="2ae81-391">El puntero está contenido en el miembro **itemData** de las estructuras [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) y [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-391">The pointer is contained in the **itemData** member of both the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) and [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structures.</span></span>

<span data-ttu-id="2ae81-392">Se envía un mensaje de [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) para cada elemento de menú dibujado por el propietario la primera vez que se muestra.</span><span class="sxs-lookup"><span data-stu-id="2ae81-392">A [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message is sent for each owner-drawn menu item the first time it is displayed.</span></span> <span data-ttu-id="2ae81-393">La aplicación procesa este mensaje seleccionando la fuente del elemento de menú en un contexto de dispositivo y, a continuación, determinando el espacio necesario para mostrar el texto del elemento de menú en esa fuente.</span><span class="sxs-lookup"><span data-stu-id="2ae81-393">The application processes this message by selecting the font for the menu item into a device context and then determining the space required to display the menu item text in that font.</span></span> <span data-ttu-id="2ae81-394">El texto de la fuente y del elemento de menú se especifica mediante la estructura del elemento de menú `MYITEM` (la estructura definida por la aplicación).</span><span class="sxs-lookup"><span data-stu-id="2ae81-394">The font and menu item text are both specified by the menu item's `MYITEM` structure (the structure defined by the application).</span></span> <span data-ttu-id="2ae81-395">La aplicación determina el tamaño del texto mediante la función [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-395">The application determines the size of the text by using the [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) function.</span></span>

<span data-ttu-id="2ae81-396">El procedimiento de ventana procesa el mensaje de Windows de [**WM \_**](../controls/wm-drawitem.md) mostrando el texto del elemento de menú en la fuente adecuada.</span><span class="sxs-lookup"><span data-stu-id="2ae81-396">The window procedure processes the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message by displaying the menu item text in the appropriate font.</span></span> <span data-ttu-id="2ae81-397">La estructura del elemento de menú especifica el texto de la fuente y del elemento de menú `MYITEM` .</span><span class="sxs-lookup"><span data-stu-id="2ae81-397">The font and menu item text are both specified by the menu item's `MYITEM` structure.</span></span> <span data-ttu-id="2ae81-398">La aplicación selecciona los colores de texto y de fondo adecuados para el estado del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-398">The application selects text and background colors appropriate to the menu item's state.</span></span>

<span data-ttu-id="2ae81-399">El procedimiento de ventana procesa el mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) para destruir fuentes y liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="2ae81-399">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message to destroy fonts and free memory.</span></span> <span data-ttu-id="2ae81-400">La aplicación elimina la fuente y libera la estructura de elemento definida por la aplicación para cada elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-400">The application deletes the font and frees the application-defined MYITEM structure for each menu item.</span></span>

<span data-ttu-id="2ae81-401">A continuación se muestran las partes relevantes del archivo de encabezado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-401">The following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_REGULAR   11 
#define IDM_BOLD      12 
#define IDM_ITALIC    13 
#define IDM_UNDERLINE 14 
 
// Structure associated with menu items 
 
typedef struct tagMYITEM 
{ 
    HFONT hfont; 
    int   cchItemText; 
    char  szItemText[1]; 
} MYITEM; 
 
#define CCH_MAXITEMTEXT 256 
 
```



<span data-ttu-id="2ae81-402">A continuación se muestran las partes relevantes del procedimiento de ventana de la aplicación y sus funciones asociadas.</span><span class="sxs-lookup"><span data-stu-id="2ae81-402">The following are the relevant portions of the application's window procedure and its associated functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_MEASUREITEM: 
            OnMeasureItem(hwnd, (LPMEASUREITEMSTRUCT) lParam); 
            return TRUE; 
 
        case WM_DRAWITEM: 
            OnDrawItem(hwnd, (LPDRAWITEMSTRUCT) lParam); 
            return TRUE; 
 
        // Additional message processing goes here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Modify each menu item. Assume that the IDs IDM_REGULAR 
    // through IDM_UNDERLINE are consecutive numbers. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
         // Allocate an item structure, leaving space for a 
         // string of up to CCH_MAXITEMTEXT characters. 
 
        pMyItem = (MYITEM *) LocalAlloc(LMEM_FIXED, 
                sizeof(MYITEM) + CCH_MAXITEMTEXT); 
 
        // Save the item text in the item structure. 
 
        mii.fMask = MIIM_STRING; 
        mii.dwTypeData = pMyItem->szItemText; 
        mii.cch = CCH_MAXITEMTEXT; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem->cchItemText = mii.cch; 
 
        // Reallocate the structure to the minimum required size. 
 
        pMyItem = (MYITEM *) LocalReAlloc(pMyItem, 
                sizeof(MYITEM) + mii.cch, LMEM_MOVEABLE); 
 
        // Create the font used to draw the item. 
 
        pMyItem->hfont = CreateMenuItemFont(uID); 
 
        // Change the item to an owner-drawn item, and save 
        // the address of the item structure as item data. 
 
        mii.fMask = MIIM_FTYPE | MIIM_DATA; 
        mii.fType = MFT_OWNERDRAW; 
        mii.dwItemData = (ULONG_PTR) pMyItem; 
        SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
    } 
    return TRUE; 
} 
 
HFONT CreateMenuItemFont(UINT uID) 
{ 
    LOGFONT lf;
    HRESULT hr; 
 
    ZeroMemory(&lf, sizeof(lf)); 
    lf.lfHeight = 20; 
    hr = StringCchCopy(lf.lfFaceName, 32, "Times New Roman");
    if (FAILED(hr))
    {
    // TODO: writer error handler
    } 
 
    switch (uID) 
    { 
        case IDM_BOLD: 
            lf.lfWeight = FW_HEAVY; 
            break; 
 
        case IDM_ITALIC: 
            lf.lfItalic = TRUE; 
            break; 
 
        case IDM_UNDERLINE: 
            lf.lfUnderline = TRUE; 
            break; 
    } 
    return CreateFontIndirect(&lf); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get  
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Free resources associated with each menu item. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
        // Get the item data. 
 
        mii.fMask = MIIM_DATA; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem = (MYITEM *) mii.dwItemData; 
 
        // Destroy the font and free the item structure. 
 
        DeleteObject(pMyItem->hfont); 
        LocalFree(pMyItem); 
    } 
} 
 
VOID WINAPI OnMeasureItem(HWND hwnd, LPMEASUREITEMSTRUCT lpmis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpmis->itemData; 
    HDC hdc = GetDC(hwnd); 
    HFONT hfntOld = (HFONT)SelectObject(hdc, pMyItem->hfont); 
    SIZE size; 
 
    GetTextExtentPoint32(hdc, pMyItem->szItemText, 
            pMyItem->cchItemText, &size); 
 
    lpmis->itemWidth = size.cx; 
    lpmis->itemHeight = size.cy; 
 
    SelectObject(hdc, hfntOld); 
    ReleaseDC(hwnd, hdc); 
} 
 
VOID WINAPI OnDrawItem(HWND hwnd, LPDRAWITEMSTRUCT lpdis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpdis->itemData; 
    COLORREF clrPrevText, clrPrevBkgnd; 
    HFONT hfntPrev; 
    int x, y; 
 
    // Set the appropriate foreground and background colors. 
 
    if (lpdis->itemState & ODS_SELECTED) 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHTTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHT)); 
    } 
    else 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_MENUTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_MENU)); 
    } 
 
    // Determine where to draw and leave space for a check mark. 
 
    x = lpdis->rcItem.left; 
    y = lpdis->rcItem.top; 
    x += GetSystemMetrics(SM_CXMENUCHECK); 
 
    // Select the font and draw the text. 
 
    hfntPrev = (HFONT)SelectObject(lpdis->hDC, pMyItem->hfont); 
    ExtTextOut(lpdis->hDC, x, y, ETO_OPAQUE, 
            &lpdis->rcItem, pMyItem->szItemText, 
            pMyItem->cchItemText, NULL); 
 
    // Restore the original font and colors. 
 
    SelectObject(lpdis->hDC, hfntPrev); 
    SetTextColor(lpdis->hDC, clrPrevText); 
    SetBkColor(lpdis->hDC, clrPrevBkgnd); 
} 
```



## <a name="using-custom-check-mark-bitmaps"></a><span data-ttu-id="2ae81-403">Usar mapas de bits de marca de verificación personalizada</span><span class="sxs-lookup"><span data-stu-id="2ae81-403">Using Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="2ae81-404">El sistema proporciona un mapa de bits predeterminado de la marca de verificación para mostrar junto a un elemento de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="2ae81-404">The system provides a default check-mark bitmap for displaying next to a menu item that is selected.</span></span> <span data-ttu-id="2ae81-405">Puede personalizar un elemento de menú individual si proporciona un par de mapas de bits para reemplazar el mapa de bits predeterminado de la marca de verificación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-405">You can customize an individual menu item by providing a pair of bitmaps to replace the default check-mark bitmap.</span></span> <span data-ttu-id="2ae81-406">El sistema muestra un mapa de bits cuando el elemento está seleccionado y el otro cuando está claro.</span><span class="sxs-lookup"><span data-stu-id="2ae81-406">The system displays one bitmap when the item is selected and the other when it is clear.</span></span> <span data-ttu-id="2ae81-407">En esta sección se describen los pasos necesarios para crear y usar mapas de bits de marca de verificación personalizados.</span><span class="sxs-lookup"><span data-stu-id="2ae81-407">This section describes the steps involved in creating and using custom check-mark bitmaps.</span></span>

-   [<span data-ttu-id="2ae81-408">Crear mapas de bits de marcas de verificación personalizadas</span><span class="sxs-lookup"><span data-stu-id="2ae81-408">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
-   [<span data-ttu-id="2ae81-409">Asociar mapas de bits a un elemento de menú</span><span class="sxs-lookup"><span data-stu-id="2ae81-409">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
-   [<span data-ttu-id="2ae81-410">Establecer el atributo de marca de verificación</span><span class="sxs-lookup"><span data-stu-id="2ae81-410">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
-   [<span data-ttu-id="2ae81-411">Simular casillas en un menú</span><span class="sxs-lookup"><span data-stu-id="2ae81-411">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
-   [<span data-ttu-id="2ae81-412">Ejemplo de uso de mapas de bits de marcas de verificación personalizadas</span><span class="sxs-lookup"><span data-stu-id="2ae81-412">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a><span data-ttu-id="2ae81-413">Crear mapas de bits de marcas de verificación personalizadas</span><span class="sxs-lookup"><span data-stu-id="2ae81-413">Creating Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="2ae81-414">Un mapa de bits de marca de verificación personalizado debe tener el mismo tamaño que el mapa de bits predeterminado de la marca de verificación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-414">A custom check-mark bitmap must be the same size as the default check-mark bitmap.</span></span> <span data-ttu-id="2ae81-415">Puede recuperar el tamaño predeterminado de la marca de verificación del mapa de bits llamando a la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-415">You can retrieve the default check-mark size of the bitmap by calling the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="2ae81-416">La palabra de orden inferior del valor devuelto de esta función especifica el ancho; la palabra de orden superior especifica el alto.</span><span class="sxs-lookup"><span data-stu-id="2ae81-416">The low-order word of this function's return value specifies the width; the high-order word specifies the height.</span></span>

<span data-ttu-id="2ae81-417">Puede usar los recursos de mapa de bits para proporcionar los mapas de bits de la marca de verificación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-417">You can use bitmap resources to provide check-mark bitmaps.</span></span> <span data-ttu-id="2ae81-418">Sin embargo, dado que el tamaño del mapa de bits necesario varía en función del tipo de presentación, puede que necesite cambiar el tamaño del mapa de bits en tiempo de ejecución mediante la función [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-418">However, because the required bitmap size varies depending on the display type, you may need to resize the bitmap at run time by using the [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) function.</span></span> <span data-ttu-id="2ae81-419">Dependiendo del mapa de bits, la distorsión causada por el ajuste de tamaño podría producir resultados no aceptables.</span><span class="sxs-lookup"><span data-stu-id="2ae81-419">Depending on the bitmap, the distortion caused by sizing could produce unacceptable results.</span></span>

<span data-ttu-id="2ae81-420">En lugar de utilizar un recurso de mapa de bits, puede crear un mapa de bits en tiempo de ejecución mediante las funciones GDI.</span><span class="sxs-lookup"><span data-stu-id="2ae81-420">Instead of using a bitmap resource, you can create a bitmap at run time by using GDI functions.</span></span>

<span data-ttu-id="2ae81-421">**Para crear un mapa de bits en tiempo de ejecución**</span><span class="sxs-lookup"><span data-stu-id="2ae81-421">**To create a bitmap at run time**</span></span>

1.  <span data-ttu-id="2ae81-422">Use la función [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) para crear un contexto de dispositivo compatible con el que usa la ventana principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-422">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the one used by the application's main window.</span></span>

    <span data-ttu-id="2ae81-423">El parámetro *HDC* de la función puede especificar **null** o el valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="2ae81-423">The function's *hdc* parameter can specify either **NULL** or the return value from the function.</span></span> <span data-ttu-id="2ae81-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) devuelve un identificador para el contexto de dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="2ae81-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) returns a handle to the compatible device context.</span></span>

2.  <span data-ttu-id="2ae81-425">Use la función [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) para crear un mapa de bits compatible con la ventana principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-425">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window.</span></span>

    <span data-ttu-id="2ae81-426">Los parámetros *nWidth* y *nHeight* de esta función establecen el tamaño del mapa de bits; deben especificar la información de ancho y alto devuelta por la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-426">This function's *nWidth* and *nHeight* parameters set the size of the bitmap; they should specify the width and height information returned by the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span>

    > [!Note]  
    > <span data-ttu-id="2ae81-427">También puede usar la función [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) para crear un mapa de bits monocromo.</span><span class="sxs-lookup"><span data-stu-id="2ae81-427">You can also use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>

     

3.  <span data-ttu-id="2ae81-428">Use la función [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para seleccionar el mapa de bits en el contexto de dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="2ae81-428">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="2ae81-429">Use funciones de dibujo de GDI, como [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) y [**lineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), para dibujar una imagen en el mapa de bits, o use funciones como [**bitblt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) y [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) para copiar una imagen en el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="2ae81-429">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap, or use functions such as [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) and [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) to copy an image into the bitmap.</span></span>

<span data-ttu-id="2ae81-430">Para obtener más información, vea [mapas de bits](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="2ae81-430">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="associating-bitmaps-with-a-menu-item"></a><span data-ttu-id="2ae81-431">Asociar mapas de bits a un elemento de menú</span><span class="sxs-lookup"><span data-stu-id="2ae81-431">Associating Bitmaps with a Menu Item</span></span>

<span data-ttu-id="2ae81-432">Para asociar un par de mapas de bits de marca de verificación a un elemento de menú, puede pasar los identificadores de los mapas de bits a la función [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-432">You associate a pair of check-mark bitmaps with a menu item by passing the handles of the bitmaps to the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span> <span data-ttu-id="2ae81-433">El parámetro *hBitmapUnchecked* identifica el mapa de bits de borrado y el parámetro *hBitmapChecked* identifica el mapa de bits seleccionado.</span><span class="sxs-lookup"><span data-stu-id="2ae81-433">The *hBitmapUnchecked* parameter identifies the clear bitmap, and the *hBitmapChecked* parameter identifies the selected bitmap.</span></span> <span data-ttu-id="2ae81-434">Si desea quitar una o ambas marcas de verificación de un elemento de menú, puede establecer el parámetro *hBitmapUnchecked* o *hBitmapChecked* , o ambos, en **null**.</span><span class="sxs-lookup"><span data-stu-id="2ae81-434">If you want to remove one or both check marks from a menu item, you can set the *hBitmapUnchecked* or *hBitmapChecked* parameter, or both, to **NULL**.</span></span>

### <a name="setting-the-check-mark-attribute"></a><span data-ttu-id="2ae81-435">Establecer el atributo de marca de verificación</span><span class="sxs-lookup"><span data-stu-id="2ae81-435">Setting the Check-mark Attribute</span></span>

<span data-ttu-id="2ae81-436">La función [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) establece el atributo de marca de verificación de un elemento de menú en activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="2ae81-436">The [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) function sets a menu item's check-mark attribute to either selected or cleared.</span></span> <span data-ttu-id="2ae81-437">Puede especificar el valor de **MF \_ activado** para establecer el atributo de marca de verificación en seleccionado y el valor de **MF sin \_ comprobar** para establecerlo en borrar.</span><span class="sxs-lookup"><span data-stu-id="2ae81-437">You can specify the **MF\_CHECKED** value to set the check-mark attribute to selected and the **MF\_UNCHECKED** value to set it to clear.</span></span>

<span data-ttu-id="2ae81-438">También puede establecer el estado de activación de un elemento de menú mediante la función [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-438">You can also set the check state of a menu item by using the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="2ae81-439">A veces, un grupo de elementos de menú representa un conjunto de opciones mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="2ae81-439">Sometimes a group of menu items represents a set of mutually exclusive options.</span></span> <span data-ttu-id="2ae81-440">Mediante el uso de la función [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) , puede comprobar un elemento de menú mientras quita simultáneamente la marca de verificación de los demás elementos de menú del grupo.</span><span class="sxs-lookup"><span data-stu-id="2ae81-440">By using the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function, you can check one menu item while simultaneously removing the check mark from all other menu items in the group.</span></span>

### <a name="simulating-check-boxes-in-a-menu"></a><span data-ttu-id="2ae81-441">Simular casillas en un menú</span><span class="sxs-lookup"><span data-stu-id="2ae81-441">Simulating Check Boxes in a Menu</span></span>

<span data-ttu-id="2ae81-442">Este tema contiene un ejemplo que muestra cómo simular casillas en un menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-442">This topic contains an example that shows how to simulate check boxes in a menu.</span></span> <span data-ttu-id="2ae81-443">El ejemplo contiene un menú de caracteres cuyos elementos permiten al usuario establecer los atributos Bold, Italic y underline de la fuente actual.</span><span class="sxs-lookup"><span data-stu-id="2ae81-443">The example contains a Character menu whose items allow the user to set the bold, italic, and underline attributes of the current font.</span></span> <span data-ttu-id="2ae81-444">Cuando un atributo de fuente está en vigor, se muestra una marca de verificación en la casilla situada junto al elemento de menú correspondiente; de lo contrario, se muestra una casilla vacía junto al elemento.</span><span class="sxs-lookup"><span data-stu-id="2ae81-444">When a font attribute is in effect, a check mark is displayed in the check box next to the corresponding menu item; otherwise, an empty check box is displayed next to the item.</span></span>

<span data-ttu-id="2ae81-445">En el ejemplo se reemplaza el mapa de bits de la marca de verificación predeterminada con dos mapas de bits: un mapa de bits con una casilla seleccionada y el mapa de bits con un cuadro vacío.</span><span class="sxs-lookup"><span data-stu-id="2ae81-445">The example replaces the default check-mark bitmap with two bitmaps: a bitmap with a selected check box and the bitmap with an empty box.</span></span> <span data-ttu-id="2ae81-446">El mapa de bits seleccionado se muestra junto al elemento de menú negrita, cursiva o subrayado cuando el atributo de marca de verificación del elemento está **\_ activado MF**.</span><span class="sxs-lookup"><span data-stu-id="2ae81-446">The selected check box bitmap is displayed next to the Bold, Italic, or Underline menu item when the item's check-mark attribute is set to **MF\_CHECKED**.</span></span> <span data-ttu-id="2ae81-447">El mapa de bits de la casilla de verificación borrar o vacío se muestra cuando el atributo de marca de verificación está establecido en **MF \_ desactivado**.</span><span class="sxs-lookup"><span data-stu-id="2ae81-447">The clear or empty check box bitmap is displayed when the check-mark attribute is set to **MF\_UNCHECKED**.</span></span>

<span data-ttu-id="2ae81-448">El sistema proporciona un mapa de bits predefinido que contiene las imágenes que se utilizan para las casillas y los botones de radio.</span><span class="sxs-lookup"><span data-stu-id="2ae81-448">The system provides a predefined bitmap that contains the images used for check boxes and radio buttons.</span></span> <span data-ttu-id="2ae81-449">En el ejemplo se aíslan las casillas de verificación seleccionadas y vacías, se copian en dos mapas de bits independientes y, a continuación, se usan como los mapas de bits seleccionados y borrados para los elementos del menú de **caracteres** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-449">The example isolates the selected and empty check boxes, copies them to two separate bitmaps, and then uses them as the selected and cleared bitmaps for items in the **Character** menu.</span></span>

<span data-ttu-id="2ae81-450">Para recuperar un identificador del mapa de bits de la casilla de verificación definida por el sistema, el ejemplo llama a la función [**loadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , especificando **null** como el parámetro *hInstance* y las **\_ casillas OBM** como el parámetro *lpBitmapName* .</span><span class="sxs-lookup"><span data-stu-id="2ae81-450">To retrieve a handle to the system-defined check box bitmap, the example calls the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, specifying **NULL** as the *hInstance* parameter and **OBM\_CHECKBOXES** as the *lpBitmapName* parameter.</span></span> <span data-ttu-id="2ae81-451">Dado que las imágenes del mapa de bits tienen el mismo tamaño, el ejemplo puede aislarlas dividiendo el ancho y el alto del mapa de bits entre el número de imágenes de sus filas y columnas.</span><span class="sxs-lookup"><span data-stu-id="2ae81-451">Because the images in the bitmap are all the same size, the example can isolate them by dividing the bitmap width and height by the number of images in its rows and columns.</span></span>

<span data-ttu-id="2ae81-452">La siguiente parte de un archivo de definición de recursos muestra cómo se definen los elementos de menú en el menú de **caracteres** .</span><span class="sxs-lookup"><span data-stu-id="2ae81-452">The following portion of a resource-definition file shows how the menu items in the **Character** menu are defined.</span></span> <span data-ttu-id="2ae81-453">Tenga en cuenta que no se aplica inicialmente ningún atributo de fuente, por lo que el atributo de marca de verificación del elemento **normal** se establece en seleccionado y, de forma predeterminada, el atributo de marca de verificación de los elementos restantes se establece en borrar.</span><span class="sxs-lookup"><span data-stu-id="2ae81-453">Note that no font attributes are in effect initially, so the check-mark attribute for the **Regular** item is set to selected and, by default, the check-mark attribute of the remaining items is set to clear.</span></span>


```
#include "men3.h" 
 
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "&Regular",     IDM_REGULAR, CHECKED 
        MENUITEM SEPARATOR 
        MENUITEM    "&Bold",        IDM_BOLD 
        MENUITEM    "&Italic",      IDM_ITALIC 
        MENUITEM    "&Underline",   IDM_ULINE 
    END 
END
```



<span data-ttu-id="2ae81-454">Este es el contenido pertinente del archivo de encabezado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-454">Here are the relevant contents of the application's header file.</span></span>


```
// Menu-item identifiers  
 
#define IDM_REGULAR 0x1 
#define IDM_BOLD    0x2 
#define IDM_ITALIC  0x4 
#define IDM_ULINE   0x8 
 
// Check-mark flags  
 
#define CHECK   1 
#define UNCHECK 2 
 
// Font-attribute mask  
 
#define ATTRIBMASK 0xe 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
HBITMAP GetMyCheckBitmaps(UINT); 
BYTE CheckOrUncheckMenuItem(BYTE, HMENU); 
```



<span data-ttu-id="2ae81-455">En el ejemplo siguiente se muestran las partes del procedimiento de ventana que crean los mapas de bits de la marca de verificación; Establezca el atributo de marca de verificación de los elementos de menú **negrita**, **cursiva** y **subrayado** ; y destruyen los mapas de bits de la marca de verificación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-455">The following example shows the portions of the window procedure that create the check-mark bitmaps; set the check-mark attribute of the **Bold**, **Italic**, and **Underline** menu items; and destroy check-mark bitmaps.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HBITMAP hbmpCheck;   // handle to checked bitmap    
    static HBITMAP hbmpUncheck; // handle to unchecked bitmap  
    static HMENU hmenu;         // handle to main menu         
    BYTE fbFontAttrib;          // font-attribute flags        
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Call the application-defined GetMyCheckBitmaps 
            // function to get the predefined checked and 
            // unchecked check box bitmaps. 
 
            hbmpCheck = GetMyCheckBitmaps(CHECK); 
            hbmpUncheck = GetMyCheckBitmaps(UNCHECK); 
 
            // Set the checked and unchecked bitmaps for the menu 
            // items. 
 
            hmenu = GetMenu(hwndMain); 
            SetMenuItemBitmaps(hmenu, IDM_BOLD, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ITALIC, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ULINE, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the menu commands.  
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // CheckOrUncheckMenuItem is an application- 
                    // defined function that sets the menu item 
                    // checkmarks and returns the user-selected 
                    // font attributes. 
 
                    fbFontAttrib = CheckOrUncheckMenuItem( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // Set the font attributes.  
 
                    return 0; 
 
                // Process other command messages.  
 
                default: 
                    break; 
            } 
 
            break; 
 
        // Process other window messages.  
 
        case WM_DESTROY: 
 
            // Destroy the checked and unchecked bitmaps.  
 
            DeleteObject(hbmpCheck); 
            DeleteObject(hbmpUncheck); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HBITMAP GetMyCheckBitmaps(UINT fuCheck) 
{ 
    COLORREF crBackground;  // background color                  
    HBRUSH hbrBackground;   // background brush                  
    HBRUSH hbrTargetOld;    // original background brush         
    HDC hdcSource;          // source device context             
    HDC hdcTarget;          // target device context             
    HBITMAP hbmpCheckboxes; // handle to check-box bitmap        
    BITMAP bmCheckbox;      // structure for bitmap data         
    HBITMAP hbmpSourceOld;  // handle to original source bitmap  
    HBITMAP hbmpTargetOld;  // handle to original target bitmap  
    HBITMAP hbmpCheck;      // handle to check-mark bitmap       
    RECT rc;                // rectangle for check-box bitmap    
    WORD wBitmapX;          // width of check-mark bitmap        
    WORD wBitmapY;          // height of check-mark bitmap       
 
    // Get the menu background color and create a solid brush 
    // with that color. 
 
    crBackground = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crBackground); 
 
    // Create memory device contexts for the source and 
    // destination bitmaps. 
 
    hdcSource = CreateCompatibleDC((HDC) NULL); 
    hdcTarget = CreateCompatibleDC(hdcSource); 
 
    // Get the size of the system default check-mark bitmap and 
    // create a compatible bitmap of the same size. 
 
    wBitmapX = GetSystemMetrics(SM_CXMENUCHECK); 
    wBitmapY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    hbmpCheck = CreateCompatibleBitmap(hdcSource, wBitmapX, 
        wBitmapY); 
 
    // Select the background brush and bitmap into the target DC. 
 
    hbrTargetOld = SelectObject(hdcTarget, hbrBackground); 
    hbmpTargetOld = SelectObject(hdcTarget, hbmpCheck); 
 
    // Use the selected brush to initialize the background color 
    // of the bitmap in the target device context. 
 
    PatBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, PATCOPY); 
 
    // Load the predefined check box bitmaps and select it 
    // into the source DC. 
 
    hbmpCheckboxes = LoadBitmap((HINSTANCE) NULL, 
        (LPTSTR) OBM_CHECKBOXES); 
 
    hbmpSourceOld = SelectObject(hdcSource, hbmpCheckboxes); 
 
    // Fill a BITMAP structure with information about the 
    // check box bitmaps, and then find the upper-left corner of 
    // the unchecked check box or the checked check box. 
 
    GetObject(hbmpCheckboxes, sizeof(BITMAP), &bmCheckbox); 
 
    if (fuCheck == UNCHECK) 
    { 
        rc.left = 0; 
        rc.right = (bmCheckbox.bmWidth / 4); 
    } 
    else 
    { 
        rc.left = (bmCheckbox.bmWidth / 4); 
        rc.right = (bmCheckbox.bmWidth / 4) * 2; 
    } 
 
    rc.top = 0; 
    rc.bottom = (bmCheckbox.bmHeight / 3); 
 
    // Copy the appropriate bitmap into the target DC. If the 
    // check-box bitmap is larger than the default check-mark 
    // bitmap, use StretchBlt to make it fit; otherwise, just 
    // copy it. 
 
    if (((rc.right - rc.left) > (int) wBitmapX) || 
            ((rc.bottom - rc.top) > (int) wBitmapY)) 
    {
        StretchBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, 
            hdcSource, rc.left, rc.top, rc.right - rc.left, 
            rc.bottom - rc.top, SRCCOPY); 
    }
 
    else 
    {
        BitBlt(hdcTarget, 0, 0, rc.right - rc.left, 
            rc.bottom - rc.top, 
            hdcSource, rc.left, rc.top, SRCCOPY); 
    }
 
    // Select the old source and destination bitmaps into the 
    // source and destination DCs, and then delete the DCs and 
    // the background brush. 
 
    SelectObject(hdcSource, hbmpSourceOld); 
    SelectObject(hdcTarget, hbrTargetOld); 
    hbmpCheck = SelectObject(hdcTarget, hbmpTargetOld); 
 
    DeleteObject(hbrBackground); 
    DeleteObject(hdcSource); 
    DeleteObject(hdcTarget); 
 
    // Return a handle to the new check-mark bitmap.  
 
    return hbmpCheck; 
} 
 
 
BYTE CheckOrUncheckMenuItem(BYTE bMenuItemID, HMENU hmenu) 
{ 
    DWORD fdwMenu; 
    static BYTE fbAttributes; 
 
    switch (bMenuItemID) 
    { 
        case IDM_REGULAR: 
 
            // Whenever the Regular menu item is selected, add a 
            // check mark to it and then remove checkmarks from 
            // any font-attribute menu items. 
 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
            } 
            fbAttributes = IDM_REGULAR; 
            return fbAttributes; 
 
        case IDM_BOLD: 
        case IDM_ITALIC: 
        case IDM_ULINE: 
 
            // Toggle the check mark for the selected menu item and 
            // set the font attribute flags appropriately. 
 
            fdwMenu = GetMenuState(hmenu, (UINT) bMenuItemID, 
                MF_BYCOMMAND); 
            if (!(fdwMenu & MF_CHECKED)) 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes |= bMenuItemID; 
            }
            else 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes ^= bMenuItemID; 
            } 
 
            // If any font attributes are currently selected, 
            // remove the check mark from the Regular menu item; 
            // if no attributes are selected, add a check mark 
            // to the Regular menu item. 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes &= (BYTE) ~IDM_REGULAR; 
            }
            else 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes = IDM_REGULAR; 
            } 
 
            return fbAttributes; 
    } 
} 
```



### <a name="example-of-using-custom-check-mark-bitmaps"></a><span data-ttu-id="2ae81-456">Ejemplo de uso de mapas de bits de marcas de verificación personalizadas</span><span class="sxs-lookup"><span data-stu-id="2ae81-456">Example of Using Custom Check-mark Bitmaps</span></span>

<span data-ttu-id="2ae81-457">En el ejemplo de este tema se asignan mapas de bits de marca de verificación personalizados a los elementos de menú de dos menús.</span><span class="sxs-lookup"><span data-stu-id="2ae81-457">The example in this topic assigns custom check-mark bitmaps to menu items in two menus.</span></span> <span data-ttu-id="2ae81-458">Los elementos de menú del primer menú especifican los atributos de carácter: negrita, cursiva y subrayado.</span><span class="sxs-lookup"><span data-stu-id="2ae81-458">The menu items in the first menu specify character attributes: bold, italic, and underline.</span></span> <span data-ttu-id="2ae81-459">Cada elemento de menú puede seleccionarse o borrarse.</span><span class="sxs-lookup"><span data-stu-id="2ae81-459">Each menu item can be either selected or cleared.</span></span> <span data-ttu-id="2ae81-460">En el caso de estos elementos de menú, el ejemplo utiliza los mapas de bits de la marca de verificación que se asemejan a los Estados seleccionados y desactivados de un control de casilla.</span><span class="sxs-lookup"><span data-stu-id="2ae81-460">For these menu items, the example uses check-mark bitmaps that resemble the selected and cleared states of a check box control.</span></span>

<span data-ttu-id="2ae81-461">Los elementos de menú del segundo menú especifican la configuración de alineación de párrafo: izquierda, centrada y derecha.</span><span class="sxs-lookup"><span data-stu-id="2ae81-461">The menu items in the second menu specify paragraph alignment settings: left, centered, and right.</span></span> <span data-ttu-id="2ae81-462">En cualquier momento solo se selecciona uno de estos elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-462">Only one of these menu items is selected at any time.</span></span> <span data-ttu-id="2ae81-463">En el caso de estos elementos de menú, el ejemplo utiliza mapas de bits de marca de verificación que se asemejan a los Estados seleccionados y claros de un control de botón de radio.</span><span class="sxs-lookup"><span data-stu-id="2ae81-463">For these menu items, the example uses check-mark bitmaps that resemble the selected and clear states of a radio button control.</span></span>

<span data-ttu-id="2ae81-464">El procedimiento de ventana procesa el mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) llamando a la función de creación definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-464">The window procedure processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message by calling the application-defined OnCreate function.</span></span> <span data-ttu-id="2ae81-465">`OnCreate` crea los cuatro mapas de bits de la marca de verificación y, a continuación, los asigna a los elementos de menú correspondientes mediante la función [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-465">`OnCreate` creates the four check-mark bitmaps and then assigns them to their appropriate menu items by using the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span>

<span data-ttu-id="2ae81-466">Para crear cada mapa de bits, alcrear llama a la función CreateMenuBitmaps definida por la aplicación, especificando un puntero a una función de dibujo específica del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="2ae81-466">To create each bitmap, OnCreate calls the application-defined CreateMenuBitmaps function, specifying a pointer to a bitmap-specific drawing function.</span></span> <span data-ttu-id="2ae81-467">CreateMenuBitmaps crea un mapa de bits monocromo del tamaño requerido, lo selecciona en un contexto de dispositivo de memoria y borra el fondo.</span><span class="sxs-lookup"><span data-stu-id="2ae81-467">CreateMenuBitmaps creates a monochrome bitmap of the required size, selects it into a memory device context, and erases the background.</span></span> <span data-ttu-id="2ae81-468">A continuación, llama a la función de dibujo especificada para rellenar el primer plano.</span><span class="sxs-lookup"><span data-stu-id="2ae81-468">Then it calls the specified drawing function to fill in the foreground.</span></span>

<span data-ttu-id="2ae81-469">Las cuatro funciones de dibujo definidas por la aplicación son DrawCheck, DrawUncheck, **DrawRadioCheck** y DrawRadioUncheck.</span><span class="sxs-lookup"><span data-stu-id="2ae81-469">The four application-defined drawing functions are DrawCheck, DrawUncheck, **DrawRadioCheck**, and DrawRadioUncheck.</span></span> <span data-ttu-id="2ae81-470">Dibujan un rectángulo con una X, un rectángulo vacío, una elipse que contiene una elipse rellena más pequeña y una elipse vacía, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2ae81-470">They draw a rectangle with an X, an empty rectangle, an ellipse containing a smaller filled ellipse, and an empty ellipse, respectively.</span></span>

<span data-ttu-id="2ae81-471">El procedimiento de ventana procesa el mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) eliminando los mapas de bits de la marca de verificación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-471">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message by deleting the check-mark bitmaps.</span></span> <span data-ttu-id="2ae81-472">Recupera cada identificador de mapa de bits mediante la función [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) y, a continuación, pasa un identificador a la función.</span><span class="sxs-lookup"><span data-stu-id="2ae81-472">It retrieves each bitmap handle by using the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function and then passes a handle to the function.</span></span>

<span data-ttu-id="2ae81-473">Cuando el usuario elige un elemento de menú, se envía un mensaje de [**\_ comando de WM**](wm-command.md) a la ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="2ae81-473">When the user chooses a menu item, a [**WM\_COMMAND**](wm-command.md) message is sent to the owner window.</span></span> <span data-ttu-id="2ae81-474">En el caso de los elementos de menú en el menú **carácter** , el procedimiento de ventana llama a la función CheckCharacterItem definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-474">For menu items on the **Character** menu, the window procedure calls the application-defined CheckCharacterItem function.</span></span> <span data-ttu-id="2ae81-475">En el caso de los elementos del menú **párrafo** , el procedimiento de ventana llama a la función CheckParagraphItem definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-475">For items on the **Paragraph** menu, the window procedure calls the application-defined CheckParagraphItem function.</span></span>

<span data-ttu-id="2ae81-476">Cada elemento del menú de **caracteres** puede seleccionarse y borrarse de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="2ae81-476">Each item on the **Character** menu can be selected and cleared independently.</span></span> <span data-ttu-id="2ae81-477">Por lo tanto, CheckCharacterItem simplemente cambia el estado de activación del elemento de menú especificado.</span><span class="sxs-lookup"><span data-stu-id="2ae81-477">Therefore, CheckCharacterItem simply switches the specified menu item's check state.</span></span> <span data-ttu-id="2ae81-478">En primer lugar, la función llama a la función [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) para obtener el estado del elemento de menú actual.</span><span class="sxs-lookup"><span data-stu-id="2ae81-478">First, the function calls the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function to get the current menu item state.</span></span> <span data-ttu-id="2ae81-479">A continuación, cambia la marca de estado **\_ Checked de MFS** y establece el nuevo estado mediante una llamada a la función [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-479">Then it switches the **MFS\_CHECKED** state flag and sets the new state by calling the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="2ae81-480">A diferencia de los atributos de carácter, solo se puede seleccionar una alineación de párrafo a la vez.</span><span class="sxs-lookup"><span data-stu-id="2ae81-480">Unlike character attributes, only one paragraph alignment can be selected at a time.</span></span> <span data-ttu-id="2ae81-481">Por lo tanto, CheckParagraphItem comprueba el elemento de menú especificado y quita la marca de verificación de todos los demás elementos del menú.</span><span class="sxs-lookup"><span data-stu-id="2ae81-481">Therefore, CheckParagraphItem checks the specified menu item and removes the check mark from all other items on the menu.</span></span> <span data-ttu-id="2ae81-482">Para ello, llama a la función [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) .</span><span class="sxs-lookup"><span data-stu-id="2ae81-482">To do so, it calls the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function.</span></span>

<span data-ttu-id="2ae81-483">A continuación se muestran las partes relevantes del archivo de encabezado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ae81-483">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_BOLD      11 
#define IDM_ITALIC    12 
#define IDM_UNDERLINE 13 
 
// Menu-item identifiers for the Paragraph menu 
 
#define IDM_PARAGRAPH 20 
#define IDM_LEFT      21 
#define IDM_CENTER    22 
#define IDM_RIGHT     23 
 
// Function-pointer type for drawing functions 
 
typedef VOID (WINAPI * DRAWFUNC)(HDC hdc, SIZE size); 
 
```



<span data-ttu-id="2ae81-484">A continuación se muestran las partes relevantes del procedimiento de ventana de la aplicación y las funciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2ae81-484">The following are the relevant portions of the application's window procedure and related functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_UNDERLINE: 
                    CheckCharacterItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                case IDM_LEFT: 
                case IDM_CENTER: 
                case IDM_RIGHT: 
                    CheckParagraphItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                // Process other commands here. 
 
            } 
            break; 
 
        // Process other messages here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
VOID WINAPI CheckCharacterItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the state of the specified menu item. 
 
    mii.fMask = MIIM_STATE;    // information to get 
    GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
 
    // Toggle the checked state. 
 
    mii.fState ^= MFS_CHECKED; 
    SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
} 
 
VOID WINAPI CheckParagraphItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Check the specified item and uncheck all the others. 
 
    CheckMenuRadioItem( 
            hmenuPopup,         // handle to menu 
            IDM_LEFT,           // first item in range 
            IDM_RIGHT,          // last item in range 
            uID,                // item to check 
            MF_BYCOMMAND        // IDs, not positions 
            ); 
} 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    HBITMAP hbmChecked; 
    HBITMAP hbmUnchecked; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_BOLD; uID <= IDM_UNDERLINE; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Get a handle to the Paragraph pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawRadioCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawRadioUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_LEFT; uID <= IDM_RIGHT; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Initially check the IDM_LEFT paragraph item. 
 
    CheckMenuRadioItem(hmenuPopup, IDM_LEFT, IDM_RIGHT, 
            IDM_LEFT, MF_BYCOMMAND); 
    return TRUE; 
} 
 
HBITMAP WINAPI CreateMenuBitmap(DRAWFUNC lpfnDraw) 
{ 
    // Create a DC compatible with the desktop window's DC. 
 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
 
    // Determine the required bitmap size. 
 
    SIZE size = { GetSystemMetrics(SM_CXMENUCHECK), 
                  GetSystemMetrics(SM_CYMENUCHECK) }; 
 
    // Create a monochrome bitmap and select it. 
 
    HBITMAP hbm = CreateBitmap(size.cx, size.cy, 1, 1, NULL); 
    HBITMAP hbmOld = SelectObject(hdcMem, hbm); 
 
    // Erase the background and call the drawing function. 
 
    PatBlt(hdcMem, 0, 0, size.cx, size.cy, WHITENESS); 
    (*lpfnDraw)(hdcMem, size); 
 
    // Clean up. 
 
    SelectObject(hdcMem, hbmOld); 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
    return hbm; 
} 
 
VOID WINAPI DrawCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    MoveToEx(hdc, 0, 0, NULL); 
    LineTo(hdc, size.cx, size.cy); 
    MoveToEx(hdc, 0, size.cy - 1, NULL); 
    LineTo(hdc, size.cx - 1, 0); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, GetStockObject(BLACK_BRUSH)); 
    Ellipse(hdc, 2, 2, size.cx - 2, size.cy - 2); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_BOLD, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_LEFT, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
} 
```



 

 