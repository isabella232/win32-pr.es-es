---
title: Cómo usar secuencias
description: Puede usar secuencias para transferir datos dentro o fuera de un control Rich Edit. Una secuencia se define mediante una estructura EDITSTREAM, que especifica un búfer y una función de devolución de llamada definida por la aplicación.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89a9cc2a8caa157f9c65220fc5cead7564bc555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104149145"
---
# <a name="how-to-use-streams"></a>Cómo usar secuencias

Puede usar secuencias para transferir datos dentro o fuera de un control Rich Edit. Una secuencia se define mediante una estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) , que especifica un búfer y una función de devolución de llamada definida por la aplicación.

Para leer los datos en un control Rich Edit (es decir, el flujo en los datos), use el mensaje [**\_ secuencia em**](em-streamin.md) . El control llama repetidamente a la función de devolución de llamada de la aplicación, que transfiere una parte de los datos en el búfer cada vez.

Para guardar el contenido de un control Rich Edit (es decir, hacer streaming de los datos), puede usar el mensaje [**\_ STREAMOUT em**](em-streamout.md) . El control escribe repetidamente en el búfer y, a continuación, llama a la función de devolución de llamada de la aplicación. Para cada llamada, la función de devolución de llamada guarda el contenido del búfer.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="use-a-stream"></a>Usar una secuencia

En el ejemplo de código siguiente se muestra cómo leer un archivo. rtf en un control Rich Edit. El identificador de archivo se pasa a la función de devolución de llamada a través del miembro **dwCookie** de la estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .


```C++
DWORD CALLBACK EditStreamCallback(DWORD_PTR dwCookie, 
                                  LPBYTE lpBuff,
                                  LONG cb, 
                                  PLONG pcb)
{
    HANDLE hFile = (HANDLE)dwCookie;
    
    if (ReadFile(hFile, lpBuff, cb, (DWORD *)pcb, NULL)) 
    {
        return 0;
    }
    
    return -1;
}

BOOL FillRichEditFromFile(HWND hwnd, LPCTSTR pszFile)
{
    BOOL fSuccess = FALSE;
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, 
                              FILE_SHARE_READ, 0, OPEN_EXISTING,
                              FILE_FLAG_SEQUENTIAL_SCAN, NULL);
        
    if (hFile != INVALID_HANDLE_VALUE) 
    {
        EDITSTREAM es = { 0 };
        
        es.pfnCallback = EditStreamCallback;
        es.dwCookie    = (DWORD_PTR)hFile;
        
        if (SendMessage(hwnd, EM_STREAMIN, SF_RTF, (LPARAM)&es) && es.dwError == 0) 
        {
                fSuccess = TRUE;
        }
        
        CloseHandle(hFile);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




