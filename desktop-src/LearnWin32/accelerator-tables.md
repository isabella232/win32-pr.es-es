---
title: Tablas de aceleradores
description: .
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9929445809bee71f273b6bd2334e182de59edbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077762"
---
# <a name="accelerator-tables"></a><span data-ttu-id="3eb17-103">Tablas de aceleradores</span><span class="sxs-lookup"><span data-stu-id="3eb17-103">Accelerator Tables</span></span>

<span data-ttu-id="3eb17-104">Las aplicaciones a menudo definen los métodos abreviados de teclado, como CTRL + O para el comando Abrir archivo.</span><span class="sxs-lookup"><span data-stu-id="3eb17-104">Applications often define keyboard shortcuts, such as CTRL+O for the File Open command.</span></span> <span data-ttu-id="3eb17-105">Puede implementar los métodos abreviados de teclado mediante el control de mensajes [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) individuales, pero las tablas de aceleradores proporcionan una mejor solución que:</span><span class="sxs-lookup"><span data-stu-id="3eb17-105">You could implement keyboard shortcuts by handling individual [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, but accelerator tables provide a better solution that:</span></span>

-   <span data-ttu-id="3eb17-106">Requiere menos codificación.</span><span class="sxs-lookup"><span data-stu-id="3eb17-106">Requires less coding.</span></span>
-   <span data-ttu-id="3eb17-107">Consolida todos los accesos directos en un archivo de datos.</span><span class="sxs-lookup"><span data-stu-id="3eb17-107">Consolidates all of your shortcuts into one data file.</span></span>
-   <span data-ttu-id="3eb17-108">Admite la localización en otros idiomas.</span><span class="sxs-lookup"><span data-stu-id="3eb17-108">Supports localization into other languages.</span></span>
-   <span data-ttu-id="3eb17-109">Permite que los accesos directos y los comandos de menú usen la misma lógica de aplicación.</span><span class="sxs-lookup"><span data-stu-id="3eb17-109">Enables shortcuts and menu commands to use the same application logic.</span></span>

<span data-ttu-id="3eb17-110">Una *tabla de aceleradores* es un recurso de datos que asigna combinaciones de teclado, como Ctrl + O, a comandos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3eb17-110">An *accelerator table* is a data resource that maps keyboard combinations, such as CTRL+O, to application commands.</span></span> <span data-ttu-id="3eb17-111">Antes de que podamos ver cómo usar una tabla de aceleradores, necesitamos una introducción rápida a los recursos.</span><span class="sxs-lookup"><span data-stu-id="3eb17-111">Before we see how to use an accelerator table, we'll need a quick introduction to resources.</span></span> <span data-ttu-id="3eb17-112">Un *recurso* es un BLOB de datos integrado en un archivo binario de la aplicación (exe o dll).</span><span class="sxs-lookup"><span data-stu-id="3eb17-112">A *resource* is a data blob that is built into an application binary (EXE or DLL).</span></span> <span data-ttu-id="3eb17-113">Los recursos almacenan los datos que necesita la aplicación, como menús, cursores, iconos, imágenes, cadenas de texto o cualquier dato de aplicación personalizado.</span><span class="sxs-lookup"><span data-stu-id="3eb17-113">Resources store data that are needed by the application, such as menus, cursors, icons, images, text strings, or any custom application data.</span></span> <span data-ttu-id="3eb17-114">La aplicación carga los datos de recursos desde el archivo binario en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3eb17-114">The application loads the resource data from the binary at run time.</span></span> <span data-ttu-id="3eb17-115">Para incluir recursos en un archivo binario, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3eb17-115">To include resources in a binary, do the following:</span></span>

1.  <span data-ttu-id="3eb17-116">Cree un archivo de definición de recursos (. RC).</span><span class="sxs-lookup"><span data-stu-id="3eb17-116">Create a resource definition (.rc) file.</span></span> <span data-ttu-id="3eb17-117">Este archivo define los tipos de recursos y sus identificadores.</span><span class="sxs-lookup"><span data-stu-id="3eb17-117">This file defines the types of resources and their identifiers.</span></span> <span data-ttu-id="3eb17-118">El archivo de definición de recursos puede incluir referencias a otros archivos.</span><span class="sxs-lookup"><span data-stu-id="3eb17-118">The resource definition file may include references to other files.</span></span> <span data-ttu-id="3eb17-119">Por ejemplo, un recurso de icono se declara en el archivo. rc, pero la imagen de icono se almacena en un archivo independiente.</span><span class="sxs-lookup"><span data-stu-id="3eb17-119">For example, an icon resource is declared in the .rc file, but the icon image is stored in a separate file.</span></span>
2.  <span data-ttu-id="3eb17-120">Use el compilador de recursos de Microsoft Windows (RC) para compilar el archivo de definición de recursos en un archivo de recursos compilado (. res).</span><span class="sxs-lookup"><span data-stu-id="3eb17-120">Use the Microsoft Windows Resource Compiler (RC) to compile the resource definition file into a compiled resource (.res) file.</span></span> <span data-ttu-id="3eb17-121">El compilador RC se proporciona con Visual Studio y también el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3eb17-121">The RC compiler is provided with Visual Studio and also the Windows SDK.</span></span>
3.  <span data-ttu-id="3eb17-122">Vincule el archivo de recursos compilado al archivo binario.</span><span class="sxs-lookup"><span data-stu-id="3eb17-122">Link the compiled resource file to the binary file.</span></span>

<span data-ttu-id="3eb17-123">Estos pasos son aproximadamente equivalentes al proceso de compilación y vinculación de archivos de código.</span><span class="sxs-lookup"><span data-stu-id="3eb17-123">These steps are roughly equivalent to the compile/link process for code files.</span></span> <span data-ttu-id="3eb17-124">Visual Studio proporciona un conjunto de editores de recursos que facilitan la creación y modificación de recursos.</span><span class="sxs-lookup"><span data-stu-id="3eb17-124">Visual Studio provides a set of resource editors that make it easy to create and modify resources.</span></span> <span data-ttu-id="3eb17-125">(Estas herramientas no están disponibles en las ediciones Express de Visual Studio). Pero un archivo. RC es simplemente un archivo de texto y la sintaxis se documenta en MSDN, por lo que es posible crear un archivo. RC con cualquier editor de texto.</span><span class="sxs-lookup"><span data-stu-id="3eb17-125">(These tools are not available in the Express editions of Visual Studio.) But an .rc file is simply a text file, and the syntax is documented on MSDN, so it is possible to create an .rc file using any text editor.</span></span> <span data-ttu-id="3eb17-126">Para obtener más información, consulte [acerca de los archivos de recursos](/windows/desktop/menurc/about-resource-files).</span><span class="sxs-lookup"><span data-stu-id="3eb17-126">For more information, see [About Resource Files](/windows/desktop/menurc/about-resource-files).</span></span>

## <a name="defining-an-accelerator-table"></a><span data-ttu-id="3eb17-127">Definir una tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="3eb17-127">Defining an Accelerator Table</span></span>

<span data-ttu-id="3eb17-128">Una tabla de aceleradores es una tabla de métodos abreviados de teclado.</span><span class="sxs-lookup"><span data-stu-id="3eb17-128">An accelerator table is a table of keyboard shortcuts.</span></span> <span data-ttu-id="3eb17-129">Cada acceso directo se define mediante:</span><span class="sxs-lookup"><span data-stu-id="3eb17-129">Each shortcut is defined by:</span></span>

-   <span data-ttu-id="3eb17-130">Identificador numérico.</span><span class="sxs-lookup"><span data-stu-id="3eb17-130">A numeric identifier.</span></span> <span data-ttu-id="3eb17-131">Este número identifica el comando de aplicación que se invocará mediante el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="3eb17-131">This number identifies the application command that will be invoked by the shortcut.</span></span>
-   <span data-ttu-id="3eb17-132">Carácter ASCII o código de tecla virtual del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="3eb17-132">The ASCII character or virtual-key code of the shortcut.</span></span>
-   <span data-ttu-id="3eb17-133">Teclas modificadoras opcionales: ALT, Mayús o CTRL.</span><span class="sxs-lookup"><span data-stu-id="3eb17-133">Optional modifier keys: ALT, SHIFT, or CTRL.</span></span>

<span data-ttu-id="3eb17-134">La tabla de aceleradores tiene un identificador numérico, que identifica la tabla en la lista de recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3eb17-134">The accelerator table itself has a numeric identifier, which identifies the table in the list of application resources.</span></span> <span data-ttu-id="3eb17-135">Vamos a crear una tabla de aceleradores para un programa de dibujo sencillo.</span><span class="sxs-lookup"><span data-stu-id="3eb17-135">Let's create an accelerator table for a simple drawing program.</span></span> <span data-ttu-id="3eb17-136">Este programa tendrá dos modos: modo de dibujo y modo de selección.</span><span class="sxs-lookup"><span data-stu-id="3eb17-136">This program will have two modes, draw mode and selection mode.</span></span> <span data-ttu-id="3eb17-137">En el modo Draw, el usuario puede dibujar formas.</span><span class="sxs-lookup"><span data-stu-id="3eb17-137">In draw mode, the user can draw shapes.</span></span> <span data-ttu-id="3eb17-138">En el modo de selección, el usuario puede seleccionar formas.</span><span class="sxs-lookup"><span data-stu-id="3eb17-138">In selection mode, the user can select shapes.</span></span> <span data-ttu-id="3eb17-139">Para este programa, nos gustaría definir los siguientes métodos abreviados de teclado.</span><span class="sxs-lookup"><span data-stu-id="3eb17-139">For this program, we would like to define the following keyboard shortcuts.</span></span>



| <span data-ttu-id="3eb17-140">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="3eb17-140">Shortcut</span></span> | <span data-ttu-id="3eb17-141">Get-Help</span><span class="sxs-lookup"><span data-stu-id="3eb17-141">Command</span></span>                   |
|----------|---------------------------|
| <span data-ttu-id="3eb17-142">CTRL+M</span><span class="sxs-lookup"><span data-stu-id="3eb17-142">CTRL+M</span></span>   | <span data-ttu-id="3eb17-143">Alterna entre los modos.</span><span class="sxs-lookup"><span data-stu-id="3eb17-143">Toggle between modes.</span></span>     |
| <span data-ttu-id="3eb17-144">F1</span><span class="sxs-lookup"><span data-stu-id="3eb17-144">F1</span></span>       | <span data-ttu-id="3eb17-145">Cambiar al modo de dibujo.</span><span class="sxs-lookup"><span data-stu-id="3eb17-145">Switch to draw mode.</span></span>      |
| <span data-ttu-id="3eb17-146">F2</span><span class="sxs-lookup"><span data-stu-id="3eb17-146">F2</span></span>       | <span data-ttu-id="3eb17-147">Cambiar al modo de selección.</span><span class="sxs-lookup"><span data-stu-id="3eb17-147">Switch to selection mode.</span></span> |



 

<span data-ttu-id="3eb17-148">En primer lugar, defina los identificadores numéricos para la tabla y los comandos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3eb17-148">First, define numeric identifiers for the table and for the application commands.</span></span> <span data-ttu-id="3eb17-149">Estos valores son arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="3eb17-149">These values are arbitrary.</span></span> <span data-ttu-id="3eb17-150">Puede asignar constantes simbólicas para los identificadores al definirlas en un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="3eb17-150">You can assign symbolic constants for the identifiers by defining them in a header file.</span></span> <span data-ttu-id="3eb17-151">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3eb17-151">For example:</span></span>


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



<span data-ttu-id="3eb17-152">En este ejemplo, el valor `IDR_ACCEL1` identifica la tabla de aceleradores y las tres constantes siguientes definen los comandos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3eb17-152">In this example, the value `IDR_ACCEL1` identifies the accelerator table, and the next three constants define the application commands.</span></span> <span data-ttu-id="3eb17-153">Por Convención, un archivo de encabezado que define las constantes de recursos se denomina a menudo Resource. h.</span><span class="sxs-lookup"><span data-stu-id="3eb17-153">By convention, a header file that defines resource constants is often named resource.h.</span></span> <span data-ttu-id="3eb17-154">La siguiente lista muestra el archivo de definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="3eb17-154">The next listing shows the resource definition file.</span></span>


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



<span data-ttu-id="3eb17-155">Los métodos abreviados de acelerador se definen dentro de las llaves.</span><span class="sxs-lookup"><span data-stu-id="3eb17-155">The accelerator shortcuts are defined within the curly braces.</span></span> <span data-ttu-id="3eb17-156">Cada acceso directo contiene las siguientes entradas.</span><span class="sxs-lookup"><span data-stu-id="3eb17-156">Each shortcut contains the following entries.</span></span>

-   <span data-ttu-id="3eb17-157">Código de tecla virtual o carácter ASCII que invoca el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="3eb17-157">The virtual-key code or ASCII character that invokes the shortcut.</span></span>
-   <span data-ttu-id="3eb17-158">El comando de aplicación.</span><span class="sxs-lookup"><span data-stu-id="3eb17-158">The application command.</span></span> <span data-ttu-id="3eb17-159">Observe que se utilizan constantes simbólicas en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3eb17-159">Notice that symbolic constants are used in the example.</span></span> <span data-ttu-id="3eb17-160">El archivo de definición de recursos incluye Resource. h, donde se definen estas constantes.</span><span class="sxs-lookup"><span data-stu-id="3eb17-160">The resource definition file includes resource.h, where these constants are defined.</span></span>
-   <span data-ttu-id="3eb17-161">La palabra clave **VIRTKEY** significa que la primera entrada es un código de clave virtual.</span><span class="sxs-lookup"><span data-stu-id="3eb17-161">The keyword **VIRTKEY** means the first entry is a virtual-key code.</span></span> <span data-ttu-id="3eb17-162">La otra opción es usar caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="3eb17-162">The other option is to use ASCII characters.</span></span>
-   <span data-ttu-id="3eb17-163">Modificadores opcionales: ALT, CONTROL o SHIFT.</span><span class="sxs-lookup"><span data-stu-id="3eb17-163">Optional modifiers: ALT, CONTROL, or SHIFT.</span></span>

<span data-ttu-id="3eb17-164">Si usa caracteres ASCII para los accesos directos, un carácter en minúsculas será un método abreviado diferente que un carácter en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="3eb17-164">If you use ASCII characters for shortcuts, then a lowercase character will be a different shortcut than an uppercase character.</span></span> <span data-ttu-id="3eb17-165">(Por ejemplo, escribir ' a ' puede invocar un comando diferente que escribir ' A '). Esto puede confundir a los usuarios, por lo que suele ser mejor usar códigos de tecla virtual, en lugar de caracteres ASCII, para los accesos directos.</span><span class="sxs-lookup"><span data-stu-id="3eb17-165">(For example, typing 'a' might invoke a different command than typing 'A'.) That might confuse users, so it is generally better to use virtual-key codes, rather than ASCII characters, for shortcuts.</span></span>

## <a name="loading-the-accelerator-table"></a><span data-ttu-id="3eb17-166">Cargar la tabla de aceleradores</span><span class="sxs-lookup"><span data-stu-id="3eb17-166">Loading the Accelerator Table</span></span>

<span data-ttu-id="3eb17-167">El recurso de la tabla de aceleradores debe cargarse antes de que el programa pueda usarlo.</span><span class="sxs-lookup"><span data-stu-id="3eb17-167">The resource for the accelerator table must be loaded before the program can use it.</span></span> <span data-ttu-id="3eb17-168">Para cargar una tabla de aceleradores, llame a la función [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) .</span><span class="sxs-lookup"><span data-stu-id="3eb17-168">To load an accelerator table, call the [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) function.</span></span>


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



<span data-ttu-id="3eb17-169">Llame a esta función antes de escribir el bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3eb17-169">Call this function before you enter the message loop.</span></span> <span data-ttu-id="3eb17-170">El primer parámetro es el identificador del módulo.</span><span class="sxs-lookup"><span data-stu-id="3eb17-170">The first parameter is the handle to the module.</span></span> <span data-ttu-id="3eb17-171">(Este parámetro se pasa a la función [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="3eb17-171">(This parameter is passed to your [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="3eb17-172">Para obtener más información, vea [WinMain: el punto de entrada de la aplicación](winmain--the-application-entry-point.md)). El segundo parámetro es el identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="3eb17-172">For details, see [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).) The second parameter is the resource identifier.</span></span> <span data-ttu-id="3eb17-173">La función devuelve un identificador al recurso.</span><span class="sxs-lookup"><span data-stu-id="3eb17-173">The function returns a handle to the resource.</span></span> <span data-ttu-id="3eb17-174">Recuerde que un identificador es un tipo opaco que hace referencia a un objeto administrado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="3eb17-174">Recall that a handle is an opaque type that refers to an object managed by the system.</span></span> <span data-ttu-id="3eb17-175">Si se produce un error en la función, devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="3eb17-175">If the function fails, it returns **NULL**.</span></span>

<span data-ttu-id="3eb17-176">Puede liberar una tabla de aceleradores llamando a [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span><span class="sxs-lookup"><span data-stu-id="3eb17-176">You can release an accelerator table by calling [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span></span> <span data-ttu-id="3eb17-177">Sin embargo, el sistema libera automáticamente la tabla cuando el programa finaliza, por lo que solo necesita llamar a esta función si está reemplazando una tabla por otra.</span><span class="sxs-lookup"><span data-stu-id="3eb17-177">However, the system automatically releases the table when the program exits, so you only need to call this function if you are replacing one table with another.</span></span> <span data-ttu-id="3eb17-178">Hay un ejemplo interesante de esto en el tema [creación de aceleradores editables](/windows/desktop/menurc/using-keyboard-accelerators)por el usuario.</span><span class="sxs-lookup"><span data-stu-id="3eb17-178">There is an interesting example of this in the topic [Creating User Editable Accelerators](/windows/desktop/menurc/using-keyboard-accelerators).</span></span>

## <a name="translating-key-strokes-into-commands"></a><span data-ttu-id="3eb17-179">Traducir los trazos de tecla en comandos</span><span class="sxs-lookup"><span data-stu-id="3eb17-179">Translating Key Strokes into Commands</span></span>

<span data-ttu-id="3eb17-180">Una tabla de aceleradores funciona traduciendo los trazos clave en mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="3eb17-180">An accelerator table works by translating key strokes into [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="3eb17-181">El parámetro *wParam* del **\_ comando WM** contiene el identificador numérico del comando.</span><span class="sxs-lookup"><span data-stu-id="3eb17-181">The *wParam* parameter of **WM\_COMMAND** contains the numeric identifier of the command.</span></span> <span data-ttu-id="3eb17-182">Por ejemplo, con la tabla mostrada anteriormente, el trazo de tecla CTRL + M se convierte en un mensaje de **\_ comando de WM** con el valor `ID_TOGGLE_MODE` .</span><span class="sxs-lookup"><span data-stu-id="3eb17-182">For example, using the table shown previously, the key stroke CTRL+M is translated into a **WM\_COMMAND** message with the value `ID_TOGGLE_MODE`.</span></span> <span data-ttu-id="3eb17-183">Para que esto suceda, cambie el bucle de mensajes a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3eb17-183">To make this happen, change your message loop to the following:</span></span>


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



<span data-ttu-id="3eb17-184">Este código agrega una llamada a la función [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) dentro del bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3eb17-184">This code adds a call to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function inside the message loop.</span></span> <span data-ttu-id="3eb17-185">La función **TranslateAccelerator** examina cada mensaje de ventana, buscando mensajes de tecla presionada.</span><span class="sxs-lookup"><span data-stu-id="3eb17-185">The **TranslateAccelerator** function examines each window message, looking for key-down messages.</span></span> <span data-ttu-id="3eb17-186">Si el usuario presiona una de las combinaciones de teclas enumeradas en la tabla de aceleradores, **TranslateAccelerator** envía un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="3eb17-186">If the user presses one of the key combinations listed in the accelerator table, **TranslateAccelerator** sends a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message to the window.</span></span> <span data-ttu-id="3eb17-187">La función envía **un \_ comando de WM** mediante la invocación directa del procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="3eb17-187">The function sends **WM\_COMMAND** by directly invoking the window procedure.</span></span> <span data-ttu-id="3eb17-188">Cuando **TranslateAccelerator** traduce correctamente un trazo de clave, la función devuelve un valor distinto de cero, lo que significa que debe omitir el procesamiento normal del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3eb17-188">When **TranslateAccelerator** successfully translates a key stroke, the function returns a non-zero value, which means you should skip the normal processing for the message.</span></span> <span data-ttu-id="3eb17-189">De lo contrario, **TranslateAccelerator** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="3eb17-189">Otherwise, **TranslateAccelerator** returns zero.</span></span> <span data-ttu-id="3eb17-190">En ese caso, pase el mensaje de ventana a [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) y [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), como es habitual.</span><span class="sxs-lookup"><span data-stu-id="3eb17-190">In that case, pass the window message to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), as normal.</span></span>

<span data-ttu-id="3eb17-191">Este es el modo en que el programa de dibujo podría controlar el mensaje del [**\_ comando de WM**](/windows/desktop/menurc/wm-command) :</span><span class="sxs-lookup"><span data-stu-id="3eb17-191">Here is how the drawing program might handle the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message:</span></span>


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



<span data-ttu-id="3eb17-192">En este código se supone que `SetMode` es una función definida por la aplicación para cambiar entre los dos modos.</span><span class="sxs-lookup"><span data-stu-id="3eb17-192">This code assumes that `SetMode` is a function defined by the application to switch between the two modes.</span></span> <span data-ttu-id="3eb17-193">Los detalles de cómo controlar cada comando obviamente dependen de su programa.</span><span class="sxs-lookup"><span data-stu-id="3eb17-193">The details of how you would handle each command obviously depend on your program.</span></span>

## <a name="next"></a><span data-ttu-id="3eb17-194">Siguientes</span><span class="sxs-lookup"><span data-stu-id="3eb17-194">Next</span></span>

[<span data-ttu-id="3eb17-195">Establecer la imagen del cursor</span><span class="sxs-lookup"><span data-stu-id="3eb17-195">Setting the Cursor Image</span></span>](setting-the-cursor-image.md)

 

 