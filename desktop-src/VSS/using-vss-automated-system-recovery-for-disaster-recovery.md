---
description: Una aplicación de copia de seguridad y recuperación de VSS que realiza la recuperación ante desastres (también denominada recuperación sin sistema operativo) puede usar el sistema de escritura Recuperación del sistema automatizado (ASR) junto con un entorno de preinstalación de Windows (Windows PE) para realizar copias de seguridad y restaurar volúmenes críticos y otros componentes del estado del sistema de arranque. La aplicación de copia de seguridad se implementa como solicitante de VSS.
ms.assetid: 13adfd79-f26a-4385-9b59-129d06fa72eb
title: Uso de VSS Automated Recuperación del sistema para la recuperación ante desastres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813f0f746600fa665ed20bb208f3241cb1a88a12de721d53a8afa77be4a4c35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998067"
---
# <a name="using-vss-automated-system-recovery-for-disaster-recovery"></a>Uso de VSS Automated Recuperación del sistema para la recuperación ante desastres

Una aplicación de copia de seguridad y recuperación de VSS que realiza la recuperación ante desastres (también denominada recuperación sin sistema operativo) puede usar el sistema de escritura Recuperación del sistema automatizado (ASR) junto con un entorno de preinstalación de Windows (Windows PE) para realizar copias de seguridad y restaurar volúmenes críticos y otros componentes del estado del sistema de arranque. La aplicación de copia de seguridad se implementa como solicitante de VSS.

**Nota**  Las aplicaciones que usan ASR deben tener Windows PE.

**Windows Server 2003 y Windows XP:** ASR no se implementa como vss writer.

Para obtener información sobre las herramientas de seguimiento que puede usar con ASR, vea [Using Tracing Tools with VSS ASR Applications](using-tracing-tools-with-vss-asr-applications.md).

**En este artículo:**

