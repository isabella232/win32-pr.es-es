---
description: 'Nota: este tema solo se aplica a Windows Server 2003 R2 y Windows Server 2003 con Service Pack 1 (SP1).'
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: Copia de seguridad y restauración del estado del sistema en Windows Server 2003 R2 y Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2fdb50e3f719a5208c2894f5659f927bcc922d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002951"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a>Copia de seguridad y restauración del estado del sistema en Windows Server 2003 R2 y Windows Server 2003 SP1

> [!Note]  
> Este tema solo se aplica a Windows Server 2003 R2 y Windows Server 2003 con Service Pack 1 (SP1). Para obtener información acerca de otras versiones de sistema operativo, consulte [copia de seguridad y restauración del estado del sistema](locating-additional-system-files.md).

 

> [!Note]  
> Microsoft no proporciona soporte técnico para desarrolladores o profesionales de TI para implementar restauraciones de estado del sistema en línea en Windows (todas las versiones). Para obtener información sobre el uso de las API y los procedimientos proporcionados por Microsoft para implementar restauraciones de estado del sistema en línea, consulte los recursos de la comunidad disponibles en [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).

 

Al realizar una copia de seguridad o restauración de VSS, el estado del sistema de Windows se define como una colección de varios elementos clave del sistema operativo y sus archivos. Estos elementos se deben tratar siempre mediante operaciones de copia de seguridad y restauración como una unidad.

En Windows Server 2003 R2 y Windows Server 2003 con SP1, no hay ninguna API de Windows diseñada para tratar estos objetos como uno, por lo que se recomienda que los solicitantes tengan su propio objeto de estado del sistema para que puedan procesar estos componentes de una manera coherente.

Dado que VSS se ejecuta en versiones de Windows en las que [*protección de archivos del sistema*](vssgloss-s.md) (WFP) protege los archivos de estado del sistema de daños, se necesitan pasos especiales para realizar copias de seguridad y restaurar el estado del sistema.

El estado del sistema consta de lo siguiente:

-   Todos los archivos protegidos por WFP, archivos de arranque, como NTLDR, Ntdetect y configuraciones de contador de rendimiento
-   El Active Directory (ADSI) (en los sistemas que son controladores de dominio)
-   La carpeta de volumen del sistema (SYSVOL) replicada por el servicio de replicación de archivos (FRS) (en sistemas que son controladores de dominio)
-   Servidor de certificados (en sistemas que proporcionan una entidad de certificación)
-   Base de datos de clúster (en sistemas que son un nodo de un clúster de Windows)
-   Servicio del Registro
-   Base de datos de registro de clase COM+

Se puede realizar una copia de seguridad del estado del sistema en cualquier orden.

Sin embargo, la restauración del estado del sistema debe reemplazar primero los archivos de arranque y confirmar la sección del sistema (Hive) del registro como último paso del proceso y puede producirse en el siguiente orden:

1.  Restaure los archivos de arranque.
2.  Base de datos de registro de clase COM+
3.  Restaure SYSVOL, el servidor de certificados y las bases de datos de clúster (si es necesario).
4.  Restaure Active Directory (si es necesario).
5.  Restaure el registro.

Algunos servicios del sistema, como la entidad de certificación, tienen escritores de VSS convencionales y siguen los algoritmos de copia de seguridad y restauración de VSS. Otros, como el registro, requieren operaciones personalizadas de copia de seguridad o restauración; para obtener más información, consulte [copias de seguridad y restauraciones personalizadas](custom-backups-and-restores.md).

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a>Copias de seguridad y restauraciones de VSS de archivos de arranque y del sistema

Se debe realizar una copia de seguridad y restaurar los archivos de sistema y de arranque solo como una entidad única.

Un solicitante puede usar de forma segura las versiones de instantáneas de estos archivos, y debe asegurarse de que el volumen del sistema y el dispositivo de arranque son [*instantáneas*](vssgloss-s.md).

Los archivos de sistema y de arranque incluyen:

-   Los archivos de arranque principales: <dl> NtLdr.exe  
    Boot.ini  
    NtDetect.com  
    NtBootDD.sys (si existe)  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> % SystemRoot% \\ system32 \\ CatRoot \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE} </dl>
