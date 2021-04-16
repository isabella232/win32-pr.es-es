---
description: Para compartir datos, varios procesos pueden usar archivos asignados a memoria que almacena el archivo de paginación del sistema.
ms.assetid: 17458be2-3ef7-42f2-a717-abf73ac4846f
title: Crear memoria compartida con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ac708497ceb12ed099c7a9c0b3788d7a05a925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686703"
---
# <a name="creating-named-shared-memory"></a>Crear memoria compartida con nombre

Para compartir datos, varios procesos pueden usar archivos asignados a memoria que almacena el archivo de paginación del sistema.

## <a name="first-process"></a>Primer proceso

El primer proceso crea el objeto de asignación de archivos llamando a la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) con un **\_ \_ valor de identificador no válido** y un nombre para el objeto. Mediante el uso de la marca **\_ ReadWrite de página** , el proceso tiene permiso de lectura y escritura en la memoria a través de cualquier vista de archivo que se cree.

Después, el proceso usa el identificador de objeto de asignación de archivos que [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) devuelve en una llamada a [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para crear una vista del archivo en el espacio de direcciones de proceso. La función **MapViewOfFile** devuelve un puntero a la vista de archivo, `pBuf` . Después, el proceso utiliza la función [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) para escribir una cadena en la vista a la que pueden tener acceso otros procesos.

El prefijo de los nombres de objeto de asignación de archivos con "global \\ " permite a los procesos comunicarse entre sí incluso si se encuentran en sesiones de Terminal Server diferentes. Esto requiere que el primer proceso tenga el privilegio [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) .

Cuando el proceso ya no necesita tener acceso al objeto de asignación de archivos, debe llamar a la función [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) . Cuando se cierran todos los identificadores, el sistema puede liberar la sección del archivo de paginación que utiliza el objeto.


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");
TCHAR szMsg[]=TEXT("Message from first process.");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = CreateFileMapping(
                 INVALID_HANDLE_VALUE,    // use paging file
                 NULL,                    // default security
                 PAGE_READWRITE,          // read/write access
                 0,                       // maximum object size (high-order DWORD)
                 BUF_SIZE,                // maximum object size (low-order DWORD)
                 szName);                 // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not create file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }
   pBuf = (LPTSTR) MapViewOfFile(hMapFile,   // handle to map object
                        FILE_MAP_ALL_ACCESS, // read/write permission
                        0,
                        0,
                        BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

       CloseHandle(hMapFile);

      return 1;
   }


   CopyMemory((PVOID)pBuf, szMsg, (_tcslen(szMsg) * sizeof(TCHAR)));
    _getch();

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="second-process"></a>Segundo proceso

Un segundo proceso puede tener acceso a la cadena escrita en la memoria compartida por el primer proceso mediante una llamada a la función [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) que especifica el mismo nombre para el objeto de asignación que el primer proceso. Después, puede usar la función [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para obtener un puntero a la vista de archivo, `pBuf` . El proceso puede mostrar esta cadena como cualquier otra cadena. En este ejemplo, el cuadro de mensaje que se muestra contiene el mensaje "mensaje del primer proceso" escrito por el primer proceso.


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>
#pragma comment(lib, "user32.lib")

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = OpenFileMapping(
                   FILE_MAP_ALL_ACCESS,   // read/write access
                   FALSE,                 // do not inherit the name
                   szName);               // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not open file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }

   pBuf = (LPTSTR) MapViewOfFile(hMapFile, // handle to map object
               FILE_MAP_ALL_ACCESS,  // read/write permission
               0,
               0,
               BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

      CloseHandle(hMapFile);

      return 1;
   }

   MessageBox(NULL, pBuf, TEXT("Process2"), MB_OK);

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compartir archivos y memoria](sharing-files-and-memory.md)
</dt> </dl>

 

 
