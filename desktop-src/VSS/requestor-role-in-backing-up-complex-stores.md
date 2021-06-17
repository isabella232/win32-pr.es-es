---
description: Obtenga información sobre el rol de solicitante en las copias de seguridad incrementales y diferenciales, que requieren una estrecha cooperación entre los solicitantes y los escritores.
ms.assetid: 00391a49-8c81-4518-88a2-741ad5ee4ac3
title: Rol del solicitante en la copia de seguridad de almacenes complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dfa1b0b1837bacc2488b6bd9e3ffdd51b92c0
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262187"
---
# <a name="requester-role-in-backing-up-complex-stores"></a>Rol del solicitante en la copia de seguridad de almacenes complejos

Al igual que con todas las [](vssgloss-d.md) operaciones importantes en VSS, las copias de seguridad [*incrementales*](vssgloss-i.md) y diferenciales requieren una estrecha cooperación entre solicitantes y escritores.

## <a name="backup-type"></a>Tipo de copia de seguridad

La infraestructura proporciona compatibilidad especial para cinco tipos de copia de seguridad. A continuación se detalla la descripción de estos pasos:

-   Full **(VSS \_ BT \_ FULL).** Se realizará una copia de seguridad de los archivos, independientemente de la fecha de la última copia de seguridad. Se actualizará el historial de copia de seguridad de cada archivo y este tipo de copia de seguridad se puede usar como base de una copia de seguridad incremental o diferencial. Si hay archivos de registro, pueden truncarse como resultado de esta copia de seguridad.

    La restauración de una copia de seguridad completa solo requiere una sola imagen de copia de seguridad.

-   Diferencial **(VSS \_ BT \_ DIFFERENTIAL).** La API de VSS se usa para asegurarse de que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa se copiarán en un medio de almacenamiento. se omite toda la información de copia de seguridad intermedia. Esto puede incluir archivos completos o intervalos específicos dentro de los archivos. Una copia de seguridad diferencial está asociada a una copia de seguridad completa y, por lo general, no se puede restaurar hasta que se haya restaurado la copia de seguridad completa. Si hay archivos de registro, normalmente no se truncarán como resultado de esta copia de seguridad.

    La restauración de una copia de seguridad diferencial requiere la imagen de copia de seguridad original y la imagen de copia de seguridad diferencial más reciente realizada desde la última copia de seguridad completa.

-   Incremental (**VSS \_ BT \_ INCREMENTAL**). La API de VSS se usa para asegurarse de que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa o incremental se copiarán en un medio de almacenamiento. Esto puede incluir archivos completos o intervalos específicos dentro de los archivos. Algunos escritores no permiten que las copias de seguridad incrementales se mezclen con copias de seguridad diferenciales. Si hay archivos de registro, pueden truncarse como resultado de esta copia de seguridad.

    La restauración de una copia de seguridad incremental requiere la imagen de copia de seguridad original y todas las imágenes de copia de seguridad incremental realizadas desde la copia de seguridad inicial.

-   Copia de seguridad de registros (**VSS \_ BT \_ LOG**). Solo se realizará una copia de seguridad de los archivos de registro de un escritor (archivos agregados a un componente con el método [**IVssCreateWriterMetadata::AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) y recuperados mediante una llamada a [**IVssWMComponent::GetDatabaseLogFile).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) Este tipo de copia de seguridad es específico de VSS. Las copias de seguridad de registros tienden a realizarse con bastante frecuencia. Normalmente, el archivo de registro se truncará como resultado de esta copia de seguridad.
-   Copia de seguridad (**COPIA DE VSS \_ BT \_**). Al igual que el tipo de copia de seguridad FULL de VSS BT, se realizará una copia de seguridad de los archivos \_ \_ independientemente de la fecha de la última copia de seguridad. Sin embargo, el historial de copia de seguridad de cada archivo no se actualizará y este tipo de copia de seguridad no se puede usar como base de una copia de seguridad incremental o diferencial. Los archivos de registro nunca se deben truncar como resultado de una copia de seguridad.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Compatibilidad con archivos parciales
</dt> <dd>

