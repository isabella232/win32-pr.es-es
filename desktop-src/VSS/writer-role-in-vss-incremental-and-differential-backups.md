---
description: 'Normalmente, la participación de un escritor en copias de seguridad incrementales y diferenciales tiene lugar mientras se controlan los eventos de identificación (CVssWriter:: he identify), PrepareForBackup (CVssWriter: OnPrepareBackup) y postsnapshot (CVssWriter: OnPostSnapshot).'
ms.assetid: 85c4e003-b531-4283-83aa-dd5cc53f35b1
title: Rol de escritor en copias de seguridad incrementales y diferenciales de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2cda57d907bed4572f0c0f71f9ee829bee18299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541699"
---
# <a name="writer-role-in-vss-incremental-and-differential-backups"></a>Rol de escritor en copias de seguridad incrementales y diferenciales de VSS

Normalmente, la participación de un escritor en copias de seguridad incrementales y diferenciales tiene lugar mientras se controlan los eventos de [*identificación*](vssgloss-i.md) ([**CVssWriter:: he Identify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)), [*PrepareForBackup*](vssgloss-p.md) ([**CVssWriter: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)) y *postsnapshot* ([**CVssWriter: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)). La forma en que participa un escritor es la forma de si admite marcas de copia de seguridad y horas de última modificación, y si el solicitante que ejecuta la copia de seguridad admite [*operaciones de archivo parciales*](vssgloss-p.md).

## <a name="handling-identify-events-during-incremental-and-differential-backups"></a>Control de eventos de identificación durante las copias de seguridad incrementales y diferenciales

