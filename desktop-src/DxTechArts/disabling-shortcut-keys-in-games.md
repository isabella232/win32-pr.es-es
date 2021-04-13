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
# <a name="disabling-shortcut-keys-in-games"></a>Deshabilitar teclas de método abreviado en juegos

En este artículo se describe cómo deshabilitar temporalmente los métodos abreviados de teclado en Microsoft Windows para evitar la interrupción del juego para juegos de pantalla completa. La tecla Mayús y la tecla CTRL se usan a menudo como botones activar o ejecutar en juegos. Si los usuarios presionan accidentalmente la tecla de Windows (que se encuentra cerca de estas teclas), pueden provocar que se salten repentinamente la aplicación, lo que deteriora la experiencia del juego. El uso de la tecla Mayús como botón de juego puede ejecutar accidentalmente el acceso directo de StickyKeys, que puede mostrar un cuadro de diálogo de advertencia. Para evitar estos problemas, debe deshabilitar estas claves cuando se ejecute en modo de pantalla completa y habilitar las claves de nuevo en sus controladores predeterminados cuando se ejecute en modo de ventana o salga de la aplicación.

En este artículo se describe cómo hacer lo siguiente:

-   [Deshabilitar la tecla Windows con un enlace de teclado](#disable-the-windows-key-with-a-keyboard-hook)
-   [Deshabilitar las teclas de método abreviado de accesibilidad](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a>Deshabilitar la tecla Windows con un enlace de teclado

Use un enlace de teclado de bajo nivel para filtrar la clave de Windows para que no se procese. El enlace de teclado de bajo nivel que se muestra en el ejemplo 1 permanece en vigor aunque un usuario minimice la ventana o cambie a otra aplicación. Esto significa que debe asegurarse de que la clave de Windows no está deshabilitada cuando se desactiva la aplicación. Para ello, el código del ejemplo 1 controla el mensaje de ACTIVATEAPP de WM \_ .

> [!Note]  
> Este método funciona en Windows 2000 y versiones posteriores de Windows. Este método también funciona con cuentas de usuario con privilegios mínimos (también conocidas como cuentas de usuario limitado).

 

DXUT usa este método y se muestra en el ejemplo de código siguiente.

**Ejemplo 1: Usar un enlace de teclado de bajo nivel para deshabilitar la tecla Windows**


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



## <a name="disable-the-accessibility-shortcut-keys"></a>Deshabilitar las teclas de método abreviado de accesibilidad

Windows incluye características de accesibilidad como StickyKeys, FilterKeys y ToggleKeys (vea [accesibilidad de Windows](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))). Cada una de ellas sirve para un propósito diferente; StickyKeys, por ejemplo, está diseñado para personas que tienen dificultades para mantener presionadas dos o más teclas simultáneamente. Cada una de estas características de accesibilidad también tiene un método abreviado de teclado que permite activar o desactivar la característica. Por ejemplo, el acceso directo de StickyKeys se desencadena presionando la tecla Mayús cinco veces. Si la tecla Mayús también se usa en el juego, el usuario podría desencadenar accidentalmente este acceso directo durante la reproducción del juego. Cuando se desencadena el acceso directo, Windows (de forma predeterminada) presenta una advertencia en un cuadro de diálogo, lo que haría que Windows minimizara un juego que se ejecuta en modo de pantalla completa. Por supuesto, esto puede tener un efecto drástico en la reproducción de juegos.

Las características de accesibilidad son necesarias para algunos clientes y no interfieren en los juegos de pantalla completa. por lo tanto, no debe cambiar la configuración de accesibilidad. Sin embargo, dado que los métodos abreviados para las características de accesibilidad pueden interrumpir la reproducción del juego si se desencadena accidentalmente, debe desactivar un acceso directo de accesibilidad solo si esa característica no está habilitada llamando a [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).

Un acceso directo de accesibilidad que está desactivado por [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) permanece desactivado incluso después de salir de la aplicación. Esto significa que debe restaurar la configuración antes de salir de la aplicación. Dado que es posible que la aplicación no pueda salir correctamente, debe escribir esta configuración en el almacenamiento persistente para que se puedan restaurar cuando se vuelva a ejecutar la aplicación. También puede usar un controlador de excepciones para restaurar esta configuración si se produce un bloqueo.

**Para desactivar estos métodos abreviados**

1.  Capture la configuración de accesibilidad actual antes de deshabilitarla.
2.  Deshabilite el acceso directo de accesibilidad cuando la aplicación pase al modo de pantalla completa si la característica de accesibilidad está desactivada.
3.  Restaure la configuración de accesibilidad cuando la aplicación pase a modo de ventana o se cierre.

Este método se utiliza en DXUT y se muestra en el ejemplo de código siguiente.

> [!Note]  
> Este método funciona cuando se ejecuta en una cuenta de usuario limitada.

 

**Ejemplo 2: Deshabilitar las teclas de método abreviado de accesibilidad**


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



 

 