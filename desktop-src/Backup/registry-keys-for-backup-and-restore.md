---
title: Claves y valores del Registro para copias de seguridad y restauración
ms.assetid: 83449f78-cca1-449b-8c5f-3c8a91c8b3e7
description: 'Más información sobre: Claves y valores del Registro para copias de seguridad y restauración'
keywords:
- copia de seguridad de copia de seguridad, claves del Registro
- Copia de seguridad de claves del Registro
- Copia de seguridad de CustomPerformanceSettings
- DisableMonitoring Backup
- Copia de seguridad de FilesNotToBackup
- FilesNotToSnapshot Backup
- Copia de seguridad de KeysNotToRestore
- Copia de seguridad de LastInstance
- Copia de seguridad de LastRestoreId
- Copia de seguridad de MaxShadowCopies
- Copia de seguridad de MinDiffAreaFileSize
- OverallPerformanceSetting Backup
- Copia de seguridad de SYSVOL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7058378561072bdc0f51abb455c098a22a9ad5e
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386794"
---
# <a name="registry-keys-and-values-for-backup-and-restore"></a>Claves y valores del Registro para copias de seguridad y restauración

Las aplicaciones que solicitan o realizan operaciones de copia de seguridad y restauración deben usar las siguientes claves y valores del Registro para comunicarse entre sí o con características como [Servicio de instantáneas de volumen (VSS)](/windows/desktop/VSS/volume-shadow-copy-service-portal) y Copias de seguridad de Windows:

