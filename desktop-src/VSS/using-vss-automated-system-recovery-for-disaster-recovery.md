---
description: Una aplicación VSS de copia de seguridad y recuperación que realiza la recuperación ante desastres (también denominada reconstrucción completa) puede usar el escritor de recuperación automática del sistema (ASR) junto con Entorno de preinstalación de Windows (Windows PE) para realizar una copia de seguridad y restaurar los volúmenes críticos y otros componentes del estado del sistema de arranque. La aplicación de copia de seguridad se implementa como un solicitante de VSS.
ms.assetid: 13adfd79-f26a-4385-9b59-129d06fa72eb
title: Uso de la recuperación automatizada del sistema de VSS para la recuperación ante desastres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e31ef8ba223f40928e2422fa92240656f94592d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696485"
---
# <a name="using-vss-automated-system-recovery-for-disaster-recovery"></a>Uso de la recuperación automatizada del sistema de VSS para la recuperación ante desastres

Una aplicación VSS de copia de seguridad y recuperación que realiza la recuperación ante desastres (también denominada reconstrucción completa) puede usar el escritor de recuperación automática del sistema (ASR) junto con Entorno de preinstalación de Windows (Windows PE) para realizar una copia de seguridad y restaurar los volúmenes críticos y otros componentes del estado del sistema de arranque. La aplicación de copia de seguridad se implementa como un solicitante de VSS.

**Nota:**  Las aplicaciones que usan ASR deben tener una licencia de Windows PE.

**Windows Server 2003 y Windows XP:** ASR no se implementa como VSS Writer.

Para obtener información acerca de las herramientas de seguimiento que puede usar con ASR, consulte [uso de herramientas de seguimiento con aplicaciones de ASR de VSS](using-tracing-tools-with-vss-asr-applications.md).

**En este artículo:**

