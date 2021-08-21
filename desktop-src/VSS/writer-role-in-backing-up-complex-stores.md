---
description: Obtenga información sobre el rol de escritor en las copias de seguridad incrementales y diferenciales, que requieren una estrecha cooperación entre solicitantes y escritores.
ms.assetid: 3cf5dd1f-dc58-42bc-925f-fee7d34053c5
title: Rol de escritor en la copia de seguridad de almacenes complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbb4041ca2d05e1adf6920db617a315764f4f691768fad732c419691cf93799f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842329"
---
# <a name="writer-role-in-backing-up-complex-stores"></a>Rol de escritor en la copia de seguridad de almacenes complejos

Al igual que con todas las operaciones importantes en VSS, las copias de seguridad [*incrementales*](vssgloss-i.md) y [*diferenciales*](vssgloss-d.md) requieren una estrecha cooperación entre solicitantes y escritores.

## <a name="backup-types"></a>Tipos de copia de seguridad

La infraestructura proporciona compatibilidad especial con cinco tipos de copia de seguridad. A continuación se detalla la descripción de estos pasos:

-   Full **(VSS \_ BT \_ FULL).** Se realizará una copia de seguridad de los archivos, independientemente de la fecha de la última copia de seguridad. Se actualizará el historial de copias de seguridad de cada archivo y este tipo de copia de seguridad se puede usar como base de una copia de seguridad incremental o diferencial. Si hay archivos de registro, pueden truncarse como resultado de esta copia de seguridad.

    La restauración de una copia de seguridad completa solo requiere una sola imagen de copia de seguridad.

-   Diferencial **(VSS \_ BT \_ DIFFERENTIAL).** La API de VSS se usa para asegurarse de que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa se copiarán en un medio de almacenamiento. se omite toda la información de copia de seguridad intermedia. Esto puede incluir archivos completos o intervalos específicos dentro de los archivos. Una copia de seguridad diferencial está asociada a una copia de seguridad completa y, por lo general, no se puede restaurar hasta que se haya restaurado la copia de seguridad completa. Si hay archivos de registro, normalmente no se truncarán como resultado de esta copia de seguridad.

    La restauración de una copia de seguridad diferencial requiere la imagen de copia de seguridad original y la imagen de copia de seguridad diferencial más reciente realizada desde la última copia de seguridad completa.

-   Incremental (**VSS \_ BT \_ INCREMENTAL**). La API de VSS se usa para asegurarse de que solo los archivos que se han cambiado o agregado desde la última copia de seguridad completa o incremental se copiarán en un medio de almacenamiento. Esto puede incluir archivos completos o intervalos específicos dentro de los archivos. Algunos escritores no permiten que las copias de seguridad incrementales se mezclen con copias de seguridad diferenciales. Si hay archivos de registro, pueden truncarse como resultado de esta copia de seguridad.

    La restauración de una copia de seguridad incremental requiere la imagen de copia de seguridad original y todas las imágenes de copia de seguridad incremental realizadas desde la copia de seguridad inicial.

-   Copia de seguridad de registros (**VSS \_ BT \_ LOG**). Solo se realizará una copia de seguridad de los archivos de registro de un escritor (archivos agregados a un componente con el método [**IVssCreateWriterMetadata::AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) y recuperados mediante una llamada a [**IVssWMComponent::GetDatabaseLogFile).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) Este tipo de copia de seguridad es específico de VSS. Las copias de seguridad de registros tienden a realizarse con bastante frecuencia. Normalmente, el archivo de registro se truncará como resultado de esta copia de seguridad.
-   Copia de seguridad **(COPIA DE VSS \_ BT). \_** Al igual que el tipo de copia de seguridad COMPLETA de VSS BT, se realizará una copia de seguridad de los \_ \_ archivos, independientemente de su última fecha de copia de seguridad. Sin embargo, el historial de copias de seguridad de cada archivo no se actualizará y este tipo de copia de seguridad no se puede usar como base de una copia de seguridad incremental o diferencial. Los archivos de registro nunca se deben truncar como resultado de una copia de seguridad.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Compatibilidad con archivos parciales
</dt> <dd>

