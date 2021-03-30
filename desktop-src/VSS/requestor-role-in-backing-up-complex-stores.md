---
description: Como con todas las operaciones importantes de VSS, las copias de seguridad incrementales y diferenciales requieren una estrecha colaboración entre los solicitantes y los escritores.
ms.assetid: 00391a49-8c81-4518-88a2-741ad5ee4ac3
title: Rol de solicitante en copias de seguridad de almacenes complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197351e76b6861ee9b9d1e0589ef028c911430ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082480"
---
# <a name="requester-role-in-backing-up-complex-stores"></a>Rol de solicitante en copias de seguridad de almacenes complejos

Como con todas las operaciones importantes de VSS, las copias de seguridad [*incrementales*](vssgloss-i.md) y [*diferenciales*](vssgloss-d.md) requieren una estrecha colaboración entre los solicitantes y los escritores.

## <a name="backup-type"></a>Tipo de copia de seguridad

La infraestructura proporciona compatibilidad especial para cinco tipos de copia de seguridad. A continuación se detalla la descripción de estos pasos:

-   Completo (**VSS \_ BT \_ completo**). Se realizará una copia de seguridad de los archivos, independientemente de la fecha de la última copia de seguridad. Se actualizará el historial de copia de seguridad de cada archivo y este tipo de copia de seguridad se puede usar como base de una copia de seguridad incremental o diferencial. Si hay archivos de registro, se pueden truncar como resultado de esta copia de seguridad.

    La restauración de una copia de seguridad completa requiere una sola imagen de copia de seguridad.

-   Diferencial (**\_ \_ diferencial de VSS BT**). La API de VSS se usa para garantizar que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa se copien en un medio de almacenamiento. se omite toda la información de copia de seguridad intermedia. Esto puede incluir archivos completos o intervalos específicos dentro de los archivos. Una copia de seguridad diferencial está asociada a una copia de seguridad completa y, por lo general, no se puede restaurar hasta que se haya restaurado la copia de seguridad completa. Si hay archivos de registro, normalmente no se truncarán como resultado de esta copia de seguridad.

    La restauración de una copia de seguridad diferencial requiere la imagen de copia de seguridad original y la imagen de copia de seguridad diferencial más reciente realizada desde la última copia de seguridad completa.

-   Incremental (**se \_ \_ incremental de VSS BT**). La API de VSS se usa para asegurarse de que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa o incremental se copiarán en un medio de almacenamiento. Esto puede incluir archivos completos o intervalos específicos dentro de los archivos. Algunos escritores no permiten mezclar copias de seguridad incrementales con copias de seguridad diferenciales. Si hay archivos de registro, se pueden truncar como resultado de esta copia de seguridad.

    La restauración de una copia de seguridad incremental requiere la imagen de copia de seguridad original y todas las imágenes de copia de seguridad incremental realizadas desde la copia de seguridad inicial.

-   Copia de seguridad de registros (**\_ \_ registro de VSS BT**). Solo se realizará una copia de seguridad de los archivos de registro de un escritor (los archivos agregados a un componente con el método [**IVssCreateWriterMetadata:: AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) y recuperados mediante una llamada a [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)). Este tipo de copia de seguridad es específico de VSS. Las copias de seguridad de registros tienden a realizarse con mucha frecuencia. Normalmente, el archivo de registro se truncará como resultado de esta copia de seguridad.
-   Copia de seguridad (copia de **VSS \_ BT \_**). Al igual que el \_ tipo de copia de seguridad completa de VSS BT, se realizará \_ una copia de seguridad de los archivos, independientemente de su fecha de última copia de seguridad. Sin embargo, el historial de copia de seguridad de cada archivo no se actualizará y este tipo de copia de seguridad no se puede usar como base de una copia de seguridad incremental o diferencial. Los archivos de registro nunca se deben truncar como resultado de una copia de seguridad de copia.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Compatibilidad con archivos parciales
</dt> <dd>

