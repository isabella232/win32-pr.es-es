---
title: Cómo crear controles SysLink
description: Los hipervínculos del control SysLink se implementan a través del marcado en la cadena de inicialización del control o mediante el envío de un mensaje \_ SETITEM de LM.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2b50e364a2701d52aa0ed62222b0901a66b6c4073891b7f9348fffc8997fdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878515"
---
# <a name="how-to-create-syslink-controls"></a>Cómo crear controles SysLink

Los hipervínculos del control SysLink se implementan a través del marcado en la cadena de inicialización del control o mediante el envío de un [**mensaje \_ SETITEM de LM.**](lm-setitem.md)

> [!Note]  
> Antes de crear controles SysLink, debe llamar a la [**función InitCommonControlsEx,**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) especificando LA CLASE LINK DE LA ORDEN DE ENLACE. \_ \_

 

Para crear un syslink, llame a [**las funciones CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la [**clase de ventana WC \_ LINK.**](common-control-window-classes.md) El *parámetro lpWindowName* común a estas funciones especifica un puntero a una cadena terminada en cero que contiene el texto marcado que se va a mostrar. Para obtener estilos de ventana específicos de los controles SysLink, vea [Estilos de control SysLink](syslink-control-styles.md).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="create-a-syslink-control"></a>Crear un control SysLink

El código de ejemplo siguiente crea un control SysLink que muestra dos hipervínculos. El primer hipervínculo es una dirección URL de Internet y el segundo está definido por la aplicación.


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



## <a name="remarks"></a>Comentarios

Se supone que ya se ha llamado a [**InitCommonControlsEx.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)

Al especificar el [**estilo \_ TABSTOP de WS,**](/windows/desktop/winmsg/window-styles) se garantiza que el usuario podrá seleccionar un vínculo con tabulación y presionar la tecla Entrar.

La versión 6 de ComCtl32.dll solo admite Unicode. Por lo tanto, no se pueden crear versiones ANSI de controles SysLink, solo Unicode.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de controles SysLink](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 