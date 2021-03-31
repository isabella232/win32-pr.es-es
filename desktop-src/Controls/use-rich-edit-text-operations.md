---
title: Cómo usar operaciones de edición de texto enriquecidas
description: Una aplicación puede enviar mensajes para recuperar o buscar texto en un control Rich Edit. Puede recuperar el texto seleccionado o un intervalo de texto especificado.
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b54619e1ce5952b7c0d06527c6aca2402a4e714
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995676"
---
# <a name="how-to-use-rich-edit-text-operations"></a>Cómo usar operaciones de edición de texto enriquecidas

Una aplicación puede enviar mensajes para recuperar o buscar texto en un control Rich Edit. Puede recuperar el texto seleccionado o un intervalo de texto especificado.

Para obtener el texto seleccionado en un control Rich Edit, utilice el [**mensaje \_ GETSELTEXT em**](em-getseltext.md) . El texto se copia en la matriz de caracteres especificada. Debe asegurarse de que la matriz es lo suficientemente grande como para contener el texto seleccionado más un carácter nulo de terminación.

Para recuperar un intervalo de texto especificado, use el [**mensaje \_ GETTEXTRANGE em**](em-gettextrange.md) . La estructura [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) utilizada con este mensaje especifica el intervalo de texto que se va a recuperar y apunta a una matriz de caracteres que recibe el texto. En este caso, la aplicación debe asegurarse de que la matriz es lo suficientemente grande como para el texto especificado y un carácter nulo de terminación.

Puede buscar una cadena en un control Rich Edit mediante los mensajes [**em \_ Textobuscado**](em-findtext.md) o [**em \_ FINDTEXTEX**](em-findtextex.md) , o sus equivalentes de Unicode, [**em \_ FINDTEXTW**](em-findtextw.md) y [**em \_ FINDTEXTEXW**](em-findtextexw.md). La estructura [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) que se usa con las versiones no extendidas especifica el intervalo de texto que se va a buscar y la cadena que se va a buscar. Las versiones extendidas usan una estructura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , que especifica la misma información y también recibe los puntos inicial y final del intervalo de caracteres del texto encontrado. También puede especificar estas opciones como si la búsqueda distinga mayúsculas de minúsculas.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="use-a-rich-edit-text-operation"></a>Usar una operación de edición de texto enriquecida

En la función de ejemplo siguiente se busca el texto especificado en el texto seleccionado en un control Rich Edit que admita Unicode. Si se encuentra el destino, se convierte en la nueva selección.


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

Microsoft Rich Edit 3,0 también es compatible con la función del editor de métodos de entrada (IME) HexToUnicode, que permite a un usuario convertir entre hexadecimales y Unicode mediante el uso de teclas de acceso rápido. Para obtener más información, consulte [HEXTOUNICODE IME](/windows/desktop/Intl/hextounicode-ime).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 