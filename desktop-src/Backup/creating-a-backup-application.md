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
# <a name="creating-a-backup-application"></a><span data-ttu-id="1b14d-107">Crear una aplicación de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="1b14d-107">Creating a Backup Application</span></span>

<span data-ttu-id="1b14d-108">Para realizar la entrada o salida en una cinta, una aplicación de copia de seguridad debe obtener primero un identificador del dispositivo de cinta.</span><span class="sxs-lookup"><span data-stu-id="1b14d-108">To perform input or output on a tape, a backup application must first obtain a handle of the tape device.</span></span> <span data-ttu-id="1b14d-109">En el ejemplo de código siguiente se muestra cómo utilizar la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un dispositivo de cinta.</span><span class="sxs-lookup"><span data-stu-id="1b14d-109">The following code sample shows you how to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a tape device.</span></span>


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



<span data-ttu-id="1b14d-110">Para hacer una copia de seguridad de un árbol de directorios en una cinta, una aplicación debe usar las funciones [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) y [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) para atravesar el árbol de directorios.</span><span class="sxs-lookup"><span data-stu-id="1b14d-110">To back up a directory tree to a tape, an application must use the [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) functions to traverse the directory tree.</span></span> <span data-ttu-id="1b14d-111">Cada vez que se encuentra un archivo, la aplicación debe obtener los atributos de archivo mediante la función [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="1b14d-111">Each time a file is found, the application should get the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) function.</span></span>

<span data-ttu-id="1b14d-112">Si hay vínculos físicos, una aplicación debe determinar el número de vínculos y guardar el identificador único del archivo en una tabla para futuras comparaciones.</span><span class="sxs-lookup"><span data-stu-id="1b14d-112">If there are hard links, an application should determine the number of links, and save the unique identifier of the file in a table for future comparisons.</span></span> <span data-ttu-id="1b14d-113">La primera vez que se encuentra un archivo, la aplicación debe usar [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir el archivo y la función [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) para iniciar la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1b14d-113">The first time a file is found, the application should use [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open the file, and the [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) function to begin the backup.</span></span> <span data-ttu-id="1b14d-114">Después, puede usar la función [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) repetidamente para transferir toda la información del búfer usado por **BackupRead** a la cinta.</span><span class="sxs-lookup"><span data-stu-id="1b14d-114">Then it can use the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function repeatedly to transfer all the information in the buffer used by **BackupRead** to the tape.</span></span> <span data-ttu-id="1b14d-115">La segunda vez que se encuentra un archivo (comprobada en la tabla de identificadores de archivos cuando hay vínculos físicos), la aplicación puede escribir la información de archivo General en la cinta, seguida de una secuencia que tiene un identificador que es un **\_ vínculo de copia de seguridad**.</span><span class="sxs-lookup"><span data-stu-id="1b14d-115">The second time a file is found (checked against the table of file identifiers when there are hard links), the application can write the general file information to the tape, followed by a stream that has an identifier that is **BACKUP\_LINK**.</span></span>

<span data-ttu-id="1b14d-116">Al restaurar archivos de cinta a disco, una aplicación debe usar las funciones [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)y [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) .</span><span class="sxs-lookup"><span data-stu-id="1b14d-116">When restoring files from tape to disk, an application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite), and [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) functions.</span></span> <span data-ttu-id="1b14d-117">Para cada archivo de una cinta, la aplicación debe usar **CreateFile** para crear un nuevo archivo en el disco y **BackupWrite** para empezar a restaurar el archivo.</span><span class="sxs-lookup"><span data-stu-id="1b14d-117">For each file on a tape, the application should use **CreateFile** to create a new file on disk, and **BackupWrite** to begin restoring the file.</span></span> <span data-ttu-id="1b14d-118">A continuación, la aplicación debe usar **readfile** varias veces hasta que toda la información del archivo se lea desde la cinta en el búfer rellenado por **BackupWrite**.</span><span class="sxs-lookup"><span data-stu-id="1b14d-118">Then the application should use **ReadFile** repeatedly until all the information for the file is read from the tape into the buffer filled by **BackupWrite**.</span></span>

<span data-ttu-id="1b14d-119">Si una de las secuencias en el búfer de [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) tiene un identificador de flujo de **\_ vínculo de copia de seguridad** , la aplicación debe establecer un vínculo físico.</span><span class="sxs-lookup"><span data-stu-id="1b14d-119">If one of the streams in the [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) buffer has a **BACKUP\_LINK** stream identifier, the application must establish a hard link.</span></span> <span data-ttu-id="1b14d-120">Si los datos necesarios para establecer el vínculo no existen, se produce un error en **BackupWrite** .</span><span class="sxs-lookup"><span data-stu-id="1b14d-120">If the data needed to establish the link does not exist, **BackupWrite** fails.</span></span> <span data-ttu-id="1b14d-121">La aplicación puede utilizar un catálogo existente previamente para buscar y restaurar los datos originales, o puede notificar al usuario que los datos de archivo que se van a restaurar están en una ubicación diferente.</span><span class="sxs-lookup"><span data-stu-id="1b14d-121">The application can use a pre-existing catalog to locate and restore the original data, or it can notify the user that the file data to be restored is in a different location.</span></span>

 

 