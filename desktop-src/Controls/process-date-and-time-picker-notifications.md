---
title: Cómo procesar notificaciones de selector de fecha y hora
description: En esta sección se muestra cómo procesar las notificaciones de selector de fecha y hora.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b904c464677a81151b03e3ae89085847e4e8bdf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078635"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a>Cómo procesar notificaciones de selector de fecha y hora

En esta sección se muestra cómo procesar las notificaciones de selector de fecha y hora.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Un control de selector de fecha y hora (DTP) envía mensajes de notificación a la ventana primaria cuando los eventos, normalmente desencadenados por la entrada del usuario, se producen en el control. La aplicación debe incluir código para determinar el tipo de mensaje de notificación y responder de forma adecuada.

Si planea usar campos de devolución de llamada con los controles de DTP en la aplicación, debe estar preparado para controlar los códigos de notificación [DTN \_ FORMATQUERY](dtn-formatquery.md), [DTN \_ ](dtn-format.md)y [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) . Para obtener más información sobre los campos de devolución de llamada, vea [campos de devolución de llamada](date-and-time-picker-controls.md).

En el siguiente ejemplo de código de C++ se identifica el mensaje de notificación enviado por un control de DTP y se llama a la función definida por la aplicación adecuada. Consulte los siguientes temas para obtener ejemplos de código que muestran cómo procesar las notificaciones que aparecen en este ejemplo.

|                                                                                                        |
|--------------------------------------------------------------------------------------------------------|
| [Cómo procesar la notificación de \_ DATETIMECHANGE de DTN](process-the-dtn-datetimechange-notification.md) |
| [Cómo procesar la notificación de DTN \_ FORMATQUERY](process-the-dtn-formatquery-notification.md)       |
| [Cómo procesar la notificación de \_ formato DTN](process-the-dtn-format-notfication.md)                  |
| [Cómo procesar la notificación de \_ WMKEYDOWN de DTN](process-the-dtn-wmkeydown-notification.md)           |



 



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

[Notificaciones de selector de fecha y hora](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[Referencia de control de selector de fecha y hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Usar controles de selector de fecha y hora](using-date-and-time-picker.md)
</dt> <dt>

[Selector de fecha y hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




