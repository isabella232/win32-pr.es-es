---
description: En el ejemplo siguiente se usa la función CreateFileMapping con la \_ marca de páginas grandes de sec \_ para usar páginas grandes. Requiere Windows Server 2003 con Service Pack 1 (SP1) o posterior.
ms.assetid: be2cdcbc-03e8-407d-8ae2-569f8fd8cba8
title: Crear una asignación de archivos mediante páginas grandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a852de187f6798904ef1795dca5955663283f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686706"
---
# <a name="creating-a-file-mapping-using-large-pages"></a><span data-ttu-id="eae07-104">Crear una asignación de archivos mediante páginas grandes</span><span class="sxs-lookup"><span data-stu-id="eae07-104">Creating a File Mapping Using Large Pages</span></span>

<span data-ttu-id="eae07-105">En el ejemplo siguiente se usa la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) con la marca de **\_ \_ páginas grandes de sec** para usar páginas grandes.</span><span class="sxs-lookup"><span data-stu-id="eae07-105">The following example uses the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function with the **SEC\_LARGE\_PAGES** flag to use large pages.</span></span> <span data-ttu-id="eae07-106">El búfer debe ser lo suficientemente grande como para contener el tamaño mínimo de una página grande.</span><span class="sxs-lookup"><span data-stu-id="eae07-106">The buffer must be large enough to contain the minimum size of a large page.</span></span> <span data-ttu-id="eae07-107">Este valor se obtiene mediante la función [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) .</span><span class="sxs-lookup"><span data-stu-id="eae07-107">This value is obtained using the [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) function.</span></span> <span data-ttu-id="eae07-108">Esta característica también requiere el privilegio "SeLockMemoryPrivilege".</span><span class="sxs-lookup"><span data-stu-id="eae07-108">This feature also requires the "SeLockMemoryPrivilege" privilege.</span></span>

> [!NOTE]
> <span data-ttu-id="eae07-109">A partir de la versión 1703 de Windows 10, la función [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) asigna una vista mediante páginas pequeñas de forma predeterminada, incluso para los objetos de asignación de archivos creados con la marca de **\_ \_ páginas grandes de segundos** .</span><span class="sxs-lookup"><span data-stu-id="eae07-109">Starting in Windows 10, version 1703, the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function maps a view using small pages by default, even for file mapping objects created with the **SEC\_LARGE\_PAGES** flag.</span></span> <span data-ttu-id="eae07-110">En esta versión y versiones posteriores del sistema operativo, debe especificar el indicador de **\_ \_ \_ páginas grandes de mapa de archivos** con la función [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para asignar páginas grandes.</span><span class="sxs-lookup"><span data-stu-id="eae07-110">In this and later OS versions, you must specify the **FILE\_MAP\_LARGE\_PAGES** flag with the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function to map large pages.</span></span> <span data-ttu-id="eae07-111">Esta marca se omite en las versiones del sistema operativo anteriores a Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="eae07-111">This flag is ignored on OS versions before Windows 10, version 1703.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="eae07-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eae07-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eae07-113">Crear un objeto de asignación de archivos</span><span class="sxs-lookup"><span data-stu-id="eae07-113">Creating a File Mapping Object</span></span>](creating-a-file-mapping-object.md)
</dt> <dt>

[<span data-ttu-id="eae07-114">Compatibilidad con páginas de gran tamaño</span><span class="sxs-lookup"><span data-stu-id="eae07-114">Large Page Support</span></span>](large-page-support.md)
</dt> </dl>

 

 
