---
title: Cómo crear un control Animation
description: En este tema se muestra cómo crear un control de animación.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ff190617996e42e6580b82311fb51f4248000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075344"
---
# <a name="how-to-create-an-animation-control"></a>Cómo crear un control Animation

En este tema se muestra cómo crear un control de animación. El ejemplo de código de C++ que lo acompaña crea un control de animación en un cuadro de diálogo. Coloca el control Animation debajo de un control especificado y establece las dimensiones del control Animation basándose en las dimensiones de un marco en el Audio-Video clip intercalado (AVI).

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows
-   Archivos AVI

## <a name="instructions"></a>Instrucciones

### <a name="step-1-create-an-instance-of-the-animation-control"></a>Paso 1: crear una instancia del control Animation.

Utilice [**Animate \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro para crear una instancia del control Animation.


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a>Paso 2: colocar el control de animación.

Obtiene las coordenadas de pantalla del botón de control especificado.


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



Convierte las coordenadas de la esquina inferior izquierda en coordenadas de cliente.


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

Llame a la macro [**animada \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) para abrir el clip AVI y mostrar el primer fotograma en el control Animation. Llame a la función **ShowWindow** para que el control de animación sea visible.


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

[Referencia de control de animación](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Usar controles de animación](using-animation-control.md)
</dt> <dt>

[Animación](animation-control-reference.md)
</dt> </dl>

 

 




