---
title: Cómo procesar notificaciones de selector de fecha y hora
description: En esta sección se muestra cómo procesar las notificaciones del selector de fecha y hora.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa1214ebd671b4ae222990bde4b44586e6d7b11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167653"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a>Cómo procesar notificaciones de selector de fecha y hora

En esta sección se muestra cómo procesar las notificaciones del selector de fecha y hora.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instrucciones


Un control selector de fecha y hora (DTP) envía mensajes de notificación a la ventana primaria cuando se producen eventos, normalmente desencadenados por la entrada del usuario, en el control . La aplicación debe incluir código para determinar el tipo de mensaje de notificación y responder correctamente.

Si tiene previsto usar campos de devolución de llamada con los controles DTP de la aplicación, debe estar preparado para controlar los códigos de [notificación DTN \_ FORMATQUERY,](dtn-formatquery.md) [DTN \_ FORMAT](dtn-format.md)y [ \_ DTN WMKEYDOWN.](dtn-wmkeydown.md) Para obtener información adicional sobre los campos de devolución de llamada, vea [Campos de devolución de llamada](date-and-time-picker-controls.md).

El siguiente ejemplo de código de C++ identifica el mensaje de notificación enviado por un control DTP y llama a la función adecuada definida por la aplicación. Consulte los temas siguientes para obtener ejemplos de código que ilustran cómo procesar las notificaciones que aparecen en este ejemplo.

|   Temas                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [Cómo procesar la notificación \_ DATETIMECHANGE de DTN](process-the-dtn-datetimechange-notification.md) |
| [Cómo procesar la notificación FORMATQUERY de DTN \_](process-the-dtn-formatquery-notification.md)       |
| [Cómo procesar la notificación DTN \_ FORMAT](process-the-dtn-format-notfication.md)                  |
| [Cómo procesar la notificación \_ WMKEYDOWN de DTN](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Notificaciones del selector de fecha y hora](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[Referencia del control selector de fecha y hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Usar controles selectores de fecha y hora](using-date-and-time-picker.md)
</dt> <dt>

[Selector de fecha y hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