Algunos escritores admiten la restauración de archivos a través de la sobrescritura de partes de los archivos que administran. Un solicitante puede estar diseñado para aprovecharse de esto y, si es así, lo indica estableciendo la información en [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

El solicitante especifica qué tipo de copia de seguridad se realiza mediante el parámetro *copia* de [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Los escritores diferentes admitirán diferentes tipos de copia de seguridad. Después de haber llamado a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) , el solicitante puede determinar qué tipos de copia de seguridad admite un escritor determinado llamando a [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). El valor devuelto es una máscara de bits que indica compatibilidad con distintos tipos de copia de seguridad. **VSS \_ La \_ diferencia diferencial de BS** indica compatibilidad con copias de seguridad diferenciales, de **VSS \_ BS \_ incrementales** para copias de seguridad incrementales, **registro de VSS \_ BS \_** para copias de seguridad de registros y **copia de VSS \_ BS \_** para copias de seguridad de copia; todos los escritores deben admitir copias de seguridad completas. Si un escritor no admite la combinación de copias de seguridad incrementales con copias de seguridad diferenciales, se agregará también la marca **\_ \_ \_ \_ diferencial incremental exclusiva de VSS BS** . Si el solicitante realiza una copia de seguridad incremental o diferencial y un escritor determinado no admite ese tipo de copia de seguridad, se debe realizar una copia de seguridad completa en ese escritor.

## <a name="backup-stamps"></a>Marcas de copia de seguridad

Las copias de seguridad incrementales y diferenciales siempre están ligadas a una copia de seguridad anterior. Hay dos formas de asociar las copias de seguridad. En el caso de los almacenes de datos simples, el solicitante puede realizar un seguimiento de la correlación entre las copias de seguridad. Sin embargo, para almacenes de datos más complejos, el escritor deberá mantener su propia marca de tiempo con la copia de seguridad; esta marca de tiempo puede realizar un seguimiento de la posición del registro, la información del punto de comprobación, etc. El solicitante puede determinar si un escritor determinado necesita almacenar su propia marca de tiempo comprobando el bit **de \_ \_ marca** de tiempo de VSS BS en el valor devuelto por [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

Los escritores que almacenan una marca de tiempo en una copia de seguridad agregarán la marca de tiempo al procesar [**ivssbackupcomponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o al procesar [**Ivssbackupcomponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). El solicitante puede obtener esta marca de tiempo mediante una llamada a [**IVssComponent:: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp). Al realizar una copia de seguridad incremental o diferencial, el solicitante debe enlazar la copia de seguridad actual a alguna copia de seguridad anterior. Esto se hace obteniendo la marca de tiempo de la copia de seguridad anterior de un componente específico y pasándola a la función [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) . Esto se debe hacer para cada componente del que se realizó una copia de seguridad en la copia de seguridad anterior.

## <a name="backing-up-files"></a>Copia de seguridad de archivos

### <a name="backing-up-files-reported-by-writer"></a>Copia de seguridad de archivos detectados por el escritor

Cada especificación de archivo que un escritor agrega a sus metadatos durante la fase GatherWriterMetadata contiene una máscara de tipo de copia de seguridad que especifica cuándo se debe realizar la copia de seguridad del archivo. El solicitante determina cuál es esta máscara mediante una llamada a [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask). Los valores de esta máscara se usan para determinar para qué tipos de copia de seguridad se debe realizar una copia de seguridad de la especificación de archivo. La máscara puede contener uno o varios de los siguientes valores de bit:

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**se \_ \_ requiere la \_ copia de seguridad completa de FSBT de VSS \_**
</dt> <dd>

Necesario para copias de seguridad completas.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**se \_ \_ requiere la \_ copia de seguridad diferencial FSBT \_ de VSS**
</dt> <dd>

Se requiere para las copias de seguridad diferenciales.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**se \_ \_ requiere la copia de seguridad incremental FSBT de VSS \_ \_**
</dt> <dd>

Se requiere para las copias de seguridad incrementales.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**se \_ \_ requiere la \_ copia de seguridad de registros FSBT \_ de VSS**
</dt> <dd>

Se requiere para las copias de seguridad de registros.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**VSS \_ FSBT \_ todas las \_ copias de seguridad \_ necesarias**
</dt> <dd>

Obligatorio para todos los tipos de copia de seguridad; Este es el valor predeterminado.

</dd> </dl>

Esta especificación invalida la especificación de selectividad del componente. Por ejemplo, considere un componente cuyos archivos están marcados con **la \_ copia \_ de \_ seguridad \_ de registros de VSS FSBT** , pero no con la **copia de \_ seguridad completa de VSS FSBT \_ \_ \_ necesaria**. Supongamos que este componente no es seleccionable para copia de seguridad (*bSelectable* era false cuando se llamó a [**IVssCreateWriterMetadata:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) ). En el caso de una copia de seguridad de registros, esto significa que siempre se debe hacer una copia de seguridad de todos los archivos de este componente. Sin embargo, en el caso de una copia de seguridad completa, no es necesario hacer una copia de seguridad de ninguno de los archivos, a pesar de que la selectividad del componente implica que se debe hacer una copia de seguridad.

### <a name="backup-by-last-modify-time"></a>Copia de seguridad por hora de última modificación

La información de especificación de archivo especificada en la fase [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) no proporciona al solicitante información sobre lo que ha cambiado desde la última copia de seguridad. Una manera de que un escritor indique que los cambios se han realizado en el solicitante es mediante el mecanismo de archivos diferenciados. Un escritor puede especificar que solo se debe realizar una copia de seguridad de determinados archivos de un componente si se han modificado desde cierto momento; el escritor puede especificar estos archivos en [**ivssbackupcomponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o en [**Ivssbackupcomponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Un solicitante puede determinar estos archivos mediante una llamada a [**IVssComponent:: GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) y [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). Si la especificación de archivo coincide con un conjunto de **IVssBackupComponents:: GatherWriterMetadata** (que actualmente es válido en función de la máscara del tipo de copia de seguridad), la información de archivo diferenciado invalida la información anterior. es decir, ahora se realiza una copia de seguridad de los archivos que coinciden con esa especificación de archivo solo si se han modificado desde la hora especificada. La hora de la última modificación se comunica mediante una estructura de [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) . Si el valor de esta estructura es cero, esto implica que la hora de la última modificación debe determinarse en función del registro del solicitante de la hora de la última copia de seguridad.

### <a name="partial-file-backup"></a>Copia de seguridad de archivos parcial

Otra forma de que un escritor indique que los cambios se han realizado en el solicitante es mediante el mecanismo de archivos parciales. Un escritor puede especificar intervalos de bytes dentro de archivos de componentes de los que es necesario hacer una copia de seguridad; el escritor puede especificar estos intervalos de archivos en [**ivssbackupcomponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o en [**Ivssbackupcomponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Un solicitante puede determinar estos archivos mediante una llamada a [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) y [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). **IVssComponent:: GetPartialFile** devolverá una ruta de acceso y un nombre de archivo que señalen al archivo, y una cadena de intervalos que indique de qué debe realizarse una copia de seguridad en el archivo. Al igual que con los archivos diferenciados, si la ruta de acceso y el nombre de archivo coinciden con una especificación de archivo establecida por el escritor en [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), la información de archivo parcial invalida la configuración anterior. La cadena de rangos puede tener dos formatos: puede especificar los intervalos directamente o puede especificar un archivo que contenga información de rangos. Si se especifican intervalos directamente, la sintaxis es una lista separada por comas con el formato offset1: length1 (, offset2: length2 (, donde cada desplazamiento y longitud es un entero sin signo de 64 bits. Si se especifica un archivo de rangos, la cadena de rangos debe establecerse en file = *filename*, donde *filename* es la ruta de acceso completa al archivo de intervalos. El propio archivo de intervalos es un archivo binario que se formatea como una lista de enteros de 64 bits sin signo. El primer entero indica el número de intervalos que se representan en el archivo. Cada par de enteros subsiguiente representa el desplazamiento y la longitud de un intervalo. El solicitante debe tener cuidado con la copia de seguridad y la restauración de este archivo de intervalos también.

### <a name="file-specification-rules"></a>Reglas de especificación de archivo

Las especificaciones de archivo agregadas a través de los mecanismos de archivo diferenciado y de archivo parcial modificarán las especificaciones de archivo establecidas en [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) o agregarán archivos completamente nuevos. Si se modifican las especificaciones de los archivos establecidas en **IVssBackupComponents:: GatherWriterMetadata** mediante el mecanismo de archivo parcial, un solicitante puede esperar que la especificación del archivo coincida exactamente con una de las especificaciones de archivo establecidas en el componente en **IVssBackupComponents:: GatherWriterMetadata**. La especificación de archivo no se superpondrá parcialmente a otra especificación de archivo y no coincidirá con ninguna especificación de archivo en ningún otro de los componentes de ese escritor. Las especificaciones de archivo agregadas mediante el mecanismo de archivo parcial pueden, sin embargo, superponerse parcialmente a otra especificación de archivo. Cuando esto es así, la especificación de archivo diferenciado o parcial invalida la especificación establecida en **IVssBackupComponents:: GatherWriterMetadata**. Las especificaciones de archivo generales pueden tener un valor de ubicación alternativa (devuelto por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)) que indica un lugar alternativo en el que obtener el archivo en el momento de la copia de seguridad. Si las especificaciones de archivo establecidas a través de los mecanismos de archivos diferenciados o parciales coinciden con una especificación de archivos existente que tiene una ubicación alternativa, los datos se deben recoger desde esta ubicación alternativa. Si las especificaciones de archivo establecidas a través de los mecanismos de archivos diferenciados o parciales no coinciden con las especificaciones existentes del componente, estos intervalos de archivos deberían agregarse ahora a la copia de seguridad. El solicitante puede esperar que solo se agreguen los archivos de los volúmenes que ya se han incluido en el conjunto de instantáneas mediante uno de estos mecanismos.

### <a name="backup-without-a-shadow-copy"></a>Copia de seguridad sin una instantánea

Es posible que no sea necesario hacer una copia de seguridad de determinados tipos de archivos en un volumen de instantáneas. Por ejemplo, esto suele ser cierto en los archivos de registro de base de datos. Dado que los archivos de registro crecen de forma monotónica, y un escritor puede especificar exactamente qué partes del archivo se van a incluir en la copia de seguridad mediante archivos parciales, a menudo es posible hacer una copia de seguridad del volumen original. Como optimización, un escritor puede marcar qué archivos requieren instantáneas para diferentes tipos de copia de seguridad mediante la máscara de tipo de copia de seguridad. El valor devuelto de [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) puede contener uno o varios de los siguientes valores de bit:

<dl> <dt>

<span id="VSS_FSBT_FULL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_full_snapshot_required"></span>**se \_ \_ requiere una \_ instantánea \_ completa de FSBT de VSS**
</dt> <dd>

Instantánea necesaria para las copias de seguridad completas.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_differential_snapshot_required"></span>**se \_ \_ requiere la \_ instantánea \_ diferencial FSBT de VSS**
</dt> <dd>

Instantánea necesaria para las copias de seguridad diferenciales.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_incremental_snapshot_required"></span>**se \_ \_ requiere la instantánea incremental FSBT de VSS \_ \_**
</dt> <dd>

Instantánea necesaria para las copias de seguridad incrementales.

</dd> <dt>

<span id="VSS_FSBT_LOG_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_log_snapshot_required"></span>**se \_ \_ requiere la \_ instantánea de registro FSBT de VSS \_**
</dt> <dd>

Instantánea necesaria para las copias de seguridad de registros.

</dd> <dt>

<span id="VSS_FSBT_ALL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_all_snapshot_required"></span>**VSS \_ FSBT \_ todas las \_ instantáneas \_ necesarias**
</dt> <dd>

Instantánea necesaria para todos los tipos de copia de seguridad; Este es el valor predeterminado.

</dd> </dl>

Si un volumen específico solo contiene componentes que no requieren una instantánea para esta copia de seguridad, el solicitante puede omitir el paso de crear una instantánea para este volumen. Todos los datos de este volumen se pueden copiar directamente en el medio de copia de seguridad desde el volumen original.

## <a name="restoring-files"></a>Restaurar archivos

### <a name="sequential-restores"></a>Restauraciones secuenciales

Una vez que el solicitante ha terminado de realizar una operación de restauración, envía el evento postrestore a todos los escritores. Por lo general, los escritores controlan este evento realizando una recuperación u otras operaciones posteriores a la restauración. La restauración de copias de seguridad incrementales, sin embargo, normalmente se produce como una secuencia de operaciones de restauración, una por copia de seguridad incremental. El solicitante debe informar al escritor de que dicha restauración está en curso con el fin de evitar que se produzca la recuperación u otras operaciones no deseadas hasta que se complete la restauración. Esto se hace llamando a [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores). Se llama a este método por componente e indica al escritor que hay más restauraciones para ese componente. Para la restauración final de la secuencia, la marca Additional-restore debe establecerse en false (su valor predeterminado), lo que indica que se trata de la última restauración de la secuencia de ese componente.

### <a name="new-targets"></a>Nuevos destinos

Si es compatible con el escritor, el solicitante puede restaurar los archivos de datos en una ubicación distinta de la ubicación de la copia de seguridad original. El solicitante puede comprobar esta compatibilidad llamando a [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). **VSS \_ BS \_ Writer \_ admite el \_ nuevo \_** bit de destino se establecerá si el escritor admite este comportamiento. El solicitante informa al escritor de la nueva ubicación mediante una llamada a [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) para cada especificación de archivo que se ha reubicado. El solicitante también puede decidir restaurar un archivo de intervalos específico en una ubicación diferente. El solicitante informa al escritor de este cambio mediante una llamada a [**IVssBackupComponents:: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

### <a name="directed-targets"></a>Destinos dirigidos

En escenarios de restauración complicados, es posible que un escritor desee asignar los intervalos de un archivo de copia de seguridad en distintos intervalos del mismo archivo o de otro diferente. Esto puede realizarse mediante el mecanismo de destino dirigido. El solicitante puede determinar después de la fase de [**Rerestauración de IVssBackupComponents::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) que este mecanismo se usa para un componente mediante una llamada a [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) y la comprobación de la devolución de **VSS \_ RT \_ dirigida**. El solicitante puede obtener todas estas restauraciones redirigidas mediante una llamada a [**IVssComponent:: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) y [**IVssComponent:: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget). **IVssComponent:: GetDirectedTarget** devolverá una ruta de acceso completa a un archivo de origen en la copia de seguridad y una ruta de acceso completa a un archivo de destino que se restaurará en. También devuelve una lista de intervalos para cada uno de estos archivos. A continuación, el solicitante es responsable de restaurar los intervalos especificados en el archivo de código fuente en los intervalos asignados en el archivo de destino. El formato de la cadena de rangos es el mismo que en [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile).

-   [Rol de escritor en copias de seguridad incrementales y diferenciales de VSS](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Rol de solicitante en copias de seguridad incrementales y diferenciales de VSS](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 
