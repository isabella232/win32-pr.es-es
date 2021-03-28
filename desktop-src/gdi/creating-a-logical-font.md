---
description: Puede usar el cuadro de diálogo fuente común para mostrar las fuentes disponibles.
ms.assetid: 317ea311-0592-432a-87b5-58296de003aa
title: Crear una fuente lógica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4398f426ae2dd0f18c21409422dfbcb53f0e6ee8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985014"
---
# <a name="creating-a-logical-font"></a>Crear una fuente lógica

Puede usar el cuadro de diálogo **fuente** común para mostrar las fuentes disponibles. El cuadro de diálogo **ChooseFont** se muestra después de que una aplicación inicialice los miembros de una estructura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) y llame a la función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) . Después de que el usuario seleccione una de las fuentes disponibles y presione el botón **Aceptar** , la función **ChooseFont** Inicializa una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) con los datos pertinentes. A continuación, la aplicación puede llamar a la función [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta) y crear una fuente lógica basada en la solicitud del usuario. En el ejemplo siguiente se muestra cómo hacerlo.


```C++
HFONT FAR PASCAL MyCreateFont( void ) 
{ 
    CHOOSEFONT cf; 
    LOGFONT lf; 
    HFONT hfont; 
 
    // Initialize members of the CHOOSEFONT structure.  
 
    cf.lStructSize = sizeof(CHOOSEFONT); 
    cf.hwndOwner = (HWND)NULL; 
    cf.hDC = (HDC)NULL; 
    cf.lpLogFont = &lf; 
    cf.iPointSize = 0; 
    cf.Flags = CF_SCREENFONTS; 
    cf.rgbColors = RGB(0,0,0); 
    cf.lCustData = 0L; 
    cf.lpfnHook = (LPCFHOOKPROC)NULL; 
    cf.lpTemplateName = (LPSTR)NULL; 
    cf.hInstance = (HINSTANCE) NULL; 
    cf.lpszStyle = (LPSTR)NULL; 
    cf.nFontType = SCREEN_FONTTYPE; 
    cf.nSizeMin = 0; 
    cf.nSizeMax = 0; 
 
    // Display the CHOOSEFONT common-dialog box.  
 
    ChooseFont(&cf); 
 
    // Create a logical font based on the user's  
    // selection and return a handle identifying  
    // that font.  
 
    hfont = CreateFontIndirect(cf.lpLogFont); 
    return (hfont); 
} 
```



 

 
