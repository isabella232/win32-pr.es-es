---
title: Claves y valores del registro para copias de seguridad y restauración
ms.assetid: 83449f78-cca1-449b-8c5f-3c8a91c8b3e7
description: 'Más información acerca de: claves y valores del registro para copias de seguridad y restauración'
keywords:
- copia de seguridad, claves del registro
- Copia de seguridad de claves del registro
- Copia de seguridad de CustomPerformanceSettings
- Copia de seguridad de DisableMonitoring
- Copia de seguridad de FilesNotToBackup
- Copia de seguridad de FilesNotToSnapshot
- Copia de seguridad de KeysNotToRestore
- Copia de seguridad de LastInstance
- Copia de seguridad de LastRestoreId
- Copia de seguridad de MaxShadowCopies
- Copia de seguridad de MinDiffAreaFileSize
- Copia de seguridad de OverallPerformanceSetting
- Copia de seguridad de SYSVOL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9796ff96efbc20ac90de6d26a0c1bac7b17633
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153517"
---
# <a name="registry-keys-and-values-for-backup-and-restore"></a>Claves y valores del registro para copias de seguridad y restauración

Las aplicaciones que solicitan o realizan operaciones de copia de seguridad y restauración deben usar las siguientes claves y valores del registro para comunicarse entre sí o con características como el [servicio de instantáneas de volumen (VSS)](/windows/desktop/VSS/volume-shadow-copy-service-portal) y la copia de seguridad de Windows:

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

Vea [OverallPerformanceSetting y CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings).

## <a name="disablemonitoring"></a>DisableMonitoring

En las plataformas de cliente de Windows a partir de Windows 7, se solicita automáticamente a los usuarios que configuren la característica copia de seguridad de Windows si aún no lo han hecho. Estas notificaciones aparecen en el momento de inicio del equipo, empezando siete días después de instalar el sistema operativo. También aparecen cuando el usuario se conecta a una unidad de disco duro; en este caso, las notificaciones aparecen inmediatamente.

Los OEM y los desarrolladores de aplicaciones de copia de seguridad de terceros pueden usar el valor del registro **DisableMonitoring** para desactivar estas notificaciones automáticas.

Este valor no existe de forma predeterminada, por lo que se debe crear en la siguiente clave del registro:

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsBackup**

El valor del registro **DisableMonitoring** tiene el tipo de datos reg \_ DWORD y se interpreta de la siguiente manera:

-   Si los datos del valor se establecen en 1 y si los usuarios aún no han configurado la característica copia de seguridad de Windows, se desactivan las notificaciones automáticas. Si ya hay una notificación automática en el centro de actividades, el establecimiento de este valor del registro hace que la notificación se quite en 10:00 la mañana siguiente.
-   Si el valor no existe, si sus datos no están establecidos o si sus datos se establecen en cero, las notificaciones automáticas no se desactivan.

**Windows Vista y Windows XP:** No se admite este valor del registro.

## <a name="filesnottobackup"></a>FilesNotToBackup

La clave del registro **FilesNotToBackup** especifica los nombres de los archivos y directorios en los que las aplicaciones de copia de seguridad no deben realizar copias de seguridad ni restaurar. Cada una de las entradas de esta clave es una \_ cadena reg multi \_ SZ con el siguiente formato:

\[*Unidad de* \] \[ *Ruta de acceso* \] \\ *Nombre de archivo* \[ modificado\]

-   *Especifica la unidad y* es opcional. Por ejemplo, c:. Para especificar todas las unidades, use una barra diagonal inversa ( \) ; no se necesita ninguna letra de unidad.
-   *Path* especifica la ruta de acceso y es opcional. No puede contener caracteres comodín.
-   *Filename* especifica el archivo o directorio y es obligatorio. Puede contener caracteres comodín.
-   /s especifica que se incluirán todos los subdirectorios de la ruta de acceso especificada.
-   Las variables de entorno como% SystemRoot% se pueden sustituir por toda o parte de toda la cadena.

En la tabla siguiente se muestran algunas entradas típicas.

| Nombre de la entrada                             | Valor predeterminado                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| Internet Explorer                      | Archivos temporales                                                                           |
| Archivo de paginación de memoria                       | \\Pagefile.sys                                                                            |
| Coordinador de transacciones distribuidas MS | C: \\ Windows \\ system32 \\ MSDTC \\ MSDTC. REGISTRO C: \\ Windows \\ system32 \\ MSDtc \\ Trace \\ dtctrace. log |
| Caché de Archivos sin conexión                    | % SystemRoot% \\ CSC \\ \* /s                                                                  |
| Administración de energía                       | \\hiberfil.sys                                                                            |
| Almacenamiento de instancia única                | \\SIS Common Store \\ \* . \* /s                                                              |
| Archivos temporales                        | % TEMP% \\ \* /s                                                                             |



 

