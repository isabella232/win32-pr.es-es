---
description: Código de ejemplo que muestra cómo una aplicación puede anexar un archivo al final de otro archivo, incluido cómo abrir y cerrar archivos, leer y escribir en archivos, y bloquear y desbloquear archivos.
ms.assetid: e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5
title: Anexar un archivo a otro archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585521c1d0bb85c41806ba83c2c0940dc3523035731279d4da3f06af45334984
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766235"
---
# <a name="appending-one-file-to-another-file"></a>Anexar un archivo a otro archivo

En el ejemplo de código de este tema se muestra cómo abrir y cerrar archivos, leer y escribir en archivos, y bloquear y desbloquear archivos.

En el ejemplo, la aplicación anexa un archivo al final de otro archivo. En primer lugar, la aplicación abre el archivo que se anexa con permisos que solo permiten que la aplicación escriba en él. Sin embargo, durante el proceso de anexar, otros procesos pueden abrir el archivo con permiso de solo lectura, lo que proporciona una vista de instantánea del archivo que se va a anexar. A continuación, el archivo se bloquea durante el proceso de anexado real para garantizar la integridad de los datos que se escriben en el archivo.

En este ejemplo no se usan transacciones. Si usara operaciones de transacción, solo podría tener acceso de solo lectura. En este caso, solo verá los datos anexados una vez completada la operación de confirmación de la transacción.

En el ejemplo también se muestra que la aplicación abre dos archivos mediante [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):

-   One.txt se abre para lectura.
-   Two.txt se abre para escritura y lectura compartida.

A continuación, la aplicación usa [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) para anexar el contenido de One.txt al final de Two.txt al leer y escribir los bloques de 4 KB. Sin embargo, antes de escribir en el segundo archivo, la aplicación usa [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) para establecer el puntero del segundo archivo al final de ese archivo y usa [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) para bloquear el área que se va a escribir. Esto evita que otro subproceso o proceso con un identificador duplicado acceda al área mientras la operación de escritura está en curso. Cuando se completa cada operación de escritura, [**se usa UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) para desbloquear el área bloqueada.


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



 

 



