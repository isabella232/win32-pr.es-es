---
title: Cómo etiquetar dinámicamente los botones de la barra de herramientas
description: Puede asignar texto a un botón existente mediante el mensaje \_ SETBUTTONINFO de TB.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246926"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Cómo etiquetar dinámicamente los botones de la barra de herramientas

Puede asignar texto a un botón existente mediante el mensaje [**\_ SETBUTTONINFO de TB.**](tb-setbuttoninfo.md)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="dynamically-label-a-toolbar-button"></a>Etiquetar dinámicamente un botón de barra de herramientas

En el ejemplo siguiente se muestra cómo cambiar el texto del tercer botón en los ejemplos anteriores de **Guardar** a **Guardar como**.


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

Cambiar el texto de un botón mediante [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) no afecta a la cadena asignada a ese botón en la lista de cadenas interna.

Si agrega una cadena de botón de barra de herramientas a la lista de texto interna, no puede recuperar el índice de esa cadena llamando a [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md); en su lugar, debe usar el mensaje [**\_ GETBUTTON de TB.**](tb-getbutton.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de barra de herramientas](using-toolbar-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