> [!Note]  
> Las aplicaciones que realizan copias de seguridad de nivel de volumen generalmente lo hacen copiando todo el volumen en el nivel de bloque, por lo que no pueden respetar la clave del registro **FilesNotToBackup** en el momento de la copia de seguridad. En su lugar, esperan hasta el momento de la restauración para eliminar los archivos de los que no se ha realizado una copia de seguridad. En la mayoría de los casos, se trata de una estrategia razonable. Sin embargo, en el caso de los archivos de almacenamiento de instancia única, los archivos del almacén común de SIS no deben eliminarse en el momento de la restauración.

 

En el caso de las copias de seguridad de volumen de nivel de bloque, Copias de seguridad de Windows Server y la utilidad Wbadmin de Windows respetan la clave del registro **FilesNotToBackup** eliminando los archivos correspondientes en el momento de la restauración. La restauración del sistema y la copia de seguridad del estado del sistema no respetan la clave del registro **FilesNotToBackup** .

**Windows XP:** Restaurar sistema admite la clave del registro **FilesNotToBackup** .

## <a name="filesnottosnapshot"></a>FilesNotToSnapshot

VSS admite la clave del registro **FilesNotToSnapshot** . Las aplicaciones y los servicios pueden usar esta clave para especificar los archivos que se van a eliminar de las instantáneas recién creadas. Para obtener más información, vea [excluir archivos de instantáneas](/windows/desktop/VSS/excluding-files-from-shadow-copies).

**Windows Server 2003 y Windows XP:** Esta clave del registro no es compatible.

En el caso de las copias de seguridad de volumen de nivel de bloque, Copias de seguridad de Windows Server respeta la clave del registro **FilesNotToSnapshot** eliminando los archivos correspondientes en el momento de la restauración.

## <a name="idletimeout"></a>IdleTimeout

El valor del registro **IdleTimeout** especifica la cantidad de tiempo, en segundos, que el servicio VSS esperará cuando esté inactivo. Si se alcanza este valor de tiempo de espera y no hay ninguna tarea que llevar a cabo, se cerrará el servicio VSS.

Este valor del registro puede encontrarse en la siguiente clave del registro:

**HKEY \_ \_** Configuración de \\  \\  \\  \\ **VSS** \\  de sistema de equipo local

Si este valor del registro no existe:

-   De forma predeterminada, el valor de tiempo de espera real que se usa es de 180 segundos (3 minutos).
-   Puede crear un valor con el nombre **IdleTimeout** y el tipo DWORD y establecerlo en el valor deseado.

Si este valor del registro se establece en 0 segundos:

-   El valor de tiempo de espera real que se usa es de 180 segundos (3 minutos).

Si establece este valor del registro:

-   VSS usa el valor de tiempo de espera establecido.
-   Puede especificar cualquier valor entre 1 y FFFFFFFF segundos. Sin embargo, se recomienda elegir un valor entre 1 y 180 segundos.

**Windows Server 2003 y Windows XP:** Esta clave del registro no es compatible.

## <a name="keysnottorestore"></a>KeysNotToRestore

La clave del registro **KeysNotToRestore** especifica los nombres de las subclaves del registro y los valores que las aplicaciones de copia de seguridad no deben restaurar. Para obtener más información, vea [KeysNotToRestore](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10)). No es necesario respetar la clave del registro **KeysNotToRestore** .

**Windows Server 2003 y Windows XP:** Debe respetar la clave del registro **KeysNotToRestore** .

En el caso de las copias de seguridad de volumen de nivel de bloque, Copias de seguridad de Windows Server respeta la clave del registro **KeysNotToRestore** eliminando los archivos correspondientes en el momento de la restauración.

La copia de seguridad del estado del sistema respeta la clave del registro **KeysNotToRestore** .

## <a name="lastinstance"></a>LastInstance

El valor del registro **LastInstance** indica que se ha realizado una operación de restauración sin sistema operativo y que los volúmenes se han sobrescrito pero no están formateados. Para obtener más información, consulte [uso de la recuperación automática del sistema de VSS para la recuperación ante desastres](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery).

**Windows Server 2003 y Windows XP:** No se admite este valor del registro.

## <a name="lastrestoreid"></a>LastRestoreId

Cuando una aplicación de copia de seguridad realiza una restauración del estado del sistema, debe indicar que se ha hecho estableciendo el valor del registro **LastRestoreId** . En este caso, "restauración del estado del sistema" hace referencia a cualquier restauración que restaure selectivamente los archivos binarios y controladores del sistema operativo.

Si todo el volumen de arranque y del sistema se restaura en el nivel de volumen, no se debe establecer este valor.

