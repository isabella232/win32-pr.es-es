---
description: Código de ejemplo que muestra cómo una aplicación puede anexar un archivo al final de otro archivo, incluido cómo abrir y cerrar archivos, leer y escribir en archivos, y bloquear y desbloquear archivos.
ms.assetid: e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5
title: Anexar un archivo a otro archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 546d24fe88a2bbf22c190a0caca3b3f98e753720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687659"
---
# <a name="appending-one-file-to-another-file"></a><span data-ttu-id="3da5a-103">Anexar un archivo a otro archivo</span><span class="sxs-lookup"><span data-stu-id="3da5a-103">Appending One File to Another File</span></span>

<span data-ttu-id="3da5a-104">En el ejemplo de código de este tema se muestra cómo abrir y cerrar archivos, leer y escribir en archivos, y bloquear y desbloquear archivos.</span><span class="sxs-lookup"><span data-stu-id="3da5a-104">The code example in this topic shows you how to open and close files, read and write to files, and lock and unlock files.</span></span>

<span data-ttu-id="3da5a-105">En el ejemplo, la aplicación anexa un archivo al final de otro archivo.</span><span class="sxs-lookup"><span data-stu-id="3da5a-105">In the example, the application appends one file to the end of another file.</span></span> <span data-ttu-id="3da5a-106">En primer lugar, la aplicación abre el archivo que se está anexando con permisos que solo permiten que la aplicación escriba en él.</span><span class="sxs-lookup"><span data-stu-id="3da5a-106">First, the application opens the file being appended with permissions that allow only the application to write to it.</span></span> <span data-ttu-id="3da5a-107">Sin embargo, durante el proceso de anexar otros procesos pueden abrir el archivo con permiso de solo lectura, que proporciona una vista de instantánea del archivo que se va a anexar.</span><span class="sxs-lookup"><span data-stu-id="3da5a-107">However, during the append process other processes can open the file with read-only permission, which provides a snapshot view of the file being appended.</span></span> <span data-ttu-id="3da5a-108">A continuación, el archivo se bloquea durante el proceso de anexión real para garantizar la integridad de los datos que se escriben en el archivo.</span><span class="sxs-lookup"><span data-stu-id="3da5a-108">Then, the file is locked during the actual append process to ensure the integrity of the data being written to the file.</span></span>

<span data-ttu-id="3da5a-109">En este ejemplo no se usan transacciones.</span><span class="sxs-lookup"><span data-stu-id="3da5a-109">This example does not use transactions.</span></span> <span data-ttu-id="3da5a-110">Si usaba operaciones de transacción, solo podría tener acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3da5a-110">If you were using transacted operations, you would only be able have read-only access.</span></span> <span data-ttu-id="3da5a-111">En este caso, solo verá los datos anexados después de que se complete la operación de confirmación de la transacción.</span><span class="sxs-lookup"><span data-stu-id="3da5a-111">In this case, you would only see the appended data after the transaction commit operation completed.</span></span>

<span data-ttu-id="3da5a-112">En el ejemplo también se muestra que la aplicación abre dos archivos mediante [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):</span><span class="sxs-lookup"><span data-stu-id="3da5a-112">The example also shows that the application opens two files by using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):</span></span>

-   <span data-ttu-id="3da5a-113">One.txt se abre para lectura.</span><span class="sxs-lookup"><span data-stu-id="3da5a-113">One.txt is opened for reading.</span></span>
-   <span data-ttu-id="3da5a-114">Two.txt se abre para escritura y lectura compartida.</span><span class="sxs-lookup"><span data-stu-id="3da5a-114">Two.txt is opened for writing and shared reading.</span></span>

<span data-ttu-id="3da5a-115">A continuación, la aplicación usa [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) para anexar el contenido de One.txt al final de Two.txt mediante la lectura y escritura de los bloques de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="3da5a-115">Then the application uses [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) to append the contents of One.txt to the end of Two.txt by reading and writing the 4 KB blocks.</span></span> <span data-ttu-id="3da5a-116">Sin embargo, antes de escribir en el segundo archivo, la aplicación usa [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) para establecer el puntero del segundo archivo al final de ese archivo y usa [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) para bloquear el área que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="3da5a-116">However, before writing to the second file, the application uses [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) to set the pointer of the second file to the end of that file, and uses [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) to lock the area to be written.</span></span> <span data-ttu-id="3da5a-117">Esto impide que otro subproceso o proceso con un identificador duplicado tenga acceso al área mientras la operación de escritura está en curso.</span><span class="sxs-lookup"><span data-stu-id="3da5a-117">This prevents another thread or process with a duplicate handle from accessing the area while the write operation is in progress.</span></span> <span data-ttu-id="3da5a-118">Cuando se completa cada operación de escritura, se usa [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) para desbloquear el área bloqueada.</span><span class="sxs-lookup"><span data-stu-id="3da5a-118">When each write operation is complete, [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) is used to unlock the locked area.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void main()
{
  HANDLE hFile;
  HANDLE hAppend;
  DWORD  dwBytesRead, dwBytesWritten, dwPos;
  BYTE   buff[4096];

  // Open the existing file.

  hFile = CreateFile(TEXT("one.txt"), // open One.txt
            GENERIC_READ,             // open for reading
            0,                        // do not share
            NULL,                     // no security
            OPEN_EXISTING,            // existing file only
            FILE_ATTRIBUTE_NORMAL,    // normal file
            NULL);                    // no attr. template

  if (hFile == INVALID_HANDLE_VALUE)
  {
     printf("Could not open One.txt."); 
     return;
  }

  // Open the existing file, or if the file does not exist,
  // create a new file.

  hAppend = CreateFile(TEXT("two.txt"), // open Two.txt
              FILE_APPEND_DATA,         // open for writing
              FILE_SHARE_READ,          // allow multiple readers
              NULL,                     // no security
              OPEN_ALWAYS,              // open or create
              FILE_ATTRIBUTE_NORMAL,    // normal file
              NULL);                    // no attr. template

  if (hAppend == INVALID_HANDLE_VALUE)
  {
     printf("Could not open Two.txt."); 
     return;
  }

  // Append the first file to the end of the second file.
  // Lock the second file to prevent another process from
  // accessing it while writing to it. Unlock the
  // file when writing is complete.

  while (ReadFile(hFile, buff, sizeof(buff), &dwBytesRead, NULL)
      && dwBytesRead > 0)
    {
    dwPos = SetFilePointer(hAppend, 0, NULL, FILE_END);
    LockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    WriteFile(hAppend, buff, dwBytesRead, &dwBytesWritten, NULL);
    UnlockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    }

  // Close both files.

  CloseHandle(hFile);
  CloseHandle(hAppend);
}
```



 

 



