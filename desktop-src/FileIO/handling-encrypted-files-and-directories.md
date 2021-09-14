---
description: El sistema de archivos NTFS cifra un archivo marcado como cifrado mediante el controlador de cifrado actual.
ms.assetid: 166bfb8c-b97d-4cc7-bf6b-399837cb8ad0
title: Control de archivos y directorios cifrados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2718656a28eb678c10076e228e08a2a95cabd1fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069934"
---
# <a name="handling-encrypted-files-and-directories"></a>Control de archivos y directorios cifrados

Un programador o usuario puede marcar un directorio o archivo como cifrado. El sistema de archivos NTFS cifra un archivo marcado como cifrado mediante el controlador de cifrado actual. Si más adelante el archivo se marca como no cifrado, se descifra y se deja en un estado de texto sin formato (no seguro).

Los directorios no se cifran por sí mismos. En su lugar, de forma predeterminada, en un directorio "cifrado", todos los archivos nuevos del directorio se cifran en la creación. Un usuario debe cambiar específicamente el estado de un nuevo archivo a descifrado si el usuario no desea que se cifra el archivo. Un directorio cifrado está visible. Para que otros usuarios no puedan acceder a un directorio, use los métodos estándar de control de acceso.

Las funciones de cifrado no se pueden usar con la [API de copia de seguridad](/windows/desktop/Backup/backup).

Para cifrar un nuevo archivo, use la [**función CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con la **marca FILE ATTRIBUTE \_ \_ ENCRYPTED.** Para cifrar un archivo existente, use la [**función EncryptFile.**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) Todos los flujos de datos del archivo están cifrados. Si el archivo ya está cifrado, **EncryptFile** no hace nada, pero devuelve un valor distinto de cero, lo que indica que se ha hecho correctamente. Si el archivo está comprimido, **EncryptFile** descomprime el archivo antes de cifrarlo.

Para descifrar un archivo cifrado, use la [**función DecryptFile.**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) Si el archivo no está cifrado, **DecryptFile** no hace nada, pero devuelve un valor distinto de cero que indica que se ha hecho correctamente.

La [**función EncryptionDisable**](/windows/desktop/api/WinEfs/nf-winefs-encryptiondisable) deshabilita o habilita el cifrado del directorio indicado y los archivos que contiene. No afecta al cifrado de subdirectorios por debajo del directorio indicado.

Para recuperar el estado de cifrado de un archivo, use la [**función FileEncryptionStatus.**](/windows/desktop/api/WinBase/nf-winbase-fileencryptionstatusa) Como alternativa, llame a [**la función GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) y examine la marca **FILE ATTRIBUTE \_ \_ ENCRYPTED** en el valor devuelto.

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) y [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) intentan cifrar el archivo de destino con las claves usadas en el cifrado del archivo de origen. Si esto no se puede hacer, ambas funciones intentan cifrar el archivo de destino con claves predeterminadas. Si no se pueden realizar ambos métodos, **CopyFile** y **CopyFileEx** producirán un **error ERROR ENCRYPTION \_ \_ FAILED.** Si desea que **CopyFileEx** complete la operación de copia incluso cuando no se pueda cifrar el archivo de destino, incluya la marca **COPY FILE ALLOW \_ \_ \_ DECRYPTED \_ DESTINATION** en el valor del parámetro *dwCopyFlags* en la llamada a **CopyFileEx**.

 

 
