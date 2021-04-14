---
title: Cómo crear un control de List-View
description: En este tema se muestra cómo crear un control de vista de lista. Para crear un control de vista de lista, use la función CreateWindow o CreateWindowEx y especifique la clase de ventana de ListView de WC \_ .
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050498b87aaf701249a06cfe2c3ad18afdc1d84
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488561"
---
# <a name="how-to-create-a-list-view-control"></a>Cómo crear un control de List-View

En este tema se muestra cómo crear un control de vista de lista. Para crear un control de vista de lista, use la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la clase de ventana de [**\_ ListView de WC**](common-control-window-classes.md) .

Un control de vista de lista también se puede crear como parte de una plantilla de cuadro de diálogo. Debe especificar el [**\_ control de vista de WC**](common-control-window-classes.md) como el nombre de clase. Para usar un control de vista de lista como parte de una plantilla de cuadro de diálogo, debe llamar a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) o [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) antes de crear una instancia del cuadro de diálogo.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


En primer lugar, registre la clase de ventana mediante una llamada a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) y especificando el bit de [**\_ \_ las clases de ListView de ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) en la estructura **InitCommonControlsEx** correspondiente. Esto garantiza que se cargue el archivo DLL de controles comunes. A continuación, use la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la clase de ventana de [**\_ ListView de WC**](common-control-window-classes.md) .

> [!Note]  
> De forma predeterminada, un control de vista de lista usa la fuente del título del icono. Sin embargo, puede utilizar un mensaje de [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) para especificar la fuente que se va a usar para el texto. Debe enviar este mensaje antes de insertar elementos. El control utiliza las dimensiones de la fuente especificada por el mensaje de **WM \_ SETFONT** para determinar el espaciado y el diseño. También puede personalizar la fuente para cada elemento. Para obtener más información, vea [dibujo personalizado](custom-draw.md).

 

En el siguiente ejemplo de código de C++ se crea un control de vista de lista en la vista de informe.


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




Normalmente, las aplicaciones de vista de lista permiten al usuario cambiar de una vista a otra.

En el siguiente ejemplo de código de C++ se cambia el estilo de ventana de la vista de lista, que a su vez cambia la vista.


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de vista de lista](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Acerca de los controles List-View](list-view-controls-overview.md)
</dt> <dt>

[Usar controles List-View](using-list-view-controls.md)
</dt> </dl>

 

 