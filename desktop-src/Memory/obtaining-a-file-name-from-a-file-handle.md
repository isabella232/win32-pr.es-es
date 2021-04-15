---
description: GetFinalPathNameByHandle, introducido en Windows Vista y Windows Server 2008, devolverá una ruta de acceso de un identificador.
ms.assetid: 359673bf-cc4c-4881-b946-ecdbef4a7ecb
title: Obtener un nombre de archivo de un identificador de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7d0c6fd8ea6839fdbfbe887f7a28b38571013b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669931"
---
# <a name="obtaining-a-file-name-from-a-file-handle"></a><span data-ttu-id="51e9c-103">Obtener un nombre de archivo de un identificador de archivo</span><span class="sxs-lookup"><span data-stu-id="51e9c-103">Obtaining a File Name From a File Handle</span></span>

<span data-ttu-id="51e9c-104">[**GetFinalPathNameByHandle**](/windows/win32/api/fileapi/nf-fileapi-getfinalpathnamebyhandlea), introducido en Windows Vista y windows Server 2008, devolverá una ruta de acceso de un identificador.</span><span class="sxs-lookup"><span data-stu-id="51e9c-104">[**GetFinalPathNameByHandle**](/windows/win32/api/fileapi/nf-fileapi-getfinalpathnamebyhandlea), introduced in Windows Vista and Windows Server 2008, will return a path from a handle.</span></span> <span data-ttu-id="51e9c-105">Si necesita hacer esto en versiones anteriores de Windows, en el ejemplo siguiente se obtiene un nombre de archivo de un identificador a un objeto de archivo mediante un objeto de asignación de archivos.</span><span class="sxs-lookup"><span data-stu-id="51e9c-105">If you need to do this on earlier releases of Windows, the following example obtains a file name from a handle to a file object using a file mapping object.</span></span> <span data-ttu-id="51e9c-106">Usa las funciones [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) y [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para crear la asignación.</span><span class="sxs-lookup"><span data-stu-id="51e9c-106">It uses the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) and [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) functions to create the mapping.</span></span> <span data-ttu-id="51e9c-107">A continuación, se usa la función [**GetMappedFileName**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) para obtener el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="51e9c-107">Next, it uses the [**GetMappedFileName**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) function to obtain the file name.</span></span> <span data-ttu-id="51e9c-108">En el caso de los archivos remotos, imprime la ruta de acceso del dispositivo recibida de esta función.</span><span class="sxs-lookup"><span data-stu-id="51e9c-108">For remote files, it prints the device path received from this function.</span></span> <span data-ttu-id="51e9c-109">En el caso de los archivos locales, convierte la ruta de acceso para usar una letra de unidad e imprime esta ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="51e9c-109">For local files, it converts the path to use a drive letter and prints this path.</span></span> <span data-ttu-id="51e9c-110">Para probar este código, cree una función **Main** que abra un archivo mediante [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) y pase el identificador resultante a `GetFileNameFromHandle` .</span><span class="sxs-lookup"><span data-stu-id="51e9c-110">To test this code, create a **main** function that opens a file using [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) and passes the resulting handle to `GetFileNameFromHandle`.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <string.h>
#include <psapi.h>
#include <strsafe.h>

#define BUFSIZE 512

BOOL GetFileNameFromHandle(HANDLE hFile) 
{
  BOOL bSuccess = FALSE;
  TCHAR pszFilename[MAX_PATH+1];
  HANDLE hFileMap;

  // Get the file size.
  DWORD dwFileSizeHi = 0;
  DWORD dwFileSizeLo = GetFileSize(hFile, &dwFileSizeHi); 

  if( dwFileSizeLo == 0 && dwFileSizeHi == 0 )
  {
     _tprintf(TEXT("Cannot map a file with a length of zero.\n"));
     return FALSE;
  }

  // Create a file mapping object.
  hFileMap = CreateFileMapping(hFile, 
                    NULL, 
                    PAGE_READONLY,
                    0, 
                    1,
                    NULL);

  if (hFileMap) 
  {
    // Create a file mapping to get the file name.
    void* pMem = MapViewOfFile(hFileMap, FILE_MAP_READ, 0, 0, 1);

    if (pMem) 
    {
      if (GetMappedFileName (GetCurrentProcess(), 
                             pMem, 
                             pszFilename,
                             MAX_PATH)) 
      {

        // Translate path with device name to drive letters.
        TCHAR szTemp[BUFSIZE];
        szTemp[0] = '\0';

        if (GetLogicalDriveStrings(BUFSIZE-1, szTemp)) 
        {
          TCHAR szName[MAX_PATH];
          TCHAR szDrive[3] = TEXT(" :");
          BOOL bFound = FALSE;
          TCHAR* p = szTemp;

          do 
          {
            // Copy the drive letter to the template string
            *szDrive = *p;

            // Look up each device name
            if (QueryDosDevice(szDrive, szName, MAX_PATH))
            {
              size_t uNameLen = _tcslen(szName);

              if (uNameLen < MAX_PATH) 
              {
                bFound = _tcsnicmp(pszFilename, szName, uNameLen) == 0
                         && *(pszFilename + uNameLen) == _T('\\');

                if (bFound) 
                {
                  // Reconstruct pszFilename using szTempFile
                  // Replace device path with DOS path
                  TCHAR szTempFile[MAX_PATH];
                  StringCchPrintf(szTempFile,
                            MAX_PATH,
                            TEXT("%s%s"),
                            szDrive,
                            pszFilename+uNameLen);
                  StringCchCopyN(pszFilename, MAX_PATH+1, szTempFile, _tcslen(szTempFile));
                }
              }
            }

            // Go to the next NULL character.
            while (*p++);
          } while (!bFound && *p); // end of string
        }
      }
      bSuccess = TRUE;
      UnmapViewOfFile(pMem);
    } 

    CloseHandle(hFileMap);
  }
  _tprintf(TEXT("File name is %s\n"), pszFilename);
  return(bSuccess);
}

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile;

    if( argc != 2 )
    {
        _tprintf(TEXT("This sample takes a file name as a parameter.\n"));
        return 0;
    }
    hFile = CreateFile(argv[1], GENERIC_READ, FILE_SHARE_READ, NULL,
        OPEN_EXISTING, 0, NULL);

    if(hFile == INVALID_HANDLE_VALUE)
    {
        _tprintf(TEXT("CreateFile failed with %d\n"), GetLastError());
        return 0;
    }
    GetFileNameFromHandle( hFile );
}
```



## <a name="related-topics"></a><span data-ttu-id="51e9c-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51e9c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51e9c-112">Usar la asignación de archivos</span><span class="sxs-lookup"><span data-stu-id="51e9c-112">Using File Mapping</span></span>](using-file-mapping.md)
</dt> <dt>

[<span data-ttu-id="51e9c-113">**GetFinalPathNameByHandle**</span><span class="sxs-lookup"><span data-stu-id="51e9c-113">**GetFinalPathNameByHandle**</span></span>](/windows/win32/api/fileapi/nf-fileapi-getfinalpathnamebyhandlea)
</dt> </dl>

 

 
