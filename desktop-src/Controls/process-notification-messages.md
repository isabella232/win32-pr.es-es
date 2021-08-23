---
title: Cómo procesar mensajes de notificación
description: Una hoja de propiedades envía mensajes WM NOTIFY para recuperar información de las páginas y \_ notificar a las páginas las acciones del usuario.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9baf0c58fdbcbe5378dd46e828a2d29a7c91832174c9564660a82c5ab70997a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575485"
---
# <a name="how-to-process-notification-messages"></a>Cómo procesar mensajes de notificación

Una hoja de propiedades envía [**mensajes WM \_ NOTIFY**](wm-notify.md) para recuperar información de las páginas y notificar a las páginas las acciones del usuario.

El *parámetro lParam* del mensaje es la dirección de una estructura [**NMHDR,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene el identificador del cuadro de diálogo de la hoja de propiedades, el identificador del cuadro de diálogo de página y un código de notificación. La página debe responder a algunos mensajes de notificación estableciendo el valor MSGRESULT de DWL de la página \_ en **TRUE** o **FALSE.**

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="process-notification-messages"></a>Procesar mensajes de notificación

El ejemplo siguiente es un fragmento de código del procedimiento de cuadro de diálogo de una página. Muestra cómo procesar el código de [notificación de LA AYUDA \_ de PSN.](psn-help.md)


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

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




