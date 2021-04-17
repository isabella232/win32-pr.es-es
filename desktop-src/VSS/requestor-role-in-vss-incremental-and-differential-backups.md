---
description: 'Para admitir una operación de copia de seguridad incremental o diferencial, un solicitante debe hacer lo siguiente:'
ms.assetid: a77700e3-8217-460e-bec9-1041d03eec41
title: Rol de solicitante en copias de seguridad incrementales y diferenciales de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 718a5a0b22d9cc1cfa31404b3a0ac71a3a07731f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696978"
---
# <a name="requester-role-in-vss-incremental-and-differential-backups"></a>Rol de solicitante en copias de seguridad incrementales y diferenciales de VSS

Para admitir una operación de copia de seguridad [*incremental*](vssgloss-i.md) o [*diferencial*](vssgloss-d.md) , un solicitante debe hacer lo siguiente:

1.  Determine qué grado de compatibilidad con el escritor está disponible (mediante [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para obtener acceso a la información de los documentos de metadatos del escritor), en concreto, para determinar qué esquema de copia de seguridad se admite ([**\_ \_ esquema de copia de seguridad de VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)).
2.  Establezca un estado de copia de seguridad adecuado.
3.  Obtener especificaciones de nivel de archivo y de conjunto de archivos para una copia de seguridad incremental o diferencial.
4.  Realice la copia de seguridad.

## <a name="requester-determination-of-incremental-and-differential-support-and-configuration"></a>Determinación del solicitante de compatibilidad y configuración incremental y diferencial

Un solicitante debe obtener información sobre la compatibilidad del escritor antes de seleccionar los componentes para su inclusión en una copia de seguridad incremental o diferencial, o bien establecer su propio estado.

<dl> <dt>

<span id="Determining_Writer_Support"></span><span id="determining_writer_support"></span><span id="DETERMINING_WRITER_SUPPORT"></span>Determinar la compatibilidad del escritor
</dt> <dd>

Un solicitante determina si un escritor determinado admite copias de seguridad incrementales o diferenciales de VSS mediante la recuperación de la máscara del esquema de copia de seguridad del escritor mediante el método [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema) .

La máscara del esquema de copia de seguridad de un escritor que admite técnicas incrementales o diferenciales de VSS contendrá la diferencia de VSS **\_ BS \_ incremental** o de **VSS \_ BS \_**, o ambos. Los escritores también pueden indicar restricciones en su participación con la marca **\_ \_ \_ \_ diferencial incremental exclusiva de VSS BS** . (Consulte [**\_ \_ esquema de copia de seguridad de VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) para obtener más información sobre los esquemas de copia de seguridad).

</dd> <dt>

<span id="Setting_Requester_Backup_State"></span><span id="setting_requester_backup_state"></span><span id="SETTING_REQUESTER_BACKUP_STATE"></span>Establecer el estado de copia de seguridad del solicitante
</dt> <dd>

Un solicitante indica que una copia de seguridad es una copia de seguridad incremental o diferencial mediante la configuración de un tipo de copia de seguridad en la diferencia **\_ \_ incremental** de VSS BT o en la **\_ \_ diferencial de VSS BT** mediante el método [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) antes de generar un evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

El método [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) también se usa para indicar si el solicitante proporciona [*compatibilidad parcial con archivos*](vssgloss-p.md), que se usa con frecuencia para implementar ciertas operaciones de copia de seguridad y restauración incrementales.

</dd> </dl>

## <a name="getting-writer-specifications-for-incremental-and-differential-backups"></a>Obtener especificaciones de escritor para copias de seguridad incrementales y diferenciales

La información de especificación de copia de seguridad de archivos de nivel de conjunto de archivos ([**\_ tipo de copia de \_ \_ seguridad \_ de especificación de archivo VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) contenida en el documento de metadatos del escritor de cada escritor está disponible para su examen después de la devolución correcta de [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Sin embargo, un escritor puede agregar [*archivos diferenciados*](vssgloss-d.md) o pedir [*compatibilidad con archivos parciales*](vssgloss-p.md) hasta que el control del evento de [*instantáneas*](vssgloss-p.md) sea correcto.

La especificación de compatibilidad con archivos diferenciados y archivos parciales puede invalidar el tipo de copia de seguridad de especificación de archivo, por lo que es posible que los solicitantes deseen aplazar un análisis completo de todas las especificaciones del escritor sobre las copias de seguridad incrementales y diferenciales hasta después de la devolución correcta de [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).

<dl> <dt>

<span id="Getting_File_Backup_Specification_Information"></span><span id="getting_file_backup_specification_information"></span><span id="GETTING_FILE_BACKUP_SPECIFICATION_INFORMATION"></span>Obtención de información de especificación de copias de seguridad de archivos
</dt> <dd>

La información de especificación de copia de seguridad de archivos de nivel de conjunto de archivos ([**\_ tipo de copia de \_ \_ seguridad \_ de especificación de archivo de VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) se incluye en el documento de metadatos del escritor de cada escritor y se puede examinar inmediatamente después de la devolución correcta de [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Los solicitantes deben obtener las máscaras de especificación de copia de seguridad de archivos ([**tipo de \_ copia de \_ \_ seguridad \_ de especificación de archivo de VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) para cada conjunto de archivos de los componentes de un escritor que se van a incluir en la copia de seguridad incremental o diferencial, independientemente de si el componente se incluyó [*explícita*](vssgloss-e.md) o [*implícitamente*](vssgloss-i.md) .

Un solicitante puede determinar qué documento de metadatos del escritor de escritores se debe consultar mediante [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) y [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). La instancia de la interfaz [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) devuelta por **IVssBackupComponents:: GetWriterComponents** proporciona información del escritor a través del método [**IVssWriterComponentsExt:: GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo) .

El solicitante obtiene información de componentes a través de instancias de la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) correspondiente a un componente incluido administrado por un escritor determinado mediante [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

La información sobre los conjuntos de archivos administrados por el componente correspondiente a la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) se obtiene mediante llamadas a [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent:: GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)o [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) (según corresponda).

Estas llamadas pueden devolver instancias de la interfaz [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) para cada uno de los conjuntos de archivos de un componente.

El tipo de copia de seguridad de especificación de archivo de un conjunto de archivos se obtiene llamando a [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask).

</dd> <dt>

<span id="Getting_Partial_File_and_Differenced_File_Information"></span><span id="getting_partial_file_and_differenced_file_information"></span><span id="GETTING_PARTIAL_FILE_AND_DIFFERENCED_FILE_INFORMATION"></span>Obtención de información de archivos parciales y de diferencias
</dt> <dd>

Un solicitante obtiene información de archivos parciales y de diferencias a través de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Un solicitante puede recorrer en iteración todos los escritores incluidos en una copia de seguridad mediante [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) y [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

La instancia de una interfaz [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) devuelta por [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) proporciona acceso a todas las instancias de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente a los componentes [*incluidos explícitamente*](vssgloss-e.md) de un escritor determinado a través de los métodos [**IVssWriterComponentsExt:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) y [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) .

Un solicitante tendrá que recorrer todas las instancias de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para todos los escritores cuyo esquema sea compatible con la copia de seguridad incremental o diferencial, es decir, los escritores cuya máscara de esquema de copia de seguridad, tal como la devuelve [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), incluye el servicio de **VSS \_ BS \_ incremental** cuando el tipo de copia de seguridad **es \_ \_** **\_ \_ incremental de VSS BT** o la **diferencia de VSS \_ BS \_**

La información de los archivos parciales se obtiene mediante una llamada a [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) y [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) (consulte [trabajar con archivos parciales](working-with-partial-files.md)).

Para los sistemas de escritura que admiten operaciones de copia de seguridad en función de los datos de última modificación de un archivo (escritores cuya máscara de esquema de copia de seguridad, tal como la devuelve [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), incluye la **\_ \_ última \_ modificación de VSS BS**), la información de archivos diferenciados se obtiene llamando a [**IVssComponent:: GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) y [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile).

Tenga en cuenta que los archivos diferenciados pueden ser archivos nuevos, es decir, archivos que no son miembros de ningún archivo establecido actualmente en el documento de metadatos del escritor de un escritor determinado.

Los solicitantes no deben encontrar los archivos incluidos tanto para las operaciones de archivo parciales como para los archivos diferenciados. Si un solicitante detecta este tipo de circunstancias, debe devolver y registrar un error del escritor.

Un solicitante puede seguir optando por continuar con la copia de seguridad de los archivos del escritor problemático, pero en ese caso debe hacerlo de acuerdo con la especificación que se encuentra en la información sobre el archivo diferenciado.

</dd> </dl>

## <a name="implementing-incremental-or-differential-backups"></a>Implementar copias de seguridad incrementales o diferenciales

Antes de implementar una copia de seguridad, los solicitantes deben tener información sobre qué escritores admiten una copia de seguridad [*incremental*](vssgloss-i.md) o [*diferencial*](vssgloss-d.md) , todas las operaciones de archivos parciales solicitadas, todos los archivos diferenciados y el tipo de copia de seguridad de especificación de archivo de todos los demás archivos.

<dl> <dt>

<span id="Nonsupporting_Writers"></span><span id="nonsupporting_writers"></span><span id="NONSUPPORTING_WRITERS"></span>Escritores no compatibles
</dt> <dd>

Los escritores cuyo esquema no admiten la copia de seguridad incremental o diferencial (escritores cuya máscara de esquema de copia de seguridad, tal y como la devuelven [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), incluye **VSS \_ BS \_ incremental** cuando el tipo de copia de seguridad es de **VSS \_ BT \_ incremental** o no incluye la **\_ \_ diferencia diferencial de VSS BS** cuando el tipo de copia de seguridad es el **\_ \_ diferencial de VSS**

Esto no significa necesariamente que los datos de los escritores no vayan a participar en una operación de copia de seguridad incremental o diferencial. Sin embargo, la elección de lo que se debe hacer es a discreción del solicitante. El solicitante puede realizar cualquiera de las siguientes acciones:

-   Hacer copia de seguridad de archivos que no pertenecen a los escritores que no son compatibles (lo indican claramente al usuario)
-   Copia de seguridad de todos los archivos de escritores que no son compatibles
-   Realice una copia de seguridad incremental con los datos del sistema de archivos y los registros de historial propios del solicitante.

La última alternativa debe usarse con gran cuidado y solo si el solicitante entiende si los escritores implicados pueden admitir copias de seguridad incrementales o diferenciales y restauraciones de datos independientes del mecanismo de VSS.

</dd> <dt>

<span id="Supporting_Writers"></span><span id="supporting_writers"></span><span id="SUPPORTING_WRITERS"></span>Escritores compatibles
</dt> <dd>

Un solicitante debe procesar (en orden) todos los [*archivos diferenciados*](vssgloss-d.md)del escritor, administrar las solicitudes de [*archivos parciales*](vssgloss-p.md) y, a continuación, hacer una copia de seguridad de los archivos restantes según el tipo de copia de seguridad de especificación de archivo ([**\_ tipo de copia de \_ \_ seguridad \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)de especificación de archivo de VSS).

1.  **Copia de seguridad de archivos diferenciados:**

    Para escritores que admiten operaciones de copia de seguridad en función de los datos de última modificación (escritores cuya máscara de esquema de copia de seguridad, tal como la devuelve [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), incluye la **\_ \_ última \_ modificación de VSS BS**), un solicitante utiliza la ruta de acceso, la especificación de archivo y la información de marca de recursividad devuelta por [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) para generar una lista de archivos

    [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) también puede devolver una hora de última modificación (expresada como una estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) ).

    Si la hora de la última modificación proporcionada por el sistema de escritura es distinta de cero, el solicitante la usa como base (en lugar de la información del sistema de archivos o los datos almacenados propios del solicitante) para determinar si el archivo debe incluirse en la copia de seguridad [*incremental*](vssgloss-i.md) o [*diferencial*](vssgloss-d.md) .

    Por ejemplo, si la hora de la última modificación de un archivo devuelta por el escritor era:

    -   Después de la última copia de seguridad completa, el archivo debe estar incluido en las copias de seguridad incrementales y diferenciales.
    -   Después de la última copia de seguridad completa, pero antes de la última copia de seguridad incremental, el archivo debe incluirse en las operaciones de copia de seguridad incremental, pero no en las copias de seguridad diferenciales.

    Si la hora de la última modificación proporcionada por el escritor es cero, el solicitante debe utilizar la información del sistema de archivos y sus propios datos almacenados para determinar la hora de modificación del archivo diferenciado.

2.  **Uso de operaciones de archivo parciales:**

    Si un escritor ha solicitado que se realice una copia de seguridad de un archivo mediante una operación de archivo parcial, el solicitante usa la información de desplazamiento de archivo para guardar los segmentos de archivo indicados en el medio de copia de seguridad. (Consulte [trabajar con archivos parciales](working-with-partial-files.md) para obtener más información sobre las operaciones de archivos parciales).

    Como se indicó anteriormente, un escritor no debe designar un archivo como un archivo diferenciado y como participante en una operación de archivo parcial. Si un solicitante detecta este tipo de circunstancias, debe devolver y registrar un error del escritor.

    Un solicitante puede seguir optando por continuar con la copia de seguridad de los archivos del escritor problemático, pero en ese caso debe hacerlo de acuerdo con la especificación que se encuentra en la información sobre el archivo diferenciado.

3.  **Trabajando con el tipo de copia de seguridad de especificación de archivo:**

    Una vez procesados todos los archivos diferenciados y las operaciones de archivos parciales, el solicitante procesa ahora todos los archivos restantes en su conjunto de copia de seguridad en función del tipo de copia de seguridad de especificación de archivo (tipo de copia de seguridad de especificación de [**\_ archivo \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

    Hay tres valores de "copia de seguridad necesaria" de la enumeración de [**\_ tipo de copia de \_ \_ seguridad \_ de especificación de archivo de VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que afectan a las copias de seguridad diferenciales e incrementales:

    -   VSS \_ FSBT \_ todas las \_ copias de seguridad \_ necesarias
    -   se \_ \_ requiere la copia de seguridad incremental FSBT de VSS \_ \_
    -   se \_ \_ requiere la \_ copia de seguridad diferencial FSBT \_ de VSS

    Hay tres valores de "se requiere la instantánea":

    -   VSS \_ FSBT \_ todas las \_ instantáneas \_ necesarias
    -   se \_ \_ requiere la instantánea incremental FSBT de VSS \_ \_
    -   se \_ \_ requiere la \_ instantánea \_ diferencial FSBT de VSS

    Los conjuntos de archivos etiquetados con un tipo de copia de seguridad de especificación de archivo de "instantánea necesaria" indican que un solicitante debe copiar datos de una instantánea al realizar operaciones de copia de seguridad INCREMENTAl, diferencial o de todos (lo que incluye operaciones incrementales y diferenciales).

    La marca "se requiere copia de seguridad", que se aplica a las operaciones de copia de seguridad INCREMENTAl, diferencial o todas, indica que el escritor espera que haya una copia de la versión actual del conjunto de archivos disponible después de la restauración de cualquier operación de copia de seguridad. Por lo general, esto significa que si un conjunto de archivos se etiqueta con "se requiere copia de seguridad", un solicitante copiará todos sus miembros en el medio de copia de seguridad durante una copia de seguridad incremental o diferencial, independientemente de Cuándo se haya producido la última copia de seguridad o modificación.

    De forma predeterminada, los conjuntos de archivos se agregan a los componentes con un tipo de copia de seguridad de especificación de archivo de VSS \_ FSBT \_ All \_ backup \_ required \| VSS \_ FSBT \_ All \_ Snapshot \_ required. Por lo tanto, a menos que un escritor establezca explícitamente el tipo de copia de seguridad de especificación de archivo, de lo contrario, los solicitantes tendrán que copiar los archivos no controlados por operaciones de archivo parcial o archivos diferenciados designados en la mayoría de los conjuntos de archivos normalmente se copiarán en su totalidad en medios de copia de seguridad

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Marcas de copia de seguridad
</dt> <dd>

Los escritores que admiten sellos de copias de seguridad (marca de tiempo de VSS \_ BS \_ ) pueden optar por generar información de marca de copia de seguridad que se usará para admitir operaciones de copia de seguridad y restauración incrementales y diferenciales.

El formato y la información contenidos en las cadenas que contienen información de marca de copia de seguridad son privados para el escritor que los genera. el solicitante no sabe cómo procesar esta información.

Los escritores de soporte almacenan el sello de copia de seguridad en el documento componentes de copia de seguridad como una cadena mediante el método [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) .

El rol del solicitante en el control de la información de marca de copia de seguridad es (si existe) para que esté disponible para el escritor llamando a [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) en una operación de restauración o copia de seguridad futura.

</dd> </dl>

 

 