-   [CustomPerformanceSettings](#customperformancesettings)
-   [DisableMonitoring](#disablemonitoring)
-   [FilesNotToBackup](#filesnottobackup)
-   [FilesNotToSnapshot](#filesnottosnapshot)
-   [IdleTimeout](#idletimeout)
-   [KeysNotToRestore](#keysnottorestore)
-   [LastInstance](#lastinstance)
-   [LastRestoreId](#lastrestoreid)
-   [MaxShadowCopies](#maxshadowcopies)
-   [MinDiffAreaFileSize](#mindiffareafilesize)
-   [OverallPerformanceSetting y CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings)
-   [SYSVOL](#sysvol)

## <a name="customperformancesettings"></a>CustomPerformanceSettings

Vea [OverallPerformanceSetting y CustomPerformanceSettings.](#overallperformancesetting-and-customperformancesettings)

## <a name="disablemonitoring"></a>DisableMonitoring

En las plataformas cliente de Windows a partir de Windows 7, se solicita automáticamente a los usuarios que configuren la característica Copias de seguridad de Windows si aún no lo han hecho. Estas notificaciones aparecen en el momento de inicio del equipo, empezando siete días después de instalar el sistema operativo. También aparecen cuando el usuario conecta una unidad de disco duro; En este caso, las notificaciones aparecen inmediatamente.

Los OEM y desarrolladores de aplicaciones de copia de seguridad de terceros pueden usar el valor del Registro **DisableMonitoring** para desactivar estas notificaciones automáticas.

Este valor no existe de forma predeterminada, por lo que debe crearse en la siguiente clave del Registro:

**HKEY \_ SOFTWARE DE \_ MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsBackup**

El **valor del Registro DisableMonitoring** tiene el tipo de datos REG \_ DWORD y se interpreta como sigue:

-   Si los datos del valor se establecen en 1 y los usuarios aún no han configurado la característica Copias de seguridad de Windows, las notificaciones automáticas se desactivarán. Si ya hay una notificación automática en el Centro de acciones, al establecer este valor del Registro, la notificación se quitará a las 10:00 de la mañana siguiente.
-   Si el valor no existe, si sus datos no están establecidos o si sus datos están establecidos en cero, las notificaciones automáticas no se desactivarán.

**Windows Vista y Windows XP:** No se admite este valor del Registro.

## <a name="filesnottobackup"></a>FilesNotToBackup

La **clave del Registro FilesNotToBackup** especifica los nombres de los archivos y directorios que las aplicaciones de copia de seguridad no deben realizar copias de seguridad ni restaurar. Cada una de las entradas de esta clave es una cadena REG \_ MULTI SZ en el formato \_ siguiente:

\[ \] Unidad \[ *Ruta de acceso* \] \\ *FileName* \[ /s\]

-   *Unidad* especifica la unidad y es opcional. Por ejemplo, c:. Para especificar todas las unidades, use una barra diagonal inversa ( \\ ); no se necesitan letras de unidad.
-   *Path* especifica la ruta de acceso y es opcional. No puede contener caracteres comodín.
-   *FileName* especifica el archivo o directorio y es necesario. Puede contener caracteres comodín.
-   /s especifica que se van a incluir todos los subdirectorios de la ruta de acceso especificada.
-   Las variables de entorno como %Systemroot% se pueden sustituir por toda la cadena o parte de esta.

En la tabla siguiente se muestran algunas entradas típicas.

| Nombre de la entrada                             | Valor predeterminado                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| Internet Explorer                      | Archivos temporales                                                                           |
| Archivo de página de memoria                       | \\Pagefile.sys                                                                            |
| MS Coordinador de transacciones distribuidas | C: \\ Sistema de \\ Windows32 \\ MSDtc \\ MSDTC. LOG C: \\ Windows \\ system32 \\ MSDtc \\ trace \\ dtctrace.log |
| Archivos sin conexión cache                    | %Systemroot% \\ CSC \\ \* /s                                                                  |
| Administración de energía                       | \\hiberfil.sys                                                                            |
| Almacenamiento de instancia única                | \\SIS Common Store \\ \* . \* /s                                                              |
| Archivos temporales                        | %TEMP% \\ \* /s                                                                             |



 

> [!Note]  
> Las aplicaciones que realizan copias de seguridad de nivel de volumen generalmente lo hacen copiando todo el volumen en el nivel de bloque, por lo que no pueden respetar la clave del Registro **FilesNotToBackup** en el momento de la copia de seguridad. En su lugar, esperan hasta el tiempo de restauración para eliminar los archivos de los que no se va a realizar una copia de seguridad. En la mayoría de los casos, se trata de una estrategia razonable. Sin embargo, en el caso de los archivos de almacenamiento de instancia única, los archivos del Almacén común de SIS no deben eliminarse en el momento de la restauración.

 

En el caso de las copias de seguridad de volúmenes de nivel de bloque, Copias de seguridad de Windows Server y la utilidad Wbadmin de Windows respetan la clave del Registro **FilesNotToBackup** mediante la eliminación de los archivos adecuados en tiempo de restauración. Restaurar sistema y copia de seguridad del estado del sistema no respetan la clave del Registro **FilesNotToBackup.**

**Windows XP:** Restaurar sistema respeta la clave del Registro **FilesNotToBackup.**

## <a name="filesnottosnapshot"></a>FilesNotToSnapshot

VSS admite la **clave del Registro FilesNotToSnapshot.** Las aplicaciones y los servicios pueden usar esta clave para especificar los archivos que se eliminarán de las instantáneas recién creadas. Para obtener más información, vea [Excluir archivos de instantáneas.](/windows/desktop/VSS/excluding-files-from-shadow-copies)

**Windows Server 2003 y Windows XP:** No se admite esta clave del Registro.

En el caso de las copias de seguridad de volúmenes de nivel de bloque, Copias de seguridad de Windows Server respeta la clave del Registro **FilesNotToSnapshot** mediante la eliminación de los archivos adecuados en tiempo de restauración.

## <a name="idletimeout"></a>IdleTimeout

El **valor del Registro IdleTimeout** especifica la cantidad de tiempo, en segundos, que el servicio VSS esperará cuando esté inactivo. Si se alcanza este valor de tiempo de espera y no hay ninguna tarea que realizar, el servicio VSS se cerrará.

Este valor del Registro se puede encontrar en la siguiente clave del Registro:

**HKEY \_ Configuración \_ de** \\  \\ VSS del sistema de MÁQUINA LOCAL **CurrentControlSet** \\  \\  \\ **Services**

Si este valor del Registro no existe:

-   El valor de tiempo de espera real que se usa es de 180 segundos (3 minutos) de forma predeterminada.
-   Puede crear un valor con el nombre **IdleTimeout** y el tipo DWORD y establecerlo en el valor deseado.

Si este valor del Registro se establece en 0 segundos:

-   El valor de tiempo de espera real que se usa es de 180 segundos (3 minutos).

Si establece este valor del Registro:

-   VSS usa el valor de tiempo de espera establecido.
-   Puede especificar cualquier valor entre 1 y FFFFFFFF segundos. Sin embargo, se recomienda elegir un valor entre 1 y 180 segundos.

**Windows Server 2003 y Windows XP:** No se admite esta clave del Registro.

## <a name="keysnottorestore"></a>KeysNotToRestore

La **clave del Registro KeysNotToRestore** especifica los nombres de las subclaves del Registro y los valores que las aplicaciones de copia de seguridad no deben restaurar. Para obtener más información, [vea KeysNotToRestore](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10)). No es necesario respetar la clave del Registro **KeysNotToRestore.**

**Windows Server 2003 y Windows XP:** Debe respetar la clave **del Registro KeysNotToRestore.**

En el caso de las copias de seguridad de volúmenes de nivel de bloque, Copias de seguridad de Windows Server la clave del Registro **KeysNotToRestore** mediante la eliminación de los archivos adecuados en el momento de la restauración.

Copia de seguridad de estado del sistema respeta la clave del Registro **KeysNotToRestore.**

## <a name="lastinstance"></a>LastInstance

El valor del Registro **LastInstance** indica que se ha realizado una operación de restauración sin sistema operativo y que los volúmenes se han sobrescrito pero no tienen formato. Para obtener más información, vea [Using VSS Automated Recuperación del sistema for Disaster Recovery](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery).

**Windows Server 2003 y Windows XP:** No se admite este valor del Registro.

## <a name="lastrestoreid"></a>LastRestoreId

Cuando una aplicación de copia de seguridad realiza una restauración del estado del sistema, debe indicar que lo ha hecho estableciendo el valor del Registro **LastRestoreId.** En este caso, "Restauración de estado del sistema" hace referencia a cualquier restauración que restaure de forma selectiva los archivos binarios y los controladores del sistema operativo.

Si todo el volumen de arranque y del sistema se restauran en el nivel de volumen, no se debe establecer este valor.

Si el **valor del Registro LastRestoreId** no existe, la aplicación de copia de seguridad debe crearlo con la siguiente clave del Registro:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **BackupRestore** \\ **SystemStateRestore**

Cree un valor con el nombre **LastRestoreId** y escriba REG \_ SZ. El valor debe ser un valor opaco único, como un GUID.

Cada vez que se realiza una nueva restauración del estado del sistema, la aplicación de copia de seguridad debe cambiar los datos **del valor LastRestoreId.**

Otras aplicaciones que necesitan supervisar las restauraciones de estado del sistema deben almacenar los datos de este valor del Registro. Estos datos se pueden comparar con los datos actuales del valor del Registro **LastRestoreId** para determinar si se ha realizado una nueva restauración del estado del sistema.

**Windows Vista, Windows Server 2003 y Windows XP:** Este valor del Registro no se admite hasta Windows Vista con Service Pack 1 (SP1) y Windows Server 2008.

## <a name="maxshadowcopies"></a>MaxShadowCopies

El **valor del Registro MaxShadowCopies** [](/windows/desktop/VSS/vssgloss-c) especifica el número máximo de instantáneas accesibles para el cliente que se pueden almacenar en cada volumen del equipo. Una instantánea accesible desde el cliente es una instantánea que se crea mediante el valor ACCESIBLE DE **CLIENTE DE VSS \_ CTX \_ \_** de la [**\_ enumeración SNAPSHOT \_ CONTEXT \_ de VSS.**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context) La característica Instantáneas para carpetas compartidas usa las instantáneas accesibles para el cliente. Para obtener más información sobre las instantáneas, vea la [documentación de VSS.](/windows/desktop/VSS/volume-shadow-copy-service-portal)

Si el valor del Registro **MaxShadowCopies** no existe, la aplicación de copia de seguridad puede crearlo con la siguiente clave del Registro:

**HKEY \_ Configuración \_ de** \\  \\ VSS de LOCAL MACHINE System **CurrentControlSet** \\ **Services** \\  \\ 

Cree un valor con el nombre **MaxShadowCopies y** escriba DWORD. Los datos predeterminados para este valor son 64. El mínimo es 1. El máximo es 512.

> [!Note]  
> Para otros tipos de instantáneas, no hay ningún valor del Registro que se corresponda con **MaxShadowCopies.** El número máximo de instantáneas es 512 por volumen.

 

**Nota**  La **opción MaxShadowCopies se** admite en Windows Server 2003 o versiones posteriores.

**Windows Server 2003:** En los servidores de clúster, es posible que los datos del valor del Registro **MaxShadowCopies** deba establecerse en un número inferior. Para obtener más información, vea "Cuando se usa el Servicio de instantáneas de volumen en equipos basados en Windows Server 2003 que ejecutan muchas operaciones de E/S, los volúmenes de disco tardan más tiempo en estar en línea" en la página ayuda y soporte Knowledge Base en [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058) .

**Windows XP:** No se admite este valor del Registro.

## <a name="mindiffareafilesize"></a>MinDiffAreaFileSize

[VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) asigna un área de almacenamiento de instantáneas (o "área de diferencias") para almacenar datos para instantáneas. El tamaño mínimo del área de almacenamiento de instantáneas es una configuración por equipo que se puede especificar mediante el valor del Registro **MinDiffAreaFileSize.**

Si no se establece el valor del Registro **MinDiffAreaFileSize,** el tamaño mínimo del área de almacenamiento de instantáneas es de 32 MB para los volúmenes que son menores que 500 MB y 320 MB para los volúmenes mayores de 500 MB.

**Windows Server 2008, Windows Server 2003 con SP1 y Windows Vista:** Si no se establece el valor del Registro **MinDiffAreaFileSize,** el área de almacenamiento de instantáneas tiene un tamaño mínimo de 300 MB. Si se establece el valor del Registro **MinDiffAreaFileSize,** sus datos deben estar entre 300 MB y 3000 MB (3 GB) y deben ser un múltiplo de 300 MB.

**Windows Server 2003:** Si no se establece el valor del Registro **MinDiffAreaFileSize,** el tamaño mínimo del área de almacenamiento de instantáneas es de 100 MB.

**Windows XP:** No se admite este valor del Registro.

Si el valor del Registro **MinDiffAreaFileSize** no existe, la aplicación de copia de seguridad puede crearlo con la siguiente clave del Registro:

**HKEY \_ Sistema \_ LOCAL MACHINE** \\  \\ **CurrentControlSet** \\ **Services** \\ **VolSnap**

Cree un valor con el nombre **MinDiffAreaFileSize** y escriba REG \_ DWORD. Los datos de esta clave se especifican en megabytes. 320 es igual a 320 MB y 3200 es igual a 3,2 GB. Debe especificar un número que sea un múltiplo de 32. Si especifica un valor que no es un múltiplo de 32, se usará el múltiplo siguiente de 32.

Es posible que las instantáneas no funcionen correctamente si el valor del Registro **MinDiffAreaFileSize** especifica un tamaño mínimo mayor que el tamaño máximo del área de almacenamiento de instantáneas. Para especificar el tamaño máximo del área de almacenamiento de instantáneas, use el comando [Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) add shadowstorage o el comando Vssadmin resize shadowstorage. Para ver el tamaño máximo actual, use el comando shadowstorage de la [lista de vssadmin.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) Si no ha establecido un tamaño máximo, no hay ningún límite en la cantidad de espacio que se puede usar.

## <a name="overallperformancesetting-and-customperformancesettings"></a>OverallPerformanceSetting y CustomPerformanceSettings

Los valores del Registro **OverallPerformanceSetting** y **CustomPerformanceSettings** se usan para especificar la configuración de rendimiento Copias de seguridad de Windows Server. Estos valores del Registro solo se admiten en sistemas operativos Windows Server.

**Windows Server 2003:** Estos valores del Registro no se admiten.

Si estos valores del Registro no existen, la aplicación de copia de seguridad puede crearlos con la siguiente clave del Registro:

**HKEY \_ SOFTWARE DE \_ MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Copia de seguridad de nivel de bloque de Windows**

Para especificar la configuración de rendimiento de todos los volúmenes, cree un valor con el nombre **OverallPerformanceSetting** y escriba REG \_ DWORD. Los datos del valor deben establecerse en uno de los valores siguientes.

| Valor | Significado                                                                                                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Rendimiento normal de la copia de seguridad (mediante copias de seguridad completas). Esta configuración corresponde a la configuración Rendimiento de copia de seguridad normal que se describe en Optimización de la copia de [seguridad y el rendimiento del servidor.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))            |
| 2     | Rendimiento de copia de seguridad más rápido (mediante copias de seguridad incrementales). Esta configuración corresponde a la configuración Rendimiento de copia de seguridad más rápido que se describe en [Optimización de la copia de seguridad y el rendimiento del servidor.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))     |
| 3     | Rendimiento de copia de seguridad personalizado (especificando una configuración de rendimiento para cada volumen). Esta configuración corresponde a la configuración Personalizada que se describe en Optimización de la copia de [seguridad y el rendimiento del servidor.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)) |



 

Si establece **OverallPerformanceSetting** en 3, también debe especificar la configuración de rendimiento de cada volumen individualmente. Para ello, cree un valor con el nombre **CustomPerformanceSettings** y escriba REG \_ MULTI \_ SZ. Los datos de este valor deben establecerse de la siguiente manera:

-   Cada cadena de la secuencia \_ REG MULTI SZ de \_ cadenas contiene la configuración de un volumen.
-   Cada cadena consta de un GUID de volumen, seguido de una coma, seguido de un valor DWORD.
-   Cada uno de los valores DWORD es 1 (copia de seguridad completa) o 2 (copia de seguridad incremental).

Por ejemplo, suponga que el equipo tiene dos volúmenes como sigue:

-   Los dos volúmenes son C: \\ y D: \\ .
-   El GUID del volumen C: \\ es 07c473ca4-2df8-11de-9d80-806e6f6e6963 y el GUID del volumen D: \\ es 0ac22ea6c-712f-11de-adb0-00215a67606e.
-   Quiere especificar la perfornidad de copia de seguridad normal para el volumen C: y un rendimiento de copia de \\ seguridad más rápido para el volumen D: \\ .

Para ello, establecería **OverallPerformanceSetting** en 3 y **CustomPerformanceSettings** en "07c473ca4-2df8-11de-9d80-806e6f6e6963,1 \\ 00ac22ea6c-712f-11de-adb0-00215a67606e,2".

Si establece **OverallPerformanceSetting** en 1 o 2, se omiten los datos del valor **CustomPerformanceSettings.**

## <a name="sysvol"></a>SYSVOL

El **valor del Registro SYSVOL** es una manera de notificar al servicio Sistema de archivos distribuido Replication (DFSR) que se ha iniciado una operación de restauración del estado del sistema. Cualquier aplicación de copia de seguridad que realice la restauración del estado del sistema de SYSVOL debe usar este valor para indicar si la operación de restauración es autoritativa o no autenticativa. El servicio DFSR lee este valor. Si no se establece este valor, la restauración de SYSVOL se realiza de forma no autenticativa de forma predeterminada.

Si el **valor del Registro SYSVOL** no existe, la aplicación de copia de seguridad debe crearlo con la siguiente clave del Registro:

**HKEY \_ Sistema \_ DE MÁQUINA LOCAL** \\  \\ **CurrentControlSet** \\ **Services** \\ **Restauración DFSR** \\ 

Cree un valor con el nombre **SYSVOL y** escriba REG \_ SZ. Los datos del valor deben establecerse en "autoritativo" o "no autoritativo" en función de la solicitud del administrador del sistema.

**Windows Vista, Windows Server 2003 y Windows XP:** No se admite este valor del Registro.

 

 
