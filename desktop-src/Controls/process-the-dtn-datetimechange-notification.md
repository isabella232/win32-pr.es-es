---
title: Cómo procesar la notificación de DTN_DATETIMECHANGE
description: En este tema se muestra cómo procesar la notificación de cambios realizados por el usuario en el control selector de fecha y hora (DTP).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434c7ebbda673f76a757375e9a3d23504483d42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995775"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a>Cómo procesar la notificación de \_ DATETIMECHANGE de DTN

En este tema se muestra cómo procesar la notificación de cambios realizados por el usuario en el control selector de fecha y hora (DTP).

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Un control de DTP envía el código de notificación [ \_ DATETIMECHANGE de DTN](dtn-datetimechange.md) cada vez que se produce un cambio. Por ejemplo, esta notificación se generará cuando el usuario cambie uno de los campos del control o, en el caso de que el control se establezca en el [**estilo \_ SHOWNONE de DTS**](date-and-time-picker-control-styles.md) , cuando el usuario cambie el estado de la casilla del control.

La aplicación debe incluir código para procesar \_ los mensajes de DTN DATETIMECHANGE que envía el control de DTP.

El siguiente ejemplo de código C++ es una función definida por la aplicación diseñada para indicar el estado de un control de DTP establecido en el estilo **\_ SHOWNONE de DTS** .



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

[Usar controles de selector de fecha y hora](using-date-and-time-picker.md)
</dt> <dt>

[Referencia de control de selector de fecha y hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selector de fecha y hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




