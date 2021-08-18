---
title: Deshabilitar teclas de método abreviado en juegos
description: En este artículo se describe cómo deshabilitar temporalmente los métodos abreviados de teclado en Microsoft Windows para evitar la interrupción del juego para juegos de pantalla completa.
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08eae2ee1b30e78b17440f2c6144c529de4e6d7b6272a5d497de5c5e631ac1c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070525"
---
# <a name="disabling-shortcut-keys-in-games"></a>Deshabilitar teclas de método abreviado en juegos

En este artículo se describe cómo deshabilitar temporalmente los métodos abreviados de teclado en Microsoft Windows para evitar la interrupción del juego para juegos de pantalla completa. La tecla MAYÚS y la tecla CTRL se suelen usar como botones de encendido o ejecución en juegos. Si los usuarios presionan accidentalmente la tecla Windows (ubicada cerca de estas teclas), pueden provocar que se salte repentinamente de la aplicación, lo que provoca la experiencia de juego. El simple uso de la tecla MAYÚS como botón de juego puede ejecutar accidentalmente el acceso directo StickyKeys, que puede mostrar un cuadro de diálogo de advertencia. Para evitar estos problemas, debe deshabilitar estas claves cuando se ejecuten en modo de pantalla completa y habilitar las claves de vuelta a sus controladores predeterminados cuando se ejecuten en modo de ventana o salir de la aplicación.

En este artículo se describe cómo hacer lo siguiente:

-   [Deshabilitar la Windows con un enlace de teclado](#disable-the-windows-key-with-a-keyboard-hook)
-   [Deshabilitar las teclas de método abreviado de accesibilidad](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a>Deshabilitar la Windows con un enlace de teclado

Use un enlace de teclado de bajo nivel para filtrar la Windows que se va a procesar. El enlace de teclado de bajo nivel que se muestra en el ejemplo 1 permanece en vigor incluso si un usuario minimiza la ventana o cambia a otra aplicación. Esto significa que debe tener cuidado de asegurarse de que la clave Windows está deshabilitada cuando se desactiva la aplicación. El código del ejemplo 1 lo hace controlando el mensaje \_ WM ACTIVATEAPP.

> [!Note]  
> Este método funciona en Windows 2000 y versiones posteriores de Windows. Este método también funciona con cuentas de usuario con privilegios mínimos (también conocidas como cuentas de usuario limitado).

 

DXUT usa este método y se muestra en el ejemplo de código siguiente.

**Ejemplo 1. Uso de un enlace de teclado de bajo nivel para deshabilitar Windows teclado**


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

Windows incluye características de accesibilidad como StickyKeys, FilterKeys y ToggleKeys (consulte [Windows Accessibility](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))). Cada uno de ellos tiene un propósito diferente; StickyKeys, por ejemplo, está diseñado para personas que tienen dificultades para mantener dos o más claves simultáneamente. Cada una de estas características de accesibilidad también tiene un método abreviado de teclado que permite que la característica esté activada o desactivada. Por ejemplo, el acceso directo StickyKeys se desencadena presionando la tecla MAYÚS cinco veces. Si también se usa la tecla MAYÚS en el juego, el usuario podría desencadenar accidentalmente este acceso directo durante el juego. Cuando se desencadena el acceso directo, Windows (de forma predeterminada) presenta una advertencia en un cuadro de diálogo, lo que haría que Windows minimizara un juego que se ejecuta en modo de pantalla completa. Esto, por supuesto, puede tener un efecto drástico en el juego.

Las características de accesibilidad son necesarias para algunos clientes y no interfieren con los juegos de pantalla completa. por lo tanto, no debe cambiar la configuración de accesibilidad. Sin embargo, dado que los accesos directos para las características de accesibilidad pueden interrumpir el juego si se desencadenan accidentalmente, debe desactivar un acceso directo de accesibilidad solo cuando esa característica no esté habilitada llamando a [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).

Un acceso directo de accesibilidad desactivado por [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) permanece desactivado incluso después de que se haya salido de la aplicación. Esto significa que debe restaurar la configuración antes de salir de la aplicación. Dado que es posible que la aplicación no se cierre correctamente, debe escribir esta configuración en el almacenamiento persistente para que se pueda restaurar cuando se vuelva a ejecutar la aplicación. También puede usar un controlador de excepciones para restaurar esta configuración si se produce un bloqueo.

**Para desactivar estos accesos directos**

1.  Capture la configuración de accesibilidad actual antes de deshabilitarla.
2.  Deshabilite el acceso directo de accesibilidad cuando la aplicación entre en modo de pantalla completa si la característica de accesibilidad está desactivada.
3.  Restaure la configuración de accesibilidad cuando la aplicación entre en modo de ventana o salga.

Este método se usa en DXUT y se muestra en el ejemplo de código siguiente.

> [!Note]  
> Este método funciona cuando se ejecuta en una cuenta de usuario limitada.

 

**Ejemplo 2. Deshabilitación de las teclas de método abreviado de accesibilidad**


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



 

 