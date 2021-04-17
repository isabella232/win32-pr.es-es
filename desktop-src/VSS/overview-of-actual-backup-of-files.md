---
description: VSS permite que un solicitante tenga acceso a la instantánea de los volúmenes que contienen datos para copia de seguridad y para copiar los datos en un medio de copia de seguridad.
ms.assetid: 187f26f2-f191-4703-9bde-3357f1ceef0c
title: Información general sobre la copia de seguridad real de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a504ff5a41725e33a2eb27792a3c6c89d00276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696997"
---
# <a name="overview-of-actual-backup-of-files"></a>Información general sobre la copia de seguridad real de archivos

VSS permite que un solicitante tenga acceso a la instantánea de los volúmenes que contienen datos para copia de seguridad y para copiar los datos en un medio de copia de seguridad. Normalmente, los escritores continúan con el funcionamiento normal durante este proceso. Para obtener más información, vea [información general sobre el procesamiento de una copia de seguridad en VSS](overview-of-processing-a-backup-under-vss.md).

En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para realizar una copia de seguridad de los archivos.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Acción del solicitante</th>
<th>Evento</th>
<th>Acción del escritor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Acceder a los archivos en el volumen de copia sombra (consulte <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties"><strong>IVssBackupComponents:: GetSnapshotProperties</strong></a>, <a href="/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop"><strong>VSS_SNAPSHOT_PROP</strong></a>)</td>
<td>None</td>
<td>None</td>
</tr>
<tr class="even">
<td>Generar la lista de archivos de los que se realizará una copia de seguridad y copiar los datos de archivos en los medios de copia de seguridad.</td>
<td>None</td>
<td>None</td>
</tr>
<tr class="odd">
<td>Indica si la copia de seguridad se realizó correctamente o no con <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded"><strong>IVssBackupComponents:: SetBackupSucceeded</strong></a>.</td>
<td>None</td>
<td>None</td>
</tr>
<tr class="even">
<td>El solicitante indica que la copia de seguridad se ha completado llamando a <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents:: BackupComplete</strong></a>.</td>
<td><a href="vssgloss-b.md"><em>BackupComplete</em></a></td>
<td>Realice cualquier limpieza posterior a la copia de seguridad (vea <a href="/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete"><strong>CVssWriter:: OnBackupComplete</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents"><strong>IVssWriterComponents</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent"><strong>IVssComponent</strong></a>).</td>
</tr>
<tr class="odd">
<td>El solicitante espera a que todos los escritores confirmen la recepción del evento <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents:: BackupComplete</strong></a> mediante <a href="/windows/desktop/api/Vss/nn-vss-ivssasync"><strong>IVssAsync</strong></a>. También debe comprobar el estado del escritor (consulte <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus"><strong>IVssBackupComponents:: GatherWriterStatus</strong></a>, <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus"><strong>IVssBackupComponents:: GetWriterStatus</strong></a>). El solicitante debe llamar a <strong>GatherWriterStatus</strong> en este momento para que la sesión del escritor se establezca en un estado completado.
<blockquote>
[!Note]<br />
Esto solo es necesario en Windows Server 2008 con Service Pack 2 (SP2) y versiones anteriores.
</blockquote>
<br/></td>
<td>None</td>
<td>None</td>
</tr>
<tr class="even">
<td>Guarde el documento componentes de copia de seguridad y cada documento de metadatos de escritor en documentos XML, que se pueden escribir en el medio de copia de seguridad (vea <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml"><strong>IVssBackupComponents:: SaveAsXML</strong></a> y <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml"><strong>IVssExamineWriterMetadata:: SaveAsXML</strong></a>).</td>
<td>None</td>
<td>None</td>
</tr>
</tbody>
</table>



 

## <a name="writer-actions-during-backup-of-files"></a>Acciones del escritor durante la copia de seguridad de archivos

Una vez completada la instantánea, todas las operaciones de e/s en el sistema del que se realiza una copia de seguridad deberían ser capaces de reanudar sin interrumpir la integridad de la copia de seguridad. Esta es una de las motivaciones principales para tener la funcionalidad de la instantánea.

Por lo tanto, como en la fase de detección (consulte [información general de la fase de detección de copias de seguridad](overview-of-the-backup-discovery-phase.md)), hay pocas peticiones en los escritores mientras se realiza una copia de seguridad de los archivos.

Una vez que se ha completado una copia de seguridad y un solicitante ha generado un evento [*BackupComplete*](vssgloss-b.md) , VSS llamará al método [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) de cada escritor, un método virtual que, de forma predeterminada, simplemente devuelve **true**. Sin embargo, los escritores pueden invalidar la implementación predeterminada y realizar acciones como la eliminación de los archivos temporales restantes, o bien usar la interfaz [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) con la que se llama para comprobar el estado de la copia de seguridad de cada uno de los componentes que se [*incluyen explícitamente*](vssgloss-e.md) (y cualquier [*conjunto de componentes*](vssgloss-c.md) que puedan definir) recuperando el objeto [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente. Después, el escritor puede determinar, y actuar sobre, el éxito o el error de la copia de seguridad mediante una llamada a [**IVssComponent: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded). El valor devuelto por **IVssComponent: GetBackupSucceeded** solo será **true** si se ha realizado correctamente la copia de seguridad de todos los archivos incluidos explícitamente en el componente y todos los [*incluidos implícitamente*](vssgloss-i.md) de cualquiera de sus [*subcomponentes*](vssgloss-s.md) .

Cuando se ha completado la llamada a [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) , el solicitante debe llamar a [**Ivssbackupcomponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) y [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (para cada escritor) una última vez. La memoria de estado de sesión del escritor es un recurso limitado y los escritores deben volver a usar los Estados de sesión. Este paso marca el estado de la sesión de copia de seguridad del escritor como completado e informa a VSS de que esta ranura de sesión de copia de seguridad se puede volver a usar en una operación de copia de seguridad posterior.

## <a name="requester-actions-during-backup-of-files"></a>Acciones del solicitante durante la copia de seguridad de archivos

Como se indicó en [información general de la fase de detección de copias de seguridad](overview-of-the-backup-discovery-phase.md), no debe generar la lista real de archivos de los que se realizará una copia de seguridad hasta que se haya completado la instantánea.

El [*objeto de dispositivo*](vssgloss-d.md) correspondiente a la instantánea de un volumen determinado se usa para obtener acceso a los archivos del volumen de instantáneas una vez que se ha completado la instantánea. El objeto de dispositivo se obtiene del objeto de [**\_ \_ prop de instantáneas de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) devuelto por [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties). Cada instantánea de un conjunto de instantáneas tendrá su propio objeto de dispositivo.

El objeto de dispositivo y las rutas de acceso obtenidas a partir de las especificaciones de los documentos de metadatos de escritura se usan para seleccionar archivos para copia de seguridad. Vea [acceso del solicitante a los datos de copia sombra](requestor-access-to-shadow-copied-data.md) para obtener más información.

Los archivos que se incluirán en la lista de copia de seguridad dependen de la naturaleza de la copia de seguridad determinada, tras la selección de componentes [*para la copia de seguridad*](vssgloss-s.md)y la estructura de ruta de acceso lógica del escritor (vea [trabajar con la selección de copias de seguridad](working-with-selectability-for-backup.md)).

Además de los archivos especificados en los componentes, un escritor determinado también puede tener archivos excluidos explícitamente. La exclusión de archivos debe respetarse siempre, independientemente de los componentes seleccionados.

También como se indicó en [información general de la fase de detección de copias de seguridad](overview-of-the-backup-discovery-phase.md), puede aparecer una carpeta montada o un punto de reanálisis en una instantánea y se puede realizar una copia de seguridad de ella. Sin embargo, no se puede atravesar una carpeta montada o un punto de reanálisis en el volumen de copia sombra (vea [trabajar con carpetas montadas y puntos de análisis](working-with-reparse-and-mount-points.md)).

También se debe tener cuidado durante una operación de copia de seguridad, si la [*ruta de acceso alternativa*](vssgloss-a.md) devuelta por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) no está en blanco. Una ruta de acceso alternativa difiere de una [*asignación de ubicación alternativa*](vssgloss-a.md) en que solo se usa durante las copias de seguridad, mientras que una asignación de ubicación alternativa se usa solo durante las restauraciones.

En este caso, no se realizará una copia de seguridad de los datos desde su ubicación normal (indicada por [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), sino desde la ubicación devuelta por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation). En la restauración, el archivo se debe devolver a su ubicación normal. Vea [ubicaciones de copia de seguridad y restauración no predeterminadas](non-default-backup-and-restore-locations.md) para obtener más información.

VSS no impone restricciones en el mecanismo real de copia de seguridad de datos en un medio de almacenamiento ni en la elección de ese medio. Sin embargo, se recomienda que los archivos de cada componente de cada [*instancia del escritor*](vssgloss-w.md) se procesen como una unidad. Vea [generar un conjunto de copia de seguridad](generating-a-backup-set.md) para obtener una explicación de los procedimientos recomendados para generar la lista de archivos de copia de seguridad.

El éxito o el error de la copia de seguridad de cualquiera de los archivos administrados por un componente determinado y, si define un [*conjunto de componentes*](vssgloss-c.md), sus [*subcomponentes*](vssgloss-s.md) de una instancia de escritor determinada deben conservarse en el documento de componentes de copia de seguridad llamando a [**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded). Si no se puede realizar una copia de seguridad de un archivo administrado por un componente o un conjunto de componentes, se dice que se produce un error en todo el componente. Siempre se debe registrar la información exacta sobre el archivo del que no se pudo realizar la copia de seguridad.

Es posible que los desarrolladores le resulten útiles para almacenar un registro en el medio de copia de seguridad del que se realizan copias de seguridad de los archivos, los componentes y conjuntos de componentes de los que eran miembros, su especificación y sus rutas de acceso originales. También puede ser útil almacenar información, como la definición de componente de cada escritor. Esto puede hacer que la operación de recuperación sea más sencilla. Sin embargo, estos detalles se dejan en el desarrollador del solicitante.

Dado que los escritores pueden modificar el documento de componentes de copia de seguridad mientras controlan el evento de [**instantáneas**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) que genera la llamada del solicitante a [**IVssBackupComponents::D Osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), el documento componentes de copia de seguridad no debe guardarse hasta que se haya completado la llamada asincrónica.

Aunque puede tener lugar antes, esto también es un momento conveniente para guardar el documento de metadatos del escritor.

Es muy importante que el documento componentes de copia de seguridad y los documentos de metadatos del escritor se conserven mediante [**IVssBackupComponents:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) y [**IVssExamineWriterMetadata:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml). Si no es así, no será posible usar VSS durante la restauración de archivos.

Además de almacenar los metadatos originales, algunas aplicaciones de copia de seguridad pueden resultar útiles para guardar una copia de su propia lista de archivos (en su propio formato optimizado), y su escritor, componente, procedimiento de restauración y información de ubicación asociados, en el medio de copia de seguridad para su recuperación posterior. Esta lista se puede usar para evitar algunos de los análisis y la comparación de los documentos de metadatos del escritor y los documentos de componentes de copia de seguridad durante la restauración.

Los volúmenes de los que se realiza una copia de seguridad pueden tener datos no administrados por escritores de VSS. Se puede realizar una copia de seguridad de estos datos desde el volumen de instantáneas, donde estará en un [*estado coherente con el bloqueo*](vssgloss-c.md). Consulte [copias de seguridad sin participación del escritor](backups-without-writer-participation.md) para obtener más información.

 

 




