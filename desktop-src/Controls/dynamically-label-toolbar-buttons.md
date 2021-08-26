---
title: Cómo etiquetar dinámicamente los botones de la barra de herramientas
description: Puede asignar texto a un botón existente mediante el mensaje \_ TB SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063a3b8be8a23dc8cead219c53989a8ff1a40225dc8411f9e8a1b156b6bb55bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877445"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Cómo etiquetar dinámicamente los botones de la barra de herramientas

Puede asignar texto a un botón existente mediante el mensaje [**\_ TB SETBUTTONINFO.**](tb-setbuttoninfo.md)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

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



## <a name="remarks"></a>Comentarios

Cambiar el texto de un botón mediante [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) no afecta a la cadena asignada a ese botón en la lista de cadenas interna.

Si agrega una cadena de botón de barra de herramientas a la lista de texto interno, no puede recuperar el índice de esa cadena mediante una llamada a [TBN \_ GETBUTTONINFO;](tbn-getbuttoninfo.md)en su lugar, debe usar el mensaje [**TB \_ GETBUTTON.**](tb-getbutton.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de barra de herramientas](using-toolbar-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