-   [Información general de las tareas de fase de copia de seguridad](#overview-of-backup-phase-tasks)
-   [Elección de los componentes críticos de la copia de seguridad](#choosing-which-critical-components-to-back-up)
-   [Información general sobre las tareas de la fase de restauración](#overview-of-restore-phase-tasks)
-   [Excluir todos los discos de un volumen](#excluding-all-disks-for-a-volume)

## <a name="overview-of-backup-phase-tasks"></a>Información general de las tareas de fase de copia de seguridad

En el momento de la copia de seguridad, el solicitante realiza los pasos siguientes.

> [!Note]  
> Todos los pasos son necesarios a menos que se indique lo contrario.

 

1.  Llame a la función [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) para crear una instancia de la interfaz [**ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) y llamar al método [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) para inicializar la instancia para administrar una copia de seguridad.
2.  Llame a [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) para establecer el contexto de la operación de instantánea.
3.  Llame a [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) para configurar la copia de seguridad. Establezca el parámetro *bBackupBootableSystemState* en **true** para indicar que la copia de seguridad incluirá un estado del sistema de arranque.
4.  Elija los componentes críticos del documento de metadatos del escritor del escritor de ASR para realizar copias de seguridad y llamar a [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para cada uno de ellos.
5.  Llame a [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para crear un nuevo conjunto de instantáneas vacío.
6.  Llame a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) para iniciar el contacto asincrónico con escritores.
7.  Llame a [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para recuperar el documento de metadatos del escritor del escritor de ASR. El ID. de escritor del escritor de ASR es BE000CBE-11FE-4426-9C58-531AA6355FC4 y la cadena de nombre de escritor es "ASR Writer".
8.  Llame a [**IVssExamineWriterMetadata:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) para guardar una copia del documento de metadatos del escritor del escritor de ASR.
9.  Llame a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) para cada volumen que pueda participar en instantáneas para agregar el volumen al conjunto de instantáneas.
10. Llame a [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) para notificar a los escritores que deben prepararse para una operación de copia de seguridad.
11. Llame a [**ivssbackupcomponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) y [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (o [**IVssBackupComponentsEx3:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex)) para comprobar el estado del escritor de ASR.
12. En este momento, puede consultar los mensajes de error establecidos por el escritor en su método [**CVssWriter:: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) . Para obtener un ejemplo de código que muestra cómo ver estos mensajes, vea [**IVssComponentEx:: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).
13. Llame a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) para crear una instantánea de volumen.
14. Llame a [**ivssbackupcomponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) y [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) para comprobar el estado del escritor de ASR.
15. Realice una copia de seguridad de los datos.
16. Indica si la operación de copia de seguridad se realizó correctamente llamando a [**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded).
17. Llame a [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) para indicar que se ha completado la operación de copia de seguridad.
18. Llame a [**ivssbackupcomponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) y [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus). La memoria de estado de sesión del escritor es un recurso limitado y los escritores deben volver a usar los Estados de sesión. Este paso marca el estado de la sesión de copia de seguridad del escritor como completado e informa a VSS de que esta ranura de sesión de copia de seguridad se puede volver a usar en una operación de copia de seguridad posterior.
    > [!Note]  
    > Esto solo es necesario en Windows Server 2008 con Service Pack 2 (SP2) y versiones anteriores.

     

19. Llame a [**IVssBackupComponents:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) para guardar una copia del documento de componentes de copia de seguridad del solicitante. La información del documento componentes de copia de seguridad se usa en el momento de la restauración cuando el solicitante llama al método [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) .

## <a name="choosing-which-critical-components-to-back-up"></a>Elección de los componentes críticos de la copia de seguridad

En la fase de inicialización de la copia de seguridad, el escritor de ASR informa de los siguientes tipos de componentes en su documento de metadatos de escritura:

-   Volúmenes críticos, como los volúmenes de arranque, sistema y entorno de recuperación de Windows (Windows RE) y la partición de Windows RE asociada a la instancia de Windows Vista o Windows Server 2008 que se está ejecutando actualmente. Un volumen es un *volumen crítico* si contiene información de estado del sistema. Los volúmenes de arranque y del sistema se incluyen automáticamente. El solicitante debe incluir todos los volúmenes que contengan componentes críticos del sistema detectados por escritores, como los volúmenes que contienen el Active Directory. Los componentes críticos del sistema se marcan como "no seleccionable para copia de seguridad". En VSS, "no seleccionable" significa "no opcional". Por lo tanto, se requiere que el solicitante realice una copia de seguridad de ellos como parte del estado del sistema. Para obtener más información, consulte [copia de seguridad y restauración del estado del sistema](locating-additional-system-files.md). Los componentes para los que \_ se establece la marca de estado CF de VSS \_ no \_ son críticos para el \_ sistema.
    > [!Note]  
    > El componente ASR es un componente crítico para el sistema que es detectado por el escritor de ASR.

     

-   Disco. Cada disco fijo del equipo se expone como componente en ASR. Si un disco no se ha excluido durante la copia de seguridad, se asignará durante la restauración y se podrá volver a crear y formatear. Tenga en cuenta que durante la restauración, el solicitante puede volver a crear un disco que se ha excluido durante la copia de seguridad llamando al método [**IVssBackupComponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) . Si se selecciona un disco en un paquete de disco dinámico, también se deben seleccionar todos los demás discos de ese paquete. Si se selecciona un volumen porque es un volumen crítico (es decir, un volumen que contiene información de estado del sistema), también se deben seleccionar todos los discos que contengan una extensión para ese volumen. Para buscar las extensiones de un volumen, use el código de control de [**volumen de ioctl \_ \_ Get \_ Volume \_ \_ extents**](/windows/win32/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents) .

    > [!Note]  
    > Durante la copia de seguridad, el solicitante debe incluir todos los discos fijos. Si el disco que contiene el conjunto de copia de seguridad del solicitante es un disco local, se debe incluir este disco. Durante la restauración, el solicitante debe excluir el disco que contiene el conjunto de copia de seguridad del solicitante para evitar que se sobrescriba.

     

    En un entorno de clústeres, ASR no vuelve a crear el diseño de los discos compartidos del clúster. Esos discos deben restaurarse en línea después de restaurar el sistema operativo en Windows RE.

-   Almacén datos de la configuración de arranque (BCD) (BCD). Este componente especifica la ruta de acceso del directorio que contiene el almacén BCD. El solicitante debe especificar este componente y realizar una copia de seguridad de todos los archivos del directorio del almacén BCD. Para obtener más información sobre el almacén BCD, consulte [acerca de BCD](/previous-versions/windows/desktop/bcd/about-bcd).
    > [!Note]  
    > En los equipos que usan la interfaz de firmware extendido (EFI), la partición del sistema EFI (ESP) siempre está oculta y no se puede incluir en una instantánea de volumen. El solicitante debe realizar una copia de seguridad del contenido de esta partición. Dado que esta partición no se puede incluir en una instantánea de volumen, la copia de seguridad solo se puede realizar desde el volumen activo, no desde la instantánea. Para obtener más información acerca de EFI y ESP, consulte la [Guía de introducción](/windows-hardware/drivers/bringup/).

Los nombres de componente usan los formatos siguientes:

-   En el caso de los componentes de disco, el formato es

    <COMPONENT logicalPath="Disks" componentName="harddisk*n*" componentType="filegroup" />

    donde *n* es el número de disco. Solo se registra el número de disco. Para obtener el número de disco, use el código de control de [**\_ \_ \_ \_ número de dispositivo de almacenamiento de ioctl**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) .

-   En el caso de los componentes de volumen, el formato es

    <COMPONENT logicalPath="Volumes" componentName="Volume{*GUID*}" componentType="filegroup" />

    donde *GUID* es el GUID del volumen.

-   En el caso del componente de almacén BCD, el formato es

    <COMPONENT logicalPath="BCD" componentName="BCD" componentType="filegroup" componentCaption = "This is the path to the boot BCD store and the boot managers...All the files in this directory need to be backed up...">

    Si la partición del sistema tiene un nombre de GUID de volumen, este componente es seleccionable. De lo contrario, no es seleccionable.

    > [!Note]  
    > ASR agrega los archivos al grupo de archivos del componente de almacén BCD como se indica a continuación:
    >
    > -   Para los discos EFI, ASR agrega
    >
    >     *SystemPartitionPath* \\ Arranque de EFI de \\ Microsoft \\ \\ \* .\*
    >
    >     donde *SystemPartitionPath* es la ruta de acceso a la partición del sistema.
    >
    > -   Para discos GPT, ASR agrega
    >
    >     *SystemPartitionPath* \\ Arranque \\ \* .\*
    >
    >     donde *SystemPartitionPath* es la ruta de acceso a la partición del sistema.
    >
    > -   La ruta de acceso de la partición del sistema se puede encontrar en la siguiente clave del registro: **HKEY \_ local \_ Machine** \\ **System** \\ **setup** \\ **SystemPartition**

     

En la restauración, se deben restaurar todos los componentes marcados como volúmenes críticos. Si no se pueden restaurar uno o más volúmenes críticos, se produce un error en la operación de restauración.

En la fase de [**prerestauración**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) de la secuencia de restauración, los discos que no se excluyeron durante la copia de seguridad se vuelven a crear y se cambian de formato de forma predeterminada. Sin embargo, no se vuelven a crear ni se les vuelve a dar formato si cumplen las condiciones siguientes:

-   Un disco básico no se vuelve a crear si el diseño del disco está intacto o solo se han realizado cambios aditivos en él. El diseño del disco está intacto si se cumplen las condiciones siguientes:
    -   La firma de disco, el estilo de disco (GPT o MBR), el tamaño de sector lógico y el desplazamiento de inicio de volumen no cambian.
    -   No se reduce el tamaño del volumen.
    -   En el caso de los discos GPT, no se cambia el identificador de la partición.
-   Un disco dinámico no se vuelve a crear si el diseño del disco está intacto o solo se han realizado cambios aditivos en él. Para que un disco dinámico quede intacto, deben cumplirse todas las condiciones de un disco básico. Además, la estructura de volumen de todo el paquete de disco debe estar intacta. La estructura de volumen del paquete de disco está intacta si cumple las siguientes condiciones, que se aplican a los discos MBR y GPT:
    -   El número de volúmenes que están disponibles en el paquete físico durante la restauración debe ser mayor o igual que el número de volúmenes que se especificaron en los metadatos del escritor de ASR durante la copia de seguridad.
    -   El número de [*complejos*](../vds/virtual-disk-service-glossary-all.md) por volumen debe ser inalterado.
    -   El número de [*miembros*](../vds/virtual-disk-service-glossary-all.md) no debe modificarse.
    -   El número de extensiones de disco físico debe ser mayor que el número de extensiones de disco especificado en los metadatos del escritor de ASR.
    -   Un paquete intacto permanece intacto cuando se agregan volúmenes adicionales o si se extiende un volumen del paquete (por ejemplo, de un volumen simple a un volumen distribuido).
        > [!Note]  
        > Si un volumen simple está reflejado, el paquete no está intacto y se volverá a crear para asegurarse de que los BCD y el estado del volumen de arranque siguen siendo coherentes después de la restauración. Si se eliminan los volúmenes, se vuelve a crear el paquete.

         
-   Si la estructura de volumen del paquete de disco dinámico está intacta y solo se han realizado cambios aditivos en ella, los discos del módulo no se vuelven a crear.

    **Windows Vista:** Los discos dinámicos siempre se vuelven a crear. Tenga en cuenta que este comportamiento ha cambiado con Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

En cualquier momento antes del comienzo de la fase de restauración, el solicitante puede especificar que los discos deben tener un formato rápido estableciendo la clave del registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** . Bajo esta clave, hay un valor denominado **QuickFormat** con el tipo de datos reg \_ DWORD. Si este valor no existe, debe crearlo. Establezca los datos del valor de **QuickFormat** en 1 para el formato rápido o 0 para el formato lento.

Si el valor **QuickFormat** no existe, los discos tendrán un formato lento.

El formato rápido es mucho más rápido que el formato lento (también denominado formato completo). Sin embargo, el formato rápido no comprueba cada sector del volumen.

## <a name="overview-of-restore-phase-tasks"></a>Información general sobre las tareas de la fase de restauración

En el momento de la restauración, el solicitante realiza los siguientes pasos:

> [!Note]  
> Todos los pasos son necesarios a menos que se indique lo contrario.

 

1.  Llame a la función [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) para crear una instancia de la interfaz [**ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) y llamar al método [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) para inicializar la instancia para la restauración mediante la carga del documento de componentes de copia de seguridad del solicitante en la instancia.
2.  \[Este paso solo es necesario si el solicitante debe cambiar si se especifica "IncludeDisk" o "ExcludeDisk" para uno o varios discos. \] Llame a [**IVssBackupComponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) para establecer las opciones de restauración de los componentes del escritor de ASR. El escritor de ASR admite las siguientes opciones: "IncludeDisk" permite que el solicitante incluya un disco en el sistema de destino que se va a considerar para la restauración, aunque no se haya seleccionado durante la fase de copia de seguridad. "ExcludeDisk" permite al solicitante impedir que se vuelva a crear un disco en el sistema de destino. Tenga en cuenta que si se especifica "ExcludeDisk" para un disco que contiene un volumen crítico, se producirá un error en la siguiente llamada a [**IVssBackupComponents::P Rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .

    En el ejemplo siguiente se muestra cómo usar [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) para evitar que se vuelvan a crear el disco 0 y el disco 1, así como para inyectar controladores de terceros en el volumen de arranque restaurado.

    **Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admite la inyección de controladores de terceros.

    En el ejemplo se da por supuesto que el puntero [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , m \_ pBackupComponents, es válido.

    ```C++
        m_pBackupComponents->SetRestoreOptions(
            AsrWriterId,
            VSS_CT_FILEGROUP,
            NULL,
            TEXT("ASR"),
            TEXT("\"ExcludeDisk\"=\"0\", \"ExcludeDisk\"=\"1\" "),
            TEXT("\"InjectDrivers\"=\"1\" ")
            );
    ```

    

    Para excluir todos los discos de un volumen especificado, consulte la siguiente sección "excluir todos los discos de un volumen".

3.  Llame a [**IVssBackupComponents::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) volver a restaurar para notificar al escritor de ASR que debe prepararse para una operación de restauración. Llame a [**IVssAsync:: QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) tantas veces como sea necesario hasta que el valor de estado devuelto en el parámetro *pHrResult* no esté pendiente de VSS \_ S \_ Async \_ .
4.  Restaure los datos. En la fase de restauración, ASR vuelve a configurar la ruta de acceso del GUID del volumen ( \\ \\ ? \\ Volumen {GUID}) de cada volumen para que coincida con la ruta de acceso del GUID del volumen que se usó durante la fase de copia de seguridad. No obstante, las letras de unidad no se conservan, ya que esto provocaría colisiones con las letras de unidad que se asignan automáticamente en el entorno de recuperación. Por lo tanto, al restaurar los datos, el solicitante debe usar las rutas de acceso de GUID de volumen, no las letras de unidad, para acceder a los volúmenes.
5.  Establezca la  \\  \\ clave del registro HKLM software **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** para indicar el conjunto de volúmenes que se han restaurado o cambiado de formato.

    Bajo esta clave, hay un valor denominado **RestoredVolumes** con el tipo de datos reg \_ multi \_ SZ. Si este valor no existe, debe crearlo. En este valor, el solicitante debe crear una entrada de GUID de volumen para cada volumen que se ha restaurado. Esta entrada debe tener el formato siguiente: \\ \\ ? \\ Volumen {78618c8f-AEFD-11da-a898-806e6f6e6963}. Cada vez que se realiza una reconstrucción completa, ASR establece el valor de **RestoredVolumes** en el conjunto de volúmenes restaurados con ASR. Si el solicitante restauró volúmenes adicionales, debe establecer este valor en la Unión del conjunto de volúmenes restaurado por el solicitante y en el conjunto de volúmenes restaurados con ASR. Si el solicitante no usó ASR, debe reemplazar la lista de volúmenes.

    También debe crear un valor denominado **LastInstance** con el tipo de datos reg \_ SZ. Esta clave debe contener una cookie aleatoria que identifique de forma única la operación de restauración actual. Esta cookie se puede crear mediante las funciones [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) y [**UuidToString**](/windows/win32/api/rpcdce/nf-rpcdce-uuidtostring) . Cada vez que se realiza una reconstrucción completa, ASR restablece este valor del registro para notificar a los solicitantes y a las aplicaciones de copia de seguridad que no son de VSS que se ha producido la recuperación.

6.  Llame a [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) para indicar el final de la operación de restauración. Llame a [**IVssAsync:: QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) tantas veces como sea necesario hasta que el valor de estado devuelto en el parámetro *pHrResult* no esté pendiente de VSS \_ S \_ Async \_ .

En la fase de restauración, ASR puede crear o quitar particiones para restaurar el equipo a su estado anterior. Los solicitantes no deben intentar asignar los números de disco de la fase de copia de seguridad a la fase de restauración.

En la restauración, el solicitante debe excluir el disco que contiene el conjunto de copia de seguridad del solicitante. De lo contrario, la operación de restauración puede sobrescribir el conjunto de copia de seguridad.

En la restauración, se excluye un disco si no se seleccionó como componente durante la copia de seguridad, o si se excluye explícitamente mediante una llamada a [**IVssBackupComponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) con la opción "ExcludeDisk" durante la restauración.

Es importante tener en cuenta que durante la recuperación ante desastres de WinPE, la funcionalidad del escritor de ASR está presente, pero no hay ningún otro escritor disponible y el servicio VSS no se está ejecutando. Una vez finalizada la recuperación ante desastres de WinPE, el equipo se ha reiniciado y el sistema operativo Windows se ejecuta con normalidad, se puede iniciar el servicio VSS y el solicitante puede realizar cualquier operación de restauración adicional que requiera la participación de escritores distintos del escritor de ASR.

Si durante la sesión de restauración la aplicación de copia de seguridad detecta que los identificadores únicos del volumen no han cambiado y, por tanto, todos los volúmenes desde el momento de la copia de seguridad están presentes e intactos en WinPE, la aplicación de copia de seguridad puede continuar para restaurar solo el contenido de los volúmenes, sin necesidad de ASR. En este caso, la aplicación de copia de seguridad debe indicar que el equipo se restauró mediante la configuración de la siguiente clave del registro en el sistema operativo restaurado: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession**

Bajo esta clave, especifique **LastInstance** para el nombre de valor, REG \_ SZ para el tipo de valor y una cookie aleatoria (como un GUID creado por la función [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) ) para los datos del valor.

Si durante la sesión de restauración la aplicación de copia de seguridad detecta que uno o varios volúmenes se han modificado o faltan, la aplicación de copia de seguridad debe usar ASR para realizar la restauración. ASR volverá a crear los volúmenes exactamente del modo en que se encontraban en el momento de la copia de seguridad y establecerá la clave del registro **RestoreSession** .

## <a name="excluding-all-disks-for-a-volume"></a>Excluir todos los discos de un volumen

En el ejemplo siguiente se muestra cómo excluir todos los discos de un volumen especificado.


```C++
HRESULT BuildRestoreOptionString
(
    const WCHAR             *pwszVolumeNamePath,
    CMyString               *pstrExclusionList
)
{
    HANDLE                  hVolume           = INVALID_HANDLE_VALUE;
    DWORD                   cbSize            = 0;
    VOLUME_DISK_EXTENTS     * pExtents        = NULL;
    DISK_EXTENT             * pExtent         = NULL;
    ULONG                   i                 = 0;
    BOOL                    fIoRet            = FALSE;
    WCHAR                   wszDest[MAX_PATH] = L"";
    CMyString               strVolumeName;
    CMyString               strRestoreOption;

    // Open a handle to the volume device.
    strVolumeName.Set( pwszVolumeNamePath );
    // If the volume name contains a trailing backslash, remove it.
    strVolumeName.UnTrailing( L'\\' );
    hVolume = ::CreateFile(strVolumeName, 0, FILE_SHARE_READ | FILE_SHARE_WRITE, NULL, OPEN_EXISTING, NULL, 0);
    // Check whether the call to CreateFile succeeded.

    // Get the list of disks used by this volume.
    cbSize = sizeof(VOLUME_DISK_EXTENTS);
    pExtents = (VOLUME_DISK_EXTENTS *)::CoTaskMemAlloc(cbSize);

    ::ZeroMemory(pExtents, cbSize);

    fIoRet = ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
    if ( !fIoRet && GetLastError() == ERROR_MORE_DATA )
    {
        // Allocate more memory.
        cbSize = FIELD_OFFSET(VOLUME_DISK_EXTENTS, Extents) + pExtents->NumberOfDiskExtents * sizeof(DISK_EXTENT);
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;

        pExtents = (VOLUME_DISK_EXTENTS *) ::CoTaskMemAlloc(cbSize);
        // Check whether CoTaskMemAlloc returned an out-of-memory error.
        ::ZeroMemory(pExtents, cbSize);

        // Now the buffer should be big enough.
        ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
        // Check whether the IOCTL succeeded.
    }
    // Check for errors; note that the IOCTL can fail for a reason other than insufficient memory.

    // For each disk, mark it to be excluded in the Restore Option string.
    for (i = 0; i < pExtents->NumberOfDiskExtents; i++)
    {
        pExtent = &pExtents->Extents[i];

        *wszDest = L'\0';
        StringCchPrintf(wszDest, MAX_PATH, L"\"ExcludeDisk\"=\"%d\", ", pExtent->DiskNumber); // check errors

        strRestoreOption.Append(wszDest);
        // Check for an out-of-memory error.
    }

    // Remove the trailing comma.
    strRestoreOption.TrimRight();
    strRestoreOption.UnTrailing(',');

    // Set the output parameter.
    strRestoreOption.Transfer( pstrExclusionList );

Exit:
    if( pExtents )
    {
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;
    }

    if( hVolume != INVALID_HANDLE_VALUE )
    {
        ::CloseHandle(hVolume);
        hVolume = INVALID_HANDLE_VALUE;
    }

    return ( hr );
}

```



 

 
