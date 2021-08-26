---
description: Nota Este tema solo se aplica a Windows Server 2003 R2 y Windows Server 2003 con Service Pack 1 (SP1).
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: Copia de seguridad y restauración del estado del sistema en Windows Server 2003 R2 y Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4803acc5981cc74084789064bd276baa28b35c0ffe225e49d2b65ba5485e51a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032955"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a>Copia de seguridad y restauración del estado del sistema en Windows Server 2003 R2 y Windows Server 2003 SP1

> [!Note]  
> Este tema solo se aplica a Windows Server 2003 R2 y Windows Server 2003 con Service Pack 1 (SP1). Para obtener información sobre otras versiones del sistema operativo, vea [Realizar copias de seguridad y restaurar el estado del sistema.](locating-additional-system-files.md)

 

> [!Note]  
> Microsoft no proporciona soporte técnico para desarrolladores ni profesionales de TI para implementar restauraciones de estado del sistema en línea Windows (todas las versiones). Para obtener información sobre el uso de api y procedimientos proporcionados por Microsoft para implementar restauraciones de estado del sistema en línea, consulte los recursos de la comunidad disponibles en [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).

 

Al realizar una copia de seguridad o restauración de VSS, Windows estado del sistema se define como una colección de varios elementos clave del sistema operativo y sus archivos. Estos elementos siempre deben tratarse mediante operaciones de copia de seguridad y restauración como una unidad.

En Windows Server 2003 R2 y Windows Server 2003 con SP1, no hay ninguna API de Windows diseñada para tratar estos objetos como uno, por lo que se recomienda que los solicitantes tengan su propio objeto de estado del sistema para que puedan procesar estos componentes de una manera coherente.

Dado que VSS se ejecuta en versiones de Windows donde [*Protección*](vssgloss-s.md) de archivos del sistema (WFP) protege los archivos de estado del sistema frente a daños, se necesitan pasos especiales para hacer copias de seguridad y restaurar el estado del sistema.

El estado del sistema consta de lo siguiente:

-   Todos los archivos protegidos por WFP, archivos de arranque incluidos ntldr, ntdetect y configuraciones de contadores de rendimiento
-   El Active Directory (ADSI) (en sistemas que son controladores de dominio)
-   La carpeta de volúmenes del sistema (SYSVOL) que replica el Servicio de replicación de archivos (FRS) (en sistemas que son controladores de dominio)
-   Servidor de certificados (en sistemas que proporcionan la entidad de certificación)
-   Base de datos de clúster (en sistemas que son un nodo de un clúster Windows clúster)
-   Servicio del Registro
-   Base de datos de registro de clases COM+

Se puede hacer una copia de seguridad del estado del sistema en cualquier orden.

Sin embargo, la restauración del estado del sistema debe reemplazar primero los archivos de arranque y confirmar la sección del sistema (hive) del registro como paso final del proceso y puede producirse en el orden siguiente:

1.  Restaure los archivos de arranque.
2.  Base de datos de registro de clases COM+
3.  Restaure sysvol, servidor de certificados y bases de datos de clúster (si es necesario).
4.  Restaurar Active Directory (si es necesario).
5.  Restaure el registro.

Algunos servicios del sistema, como la entidad de certificación, tienen escritores VSS convencionales y siguen los algoritmos de copia de seguridad y restauración de VSS. Otros, como el registro, requieren operaciones personalizadas de copia de seguridad o restauración. Para obtener más información, vea [Copias de seguridad y restauraciones personalizadas.](custom-backups-and-restores.md)

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a>Copias de seguridad y restauraciones de archivos de arranque y del sistema de VSS

Solo se debe realizar una copia de seguridad de los archivos de arranque y del sistema y restaurarse como una sola entidad.

Un solicitante puede usar de forma segura versiones de instantáneas de estos archivos y debe asegurarse de que el volumen del sistema y el dispositivo de arranque se [*copian en la sombra.*](vssgloss-s.md)

Los archivos de arranque y del sistema incluyen:

-   Los archivos de arranque principales: <dl> NtLdr.exe  
    Boot.ini  
    NtDetect.com  
    NtBootDD.sys (si está presente)  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> %SystemRoot% \\ System32 \\ CatRoot \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE} </dl>
