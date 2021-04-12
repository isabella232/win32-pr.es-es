---
title: Cómo crear un control de dirección IP
description: En este tema se muestra cómo crear una instancia de un control de dirección IP.
ms.assetid: E4DBECA6-B3F2-405F-8D95-32FA2334114D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8427a5695c0b9c79c19d328f4abc2ab0ffb2e5a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149738"
---
# <a name="how-to-create-an-ip-address-control"></a>Cómo crear un control de dirección IP

En este tema se muestra cómo crear una instancia de un control de dirección IP.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Antes de crear un control de dirección IP, cargue el archivo DLL de controles comunes llamando a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex). A continuación, use la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de dirección IP de instancia. El nombre de clase del control es [**WC \_ IPAddress**](common-control-window-classes.md). Use el [**estilo \_ secundario WS**](/windows/desktop/winmsg/window-styles) , ya que no hay ninguna constante de estilo específica asociada con el control de dirección IP.

En el siguiente ejemplo de código de C++, la función definida por la aplicación llama primero a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) y establece el miembro **dwICC** de la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) en [**\_ \_ las clases de Internet de ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), que especifica la clase de dirección IP. A continuación, llama a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear una instancia del control de dirección IP.


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

[Referencia de control de dirección IP](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[Acerca de los controles de dirección IP](ip-address-controls.md)
</dt> <dt>

[Usar controles de direcciones IP](using-ip-address-controls.md)
</dt> </dl>

 

 