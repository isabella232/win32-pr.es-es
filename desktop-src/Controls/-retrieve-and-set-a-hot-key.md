---
title: Cómo recuperar y establecer una tecla de acceso rápido
description: En este tema se muestra cómo recuperar o establecer la combinación de teclas de un control de tecla de acceso rápido.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105656443"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a>Cómo recuperar y establecer una tecla de acceso rápido

En este tema se muestra cómo recuperar o establecer la combinación de teclas de un control de tecla de acceso rápido. El mensaje [**HKM \_ SETHOTKEY**](hkm-sethotkey.md) permite a una aplicación establecer la combinación de teclas de acceso rápido para un control de tecla de acceso rápido. Las aplicaciones usan el mensaje [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) para recuperar el código de tecla virtual y los marcadores modificadores de la tecla de acceso rápido que el usuario elige.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Use el mensaje [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) para recuperar el código de tecla virtual y las teclas modificadoras que describen una tecla de acceso rápido elegida por el usuario. Use el [**mensaje \_ SETHOTKEY de HKM**](hkm-sethotkey.md) para establecer los valores de una tecla de acceso rápido.

En el siguiente ejemplo de código de C++, la función definida por la aplicación utiliza el mensaje [**\_ GETHOTKEY de HKM**](hkm-gethotkey.md) para recuperar una combinación de teclas de un control de tecla de acceso rápido y, a continuación, usa el mensaje de [**\_ SETHOTKEY de WM**](/windows/desktop/inputdev/wm-sethotkey) para establecer una tecla de acceso rápido global. Tenga en cuenta que no puede establecer una tecla de acceso rápido global para una ventana que tenga el estilo de ventana [**\_ secundaria de WS**](/windows/desktop/winmsg/window-styles) .



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de teclas de acceso rápido](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Acerca de los controles de tecla de acceso rápido](hot-key-controls.md)
</dt> <dt>

[Usar controles de tecla de acceso rápido](using-hot-key-controls.md)
</dt> </dl>

 

 