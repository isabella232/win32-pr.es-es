---
title: Cómo limitar el movimiento del control deslizante
description: Como se describe en Acerca de los controles trackbar, es posible desactivar parte del intervalo de la barra de seguimiento como un intervalo de selección. Un propósito de un intervalo de selección podría ser limitar el movimiento del control deslizante, lo que hace que algunas partes del intervalo completo no se limiten.
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4faf4a88f95ec521330e9084eef66f29b2f5d872c1f6375020b1d4519cf64e25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085155"
---
# <a name="how-to-limit-slider-movement"></a>Cómo limitar el movimiento del control deslizante

Como se describe en [Acerca de los controles de](trackbar-controls.md)la barra de seguimiento , es posible desactivar parte del intervalo de la barra de seguimiento como un intervalo de selección. Un propósito de un intervalo de selección podría ser limitar el movimiento del control deslizante, lo que hace que algunas partes del intervalo completo no se limiten.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="limit-slider-movement"></a>Limitar movimiento del control deslizante

El código de ejemplo siguiente limita el movimiento del control deslizante mediante el restablecimiento de la posición del control deslizante cada vez que se mueve fuera del intervalo de selección.


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a>Comentarios

Este fragmento de código formaría parte del procedimiento de ventana de un cuadro de diálogo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles trackbar](using-trackbar-controls.md)
</dt> </dl>

 

 




