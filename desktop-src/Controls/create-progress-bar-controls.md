---
title: Cómo usar controles de barra de progreso
description: En este tema se explica cómo usar una barra de progreso para indicar el progreso de una operación de análisis de archivos larga.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e65d47d6b41422853d401a1fb2686e03e3d3f5bc378b78b7ba762b86fc7ffe30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826425"
---
# <a name="how-to-use-progress-bar-controls"></a>Cómo usar controles de barra de progreso

En este tema se explica cómo usar una barra de progreso para indicar el progreso de una operación de análisis de archivos larga.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="create-a-progress-bar-control"></a>Crear un control de barra de progreso

El código de ejemplo siguiente crea una barra de progreso y la coloca a lo largo de la parte inferior del área de cliente de la ventana primaria. El alto de la barra de progreso se basa en el alto del mapa de bits de flecha usado en una barra de desplazamiento. El intervalo se basa en el tamaño del archivo dividido entre 2048, que es el tamaño de cada "fragmento" de datos que se lee del archivo. En el ejemplo también se establece un incremento y se avanza la posición actual de la barra de progreso en el incremento después de analizar cada fragmento.


```C++
// ParseALargeFile - uses a progress bar to indicate the progress of a parsing operation.
//
// Returns TRUE if successful, or FALSE otherwise.
//
// hwndParent - parent window of the progress bar.
//
// lpszFileName - name of the file to parse. 
// 
// Global variable 
//     g_hinst - instance handle.
//

extern HINSTANCE g_hinst; 

BOOL ParseALargeFile(HWND hwndParent, LPTSTR lpszFileName) 
{ 
    RECT rcClient;  // Client area of parent window.
    int cyVScroll;  // Height of scroll bar arrow.
    HWND hwndPB;    // Handle of progress bar.
    HANDLE hFile;   // Handle of file.
    DWORD cb;       // Size of file and count of bytes read.
    LPCH pch;       // Address of data read from file.
    LPCH pchTmp;    // Temporary pointer.

    // Ensure that the common control DLL is loaded, and create a progress bar 
    // along the bottom of the client area of the parent window. 
    //
    // Base the height of the progress bar on the height of a scroll bar arrow.
    
    InitCommonControls(); 
    
    GetClientRect(hwndParent, &rcClient); 
    
    cyVScroll = GetSystemMetrics(SM_CYVSCROLL); 

    hwndPB = CreateWindowEx(0, PROGRESS_CLASS, (LPTSTR) NULL, 
                            WS_CHILD | WS_VISIBLE, rcClient.left, 
                            rcClient.bottom - cyVScroll, 
                            rcClient.right, cyVScroll, 
                            hwndParent, (HMENU) 0, g_hinst, NULL);

    // Open the file for reading, and retrieve the size of the file. 

    hFile = CreateFile(lpszFileName, GENERIC_READ, FILE_SHARE_READ, 
                       (LPSECURITY_ATTRIBUTES) NULL, OPEN_EXISTING, 
                       FILE_ATTRIBUTE_NORMAL, (HANDLE) NULL); 

    if (hFile == (HANDLE) INVALID_HANDLE_VALUE)
        return FALSE; 

    cb = GetFileSize(hFile, (LPDWORD) NULL); 

    // Set the range and increment of the progress bar. 

    SendMessage(hwndPB, PBM_SETRANGE, 0, MAKELPARAM(0, cb / 2048));
    
    SendMessage(hwndPB, PBM_SETSTEP, (WPARAM) 1, 0); 

    // Parse the file. 
    pch = (LPCH) LocalAlloc(LPTR, sizeof(char) * 2048); 
    
    pchTmp = pch; 
    
    do { 
        ReadFile(hFile, pchTmp, sizeof(char) * 2048, &cb, (LPOVERLAPPED) NULL);
        
        // TODO: Write an error handler to check that all the
        // requested data was read.
        //
        // Include here any code that parses the
        // file. 
        //  
        //  
        //  
        // Advance the current position of the progress bar by the increment.
        
        SendMessage(hwndPB, PBM_STEPIT, 0, 0); 
        
    } while (cb); 

    CloseHandle((HANDLE) hFile);
    
    DestroyWindow(hwndPB);

    return TRUE; 
}
```



## <a name="remarks"></a>Comentarios

Debe asegurarse de usar correctamente la [**función ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) para garantizar la seguridad de la aplicación. Por ejemplo, en el código de ejemplo, debe comprobar que realmente lee `ReadFile` todos los datos solicitados.

Observe también que el cuarto parámetro de [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)(LPSECURITY \_ ATTRIBUTES)**NULL** establece los valores de seguridad predeterminados. Si necesita una configuración de seguridad específica, debe establecer los valores adecuados en los miembros de la estructura. Llame **a sizeof** para establecer el tamaño correcto de la **estructura LPSECURITY \_ ATTRIBUTES.**

Para obtener más información, vea [Security Considerations: Microsoft Windows Controls](sec-comctls.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de barra de progreso](using-progress-bar-controls.md)
</dt> <dt>

[Consideraciones de seguridad: Controles de Windows Microsoft](sec-comctls.md)
</dt> </dl>

 

 