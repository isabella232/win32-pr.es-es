---
description: En el ejemplo siguiente se usa la función GetFileTime para recuperar la hora de la última escritura de un archivo. Convierte el tiempo en la hora local en función de la configuración actual de la zona horaria y crea una cadena de fecha y hora que se puede mostrar al usuario.
ms.assetid: 54509a35-fa6a-4ee6-90f8-36c9ef55e1bc
title: Recuperación del tiempo de Last-Write
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2332a55744eda1ea93853e6967f0cf1b4d45046d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277951"
---
# <a name="retrieving-the-last-write-time"></a>Recuperación del tiempo de Last-Write

En el ejemplo siguiente se usa la función [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) para recuperar la hora de la última escritura de un archivo. Convierte el tiempo en la hora local en función de la configuración actual de la zona horaria y crea una cadena de fecha y hora que se puede mostrar al usuario.


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>

// GetLastWriteTime - Retrieves the last-write time and converts
//                    the time to a string
//
// Return value - TRUE if successful, FALSE otherwise
// hFile      - Valid file handle
// lpszString - Pointer to buffer to receive string

BOOL GetLastWriteTime(HANDLE hFile, LPTSTR lpszString, DWORD dwSize)
{
    FILETIME ftCreate, ftAccess, ftWrite;
    SYSTEMTIME stUTC, stLocal;
    DWORD dwRet;

    // Retrieve the file times for the file.
    if (!GetFileTime(hFile, &ftCreate, &ftAccess, &ftWrite))
        return FALSE;

    // Convert the last-write time to local time.
    FileTimeToSystemTime(&ftWrite, &stUTC);
    SystemTimeToTzSpecificLocalTime(NULL, &stUTC, &stLocal);

    // Build a string showing the date and time.
    dwRet = StringCchPrintf(lpszString, dwSize, 
        TEXT("%02d/%02d/%d  %02d:%02d"),
        stLocal.wMonth, stLocal.wDay, stLocal.wYear,
        stLocal.wHour, stLocal.wMinute);

    if( S_OK == dwRet )
        return TRUE;
    else return FALSE;
}

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile;
    TCHAR szBuf[MAX_PATH];

    if( argc != 2 )
    {
        printf("This sample takes a file name as a parameter\n");
        return 0;
    }
    hFile = CreateFile(argv[1], GENERIC_READ, FILE_SHARE_READ, NULL,
        OPEN_EXISTING, 0, NULL);

    if(hFile == INVALID_HANDLE_VALUE)
    {
        printf("CreateFile failed with %d\n", GetLastError());
        return 0;
    }
    if(GetLastWriteTime( hFile, szBuf, MAX_PATH ))
        _tprintf(TEXT("Last write time is: %s\n"), szBuf);
        
    CloseHandle(hFile);    
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)
</dt> <dt>

[**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)
</dt> </dl>

 

 