Si el valor del registro **LastRestoreId** no existe, la aplicación de copia de seguridad debe crearlo en la siguiente clave del registro:

**HKEY \_ \_Equipo local** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **BackupRestore** \\ **SystemStateRestore**

Cree un valor con el nombre **LastRestoreId** y escriba reg \_ SZ. El valor debe ser un valor opaco único, como un GUID.

Cada vez que se realiza una nueva restauración del estado del sistema, la aplicación de copia de seguridad debe cambiar los datos del valor **LastRestoreId** .

Otras aplicaciones que necesitan supervisar restauraciones de estado del sistema deben almacenar los datos de este valor del registro. Estos datos se pueden comparar con los datos actuales del valor del registro **LastRestoreId** para determinar si se ha realizado una nueva restauración del estado del sistema.

**Windows Vista, Windows Server 2003 y Windows XP:** Este valor del registro no se admite hasta Windows Vista con Service Pack 1 (SP1) y Windows Server 2008.

## <a name="maxshadowcopies"></a>MaxShadowCopies

El valor del registro **MaxShadowCopies** especifica el número máximo de [*instantáneas accesibles para el cliente*](/windows/desktop/VSS/vssgloss-c) que se pueden almacenar en cada volumen del equipo. Una instantánea accesible desde el cliente es una instantánea que se crea mediante el valor **\_ accesible del \_ cliente \_ de VSS CTX** de la enumeración de [**\_ \_ \_ contexto de instantáneas de VSS**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context) . La característica Instantáneas para carpetas compartidas usa las instantáneas accesibles para el cliente. Para obtener más información sobre las instantáneas, consulte la documentación de [VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) .

Si el valor del registro **MaxShadowCopies** no existe, la aplicación de copia de seguridad puede crearlo en la siguiente clave del registro:

**HKEY \_ \_** Configuración de \\  \\  \\  \\ **VSS** \\  de sistema de equipo local

Cree un valor con el nombre **MaxShadowCopies** y escriba DWORD. Los datos predeterminados para este valor son 64. El valor mínimo es 1. El máximo es 512.

> [!Note]  
> Para otros tipos de instantáneas, no hay ningún valor de registro que corresponda a **MaxShadowCopies**. El número máximo de instantáneas es 512 por volumen.

 

**Nota:**  La configuración **MaxShadowCopies** es compatible con Windows Server 2003 o posterior.

**Windows Server 2003:** En los servidores de clúster, es posible que los datos del valor del registro **MaxShadowCopies** deban establecerse en un número menor. Para obtener más información, consulte "cuando se usa la Servicio de instantáneas de volumen en equipos basados en Windows Server 2003 que ejecutan muchas operaciones de e/s, los volúmenes de disco tardan más en estar en línea" en la base de conocimiento de ayuda y soporte técnico en [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058) .

**Windows XP:** No se admite este valor del registro.

## <a name="mindiffareafilesize"></a>MinDiffAreaFileSize

[VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) asigna un área de almacenamiento de instantáneas (o "área de diferencia") para almacenar los datos de las instantáneas. El tamaño mínimo del área de almacenamiento de instantáneas es un valor por equipo que se puede especificar mediante el valor del registro **MinDiffAreaFileSize** .

Si no se establece el valor del registro **MinDiffAreaFileSize** , el tamaño mínimo del área de almacenamiento de instantáneas es 32 MB para los volúmenes menores de 500 mb y 320 MB para los volúmenes mayores de 500 MB.

**Windows server 2008, Windows server 2003 con SP1 y Windows Vista:** Si no se establece el valor del registro **MinDiffAreaFileSize** , el área de almacenamiento de instantáneas tiene un tamaño mínimo de 300 MB. Si se establece el valor del registro **MinDiffAreaFileSize** , sus datos deben estar entre 300 mb y 3000 MB (3 GB) y deben ser un múltiplo de 300 MB.

**Windows Server 2003:** Si no se establece el valor del registro **MinDiffAreaFileSize** , el tamaño mínimo del área de almacenamiento de instantáneas es 100 MB.

**Windows XP:** No se admite este valor del registro.

Si el valor del registro **MinDiffAreaFileSize** no existe, la aplicación de copia de seguridad puede crearlo en la siguiente clave del registro:

**HKEY \_ \_** VolSnap de \\  \\  \\ **servicios** \\  del sistema de equipo local

Cree un valor con el nombre **MinDiffAreaFileSize** y escriba reg \_ DWORD. Los datos de esta clave se especifican en megabytes. 320 es igual a 320 MB y 3200 es igual a 3,2 GB. Debe especificar un número que sea un múltiplo de 32. Si especifica un valor que no es múltiplo de 32, se usará el siguiente múltiplo de 32.

