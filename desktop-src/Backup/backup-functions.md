---
title: Funciones de copia de seguridad
description: Las siguientes funciones se usan con la copia de seguridad en cinta.
ms.assetid: 8c5f92f7-4918-475c-bc86-2b02291488d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312c7477c28f83b7c1c64073234799219346f89a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792838"
---
# <a name="backup-functions"></a>Funciones de copia de seguridad

Las siguientes funciones se usan con la [copia de seguridad en cinta](tape-backup.md).



| Función                                           | Descripción                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread)                   | Lee los datos asociados a un archivo o directorio especificado en un búfer.                                |
| [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek)                   | Busca hacia delante en un flujo de datos.                                                                        |
| [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)                 | Escribe una secuencia de datos de un búfer en un archivo o directorio especificado.                                |
| [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) | Cambiar el formato de una cinta.                                                                                      |
| [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape)                     | Borra todo o parte de una cinta.                                                                          |
| [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)     | Recupera información que describe la cinta o la unidad de cinta.                                       |
| [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition)         | Recupera la dirección actual de la cinta.                                                             |
| [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)             | Determina si el dispositivo de cinta está listo para procesar comandos de cinta.                                  |
| [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape)                 | Prepara la cinta a la que se va a tener acceso o quitar.                                                           |
| [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)     | Especifica el tamaño de bloque de una cinta o configura el dispositivo de cinta.                                      |
| [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition)         | Establece la posición de la cinta en el dispositivo especificado.                                                        |
| [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark)             | Escribe un número especificado de filemarks, setmarks, Short filemarks o Long filemarks en un dispositivo de cinta. |



 

Se proporcionan las siguientes funciones para trabajar con [el almacén de instancia única y la copia de seguridad de SIS](single-instance-store-and-sis-backup.md).



| Función                                                          | Descripción                                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**SisCreateBackupStructure**](siscreatebackupstructure.md)      | Crea la estructura de copia de seguridad de SIS especificada basándose en la información proporcionada.                      |
| [**SisCreateRestoreStructure**](siscreaterestorestructure.md)    | Crea la estructura de restauración de SIS especificada basándose en la información proporcionada.                     |
| [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)    | Devuelve información que describe los archivos de almacenamiento común a los que apunta el vínculo SIS especificado.            |
| [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)          | Libera memoria asignada por las funciones de la API de SIS.                                                       |
| [**SisFreeBackupStructure**](sisfreebackupstructure.md)          | Libera la estructura de copia de seguridad de SIS especificada.                                                          |
| [**SisFreeRestoreStructure**](sisfreerestorestructure.md)        | Libera la estructura de restauración de SIS especificada.                                                         |
| [**SisRestoredCommon StoreFile**](sisrestoredcommonstorefile.md) | Informa a la arquitectura de SIS de que se ha escrito un archivo de almacenamiento común.                         |
| [**SisRestoredLink**](sisrestoredlink.md)                        | Devuelve los nombres de los archivos de almacenamiento común a los que apunta el vínculo SIS restaurado especificado. |



 

Se proporcionan las siguientes funciones para trabajar con la [copia de seguridad y restauración de archivos cifrados](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).



| Función                                                | Descripción                                                                                |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CloseEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw) | Cierre un archivo cifrado abierto con [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa). |
| [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)   | Abra un archivo cifrado con acceso a los datos en formato cifrado.                            |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw)   | Leer un archivo cifrado y mantener sus datos en formato cifrado.                               |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw) | Escribir un archivo cifrado y mantener sus datos en formato cifrado.                              |



 

 

 