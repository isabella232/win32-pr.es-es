---
description: Cada vez que un proceso crea o abre un objeto de directorio, recibe un identificador para el objeto .
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Identificadores de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc8f983748154a781e5dd2923e0c3e3351a26acb47c2230d3142d6ad6444513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015224"
---
# <a name="directory-handles"></a>Identificadores de directorio

Cada vez que un proceso crea o abre un objeto de directorio, recibe un identificador para el objeto .

Para obtener un identificador para un directorio existente, llame a la [**función CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con la **marca FILE FLAG BACKUP \_ \_ \_ SEMANTICS.**

Puede pasar un identificador de directorio a las siguientes funciones.



| Función                                                         | Descripción                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)                              | Haga una copia de seguridad de un archivo o directorio, incluida la información de seguridad.<br/>                                                                                      |
| [**BackupSeek**](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | Busca hacia delante en un flujo de datos al que se accede inicialmente mediante la [**función BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) [**o BackupWrite.**](/windows/desktop/api/winbase/nf-winbase-backupwrite)<br/> |
| [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | Restaure un archivo o directorio del que se ha hecho una copia de seguridad [**mediante BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).<br/>                                                             |
| [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | Recupera la información del archivo especificado.<br/>                                                                                                    |
| [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | Recupera el tamaño del archivo especificado, en bytes.<br/>                                                                                                   |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Recupera la fecha y hora en que se creó un archivo o directorio, se tuvo acceso por última vez y se modificó por última vez.<br/>                                                   |
| [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | Recupera el tipo de archivo del archivo especificado.<br/>                                                                                                        |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | Recupera información que describe los cambios en el directorio especificado.<br/>                                                                      |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Establece la fecha y hora en que se creó el archivo o directorio especificado, se tuvo acceso por última vez o se modificó por última vez.<br/>                                             |



 

 

