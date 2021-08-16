---
title: Uso de La Windows
description: Al establecer otros controles como ventanas de acceso para una barra de seguimiento, puede colocar automáticamente esos controles en los extremos de la barra de seguimiento como etiquetas.
ms.assetid: 5797AA55-BD8D-407A-8896-08EE0DDC7E30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6819e0f37f07a90ae08a623f14c6c26d1d67f55ea81143834dfd10816f74396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829065"
---
# <a name="how-to-use-buddy-windows"></a>Uso de La Windows

Al establecer otros controles como ventanas de acceso para una barra de seguimiento, puede colocar automáticamente esos controles en los extremos de la barra de seguimiento como etiquetas.

En la ilustración siguiente se muestra una barra de seguimiento horizontal y vertical, ambas con controles estáticos como ventanas de trabajo.

![captura de pantalla que muestra un cuadro de diálogo con una barra de seguimiento horizontal y una barra de seguimiento vertical](images/tkb-buddy.png)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-buddy-windows"></a>Uso de La Windows

En el ejemplo de código siguiente se crean las ventanas de los compañeros que se muestran en la ilustración.


```
void LabelTrackbarsWithBuddies(HWND hDlg)
{
    HWND hwndTrackbar;
    HWND hwndBuddy;
    
    const int staticWidth   = 50;
    const int staticHeight  = 20;

//======================================================
// For horizontal Trackbar.

    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Left", SS_RIGHT | WS_CHILD | WS_VISIBLE, 
                                    0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                    
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);
    
    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Right", SS_LEFT | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
    
//======================================================    
// For vertical Trackbar.
    
    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER2);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Top", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);

    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Bottom", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
}
```



## <a name="remarks"></a>Comentarios

**IDC \_ SLIDER1** e **IDC \_ SLIDER2** son barras de seguimiento creadas en el editor de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Trackbar](using-trackbar-controls.md)
</dt> </dl>

 

 




