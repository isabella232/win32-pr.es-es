---
title: Cómo etiquetar dinámicamente botones de barra de herramientas
description: Puede asignar texto a un botón existente mediante el \_ mensaje TB SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104487375"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Cómo etiquetar dinámicamente botones de barra de herramientas

Puede asignar texto a un botón existente mediante el mensaje [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) .

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="dynamically-label-a-toolbar-button"></a>Etiquetar dinámicamente un botón de la barra de herramientas

En el ejemplo siguiente se muestra cómo cambiar el texto del tercer botón en los ejemplos anteriores de **Guardar** para **Guardar como**.


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a>Observaciones

Cambiar el texto de un botón mediante [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) no afecta a la cadena asignada a ese botón en la lista de cadenas internas.

Si agrega una cadena de botón de barra de herramientas a la lista de texto interno, no puede recuperar el índice de esa cadena mediante una llamada a [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md); debe usar el mensaje [**\_ GETBUTTON TB**](tb-getbutton.md) en su lugar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Toolbar](using-toolbar-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




