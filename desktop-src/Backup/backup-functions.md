---
title: Funciones de copia de seguridad
description: Las siguientes funciones se usan con la copia de seguridad en cinta.
ms.assetid: 8c5f92f7-4918-475c-bc86-2b02291488d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2164958d7261c4c22caf1ac5124f524eca2f7ed355b082bede59d66a2e6fe697
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529615"
---
# <a name="backup-functions"></a>Funciones de copia de seguridad

Las siguientes funciones se usan con la copia [de seguridad en cinta](tape-backup.md).



| Función                                           | Descripción                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread)                   | Lee los datos asociados a un archivo o directorio especificados en un búfer.                                |
| [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek)                   | Busca hacia delante en un flujo de datos.                                                                        |
| [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)                 | Escribe un flujo de datos de un búfer en un archivo o directorio especificado.                                |
| [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) | Cambia el formato de una cinta.                                                                                      |
| [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape)                     | Borra todo o parte de una cinta.                                                                          |
| [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)     | Recupera información que describe la cinta o la unidad de cinta.                                       |
| [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition)         | Recupera la dirección actual de la cinta.                                                             |
| [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)             | Determina si el dispositivo de cinta está listo para procesar los comandos de cinta.                                  |
| [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape)                 | Prepara la cinta a la que se va a acceder o quitar.                                                           |
| [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)     | Especifica el tamaño de bloque de una cinta o configura el dispositivo de cinta.                                      |
| [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition)         | Establece la posición de cinta en el dispositivo especificado.                                                        |
| [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark)             | Escribe un número especificado de marcas de archivo, marcas de conjunto, marcas de archivo cortas o marcas de archivo largas en un dispositivo de cinta. |



 

Se proporcionan las siguientes funciones para trabajar con el almacén [de instancia única y la copia de seguridad de SIS.](single-instance-store-and-sis-backup.md)



| Función                                                          | Descripción                                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**SisCreateBackupStructure**](siscreatebackupstructure.md)      | Crea la estructura de copia de seguridad de SIS especificada basándose en la información proporcionada.                      |
| [**SisCreateRestoreStructure**](siscreaterestorestructure.md)    | Crea la estructura de restauración de SIS especificada basándose en la información proporcionada.                     |
| [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)    | Devuelve información que describe los archivos de almacenamiento común a los que apunta el vínculo de SIS especificado.            |
| [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)          | Libera la memoria asignada por las funciones de LA API de SIS.                                                       |
| [**SisFreeBackupStructure**](sisfreebackupstructure.md)          | Libera la estructura de copia de seguridad de SIS especificada.                                                          |
| [**SisFreeRestoreStructure**](sisfreerestorestructure.md)        | Libera la estructura de restauración de SIS especificada.                                                         |
| [**SisRestoredCommon StoreFile**](sisrestoredcommonstorefile.md) | Informa a la arquitectura de SIS de que se ha escrito un archivo de almacén común.                         |
| [**SisRestoredLink**](sisrestoredlink.md)                        | Devuelve los nombres del archivo de almacenamiento común o los archivos a los que apunta el vínculo de SIS restaurado especificado. |



 

Se proporcionan las siguientes funciones para trabajar con la copia [de seguridad y restauración de archivos cifrados.](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)



| Función                                                | Descripción                                                                                |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CloseEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw) | Cierre un archivo cifrado abierto con [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa). |
| [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)   | Abra un archivo cifrado con acceso a los datos en formato cifrado.                            |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw)   | Lee un archivo cifrado y deja sus datos en formato cifrado.                               |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw) | Escriba un archivo cifrado dejando sus datos en formato cifrado.                              |



 

 

 