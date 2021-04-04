---
title: Crear una aplicación de copia de seguridad
description: Para realizar la entrada o salida en una cinta, una aplicación de copia de seguridad debe obtener primero un identificador del dispositivo de cinta. En el ejemplo de código siguiente se muestra cómo utilizar la función CreateFile para abrir un dispositivo de cinta.
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- copia de seguridad de aplicaciones copias de seguridad
- crear copias de seguridad de aplicaciones de copia de seguridad
- copia de seguridad, crear aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77409a0c74ee61e333b92dad8b22d9c68ed92eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078122"
---
# <a name="creating-a-backup-application"></a>Crear una aplicación de copia de seguridad

Para realizar la entrada o salida en una cinta, una aplicación de copia de seguridad debe obtener primero un identificador del dispositivo de cinta. En el ejemplo de código siguiente se muestra cómo utilizar la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un dispositivo de cinta.


```C++
HANDLE hTape;   // handle to tape device
 
hTape = CreateFile(TEXT("\\\\.\\TAPE0"),         // tape dev to open
                   GENERIC_READ | GENERIC_WRITE, // read/write access
                   0,                            // not used
                   0,                            // not used
                   OPEN_EXISTING,                // req for tape devs
                   0,                            // not used
                   NULL);                        // not used
```



Para hacer una copia de seguridad de un árbol de directorios en una cinta, una aplicación debe usar las funciones [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) y [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) para atravesar el árbol de directorios. Cada vez que se encuentra un archivo, la aplicación debe obtener los atributos de archivo mediante la función [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) .

Si hay vínculos físicos, una aplicación debe determinar el número de vínculos y guardar el identificador único del archivo en una tabla para futuras comparaciones. La primera vez que se encuentra un archivo, la aplicación debe usar [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir el archivo y la función [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) para iniciar la copia de seguridad. Después, puede usar la función [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) repetidamente para transferir toda la información del búfer usado por **BackupRead** a la cinta. La segunda vez que se encuentra un archivo (comprobada en la tabla de identificadores de archivos cuando hay vínculos físicos), la aplicación puede escribir la información de archivo General en la cinta, seguida de una secuencia que tiene un identificador que es un **\_ vínculo de copia de seguridad**.

Al restaurar archivos de cinta a disco, una aplicación debe usar las funciones [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)y [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) . Para cada archivo de una cinta, la aplicación debe usar **CreateFile** para crear un nuevo archivo en el disco y **BackupWrite** para empezar a restaurar el archivo. A continuación, la aplicación debe usar **readfile** varias veces hasta que toda la información del archivo se lea desde la cinta en el búfer rellenado por **BackupWrite**.

Si una de las secuencias en el búfer de [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) tiene un identificador de flujo de **\_ vínculo de copia de seguridad** , la aplicación debe establecer un vínculo físico. Si los datos necesarios para establecer el vínculo no existen, se produce un error en **BackupWrite** . La aplicación puede utilizar un catálogo existente previamente para buscar y restaurar los datos originales, o puede notificar al usuario que los datos de archivo que se van a restaurar están en una ubicación diferente.

 

 