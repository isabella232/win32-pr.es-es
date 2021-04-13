---
title: Deshabilitar teclas de método abreviado en juegos
description: En este artículo se describe cómo deshabilitar temporalmente los métodos abreviados de teclado en Microsoft Windows para evitar la interrupción del juego para juegos de pantalla completa.
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff426e0d728150cf5f6ac3cd8d46a711c9b4f8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487926"
---
# <a name="disabling-shortcut-keys-in-games"></a><span data-ttu-id="4da01-103">Deshabilitar teclas de método abreviado en juegos</span><span class="sxs-lookup"><span data-stu-id="4da01-103">Disabling Shortcut Keys in Games</span></span>

<span data-ttu-id="4da01-104">En este artículo se describe cómo deshabilitar temporalmente los métodos abreviados de teclado en Microsoft Windows para evitar la interrupción del juego para juegos de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="4da01-104">This articles describes how to temporarily disable keyboard shortcuts in Microsoft Windows to prevent disruption of game play for full screen games.</span></span> <span data-ttu-id="4da01-105">La tecla Mayús y la tecla CTRL se usan a menudo como botones activar o ejecutar en juegos.</span><span class="sxs-lookup"><span data-stu-id="4da01-105">The SHIFT key and the CTRL key are often used as fire or run buttons in games.</span></span> <span data-ttu-id="4da01-106">Si los usuarios presionan accidentalmente la tecla de Windows (que se encuentra cerca de estas teclas), pueden provocar que se salten repentinamente la aplicación, lo que deteriora la experiencia del juego.</span><span class="sxs-lookup"><span data-stu-id="4da01-106">If users accidentally press the Windows key (located near these keys), they can cause themselves to suddenly jump out of the application, which ruins the game experience.</span></span> <span data-ttu-id="4da01-107">El uso de la tecla Mayús como botón de juego puede ejecutar accidentalmente el acceso directo de StickyKeys, que puede mostrar un cuadro de diálogo de advertencia.</span><span class="sxs-lookup"><span data-stu-id="4da01-107">Simply using the SHIFT key as a game button can inadvertently execute the StickyKeys shortcut which may display a warning dialog.</span></span> <span data-ttu-id="4da01-108">Para evitar estos problemas, debe deshabilitar estas claves cuando se ejecute en modo de pantalla completa y habilitar las claves de nuevo en sus controladores predeterminados cuando se ejecute en modo de ventana o salga de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4da01-108">To avoid these issues, you should disable these keys when running in full-screen mode, and either enable the keys back to their default handlers when running in windowed mode or exit the application.</span></span>

<span data-ttu-id="4da01-109">En este artículo se describe cómo hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4da01-109">This article describes how to do the following:</span></span>

