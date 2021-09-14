---
title: Cómo implementar información sobre herramientas de globos
description: La información sobre herramientas del globo es similar a la información sobre herramientas estándar, pero se muestra en un estilo de animación \ 0034;globo \ 0034; con una lemat que apunta a la herramienta.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061915"
---
# <a name="how-to-implement-balloon-tooltips"></a>Cómo implementar información sobre herramientas de globos

La información sobre herramientas del globo es similar a la información sobre herramientas estándar, pero se muestra en un "globo" de estilo de animación con una lematización que apunta a la herramienta. La información sobre herramientas del globo puede ser de una sola línea o de varias líneas. Se crean y controlan de la misma manera que la información sobre herramientas estándar.

La posición predeterminada de la lemat y el rectángulo se muestra en la ilustración siguiente. Si la herramienta está demasiado cerca de la parte superior de la pantalla, la información sobre herramientas aparece a continuación y a la derecha del rectángulo de la herramienta. Si la herramienta está demasiado cerca del lado derecho de la pantalla, se aplican principios similares, pero la información sobre herramientas aparece a la izquierda del rectángulo de la herramienta.

![captura de pantalla de un cuadro de diálogo; aparece una información sobre herramientas de globo con una línea de texto encima y a la derecha del destino.](images/tt-balloon.png)

Puede cambiar el posicionamiento predeterminado estableciendo la marca **TTF \_ CENTERTIP** en el **miembro uFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de información sobre herramientas. En ese caso, el lemat normalmente apunta al centro del borde inferior del rectángulo de la herramienta y el rectángulo de texto se muestra directamente debajo de la herramienta. La lemat se adjunta al rectángulo de texto en el centro del borde superior. Si la herramienta está demasiado cerca de la parte inferior de la pantalla, el rectángulo de texto se centra sobre la herramienta y la lemat se conecta al centro del borde inferior.

En la ilustración siguiente se muestra una información sobre herramientas centrada en la herramienta.

![captura de pantalla de un cuadro de diálogo; aparece una información sobre herramientas de globo con una línea de texto centrada debajo del destino](images/tt-ballooncenter.png)

Si desea especificar dónde apunta el lemat, establezca la marca **\_ TTF TRACK** en el **miembro uFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de información sobre herramientas. A continuación, especifique la coordenada mediante el envío de un mensaje [**\_ TRACKPOSITION de TTM,**](ttm-trackposition.md) con las coordenadas x e y en el *valor lParam.* Si **también se establece TTF \_ CENTERTIP,** la lemat sigue apuntando a la posición especificada por el **mensaje \_ TRACKPOSITION de TTM.**

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="implement-balloon-tooltips"></a>Implementación de información sobre herramientas de globo

En el código de ejemplo siguiente se muestra cómo implementar una información sobre herramientas de globo centrada mediante el estilo de control de información sobre herramientas **\_ TTS BALLOON.**


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

[Uso de controles de información sobre herramientas](using-tooltip-contro.md)
</dt> <dt>

[**Estilos de información sobre herramientas**](tooltip-styles.md)
</dt> </dl>

 

 




