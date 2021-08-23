---
title: Cómo mostrar información sobre herramientas para botones
description: Al especificar el estilo TBSTYLE TOOLTIPS, la barra de \_ herramientas crea y administra un control de información sobre herramientas. El control de información sobre herramientas está oculto y solo aparece cuando los usuarios mueven el puntero sobre un botón de la barra de herramientas y lo dejan allí durante aproximadamente un segundo.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f169c6cc9324c98ed085b38f14802fcaa3c5cfbc8bd7ee9aa29af62ef41a6adc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320005"
---
# <a name="how-to-display-tooltips-for-buttons"></a>Cómo mostrar información sobre herramientas para botones

Al especificar el estilo [**TBSTYLE \_ TOOLTIPS,**](toolbar-control-and-button-styles.md) la barra de herramientas crea y administra un control de información sobre herramientas. El control de información sobre herramientas está oculto y solo aparece cuando los usuarios mueven el puntero sobre un botón de la barra de herramientas y lo dejan allí durante aproximadamente un segundo.

La aplicación puede proporcionar texto al control de información sobre herramientas de cualquiera de las maneras siguientes:

-   Establezca el texto de la información sobre herramientas como el **miembro iString** de la [**estructura TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) para cada botón. También debe enviar un mensaje [**\_ SETMAXTEXTROWS**](tb-setmaxtextrows.md) de TB y establecer las filas de texto máximas en 0, para que el texto no aparezca como la etiqueta del botón en lugar de como información sobre herramientas.
-   Cree la barra de herramientas con el [**estilo TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) y, a continuación, establezca el estilo extendido [**\_ TBSTYLE EX \_ MIXEDBUTTONS.**](toolbar-extended-styles.md) Las etiquetas solo se muestran para los botones que tienen el estilo [**\_ SHOWTEXT de BTNS.**](toolbar-control-and-button-styles.md) Para los botones que no tienen este estilo, se muestra una información sobre herramientas que contiene el texto del botón.
-   Responda al código [de notificación \_ GETDISPINFO de TTN.](ttn-getdispinfo.md)
-   Responda al código [de notificación \_ GETINFOTIP de TBN.](tbn-getinfotip.md)

Una aplicación que necesita enviar mensajes directamente al control de información sobre herramientas puede recuperar el identificador del control mediante el mensaje [**\_ GETTOOLTIPS de TB.**](tb-gettooltips.md) Una aplicación puede reemplazar el control de información sobre herramientas de una barra de herramientas por otro control de información sobre herramientas mediante el mensaje [**\_ SETTOOLTIPS de TB.**](tb-settooltips.md)

La manera más flexible de proporcionar texto sobre herramientas es responder al código de notificación [ \_ GETDISPINFO](ttn-getdispinfo.md) o [TBN \_ GETINFOTIP](tbn-getinfotip.md) de TTN enviado por el control de barra de herramientas a su elemento primario en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) Para [TTN \_ GETDISPINFO](ttn-getdispinfo.md), el parámetro *lParam* incluye un puntero a una estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (también definida como **LPTOOLTIPTEXT)** que especifica el identificador de comando del botón para el que se necesita texto de ayuda. Este identificador está en el **miembro NMTTDISPINFO.hdr.idFrom.** Una aplicación puede copiar el texto de ayuda en la estructura , especificar la dirección de una cadena que contiene el texto de ayuda o especificar el identificador de instancia y el identificador de recurso de un recurso de cadena.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="display-a-tooltip-for-a-button"></a>Mostrar información sobre herramientas para un botón

El código de ejemplo siguiente controla el código de notificación de información sobre herramientas [ \_ GETDISPINFO de TTN](ttn-getdispinfo.md) proporcionando texto de identificadores de recursos.


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de barra de herramientas](using-toolbar-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




