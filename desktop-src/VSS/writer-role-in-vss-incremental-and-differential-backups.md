---
description: La participación de un escritor en copias de seguridad incrementales y diferenciales suele tener lugar al controlar eventos Identify (CVssWriter::OnIdentify), PrepareForBackup (CVssWriter:OnPrepareBackup) y PostSnapshot (CVssWriter:OnPostSnapshot).
ms.assetid: 85c4e003-b531-4283-83aa-dd5cc53f35b1
title: Rol escritor en copias de seguridad incrementales y diferenciales de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2cda57d907bed4572f0c0f71f9ee829bee18299
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241124"
---
# <a name="writer-role-in-vss-incremental-and-differential-backups"></a>Rol escritor en copias de seguridad incrementales y diferenciales de VSS

La participación de un escritor en copias de seguridad incrementales y diferenciales suele tener lugar al controlar los eventos [*Identify*](vssgloss-i.md) [**(CVssWriter::OnIdentify),**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) [*PrepareForBackup*](vssgloss-p.md) ([**CVssWriter:OnPrepareBackup)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)y *PostSnapshot* [**(CVssWriter:OnPostSnapshot).**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) La forma en que participa un escritor se determina si admite marcas de copia de seguridad y las últimas horas de modificación, y si el solicitante que ejecuta la copia de seguridad admite operaciones [*de archivo parciales*](vssgloss-p.md).

## <a name="handling-identify-events-during-incremental-and-differential-backups"></a>Control de eventos de identificación durante copias de seguridad incrementales y diferenciales

Al controlar el evento Identify, los escritores establecen su arquitectura básica para la operación de copia de seguridad incremental y diferencial a través del esquema de copia de seguridad (ESQUEMA DE COPIA DE SEGURIDAD DE [**VSS) \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)y las máscaras del tipo de copia de seguridad de especificación de archivo [**(VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE).**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)

Un sistema de escritura indica qué operaciones admite en su documento de metadatos del escritor mediante la creación de una máscara de bits de valores DE ESQUEMA DE COPIA DE SEGURIDAD de [**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) y su paso al método [**IVssCreateWriterMetadata::SetBackupSchema.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) Con esto, un escritor puede indicar si admite lo siguiente:

-   Copias de seguridad **incrementales (INCREMENTAL \_ de VSS BS) \_**
-   Copias de seguridad **diferenciales \_ (VSS BS \_ DIFFERENTIAL)**
-   No se pueden mezclar copias de seguridad incrementales y diferenciales **(DIFERENCIAL \_ INCREMENTAL EXCLUSIVO \_ \_ \_ DE VSS BS)**
-   Copias de seguridad incrementales y diferenciales mediante marcas de copia de seguridad **\_ (VSS BS \_ TIMESTAMPED)**
-   Copias de seguridad incrementales y diferenciales en función de la información sobre la última modificación de un archivo (**\_ VSS BS \_ LAST \_ MODIFY**)

Los escritores usan la máscara de tipo de copia de seguridad de especificación de archivo para proporcionar información de nivel de conjunto de archivos a los solicitantes sobre cómo incluir archivos en una copia de seguridad incremental o diferencial.

Un escritor puede establecer la máscara de tipo de copia de seguridad de especificación de archivos de un conjunto de archivos cuando agrega el conjunto de archivos a un componente mediante la creación de una máscara de bits de valores DE TIPO BACKUP de SPEC DE [**VSS \_ FILE \_ \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) y su paso a [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles). [](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)

