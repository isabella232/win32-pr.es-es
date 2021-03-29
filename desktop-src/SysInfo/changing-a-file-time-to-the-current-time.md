---
description: En el ejemplo siguiente se establece la hora de la última escritura para un archivo en la hora actual del sistema mediante la función SetFileTime.
ms.assetid: b4a70c01-d5ce-47e8-9918-9c9176894240
title: Cambiar una hora de archivo a la hora actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3d4b6189514196c5f8a332c259da9f8f8d7417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003209"
---
# <a name="changing-a-file-time-to-the-current-time"></a>Cambiar una hora de archivo a la hora actual

En el ejemplo siguiente se establece la hora de la última escritura para un archivo en la hora actual del sistema mediante la función [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) .

El sistema de archivos NTFS almacena los valores de hora en formato UTC, por lo que no se ven afectados por los cambios en la zona horaria o el horario de verano. El sistema de archivos FAT almacena valores de hora basados en la hora local del equipo.

El archivo se debe abrir con la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) mediante el \_ \_ acceso a los atributos de escritura de archivo.


```C++
#include <windows.h>

// SetFileToCurrentTime - sets last write time to current system time
// Return value - TRUE if successful, FALSE otherwise
// hFile  - must be a valid file handle

BOOL SetFileToCurrentTime(HANDLE hFile)
{
    FILETIME ft;
    SYSTEMTIME st;
    BOOL f;

    GetSystemTime(&st);              // Gets the current system time
    SystemTimeToFileTime(&st, &ft);  // Converts the current system time to file time format
    f = SetFileTime(hFile,           // Sets last-write time of the file 
        (LPFILETIME) NULL,           // to the converted current system time 
        (LPFILETIME) NULL, 
        &ft);    

    return f;
}
```



 

 
