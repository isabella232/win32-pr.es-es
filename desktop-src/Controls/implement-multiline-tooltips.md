---
title: Cómo implementar información sobre herramientas multilínea
description: La información sobre herramientas multilínea permite mostrar texto en más de una línea.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0d9f4172b256d2e6b72fb59ace4dc377fa3a0061e3ee0e6c0f234a74aad06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085635"
---
# <a name="how-to-implement-multiline-tooltips"></a>Cómo implementar información sobre herramientas multilínea

La información sobre herramientas multilínea permite mostrar texto en más de una línea.

Son compatibles con la [versión 4.70](common-control-versions.md) y posteriores de los controles comunes. La aplicación crea una información sobre herramientas de varias líneas mediante el envío de un mensaje [**\_ SETMAXTIPWIDTH de TTM,**](ttm-setmaxtipwidth.md) especificando el ancho del rectángulo de presentación. El texto que supera este ancho se ajusta a la línea siguiente en lugar de ampliar la región de presentación. El alto del rectángulo aumenta según sea necesario para dar cabida a las líneas adicionales. El control de información sobre herramientas ajusta las líneas automáticamente, o puede usar una combinación de retorno de carro/avance de línea, r n, para forzar saltos de línea en \\ \\ ubicaciones concretas.

La pantalla resultante se muestra en la ilustración siguiente.

![captura de pantalla de un cuadro de diálogo con información sobre herramientas que contiene texto organizado como un párrafo de varias líneas](images/tt-multiline.png)

> [!Note]  
> El búfer de texto especificado por el **miembro szText** de la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) solo puede tener 80 caracteres. Si necesita usar una cadena más larga, apunte el miembro **lpszText** de **NMTTDISPINFO** a un búfer que contenga el texto deseado.

 

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="implement-multiline-tooltips"></a>Implementación de información sobre herramientas multilínea

El fragmento de código siguiente es un ejemplo de un controlador de [notificaciones \_ GETDISPINFO de TTN](ttn-getdispinfo.md) simple. Habilita una información sobre herramientas multilínea estableciendo el rectángulo de presentación en 150 píxeles. Se inserta un salto de línea manual después de la primera palabra para mostrar que los saltos de línea pueden ser duros y flexibles.


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de controles de información sobre herramientas](using-tooltip-contro.md)
</dt> </dl>

 

 