-   [<span data-ttu-id="4da01-110">Deshabilitar la tecla Windows con un enlace de teclado</span><span class="sxs-lookup"><span data-stu-id="4da01-110">Disable the Windows Key with a Keyboard Hook</span></span>](#disable-the-windows-key-with-a-keyboard-hook)
-   [<span data-ttu-id="4da01-111">Deshabilitar las teclas de método abreviado de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="4da01-111">Disable the Accessibility Shortcut Keys</span></span>](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a><span data-ttu-id="4da01-112">Deshabilitar la tecla Windows con un enlace de teclado</span><span class="sxs-lookup"><span data-stu-id="4da01-112">Disable the Windows Key with a Keyboard Hook</span></span>

<span data-ttu-id="4da01-113">Use un enlace de teclado de bajo nivel para filtrar la clave de Windows para que no se procese.</span><span class="sxs-lookup"><span data-stu-id="4da01-113">Use a low-level keyboard hook to filter out the Windows key from being processed.</span></span> <span data-ttu-id="4da01-114">El enlace de teclado de bajo nivel que se muestra en el ejemplo 1 permanece en vigor aunque un usuario minimice la ventana o cambie a otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="4da01-114">The low-level keyboard hook shown in Example 1 remains in effect even if a user minimizes the window or switches to another application.</span></span> <span data-ttu-id="4da01-115">Esto significa que debe asegurarse de que la clave de Windows no está deshabilitada cuando se desactiva la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4da01-115">This means that you must be careful to ensure that the Windows key is not disabled when the application is deactivated.</span></span> <span data-ttu-id="4da01-116">Para ello, el código del ejemplo 1 controla el mensaje de ACTIVATEAPP de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="4da01-116">The code in Example 1 does this by handling the WM\_ACTIVATEAPP message.</span></span>

> [!Note]  
> <span data-ttu-id="4da01-117">Este método funciona en Windows 2000 y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="4da01-117">This method works on Windows 2000 and later versions of Windows.</span></span> <span data-ttu-id="4da01-118">Este método también funciona con cuentas de usuario con privilegios mínimos (también conocidas como cuentas de usuario limitado).</span><span class="sxs-lookup"><span data-stu-id="4da01-118">This method also works with least-privileged user accounts (also known as limited-user accounts).</span></span>

 

<span data-ttu-id="4da01-119">DXUT usa este método y se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="4da01-119">This method is used by DXUT and is illustrated in the following code example.</span></span>

<span data-ttu-id="4da01-120">**Ejemplo 1: Usar un enlace de teclado de bajo nivel para deshabilitar la tecla Windows**</span><span class="sxs-lookup"><span data-stu-id="4da01-120">**Example 1. Using a low-level keyboard hook to disable the Windows key**</span></span>


```C++
HHOOK g_hKeyboardHook;
BOOL g_bFullscreen;
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Initialization
    g_hKeyboardHook = SetWindowsHookEx( WH_KEYBOARD_LL,  LowLevelKeyboardProc, GetModuleHandle(NULL), 0 );
 
    // 
    // main application code here
    // 
 
    // Cleanup before shutdown
    UnhookWindowsHookEx( g_hKeyboardHook );
}
 
 
LRESULT CALLBACK LowLevelKeyboardProc( int nCode, WPARAM wParam, LPARAM lParam )
{
    if (nCode < 0 || nCode != HC_ACTION )  // do not process message 
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam); 
 
    bool bEatKeystroke = false;
    KBDLLHOOKSTRUCT* p = (KBDLLHOOKSTRUCT*)lParam;
    switch (wParam) 
    {
        case WM_KEYDOWN:  
        case WM_KEYUP:    
        {
            bEatKeystroke = (g_bFullscreen && g_bWindowActive && ((p->vkCode == VK_LWIN) || (p->vkCode == VK_RWIN)));
            break;
        }
    }
 
    if( bEatKeystroke )
        return 1;
    else
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam );
}
 
 
LRESULT CALLBACK WndProc( HWND hWnd, UINT uMsg, WPARAM wParam, LPARAM lParam )
{
    switch( uMsg )
    {
       case WM_ACTIVATEAPP:
            // g_bWindowActive is used to control if the Windows key is filtered by the keyboard hook or not.
            if( wParam == TRUE )
                g_bWindowActive  = true;           
            else 
                g_bWindowActive  = false;           
            break;
    }
}
```



## <a name="disable-the-accessibility-shortcut-keys"></a><span data-ttu-id="4da01-121">Deshabilitar las teclas de método abreviado de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="4da01-121">Disable the Accessibility Shortcut Keys</span></span>

<span data-ttu-id="4da01-122">Windows incluye características de accesibilidad como StickyKeys, FilterKeys y ToggleKeys (vea [accesibilidad de Windows](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span><span class="sxs-lookup"><span data-stu-id="4da01-122">Windows includes accessibility features such as StickyKeys, FilterKeys, and ToggleKeys (see [Windows Accessibility](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span></span> <span data-ttu-id="4da01-123">Cada una de ellas sirve para un propósito diferente; StickyKeys, por ejemplo, está diseñado para personas que tienen dificultades para mantener presionadas dos o más teclas simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="4da01-123">Each of these serves a different purpose; StickyKeys for example, is designed for people who have difficulty holding down two or more keys simultaneously.</span></span> <span data-ttu-id="4da01-124">Cada una de estas características de accesibilidad también tiene un método abreviado de teclado que permite activar o desactivar la característica.</span><span class="sxs-lookup"><span data-stu-id="4da01-124">Each of these accessibility features also has a keyboard shortcut that allows the feature to be turned on or off.</span></span> <span data-ttu-id="4da01-125">Por ejemplo, el acceso directo de StickyKeys se desencadena presionando la tecla Mayús cinco veces.</span><span class="sxs-lookup"><span data-stu-id="4da01-125">For example, the StickyKeys shortcut is triggered by pressing the SHIFT key five times.</span></span> <span data-ttu-id="4da01-126">Si la tecla Mayús también se usa en el juego, el usuario podría desencadenar accidentalmente este acceso directo durante la reproducción del juego.</span><span class="sxs-lookup"><span data-stu-id="4da01-126">If the SHIFT key is also used in the game, the user could accidentally trigger this shortcut during game play.</span></span> <span data-ttu-id="4da01-127">Cuando se desencadena el acceso directo, Windows (de forma predeterminada) presenta una advertencia en un cuadro de diálogo, lo que haría que Windows minimizara un juego que se ejecuta en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="4da01-127">When the shortcut is triggered, Windows (by default) presents a warning in a dialog box, which would cause Windows to minimize a game running in full-screen mode.</span></span> <span data-ttu-id="4da01-128">Por supuesto, esto puede tener un efecto drástico en la reproducción de juegos.</span><span class="sxs-lookup"><span data-stu-id="4da01-128">This, of course, can have a drastic effect on game play.</span></span>

<span data-ttu-id="4da01-129">Las características de accesibilidad son necesarias para algunos clientes y no interfieren en los juegos de pantalla completa. por lo tanto, no debe cambiar la configuración de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="4da01-129">The accessibility features are required for some customers and do not themselves interfere with full-screen games; therefore, you should not change the accessibility settings.</span></span> <span data-ttu-id="4da01-130">Sin embargo, dado que los métodos abreviados para las características de accesibilidad pueden interrumpir la reproducción del juego si se desencadena accidentalmente, debe desactivar un acceso directo de accesibilidad solo si esa característica no está habilitada llamando a [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="4da01-130">However, because the shortcuts for accessibility features can disrupt game play if triggered accidentally, you should turn off an accessibility shortcut only when that feature is not enabled by calling [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span></span>

<span data-ttu-id="4da01-131">Un acceso directo de accesibilidad que está desactivado por [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) permanece desactivado incluso después de salir de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4da01-131">An accessibility shortcut that is turned off by [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) remains turned off even after the application has exited.</span></span> <span data-ttu-id="4da01-132">Esto significa que debe restaurar la configuración antes de salir de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4da01-132">This means that you must restore the settings before exiting the application.</span></span> <span data-ttu-id="4da01-133">Dado que es posible que la aplicación no pueda salir correctamente, debe escribir esta configuración en el almacenamiento persistente para que se puedan restaurar cuando se vuelva a ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4da01-133">Because it is possible for the application to fail to exit correctly, you should write these settings to persistent storage so that they can be restored when the application is run again.</span></span> <span data-ttu-id="4da01-134">También puede usar un controlador de excepciones para restaurar esta configuración si se produce un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="4da01-134">You could also use an exception handler to restore these settings if a crash occurs.</span></span>

<span data-ttu-id="4da01-135">**Para desactivar estos métodos abreviados**</span><span class="sxs-lookup"><span data-stu-id="4da01-135">**To turn off these shortcuts**</span></span>

1.  <span data-ttu-id="4da01-136">Capture la configuración de accesibilidad actual antes de deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="4da01-136">Capture the current accessibility settings before disabling them.</span></span>
2.  <span data-ttu-id="4da01-137">Deshabilite el acceso directo de accesibilidad cuando la aplicación pase al modo de pantalla completa si la característica de accesibilidad está desactivada.</span><span class="sxs-lookup"><span data-stu-id="4da01-137">Disable the accessibility shortcut when the application goes into full-screen mode if the accessibility feature is off.</span></span>
3.  <span data-ttu-id="4da01-138">Restaure la configuración de accesibilidad cuando la aplicación pase a modo de ventana o se cierre.</span><span class="sxs-lookup"><span data-stu-id="4da01-138">Restore the accessibility settings when the application goes into windowed mode or exits.</span></span>

<span data-ttu-id="4da01-139">Este método se utiliza en DXUT y se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="4da01-139">This method is used in DXUT, and is illustrated in the following code example.</span></span>

> [!Note]  
> <span data-ttu-id="4da01-140">Este método funciona cuando se ejecuta en una cuenta de usuario limitada.</span><span class="sxs-lookup"><span data-stu-id="4da01-140">This method works when running on a limited user account.</span></span>

 

<span data-ttu-id="4da01-141">**Ejemplo 2: Deshabilitar las teclas de método abreviado de accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="4da01-141">**Example 2. Disabling accessibility shortcut keys**</span></span>


```C++
STICKYKEYS g_StartupStickyKeys = {sizeof(STICKYKEYS), 0};
TOGGLEKEYS g_StartupToggleKeys = {sizeof(TOGGLEKEYS), 0};
FILTERKEYS g_StartupFilterKeys = {sizeof(FILTERKEYS), 0};    
 
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Save the current sticky/toggle/filter key settings so they can be restored them later
    SystemParametersInfo(SPI_GETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
    SystemParametersInfo(SPI_GETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
    SystemParametersInfo(SPI_GETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
 
    // Disable when full screen
    AllowAccessibilityShortcutKeys( true );
 
    // Restore back when going to windowed or shutting down
    AllowAccessibilityShortcutKeys( false );
}
 
 
void AllowAccessibilityShortcutKeys( bool bAllowKeys )
{
    if( bAllowKeys )
    {
        // Restore StickyKeys/etc to original state and enable Windows key      
        STICKYKEYS sk = g_StartupStickyKeys;
        TOGGLEKEYS tk = g_StartupToggleKeys;
        FILTERKEYS fk = g_StartupFilterKeys;
        
        SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
        SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
        SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
    }
    else
    {
        // Disable StickyKeys/etc shortcuts but if the accessibility feature is on, 
        // then leave the settings alone as its probably being usefully used
 
        STICKYKEYS skOff = g_StartupStickyKeys;
        if( (skOff.dwFlags & SKF_STICKYKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            skOff.dwFlags &= ~SKF_HOTKEYACTIVE;
            skOff.dwFlags &= ~SKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &skOff, 0);
        }
 
        TOGGLEKEYS tkOff = g_StartupToggleKeys;
        if( (tkOff.dwFlags & TKF_TOGGLEKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            tkOff.dwFlags &= ~TKF_HOTKEYACTIVE;
            tkOff.dwFlags &= ~TKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &tkOff, 0);
        }
 
        FILTERKEYS fkOff = g_StartupFilterKeys;
        if( (fkOff.dwFlags & FKF_FILTERKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            fkOff.dwFlags &= ~FKF_HOTKEYACTIVE;
            fkOff.dwFlags &= ~FKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &fkOff, 0);
        }
    }
}
```



 

 