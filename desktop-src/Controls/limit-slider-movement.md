---
title: Cómo limitar el movimiento del control deslizante
description: Tal y como se describe en acerca de los controles TrackBar, es posible establecer una parte del intervalo de la barra de control como un intervalo de selección. Un propósito de un intervalo de selección puede ser limitar el movimiento del control deslizante, haciendo que algunas partes de los límites del intervalo completo estén desactivadas.
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903255"
---
# <a name="how-to-limit-slider-movement"></a>Cómo limitar el movimiento del control deslizante

Tal y como se describe en [acerca de los controles TrackBar](trackbar-controls.md), es posible establecer una parte del intervalo de la barra de control como un intervalo de selección. Un propósito de un intervalo de selección puede ser limitar el movimiento del control deslizante, haciendo que algunas partes de los límites del intervalo completo estén desactivadas.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="limit-slider-movement"></a>Límite de movimiento del control deslizante

En el siguiente código de ejemplo se limita el movimiento del control deslizante restableciendo la posición del control deslizante cada vez que se mueve fuera del intervalo de selección.


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



## <a name="remarks"></a>Observaciones

Este fragmento de código formaría parte del procedimiento de ventana de un cuadro de diálogo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