-   Todos los archivos protegidos por [*La*](vssgloss-s.md) protección de archivos del sistema y enumerados por [**SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (vea Operaciones de restauración de VSS de archivos protegidos por WFP) Los archivos de configuración del contador -   de rendimiento: <dl> %SystemRoot% \\ System32 \\ Perf?00?. Dat  
    %SystemRoot% \\ System32 \\ Perf?00?. Bak </dl>
-Si está presente, el archivo de metabase de Internet Information Server (IIS) debe incluirse en las operaciones de copia de seguridad y restauración porque contiene el estado utilizado por Microsoft Exchange y otras aplicaciones de red. Este archivo se encuentra en: <dl> %SystemRoot% \\ System32 \\ InetSrv \\ Metabase.bin </dl>
-   Si se hace una copia de seguridad del archivo de metabase de IIS, las claves para permitir que las aplicaciones lean determinadas entradas cifradas se deben restaurar como parte del estado del sistema. Los archivos se pueden encontrar en: <dl> %SystemRoot% \\ System32 \\ Microsoft \\ Protect\\\*  
    %AllUsersProfile% \\ Microsoft Crypto RSA \\ \\ \\ MachineKeys\\\* </dl>
-Al realizar una copia de seguridad de los archivos de arranque y del sistema, puede que sea necesario determinar el dispositivo de arranque DOS haciendo lo siguiente: Buscar la partición del sistema en 1. **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **Setup** \\ **SystemPartition**.
    2.  Pase la variable de entorno Raíz del sistema (%SystemRoot%) al administrador de montaje para obtener el nombre del dispositivo NT.

## <a name="vss-restore-operations-of-wfp-protected-files"></a>Operaciones de restauración de VSS de archivos protegidos de WFP

El servicio WFP está diseñado para evitar el reemplazo accidental o por fragmentos de archivos del sistema. Por lo tanto, es necesario realizar pasos especiales para restaurar los datos de WFP.

Significa que el escritor WFP debe especificar el método de restauración RESTORE AT REBOOT de **VSS \_ RME \_ \_ \_** al definir su documento de metadatos del escritor. Si un solicitante determina que el escritor WFP no ha podido especificar este método de restauración, indica un error de escritor.

Un solicitante debe implementar un método de restauración de **VSS \_ RME \_ RESTORE AT \_ \_ REBOOT** mediante la función [**Win32 MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) con el parámetro **MOVEFILE DELAY UNTIL \_ \_ \_ REBOOT** para reemplazar los archivos del sistema. Los archivos restaurados no se copian en los directorios de archivos del sistema reales hasta después del reinicio del sistema. La sobrescritura de archivos del sistema protegidos solo se producirá si el valor de la siguiente entrada del Registro **REG \_ WORD** está establecido en 1:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** \\ **AllowProtectedRenames** = 1

Este valor debe establecerse antes de cualquier arranque en el que los archivos protegidos se van a reemplazar a través de [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) y se elimina después del reinicio.

También se debe realizar una copia de seguridad o restaurar el directorio dllcache del sistema, con copia de seguridad y restauración del volumen de arranque, y se encuentra examinando la entrada del Registro **REG \_ EXPAND \_ SZ:**

**HKEY \_ SOFTWARE \_ MÁQUINA LOCAL** \\  \\ **Microsoft** Windows \\ **NT** \\ **CurrentVersion** \\ **WinLogon** \\ **SfcDllCache**<dl> <dt>

                  Data type
</dt> <dd>                  REG \_ EXPAND \_ SZ</dd> </dl>

El contenido del directorio dllcache del sistema se recompila mediante el Comprobador de archivos de sistema (SFC) desde el símbolo del sistema:

-   La **opción /SCANONCE** examina todos los archivos protegidos en el siguiente arranque del sistema.
-   La **opción /SCANNOW** examina todos los archivos protegidos inmediatamente.

Se examinarán todos los archivos protegidos y todas las versiones que no sean válidas se reemplazarán tanto en el directorio como en la ubicación de dllcache.

Hay cuatro archivos que forman parte del WFP que no se pueden restaurar con los archivos WFP:

<dl> Ctl3dv2.dll  
DtcSetup.exe  
NtDll.dll  
Smss.exe  
</dl>

Estos archivos ayudan en el proceso de restauración de los archivos WFP y, como tal, hay una dependencia circular. Actualmente, no hay ninguna manera de restaurar estos archivos excepto volver a instalar Windows.

 

 
