---
title: Cómo implementar la información sobre herramientas de globo
description: La información sobre herramientas de globos es similar a la información sobre herramientas estándar, pero se muestra en un globo 0034 de estilo animado \ 0034; con una tallo que apunta a la herramienta.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774203"
---
# <a name="how-to-implement-balloon-tooltips"></a>Cómo implementar la información sobre herramientas de globo

La información sobre herramientas de globo es similar a la información sobre herramientas estándar, pero se muestra en un "globo" de estilo animado con una tallo que apunta a la herramienta. La información sobre herramientas de globo puede ser de una o varias líneas. Se crean y se administran de forma muy similar a la información sobre herramientas estándar.

En la ilustración siguiente se muestra la posición predeterminada de la tallo y el rectángulo. Si la herramienta está demasiado cerca de la parte superior de la pantalla, la información sobre herramientas aparece debajo y a la derecha del rectángulo de la herramienta. Si la herramienta está demasiado cerca del lado derecho de la pantalla, se aplican principios similares, pero la información sobre herramientas aparece a la izquierda del rectángulo de la herramienta.

![captura de pantalla de un cuadro de diálogo; la información sobre herramientas de globo con una línea de texto aparece encima y a la derecha del destino.](images/tt-balloon.png)

Puede cambiar la posición predeterminada estableciendo la marca **ttf \_ CENTERTIP** en el miembro **UFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de la información sobre herramientas. En ese caso, el tallo normalmente apunta al centro del borde inferior del rectángulo de la herramienta y el rectángulo de texto se muestra directamente debajo de la herramienta. El tallo se adjunta al rectángulo de texto en el centro del borde superior. Si la herramienta está demasiado cerca de la parte inferior de la pantalla, el rectángulo de texto se centra encima de la herramienta y el tallo se adjunta al centro del borde inferior.

En la ilustración siguiente se muestra una información sobre herramientas que está centrada en la herramienta.

![captura de pantalla de un cuadro de diálogo; la información sobre herramientas de globo con una línea de texto aparece centrada debajo del destino](images/tt-ballooncenter.png)

Si desea especificar dónde están los puntos de tallo, establezca la marca de **\_ seguimiento ttf** en el miembro **uFlags** de la estructura ToolTip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . A continuación, especifique la coordenada mediante el envío de un mensaje [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) , con las coordenadas x e y en el valor *lParam* . Si también se establece **ttf \_ CENTERTIP** , el tallo sigue señalando a la posición especificada por el mensaje **TTM \_ TRACKPOSITION** .

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="implement-balloon-tooltips"></a>Implementar la información sobre herramientas de globo

En el ejemplo de código siguiente se muestra cómo implementar una información sobre herramientas de globo centrado mediante el estilo de control ToolTip **\_ Balloon** ToolTip.


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles ToolTip](using-tooltip-contro.md)
</dt> <dt>

[**Estilos de información sobre herramientas**](tooltip-styles.md)
</dt> </dl>

 

 




