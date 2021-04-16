---
description: Cada vez que un proceso crea o abre un objeto de directorio, recibe un identificador para el objeto.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Identificadores de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669865"
---
# <a name="directory-handles"></a>Identificadores de directorio

Cada vez que un proceso crea o abre un objeto de directorio, recibe un identificador para el objeto.

Para obtener un identificador de un directorio existente, llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con la marca de **semántica de copia de \_ \_ seguridad \_ del marcador de archivo** .

Puede pasar un identificador de directorio a las siguientes funciones.



| Función                                                         | Descripción                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)                              | Realice una copia de seguridad de un archivo o directorio, incluida la información de seguridad.<br/>                                                                                      |
| [**BackupSeek**](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | Busca hacia delante en un flujo de datos al que se tiene acceso inicialmente mediante la función [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) o [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) .<br/> |
| [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | Restaure un archivo o directorio del que se realizó una copia de seguridad con [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).<br/>                                                             |
| [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | Recupera información de archivo para el archivo especificado.<br/>                                                                                                    |
| [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | Recupera el tamaño del archivo especificado, en bytes.<br/>                                                                                                   |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Recupera la fecha y la hora en que se creó un archivo o directorio, se obtuvo acceso por última vez y se modificó por última vez.<br/>                                                   |
| [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | Recupera el tipo de archivo del archivo especificado.<br/>                                                                                                        |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | Recupera información que describe los cambios en el directorio especificado.<br/>                                                                      |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Establece la fecha y la hora en que se creó el archivo o directorio especificado, se obtuvo acceso por última vez o se modificó por última vez.<br/>                                             |



 

 

