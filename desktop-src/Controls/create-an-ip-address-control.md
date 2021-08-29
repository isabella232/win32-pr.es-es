---
title: Cómo crear un control de direcciones IP
description: En este tema se muestra cómo crear una instancia de un control de direcciones IP.
ms.assetid: E4DBECA6-B3F2-405F-8D95-32FA2334114D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308893b436760ad970025b93d49a368fa44b28c7913c433ff4febad105cc41b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063115"
---
# <a name="how-to-create-an-ip-address-control"></a>Cómo crear un control de direcciones IP

En este tema se muestra cómo crear una instancia de un control de direcciones IP.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Antes de crear un control de dirección IP, cargue el archivo DLL de controles comunes mediante una [**llamada a InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex). A continuación, use las funciones [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de dirección IP de instancia. El nombre de clase del control es [**WC \_ IPADDRESS**](common-control-window-classes.md). Use el [**estilo SECUNDARIO de WS, \_**](/windows/desktop/winmsg/window-styles) ya que no hay ninguna constante de estilo específica asociada al control de dirección IP.

En el siguiente ejemplo de código de C++, la función definida por la aplicación llama primero a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) y establece el **miembro dwICC** de la estructura [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) en [**CLASS \_ DE \_ INTERNET DE CLASS,**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)que especifica la clase de dirección IP. A continuación, [**llama a CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear una instancia del control de direcciones IP.


```C++
// CreateIPAdressFld - creates a IPAddress control.
// Returns the handle to the new control
// TO DO:  calling procedure needs to check whether the handle is NULL, in case 
// of an error in creation.
// int xcoord, ycoord the coordinates of location of the control in the parent window
// HINST hInst is the global handle to the application instance.
// HWND  hWndParent is the handle to the control's parent window. 
//
//
HWND CreateIPAddressFld (HWND hwndParent, int xcoord, int ycoord) 
{     
     
    INITCOMMONCONTROLSEX icex;
    
    // Ensure that the common control DLL is loaded. 
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC  = ICC_INTERNET_CLASSES ;
    InitCommonControlsEx(&icex); 
    
    // Create the IPAddress control.        
    HWND hWndIPAddressFld = CreateWindow(WC_IPADDRESS, 
                                L"", 
                                WS_CHILD | WS_OVERLAPPED | WS_VISIBLE, 
                                xcoord, 
                                ycoord,
                                150, 
                                20,  
                                hwndParent, 
                                NULL, 
                                hInst, 
                                NULL); 
                                
    return (hWndIPAddressFld);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de direcciones IP](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[Acerca de los controles de dirección IP](ip-address-controls.md)
</dt> <dt>

[Usar controles de dirección IP](using-ip-address-controls.md)
</dt> </dl>

 

 