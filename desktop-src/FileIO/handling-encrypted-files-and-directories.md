---
description: Un archivo marcado como cifrado está cifrado mediante el sistema de archivos NTFS mediante el controlador de cifrado actual.
ms.assetid: 166bfb8c-b97d-4cc7-bf6b-399837cb8ad0
title: Administrar archivos y directorios cifrados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2718656a28eb678c10076e228e08a2a95cabd1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002862"
---
# <a name="handling-encrypted-files-and-directories"></a>Administrar archivos y directorios cifrados

Un programador o un usuario puede marcar un directorio o un archivo como cifrado. Un archivo marcado como cifrado está cifrado mediante el sistema de archivos NTFS mediante el controlador de cifrado actual. Si en una fecha posterior el archivo se marca como no cifrado, se descifrará y quedará en un estado de texto sin formato (no seguro).

Los directorios no se cifran a sí mismos. En su lugar, de forma predeterminada, en un directorio "cifrado", todos los archivos nuevos del directorio se cifran durante la creación. Un usuario debe cambiar específicamente el estado de un nuevo archivo a descifrado si el usuario no desea cifrar el archivo. Un directorio cifrado está visible. Para hacer que un directorio sea inaccesible para otros usuarios, use los métodos estándar de control de acceso.

Las funciones de cifrado no se pueden usar con la [API de copia de seguridad](/windows/desktop/Backup/backup).

Para cifrar un archivo nuevo, utilice la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con la marca de **atributo de archivo \_ \_ cifrada** . Para cifrar un archivo existente, utilice la función [**EncryptFile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) . Se cifran todas las secuencias de datos del archivo. Si el archivo ya está cifrado, **EncryptFile** no realiza ninguna acción, pero devuelve un valor distinto de cero, que indica que la operación se ha realizado correctamente. Si el archivo está comprimido, **EncryptFile** descomprime el archivo antes de cifrarlo.

Para descifrar un archivo cifrado, use la función [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) . Si el archivo no está cifrado, **DecryptFile** no realiza ninguna acción, pero devuelve un valor distinto de cero que indica que se ha realizado correctamente.

La función [**EncryptionDisable**](/windows/desktop/api/WinEfs/nf-winefs-encryptiondisable) deshabilita o habilita el cifrado del directorio indicado y los archivos que hay en él. No afecta al cifrado de subdirectorios por debajo del directorio indicado.

Para recuperar el estado de cifrado de un archivo, use la función [**FileEncryptionStatus**](/windows/desktop/api/WinBase/nf-winbase-fileencryptionstatusa) . Como alternativa, llame a la función [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) y examine el atributo de archivo de la marca **\_ \_ cifrada** en el valor devuelto.

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) y [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) intentan cifrar el archivo de destino con las claves utilizadas en el cifrado del archivo de origen. Si esto no se puede hacer, ambas funciones intentan cifrar el archivo de destino con las claves predeterminadas. Si no se puede hacer ninguno de estos métodos, **CopyFile** y **CopyFileEx** generan un error de **\_ cifrado \_** erróneo. Si desea que **CopyFileEx** complete la operación de copia incluso cuando no se pueda cifrar el archivo de destino, incluya la marca de **destino de archivo de copia \_ \_ permitir \_ descifrado \_** en el valor del parámetro *dwCopyFlags* en la llamada a **CopyFileEx**.

 

 