Al controlar el evento de identificación, los escritores establecen su arquitectura básica para la operación de copia de seguridad incremental y diferencial mediante las máscaras esquema de copia de seguridad ([**\_ \_ esquema de copia de seguridad de VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)) y tipo de copia de seguridad de especificación de archivo ([**\_ \_ \_ \_ tipo de copia de seguridad**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)de especificación de archivo

Un escritor indica qué operaciones admite en su documento de metadatos del escritor mediante la creación de una máscara de bits de los valores de [**\_ \_ esquema de copia de seguridad de VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) y su paso al método [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) . Con esto, un escritor puede indicar si admite lo siguiente:

-   Copias de seguridad incrementales (se **\_ \_ incremental de VSS BS**)
-   Copias de seguridad diferenciales (de **VSS \_ BS \_ diferencial**)
-   Las copias de seguridad incrementales y diferenciales no se pueden mezclar (**VSS \_ BS \_ exclusivo \_ incremental \_ diferencial**)
-   Copias de seguridad incrementales y diferenciales mediante marcas de copia de seguridad (**VSS \_ BS \_ timestamp**)
-   Copias de seguridad incrementales y diferenciales en base a la información sobre la última modificación de un archivo (**VSS \_ BS \_ última \_ modificación**)

Los escritores usan la máscara de tipo de copia de seguridad de especificación de archivo para proporcionar información de nivel de conjunto de archivos a los solicitantes sobre cómo incluir archivos en una copia de seguridad incremental o diferencial.

Un escritor puede establecer la máscara del tipo de copia de seguridad de la especificación de archivo de un conjunto de archivos cuando agrega el conjunto de archivos a un componente mediante la creación de una máscara de bits de los valores del tipo de copia de seguridad de las especificaciones de archivo de VSS y pasándolo a [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup). [**\_ \_ \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)

Hay tres valores de "copia de seguridad necesaria" de la enumeración de [**\_ tipo de copia de \_ \_ seguridad \_ de especificación de archivo de VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que afectan a las copias de seguridad diferenciales e incrementales:

-   **VSS \_ FSBT \_ todas las \_ copias de seguridad \_ necesarias**
-   **se \_ \_ requiere la copia de seguridad incremental FSBT de VSS \_ \_**
-   **se \_ \_ requiere la \_ copia de seguridad diferencial FSBT \_ de VSS**

Hay tres valores de "se requiere la instantánea":

-   **VSS \_ FSBT \_ todas las \_ instantáneas \_ necesarias**
-   **se \_ \_ requiere la instantánea incremental FSBT de VSS \_ \_**
-   **se \_ \_ requiere la \_ instantánea \_ diferencial FSBT de VSS**

Los conjuntos de archivos etiquetados con un tipo de copia de seguridad de especificación de archivo de "instantánea necesaria" indican si un solicitante debe copiar datos de una instantánea al realizar operaciones de copia de seguridad INCREMENTAl, diferencial o de todos (lo que incluye operaciones incrementales y diferenciales).

La marca "se requiere copia de seguridad", que se aplica a las operaciones de copia de seguridad INCREMENTAl, diferencial o todas, indica que el escritor espera que haya una copia de la versión actual del conjunto de archivos disponible después de la restauración de cualquier operación de copia de seguridad. Normalmente, esto significa que si un conjunto de archivos se etiqueta con "se requiere copia de seguridad", todos sus miembros se copiarán en el medio de copia de seguridad durante una copia de seguridad incremental o diferencial, independientemente de Cuándo se haya producido la última copia de seguridad o modificación.

De forma predeterminada, los conjuntos de archivos se agregan a los componentes con un tipo de copia de seguridad de especificación de archivo de **VSS \_ FSBT \_ All \_ backup \_ required** \| **VSS \_ FSBT \_ All \_ Snapshot \_ required**. Por lo tanto, a menos que un programador del escritor decida no usar el valor predeterminado (al elegir otro tipo de copia de seguridad de especificación de archivo, usar operaciones de archivo parciales o usar archivos diferenciados), los archivos de la mayoría de los conjuntos de archivos se copiarán normalmente en su totalidad en medios de copia de seguridad.

En este momento, el documento de metadatos del escritor del escritor se rellena completamente con la mayor parte de la información que necesitará un solicitante para iniciar una copia de seguridad diferencial o incremental. La especificación adicional del conjunto de archivos o la información de nivel de archivo para admitir la copia de seguridad se controlará durante el evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

## <a name="handling-prepareforbackup-events-during-incremental-and-differential-backups"></a>Control de eventos PrepareForBackup durante las copias de seguridad incrementales y diferenciales

Antes de que el solicitante continúe con la operación de copia de seguridad real, los escritores pueden modificar la especificación de una copia de seguridad [*incremental*](vssgloss-i.md) o [*diferencial*](vssgloss-d.md) mediante la modificación del documento de componentes de copia de seguridad del solicitante a través de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Dado que los escritores usan la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , normalmente realizan estos preparativos al controlar el evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

En [**CVssWriter: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup), los escritores pueden especificar con mayor precisión el modo en que algunos archivos se van a evaluar para la copia de seguridad, especificar qué mecanismos deben usarse para realizar copias de seguridad y, posiblemente, establecer marcas de copia de seguridad.

<dl> <dt>

<span id="Partial_Files"></span><span id="partial_files"></span><span id="PARTIAL_FILES"></span>Archivos parciales
</dt> <dd>

Si un solicitante los admite, un escritor puede elegir tener una copia de seguridad incremental o diferencial implementada mediante operaciones de archivo parciales. (Los escritores pueden determinar si un solicitante admite operaciones de archivo parciales mediante una llamada a [**CVssWriter:: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)).

Los escritores usan [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) para indicar las partes de los archivos seleccionados de los que se va a realizar una copia de seguridad durante la operación diferencial o incremental. Los solicitantes deben respetar esta especificación y siempre deben realizar copias de seguridad de las secciones especificadas de los archivos. (Consulte [trabajar con archivos parciales](working-with-partial-files.md) para obtener más información sobre las operaciones de archivo parciales).

Mediante [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile), un escritor puede Agregar un archivo a la copia de seguridad que no se agregó previamente a uno de sus conjuntos de componentes (por [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) como un archivo parcial. Los archivos nuevos que se agreguen a la copia de seguridad de esta manera deben estar en un volumen del que ya se estén realizando instantáneas para esta copia de seguridad.

Si un archivo está implicado en operaciones de archivo parcial, reemplaza cualquier tipo de copia de seguridad de especificación de archivo, que se omite.

</dd> <dt>

<span id="Differenced_Files"></span><span id="differenced_files"></span><span id="DIFFERENCED_FILES"></span>Archivos diferenciados
</dt> <dd>

Los escritores que admiten un esquema de copia de seguridad de última modificación (**\_ \_ esquema de VSS BS**) pueden agregar [*archivos diferenciados*](vssgloss-d.md) a una copia de seguridad incremental o diferencial.

En la especificación de un archivo diferenciado, un escritor usa [**IVssComponent:: AddDifferencedFileByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) y especifica una ruta de acceso, un nombre de archivo y una marca recursiva; sin embargo, no es necesario que coincidan con un conjunto de archivos incluido en ningún componente.

De hecho, un escritor puede Agregar un archivo que no se haya agregado previamente a uno de sus conjuntos de componentes (por [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) a la copia de seguridad como un archivo diferenciado. Los archivos nuevos que se agreguen a la copia de seguridad de esta manera deben estar en un volumen del que ya se estén realizando instantáneas para esta copia de seguridad.

Normalmente, un sistema de escritura también especificará una hora de última modificación al agregar un archivo diferenciado, en función del propio mecanismo de historial del escritor. La hora de la última modificación, si se especifica, siempre debe ser utilizada por los solicitantes para determinar si un archivo debe incluirse en una copia de seguridad incremental o diferencial.

Un escritor puede optar por no especificar una hora de última modificación al agregar un archivo diferenciado a un conjunto de copia de seguridad incremental o diferencial. Si este es el caso, los solicitantes pueden usar sus propios mecanismos, por ejemplo, registros de copias de seguridad anteriores o información del sistema de archivos, para determinar si el archivo diferenciado debe incluirse en una copia de seguridad incremental o diferencial.

Se omite el tipo de copia de seguridad de especificación de archivo de cualquier archivo diferenciado.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Marcas de copia de seguridad
</dt> <dd>

Los escritores que admiten marcas de copia de seguridad (**VSS \_ BS \_ timestamp**) tienen su propio formato privado para almacenar información sobre cuándo se produjo una copia de seguridad por última vez. El escritor genera esta información durante la copia de seguridad.

El sello de copia de seguridad se almacena en el documento componentes de copia de seguridad como una cadena mediante el método [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) . La marca de copia de seguridad se aplica a todos los conjuntos de archivos del componente (o conjunto de componentes) correspondientes a la instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

Si un solicitante tiene acceso al sello de copia de seguridad de una copia de seguridad anterior, lo hará disponible para el escritor llamando a [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp).

Después, un escritor puede examinar esta marca de tiempo mediante [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).

Tenga en cuenta que el solicitante simplemente almacena y devuelve la cadena que contiene el sello de la copia de seguridad. No se sabe nada sobre el formato de la cadena o cómo usarlo; solo el escritor tiene esa información.

Un escritor puede optar por actualizar el sello de copia de seguridad actual mediante [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) después de haber llamado a [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp), con lo que se graba en su propio formato la fecha de la operación de copia de seguridad incremental o diferencial actual.

</dd> </dl>

 

 



