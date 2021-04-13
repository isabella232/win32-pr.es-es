---
title: Controlar los protectores de pantalla
description: La API de Microsoft Win32 admite aplicaciones especiales denominadas protectores de pantalla.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- protectores de pantalla
- Panel de control, protectores de pantalla
- ScreenSaverConfigureDialog
- archivos de definición de módulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b7e0d0c177af2798b041fa12b4cc5793bf9be0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487671"
---
# <a name="handling-screen-savers"></a><span data-ttu-id="43813-107">Controlar los protectores de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-107">Handling Screen Savers</span></span>

<span data-ttu-id="43813-108">La API de Microsoft Win32 admite aplicaciones especiales denominadas *protectores de pantalla*.</span><span class="sxs-lookup"><span data-stu-id="43813-108">The Microsoft Win32 API supports special applications called *screen savers*.</span></span> <span data-ttu-id="43813-109">Los protectores de pantalla se inician cuando el mouse y el teclado están inactivos durante un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="43813-109">Screen savers start when the mouse and keyboard have been idle for a specified period of time.</span></span> <span data-ttu-id="43813-110">Se usan por estos dos motivos:</span><span class="sxs-lookup"><span data-stu-id="43813-110">They are used for these two reasons:</span></span>

-   <span data-ttu-id="43813-111">Para proteger una pantalla de la grabación de fósforo causada por imágenes estáticas.</span><span class="sxs-lookup"><span data-stu-id="43813-111">To protect a screen from phosphor burn caused by static images.</span></span>
-   <span data-ttu-id="43813-112">Para ocultar la información confidencial que queda en una pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-112">To conceal sensitive information left on a screen.</span></span>

<span data-ttu-id="43813-113">Este tema se divide en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="43813-113">This topic is divided into the following sections.</span></span>

