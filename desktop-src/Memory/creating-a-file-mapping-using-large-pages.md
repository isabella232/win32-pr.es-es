---
description: En el ejemplo siguiente se usa la función CreateFileMapping con la marca SEC \_ LARGE PAGES para usar páginas \_ grandes. Requiere Windows Server 2003 con Service Pack 1 (SP1) o posterior.
ms.assetid: be2cdcbc-03e8-407d-8ae2-569f8fd8cba8
title: Crear una asignación de archivos mediante páginas grandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df68cc483856d0fe7f329b4f5e6e5c8a424a8c0e55958ca1da8de1ce51cbf71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869945"
---
# <a name="creating-a-file-mapping-using-large-pages"></a>Crear una asignación de archivos mediante páginas grandes

En el ejemplo siguiente se usa [**la función CreateFileMapping con**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) la marca SEC LARGE **\_ \_ PAGES** para usar páginas grandes. El búfer debe ser lo suficientemente grande como para contener el tamaño mínimo de una página grande. Este valor se obtiene mediante la [**función GetLargePageMinimum.**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) Esta característica también requiere el privilegio "SeLockMemoryPrivilege".

> [!NOTE]
> A partir Windows 10, versión 1703, la función [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) asigna una vista mediante páginas pequeñas de forma predeterminada, incluso para los objetos de asignación de archivos creados con la marca **SEC LARGE \_ \_ PAGES.** En esta y versiones posteriores del sistema operativo, debe especificar la marca **FILE \_ MAP LARGE \_ \_ PAGES** con la [**función MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para asignar páginas grandes. Esta marca se omite en las versiones del sistema operativo antes Windows 10, versión 1703.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUF_SIZE 65536

TCHAR szName[]=TEXT("LARGEPAGE");
typedef int (*GETLARGEPAGEMINIMUM)(void);

void DisplayError(const wchar_t* pszAPI, DWORD dwError)
{
    LPVOID lpvMessageBuffer;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER |
                  FORMAT_MESSAGE_FROM_SYSTEM |
                  FORMAT_MESSAGE_IGNORE_INSERTS,
                  NULL, dwError,
                  MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
                  (LPTSTR)&lpvMessageBuffer, 0, NULL);

    //... now display this string
    _tprintf(TEXT("ERROR: API        = %s\n"), pszAPI);
    _tprintf(TEXT("       error code = %d\n"), dwError);
    _tprintf(TEXT("       message    = %s\n"), lpvMessageBuffer);

    // Free the buffer allocated by the system
    LocalFree(lpvMessageBuffer);

    ExitProcess(GetLastError());
}

void Privilege(const wchar_t* pszPrivilege, BOOL bEnable)
{
    HANDLE           hToken;
    TOKEN_PRIVILEGES tp;
    BOOL             status;
    DWORD            error;

    // open process token
    if (!OpenProcessToken(GetCurrentProcess(), TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken))
        DisplayError(TEXT("OpenProcessToken"), GetLastError());

    // get the luid
    if (!LookupPrivilegeValue(NULL, pszPrivilege, &tp.Privileges[0].Luid))
        DisplayError(TEXT("LookupPrivilegeValue"), GetLastError());

    tp.PrivilegeCount = 1;

    // enable or disable privilege
    if (bEnable)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // enable or disable privilege
    status = AdjustTokenPrivileges(hToken, FALSE, &tp, 0, (PTOKEN_PRIVILEGES)NULL, 0);

    // It is possible for AdjustTokenPrivileges to return TRUE and still not succeed.
    // So always check for the last error value.
    error = GetLastError();
    if (!status || (error != ERROR_SUCCESS))
        DisplayError(TEXT("AdjustTokenPrivileges"), GetLastError());

    // close the handle
    if (!CloseHandle(hToken))
        DisplayError(TEXT("CloseHandle"), GetLastError());
}

int _tmain(void)
{
    HANDLE hMapFile;
    LPCTSTR pBuf;
    DWORD size;
    GETLARGEPAGEMINIMUM pGetLargePageMinimum;
    HINSTANCE  hDll;

    // call succeeds only on Windows Server 2003 SP1 or later
    hDll = LoadLibrary(TEXT("kernel32.dll"));
    if (hDll == NULL)
        DisplayError(TEXT("LoadLibrary"), GetLastError());

    pGetLargePageMinimum = (GETLARGEPAGEMINIMUM)GetProcAddress(hDll,
        "GetLargePageMinimum");
    if (pGetLargePageMinimum == NULL)
        DisplayError(TEXT("GetProcAddress"), GetLastError());

    size = (*pGetLargePageMinimum)();

    FreeLibrary(hDll);

    _tprintf(TEXT("Page Size: %u\n"), size);

    Privilege(TEXT("SeLockMemoryPrivilege"), TRUE);

    hMapFile = CreateFileMapping(
         INVALID_HANDLE_VALUE,    // use paging file
         NULL,                    // default security
         PAGE_READWRITE | SEC_COMMIT | SEC_LARGE_PAGES,
         0,                       // max. object size
         size,                    // buffer size
         szName);                 // name of mapping object

    if (hMapFile == NULL)
        DisplayError(TEXT("CreateFileMapping"), GetLastError());
    else
        _tprintf(TEXT("File mapping object successfully created.\n"));

    Privilege(TEXT("SeLockMemoryPrivilege"), FALSE);

    pBuf = (LPTSTR) MapViewOfFile(hMapFile,          // handle to map object
         FILE_MAP_ALL_ACCESS | FILE_MAP_LARGE_PAGES, // read/write permission
         0,
         0,
         BUF_SIZE);

    if (pBuf == NULL)
        DisplayError(TEXT("MapViewOfFile"), GetLastError());
    else
        _tprintf(TEXT("View of file successfully mapped.\n"));

    // do nothing, clean up an exit
    UnmapViewOfFile(pBuf);
    CloseHandle(hMapFile);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un objeto de asignación de archivos](creating-a-file-mapping-object.md)
</dt> <dt>

[Compatibilidad con páginas grandes](large-page-support.md)
</dt> </dl>

 

 
