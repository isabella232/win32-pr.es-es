---
title: Cómo usar operaciones de edición de texto enriquecido
description: Una aplicación puede enviar mensajes para recuperar o buscar texto en un control de edición enriquecido. Puede recuperar el texto seleccionado o un intervalo de texto especificado.
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b54619e1ce5952b7c0d06527c6aca2402a4e714
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165409"
---
# <a name="how-to-use-rich-edit-text-operations"></a>Cómo usar operaciones de edición de texto enriquecido

Una aplicación puede enviar mensajes para recuperar o buscar texto en un control de edición enriquecido. Puede recuperar el texto seleccionado o un intervalo de texto especificado.

Para obtener el texto seleccionado en un control de edición enriquecido, use el [**mensaje EM \_ GETSELTEXT.**](em-getseltext.md) El texto se copia en la matriz de caracteres especificada. Debe asegurarse de que la matriz sea lo suficientemente grande como para contener el texto seleccionado más un carácter nulo de terminación.

Para recuperar un intervalo de texto especificado, use el [**\_ mensaje EM GETTEXTRANGE.**](em-gettextrange.md) La [**estructura TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) utilizada con este mensaje especifica el intervalo de texto que se va a recuperar y apunta a una matriz de caracteres que recibe el texto. Aquí, de nuevo, la aplicación debe asegurarse de que la matriz sea lo suficientemente grande para el texto especificado más un carácter nulo de terminación.

Puede buscar una cadena en un control de edición enriquecido mediante los mensajes [**EM \_ FINDTEXT**](em-findtext.md) o [**EM \_ FINDTEXTEX,**](em-findtextex.md) o sus equivalentes Unicode, [**EM \_ FINDTEXTW**](em-findtextw.md) y [**EM \_ FINDTEXTEXW**](em-findtextexw.md). La [**estructura FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) que se usa con las versiones nonextended especifica el intervalo de texto que se va a buscar y la cadena que se va a buscar. Las versiones extendidas usan una [**estructura FINDTEXTEX,**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) que especifica la misma información y también recibe los puntos inicial y final del intervalo de caracteres del texto encontrado. También puede especificar opciones como si la búsqueda distingue mayúsculas de minúsculas.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-a-rich-edit-text-operation"></a>Usar una operación de edición de texto enriquecido

La siguiente función de ejemplo busca el texto especificado dentro del texto seleccionado en un control de edición enriquecido que admite Unicode. Si se encuentra el destino, se convierte en la nueva selección.


```C++
BOOL FindTextInSelection(HWND hRich, WCHAR* target)
{
    CHARRANGE selectionRange;
    
    SendMessage(hRich, EM_EXGETSEL, 0, (LPARAM)&selectionRange);
    
    FINDTEXTEX ftex;
    
    ftex.lpstrText  = target;
    ftex.chrg.cpMin = selectionRange.cpMin;
    ftex.chrg.cpMax = selectionRange.cpMax;
    
    LRESULT lr = SendMessage(hRich, EM_FINDTEXTEXW, (WPARAM)FR_DOWN, (LPARAM) &ftex);
    
    if (lr >= 0)
    {
        LRESULT lr1 = SendMessage(hRich, EM_EXSETSEL, 0, (LPARAM)&ftex.chrgText);
        
        SendMessage(hRich, EM_HIDESELECTION, (LPARAM)FALSE, 0);
        
        return TRUE;
    }
    
    return FALSE;
    
}
```



## <a name="remarks"></a>Observaciones

Microsoft Rich Edit 3.0 también admite la función Editor de métodos de entrada (IME) HexToUnicode, que permite a un usuario convertir entre hexadecimal y Unicode mediante teclas de acceso rápido. Para obtener más información, [vea HexToUnicode IME](/windows/desktop/Intl/hextounicode-ime).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 