-   [<span data-ttu-id="43813-114">Acerca de los protectores de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-114">About Screen Savers</span></span>](#about-screen-savers)
-   [<span data-ttu-id="43813-115">Usar las funciones del protector de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-115">Using the Screen Saver Functions</span></span>](#using-the-screen-saver-functions)
    -   [<span data-ttu-id="43813-116">Crear un protector de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-116">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
    -   [<span data-ttu-id="43813-117">Instalar nuevos protectores de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-117">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
    -   [<span data-ttu-id="43813-118">Agregar ayuda al cuadro de diálogo Configuración del protector de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-118">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a><span data-ttu-id="43813-119">Acerca de los protectores de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-119">About Screen Savers</span></span>

<span data-ttu-id="43813-120">La aplicación de escritorio del panel de control de Windows permite a los usuarios seleccionar en una lista de protectores de pantalla, especificar cuánto tiempo debe transcurrir antes de que se inicie el protector de pantalla, configurar protectores de pantalla y obtener una vista previa de los protectores de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-120">The Desktop application in the Windows Control Panel lets users select from a list of screen savers, specify how much time should elapse before the screen saver starts, configure screen savers, and preview screen savers.</span></span> <span data-ttu-id="43813-121">Los protectores de pantalla se cargan automáticamente cuando se inicia Windows o cuando un usuario activa el protector de pantalla a través del panel de control.</span><span class="sxs-lookup"><span data-stu-id="43813-121">Screen savers are loaded automatically when Windows starts or when a user activates the screen saver through the Control Panel.</span></span>

<span data-ttu-id="43813-122">Una vez que se elige un protector de pantalla, Windows supervisa las pulsaciones de teclas y los movimientos del mouse y, a continuación, inicia el protector de pantalla después de un período de inactividad.</span><span class="sxs-lookup"><span data-stu-id="43813-122">Once a screen saver is chosen, Windows monitors keystrokes and mouse movements and then starts the screen saver after a period of inactivity.</span></span> <span data-ttu-id="43813-123">Sin embargo, Windows no inicia el protector de pantalla si se cumple alguna de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="43813-123">However, Windows does not start the screen saver if any of the following conditions exist:</span></span>

-   <span data-ttu-id="43813-124">La aplicación activa no es una aplicación basada en Windows.</span><span class="sxs-lookup"><span data-stu-id="43813-124">The active application is not a Windows-based application.</span></span>
-   <span data-ttu-id="43813-125">Existe una ventana de aprendizaje basado en PC (CBT).</span><span class="sxs-lookup"><span data-stu-id="43813-125">A computer-based training (CBT) window is present.</span></span>
-   <span data-ttu-id="43813-126">La aplicación activa recibe el mensaje de [ \_ SYSCOMMAND de WM](../menurc/wm-syscommand.md) con el parámetro *wParam* establecido en el \_ valor SC SCREENSAVE, pero no pasa el mensaje a la función [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="43813-126">The active application receives the [WM\_SYSCOMMAND](../menurc/wm-syscommand.md) message with the *wParam* parameter set to the SC\_SCREENSAVE value, but it does not pass the message to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="43813-127">**Contexto de seguridad del protector de pantalla**</span><span class="sxs-lookup"><span data-stu-id="43813-127">**Security Context of the Screen Saver**</span></span>

<span data-ttu-id="43813-128">El contexto de seguridad del protector de pantalla depende de si un usuario ha iniciado sesión de forma interactiva.</span><span class="sxs-lookup"><span data-stu-id="43813-128">The security context of the screen saver is dependent on whether a user is interactively logged on.</span></span> <span data-ttu-id="43813-129">Si un usuario inicia sesión de forma interactiva cuando se invoca el protector de pantalla, el protector de pantalla se ejecuta en el contexto de seguridad del usuario interactivo.</span><span class="sxs-lookup"><span data-stu-id="43813-129">If a user is interactively logged on when the screen saver is invoked, the screen saver runs in the security context of the interactive user.</span></span> <span data-ttu-id="43813-130">Si ningún usuario ha iniciado sesión, el contexto de seguridad del protector de pantalla depende de la versión de Windows que se esté usando.</span><span class="sxs-lookup"><span data-stu-id="43813-130">If no user is logged on, the security context of the screen saver is dependent on the version of Windows being used.</span></span>

-   <span data-ttu-id="43813-131">Windows XP y Windows 2000: el protector de pantalla se ejecuta en el contexto de LocalSystem con cuentas restringidas.</span><span class="sxs-lookup"><span data-stu-id="43813-131">Windows XP and Windows 2000 - screen saver runs in the context of LocalSystem with accounts restricted.</span></span>
-   <span data-ttu-id="43813-132">Windows 2003-el protector de pantalla se ejecuta en el contexto de LocalService con todos los privilegios quitados y el grupo administradores está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="43813-132">Windows 2003 - screen saver runs in the context of LocalService with all privileges removed and administrators group disabled.</span></span>
-   <span data-ttu-id="43813-133">No se aplica a Windows NT4.</span><span class="sxs-lookup"><span data-stu-id="43813-133">Does not apply to Windows NT4.</span></span>

<span data-ttu-id="43813-134">El contexto de seguridad determina el nivel de las operaciones con privilegios que se pueden realizar desde un protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-134">The security context determines the level of privileged operations which can be done from a screen saver.</span></span>

<span data-ttu-id="43813-135">**Windows Vista y versiones posteriores:** Si la Directiva habilita la protección con contraseña, se inicia el protector de pantalla, independientemente de lo que hace una aplicación con la \_ notificación SC SCREENSAVE.</span><span class="sxs-lookup"><span data-stu-id="43813-135">**Windows Vista and later:** If password protection is enabled by policy, the screen saver is started regardless of what an application does with the SC\_SCREENSAVE notification.</span></span>

<span data-ttu-id="43813-136">Los protectores de pantalla contienen funciones exportadas, definiciones de recursos y declaraciones de variables específicas.</span><span class="sxs-lookup"><span data-stu-id="43813-136">Screen savers contain specific exported functions, resource definitions, and variable declarations.</span></span> <span data-ttu-id="43813-137">La biblioteca de protectores de pantalla contiene la función **principal** y otro código de inicio necesario para un protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-137">The screen saver library contains the **main** function and other startup code required for a screen saver.</span></span> <span data-ttu-id="43813-138">Cuando se inicia un protector de pantalla, el código de inicio de la biblioteca de protector de pantalla crea una ventana de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="43813-138">When a screen saver starts, the startup code in the screen saver library creates a full-screen window.</span></span> <span data-ttu-id="43813-139">La clase de ventana para esta ventana se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="43813-139">The window class for this window is declared as follows:</span></span>


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



<span data-ttu-id="43813-140">Para crear un protector de pantalla, la mayoría de los desarrolladores crean un módulo de código fuente que contiene tres funciones necesarias y los vincula con la biblioteca del protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-140">To create a screen saver, most developers create a source code module containing three required functions and link them with the screen saver library.</span></span> <span data-ttu-id="43813-141">Un módulo de protector de pantalla solo es responsable de la configuración y de proporcionar efectos visuales.</span><span class="sxs-lookup"><span data-stu-id="43813-141">A screen saver module is responsible only for configuring itself and for providing visual effects.</span></span>

<span data-ttu-id="43813-142">Una de las tres funciones requeridas en un módulo de protector de pantalla es [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span><span class="sxs-lookup"><span data-stu-id="43813-142">One of the three required functions in a screen saver module is [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="43813-143">Esta función procesa mensajes específicos y pasa los mensajes no procesados de nuevo a la biblioteca del protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-143">This function processes specific messages and passes any unprocessed messages back to the screen saver library.</span></span> <span data-ttu-id="43813-144">A continuación se muestran algunos de los mensajes típicos procesados por **ScreenSaverProc**.</span><span class="sxs-lookup"><span data-stu-id="43813-144">Following are some of the typical messages processed by **ScreenSaverProc**.</span></span>



| <span data-ttu-id="43813-145">Mensaje</span><span class="sxs-lookup"><span data-stu-id="43813-145">Message</span></span>        | <span data-ttu-id="43813-146">Significado</span><span class="sxs-lookup"><span data-stu-id="43813-146">Meaning</span></span>                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43813-147">creación de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-147">WM\_CREATE</span></span>     | <span data-ttu-id="43813-148">Recupere los datos de inicialización del archivo de Regedit.ini.</span><span class="sxs-lookup"><span data-stu-id="43813-148">Retrieve any initialization data from the Regedit.ini file.</span></span> <span data-ttu-id="43813-149">Establezca un temporizador de ventana para la ventana del protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-149">Set a window timer for the screen saver window.</span></span> <span data-ttu-id="43813-150">Realice cualquier otra inicialización requerida.</span><span class="sxs-lookup"><span data-stu-id="43813-150">Perform any other required initialization.</span></span>                                     |
| <span data-ttu-id="43813-151">ERASEBKGND de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-151">WM\_ERASEBKGND</span></span> | <span data-ttu-id="43813-152">Borre la ventana del protector de pantalla y prepárese para las operaciones de dibujo posteriores.</span><span class="sxs-lookup"><span data-stu-id="43813-152">Erase the screen saver window and prepare for subsequent drawing operations.</span></span>                                                                                                               |
| <span data-ttu-id="43813-153">temporizador de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-153">WM\_TIMER</span></span>      | <span data-ttu-id="43813-154">Realizar operaciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="43813-154">Perform drawing operations.</span></span>                                                                                                                                                                |
| <span data-ttu-id="43813-155">destrucción de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-155">WM\_DESTROY</span></span>    | <span data-ttu-id="43813-156">Destruya los temporizadores creados cuando la aplicación haya procesado el mensaje de [ \_ creación de WM](../winmsg/wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="43813-156">Destroy the timers created when the application processed the [WM\_CREATE](../winmsg/wm-create.md) message.</span></span> <span data-ttu-id="43813-157">Realice cualquier limpieza adicional requerida.</span><span class="sxs-lookup"><span data-stu-id="43813-157">Perform any additional required cleanup.</span></span> |



 

<span data-ttu-id="43813-158">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) pasa los mensajes no procesados a la biblioteca del protector de pantalla mediante una llamada a la función [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) .</span><span class="sxs-lookup"><span data-stu-id="43813-158">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passes unprocessed messages to the screen saver library by calling the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="43813-159">En la tabla siguiente se describe cómo procesa esta función varios mensajes.</span><span class="sxs-lookup"><span data-stu-id="43813-159">The following table describes how this function processes various messages.</span></span>



| <span data-ttu-id="43813-160">Message</span><span class="sxs-lookup"><span data-stu-id="43813-160">Message</span></span>         | <span data-ttu-id="43813-161">Acción</span><span class="sxs-lookup"><span data-stu-id="43813-161">Action</span></span>                                                                    |
|-----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="43813-162">SETCURSOR de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-162">WM\_SETCURSOR</span></span>   | <span data-ttu-id="43813-163">Establezca el cursor en el cursor nulo y quítelo de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-163">Set the cursor to the null cursor, removing it from the screen.</span></span>           |
| <span data-ttu-id="43813-164">pintura de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-164">WM\_PAINT</span></span>       | <span data-ttu-id="43813-165">Pinte el fondo de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-165">Paint the screen background.</span></span>                                              |
| <span data-ttu-id="43813-166">LBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-166">WM\_LBUTTONDOWN</span></span> | <span data-ttu-id="43813-167">Finalice el protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-167">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="43813-168">MBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-168">WM\_MBUTTONDOWN</span></span> | <span data-ttu-id="43813-169">Finalice el protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-169">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="43813-170">RBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-170">WM\_RBUTTONDOWN</span></span> | <span data-ttu-id="43813-171">Finalice el protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-171">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="43813-172">KEYDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-172">WM\_KEYDOWN</span></span>     | <span data-ttu-id="43813-173">Finalice el protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-173">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="43813-174">MOUSEMOVE de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-174">WM\_MOUSEMOVE</span></span>   | <span data-ttu-id="43813-175">Finalice el protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-175">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="43813-176">activación de WM \_</span><span class="sxs-lookup"><span data-stu-id="43813-176">WM\_ACTIVATE</span></span>    | <span data-ttu-id="43813-177">Finalice el protector de pantalla si el parámetro *wParam* está establecido en **false**.</span><span class="sxs-lookup"><span data-stu-id="43813-177">Terminate the screen saver if the *wParam* parameter is set to **FALSE**.</span></span> |



 

<span data-ttu-id="43813-178">La segunda función necesaria en un módulo de protector de pantalla es [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span><span class="sxs-lookup"><span data-stu-id="43813-178">The second required function in a screen saver module is [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span></span> <span data-ttu-id="43813-179">Esta función muestra un cuadro de diálogo que permite al usuario configurar el protector de pantalla (una aplicación debe proporcionar una plantilla de cuadro de diálogo correspondiente).</span><span class="sxs-lookup"><span data-stu-id="43813-179">This function displays a dialog box that enables the user to configure the screen saver (an application must provide a corresponding dialog box template).</span></span> <span data-ttu-id="43813-180">Windows muestra el cuadro de diálogo Configuración cuando el usuario selecciona el botón **configurar** en el cuadro de diálogo protector de pantalla del panel de control.</span><span class="sxs-lookup"><span data-stu-id="43813-180">Windows displays the configuration dialog box when the user selects the **Setup** button in the Control Panel's Screen Saver dialog box.</span></span>

<span data-ttu-id="43813-181">La tercera función necesaria en un módulo de protector de pantalla es [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span><span class="sxs-lookup"><span data-stu-id="43813-181">The third required function in a screen saver module is [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span></span> <span data-ttu-id="43813-182">Todas las aplicaciones de protector de pantalla deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="43813-182">This function must be called by all screen saver applications.</span></span> <span data-ttu-id="43813-183">Sin embargo, las aplicaciones que no requieren controles personalizados o de Windows especiales en el cuadro de diálogo de configuración pueden devolver simplemente **true**.</span><span class="sxs-lookup"><span data-stu-id="43813-183">However, applications that do not require special windows or custom controls in the configuration dialog box can simply return **TRUE**.</span></span> <span data-ttu-id="43813-184">Las aplicaciones que requieren Windows o controles personalizados especiales deben usar esta función para registrar las clases de ventana correspondientes.</span><span class="sxs-lookup"><span data-stu-id="43813-184">Applications requiring special windows or custom controls should use this function to register the corresponding window classes.</span></span>

<span data-ttu-id="43813-185">Además de crear un módulo que admita las tres funciones que se acaban de describir, un protector de pantalla debe proporcionar un icono.</span><span class="sxs-lookup"><span data-stu-id="43813-185">In addition to creating a module that supports the three functions just described, a screen saver should supply an icon.</span></span> <span data-ttu-id="43813-186">Este icono solo está visible cuando el protector de pantalla se ejecuta como una aplicación independiente.</span><span class="sxs-lookup"><span data-stu-id="43813-186">This icon is visible only when the screen saver is run as a standalone application.</span></span> <span data-ttu-id="43813-187">(Para que lo ejecute el panel de control, un protector de pantalla debe tener la extensión de nombre de archivo. SCR; para ejecutarse como una aplicación independiente, debe tener la extensión de nombre de archivo. exe). El icono debe identificarse en el archivo de recursos del protector de pantalla por la aplicación de ID. de constante \_ , que se define en el archivo de encabezado Scrnsave. h.</span><span class="sxs-lookup"><span data-stu-id="43813-187">(To be run by the Control Panel, a screen saver must have the .scr file name extension; to be run as a standalone application, it must have the .exe file name extension.) The icon must be identified in the screen saver's resource file by the constant ID\_APP, which is defined in the Scrnsave.h header file.</span></span>

<span data-ttu-id="43813-188">Un requisito final es una cadena de Descripción del protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-188">One final requirement is a screen saver description string.</span></span> <span data-ttu-id="43813-189">El archivo de recursos de un protector de pantalla debe contener una cadena que el panel de control muestre como el nombre del protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-189">The resource file for a screen saver must contain a string that the Control Panel displays as the screen saver name.</span></span> <span data-ttu-id="43813-190">La cadena de descripción debe ser la primera cadena de la tabla de cadenas del archivo de recursos (identificada con el valor ordinal 1).</span><span class="sxs-lookup"><span data-stu-id="43813-190">The description string must be the first string in the resource file's string table (identified with the ordinal value 1).</span></span> <span data-ttu-id="43813-191">Sin embargo, el panel de control omite la cadena de descripción si el protector de pantalla tiene un nombre de archivo largo.</span><span class="sxs-lookup"><span data-stu-id="43813-191">However, the description string is ignored by the Control Panel if the screen saver has a long filename.</span></span> <span data-ttu-id="43813-192">En tal caso, el nombre de archivo se utilizará como la cadena de descripción.</span><span class="sxs-lookup"><span data-stu-id="43813-192">In such case, the filename will be used as the description string.</span></span>

## <a name="using-the-screen-saver-functions"></a><span data-ttu-id="43813-193">Usar las funciones del protector de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-193">Using the Screen Saver Functions</span></span>

<span data-ttu-id="43813-194">En esta sección se usa el código de ejemplo tomado de una aplicación de protector de pantalla para mostrar las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="43813-194">This section uses example code taken from a screen saver application to illustrate the following tasks:</span></span>

-   [<span data-ttu-id="43813-195">Crear un protector de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-195">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
-   [<span data-ttu-id="43813-196">Instalar nuevos protectores de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-196">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
-   [<span data-ttu-id="43813-197">Agregar ayuda al cuadro de diálogo Configuración del protector de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-197">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a><span data-ttu-id="43813-198">Crear un protector de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-198">Creating a Screen Saver</span></span>

<span data-ttu-id="43813-199">En intervalos que oscilan entre 1 y 10 segundos, la aplicación de este ejemplo vuelve a dibujar la pantalla con uno de cuatro colores: blanco, gris claro, gris oscuro y negro.</span><span class="sxs-lookup"><span data-stu-id="43813-199">At intervals ranging from 1 through 10 seconds, the application in this example repaints the screen with one of four colors: white, light gray, dark gray, and black.</span></span> <span data-ttu-id="43813-200">La aplicación pinta la pantalla cada vez que recibe un [mensaje \_ del temporizador de WM](../winmsg/wm-timer.md) .</span><span class="sxs-lookup"><span data-stu-id="43813-200">The application paints the screen each time it receives a [WM\_TIMER](../winmsg/wm-timer.md) message.</span></span> <span data-ttu-id="43813-201">El usuario puede ajustar el intervalo en el que se envía este mensaje seleccionando el cuadro de diálogo de configuración de la aplicación y ajustando una sola barra de desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="43813-201">The user can adjust the interval at which this message is sent by selecting the application's configuration dialog box and adjusting a single horizontal scroll bar.</span></span>

### <a name="screen-saver-library"></a><span data-ttu-id="43813-202">Biblioteca de protector de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-202">Screen saver library</span></span>

<span data-ttu-id="43813-203">Las funciones estáticas del protector de pantalla están contenidas en la biblioteca del protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-203">The static screen saver functions are contained in the screen saver library.</span></span> <span data-ttu-id="43813-204">Hay dos versiones de la biblioteca disponibles, Scrnsave. lib y Scrnsavw. lib.</span><span class="sxs-lookup"><span data-stu-id="43813-204">There are two versions of the library available, Scrnsave.lib and Scrnsavw.lib.</span></span> <span data-ttu-id="43813-205">Debe vincular el proyecto con uno de estos.</span><span class="sxs-lookup"><span data-stu-id="43813-205">You must link your project with one of these.</span></span> <span data-ttu-id="43813-206">Scrnsave. lib se utiliza para los protectores de pantalla que usan caracteres ANSI, y Scrnsavw. lib se usa para los protectores de pantalla que usan caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="43813-206">Scrnsave.lib is used for screen savers that use ANSI characters, and Scrnsavw.lib is used for screen savers that use Unicode characters.</span></span> <span data-ttu-id="43813-207">Un protector de pantalla que esté vinculado con Scrnsavw. lib solo se ejecutará en plataformas de Windows que admitan Unicode, mientras que un protector de pantalla vinculado con Scrnsave. lib se ejecutará en cualquier plataforma de Windows.</span><span class="sxs-lookup"><span data-stu-id="43813-207">A screen saver that is linked with Scrnsavw.lib will only run on Windows platforms that support Unicode, while a screen saver linked with Scrnsave.lib will run on any Windows platform.</span></span>

### <a name="supporting-the-configuration-dialog-box"></a><span data-ttu-id="43813-208">Compatibilidad con el cuadro de diálogo de configuración</span><span class="sxs-lookup"><span data-stu-id="43813-208">Supporting the configuration dialog box</span></span>

<span data-ttu-id="43813-209">La mayoría de los protectores de pantalla proporcionan un cuadro de diálogo de configuración para permitir que el usuario especifique datos de personalización, como colores únicos, velocidades de dibujo, grosor de línea, fuentes, etc.</span><span class="sxs-lookup"><span data-stu-id="43813-209">Most screen savers provide a configuration dialog box to let the user specify customization data such as unique colors, drawing speeds, line thickness, fonts, and so on.</span></span> <span data-ttu-id="43813-210">Para admitir el cuadro de diálogo de configuración, la aplicación debe proporcionar una plantilla de cuadro de diálogo y también debe admitir la función [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) .</span><span class="sxs-lookup"><span data-stu-id="43813-210">To support the configuration dialog box, the application must provide a dialog box template and must also support the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function.</span></span> <span data-ttu-id="43813-211">A continuación se muestra la plantilla de cuadro de diálogo para la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="43813-211">Following is the dialog box template for the sample application.</span></span>


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



<span data-ttu-id="43813-212">Debe definir la constante que se usa para identificar la plantilla de cuadro de diálogo mediante el valor decimal 2003, como en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="43813-212">You must define the constant used to identify the dialog box template by using the decimal value 2003, as in the following example:</span></span>


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



<span data-ttu-id="43813-213">En el ejemplo siguiente se muestra la función [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) que se encuentra en la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="43813-213">The following example shows the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function found in the sample application.</span></span>


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



<span data-ttu-id="43813-214">Además de proporcionar la plantilla de cuadro de diálogo y la compatibilidad con la función [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , una aplicación también debe admitir la función [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) .</span><span class="sxs-lookup"><span data-stu-id="43813-214">In addition to providing the dialog box template and supporting the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function, an application must also support the [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) function.</span></span> <span data-ttu-id="43813-215">Esta función registra las clases de ventana no estándar que requiere el protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="43813-215">This function registers any nonstandard window classes required by the screen saver.</span></span> <span data-ttu-id="43813-216">Dado que la aplicación de ejemplo solo usa clases de ventana estándar en el procedimiento del cuadro de diálogo, esta función simplemente devuelve **true**, como en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="43813-216">Because the sample application used only standard window classes in its dialog box procedure, this function simply returns **TRUE**, as in the following example:</span></span>


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a><span data-ttu-id="43813-217">Compatibilidad con el procedimiento de ventana protector de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-217">Supporting the screen saver window procedure</span></span>

<span data-ttu-id="43813-218">Cada protector de pantalla debe admitir un procedimiento de ventana denominado [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span><span class="sxs-lookup"><span data-stu-id="43813-218">Each screen saver must support a window procedure named [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="43813-219">Como la mayoría de los procedimientos de ventana, **ScreenSaverProc** procesa un conjunto de mensajes específicos y pasa los mensajes no procesados a un procedimiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="43813-219">Like most window procedures, **ScreenSaverProc** processes a set of specific messages and passes any unprocessed messages to a default procedure.</span></span> <span data-ttu-id="43813-220">Sin embargo, en lugar de pasarlos a la función [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) , **ScreenSaverProc** pasa los mensajes no procesados a la función [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) .</span><span class="sxs-lookup"><span data-stu-id="43813-220">However, instead of passing them to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function, **ScreenSaverProc** passes unprocessed messages to the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="43813-221">Otra diferencia entre **ScreenSaverProc** y un procedimiento de ventana normal es que el identificador pasado a **ScreenSaverProc** identifica todo el escritorio en lugar de una ventana de cliente.</span><span class="sxs-lookup"><span data-stu-id="43813-221">Another difference between **ScreenSaverProc** and a normal window procedure is that the handle passed to **ScreenSaverProc** identifies the entire desktop rather than a client window.</span></span> <span data-ttu-id="43813-222">En el ejemplo siguiente se muestra el procedimiento de ventana **ScreenSaverProc** para el protector de pantalla de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="43813-222">The following example shows the **ScreenSaverProc** window procedure for the sample screen saver.</span></span>


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a><span data-ttu-id="43813-223">Crear un archivo de definición de módulo</span><span class="sxs-lookup"><span data-stu-id="43813-223">Creating a module-definition file</span></span>

<span data-ttu-id="43813-224">Las funciones [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) y [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) se deben exportar en el archivo de definición de módulo de la aplicación; No obstante, no se debe exportar [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) .</span><span class="sxs-lookup"><span data-stu-id="43813-224">The [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) and [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) functions must be exported in the application's module-definition file; [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) should not be exported, however.</span></span> <span data-ttu-id="43813-225">En el ejemplo siguiente se muestra el archivo de definición de módulo para la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="43813-225">The following example shows the module-definition file for the sample application.</span></span>


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a><span data-ttu-id="43813-226">Instalar nuevos protectores de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-226">Installing New Screen Savers</span></span>

<span data-ttu-id="43813-227">Al compilar la lista de protectores de pantalla disponibles, el panel de control busca archivos con la extensión. SCR en el directorio de inicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="43813-227">When compiling the list of available screen savers, the Control Panel searches the Windows Startup directory for files with the .scr extension.</span></span> <span data-ttu-id="43813-228">Dado que los protectores de pantalla son archivos ejecutables estándar de Windows con extensiones. exe, debe cambiarles el nombre para que tengan extensiones. SCR y copiarlos en el directorio correcto.</span><span class="sxs-lookup"><span data-stu-id="43813-228">Because screen savers are standard Windows executable files with .exe extensions, you must rename them so they have .scr extensions and copy them to the correct directory.</span></span>

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a><span data-ttu-id="43813-229">Agregar ayuda al cuadro de diálogo Configuración del protector de pantalla</span><span class="sxs-lookup"><span data-stu-id="43813-229">Adding Help to the Screen Saver Configuration Dialog Box</span></span>

<span data-ttu-id="43813-230">El cuadro de diálogo de configuración de un protector de pantalla incluye normalmente un botón **ayuda** .</span><span class="sxs-lookup"><span data-stu-id="43813-230">The configuration dialog box for a screen saver typically includes a **Help** button.</span></span> <span data-ttu-id="43813-231">Las aplicaciones de protector de pantalla pueden buscar el identificador del botón ayuda y llamar a la función [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) de la misma forma que la ayuda se proporciona en otras aplicaciones basadas en Windows.</span><span class="sxs-lookup"><span data-stu-id="43813-231">Screen saver applications can check for the Help button identifier and call the [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) function in the same way Help is provided in other Windows-based applications.</span></span>

 

 