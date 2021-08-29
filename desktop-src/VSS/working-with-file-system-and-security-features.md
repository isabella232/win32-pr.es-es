---
description: A continuación se incluyen sugerencias para interoperar correctamente con diversas características de seguridad y sistema de archivos que se introdujeron en Windows Vista y Windows Server 2008.
ms.assetid: 3e8a1fd2-59e5-4f18-aafc-0ce5ac1e1cfa
title: Trabajar con características de seguridad y sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410f0e859d051e04ef18e26e57438e758785c29dae69295b57969afc7b4182f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124445"
---
# <a name="working-with-file-system-and-security-features"></a>Trabajar con características de seguridad y sistema de archivos

A continuación se incluyen sugerencias para interoperar correctamente con diversas características de seguridad y sistema de archivos que se introdujeron en Windows Vista y Windows Server 2008.

## <a name="interoperability-with-transactions"></a>Interoperabilidad con transacciones

Para admitir transacciones, VSS garantiza que tanto el Administrador de transacciones de kernel (KTM) como el Coordinador de transacciones distribuidas (DTC) se inmovilizan antes de la creación de instantáneas de volumen. Si el sistema no puede inmovilizar o descongelar KTM o DTC, el método [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) puede devolver los siguientes errores de tiempo de espera:

<dl> TIEMPO DE ESPERA \_ DE \_ INMOVILIZACIÓN \_ DE TRANSACCIONES VSS E \_  
TIEMPO DE ESPERA \_ DE \_ \_ THAW DE TRANSACCIÓN VSS \_ E  
</dl>

Si el solicitante recibe uno de estos códigos de error, debe reintentar la creación de instantáneas.

Las operaciones del registro y del sistema de archivos también se pueden realizar. En el caso del registro, el escritor del registro es responsable de garantizar la coherencia transaccional. En el caso de las operaciones del sistema de archivos NTFS transaccional (TxF), el proveedor del sistema es responsable de garantizar la coherencia transaccional. Esto se logra montando la instantánea como de lectura y escritura después de crearla para permitir la recuperación automática. Durante la fase de recuperación automática, KTM revierte las transacciones incompletas.

## <a name="identifying-and-creating-hard-links"></a>Identificación y creación de vínculos duros

Al realizar copias de seguridad de archivos, una aplicación de copia de seguridad debe identificar todos los vínculos duros a cada archivo para evitar hacer copias de seguridad del mismo archivo más de una vez. Hay dos nuevas funciones disponibles para enumerar vínculos duros: [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) y [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew).

Del mismo modo, al restaurar archivos, la aplicación de copia de seguridad debe restaurar vínculos duros mediante [**la función CreateHardLink.**](/windows/win32/api/winbase/nf-winbase-createhardlinka)

Las aplicaciones de copia de seguridad también deben SE el privilegio BACKUP NAME durante la fase de copia de seguridad y SE \_ RESTORE NAME durante la fase de \_ \_ \_ restauración.

## <a name="permissions-and-privileges-required-by-backup-applications"></a>Permisos y privilegios requeridos por las aplicaciones de copia de seguridad

Las aplicaciones de copia de seguridad que restauran archivos del sistema requieren los siguientes privilegios:

<dl> \_SE NOMBRE DE COPIA \_ DE SEGURIDAD  
\_SE RESTORE \_ NAME  
\_SE NOMBRE DE \_ SEGURIDAD  
\_SE TOMAR EL \_ NOMBRE DE \_ LA PROPIEDAD  
</dl>

Las aplicaciones de copia de seguridad también deben solicitar derechos de \_ acceso WRITE OWNER durante la fase de restauración.

## <a name="windows-media-digital-rights-management"></a>Windows Media Digital Rights Management

Windows El cliente de Rights Management digital multimedia (DRM) mantiene un directorio de archivos de estado confidencial y de licencia en el directorio %ProgramData% de \\ Microsoft \\ Windows \\ DRM. Los archivos de este directorio se deben purgar al mismo tiempo que los archivos temporales y de caché. Para asegurarse de que el Windows DRM permanece en un estado coherente, debe evitar la copia de seguridad o la restauración de estos archivos. Este directorio aparece en la clave del Registro FilesNotToBackup. Para obtener más información sobre la clave FilesNotToBackup, vea [Generar un conjunto de copia de seguridad.](generating-a-backup-set.md)

## <a name="user-account-control"></a>Control de cuentas de usuario

La introducción del Control de cuentas de usuario (UAC) en Windows Vista significa que, a menos que se especifique lo contrario, las aplicaciones deben ejecutarse con una cuenta de usuario estándar. Además, la característica de virtualización de archivos y registros de UAC modifica las ubicaciones donde se almacenan los datos de usuario. Para obtener más información sobre cómo trabajar con UAC y la virtualización de archivos y registros, consulte las siguientes referencias:

<dl>

[The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10))  
[Windows Requisitos de desarrollo de aplicaciones de Vista para la compatibilidad con el control de cuentas de usuario](/previous-versions/dotnet/articles/bb530410(v=msdn.10))  
[Revisión de Control de cuentas de usuario (UAC)](../msi/user-account-control--uac--patching.md)  
</dl>

## <a name="bitlocker-drive-encryption"></a>Cifrado BitLocker de unidades

Cifrado de unidad BitLocker es una nueva característica de Windows Vista Enterprise, Windows Vista Ultimate y Windows Server 2008 que ofrece un inicio seguro y cifrado de volumen completo. Comprender esta característica es importante para los desarrolladores de aplicaciones de copia de seguridad que realizan restauraciones sin conexión donde es posible que sea necesario restaurar los datos en una unidad cifrada.

Para restaurar datos en una unidad cifrada, realice los pasos siguientes:

1.  Desbloquee la unidad.
2.  Desactive la Cifrado de unidad BitLocker.
3.  Lleve a cabo la restauración.
4.  Arranque en el sistema operativo restaurado y active Cifrado de unidad BitLocker.

Para obtener información detallada sobre Cifrado de unidad BitLocker, incluida una guía paso [](https://www.microsoft.com/technet/windowsvista/security/bitlockr.mspx) a paso, consulte Cifrado de unidad BitLocker en el sitio web de Microsoft TechNet Windows Vista. Para obtener información sobre el Cifrado de unidad BitLocker WMI, vea [Cifrado de unidad BitLocker provider](../secprov/bitlocker-drive-encryption-provider.md).

 

 
