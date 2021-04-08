---
title: Cómo crear controles SysLink
description: Los hipervínculos del control SysLink se implementan mediante el marcado de la cadena de inicialización del control o mediante el envío de un \_ mensaje SETITEM de LM.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa5c5ff3348f35f9c67cb34bea0cc495d403ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794140"
---
# <a name="how-to-create-syslink-controls"></a>Cómo crear controles SysLink

Los hipervínculos del control SysLink se implementan mediante el marcado de la cadena de inicialización del control o mediante el envío de un mensaje [**\_ SETITEM de LM**](lm-setitem.md) .

> [!Note]  
> Antes de crear los controles SysLink, debe llamar a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , especificando la \_ clase de vínculo ICC \_ .

 

Para crear un SysLink, llame a la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana de [**\_ vínculo de CT**](common-control-window-classes.md) . El parámetro *lpWindowName* que es común a estas funciones especifica un puntero a una cadena terminada en cero que contiene el texto marcado que se va a mostrar. Para los estilos de ventana concretos de los controles SysLink, consulte [estilos de control syslink](syslink-control-styles.md).

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="create-a-syslink-control"></a>Crear un control SysLink

En el código de ejemplo siguiente se crea un control SysLink que muestra dos hipervínculos. El primer hipervínculo es una dirección URL de Internet y el segundo es definido por la aplicación.


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a>Observaciones

Se supone que ya se ha llamado a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .

Al especificar el estilo de [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) , se asegura de que el usuario podrá seleccionar un vínculo con el tabulador y presionar la tecla entrar.

La versión 6 de ComCtl32.dll solo es compatible con Unicode. Por lo tanto, no se pueden crear versiones ANSI de controles SysLink, solo Unicode.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles SysLink](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 