Es posible que las instantáneas no funcionen correctamente si el valor del registro **MinDiffAreaFileSize** especifica un tamaño mínimo mayor que el tamaño máximo del área de almacenamiento de instantáneas. Para especificar el tamaño máximo del área de almacenamiento de instantáneas, use el comando [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) Add shadowstorage o vssadmin Resize shadowstorage. Para ver el tamaño máximo actual, use el comando [vssadmin List shadowstorage](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) Si no ha establecido un tamaño máximo, no hay ningún límite en la cantidad de espacio que se puede usar.

## <a name="overallperformancesetting-and-customperformancesettings"></a>OverallPerformanceSetting y CustomPerformanceSettings

Los valores del registro **OverallPerformanceSetting** y **CustomPerformanceSettings** se usan para especificar la configuración de rendimiento para copias de seguridad de Windows Server. Estos valores del registro solo se admiten en sistemas operativos Windows Server.

**Windows Server 2003:** Estos valores del registro no se admiten.

Si no existen estos valores del registro, la aplicación de copia de seguridad puede crearlos en la siguiente clave del registro:

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windows Block backup**

Para especificar la configuración de rendimiento de todos los volúmenes, cree un valor con el nombre **OverallPerformanceSetting** y escriba reg \_ DWORD. Los datos del valor deben establecerse en uno de los valores siguientes.

| Value | Significado                                                                                                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Rendimiento normal de copia de seguridad (mediante copias de seguridad completas). Esta opción corresponde a la configuración de rendimiento de copia de seguridad normal que se describe en [optimizar la copia de seguridad y el rendimiento del servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).            |
| 2     | Rendimiento de copia de seguridad más rápido (mediante copias de seguridad incrementales). Esta opción corresponde a la configuración de rendimiento de copia de seguridad más rápida que se describe en [optimizar la copia de seguridad y el rendimiento del servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).     |
| 3     | Rendimiento de copia de seguridad personalizado (especificando una configuración de rendimiento para cada volumen). Esta opción corresponde a la configuración personalizada que se describe en [optimizar la copia de seguridad y el rendimiento del servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)). |



 

Si establece **OverallPerformanceSetting** en 3, también debe especificar la configuración de rendimiento para cada volumen individualmente. Para ello, cree un valor con el nombre **CustomPerformanceSettings** y escriba reg \_ multi \_ SZ. Los datos de este valor se deben establecer de la manera siguiente:

-   Cada cadena de la \_ \_ secuencia de cadenas reg multi SZ contiene la configuración de un volumen.
-   Cada cadena consta de un GUID de volumen, seguido de una coma, seguida de un valor DWORD.
-   Cada uno de los valores DWORD es 1 (copia de seguridad completa) o 2 (copia de seguridad incremental).

Por ejemplo, supongamos que el equipo tiene dos volúmenes de la manera siguiente:

-   Los dos volúmenes son C: \\ y D: \\ .
-   El GUID del volumen C: \\ es 07c473ca4-2DF8-11de-9d80-806e6f6e6963 y el GUID del volumen D: \\ is 0ac22ea6c-712f-11de-adb0-00215a67606e.
-   Desea especificar perfornance de copia de seguridad normal para el volumen C: \\ y un rendimiento de copia de seguridad más rápido para el volumen D: \\ .

Para ello, debe establecer **OverallPerformanceSetting** en 3 y **CustomPerformanceSettings** en "07c473ca4-2DF8-11de-9d80-806e6f6e6963, 1 \\ 00ac22ea6c-712f-11de-adb0-00215a67606e, 2".

Si establece **OverallPerformanceSetting** en 1 o 2, se omiten los datos del valor **CustomPerformanceSettings** .

## <a name="sysvol"></a>SYSVOL

El valor del registro **SYSVOL** es una manera de notificar al servicio de replicación sistema de archivos distribuido (DFSR) que se ha iniciado una operación de restauración del estado del sistema. Cualquier aplicación de copia de seguridad que realice la restauración del estado del sistema de SYSVOL debe utilizar este valor para indicar si la operación de restauración es autoritativa o no autoritativa. El servicio DFSR Lee este valor. Si no se establece este valor, la restauración de SYSVOL se realiza de manera no autoritativa de forma predeterminada.

Si el valor del registro **SYSVOL** no existe, la aplicación de copia de seguridad debe crearlo en la siguiente clave del registro:

**HKEY \_ \_** Restauración de \\  \\  \\  \\ **DFSR** \\  de servicios de sistema de equipo local

Cree un valor con el nombre **SYSVOL** y escriba reg \_ SZ. Los datos del valor deben establecerse en "autoritativo" o "no autoritativo" en función de la solicitud del administrador del sistema.

**Windows Vista, Windows Server 2003 y Windows XP:** No se admite este valor del registro.

 

 
