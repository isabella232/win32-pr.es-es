---
description: El sistema de archivos cifrado (EFS) proporciona protección criptográfica de archivos individuales en volúmenes del sistema de archivos NTFS mediante un sistema de clave pública.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Cifrado de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dbbfa82024bea13eab9e672b482ea18bc1051cd6e86b97d2a405351e3b078b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107575"
---
# <a name="file-encryption"></a>Cifrado de archivos

El sistema de archivos cifrado o EFS proporciona un nivel adicional de seguridad para los archivos y directorios. Proporciona protección criptográfica de archivos individuales en volúmenes del sistema de archivos NTFS mediante un sistema de clave pública.

Normalmente, el control de acceso a los objetos de archivos y directorios proporcionado por el modelo de seguridad Windows es suficiente para proteger el acceso no autorizado a información confidencial. Sin embargo, si se pierde o roba un equipo portátil que contiene datos confidenciales, la protección de seguridad de los datos puede verse comprometida. El cifrado de los archivos aumenta la seguridad.

Para determinar si un sistema de archivos admite el cifrado de archivos para archivos y directorios, llame a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examine la marca de bits **\_ FS FILE \_ ENCRYPTION.** Tenga en cuenta que los siguientes elementos no se pueden cifrar:

-   Archivos comprimidos
-   Archivos de sistema
-   Directorios del sistema
-   Directorios raíz
-   Transacciones

Los archivos dispersos se pueden cifrar.

TxF no admite la mayoría de las operaciones en archivos del sistema de archivos cifrados (EFS). Las únicas operaciones que admite TxF son las operaciones de lectura, como [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Control de archivos y directorios cifrados](handling-encrypted-files-and-directories.md)<br/> | El sistema de archivos NTFS cifra un archivo marcado como cifrado mediante el controlador de cifrado actual.<br/>                                                          |
| [Archivos cifrados y claves de usuario](encrypted-files-and-user-keys.md)<br/>                       | Enumera las funciones que se usarán para crear una clave, agregar una clave a un archivo cifrado, consultar las claves de un archivo cifrado y quitar claves de un archivo cifrado.<br/> |
| [Copia de seguridad y restauración de archivos cifrados](backup-and-restore-of-encrypted-files.md)<br/>       | Las funciones de cifrado sin formato habilitan la copia de seguridad de archivos cifrados.<br/>                                                                                                |



 

Para obtener más información sobre el cifrado, vea [Adding Users to an Encrypted File](adding-users-to-an-encrypted-file.md).

Para obtener más información sobre la criptografía, vea [Cryptography](/windows/desktop/SecCrypto/cryptography-portal).

 