-   [Información general de las tareas de la fase de copia de seguridad](#overview-of-backup-phase-tasks)
-   [Elección de los componentes críticos de los que se va a hacer una copia de seguridad](#choosing-which-critical-components-to-back-up)
-   [Información general de las tareas de la fase de restauración](#overview-of-restore-phase-tasks)
-   [Exclusión de todos los discos de un volumen](#excluding-all-disks-for-a-volume)

## <a name="overview-of-backup-phase-tasks"></a>Información general de las tareas de la fase de copia de seguridad

En el momento de la copia de seguridad, el solicitante realiza los pasos siguientes.

> [!Note]  
> Todos los pasos son necesarios a menos que se indique lo contrario.

 

1.  Llame a la función [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) para crear una instancia de la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) y llame al método [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) para inicializar la instancia de para administrar una copia de seguridad.
2.  Llame [**a IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) para establecer el contexto de la operación de instantánea.
3.  Llame [**a IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) para configurar la copia de seguridad. Establezca el *parámetro bBackupBootableSystemState* en **true** para indicar que la copia de seguridad incluirá un estado del sistema de arranque.
4.  Elija los componentes críticos del documento de metadatos del escritor de ASR para hacer una copia de seguridad y llamar a [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para cada uno de ellos.
5.  Llame [**a IVssBackupComponents::StartSnapshotSet para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) crear un nuevo conjunto de instantáneas vacío.
6.  Llame [**a IVssBackupComponents::GatherWriterMetadata para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) iniciar el contacto asincrónico con los escritores.
7.  Llame [**a IVssBackupComponents::GetWriterMetadata para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) recuperar el documento de metadatos del escritor de ASR. El identificador del escritor de ASR es BE000CBE-11FE-4426-9C58-531AAA6355FC4 y la cadena de nombre del escritor es "ASR Writer".
8.  Llame [**a IVssExgvWriterMetadata::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) para guardar una copia del documento de metadatos del escritor de ASR.
9.  Llame [**a IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) para cada volumen que pueda participar en instantáneas para agregar el volumen al conjunto de instantáneas.
10. Llame [**a IVssBackupComponents::P repareForBackup para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) notificar a los escritores que se preparen para una operación de copia de seguridad.
11. Llame [**a IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (o [**IVssBackupComponentsEx3::GetWriterStatus)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex)para comprobar el estado del sistema de escritura de ASR.
12. En este punto, puede consultar los mensajes de error establecidos por el escritor en su [**método CVssWriter::OnPrepareBackup.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) Para obtener código de ejemplo que muestra cómo ver estos mensajes, vea [**IVssComponentEx::GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).
13. Llame [**a IVssBackupComponents::D oSnapshotSet para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) crear una instantánea de volumen.
14. Llame [**a IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) para comprobar el estado del escritor de ASR.
15. Copia de seguridad de los datos.
16. Indique si la operación de copia de seguridad se ha hecho correctamente llamando a [**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded).
17. Llame [**a IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) para indicar que se ha completado la operación de copia de seguridad.
18. Llame [**a IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus). La memoria de estado de sesión del escritor es un recurso limitado y los escritores deben volver a usar los estados de sesión. Este paso marca el estado de sesión de copia de seguridad del escritor como completado y notifica a VSS que esta ranura de sesión de copia de seguridad se puede reutilizar mediante una operación de copia de seguridad posterior.
    > [!Note]  
    > Esto solo es necesario en Windows Server 2008 con Service Pack 2 (SP2) y versiones anteriores.

     

19. Llame [**a IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) para guardar una copia del documento de componentes de copia de seguridad del solicitante. La información del documento componentes de copia de seguridad se usa en tiempo de restauración cuando el solicitante llama al método [**IVssBackupComponents::InitializeForRestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)

## <a name="choosing-which-critical-components-to-back-up"></a>Elección de los componentes críticos de los que se va a hacer una copia de seguridad

En la fase de inicialización de la copia de seguridad, asr writer notifica los siguientes tipos de componentes en su documento de metadatos del escritor:

-   Volúmenes críticos, como los volúmenes de arranque, sistema y entorno de recuperación de Windows (Windows RE) y la partición Windows RE asociada a la instancia de Windows Vista o Windows Server 2008 que se está ejecutando actualmente. Un volumen es un *volumen crítico si* contiene información de estado del sistema. Los volúmenes de arranque y del sistema se incluyen automáticamente. El solicitante debe incluir todos los volúmenes que contienen componentes críticos del sistema notificados por los escritores, como los volúmenes que contienen el Active Directory. Los componentes críticos del sistema se marcan como "no seleccionables para la copia de seguridad". En VSS, "no seleccionable" significa "no opcional". Por lo tanto, el solicitante debe realizar una copia de seguridad de ellos como parte del estado del sistema. Para obtener más información, vea [Realizar copias de seguridad y restaurar el estado del sistema.](locating-additional-system-files.md) Los componentes para los que se establece la marca \_ VSS CF \_ NOT SYSTEM STATE no son \_ \_ críticos para el sistema.
    > [!Note]  
    > El componente ASR es un componente crítico del sistema notificado por el escritor de ASR.

     

-   Discos. Todos los discos fijos del equipo se exponen como un componente en ASR. Si no se excluyó un disco durante la copia de seguridad, se asignará durante la restauración y se puede volver a crear y volver a formatear. Tenga en cuenta que durante la restauración, el solicitante todavía puede volver a crear un disco que se excluyó durante la copia de seguridad llamando al método [**IVssBackupComponents::SetRestoreOptions.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) Si se selecciona un disco en un paquete de disco dinámico, también se deben seleccionar todos los demás discos de ese paquete. Si se selecciona un volumen porque es un volumen crítico (es decir, un volumen que contiene información de estado del sistema), también se deben seleccionar todos los discos que contengan una extensión para ese volumen. Para buscar las extensiones de un volumen, use el código de control [**IOCTL \_ VOLUME GET VOLUME DISK \_ \_ \_ \_ EXTENTS.**](/windows/win32/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents)

    > [!Note]  
    > Durante la copia de seguridad, el solicitante debe incluir todos los discos fijos. Si el disco que contiene el conjunto de copia de seguridad del solicitante es un disco local, debe incluirse este disco. Durante la restauración, el solicitante debe excluir el disco que contiene el conjunto de copia de seguridad del solicitante para evitar que se sobrescriba.

     

    En un entorno de agrupación en clústeres, ASR no vuelve a crear el diseño de los discos compartidos del clúster. Estos discos deben restaurarse en línea después de restaurar el sistema operativo en el Windows RE.

-   datos de la configuración de arranque (BCD) (BCD). Este componente especifica la ruta de acceso del directorio que contiene el almacén BCD. El solicitante debe especificar este componente y hacer una copia de seguridad de todos los archivos del directorio del almacén BCD. Para obtener más información sobre el almacén de BCD, vea [Acerca de BCD.](/previous-versions/windows/desktop/bcd/about-bcd)
    > [!Note]  
    > En los equipos que usan la interfaz de firmware extendida (EFI), la partición del sistema EFI (ESP) siempre está oculta y no se puede incluir en una instantánea de volumen. El solicitante debe hacer una copia de seguridad del contenido de esta partición. Dado que esta partición no se puede incluir en una instantánea de volumen, la copia de seguridad solo se puede realizar desde el volumen en directo, no desde la instantánea. Para obtener más información acerca de EFI y ESP, consulte [la guía de inicio](/windows-hardware/drivers/bringup/).

Los nombres de componente usan los siguientes formatos:

-   Para los componentes de disco, el formato es

    <COMPONENT logicalPath="Disks" componentName="harddisk*n*" componentType="filegroup" />

    donde *n* es el número de disco. Solo se registra el número de disco. Para obtener el número de disco, use el código de control [**IOCTL \_ STORAGE GET \_ DEVICE \_ \_ NUMBER.**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_device_number)

-   Para los componentes de volumen, el formato es

    <COMPONENT logicalPath="Volumes" componentName="Volume{*GUID*}" componentType="filegroup" />

    donde *GUID* es el GUID del volumen.

-   Para el componente de almacén BCD, el formato es

    <COMPONENT logicalPath="BCD" componentName="BCD" componentType="filegroup" componentCaption = "This is the path to the boot BCD store and the boot managers...All the files in this directory need to be backed up...">

    Si la partición del sistema tiene un nombre GUID de volumen, este componente se puede seleccionar. De lo contrario, no se puede seleccionar.

    > [!Note]  
    > ASR agrega los archivos al grupo de archivos del componente de almacén BCD como se muestra a continuación:
    >
    > -   En el caso de los discos EFI, ASR agrega
    >
    >     *SystemPartitionPath* \\ EFI \\ Microsoft \\ Boot \\ \* .\*
    >
    >     donde *SystemPartitionPath es* la ruta de acceso a la partición del sistema.
    >
    > -   En el caso de los discos GPT, ASR agrega
    >
    >     *SystemPartitionPath* \\ Arranque \\ \* .\*
    >
    >     donde *SystemPartitionPath es* la ruta de acceso a la partición del sistema.
    >
    > -   La ruta de acceso de partición del sistema se puede encontrar en la siguiente clave del Registro: **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **Setup** \\ **SystemPartition**

     

En la restauración, se deben restaurar todos los componentes marcados como volúmenes críticos. Si uno o varios volúmenes críticos no se pueden restaurar, se produce un error en la operación de restauración.

En la [**fase prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) de la secuencia de restauración, los discos que no se excluyeron durante la copia de seguridad se crean y se vuelve a formatear de forma predeterminada. Sin embargo, no se vuelve a crear ni se vuelve a formatear si cumplen las condiciones siguientes:

-   No se vuelve a crear un disco básico si su diseño de disco está intacto o si solo se han realizado cambios de adiciones en él. El diseño del disco está intacto si se cumplen las condiciones siguientes:
    -   La firma de disco, el estilo de disco (GPT o MBR), el tamaño del sector lógico y el desplazamiento de inicio del volumen no cambian.
    -   El tamaño del volumen no disminuye.
    -   En el caso de los discos GPT, no se cambia el identificador de partición.
-   No se vuelve a crear un disco dinámico si su diseño de disco está intacto o solo se han realizado cambios de adición en él. Para que un disco dinámico esté intacto, se deben cumplir todas las condiciones de un disco básico. Además, toda la estructura del volumen del paquete de disco debe estar intacta. La estructura del volumen del paquete de discos está intacta si cumple las condiciones siguientes, que se aplican a los discos MBR y GPT:
    -   El número de volúmenes que están disponibles en el paquete físico durante la restauración debe ser mayor o igual que el número de volúmenes que se especificaron en los metadatos del escritor de ASR durante la copia de seguridad.
    -   El número de [*plexos*](../vds/virtual-disk-service-glossary-all.md) por volumen no debe modificarse.
    -   El número de [*miembros*](../vds/virtual-disk-service-glossary-all.md) no debe modificarse.
    -   El número de extensiones de disco físico debe ser mayor que el número de extensiones de disco especificadas en los metadatos del escritor de ASR.
    -   Un paquete intacto permanece intacto cuando se agregan volúmenes adicionales o si se extiende un volumen del paquete (por ejemplo, de un volumen simple a un volumen abarcado).
        > [!Note]  
        > Si se refleja un volumen simple, el paquete no está intacto y se volverá a crear para asegurarse de que el estado del volumen de arranque y BCD sigue siendo coherente después de la restauración. Si se eliminan volúmenes, se vuelve a crear el paquete.

         
-   Si la estructura del volumen del paquete de discos dinámico está intacta y solo se han realizado cambios adicionales en él, los discos del paquete no se vuelvan a crear.

    **Windows Vista:** Los discos dinámicos siempre se vuelve a crear. Tenga en cuenta que este comportamiento ha cambiado con Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

En cualquier momento antes del inicio de la fase de restauración, el solicitante puede especificar que se debe dar formato rápido a los discos estableciendo la clave del Registro **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession.** En esta clave, hay un valor denominado **QuickFormat** con el tipo de datos REG \_ DWORD. Si este valor no existe, debe crearlo. Establezca los datos del valor **de QuickFormat** en 1 para el formato rápido o 0 para el formato lento.

Si el **valor de QuickFormat** no existe, los discos tendrán un formato lento.

El formato rápido es significativamente más rápido que el formato lento (también denominado formato completo). Sin embargo, el formato rápido no comprueba cada sector del volumen.

## <a name="overview-of-restore-phase-tasks"></a>Información general de las tareas de la fase de restauración

En el momento de la restauración, el solicitante realiza los pasos siguientes:

> [!Note]  
> Todos los pasos son necesarios a menos que se indique lo contrario.

 

1.  Llame a la función [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) para crear una instancia de la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) y llame al método [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) para inicializar la instancia para la restauración cargando el documento de componentes de copia de seguridad del solicitante en la instancia.
2.  \[Este paso solo es necesario si el solicitante necesita cambiar si se especifica "IncludeDisk" o "ExcludeDisk" para uno o varios discos. \] Llame [**a IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) para establecer las opciones de restauración de los componentes del escritor de ASR. ASR Writer admite las siguientes opciones: "IncludeDisk" permite al solicitante incluir un disco en el sistema de destino que se debe tener en cuenta para la restauración, incluso si no se seleccionó durante la fase de copia de seguridad. "ExcludeDisk" permite al solicitante evitar que se vuelva a crear un disco en el sistema de destino. Tenga en cuenta que si se especifica "ExcludeDisk" para un disco que contiene un volumen crítico, se producirá un error en la llamada subsiguiente a [**IVssBackupComponents::P reRestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)

    En el ejemplo siguiente se muestra cómo usar [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) para evitar que el disco 0 y el disco 1 se vuelvan a crear e insertar controladores de terceros en el volumen de arranque restaurado.

    **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite la inserción de controladores de terceros.

    En el ejemplo se supone que el [**puntero IVssBackupComponents,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) m \_ pBackupComponents, es válido.

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

    

    Para excluir todos los discos de un volumen especificado, consulte el siguiente artículo "Exclusión de todos los discos para un volumen".

3.  Llame [**a IVssBackupComponents::P reRestore para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) notificar al escritor de ASR que se prepare para una operación de restauración. Llame [**a IVssAsync::QueryStatus tantas**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) veces como sea necesario hasta que el valor de estado devuelto en el *parámetro pHrResult* no sea VSS S \_ \_ ASYNC \_ PENDING.
4.  Restaure los datos. En la fase de restauración, ASR vuelve a configurar la ruta de acceso guid del volumen ( \\ \\ ? \\ Volumen{GUID}) para que cada volumen coincida con la ruta de acceso del GUID del volumen que se usó durante la fase de copia de seguridad. Sin embargo, las letras de unidad no se conservan, ya que esto provocaría colisiones con las letras de unidad que se asignan automáticamente en el entorno de recuperación. Por lo tanto, al restaurar los datos, el solicitante debe usar rutas de acceso GUID de volumen, no letras de unidad, para acceder a los volúmenes.
5.  Establezca la clave del Registro **HKLM** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** RestoreSession \\  para indicar el conjunto de volúmenes que se han restaurado o formatear.

    En esta clave, hay un valor denominado **RestoredVolumes con** el tipo de datos REG \_ MULTI \_ SZ. Si este valor no existe, debe crearlo. Con este valor, el solicitante debe crear una entrada GUID de volumen para cada volumen que se haya restaurado. Esta entrada debe tener el formato siguiente: \\ \\ ? \\ Volumen{78618c8f-aefd-11da-a898-806e6f6e6963}. Cada vez que se realiza una recuperación completa, ASR establece el valor **RestoredVolumes** en el conjunto de volúmenes restaurados por ASR. Si el solicitante restauró volúmenes adicionales, debe establecer este valor en la unión del conjunto de volúmenes que restauró el solicitante y el conjunto de volúmenes restaurados por ASR. Si el solicitante no usa asr, debe reemplazar la lista de volúmenes.

    También debe crear un valor denominado **LastInstance** con el tipo de datos REG \_ SZ. Esta clave debe contener una cookie aleatoria que identifique de forma única la operación de restauración actual. Dicha cookie se puede crear mediante las [**funciones UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) [**y UuidToString.**](/windows/win32/api/rpcdce/nf-rpcdce-uuidtostring) Cada vez que se realiza una recuperación completa, ASR restablece este valor del Registro para notificar a los solicitantes y a las aplicaciones de copia de seguridad que no son de VSS que se ha producido la recuperación.

6.  Llame [**a IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) para indicar el final de la operación de restauración. Llame [**a IVssAsync::QueryStatus tantas**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) veces como sea necesario hasta que el valor de estado devuelto en el *parámetro pHrResult* no sea VSS S \_ \_ ASYNC \_ PENDING.

En la fase de restauración, ASR puede crear o quitar particiones para restaurar el equipo a su estado anterior. Los solicitantes no deben intentar asignar números de disco de la fase de copia de seguridad a la fase de restauración.

Durante la restauración, el solicitante debe excluir el disco que contiene el conjunto de copia de seguridad del solicitante. De lo contrario, la operación de restauración puede sobrescribir el conjunto de copia de seguridad.

Durante la restauración, se excluye un disco si no se seleccionó como componente durante la copia de seguridad o si se excluye explícitamente mediante una llamada a [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) con la opción "ExcludeDisk" durante la restauración.

Es importante tener en cuenta que durante la recuperación ante desastres de WinPE, la funcionalidad de escritura de ASR está presente, pero no hay otros escritores disponibles y el servicio VSS no se está ejecutando. Una vez completada la recuperación ante desastres de WinPE, el equipo se ha reiniciado y el sistema operativo Windows se está ejecutando con normalidad, se puede iniciar el servicio VSS y el solicitante puede realizar cualquier operación de restauración adicional que requiera la participación de escritores distintos del escritor de ASR.

Si durante la sesión de restauración la aplicación de copia de seguridad detecta que los identificadores únicos del volumen no han cambiado y, por tanto, todos los volúmenes del momento de la copia de seguridad están presentes e intactos en WinPE, la aplicación de copia de seguridad puede continuar con la restauración solo del contenido de los volúmenes, sin que asr esté relacionado con ASR. En este caso, la aplicación de copia de seguridad debe indicar que el equipo se restauró estableciendo la siguiente clave del Registro en el sistema operativo restaurado: **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession**

En esta clave, especifique **LastInstance** para el nombre del valor, REG SZ para el tipo de valor y una cookie aleatoria (como un GUID creado por la \_ [**función UuidCreate)**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) para los datos de valor.

Si durante la sesión de restauración la aplicación de copia de seguridad detecta que uno o varios volúmenes han cambiado o faltan, la aplicación de copia de seguridad debe usar ASR para realizar la restauración. ASR volverá a crear los volúmenes exactamente como estaban en el momento de la copia de seguridad y establecerá la clave del Registro **RestoreSession.**

## <a name="excluding-all-disks-for-a-volume"></a>Exclusión de todos los discos de un volumen

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



 

 
