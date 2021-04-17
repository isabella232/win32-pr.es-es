---
description: El sistema de archivos cifrados (EFS) proporciona protección criptográfica de archivos individuales en volúmenes del sistema de archivos NTFS mediante un sistema de clave pública.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Cifrado de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c05d8d746e597fe180feffe25f7f553819e822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688468"
---
# <a name="file-encryption"></a>Cifrado de archivos

El sistema de archivos cifrado, o EFS, proporciona un nivel de seguridad adicional para los archivos y directorios. Proporciona protección criptográfica de archivos individuales en volúmenes del sistema de archivos NTFS mediante un sistema de clave pública.

Normalmente, el control de acceso a los objetos de archivo y directorio proporcionados por el modelo de seguridad de Windows es suficiente para proteger el acceso no autorizado a la información confidencial. Sin embargo, si se pierde o se roba un equipo portátil que contiene datos confidenciales, la protección de la seguridad de los datos puede verse comprometida. El cifrado de los archivos aumenta la seguridad.

Para determinar si un sistema de archivos admite el cifrado de archivos para archivos y directorios, llame a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examine la marca de bits de **\_ \_ cifrado de archivos FS** . Tenga en cuenta que los siguientes elementos no se pueden cifrar:

-   Archivos comprimidos
-   Archivos de sistema
-   Directorios del sistema
-   Directorios raíz
-   Transacciones

Los archivos dispersos se pueden cifrar.

TxF no admite la mayoría de las operaciones en archivos del sistema de archivos cifrados (EFS). Las únicas operaciones TxF admiten operaciones de lectura, como [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Administrar archivos y directorios cifrados](handling-encrypted-files-and-directories.md)<br/> | Un archivo marcado como cifrado está cifrado mediante el sistema de archivos NTFS mediante el controlador de cifrado actual.<br/>                                                          |
| [Archivos cifrados y claves de usuario](encrypted-files-and-user-keys.md)<br/>                       | Enumera las funciones que se van a usar para crear una nueva clave, agregar una clave a un archivo cifrado, consultar las claves de un archivo cifrado y quitar las claves de un archivo cifrado.<br/> |
| [Copia de seguridad y restauración de archivos cifrados](backup-and-restore-of-encrypted-files.md)<br/>       | Las funciones de cifrado sin procesar permiten realizar copias de seguridad de archivos cifrados.<br/>                                                                                                |



 

Para obtener más información sobre el cifrado, vea [Agregar usuarios a un archivo cifrado](adding-users-to-an-encrypted-file.md).

Para obtener más información sobre la criptografía, vea [Criptografía](/windows/desktop/SecCrypto/cryptography-portal).

 

