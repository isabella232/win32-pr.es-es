---
description: A continuación se indican sugerencias para interoperar correctamente con diversas características de seguridad y del sistema de archivos que se introdujeron en Windows Vista y Windows Server 2008.
ms.assetid: 3e8a1fd2-59e5-4f18-aafc-0ce5ac1e1cfa
title: Trabajar con el sistema de archivos y las características de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12903599beb7ed153965f4b803ad8147fd32067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154323"
---
# <a name="working-with-file-system-and-security-features"></a>Trabajar con el sistema de archivos y las características de seguridad

A continuación se indican sugerencias para interoperar correctamente con diversas características de seguridad y del sistema de archivos que se introdujeron en Windows Vista y Windows Server 2008.

## <a name="interoperability-with-transactions"></a>Interoperabilidad con transacciones

Para admitir transacciones, VSS garantiza que el administrador de transacciones de kernel (KTM) y el Coordinador de transacciones distribuidas (DTC) estén inmovilizados antes de la creación de instantáneas de volumen. Si el sistema no puede inmovilizar o reanudar KTM o DTC, los siguientes errores de tiempo de espera pueden ser devueltos por el método [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) :

<dl> \_tiempo de \_ \_ espera de inmovilización de transacción de VSS E \_  
\_tiempo de \_ \_ espera de reanudación de transacción de VSS E \_  
</dl>

Si el solicitante recibe uno de estos códigos de error, debe reintentar la creación de la instantánea.

También se pueden realizar transacciones al registro y a las operaciones del sistema de archivos. En el caso del registro, el sistema de escritura del registro es responsable de garantizar la coherencia transaccional. En el caso de las operaciones del sistema de archivos NTFS (TxF) transaccionales, el proveedor del sistema es responsable de garantizar la coherencia transaccional. Esto se consigue montando la instantánea como de lectura/escritura una vez creada para permitir la recuperación automática. Durante la fase de recuperación automática, KTM revierte las transacciones incompletas.

## <a name="identifying-and-creating-hard-links"></a>Identificación y creación de vínculos físicos

Al realizar copias de seguridad de archivos, una aplicación de copia de seguridad debe identificar todos los vínculos físicos de cada archivo para evitar realizar una copia de seguridad del mismo archivo más de una vez. Hay disponibles dos nuevas funciones para enumerar vínculos físicos: [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) y [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew).

Del mismo modo, al restaurar archivos, la aplicación de copia de seguridad debe restaurar los vínculos físicos mediante la función [**CreateHardLink**](/windows/win32/api/winbase/nf-winbase-createhardlinka) .

Las aplicaciones de copia de seguridad también deben validar el privilegio de nombre de copia de seguridad de SE \_ \_ durante la fase de copia de seguridad y el nombre de restauración de se \_ \_ durante la fase de restauración.

## <a name="permissions-and-privileges-required-by-backup-applications"></a>Permisos y privilegios necesarios para las aplicaciones de copia de seguridad

Las aplicaciones de copia de seguridad que restauran archivos del sistema requieren los privilegios siguientes:

<dl> nombre de copia de seguridad de SE \_ \_  
nombre de la restauración de SE \_ \_  
\_nombre de seguridad de se \_  
SE \_ toma \_ \_ el nombre de propiedad  
</dl>

Las aplicaciones de copia de seguridad también deben solicitar \_ derechos de acceso de propietario de escritura durante la fase de restauración.

## <a name="windows-media-digital-rights-management"></a>Rights Management digital de Windows Media

El cliente de Windows Media Digital Rights Management (DRM) mantiene un directorio de archivos de estado confidencial y de licencia en el directorio% ProgramData% \\ Microsoft \\ Windows \\ DRM. Los archivos de este directorio se deben purgar al mismo tiempo que los archivos temporales y de caché. Para asegurarse de que el cliente DRM de Windows permanece en un estado coherente, debe evitar la copia de seguridad o la restauración de estos archivos. Este directorio aparece en la clave del registro FilesNotToBackup. Para obtener más información acerca de la clave FilesNotToBackup, consulte [generar un conjunto de copia de seguridad](generating-a-backup-set.md).

## <a name="user-account-control"></a>Control de cuentas de usuario

La introducción de control de cuentas de usuario (UAC) en Windows Vista significa que, a menos que se especifique lo contrario, las aplicaciones deben ejecutarse en una cuenta de usuario estándar. Además, la característica de virtualización de archivos y del registro de UAC modifica las ubicaciones donde se almacenan los datos de usuario. Para obtener más información sobre cómo trabajar con UAC y la virtualización del registro y de archivos, vea las siguientes referencias:

<dl>

[Caso de desarrollador de Windows Vista y Windows Server 2008: requisitos de desarrollo de aplicaciones de Windows Vista para el control de cuentas de usuario (UAC)](/previous-versions/aa905330(v=msdn.10))  
[Requisitos de desarrollo de aplicaciones de Windows Vista para la compatibilidad de control de cuentas de usuario](/previous-versions/dotnet/articles/bb530410(v=msdn.10))  
[Revisión de control de cuentas de usuario (UAC)](../msi/user-account-control--uac--patching.md)  
</dl>

## <a name="bitlocker-drive-encryption"></a>Cifrado BitLocker de unidades

Cifrado de unidad BitLocker es una característica nueva de Windows Vista Enterprise, Windows Vista Ultimate y Windows Server 2008 que ofrece un inicio seguro y un cifrado de volumen completo. Comprender esta característica es importante para los desarrolladores de aplicaciones de copia de seguridad que realizan restauraciones sin conexión en las que es posible que sea necesario restaurar los datos en una unidad cifrada.

Para restaurar los datos en una unidad cifrada, siga estos pasos:

1.  Desbloquee la unidad.
2.  Desactive Cifrado de unidad BitLocker.
3.  Lleve a cabo la restauración.
4.  Arranque en el sistema operativo restaurado y Active Cifrado de unidad BitLocker.

Para obtener información detallada acerca de Cifrado de unidad BitLocker, incluida una guía paso a paso, consulte [cifrado de unidad BitLocker](https://www.microsoft.com/technet/windowsvista/security/bitlockr.mspx) en el sitio web de Microsoft TechNet Windows Vista. Para obtener información acerca del proveedor de Cifrado de unidad BitLocker WMI, consulte [cifrado de unidad BitLocker Provider](../secprov/bitlocker-drive-encryption-provider.md).

 

 
