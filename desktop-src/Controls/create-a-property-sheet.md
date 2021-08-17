---
title: Cómo crear una hoja de propiedades
description: En el ejemplo de esta sección se crea una hoja de propiedades que contiene dos páginas \ 8212; una para establecer las propiedades de fuente de una celda en una hoja de cálculo y otra para establecer las propiedades de borde de la celda.
ms.assetid: 61ACF87A-938C-4487-ACEB-484FCB677C6A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa99c3e678fa7d8e6aa70cd3f5c6e4c7bc514f94114c7bb7a411fa7df1caac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831851"
---
# <a name="how-to-create-a-property-sheet"></a>Cómo crear una hoja de propiedades

En el ejemplo de esta sección se crea una hoja de propiedades que contiene dos páginas: una para establecer las propiedades de fuente de una celda en una hoja de cálculo y otra para establecer las propiedades de borde de la celda.

En el ejemplo se definen las páginas rellenando un par de estructuras [**PROPSHEETPAGE**](pss-propsheetpage.md) y especificando la dirección en la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) que se pasa a la [**función PropertySheet.**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="create-a-property-sheet"></a>Crear una hoja de propiedades

En el ejemplo de código siguiente se muestra cómo crear una hoja de propiedades de dos páginas.


```C++
// DoPropertySheet - creates a property sheet that contains two pages.
//
// hwndOwner - handle to the owner window of the property sheet.
//
// Global variables
//     g_hinst - instance handle

extern HINSTANCE g_hinst;

VOID DoPropertySheet(HWND hwndOwner)
{
    PROPSHEETPAGE psp[2];
    
    PROPSHEETHEADER psh;
    
    psp[0].dwSize      = sizeof(PROPSHEETPAGE);
    psp[0].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[0].hInstance   = g_hinst;
    psp[0].pszTemplate = MAKEINTRESOURCE(DLG_FONT);
    psp[0].pszIcon     = MAKEINTRESOURCE(IDI_FONT);
    psp[0].pfnDlgProc  = FontDialogProc;
    psp[0].pszTitle    = MAKEINTRESOURCE(IDS_FONT)
    psp[0].lParam      = 0;
    psp[0].pfnCallback = NULL;
    psp[1].dwSize      = sizeof(PROPSHEETPAGE);
    psp[1].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[1].hInstance   = g_hinst;
    psp[1].pszTemplate = MAKEINTRESOURCE(DLG_BORDER);
    psp[1].pszIcon     = MAKEINTRESOURCE(IDI_BORDER);
    psp[1].pfnDlgProc  = BorderDialogProc;
    psp[1].pszTitle    = MAKEINTRESOURCE(IDS_BORDER);
    psp[1].lParam      = 0;
    psp[1].pfnCallback = NULL;
    
    psh.dwSize      = sizeof(PROPSHEETHEADER);
    psh.dwFlags     = PSH_USEICONID | PSH_PROPSHEETPAGE;
    psh.hwndParent  = hwndOwner;
    psh.hInstance   = g_hinst;
    psh.pszIcon     = MAKEINTRESOURCE(IDI_CELL_PROPERTIES);
    psh.pszCaption  = (LPSTR) "Cell Properties";
    psh.nPages      = sizeof(psp) / sizeof(PROPSHEETPAGE);
    psh.nStartPage  = 0;
    psh.ppsp        = (LPCPROPSHEETPAGE) &psp;
    psh.pfnCallback = NULL;
    
    PropertySheet(&psh);
    
    return;
}
```



## <a name="remarks"></a>Comentarios

Las plantillas de cuadro de diálogo, los iconos y las etiquetas de las páginas se cargan desde los recursos contenidos en el archivo ejecutable de la aplicación. El icono de la hoja de propiedades también se carga desde los recursos de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar hojas de propiedades](using-property-sheets.md)
</dt> <dt>

[Ejemplo de propiedad](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