Algunos escritores admiten la restauración de archivos mediante la sobrescritura de partes de los archivos que administran. Un solicitante se puede diseñar para aprovechar esto y, si es así, lo indica estableciendo la información en [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

Los escritores indican qué tipo de copias de seguridad se admiten mediante una llamada a [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) al procesar el [*evento Identify.*](vssgloss-i.md) El *parámetro dsSchemaMask* del método **IVssCreateWriterMetadata::SetBackupSchema** es una máscara de bits que indica qué tipos de copia de seguridad se admiten. Todos los escritores deben admitir copias de seguridad completas.

<dl> <dt>

<span id="VSS_BS_DIFFERENTIAL"></span><span id="vss_bs_differential"></span>**VSS \_ BS \_ DIFFERENTIAL**
</dt> <dd>

Indica la compatibilidad con copias de seguridad diferenciales.

</dd> <dt>

<span id="VSS_BS_INCREMENTAL"></span><span id="vss_bs_incremental"></span>**VSS \_ BS \_ INCREMENTAL**
</dt> <dd>

Indica la compatibilidad con las copias de seguridad incrementales.

</dd> <dt>

<span id="VSS_BS_LOG"></span><span id="vss_bs_log"></span>**REGISTRO DE VSS \_ BS \_**
</dt> <dd>

Indica la compatibilidad con las copias de seguridad de registros.

</dd> <dt>

<span id="VSS_BS_COPY"></span><span id="vss_bs_copy"></span>**COPIA DE VSS \_ BS \_**
</dt> <dd>

Indica la compatibilidad con copias de seguridad de copia.

</dd> <dt>

<span id="VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL"></span><span id="vss_bs_exclusive_incremental_differential"></span>**DIFERENCIAL \_ INCREMENTAL EXCLUSIVO DE VSS BS \_ \_ \_**
</dt> <dd>

Indica que un escritor no admite la combinación de copias de seguridad incrementales con copias de seguridad diferenciales.

</dd> </dl>

El escritor puede determinar qué tipo de copia de seguridad se está realizando llamando a [**CVssWriter::GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype). El punto más antiguo en el que se puede realizar es mientras se procesa el evento PrepareForBackup. **CVssWriter::GetBackupType** devolverá un miembro de la [**enumeración VSS \_ BACKUP \_ TYPE.**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) Si el escritor no admite el tipo de copia de seguridad, el escritor debe tratar la copia de seguridad como una copia de seguridad completa.

## <a name="backup-stamps"></a>Marcas de copia de seguridad

Las copias de seguridad incrementales y diferenciales siempre están asociadas a una copia de seguridad anterior. Hay dos maneras de vincular copias de seguridad. En el caso de los almacenes de datos simples, el solicitante puede realizar un seguimiento de la correlación entre las copias de seguridad. Sin embargo, para almacenes de datos más complejos, el escritor deberá mantener su propia marca de tiempo con la copia de seguridad. esta marca de tiempo puede realizar un seguimiento de la posición del registro, la información del punto de control, y así sucesivamente. Un sistema de escritura indica que necesita sus propias marcas de tiempo estableciendo el bit **\_ \_ TIMESTAMPED de VSS BS** cuando llama a [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema).

Un escritor puede almacenar una marca de tiempo con cada componente del que se va a realizar una copia de seguridad. El escritor almacena la marca de tiempo llamando a [**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)y pasando una representación de cadena de la marca para el *parámetro wszBackupStamp.* Por lo general, un escritor llamará a este método mientras se procesa el [*evento PostSnapshot.*](vssgloss-p.md) Sin embargo, para las copias de seguridad que no implican una instantánea, no se enviará el evento PostSnapshot. En este caso, **se debe llamar a IVssComponent::SetBackupStamp** al procesar el evento [*PrepareForBackup.*](vssgloss-p.md)

Cuando se realiza una copia de seguridad incremental o diferencial, el solicitante indicará al escritor la marca de copia de seguridad de la copia de seguridad anterior que sirve como base para esta copia de seguridad. El escritor puede acceder a esta marca de copia de seguridad anterior mientras se procesa el evento PrepareForBackup o PostSnapshot mediante una llamada a [**IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp). El escritor puede usar la marca devuelta para determinar de qué se debe hacer una copia de seguridad.

## <a name="backup-strategies"></a>Estrategias de copia de seguridad

### <a name="file-backup-files-strategies"></a>Estrategias de archivos de copia de seguridad de archivos

A menudo, solo es necesario hacer una copia de seguridad de determinados archivos notificados en los metadatos del escritor al realizar determinados tipos de copia de seguridad. Es posible que algunos archivos solo sean necesarios al realizar una copia de seguridad completa. Es posible que solo se requieran otros archivos al realizar una copia de seguridad incremental o diferencial. VSS proporciona un método para que los escritores indiquen esta información al solicitante. Al agregar archivos a componentes mediante [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), el parámetro *dwBackupTypeMask* indica para qué tipos de copia de seguridad se debe realizar una copia de seguridad de estos archivos. La máscara puede contener uno o varios de los valores siguientes:

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**SE REQUIERE COPIA \_ DE SEGURIDAD COMPLETA DE VSS FSBT \_ \_ \_**
</dt> <dd>

Necesario para copias de seguridad completas.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**SE REQUIERE COPIA \_ DE SEGURIDAD DIFERENCIAL DE VSS FSBT \_ \_ \_**
</dt> <dd>

Necesario para las copias de seguridad diferenciales.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**SE REQUIERE COPIA \_ DE SEGURIDAD INCREMENTAL DE VSS FSBT \_ \_ \_**
</dt> <dd>

Necesario para las copias de seguridad incrementales.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**SE REQUIERE LA \_ COPIA DE SEGURIDAD DE REGISTROS DE VSS FSBT \_ \_ \_**
</dt> <dd>

Necesario para las copias de seguridad de registros.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**VSS \_ FSBT \_ ALL \_ BACKUP \_ REQUIRED**
</dt> <dd>

Obligatorio para todos los tipos de copia de seguridad; este es el valor predeterminado.

</dd> </dl>

Esta especificación invalida la especificación de selectividad del componente. Por ejemplo, considere un componente cuyos archivos están marcados con **VSS \_ FSBT \_ LOG BACKUP \_ \_ REQUIRED** pero no con FULL BACKUP REQUIRED de **\_ VSS FSBT \_ \_ \_**. Supongamos que este componente no se puede seleccionar para la copia de seguridad (*bSelectable* era false cuando se llamó a [**IVssCreateWriterMetadata::AddComponent).**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) En el caso de una copia de seguridad de registros, esto significa que siempre se debe hacer una copia de seguridad de todos los archivos de este componente. Sin embargo, en el caso de una copia de seguridad completa, no es necesario hacer una copia de seguridad de ninguno de los archivos, a pesar de que la selectividad del componente implica que se debe hacer una copia de seguridad.

### <a name="backup-by-last-modify-time"></a>Copia de seguridad por hora de última modificación

Una manera de que un escritor indique qué archivos han cambiado es mediante el mecanismo de archivo diferenciado. Un sistema de escritura puede especificar que solo se debe hacer una copia de seguridad de determinados archivos de un componente si se han modificado desde un momento determinado. El escritor llama a [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) con una especificación de archivo y una hora de última modificación. **IVssComponent::AddDifferencedFilesByLastModifyTime** normalmente se llama al procesar el evento PostSnapshot, aunque se puede llamar al procesar el evento PrepareForBackup. A continuación, el solicitante debe hacer una copia de seguridad de todos los archivos que coincidan con la especificación de archivo que han cambiado desde la hora especificada. Si el escritor usa el mecanismo de marca de copia de seguridad, esta hora de última modificación se determinará en función de la marca de copia de seguridad anterior en el documento de copia de seguridad. El escritor también puede pasar cero durante la hora de la última modificación, lo que indica que el solicitante es responsable de determinar la hora de la última copia de seguridad y los archivos cambiados desde esa hora.

### <a name="partial-file-backup"></a>Copia de seguridad parcial de archivos

Otra manera de que un escritor indique cambios en el solicitante es mediante el mecanismo de archivo parcial. Un escritor puede especificar intervalos de bytes dentro de los archivos de componentes de los que es necesario realizar una copia de seguridad; el escritor puede especificar estos intervalos de archivos al procesar el evento PostSnapshot o PrepareForBackup. El escritor llama [**a IVssComponent::AddPartialFile para**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) agregar especificaciones de archivo parciales a la copia de seguridad. Una especificación de archivo parcial consta de una ruta de acceso y un nombre de archivo junto con información sobre los intervalos del archivo de los que se debe realizar una copia de seguridad.

### <a name="file-specification-rules"></a>Reglas de especificación de archivos

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) o [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) se pueden usar para modificar las especificaciones de archivo especificadas durante el evento Identify o para agregar archivos completamente nuevos a la especificación. Si el escritor está modificando el conjunto de información durante el evento Identify mediante **IVssComponent::AddDifferencedFilesByLastModifyTime**, la especificación de archivo debe coincidir exactamente con una de las especificaciones de archivo del componente actual. La especificación de archivo no debe superponerse parcialmente a los archivos del componente actual y no debe coincidir con los archivos de ningún otro componente. Sin embargo, los archivos especificados mediante **IVssComponent::AddPartialFile** pueden superponerse parcialmente a otra especificación de archivo. La información establecida por **IVssComponent::AddDifferencedFilesByLastModifyTime** o **IVssComponent::AddPartialFile** invalida el conjunto de información anterior mediante la interfaz [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) en respuesta al evento Identify.

