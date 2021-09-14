---
title: Cómo crear un control de animación
description: En este tema se muestra cómo crear un control de animación.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ff190617996e42e6580b82311fb51f4248000
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061917"
---
# <a name="how-to-create-an-animation-control"></a>Cómo crear un control de animación

En este tema se muestra cómo crear un control de animación. El ejemplo de código de C++ que lo acompaña crea un control de animación en un cuadro de diálogo. Coloca el control de animación debajo de un control especificado y establece las dimensiones del control de animación en función de las dimensiones de un marco en el clip Audio-Video intercalado (AVI).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación
-   Archivos AVI

## <a name="instructions"></a>Instructions

### <a name="step-1-create-an-instance-of-the-animation-control"></a>Paso 1: Crear una instancia del control de animación.

Use la [**macro Animar \_ crear**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) para crear una instancia del control de animación.


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a>Paso 2: Colocar el control de animación.

Obtiene las coordenadas de pantalla del botón de control especificado.


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



Convierta las coordenadas de la esquina inferior izquierda en coordenadas de cliente.


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



Coloque el control de animación debajo del botón de control especificado.


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a>Paso 3: Abra el clip AVI.

Llame a la macro [**Animar \_ abrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) para abrir el clip AVI y mostrar el primer fotograma en el control de animación. Llame a **la función ShowWindow** para que el control de animación sea visible.


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a>Ejemplo completo


```C++
// CreateAnimationCtrl - creates an animation control, positions it 
//                       below the specified control in a dialog box, 
//                       and opens the AVI clip for the animation control. 
// Returns the handle to the animation control. 
// hwndDlg             - handle to the dialog box. 
// nIDCtl              - identifier of the control below which the animation control 
//                       is to be positioned. 
// 
// Constants 
//     IDC_ANIMATE - identifier of the animation control. 
//     CX_FRAME, CY_FRAME - width and height of the frames 
//     in the AVI clip. 

HWND CreateAnimationCtrl(HWND hwndDlg, int nIDCtl) 
{ 
    HWND hwndAnim = NULL;    
    
    // Create the animation control.
    // IDC_ANIMATE - identifier of the animation control. 
    // hwndDlg - handle to the dialog box.
    RECT rc;
    hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
        WS_BORDER | WS_CHILD, g_hinst); 

    // Get the screen coordinates of the specified control button.
    // nIDCtl - identifier of the control below which the animation control is to be positioned.
    GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 

    // Convert the coordinates of the lower-left corner to 
    // client coordinates.
    POINT pt;
    pt.x = rc.left; 
    pt.y = rc.bottom; 
    ScreenToClient(hwndDlg, &pt); 

    // Position the animation control below the Stop button.
    // CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
    SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
        CX_FRAME, CY_FRAME, 
        SWP_NOZORDER | SWP_DRAWFRAME);

    // Open the AVI clip, and show the animation control.
    Animate_Open(hwndAnim, "SEARCH.AVI"); 
    ShowWindow(hwndAnim, SW_SHOW); 

    return hwndAnim; 
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles de animación](animation-control-overview.md)
</dt> <dt>

[Referencia de controles de animación](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Usar controles de animación](using-animation-control.md)
</dt> <dt>

[Animación](animation-control-reference.md)
</dt> </dl>

 

 