Algunos escritores admiten la restauración de archivos mediante la sobrescritura de partes de los archivos que administran. Un solicitante puede estar diseñado para aprovechar esto y, si es así, lo indica estableciendo la información en [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

El solicitante especifica qué tipo de copia de seguridad se realiza a través del parámetro *backupType* de [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Diferentes escritores admitirán diferentes tipos de copia de seguridad. Después de llamar a [**IVssBackupComponents::GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) el solicitante puede determinar qué tipos de copia de seguridad admite un escritor determinado llamando a [**IVssExwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). El valor devuelto es una máscara de bits que indica la compatibilidad con diferentes tipos de copia de seguridad. **VSS \_ BS \_ DIFFERENTIAL** indica compatibilidad con copias de seguridad diferenciales, INCREMENTAL de **VSS \_ BS \_** para copias de seguridad incrementales, REGISTRO de **\_ VSS BS \_** para copias de seguridad de registros y COPIA DE **\_ VSS BS \_** para copias de seguridad de copia; todos los escritores deben admitir copias de seguridad completas. Si un escritor no admite la combinación de copias de seguridad incrementales con copias de seguridad diferenciales, también se agregará la marca DIFERENCIAL INCREMENTAL EXCLUSIVO de **\_ VSS \_ \_ \_ BS.** Si el solicitante realiza una copia de seguridad incremental o diferencial y un escritor determinado no admite ese tipo de copia de seguridad, se debe realizar una copia de seguridad completa en ese sistema de escritura.

## <a name="backup-stamps"></a>Marcas de copia de seguridad

Las copias de seguridad incrementales y diferenciales siempre están vinculadas a una copia de seguridad anterior. Hay dos maneras de vincular las copias de seguridad. En el caso de los almacenes de datos simples, el solicitante puede realizar un seguimiento de la correlación entre las copias de seguridad. Sin embargo, para almacenes de datos más complejos, el escritor deberá mantener su propia marca de tiempo con la copia de seguridad. esta marca de tiempo puede realizar un seguimiento de la posición del registro, la información del punto de control, y así sucesivamente. El solicitante puede determinar si un escritor determinado necesita almacenar su propia marca de tiempo comprobando el bit **\_ \_ TIMESTAMPED de VSS BS** en el valor devuelto por [**IVssExwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

Los escritores que almacenan una marca de tiempo en una copia de seguridad agregarán la marca de tiempo durante el procesamiento de [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o al procesar [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). El solicitante puede obtener esta marca de tiempo llamando a [**IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp). Al realizar una copia de seguridad incremental o diferencial, el solicitante debe vincular la copia de seguridad actual a alguna copia de seguridad anterior. Para ello, se obtiene la marca de tiempo de la copia de seguridad anterior de un componente específico y se pasa a la función [**IVssBackupComponents::SetPreviousBackupStamp;**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) esto debe hacerse para cada componente del que se hizo una copia de seguridad en la copia de seguridad anterior.

## <a name="backing-up-files"></a>Copia de seguridad de archivos

### <a name="backing-up-files-reported-by-writer"></a>Copia de seguridad de archivos notificados por Writer

Cada especificación de archivo que un escritor agrega a sus metadatos durante la fase GatherWriterMetadata contiene una máscara de tipo de copia de seguridad que especifica cuándo se debe realizar una copia de seguridad del archivo. El solicitante determina cuál es esta máscara llamando a [**IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask). Los valores de esta máscara se usan para determinar para qué tipos de copia de seguridad debe realizarse la copia de seguridad de la especificación de archivo. La máscara puede contener uno o varios de los siguientes valores de bits:

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**SE REQUIERE COPIA \_ DE SEGURIDAD COMPLETA DE VSS FSBT \_ \_ \_**
</dt> <dd>

Necesario para copias de seguridad completas.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**SE REQUIERE COPIA \_ DE SEGURIDAD DIFERENCIAL DE VSS FSBT \_ \_ \_**
</dt> <dd>

Necesario para copias de seguridad diferenciales.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**SE REQUIERE COPIA \_ DE SEGURIDAD INCREMENTAL DE VSS FSBT \_ \_ \_**
</dt> <dd>

Necesario para copias de seguridad incrementales.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**SE REQUIERE LA \_ COPIA DE SEGURIDAD DE REGISTROS DE VSS FSBT \_ \_ \_**
</dt> <dd>

Necesario para las copias de seguridad de registros.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**VSS \_ FSBT \_ ALL \_ BACKUP \_ REQUIRED**
</dt> <dd>

Obligatorio para todos los tipos de copia de seguridad; este es el valor predeterminado.

</dd> </dl>

Esta especificación invalida la especificación de selectividad del componente. Por ejemplo, considere un componente cuyos archivos están marcados con **VSS \_ FSBT \_ LOG BACKUP \_ \_ REQUIRED,** pero no con **VSS \_ FSBT \_ FULL BACKUP \_ \_ REQUIRED**. Supongamos que este componente no se puede seleccionar para la copia de seguridad (*bSelectable* era false cuando se llamó a [**IVssCreateWriterMetadata::AddComponent).**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) En el caso de una copia de seguridad de registros, esto significa que siempre se debe realizar una copia de seguridad de todos los archivos de este componente. Sin embargo, en el caso de una copia de seguridad completa, no es necesario hacer una copia de seguridad de ninguno de los archivos, a pesar de que la selectividad del componente implica que se debe realizar una copia de seguridad.

### <a name="backup-by-last-modify-time"></a>Copia de seguridad por hora de última modificación

La información de especificación de archivo especificada en la fase [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) no proporciona al solicitante información sobre lo que ha cambiado desde la última copia de seguridad. Una manera de que un escritor indique cambios en el solicitante es mediante el mecanismo de archivo diferenciado. Un sistema de escritura puede especificar que solo se debe realizar una copia de seguridad de determinados archivos de un componente si se han modificado desde un momento determinado. el escritor puede especificar estos archivos en [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o [**en IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Un solicitante puede determinar estos archivos llamando a [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) e [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). Si la especificación de archivo coincide con un conjunto de **IVssBackupComponents::GatherWriterMetadata** (que actualmente es válido en función de la máscara de tipo de copia de seguridad), la información de archivo diferenciada invalida la información anterior; Es decir, ahora solo se hace una copia de seguridad de los archivos que coinciden con esa especificación de archivo si se han modificado desde la hora especificada. La hora de la última modificación se comunica mediante una [**estructura FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) Si el valor de esta estructura es cero, esto implica que se debe determinar la hora de la última modificación en función del registro del solicitante de la hora de la última copia de seguridad.

### <a name="partial-file-backup"></a>Copia de seguridad parcial de archivos

Otra manera de que un escritor indique cambios en el solicitante es mediante el mecanismo de archivo parcial. Un escritor puede especificar intervalos de bytes dentro de los archivos de componentes de los que es necesario realizar una copia de seguridad; el escritor puede especificar estos intervalos de archivos en [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o [**en IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Un solicitante puede determinar estos archivos llamando a [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). **IVssComponent::GetPartialFile** devolverá una ruta de acceso y un nombre de archivo que apuntan al archivo, y una cadena de intervalos que indica de qué se debe hacer una copia de seguridad en el archivo. Al igual que con los archivos con diferencias, si la ruta de acceso y el nombre de archivo coinciden con una especificación de archivo establecida por el escritor en [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), la información de archivo parcial invalida la configuración anterior. La cadena ranges puede tener dos formatos: puede especificar los intervalos directamente o puede especificar un archivo que contenga información de intervalos. Si especifica intervalos directamente, la sintaxis es una lista separada por comas del formato offset1:length1, offset2:length2, donde cada desplazamiento y longitud es un entero de 64 bits sin signo. Si especifica un archivo de intervalos, la cadena ranges debe establecerse en File= *filename*, donde *filename* es la ruta de acceso completa al archivo de intervalos. El propio archivo de intervalos es un archivo binario con formato de lista de enteros de 64 bits sin signo. El primer entero indica cuántos intervalos se representan en el archivo. Cada par de enteros subsiguiente representa el desplazamiento y la longitud de un intervalo. El solicitante también debe tener cuidado de realizar copias de seguridad y restaurar este archivo de intervalos.

### <a name="file-specification-rules"></a>Reglas de especificación de archivos

Las especificaciones de archivo agregadas a través del archivo diferenciado y los mecanismos de archivo parcial modificarán las especificaciones de archivo establecidas en [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) o agregarán archivos completamente nuevos. Si modifica las especificaciones de archivos establecidas en **IVssBackupComponents::GatherWriterMetadata** mediante el mecanismo de archivo parcial, un solicitante puede esperar que la especificación de archivo coincida exactamente con una de las especificaciones de archivo establecidas en el componente en **IVssBackupComponents::GatherWriterMetadata**. La especificación de archivo no se superpondrá parcialmente a otra especificación de archivo y no coincidirá con ninguna especificaciones de archivo en ningún otro de los componentes de ese escritor. Sin embargo, las especificaciones de archivo agregadas mediante el mecanismo de archivo parcial pueden superponerse parcialmente a otra especificación de archivo. Cuando esto es así, la especificación differenced-file o partial-file invalida el conjunto de especificaciones en **IVssBackupComponents::GatherWriterMetadata**. Las especificaciones generales de archivo pueden tener un valor de ubicación alternativa (devuelto por [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)) que indica un lugar alternativo desde el que obtener el archivo en el momento de la copia de seguridad. Si las especificaciones de archivo establecidas a través de los mecanismos de archivo parcial o de archivo diferenciado coinciden con una especificación de archivos existente que tiene una ubicación alternativa, los datos se deben seleccionar de esta ubicación alternativa. Si las especificaciones de archivo establecidas a través de los mecanismos de archivo diferenciado o de archivo parcial no coinciden con las especificaciones existentes para el componente, estos intervalos de archivos se deben agregar ahora a la copia de seguridad. El solicitante puede esperar que solo se agregarán archivos en volúmenes que ya se han incluido en el conjunto de instantáneas mediante uno de estos mecanismos.

### <a name="backup-without-a-shadow-copy"></a>Copia de seguridad sin instantáneas

Es posible que no sea necesario realizar una copia de seguridad de determinados tipos de archivos de un volumen de instantáneas. Por ejemplo, esto suele ser cierto para los archivos de registro de base de datos. Dado que los archivos de registro crecen de forma monónica y un escritor puede especificar exactamente qué partes del archivo se van a realizar con archivos parciales, a menudo será posible realizar una copia de seguridad del registro del volumen original. Como optimización, un escritor puede marcar qué archivos requieren instantáneas para diferentes tipos de copia de seguridad mediante la máscara de tipo de copia de seguridad. El valor devuelto por [**IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) puede contener uno o varios de los siguientes valores de bits:

<dl> <dt>

<span id="VSS_FSBT_FULL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_full_snapshot_required"></span>**SE REQUIERE UNA \_ INSTANTÁNEA COMPLETA DE VSS FSBT \_ \_ \_**
</dt> <dd>

Instantánea necesaria para copias de seguridad completas.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_differential_snapshot_required"></span>**INSTANTÁNEA DIFERENCIAL \_ DE VSS FSBT \_ \_ \_ REQUERIDA**
</dt> <dd>

Instantánea necesaria para las copias de seguridad diferenciales.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_incremental_snapshot_required"></span>**SE REQUIERE INSTANTÁNEA \_ INCREMENTAL DE VSS FSBT \_ \_ \_**
</dt> <dd>

Instantánea necesaria para las copias de seguridad incrementales.

</dd> <dt>

<span id="VSS_FSBT_LOG_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_log_snapshot_required"></span>**SE REQUIERE UNA \_ INSTANTÁNEA DE REGISTRO DE VSS FSBT \_ \_ \_**
</dt> <dd>

Instantánea necesaria para las copias de seguridad de registros.

</dd> <dt>

<span id="VSS_FSBT_ALL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_all_snapshot_required"></span>**VSS \_ FSBT \_ ALL \_ SNAPSHOT \_ REQUIRED**
</dt> <dd>

Instantánea necesaria para todos los tipos de copia de seguridad; este es el valor predeterminado.

</dd> </dl>

Si un volumen específico solo contiene componentes que no requieren una instantánea para esta copia de seguridad, el solicitante puede omitir el paso de creación de una instantánea para este volumen. Todos los datos de este volumen se pueden copiar en el medio de copia de seguridad directamente desde el volumen original.

## <a name="restoring-files"></a>Restaurar archivos

### <a name="sequential-restores"></a>Restauraciones secuenciales

Una vez que el solicitante ha terminado de realizar una operación de restauración, envía el evento PostRestore a todos los escritores. Por lo general, los escritores controlan este evento realizando operaciones de recuperación u otras operaciones posteriores a la restauración. Sin embargo, la restauración de copias de seguridad incrementales suele producirse como una secuencia de operaciones de restauración, una por cada copia de seguridad incremental. El solicitante debe informar al escritor de que dicha restauración está en curso para evitar que se haga la recuperación u otras operaciones no deseadas hasta que la restauración se haya realizado completamente. Para ello, se llama a [**IVssBackupComponents::SetAdditionalRestores.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) Este método se llama por componente e indica al escritor que hay más restauraciones para ese componente. Para la restauración final de la secuencia, la marca restauraciones adicionales debe establecerse en false (su valor predeterminado), lo que indica que se trata de la última restauración de la secuencia para ese componente.

### <a name="new-targets"></a>Nuevos destinos

Si es compatible con el sistema de escritura, el solicitante puede restaurar los archivos de datos en una ubicación que no sea la ubicación original en tiempo de copia de seguridad. El solicitante puede comprobar esta compatibilidad llamando a [**IVssExwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). El **bit VSS \_ BS WRITER SUPPORTS NEW \_ \_ \_ \_ TARGET** se establecerá si el escritor admite este comportamiento. El solicitante informa al escritor de la nueva ubicación mediante una llamada a [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) para cada especificación de archivo reubicado. El solicitante también puede decidir restaurar un archivo de intervalos específico en una ubicación diferente. El solicitante informa al escritor de este cambio mediante una llamada a [**IVssBackupComponents::SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

### <a name="directed-targets"></a>Destinos dirigidos

En escenarios de restauración complicados, es posible que un escritor quiera asignar intervalos de un archivo de copia de seguridad a intervalos diferentes del mismo archivo o de otro. Esto se puede hacer mediante el mecanismo de destino dirigido. El solicitante puede determinar después de la fase [**IVssBackupComponents::P reStore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) que este mecanismo se usa para un componente llamando a [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) y comprobando si se devuelve **VSS \_ RT \_ DIRECTED**. El solicitante puede obtener todas estas restauraciones redirigidas llamando a [**IVssComponent::GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) e [**IVssComponent::GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget). **IVssComponent::GetDirectedTarget** devolverá una ruta de acceso completa a un archivo de origen en la copia de seguridad y una ruta de acceso completa a un archivo de destino en el que se restaurará. También devuelve una lista de intervalos para cada uno de estos archivos. A continuación, el solicitante es responsable de restaurar los intervalos especificados en el archivo de origen a los intervalos asignados en el archivo de destino. El formato de la cadena de intervalos es el mismo que en [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile).

-   [Rol escritor en copias de seguridad incrementales y diferenciales de VSS](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Rol solicitante en copias de seguridad incrementales y diferenciales de VSS](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 
