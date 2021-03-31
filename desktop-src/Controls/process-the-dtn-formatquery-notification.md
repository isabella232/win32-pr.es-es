---
title: Cómo procesar la notificación de DTN_FORMATQUERY
description: En este tema se muestra cómo procesar una notificación de consulta de formato enviada por el control de fecha y hora (DTP).
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e8de1e1a80d04f9a7f9e9d0cfcda198118e67c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995766"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a>Cómo procesar la notificación de DTN \_ FORMATQUERY

En este tema se muestra cómo procesar una notificación de consulta de formato enviada por el control de fecha y hora (DTP).

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Un control de DTP envía un código de notificación de [DTN \_ FORMATQUERY](dtn-formatquery.md) para solicitar información sobre el tamaño máximo posible de un campo de devolución de llamada en el control. La aplicación debe controlar este mensaje para asegurarse de que todos los campos se muestran correctamente.

El siguiente ejemplo de código C++ es una función definida por la aplicación que procesa el código de notificación de [DTN \_ FORMATQUERY](dtn-formatquery.md) calculando el ancho de la cadena más ancha posible para un campo de devolución de llamada determinado.

**Advertencia de seguridad:** El uso incorrecto de **lstrcmp** puede poner en peligro la seguridad de la aplicación. Por ejemplo, antes de llamar a **lstrcmp** en el ejemplo de código siguiente, debe asegurarse de que las dos cadenas terminan en NULL. Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.



```C++
//  DoFormatQuery processes DTN_FORMATQUERY messages to ensure that the
//  DTP control displays callback fields properly.
//

void WINAPI DoFormatQuery(
 HWND hwndDP, 
 LPNMDATETIMEFORMATQUERY lpDTFQuery)
{
    HDC hdc;
    HFONT hFont, hOrigFont;

    //  Prepare the device context for GetTextExtentPoint32 call.
    hdc = GetDC(hwndDP);

    hFont = (HFONT) SendMessage(hwndDP, WM_GETFONT, 0L, 0L); 

    if(!hFont)
        hFont = (HFONT)GetStockObject(DEFAULT_GUI_FONT);

    hOrigFont = (HFONT) SelectObject(hdc, hFont);

    // Check to see if this is the callback segment desired. If so,
    // use the longest text segment to determine the maximum 
    // width of the callback field, and then place the information into 
    // the NMDATETIMEFORMATQUERY structure.
    if(!lstrcmp(L"XX",lpDTFQuery->pszFormat))
        GetTextExtentPoint32 (hdc,
                          L"366",  // widest date string
                          3,
                          &lpDTFQuery->szMax);

    // Reset the font in the device context; then release the context.
    SelectObject(hdc,hOrigFont);
    ReleaseDC(hwndDP, hdc);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de selector de fecha y hora](using-date-and-time-picker.md)
</dt> <dt>

[Referencia de control de selector de fecha y hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selector de fecha y hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




