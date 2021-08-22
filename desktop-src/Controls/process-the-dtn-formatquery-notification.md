---
title: Procedimiento para procesar la notificación DTN_FORMATQUERY aplicación
description: En este tema se muestra cómo procesar una notificación de consulta de formato enviada por el control selector de fecha y hora (DTP).
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c148332c36711e68b7c3b773fdb47acef202c5fd2a67f5620319f06c7fbc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696945"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a>Cómo procesar la notificación FORMATQUERY de DTN \_

En este tema se muestra cómo procesar una notificación de consulta de formato enviada por el control selector de fecha y hora (DTP).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Un control DTP envía un código de [notificación \_ FORMATQUERY](dtn-formatquery.md) de DTN para solicitar información sobre el tamaño máximo posible de un campo de devolución de llamada dentro del control. La aplicación debe controlar este mensaje para asegurarse de que todos los campos se muestran correctamente.

El siguiente ejemplo de código de C++ es una función definida por la aplicación que procesa el código de notificación [ \_ FORMATQUERY](dtn-formatquery.md) de DTN calculando el ancho de la cadena más amplia posible para un campo de devolución de llamada determinado.

**Advertencia de seguridad:** El **uso incorrecto de lstrcmp** puede poner en peligro la seguridad de la aplicación. Por ejemplo, antes de llamar **a lstrcmp en** el ejemplo de código siguiente, debe asegurarse de que las dos cadenas finalizan en NULL. Debe revisar [Consideraciones de seguridad: Controles de Windows Microsoft](sec-comctls.md) antes de continuar.



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

[Usar controles selectores de fecha y hora](using-date-and-time-picker.md)
</dt> <dt>

[Referencia del control selector de fecha y hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selector de fecha y hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




