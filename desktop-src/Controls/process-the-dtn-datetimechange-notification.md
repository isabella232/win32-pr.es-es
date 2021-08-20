---
title: Cómo procesar la notificación de DTN_DATETIMECHANGE aplicación
description: En este tema se muestra cómo procesar la notificación de los cambios realizados por el usuario en el control selector de fecha y hora (DTP).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9490059a202eff69a05b34a086e74d6df52758713fd5b66d899d1ab114a31040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829926"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a>Cómo procesar la notificación \_ DATETIMECHANGE de DTN

En este tema se muestra cómo procesar la notificación de los cambios realizados por el usuario en el control selector de fecha y hora (DTP).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Un control DTP envía el código [de notificación \_ DATETIMECHANGE de DTN](dtn-datetimechange.md) cada vez que se produce un cambio. Por ejemplo, esta notificación se generará cuando el usuario cambie uno de los campos del control o, en el caso de que el control esté establecido en el estilo [**\_ DTS SHOWNONE,**](date-and-time-picker-control-styles.md) cuando el usuario cambie el estado de la casilla del control.

La aplicación debe incluir código para procesar los mensajes \_ DATETIMECHANGE de DTN enviados por el control DTP.

El siguiente ejemplo de código de C++ es una función definida por la aplicación diseñada para indicar el estado de un control DTP que se establece en el **estilo \_ DTS SHOWNONE.**



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
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

 

 




