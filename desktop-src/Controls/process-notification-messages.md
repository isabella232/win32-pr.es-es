---
title: Cómo procesar mensajes de notificación
description: Una hoja de propiedades envía \_ mensajes de notificación de WM para recuperar información de las páginas y para notificar a las páginas las acciones del usuario.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789357"
---
# <a name="how-to-process-notification-messages"></a>Cómo procesar mensajes de notificación

Una hoja de propiedades envía mensajes de [**\_ notificación de WM**](wm-notify.md) para recuperar información de las páginas y para notificar a las páginas las acciones del usuario.

El parámetro *lParam* del mensaje es la dirección de una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene el identificador del cuadro de diálogo de la hoja de propiedades, el identificador del cuadro de diálogo de la página y un código de notificación. La página debe responder a algunos mensajes de notificación estableciendo el \_ valor de DWL MSGRESULT de la página en **true** o **false**.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="process-notification-messages"></a>Procesar mensajes de notificación

El ejemplo siguiente es un fragmento de código del procedimiento de cuadro de diálogo para una página. Muestra cómo procesar el código de notificación de la [ \_ ayuda de PSN](psn-help.md) .


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar hojas de propiedades](using-property-sheets.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




