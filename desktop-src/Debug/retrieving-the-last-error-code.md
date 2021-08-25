---
description: Cuando se produce un error en muchas funciones del sistema, establecen el último código de error.
ms.assetid: 4cc626ac-7574-44ce-8377-e0bdd8e74b7e
title: Recuperación del Last-Error código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853fb6991bab5ad761dacaf18a2ec086dbf8fc4176964888bd0ededc548fbeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912455"
---
# <a name="retrieving-the-last-error-code"></a>Recuperación del Last-Error código

Cuando se produce un error en muchas funciones del sistema, establecen el último código de error. Si la aplicación necesita más detalles sobre un error, puede recuperar el código del último error mediante la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) y mostrar una descripción del error mediante la [**función FormatMessage.**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)

En el ejemplo siguiente se incluye una función de control de errores que imprime el mensaje de error y finaliza el proceso. El *parámetro lpszFunction* es el nombre de la función que establece el código de último error.


```C++
#include <windows.h>
#include <strsafe.h>

void ErrorExit(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code

    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    // Display the error message and exit the process

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR)lpMsgBuf) + lstrlen((LPCTSTR)lpszFunction) + 40) * sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR)lpDisplayBuf, TEXT("Error"), MB_OK); 

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
    ExitProcess(dw); 
}

void main()
{
    // Generate an error

    if(!GetProcessId(NULL))
        ErrorExit(TEXT("GetProcessId"));
}
```



 

 