Las especificaciones generales de archivo pueden tener un valor de ubicación alternativa (establecido por el parámetro *wszAlternateLocation* de [**IVssCreateWriterMetadata::AddFilesToFileGroup)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)que indica una ubicación alternativa desde la que obtener el archivo en tiempo de copia de seguridad. Si la especificación de archivo establecida a través de los mecanismos differenced-file o partial-file coincide con una especificación de archivo existente que tiene una ubicación alternativa, la aplicación de copia de seguridad obtendrá los datos de esta ubicación alternativa.

Si la especificación de archivo establecida en [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) o [**en IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) no coincide con los archivos y del componente del que se realiza la copia de seguridad, todos los archivos correspondientes ahora se agregan a la copia de seguridad. Se debe tener cuidado de que el escritor solo agrega los archivos que existen en un volumen que ya se está copiando a la sombra mientras lo hace. De lo contrario, es posible que el solicitante no pueda hacer una copia de seguridad de estos archivos. Si se llama a estas funciones al procesar el evento PostSnapshot, esto se puede determinar mediante el [**método CVssWriter::IsPathAffected.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispathaffected) Si se llama al controlar el evento PrepareForBackup, el escritor debe realizar esta determinación mediante otro método.

### <a name="backup-without-a-shadow-copy"></a>Copia de seguridad sin instantáneas

