---
title: Cómo mostrar la información sobre herramientas de los botones
description: Al especificar el estilo de \_ información sobre herramientas de TBSTYLE, la barra de herramientas crea y administra un control de información sobre herramientas. El control ToolTip está oculto y solo aparece cuando los usuarios mueven el puntero sobre un botón de la barra de herramientas y lo dejan ahí durante aproximadamente un segundo.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb37de7c21c904673a1f656533497130d50bd8f7
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103904453"
---
# <a name="how-to-display-tooltips-for-buttons"></a>Cómo mostrar la información sobre herramientas de los botones

Al especificar el estilo [**de \_ información sobre herramientas de TBSTYLE**](toolbar-control-and-button-styles.md) , la barra de herramientas crea y administra un control de información sobre herramientas. El control ToolTip está oculto y solo aparece cuando los usuarios mueven el puntero sobre un botón de la barra de herramientas y lo dejan ahí durante aproximadamente un segundo.

La aplicación puede proporcionar texto al control ToolTip de cualquiera de las maneras siguientes:

-   Establezca el texto de la información sobre herramientas como el miembro **iString** de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) para cada botón. También debe enviar un mensaje de [**TB \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md) y establecer el número máximo de filas de texto en 0, de modo que el texto no aparezca como etiqueta de botón en lugar de como información sobre herramientas.
-   Cree la barra de herramientas con el estilo de [**\_ lista TBSTYLE**](toolbar-control-and-button-styles.md) y, a continuación, establezca el estilo extendido [**TBSTYLE \_ ex \_ MIXEDBUTTONS**](toolbar-extended-styles.md) . Las etiquetas solo se muestran para los botones que tienen el estilo [**BTNS \_ SHOWTEXT**](toolbar-control-and-button-styles.md) . En el caso de los botones que no tienen este estilo, se muestra una información sobre herramientas que contiene el texto del botón.
-   Responda al código de notificación de [ \_ GETDISPINFO de TTN](ttn-getdispinfo.md) .
-   Responda al código de notificación de [ \_ GETINFOTIP de TBN](tbn-getinfotip.md) .

Una aplicación que necesita enviar mensajes directamente al control ToolTip puede recuperar el identificador del control mediante el mensaje [**TB \_ GETTOOLTIPS**](tb-gettooltips.md) . Una aplicación puede reemplazar el control ToolTip de una barra de herramientas por otro control ToolTip mediante el mensaje [**\_ SETTOOLTIPS TB**](tb-settooltips.md) .

La forma más flexible de proporcionar texto de información sobre herramientas es responder al código de notificación [TTN \_ GETDISPINFO](ttn-getdispinfo.md) o [TBN \_ GETINFOTIP](tbn-getinfotip.md) enviado por el control de la barra de herramientas a su elemento primario en forma de un mensaje de [**\_ notificación de WM**](wm-notify.md) . En el caso de [TTN \_ GETDISPINFO](ttn-getdispinfo.md), el parámetro *lParam* incluye un puntero a una estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (también definida como **LPTOOLTIPTEXT**) que especifica el identificador de comando del botón para el que se necesita texto de ayuda. Este identificador está en el miembro **NMTTDISPINFO. HDR. idFrom** . Una aplicación puede copiar el texto de ayuda en la estructura, especificar la dirección de una cadena que contiene el texto de ayuda o especificar el identificador de instancia y el identificador de recurso de un recurso de cadena.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="display-a-tooltip-for-a-button"></a>Mostrar información sobre herramientas para un botón

En el ejemplo de código siguiente se controla el código de notificación de la información sobre herramientas de [TTN \_ GETDISPINFO](ttn-getdispinfo.md) proporcionando texto de los identificadores de recursos.


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

[Usar controles Toolbar](using-toolbar-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




