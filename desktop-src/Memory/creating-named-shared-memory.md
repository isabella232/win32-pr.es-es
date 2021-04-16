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
# <a name="creating-named-shared-memory"></a><span data-ttu-id="38d91-103">Crear memoria compartida con nombre</span><span class="sxs-lookup"><span data-stu-id="38d91-103">Creating Named Shared Memory</span></span>

<span data-ttu-id="38d91-104">Para compartir datos, varios procesos pueden usar archivos asignados a memoria que almacena el archivo de paginación del sistema.</span><span class="sxs-lookup"><span data-stu-id="38d91-104">To share data, multiple processes can use memory-mapped files that the system paging file stores.</span></span>

## <a name="first-process"></a><span data-ttu-id="38d91-105">Primer proceso</span><span class="sxs-lookup"><span data-stu-id="38d91-105">First Process</span></span>

<span data-ttu-id="38d91-106">El primer proceso crea el objeto de asignación de archivos llamando a la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) con un **\_ \_ valor de identificador no válido** y un nombre para el objeto.</span><span class="sxs-lookup"><span data-stu-id="38d91-106">The first process creates the file mapping object by calling the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function with **INVALID\_HANDLE\_VALUE** and a name for the object.</span></span> <span data-ttu-id="38d91-107">Mediante el uso de la marca **\_ ReadWrite de página** , el proceso tiene permiso de lectura y escritura en la memoria a través de cualquier vista de archivo que se cree.</span><span class="sxs-lookup"><span data-stu-id="38d91-107">By using the **PAGE\_READWRITE** flag, the process has read/write permission to the memory through any file views that are created.</span></span>

<span data-ttu-id="38d91-108">Después, el proceso usa el identificador de objeto de asignación de archivos que [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) devuelve en una llamada a [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para crear una vista del archivo en el espacio de direcciones de proceso.</span><span class="sxs-lookup"><span data-stu-id="38d91-108">Then the process uses the file mapping object handle that [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) returns in a call to [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) to create a view of the file in the process address space.</span></span> <span data-ttu-id="38d91-109">La función **MapViewOfFile** devuelve un puntero a la vista de archivo, `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="38d91-109">The **MapViewOfFile** function returns a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="38d91-110">Después, el proceso utiliza la función [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) para escribir una cadena en la vista a la que pueden tener acceso otros procesos.</span><span class="sxs-lookup"><span data-stu-id="38d91-110">The process then uses the [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) function to write a string to the view that can be accessed by other processes.</span></span>

<span data-ttu-id="38d91-111">El prefijo de los nombres de objeto de asignación de archivos con "global \\ " permite a los procesos comunicarse entre sí incluso si se encuentran en sesiones de Terminal Server diferentes.</span><span class="sxs-lookup"><span data-stu-id="38d91-111">Prefixing the file mapping object names with "Global\\" allows processes to communicate with each other even if they are in different terminal server sessions.</span></span> <span data-ttu-id="38d91-112">Esto requiere que el primer proceso tenga el privilegio [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="38d91-112">This requires that the first process must have the [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) privilege.</span></span>

<span data-ttu-id="38d91-113">Cuando el proceso ya no necesita tener acceso al objeto de asignación de archivos, debe llamar a la función [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="38d91-113">When the process no longer needs access to the file mapping object, it should call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="38d91-114">Cuando se cierran todos los identificadores, el sistema puede liberar la sección del archivo de paginación que utiliza el objeto.</span><span class="sxs-lookup"><span data-stu-id="38d91-114">When all handles are closed, the system can free the section of the paging file that the object uses.</span></span>


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



## <a name="second-process"></a><span data-ttu-id="38d91-115">Segundo proceso</span><span class="sxs-lookup"><span data-stu-id="38d91-115">Second Process</span></span>

<span data-ttu-id="38d91-116">Un segundo proceso puede tener acceso a la cadena escrita en la memoria compartida por el primer proceso mediante una llamada a la función [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) que especifica el mismo nombre para el objeto de asignación que el primer proceso.</span><span class="sxs-lookup"><span data-stu-id="38d91-116">A second process can access the string written to the shared memory by the first process by calling the [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) function specifying the same name for the mapping object as the first process.</span></span> <span data-ttu-id="38d91-117">Después, puede usar la función [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para obtener un puntero a la vista de archivo, `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="38d91-117">Then it can use the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function to obtain a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="38d91-118">El proceso puede mostrar esta cadena como cualquier otra cadena.</span><span class="sxs-lookup"><span data-stu-id="38d91-118">The process can display this string as it would any other string.</span></span> <span data-ttu-id="38d91-119">En este ejemplo, el cuadro de mensaje que se muestra contiene el mensaje "mensaje del primer proceso" escrito por el primer proceso.</span><span class="sxs-lookup"><span data-stu-id="38d91-119">In this example, the message box displayed contains the message "Message from first process" that was written by the first process.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="38d91-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38d91-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38d91-121">Compartir archivos y memoria</span><span class="sxs-lookup"><span data-stu-id="38d91-121">Sharing Files and Memory</span></span>](sharing-files-and-memory.md)
</dt> </dl>

 

 