Es posible que no sea necesario realizar una copia de seguridad de determinados tipos de archivos fuera de un volumen de instantáneas. Por ejemplo, esto suele ser cierto para los archivos de registro de base de datos. Dado que los archivos de registro crecen de forma monónica y un escritor puede especificar exactamente qué partes del archivo se van a realizar con archivos parciales, a menudo será posible realizar una copia de seguridad del registro del volumen original. Como optimización, un escritor puede marcar qué archivos requieren instantáneas para diferentes tipos de copia de seguridad mediante las marcas establecidas en el parámetro *dwBackupTypeMask* de [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata::AddDatabaseLogFiles o**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) [**IVssCreateWriterMetadata::AddFilesToFileGroup.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) Entre las marcas admitidas se incluyen las siguientes:

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

## <a name="backup-cleanup"></a>Limpieza de copia de seguridad

Si el escritor necesita realizar el truncamiento del registro u otra limpieza posterior a la copia de seguridad, el lugar adecuado para hacerlo es al procesar el [*evento BackupComplete.*](vssgloss-b.md) El [*evento BackupShutdown*](vssgloss-b.md) se enviará algún tiempo después de BackupComplete, por lo que también se puede realizar alguna limpieza en el controlador de eventos BackupShutdown.

El evento BackupShutdown siempre se envía después de finalizar una copia de seguridad. Si el solicitante finaliza de forma anómala al realizar una copia de seguridad, BackupShutdown se enviará inmediatamente, sin enviar primero BackupComplete. Si el escritor necesita limpiar cualquier estado, se puede hacer aquí. sin embargo, el truncamiento del registro no debe producirse en este evento porque la copia de seguridad no se ha completado necesariamente.

