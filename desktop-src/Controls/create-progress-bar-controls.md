---
title: Cómo usar los controles de barra de progreso
description: En este tema se explica cómo usar una barra de progreso para indicar el progreso de una operación prolongada de análisis de archivos.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c71ff33a14f2d2af5fa8735c5197c50acaa948b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995681"
---
# <a name="how-to-use-progress-bar-controls"></a>Cómo usar los controles de barra de progreso

En este tema se explica cómo usar una barra de progreso para indicar el progreso de una operación prolongada de análisis de archivos.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="create-a-progress-bar-control"></a>Crear un control de barra de progreso

En el código de ejemplo siguiente se crea una barra de progreso y se coloca en la parte inferior del área de cliente de la ventana primaria. El alto de la barra de progreso se basa en el alto del mapa de bits de las flechas utilizadas en una barra de desplazamiento. El intervalo se basa en el tamaño del archivo dividido por 2.048, que es el tamaño de cada "fragmento" de datos que se lee del archivo. En el ejemplo también se establece un incremento y se hace avanzar la posición actual de la barra de progreso en el incremento después de analizar cada fragmento.


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



## <a name="remarks"></a>Observaciones

Debe asegurarse de utilizar la función [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) correctamente para garantizar la seguridad de la aplicación. Por ejemplo, en el código de ejemplo, debe comprobar para asegurarse de que `ReadFile` realmente Lee todos los datos solicitados.

Observe también que el cuarto parámetro de [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)(( \_ atributos LPSECURITY)**null**: establece los valores de seguridad predeterminados. Si necesita una configuración de seguridad específica, debe establecer los valores adecuados en los miembros de la estructura. Llame a **sizeof** para establecer el tamaño correcto de la estructura de **\_ atributos LPSECURITY** .

Para obtener más información, vea [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de barra de progreso](using-progress-bar-controls.md)
</dt> <dt>

[Consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md)
</dt> </dl>

 

 