Hay tres valores "se requiere copia de seguridad" de la enumeración [**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que afectan a las copias de seguridad diferenciales e incrementales:

-   **VSS \_ FSBT \_ ALL \_ BACKUP \_ REQUIRED**
-   **SE REQUIERE COPIA \_ DE SEGURIDAD INCREMENTAL DE VSS FSBT \_ \_ \_**
-   **SE REQUIERE COPIA \_ DE SEGURIDAD DIFERENCIAL DE VSS FSBT \_ \_ \_**

Hay tres valores de "instantánea necesaria":

-   **VSS \_ FSBT \_ ALL \_ SNAPSHOT \_ REQUIRED**
-   **INSTANTÁNEA \_ INCREMENTAL DE VSS FSBT \_ \_ \_ NECESARIA**
-   **INSTANTÁNEA DIFERENCIAL \_ DE VSS FSBT \_ \_ \_ NECESARIA**

Los conjuntos de archivos etiquetados con un tipo de copia de seguridad de especificación de archivo de "instantánea necesaria" indican si un solicitante necesita copiar datos de una instantánea al realizar operaciones de copia de seguridad INCREMENTAL, DIFFERENTIAL o ALL (que incluye operaciones incrementales y diferenciales).

La marca "copia de seguridad necesaria", aplicada a las operaciones de copia de seguridad INCREMENTAL, DIFFERENTIAL o ALL, indica que el escritor espera que una copia de la versión actual del conjunto de archivos esté disponible después de la restauración de cualquier operación de copia de seguridad. Normalmente, esto significa que si un conjunto de archivos se etiqueta con "copia de seguridad necesaria", todos sus miembros se copiarán en los medios de copia de seguridad durante una copia de seguridad incremental o diferencial, independientemente de cuándo se produjo la última vez que se produjo la copia de seguridad o la modificación.

De forma predeterminada, los conjuntos de archivos se agregan a los componentes con un tipo de copia de seguridad de especificación de archivo **de VSS \_ FSBT \_ ALL BACKUP \_ \_ REQUIRED** \| **VSS \_ FSBT \_ ALL SNAPSHOT \_ \_ REQUIRED**. Por lo tanto, a menos que un desarrollador de escritores decida no usar el valor predeterminado (al elegir otro tipo de copia de seguridad de especificación de archivo, mediante operaciones de archivos parciales o mediante archivos diferenciados), los archivos de la mayoría de los conjuntos de archivos normalmente se copiarán en su totalidad en medios de copia de seguridad.

En este punto, el documento de metadatos del escritor se rellena completamente con la mayor parte de la información que un solicitante necesitará para iniciar una copia de seguridad diferencial o incremental. La especificación adicional del conjunto de archivos o la información de nivel de archivo para admitir la copia de seguridad se controlará durante el [**evento PrepareForBackup.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)

## <a name="handling-prepareforbackup-events-during-incremental-and-differential-backups"></a>Control de eventos PrepareForBackup durante copias de seguridad incrementales y diferenciales

Antes de que el solicitante continúe con la operación de copia [](vssgloss-d.md) de seguridad real, los escritores pueden modificar la especificación de una copia de seguridad [*incremental*](vssgloss-i.md) o diferencial modificando el documento de componentes de copia de seguridad del solicitante a través de la interfaz [**IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Dado que los escritores usan la [**interfaz IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) normalmente realizan estos preparativos mientras se administra [**el evento PrepareForBackup.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)

En [**CVssWriter:OnPrepareBackup,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)los escritores pueden especificar con más precisión cómo se van a evaluar algunos archivos para la copia de seguridad, especificar qué mecanismos se deben usar para realizar copias de seguridad y, posiblemente, establecer marcas de copia de seguridad.

<dl> <dt>

<span id="Partial_Files"></span><span id="partial_files"></span><span id="PARTIAL_FILES"></span>Archivos parciales
</dt> <dd>

Si un solicitante los admite, un escritor puede optar por implementar una copia de seguridad incremental o diferencial mediante operaciones de archivo parciales. (Los escritores pueden determinar si un solicitante admite operaciones de archivos parciales llamando a [**CVssWriter::IsPartialFileSupportEnabled).**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)

Los escritores [**usan IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) para indicar las partes de los archivos seleccionados de los que se va a realizar una copia de seguridad durante la operación incremental o diferencial. Los solicitantes deben respetar esta especificación y siempre deben hacer una copia de seguridad de las secciones especificadas de los archivos. (Vea [Trabajar con archivos parciales para](working-with-partial-files.md) obtener más información sobre las operaciones de archivos parciales).

Mediante [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile), un escritor puede agregar un archivo a la copia de seguridad que no se agregó previamente a uno de sus conjuntos de componentes (por [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata::AddDatabaseLogFiles o**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) [**IVssCreateWriterMetadata::AddFilesToFileGroup)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)como un archivo parcial. Los archivos nuevos agregados a la copia de seguridad de esta manera deben estar en un volumen que ya se está copiando en la sombra para esta copia de seguridad.

Si un archivo está implicado en operaciones de archivo parciales, sustituye a cualquier tipo de copia de seguridad de especificación de archivo, que se omite.

</dd> <dt>

<span id="Differenced_Files"></span><span id="differenced_files"></span><span id="DIFFERENCED_FILES"></span>Archivos diferenciados
</dt> <dd>

Los escritores que admiten un esquema de copia [](vssgloss-d.md) de seguridad modificado por última vez (ESQUEMA DE **\_ VSS BS) \_** pueden agregar archivos diferenciados a una copia de seguridad incremental o diferencial.

Al especificar un archivo diferenciado, un escritor usa [**IVssComponent::AddDifferencedFileByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) y especifica una ruta de acceso, un nombre de archivo y una marca recursiva; sin embargo, no tienen que coincidir con un conjunto de archivos incluido en ningún componente.

De hecho, un escritor puede agregar un archivo no agregado previamente a uno de sus conjuntos de componentes (por [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata::AddFilesToFileGroup)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)a la copia de seguridad como un archivo diferenciado. Los archivos nuevos agregados a la copia de seguridad de esta manera deben estar en un volumen que ya se está copiando en la sombra para esta copia de seguridad.

Normalmente, un escritor también especificará la hora de la última modificación al agregar un archivo diferenciado, en función del mecanismo de historial propio del escritor. Esta última hora de modificación, si se especifica, siempre debe ser utilizada por los solicitantes para determinar si un archivo debe incluirse en una copia de seguridad incremental o diferencial.

Un escritor puede optar por no especificar una hora de última modificación al agregar un archivo diferenciado a un conjunto de copia de seguridad incremental o diferencial. Si este es el caso, los solicitantes pueden usar sus propios mecanismos (por ejemplo, registros de copias de seguridad anteriores o información del sistema de archivos) para determinar si el archivo diferenciado debe incluirse en una copia de seguridad incremental o diferencial.

Se omite el tipo de copia de seguridad de especificación de archivo de cualquier archivo diferenciado.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Marcas de copia de seguridad
</dt> <dd>

Los escritores que admiten marcas de copia de seguridad **\_ (VSS BS \_ TIMESTAMP)** tienen su propio formato privado para almacenar información sobre cuándo se produjo una última copia de seguridad. El escritor genera esta información durante la copia de seguridad.

El método [**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) almacena la marca de copia de seguridad en el documento de componentes de copia de seguridad como una cadena. La marca de copia de seguridad se aplica a todos los conjuntos de archivos del componente (o conjunto de componentes) correspondientes a la instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

Si un solicitante tiene acceso a la marca de copia de seguridad de una copia de seguridad anterior, habrá puestola a disposición del escritor mediante una llamada a [**IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp).

A continuación, un escritor puede examinar esta marca de tiempo [**mediante IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).

Tenga en cuenta que el solicitante simplemente almacena y devuelve la cadena que contiene la marca de copia de seguridad. No sabe nada sobre el formato de la cadena ni cómo usarlo; solo el escritor tiene esa información.

Un escritor puede optar por actualizar la marca de copia de seguridad actual mediante [**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) después de llamar a [**IVssComponent::GetPreviousBackupStamp,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)registrando así en su propio formato la fecha de la operación de copia de seguridad incremental o diferencial actual.

</dd> </dl>

 

 



