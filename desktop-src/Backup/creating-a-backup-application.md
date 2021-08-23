---
title: Creación de una aplicación de copia de seguridad
description: Para realizar la entrada o salida en una cinta, una aplicación de copia de seguridad debe obtener primero un identificador del dispositivo de cinta. En el ejemplo de código siguiente se muestra cómo usar la función CreateFile para abrir un dispositivo de cinta.
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- Copia de seguridad de aplicaciones de copia de seguridad
- crear copias de seguridad de aplicaciones de copia de seguridad
- copia de seguridad de copia de seguridad, creación de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3086e51bce928b682d3e61518de29118abdc48461a77f79e48a4a4cb4b0f2c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529485"
---
# <a name="creating-a-backup-application"></a>Creación de una aplicación de copia de seguridad

Para realizar la entrada o salida en una cinta, una aplicación de copia de seguridad debe obtener primero un identificador del dispositivo de cinta. En el ejemplo de código siguiente se muestra cómo usar la [**función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un dispositivo de cinta.


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



Para realizar una copia de seguridad de un árbol de directorios en una cinta, una aplicación debe usar las funciones [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) y [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) para recorrer el árbol de directorios. Cada vez que se encuentra un archivo, la aplicación debe obtener los atributos de archivo mediante la [**función GetFileAttributes.**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa)

Si hay vínculos duros, una aplicación debe determinar el número de vínculos y guardar el identificador único del archivo en una tabla para futuras comparaciones. La primera vez que se encuentra un archivo, la aplicación debe usar [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir el archivo y la [**función BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) para iniciar la copia de seguridad. A continuación, puede usar [**la función WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) repetidamente para transferir toda la información del búfer que **usa BackupRead** a la cinta. La segunda vez que se encuentra un archivo (se comprueba con la tabla de identificadores de archivo cuando hay vínculos duros), la aplicación puede escribir la información general del archivo en la cinta, seguida de una secuencia que tiene un identificador que es **BACKUP \_ LINK**.

Al restaurar archivos de cinta en disco, una aplicación debe usar las funciones [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)y [**ReadFile.**](/windows/desktop/api/fileapi/nf-fileapi-readfile) Para cada archivo de una cinta, la aplicación debe usar **CreateFile** para crear un nuevo archivo en el disco y **BackupWrite** para empezar a restaurar el archivo. A continuación, la aplicación debe usar **ReadFile** repetidamente hasta que toda la información del archivo se lea de la cinta en el búfer rellenado **por BackupWrite**.

Si una de las secuencias del búfer [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) tiene un identificador de flujo **BACKUP \_ LINK,** la aplicación debe establecer un vínculo duro. Si los datos necesarios para establecer el vínculo no existen, Se produce un error **en BackupWrite.** La aplicación puede usar un catálogo preexistido para buscar y restaurar los datos originales, o bien puede notificar al usuario que los datos de archivo que se restaurarán se encuentra en una ubicación diferente.

 

 