---
title: Cómo recuperar y establecer una clave de acceso
description: En este tema se muestra cómo recuperar o establecer la combinación de claves para un control de tecla de acceso remoto.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac5d0bab71fea11fe3d2aba23405f6d7ee7fb1ed8c78f2578f034ae9c84cad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079499"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a>Cómo recuperar y establecer una clave de acceso

En este tema se muestra cómo recuperar o establecer la combinación de claves para un control de tecla de acceso remoto. El [**mensaje \_ SETHOTKEY**](hkm-sethotkey.md) de HKM permite a una aplicación establecer la combinación de teclas de acceso rápido para un control de tecla de acceso rápido. Las aplicaciones usan [**el mensaje \_ GETHOTKEY**](hkm-gethotkey.md) de HKM para recuperar el código de clave virtual y las marcas modificadoras de la clave de acceso rápido elegida por el usuario.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Use el [**mensaje \_ GETHOTKEY**](hkm-gethotkey.md) de HKM para recuperar el código de clave virtual y las teclas modificadoras que describen una clave de acceso rápido elegida por el usuario. Use el [**mensaje \_ SETHOTKEY**](hkm-sethotkey.md) de HKM para establecer esos valores para una clave de acceso rápido.

En el siguiente ejemplo de código de C++, la función definida por la aplicación usa el mensaje [**\_ GETHOTKEY**](hkm-gethotkey.md) de HKM para recuperar una combinación de claves de un control de tecla de acceso rápido y, a continuación, usa el mensaje [**\_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) de WM para establecer una tecla de acceso rápido global. Tenga en cuenta que no puede establecer una tecla de acceso activa global para una ventana que tenga el estilo [**de ventana WS \_ CHILD.**](/windows/desktop/winmsg/window-styles)



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

[Referencia de control de clave rápida](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Acerca de los controles de tecla de acceso](hot-key-controls.md)
</dt> <dt>

[Uso de controles de tecla de acceso](using-hot-key-controls.md)
</dt> </dl>

 

 