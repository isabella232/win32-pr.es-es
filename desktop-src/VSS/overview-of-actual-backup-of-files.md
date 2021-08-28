---
description: VSS permite a un solicitante acceder a la instantánea de volúmenes que contienen datos para la copia de seguridad y copiar datos en medios de copia de seguridad.
ms.assetid: 187f26f2-f191-4703-9bde-3357f1ceef0c
title: Información general sobre la copia de seguridad real de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2413111467014b666d219a7a1e92efad26302e5c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475701"
---
# <a name="overview-of-actual-backup-of-files"></a>Información general sobre la copia de seguridad real de archivos

VSS permite a un solicitante acceder a la instantánea de volúmenes que contienen datos para la copia de seguridad y copiar datos en medios de copia de seguridad. Los escritores suelen continuar con el funcionamiento normal durante este proceso. Para obtener más información, vea [Información general sobre el procesamiento de una copia de seguridad en VSS.](overview-of-processing-a-backup-under-vss.md)

En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para que se haga una copia de seguridad de los archivos.




| Acción del solicitante | Evento | Acción del escritor | 
|------------------|-------|---------------|
| Acceda a los archivos del volumen copiado en la sombra (vea <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties"><strong>IVssBackupComponents::GetSnapshotProperties</strong></a>, <a href="/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop"><strong>VSS_SNAPSHOT_PROP</strong></a>) | None | None | 
| Genere la lista de archivos de los que se va a realizar una copia de seguridad y copie los datos de los archivos en los medios de copia de seguridad. | None | None | 
| Indique si la copia de seguridad se ha hecho correctamente o no <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded"><strong>con IVssBackupComponents::SetBackupSucceeded.</strong></a> | None | None | 
| El solicitante indica que la copia de seguridad se ha completado llamando a <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents::BackupComplete.</strong></a> | <a href="vssgloss-b.md"><em>BackupComplete</em></a> | Realice cualquier limpieza posterior a la copia de seguridad (vea <a href="/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete"><strong>CVssWriter::OnBackupComplete</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents"><strong>IVssWriterComponents</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent"><strong>IVssComponent</strong></a>). | 
| El solicitante espera a que todos los escritores confirmen la recepción del evento <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents::BackupComplete</strong></a> mediante <a href="/windows/desktop/api/Vss/nn-vss-ivssasync"><strong>IVssAsync</strong></a>. También debe comprobar el estado del sistema de escritura (vea <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus"><strong>IVssBackupComponents::GatherWriterStatus</strong></a>, <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus"><strong>IVssBackupComponents::GetWriterStatus</strong></a>). El solicitante debe llamar a <strong>GatherWriterStatus en</strong> este momento para que la sesión de escritor se establezca en un estado completado.<blockquote>[!Note]<br />Esto solo es necesario en Windows Server 2008 con Service Pack 2 (SP2) y versiones anteriores.</blockquote><br /> | None | None | 
| Guarde el documento componentes de copia de seguridad y cada documento de metadatos del escritor en documentos XML, que se pueden escribir en los medios de copia de seguridad (vea <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml"><strong>IVssBackupComponents::SaveAsXML</strong></a> e <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml"><strong>IVssExwriterMetadata::SaveAsXML).</strong></a> | None | None | 




 

## <a name="writer-actions-during-backup-of-files"></a>Acciones de escritor durante la copia de seguridad de archivos

Una vez completada la instantánea, todas las operaciones de E/S del sistema de las que se está haciendo una copia de seguridad deben poder reanudarse sin interrumpir la integridad de la copia de seguridad. Esta es una de las principales motivaciones para tener la funcionalidad de instantánea.

Por lo tanto, al igual que en la fase de detección (consulte Información general de la fase de detección de copia de [seguridad),](overview-of-the-backup-discovery-phase.md)hay pocas demandas en los escritores mientras se hace una copia de seguridad de los archivos.

Una vez completada una copia de seguridad y un solicitante ha generado un evento [*BackupComplete,*](vssgloss-b.md) VSS llamará al método [**CVssWriter::OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) de cada escritor, un método virtual que, de forma predeterminada, simplemente devuelve **TRUE.** Sin embargo, los escritores pueden invalidar la implementación predeterminada y realizar acciones como quitar los archivos temporales restantes, o usar la [](vssgloss-e.md) interfaz [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) con la que se llama para comprobar el estado de la copia de seguridad de cada uno de sus componentes incluidos explícitamente (y cualquier conjunto de componentes que puedan definir) recuperando el objeto [**IVssComponent correspondiente.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) [](vssgloss-c.md) A continuación, el escritor puede determinar y actuar sobre el éxito o error de la copia de seguridad llamando a [**IVssComponent:GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded). El valor devuelto por **IVssComponent:GetBackupSucceeded** solo será **TRUE** si se [](vssgloss-i.md) ha realizado correctamente una copia de seguridad de todos los archivos incluidos explícitamente en el componente y todos los incluidos implícitamente de cualquiera de sus [*subcomponentes.*](vssgloss-s.md)

Una vez completada la llamada a [**CVssWriter::OnBackupComplete,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) el solicitante debe llamar a [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (para cada sistema de escritura) una última vez. La memoria de estado de sesión del escritor es un recurso limitado y los escritores deben volver a usar los estados de sesión. Este paso marca el estado de sesión de copia de seguridad del escritor como completado y notifica a VSS que esta ranura de sesión de copia de seguridad se puede reutilizar mediante una operación de copia de seguridad posterior.

## <a name="requester-actions-during-backup-of-files"></a>Acciones del solicitante durante la copia de seguridad de archivos

Como se indicó en [Información](overview-of-the-backup-discovery-phase.md)general de la fase de detección de copia de seguridad, no debe generar la lista real de archivos de los que se va a realizar una copia de seguridad hasta que se haya completado la instantánea.

El [*objeto de dispositivo*](vssgloss-d.md) correspondiente a la instantánea de un volumen determinado se usa para obtener acceso a los archivos del volumen de instantáneas una vez completada la instantánea. El objeto de dispositivo se obtiene del objeto [**PROP DE INSTANTÁNEA \_ \_ DE VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) devuelto por [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties). Cada instantánea de un conjunto de instantáneas tendrá su propio objeto de dispositivo.

A continuación, el objeto de dispositivo y las rutas de acceso obtenidas de las especificaciones del documento de metadatos del escritor de componentes se usan para seleccionar archivos para la copia de seguridad. Consulte Requester Access to Shadow Copied Data (Acceso del solicitante [a los datos copiados en la sombra)](requestor-access-to-shadow-copied-data.md) para obtener más información.

Los archivos que se incluirán en la lista de copia [](vssgloss-s.md)de seguridad dependen de la naturaleza de la copia de seguridad determinada, de la capacidad de selección de componentes para la copia de seguridad y de la estructura de ruta de acceso lógica del escritor (vea Trabajar con capacidad de selección para copia de [seguridad).](working-with-selectability-for-backup.md)

Además de los archivos especificados en los componentes, un escritor determinado también puede tener archivos excluidos explícitamente. Siempre se debe respetar la exclusión de archivos, independientemente de los componentes seleccionados.

También como se indica en [Información](overview-of-the-backup-discovery-phase.md)general de la fase de detección de copia de seguridad, puede aparecer una carpeta montada o un punto de reantal en una instantánea y se puede realizar una copia de seguridad. Sin embargo, no se puede atravesar una carpeta montada o un punto de reanual en el volumen de instantáneas (vea Trabajar con carpetas montadas y puntos [de reanual).](working-with-reparse-and-mount-points.md)

También se debe tener cuidado durante [](vssgloss-a.md) una operación de copia de seguridad si la ruta de acceso alternativa devuelta por [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) no está en blanco. Una ruta de acceso [](vssgloss-a.md) alternativa difiere de una asignación de ubicación alternativa en que solo se usa durante las copias de seguridad, mientras que una asignación de ubicación alternativa solo se usa durante las restauraciones.

En este caso, no se va a realizar una copia de seguridad de los datos desde su ubicación normal (indicada por [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), sino desde la ubicación devuelta por [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation). Durante la restauración, el archivo debe devolverse a su ubicación normal. Consulte [Ubicaciones de copia de seguridad y restauración no predeterminadas](non-default-backup-and-restore-locations.md) para obtener más información.

VSS no hace ninguna restricción en el mecanismo real de copia de seguridad de datos en un medio de almacenamiento o en la elección de ese medio. Sin embargo, se recomienda que los archivos de cada componente de cada instancia de escritor [*se*](vssgloss-w.md) procese como una unidad. Consulte [Generación de un conjunto de copia de seguridad](generating-a-backup-set.md) para obtener una explicación de los procedimientos recomendados para generar la lista de archivos de copia de seguridad.

El éxito o error de la copia de seguridad de cualquiera de los archivos administrados por un componente determinado y (si define un conjunto de componentes [*)*](vssgloss-c.md)sus [*subcomponentes*](vssgloss-s.md) para una instancia de escritor determinada se deben conservar en el documento Componentes de copia de seguridad llamando a [**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded). Si no se puede hacer una copia de seguridad de cualquier archivo administrado por un componente o conjunto de componentes, se dice que se produce un error en todo el componente. Siempre se debe registrar la información exacta sobre qué archivo no se pudo realizar la copia de seguridad.

Los desarrolladores pueden encontrar útil almacenar un registro en el medio de copia de seguridad del que se hace una copia de seguridad de los archivos, los componentes y el conjunto de componentes del que eran miembros, su especificación y cuáles eran sus rutas de acceso originales. También puede ser útil almacenar información como la definición de componentes de cada escritor. Esto puede facilitar la operación de recuperación. Sin embargo, estos detalles se quedan al desarrollador del solicitante.

Dado que los escritores pueden modificar el documento componentes de copia de seguridad mientras se administra el evento [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) generado por la llamada del solicitante a [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), el documento componentes de copia de seguridad no debe guardarse hasta que se haya completado la llamada asincrónica.

Aunque puede tener lugar antes, también es un momento conveniente para guardar el documento de metadatos del escritor.

Es muy importante que tanto el documento de componentes de copia de seguridad como los documentos de metadatos del escritor se conserven mediante [**IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) e [**IVssExgvWriterMetadata::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml). Si no lo están, no será posible usar VSS durante la restauración de archivos.

Además de almacenar los metadatos originales, algunas aplicaciones de copia de seguridad pueden resultar útiles para guardar una copia de su propia lista de los archivos (en su propio formato optimizado) y su escritor, componente, procedimiento de restauración e información de ubicación asociados en los medios de copia de seguridad para su posterior recuperación. Esta lista se puede usar para evitar algunos de los análisis y la comparación de los documentos de metadatos del escritor y los documentos del componente de copia de seguridad durante la restauración.

Los volúmenes de los que se va a hacer una copia de seguridad pueden tener datos que no administran los escritores de VSS. Se puede hacer una copia de seguridad de estos datos y deben realizarse desde el volumen copiado en la sombra, donde estarán en un estado [*coherente con los bloqueos.*](vssgloss-c.md) Consulte [Copias de seguridad sin participación del escritor](backups-without-writer-participation.md) para obtener más información.

 

 