-   Todos los archivos protegidos por [*protección de archivos del sistema*](vssgloss-s.md) y enumerados por [**SFCGETNEXTPROTECTEDFILE**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (vea VSS restore Operations of WFP Protected files) -   The performance Counter Configuration Files: <dl> % SystemRoot% \\ system32 \\ Perf? 00?. incrementa  
    % SystemRoot% \\ system32 \\ Perf? 00?. Bak </dl>
-   Si está presente, el archivo de la metabase de Internet Information Server (IIS) debe incluirse en las operaciones de copia de seguridad y restauración, ya que contiene el estado utilizado por Microsoft Exchange y otras aplicaciones de red. Este archivo se encuentra en: <dl> % SystemRoot% \\ system32 \\ InetSrv \\ metabase. bin </dl>
-   Si se realiza una copia de seguridad del archivo de metabase de IIS, las claves para permitir que las aplicaciones lean ciertas entradas cifradas deben restaurarse como parte del estado del sistema. Los archivos pueden encontrarse en: <dl> % SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*  
    % AllUsersProfile% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\* </dl>
-Al realizar copias de seguridad de los archivos de arranque y del sistema, puede ser necesario determinar el dispositivo de arranque de dos haciendo lo siguiente: 1. Busque la partición del sistema en **HKEY \_ local \_ Machine** \\ **System** \\ **setup** \\ **SystemPartition**.
    2.  Pasar la variable de entorno raíz del sistema (% SystemRoot%) al administrador de montaje para obtener el nombre del dispositivo NT.

## <a name="vss-restore-operations-of-wfp-protected-files"></a>Operaciones de restauración de VSS de archivos protegidos con WFP

El servicio WFP está diseñado para evitar la sustitución accidental o por etapas de los archivos del sistema. Por lo tanto, es necesario llevar a cabo pasos especiales para restaurar los datos de WFP.

Lo que significa que el escritor de WFP debe especificar el método de restauración de la restauración **\_ \_ de RME en el \_ \_ reinicio** al definir su documento de metadatos del escritor. Si un solicitante determina que el escritor de WFP no ha podido especificar este método de restauración, indica un error del escritor.

Un solicitante debe implementar un método de restauración de la **restauración de RME de VSS en el \_ \_ \_ \_ reinicio** mediante la función de Win32 [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) con el parámetro de **retardo de MOVEFILE \_ hasta el \_ \_ reinicio** para reemplazar los archivos del sistema. Los archivos restaurados no se copian en los directorios de archivos del sistema reales hasta después del reinicio del sistema. La sobrescritura de archivos de sistema protegidos solo se producirá si el valor de la siguiente entrada de registro de **reg \_ Word** está establecido en 1:

**HKEY \_ \_** \\ **Sistema del** equipo local \\ **CurrentControlSet** \\ **control** \\ **Session Manager** \\ **AllowProtectedRenames** = 1

Este valor debe establecerse antes que cualquier arranque en el que los archivos protegidos se reemplacen a través de [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) y se elimine después del reinicio.

También se debe hacer una copia de seguridad o restaurar el directorio dllcache del sistema, con copias de seguridad y restauración del volumen de arranque, y se encuentra examinando la entrada del registro **\_ \_ Expand de reg** :

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **SfcDllCache**<dl> <dt>

                  Data type
</dt> <dd>                  REG \_ expandir \_ SZ</dd> </dl>

El contenido del directorio dllcache del sistema se vuelve a generar con el comprobador de archivos de sistema (SFC) desde el símbolo del sistema:

-   La opción **/scanonce** examina todos los archivos protegidos en el siguiente arranque del sistema.
-   La opción **/scannow** examina inmediatamente todos los archivos protegidos.

Se examinarán todos los archivos protegidos, y las versiones que no sean válidas se reemplazarán en el directorio y en la ubicación de dllcache.

Hay cuatro archivos que forman parte de la WFP que no se pueden restaurar con los archivos WFP:

<dl> Ctl3dv2.dll  
DtcSetup.exe  
NtDll.dll  
Smss.exe  
</dl>

Estos archivos ayudan en el proceso de restauración de los archivos WFP y, como tal, hay una dependencia circular. Actualmente, no hay ninguna manera de restaurar estos archivos excepto reinstalar Windows.

 

 