## <a name="restore-strategies"></a>Estrategias de restauración

Las tareas básicas de los escritores durante la restauración son comprobar que la restauración puede producirse al controlar el evento PreRestore y que la restauración se ha producido al controlar el evento PostRestore. Los almacenes más complejos también realizarán un proceso de recuperación en el controlador PostRestore. Si la restauración forma parte de una restauración incremental o diferencial, el escritor generalmente querrá retrasar este proceso de recuperación hasta que se hayan completado todas las restauraciones incrementales o diferenciales. [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) indicará si se trata de la restauración final de este componente o si hay más restauraciones. Si **IVssComponent::GetAdditionalRestores** devuelve **true**, el escritor no debe realizar su procedimiento de recuperación en ese componente.

## <a name="new-targets"></a>Nuevos destinos

Si es compatible con el sistema de escritura, el solicitante puede restaurar los archivos de datos en una ubicación que no sea la ubicación original en tiempo de copia de seguridad. Un escritor indica la compatibilidad con este modo de restauración estableciendo el bit **VSS \_ BS \_ WRITER SUPPORTS NEW \_ \_ \_ TARGET** en el parámetro *dsSchemaMask* al llamar a [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema). Un sistema de escritura obtiene las nuevas ubicaciones de los archivos de componente en tiempo de restauración mediante una llamada a [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget).

## <a name="directed-targets"></a>Destinos dirigidos

En escenarios de restauración complicados, es posible que un escritor quiera asignar intervalos de un archivo de copia de seguridad a intervalos diferentes del mismo archivo o de otro. Esto se puede hacer mediante el mecanismo de destino dirigido. Para ello, un escritor debe indicar primero que esto sucede llamando a [**IVssComponent::SetRestoreTarget,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)pasando **VSS \_ RT \_ DIRECTED** para el parámetro *de* destino. A continuación, para cada asignación, el escritor llama [**a IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget). Este método toma una ruta de acceso completa a un archivo de código fuente en la copia de seguridad y una ruta de acceso completa a un archivo de destino en el que se restaurará. También toma una lista de intervalos para cada uno de estos archivos. El escritor llama a estas funciones mientras se administra el evento PreRestore y, a continuación, el solicitante es responsable de restaurar los intervalos especificados en el archivo de origen a los intervalos asignados en el archivo de destino. El formato de la cadena de intervalos es el mismo que en [ **IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)

## <a name="private-writer-metadata"></a>Metadatos de escritor privado

A menudo resulta útil para un escritor mantener metadatos privados con una copia de seguridad para realizar correctamente una restauración incremental o diferencial. Un escritor puede llamar a [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) mientras se administra PrepareForBackup o PostSnapshot para almacenar los metadatos. El escritor puede tener acceso a estos metadatos durante PreRestore o PostRestore llamando a [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata). Los metadatos también se pueden almacenar con especificación de archivo parcial mediante el parámetro *wszMetadata* de [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile); Se tiene acceso a estos metadatos a través del *parámetro pbstrMetadata* [**de IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). El escritor también puede pasar metadatos a sí mismo entre [**CVssWriter::OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore) y [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore). En **CVssWriter::OnPreRestore**, los metadatos se establecen mediante una llamada [**a IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata). En **CVssWriter::OnPostRestore**, los metadatos se recuperan llamando a [**IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata).

-   [Rol escritor en copias de seguridad incrementales y diferenciales de VSS](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Rol solicitante en copias de seguridad incrementales y diferenciales de VSS](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 



