---
title: Cómo crear una información sobre herramientas para un área rectangular
description: En el ejemplo siguiente se muestra cómo crear un control de información sobre herramientas estándar para todo el área de cliente de una ventana.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254570"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a>Cómo crear una información sobre herramientas para un área rectangular

En el ejemplo siguiente se muestra cómo crear un control de información sobre herramientas estándar para todo el área de cliente de una ventana.

En la ilustración siguiente se muestra la información sobre herramientas que se muestra cuando el puntero del mouse está dentro de la ventana de cliente de un cuadro de diálogo. El identificador del cuadro de diálogo se pasó a la función que se muestra en el ejemplo anterior.

![captura de pantalla de un cuadro de diálogo; el puntero del mouse está dentro de la ventana de cliente y hay una información sobre herramientas visible](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="create-a-tooltip-for-a-rectangular-area"></a>Crear una información sobre herramientas para un área rectangular

En el ejemplo siguiente se muestra cómo crear un control de información sobre herramientas estándar para todo el área de cliente de una ventana.


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de información sobre herramientas](using-tooltip-contro.md)
</dt> </dl>

 

 




