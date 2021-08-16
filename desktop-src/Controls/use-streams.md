---
title: Uso de Secuencias
description: Puede usar secuencias para transferir datos dentro o fuera de un control de edición enriquecido. Una secuencia se define mediante una estructura EDITSTREAM, que especifica un búfer y una función de devolución de llamada definida por la aplicación.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae620d123ad983cd150bf78d27d99de137ec61eea8c5a32c9fcc9698cb262a63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828627"
---
# <a name="how-to-use-streams"></a>Uso de Secuencias

Puede usar secuencias para transferir datos dentro o fuera de un control de edición enriquecido. Una secuencia se define mediante una [**estructura EDITSTREAM,**](/windows/desktop/api/Richedit/ns-richedit-editstream) que especifica un búfer y una función de devolución de llamada definida por la aplicación.

Para leer datos en un control de edición enriquecido (es decir, transmitir los datos), use el [**mensaje EM \_ STREAMIN.**](em-streamin.md) El control llama repetidamente a la función de devolución de llamada de la aplicación, que transfiere una parte de los datos al búfer cada vez.

Para guardar el contenido de un control de edición enriquecido (es decir, transmitir los datos), puede usar el [**mensaje EM \_ STREAMOUT.**](em-streamout.md) El control escribe repetidamente en el búfer y, a continuación, llama a la función de devolución de llamada de la aplicación. Para cada llamada, la función de devolución de llamada guarda el contenido del búfer.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-a-stream"></a>Usar una secuencia

En el ejemplo de código siguiente se muestra cómo leer un archivo .rtf en un control de edición enriquecido. El identificador de archivo se pasa a la función de devolución de llamada a través del **miembro dwCookie** de la [**estructura EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream)


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

[Usar controles rich edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




