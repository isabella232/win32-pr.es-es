---
description: 'Para admitir una operación de copia de seguridad incremental o diferencial, un solicitante debe hacer lo siguiente:'
ms.assetid: a77700e3-8217-460e-bec9-1041d03eec41
title: Rol solicitante en copias de seguridad incrementales y diferenciales de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637d4bf97b97d484080c85a2345599a05e4bbd89f88a0c1786b5bda911a83331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122010"
---
# <a name="requester-role-in-vss-incremental-and-differential-backups"></a>Rol solicitante en copias de seguridad incrementales y diferenciales de VSS

Para admitir una [*operación de copia*](vssgloss-i.md) de seguridad incremental o [*diferencial,*](vssgloss-d.md) un solicitante debe hacer lo siguiente:

1.  Determine qué grado de compatibilidad con el escritor está disponible (mediante [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para obtener acceso a la información de los documentos de metadatos del escritor), en concreto, determine qué esquema de copia de seguridad se admite (ESQUEMA DE COPIA DE SEGURIDAD de [**VSS). \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
2.  Establezca un estado de copia de seguridad adecuado.
3.  Obtenga especificaciones de nivel de conjunto de archivos y archivos para una copia de seguridad incremental o diferencial.
4.  Realice la copia de seguridad.

## <a name="requester-determination-of-incremental-and-differential-support-and-configuration"></a>Determinación del solicitante de compatibilidad y configuración incrementales y diferenciales

Un solicitante debe obtener información sobre la compatibilidad con el escritor antes de seleccionar componentes para su inclusión en una copia de seguridad incremental o diferencial o establecer su propio estado.

<dl> <dt>

<span id="Determining_Writer_Support"></span><span id="determining_writer_support"></span><span id="DETERMINING_WRITER_SUPPORT"></span>Determinar la compatibilidad con el escritor
</dt> <dd>

Un solicitante determina si un escritor determinado admite copias de seguridad incrementales o diferenciales de VSS mediante la recuperación de la máscara de esquema de copia de seguridad del escritor mediante el método [**IVssExminoWriterMetadata::GetBackupSchema.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)

La máscara de esquema de copia de seguridad de un escritor que admite técnicas incrementales o diferenciales de VSS contendrá INCREMENTAL de **\_ VSS BS \_** o **\_ VSS BS \_ DIFFERENTIAL,** o ambos. Los escritores también pueden indicar restricciones en su participación con la marca **\_ DIFERENCIAL INCREMENTAL EXCLUSIVO \_ \_ \_ de VSS BS.** (Vea [**ESQUEMA DE COPIA DE SEGURIDAD \_ \_ DE VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) para obtener más información sobre los esquemas de copia de seguridad).

</dd> <dt>

<span id="Setting_Requester_Backup_State"></span><span id="setting_requester_backup_state"></span><span id="SETTING_REQUESTER_BACKUP_STATE"></span>Establecer el estado de copia de seguridad del solicitante
</dt> <dd>

Un solicitante indica que una copia de seguridad es una copia de seguridad incremental o diferencial estableciendo un tipo de copia de seguridad en **VSS \_ BT \_ INCREMENTAL** o **VSS \_ BT \_ DIFFERENTIAL** mediante el método [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) antes de generar un [**evento PrepareForBackup.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)

El [**método IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) también se usa para indicar si el solicitante proporciona compatibilidad parcial con archivos [*,*](vssgloss-p.md)que se usa con frecuencia para implementar ciertas operaciones incrementales de copia de seguridad y restauración.

</dd> </dl>

## <a name="getting-writer-specifications-for-incremental-and-differential-backups"></a>Obtención de especificaciones de escritor para copias de seguridad incrementales y diferenciales

La información de especificación de copia de seguridad de archivos de nivel de conjunto de archivos [**(VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE)**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)contenida en el documento de metadatos del escritor de cada escritor está disponible para su examen después de la devolución correcta de [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Sin embargo, un escritor puede agregar [*archivos diferenciados*](vssgloss-d.md) o solicitar compatibilidad con [*archivos parciales*](vssgloss-p.md) hasta que se controle correctamente [*el evento PostSnapshot.*](vssgloss-p.md)

La especificación de compatibilidad con archivos y archivos parciales diferenciados puede invalidar el tipo de copia de seguridad de especificación de archivo, por lo que es posible que los solicitantes quieran aplazar un análisis completo de todas las especificaciones de escritor sobre las copias de seguridad incrementales y diferenciales hasta después de la devolución correcta de [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).

<dl> <dt>

<span id="Getting_File_Backup_Specification_Information"></span><span id="getting_file_backup_specification_information"></span><span id="GETTING_FILE_BACKUP_SPECIFICATION_INFORMATION"></span>Obtener información de especificación de copia de seguridad de archivos
</dt> <dd>

La información de especificación de copia de seguridad de archivos de nivel de conjunto de archivos [**(VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) se encuentra en el documento de metadatos del escritor de cada escritor y se puede examinar inmediatamente después de la devolución correcta de [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Los solicitantes deben obtener máscaras de especificación de copia de seguridad de archivos [**(VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) para cada [](vssgloss-e.md) conjunto de archivos de cada uno de los componentes de un escritor que se incluirán en la copia de seguridad incremental o diferencial, independientemente de si el componente se incluyó explícita o [*implícitamente.*](vssgloss-i.md)

Un solicitante puede determinar qué documento de metadatos del escritor de escritores se debe consultar mediante [**IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). La instancia de la [**interfaz IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) devuelta por **IVssBackupComponents::GetWriterComponents** proporciona información de escritura a través del método [**IVssWriterComponentsExt::GetWriterInfo.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo)

El solicitante obtiene información de componentes a través de instancias de la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) correspondiente a un componente incluido administrado por un escritor determinado mediante [**IVssExgvWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

La información sobre los conjuntos de archivos administrados por el componente correspondiente a la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) se obtiene mediante llamadas a [**IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent::GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)o [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) (según corresponda).

Estas llamadas pueden devolver instancias de la [**interfaz IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) para cada uno de los conjuntos de archivos de un componente.

El tipo de copia de seguridad de especificación de archivos de un conjunto de archivos se obtiene mediante una llamada a [**IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask).

</dd> <dt>

<span id="Getting_Partial_File_and_Differenced_File_Information"></span><span id="getting_partial_file_and_differenced_file_information"></span><span id="GETTING_PARTIAL_FILE_AND_DIFFERENCED_FILE_INFORMATION"></span>Obtener información de archivo parcial y de archivo diferenciado
</dt> <dd>

Un solicitante obtiene información de archivo parcial y de archivo diferenciada a través de la [**interfaz IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Un solicitante puede iterar por todos los escritores incluidos en una copia de seguridad mediante [**IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) [**e IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

La instancia de una interfaz [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) devuelta por [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) proporciona acceso a todas las instancias [](vssgloss-e.md) de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondientes a los componentes incluidos explícitamente de un escritor determinado a través de los [**métodos IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) e [**IVssWriterComponentsExt::GetComponentCount.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount)

Un solicitante tendrá que pasar por todas las instancias de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para todos los escritores cuyo esquema admita la copia de seguridad incremental o diferencial( es decir, los escritores cuya máscara de esquema de copia de seguridad, tal y como devuelve [**IVssExminoWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), incluye INCREMENTAL de **\_ VSS BS \_ cuando** el tipo de copia de seguridad es INCREMENTAL de **VSS \_ BT \_** o DIFERENCIAL DE **VSS \_ BS \_** cuando el tipo de copia de seguridad es **\_ VSS BS \_ DIFFERENTIAL.**

La información de archivo parcial se obtiene mediante una llamada a [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) (vea Trabajar con archivos [parciales).](working-with-partial-files.md)

Para los escritores que admiten operaciones de copia de seguridad en función de los últimos datos de modificación de un archivo (escritores cuya máscara de esquema de copia de seguridad, como devuelve [**IVssExbruWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), incluye **\_ VSS BS \_ LAST \_ MODIFY),** la información de archivo diferenciada se obtiene llamando a [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) e [**IVssComponent::GetDifferencedFile.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)

Tenga en cuenta que los archivos diferenciados pueden ser archivos nuevos, es decir, archivos que no son miembros de ningún conjunto de archivos actualmente en el documento de metadatos del escritor de un escritor determinado.

Los solicitantes no deben encontrar archivos incluidos para operaciones de archivos parciales y como archivos con diferencias. Si un solicitante encuentra esta circunstancia, debe devolver y registrar un error de escritor.

Un solicitante todavía puede optar por continuar con la copia de seguridad de los archivos del escritor problemático, pero en ese caso debe hacerlo según la especificación que se encuentra en la información de archivo diferenciada.

</dd> </dl>

## <a name="implementing-incremental-or-differential-backups"></a>Implementar copias de seguridad incrementales o diferenciales

Antes de implementar una copia de seguridad, los solicitantes [](vssgloss-d.md) deben tener información sobre qué escritores admiten una copia de seguridad [*incremental*](vssgloss-i.md) o diferencial, todas las operaciones de archivo parciales solicitadas, todos los archivos diferenciados y el tipo de copia de seguridad de especificación de archivo de todos los demás archivos.

<dl> <dt>

<span id="Nonsupporting_Writers"></span><span id="nonsupporting_writers"></span><span id="NONSUPPORTING_WRITERS"></span>Escritores no compatibles
</dt> <dd>

Los escritores cuyo esquema no admite la copia de seguridad incremental o diferencial (escritores cuya máscara de esquema de copia de seguridad, como devuelve [**IVssExgvWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), incluye INCREMENTAL de **VSS \_ BS \_** cuando el tipo de copia de seguridad es INCREMENTAL de **VSS \_ BT \_** o no incluye **VSS \_ BS \_ DIFFERENTIAL** cuando el tipo de copia de seguridad es **VSS \_ BS \_ DIFFERENTIAL)** no pueden proporcionar compatibilidad directa con una operación de copia de seguridad incremental o diferencial.

Esto no significa necesariamente que los datos de los escritores no intervendrán en una operación de copia de seguridad incremental o diferencial. Sin embargo, la elección de qué hacer es a discreción del solicitante. El solicitante puede realizar cualquiera de las siguientes acciones:

-   Hacer una copia de seguridad de ningún archivo que pertenezca a los escritores no compatibles (indique claramente esto al usuario).
-   Copia de seguridad de todos los archivos de escritores no compatibles
-   Realice una copia de seguridad incremental con datos del sistema de archivos y los propios registros de historial del solicitante.

La última alternativa debe usarse con mucho cuidado y solo si el solicitante entiende si los escritores implicados pueden admitir la copia de seguridad incremental o diferencial y la restauración de datos independientemente del mecanismo de VSS.

</dd> <dt>

<span id="Supporting_Writers"></span><span id="supporting_writers"></span><span id="SUPPORTING_WRITERS"></span>Escritores de apoyo
</dt> <dd>

Un solicitante debe procesar (en orden) todos los archivos diferenciados [](vssgloss-p.md) de un [*escritor,*](vssgloss-d.md)controlar las solicitudes de archivo parciales y, a continuación, realizar copias de seguridad de los archivos restantes según su tipo de copia de seguridad de especificación de archivo [**(VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

1.  **Copia de seguridad de archivos diferenciados:**

    En el caso de los escritores que admiten operaciones de copia de seguridad en función de los datos de última modificación (escritores cuya máscara de esquema de copia de seguridad, como devuelve [**IVssExbruWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), incluye **\_ VSS BS \_ LAST \_ MODIFY),** un solicitante usa la ruta de acceso, la especificación de archivo y la información de la marca de recursividad devuelta por [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) para generar una lista de archivos como candidatos para la copia de seguridad incremental o la restauración.

    [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) también puede devolver una hora de la última modificación (expresada como una [**estructura FILETIME).**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

    Si la hora de última modificación proporcionada por el escritor es distinta de cero, el solicitante la usa como base (en lugar de la información [](vssgloss-d.md) del sistema de archivos o los propios datos almacenados del solicitante) para determinar si el archivo debe incluirse en la copia de seguridad [*incremental*](vssgloss-i.md) o diferencial.

    Por ejemplo, si la hora de la última modificación de un archivo devuelta por el escritor era:

    -   Después de la última copia de seguridad completa, el archivo debe incluirse en copias de seguridad incrementales y diferenciales.
    -   Después de la última copia de seguridad completa, pero antes de la última copia de seguridad incremental, el archivo debe incluirse en las operaciones de copia de seguridad incremental, pero no en las copias de seguridad diferenciales.

    Si la hora de última modificación proporcionada por el escritor es cero, el solicitante debe usar la información del sistema de archivos y sus propios datos almacenados para determinar la hora de modificación del archivo diferenciado.

2.  **Usar operaciones de archivos parciales:**

    Si un escritor ha solicitado que se realice una copia de seguridad de un archivo mediante una operación de archivo parcial, el solicitante usa la información de desplazamiento de archivo para guardar los segmentos de archivo indicados en los medios de copia de seguridad. (Consulte [Trabajar con archivos parciales para](working-with-partial-files.md) obtener más información sobre las operaciones de archivos parciales).

    Como se indicó anteriormente, un escritor no debe designar un archivo como un archivo con diferencias y como participante en una operación de archivo parcial. Si un solicitante encuentra esta circunstancia, debe devolver y registrar un error de escritor.

    Un solicitante todavía puede optar por continuar con la copia de seguridad de los archivos del escritor problemático, pero en ese caso debe hacerlo según la especificación que se encuentra en la información de archivo diferenciada.

3.  **Trabajar con el tipo de copia de seguridad de especificación de archivo:**

    Después de haber procesado todos los archivos diferenciados y las operaciones de archivos parciales, el solicitante ahora procesa todos los archivos restantes de su conjunto de copia de seguridad en función de su tipo de copia de seguridad de especificación de archivo [**(VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

    Hay tres valores "se requiere copia de seguridad" de la enumeración [**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que afectan a las copias de seguridad diferenciales e incrementales:

    -   VSS \_ FSBT \_ ALL \_ BACKUP \_ REQUIRED
    -   SE REQUIERE COPIA \_ DE SEGURIDAD INCREMENTAL DE VSS FSBT \_ \_ \_
    -   SE REQUIERE COPIA \_ DE SEGURIDAD DIFERENCIAL DE VSS FSBT \_ \_ \_

    Hay tres valores de "instantánea necesaria":

    -   VSS \_ FSBT \_ ALL \_ SNAPSHOT \_ REQUIRED
    -   INSTANTÁNEA \_ INCREMENTAL DE VSS FSBT \_ \_ \_ REQUERIDA
    -   INSTANTÁNEA DIFERENCIAL \_ DE VSS FSBT \_ \_ \_ REQUERIDA

    Los conjuntos de archivos etiquetados con un tipo de copia de seguridad de especificación de archivo de "instantánea necesaria" indican que un solicitante debe copiar datos de una instantánea al realizar operaciones de copia de seguridad INCREMENTAL, DIFFERENTIAL o ALL (que incluye operaciones incrementales y diferenciales).

    La marca "copia de seguridad necesaria", aplicada a las operaciones de copia de seguridad INCREMENTAL, DIFFERENTIAL o ALL, indica que el escritor espera que una copia de la versión actual del conjunto de archivos esté disponible después de la restauración de cualquier operación de copia de seguridad. Normalmente, esto significa que si un conjunto de archivos se etiqueta con "copia de seguridad necesaria", un solicitante copiará todos sus miembros en medios de copia de seguridad durante una copia de seguridad incremental o diferencial, independientemente de cuándo se haya producido su última copia de seguridad o modificación.

    De forma predeterminada, los conjuntos de archivos se agregan a los componentes con un tipo de copia de seguridad de especificación de archivo de VSS \_ FSBT \_ ALL BACKUP REQUIRED \_ \_ \| VSS \_ FSBT \_ ALL SNAPSHOT \_ \_ REQUIRED. Por lo tanto, a menos que un escritor establezca explícitamente el tipo de copia de seguridad de especificación de archivo, los solicitantes tendrán que copiar esos archivos no manipulados por operaciones de archivos parciales o los archivos designados diferenciados en la mayoría de los conjuntos de archivos normalmente se copiarán en su totalidad en medios de copia de seguridad.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Marcas de copia de seguridad
</dt> <dd>

Los escritores que admiten marcas de copia de seguridad (VSS BS TIMESTAMP) pueden optar por generar información de marca de copia de seguridad que se usará para admitir futuras operaciones incrementales y diferenciales de copia de seguridad \_ \_ y restauración.

El formato y la información contenidos en las cadenas que contienen información de marca de copia de seguridad son privados para el escritor que las genera. el solicitante no sabe cómo procesar esta información.

Los escritores de compatibilidad almacenan la marca de copia de seguridad en el documento componentes de copia de seguridad como una cadena mediante el [**método IVssComponent::SetBackupStamp.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)

El rol del solicitante en el control de la información de marca de copia de seguridad es (si existe) para que esté disponible para el escritor mediante una llamada a [**IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) en una futura operación de copia de seguridad o restauración.

</dd> </dl>

 

 
