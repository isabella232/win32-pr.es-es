---
description: Las funciones de cifrado sin formato habilitan la copia de seguridad de archivos cifrados.
ms.assetid: 00f9b00e-305d-4554-8b43-7061228c92c3
title: Copia de seguridad y restauración de archivos cifrados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34308dbfc0f67a1fcf9a70f1f7a5878434018494fa1450d308fa493af78226ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766185"
---
# <a name="backup-and-restore-of-encrypted-files"></a>Copia de seguridad y restauración de archivos cifrados

El Sistema de cifrado de archivos (EFS) filtra la apertura de un archivo cifrado de forma que la aplicación que abrió el archivo obtenga acceso a la información sin cifrar, siempre que tenga las credenciales adecuadas para acceder al archivo y obtener la clave necesaria para descifrar el archivo. Las operaciones de lectura posteriores en este archivo darán como resultado texto sin cifrar. Esto es muy deseable para el acceso típico a los archivos cifrados y mantiene el cifrado y descifrado de los archivos transparentes. Sin embargo, esto dificulta la copia de seguridad de archivos cifrados, ya que si se intenta realizar la copia de seguridad con las llamadas de E/S de archivo estándar como [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)y [**WriteFile,**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)los archivos de los que se ha hecho una copia de seguridad serán la versión de texto sin formato.

Las funciones de cifrado sin formato se proporcionan para resolver este problema. Las aplicaciones de copia de seguridad son un usuario destinado principalmente a estas funciones. Las funciones de cifrado sin procesar difieren de otras funciones del sistema de archivos en que las funciones de apertura, lectura y escritura permiten el acceso a los flujos de datos cifrados sin procesar y también permiten la lectura y escritura de la secuencia $EFS datos. Por lo tanto, el autor de la llamada de las funciones de cifrado sin formato no necesita acceso a las claves criptográficas que descifran el archivo. Las siguientes API de cifrado sin formato están disponibles para su uso con aplicaciones de copia de seguridad y restauración: 

| API de cifrado sin formato                                     | Descripción                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)   | Abra un archivo cifrado con acceso a los datos en formato cifrado. Si el autor de la llamada no tiene acceso a la clave del archivo, el autor de la llamada necesita [SeBackupPrivilege](/windows/desktop/SecAuthZ/authorization-constants) para exportar archivos cifrados o SeRestorePrivilege para importar archivos cifrados. |
| [**CloseEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-closeencryptedfileraw) | Cierre de un archivo cifrado abierto con [ **OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)                                                                                                                                                                                      |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)   | Leer un archivo cifrado dejando sus datos en formato cifrado                                                                                                                                                                                                                   |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw) | Escritura de un archivo cifrado dejando sus datos en formato cifrado                                                                                                                                                                                                                  |
| [**ImportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_import_func)               | Devolución de llamada definida por la aplicación para su uso [ **con WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw)                                                                                                                                                                              |
| [**ExportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_export_func)               | Devolución de llamada definida por la aplicación para su uso [ **con ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)                                                                                                                                                                                |



 

 

 
