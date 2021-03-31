---
description: Las funciones de cifrado sin procesar permiten realizar copias de seguridad de archivos cifrados.
ms.assetid: 00f9b00e-305d-4554-8b43-7061228c92c3
title: Copia de seguridad y restauración de archivos cifrados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbc5d1babbbbb92cef9e78f9a0dade702fd63d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082285"
---
# <a name="backup-and-restore-of-encrypted-files"></a>Copia de seguridad y restauración de archivos cifrados

El Sistema de cifrado de archivos (EFS) filtra la apertura de un archivo cifrado de forma que la aplicación que abre el archivo obtiene acceso a la información sin cifrar, siempre que tenga las credenciales adecuadas para tener acceso al archivo y obtener la clave necesaria para descifrar el archivo. Las operaciones de lectura posteriores en este archivo producirán texto sin cifrar. Esto es muy conveniente para el acceso típico a los archivos cifrados y mantiene el cifrado y descifrado de los archivos de forma transparente. Sin embargo, impide la copia de seguridad de archivos cifrados, ya que si se intenta realizar una copia de seguridad con las llamadas de e/s de archivos estándar como [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)y [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), los archivos de los que se ha realizado una copia de seguridad serán la versión de texto sin formato.

Las funciones de cifrado sin formato se proporcionan para solucionar este problema. Las aplicaciones de copia de seguridad son un usuario principal previsto para estas funciones. Las funciones de cifrado sin formato se diferencian de otras funciones del sistema de archivos en que las funciones Open, Read y Write permiten el acceso a los flujos de datos cifrados sin procesar y también permiten la lectura y escritura de la secuencia de $EFS. Por lo tanto, el autor de la llamada de las funciones de cifrado sin formato no necesita tener acceso a las claves criptográficas que descifran el archivo. Las siguientes API de cifrado sin procesar están disponibles para su uso con aplicaciones de copia de seguridad y restauración: 

| API de cifrado sin formato                                     | Descripción                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)   | Abra un archivo cifrado con acceso a los datos en formato cifrado. Si el autor de la llamada no tiene acceso a la clave del archivo, el autor de la llamada necesita [SeBackupPrivilege](/windows/desktop/SecAuthZ/authorization-constants) para exportar los archivos cifrados o SeRestorePrivilege para importar los archivos cifrados. |
| [**CloseEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-closeencryptedfileraw) | Cerrar un archivo cifrado abierto con [ **OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)                                                                                                                                                                                      |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)   | Leer un archivo cifrado y mantener sus datos en formato cifrado                                                                                                                                                                                                                   |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw) | Escribir un archivo cifrado y mantener sus datos en formato cifrado                                                                                                                                                                                                                  |
| [**ImportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_import_func)               | Devolución de llamada definida por la aplicación para su uso con [ **WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw)                                                                                                                                                                              |
| [**ExportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_export_func)               | Devolución de llamada definida por la aplicación para su uso con [ **ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)                                                                                                                                                                                |



 

 

 
