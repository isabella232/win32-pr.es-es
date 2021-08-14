---
description: Trabajar con componentes seleccionados implícitamente requiere acceso tanto al documento componentes de copia de seguridad como a los documentos de metadatos del escritor.
ms.assetid: ede51931-be50-4286-818b-0e6122247bdd
title: Capacidad de selección y trabajo con propiedades de componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735481d4bd0d7fdaa4102026b74ca78be947afbab24858d88d9210dd7bd4e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751657"
---
# <a name="selectability-and-working-with-component-properties"></a>Capacidad de selección y trabajo con propiedades de componente

Trabajar con componentes seleccionados implícitamente requiere acceso tanto al documento componentes de copia de seguridad como a los documentos de metadatos del escritor.

Hay dos motivos para ello:

-   Los datos del componente almacenados en el documento de componentes de copia de seguridad (representado por la interfaz [**IVssComponent)**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) carecen de acceso a la información del conjunto de archivos de componentes( especificación de archivo, ruta de acceso y marca de recursividad). (Consulte [El documento Trabajar con componentes de copia de seguridad).](working-with-the-backup-components-document.md)
-   Solo los componentes que se [*incluyen explícitamente en*](vssgloss-e.md) el documento Componentes de copia de seguridad durante la copia de seguridad tienen su información almacenada directamente en el documento Componentes de copia de seguridad. Los solicitantes y escritores deben usar la información disponible a [](vssgloss-l.md) través de la interfaz [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) junto [](vssgloss-i.md) con la información de ruta de acceso lógica y los documentos de metadatos del escritor para obtener información sobre los componentes incluidos implícitamente y establecer las propiedades de ellos.

El caso "MyWriter" que se describe en Ruta de acceso lógica de [componentes](logical-pathing-of-components.md) se puede usar para ilustrar la capacidad de selección de la copia de seguridad.



| Nombre de componente | Ruta de acceso lógica            | Seleccionable para copia de seguridad | Seleccionable para la restauración | Incluido explícitamente |
|----------------|-------------------------|-----------------------|------------------------|---------------------|
| "Ejecutables"  | ""                      | N                     | N                      | Y                   |
| "ConfigFiles"  | "Ejecutables"           | N                     | N                      | Y                   |
| "LicenseInfo"  | ""                      | Y                     | N                      | Y                   |
| "Security"     | ""                      | Y                     | N                      | Y                   |
| "UserInfo"     | "Security"              | N                     | N                      | N                   |
| "Certificados" | "Security"              | N                     | N                      | N                   |
| "writerData"   | ""                      | Y                     | Y                      | Y                   |
| "Set1"         | "writerData"            | N                     | Y                      | N                   |
| "Jan"          | "writerData \\ Set1"      | N                     | N                      | N                   |
| "Dec"          | "writerData \\ Set1"      | N                     | N                      | N                   |
| "Set2"         | "writerData"            | N                     | Y                      | N                   |
| "Jan"          | "writerData \\ Set2"      | N                     | N                      | N                   |
| "Dec"          | "writerData \\ Set2"      | N                     | N                      | N                   |
| "Consulta"        | "writerData \\ QueryLogs" | N                     | N                      | N                   |
| "Uso"        | "writerData"            | Y                     | Y                      | N                   |
| "Jan"          | "writerData \\ Usage"     | N                     | N                      | N                   |
| "Dec"          | "writerData \\ Usage"     | N                     | N                      | N                   |



 

## <a name="implicitly-included-components-in-the-backup-set"></a>Componentes incluidos implícitamente en el conjunto de copia de seguridad

Al examinar el documento de metadatos del escritor (vea [**IVssBackupComponents::GetWriterMetadata)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)durante la copia de [](vssgloss-l.md)seguridad, un solicitante debe almacenar una lista de todos los componentes, sus rutas de acceso lógicas y su información del conjunto de archivos.

Se necesita información sobre el conjunto de archivos y los archivos excluidos para determinar una lista de archivos para cualquier componente incluido (explícita o implícitamente).

En el caso de componentes de copia de seguridad no seleccionables sin seleccionables para antecesores de copia de seguridad y seleccionables para los componentes de copia de seguridad que no definen un conjunto de componentes [*,*](vssgloss-c.md)solo será necesario el conjunto de archivos y la información de archivo excluida para identificar todos los candidatos del componente para la copia de seguridad, ya que estos componentes no definen subcomponentes.

En el caso de los componentes de copia de seguridad que se pueden seleccionar explícitamente que definen un conjunto de componentes, los archivos establecen y excluyen la información de archivo para el componente de definición y todos los [*subcomponentes*](vssgloss-s.md) deben usarse para seleccionar archivos para la copia de seguridad.

Esto significa que los conjuntos de copia de seguridad de los componentes "Ejecutables", "ConfigFiles" y "LicenseInfo" solo se pueden encontrar examinando los metadatos del sistema de escritura solo para estos componentes mediante sus instancias de la [**interfaz IVssWMComponent.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)

Sin embargo, si writerData se incluye explícitamente en la copia de seguridad, debe examinar su instancia de la [**interfaz IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) y las de "Set1", "Jan" (con la ruta de acceso lógica "writerData Set1"), "Dec" (con la ruta de acceso lógica \\ "writerData Set1"), "Set2", "Jan" (con la ruta de acceso lógica "writerData Set2"), "Dec" (con la ruta de acceso lógica \\ \\ "writerData \\ Set2"), "Query", "Usage", "Jan" (con la ruta de acceso lógica "writerData Usage") y \\ "Dec" (con la ruta de acceso lógica "writerData \\ Usage").

Para ello, un solicitante tendrá que identificar primero que el componente "writerData" (ruta de acceso lógica "") es seleccionable. A continuación, tendrá que examinar todos los demás componentes administrados por el escritor para determinar si el primer elemento de su ruta de acceso lógica es "writerData". Los componentes que tienen "writerData" como miembros principales de su ruta de acceso lógica se identifican como subcomponentes de "writerData" y se seleccionan implícitamente cuando se selecciona explícitamente.

De hecho, será necesario realizar un examen similar para determinar que ningún componente tiene "LicenseInfo" como miembro principal de su ruta de acceso lógica y, por tanto, que "LicenseInfo" no tiene subcomponentes.

Debido a la complejidad de este mecanismo en VSS, a muchos escritores solicitantes les puede resultar útil crear sus propias estructuras para almacenar información de componentes y conjunto de copia de seguridad para componentes agregados explícita e implícitamente.

## <a name="properties-of-implicitly-included-components"></a>Propiedades de componentes incluidos implícitamente

Durante las operaciones de restauración y copia de seguridad, las instancias de las interfaces [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) e [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) se usan tanto para recuperar información sobre los componentes como para establecer o cambiar las propiedades del componente. Sin embargo, solo los componentes incluidos explícitamente tendrán instancias de la **interfaz IVssComponent** o serán accesibles para la **interfaz IVssBackupComponents.**

Algunas propiedades son de ámbito de conjunto de componentes. Estas propiedades incluyen lo siguiente:

-   Estado de copia de seguridad y restauración: <dl>

[**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)  
    [**IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)  
    [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)  
    [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)  
    </dl>
-   Opciones de copia de seguridad y restauración: <dl>

[**IVssBackupComponents::SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions)  
    [**IVssComponent::GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)  
    [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)  
    [**IVssComponent::GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)  
    </dl>
-   Mensajes de error: <dl>

[**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    [**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    </dl>
-   Destinos de restauración: <dl>

[**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)  
    [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)  
    </dl>
-   Marcas de copia de seguridad: <dl>

[**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)  
    [**IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)  
    </dl>
-   Metadatos adicionales: <dl>

[**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)  
    [**IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)  
    [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)  
    [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)  
    </dl>

Por lo tanto, se usa la instancia de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) del miembro de definición de un conjunto de componentes o se usa el nombre, el tipo y la ruta de acceso lógica del miembro de definición con un método [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) para establecer o recuperar las propiedades de todos los miembros del conjunto de componentes.

Por este motivo, los conjuntos de componentes se tratan como unidades. Por ejemplo, una copia de seguridad de un conjunto de componentes es correcta solo si la copia de seguridad de todos los conjuntos de archivos de todos sus componentes es correcta.

En el ejemplo anterior, supongamos que un archivo del componente "Jan" (con la ruta de acceso lógica "writerData Set2") es miembro del conjunto de componentes definido \\ por "writerData". Si no se pudo hacer una copia de seguridad de uno de los archivos de "Jan", un solicitante usaría la información de "writerData" (su nombre "writerData", su ruta de acceso "" y su tipo de componente) como argumentos al establecer [**IVssBackupComponents::SetBackupSucceeded con**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) **false** para indicar el error del conjunto de componentes.

Del mismo modo, el estado devuelto por [**IVssComponent::GetBackupSucceeded para**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) la instancia de "writerData" de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) no solo se aplica a "writerData", sino también a todos sus subcomponentes.

Además, si un escritor decide cambiar el destino de restauración mediante [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) de la instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)de "writerData", cambiaría el destino de restauración de todos los conjuntos de archivos de todos los subcomponentes de "writerData".

Las siguientes propiedades no se aplican a todo el componente, sino a determinados archivos o conjuntos de archivos:

-   Asignaciones de ubicación alternativas: <dl>

[**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)  
    [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)  
    [**IVssComponent::GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)  
    </dl>
-   Archivos con diferencias: <dl>

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)  
    [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)  
    [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)  
    </dl>
-   Archivos parciales: <dl>

[**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)  
    [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)  
    [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)  
    </dl>
-   Destinos dirigidos: <dl>

[**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)  
    [**IVssComponent::GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)  
    [**IVssComponent::GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount)  
    </dl>
-   Nuevos destinos: <dl>

[**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)  
    [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)  
    [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)  
    </dl>

Cuando un solicitante tiene acceso a estas características para un subcomponente mediante la interfaz [**IVssBackupComponents,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) usa la información de componente para el componente de definición del conjunto de componentes, pero la información del archivo o del conjunto de archivos para el subcomponente.

Del mismo modo, si se puede acceder a la propiedad a través de la interfaz [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) se usa la instancia correspondiente al subcomponente de definición, pero los argumentos del archivo o del conjunto de archivos se toman del subcomponente.

Por ejemplo, suponga que el subcomponente "Jan" (con la ruta de acceso lógica "writerData Set2") tenía un archivo establecido con una ruta de acceso de "c: fred", una especificación de archivo de ".dat" y una marca recursiva de true podría tener que restaurarse en \\ \\ una ubicación \* alternativa. 

Si este fuera el caso, un solicitante llamaría a [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)mediante la información de "writerData" (tipo de componente, un nombre de componente de "writeData" y una ruta de acceso lógica de "") junto con la información del conjunto de archivos de "Jan" (ruta de acceso "c: fred", especificación de archivo \\ " .dat" y recursividad es igual a \* **true).**

Tenga en cuenta que, en este caso, la información del conjunto de archivos debe coincidir exactamente con la información del conjunto de archivos que usa [**IVssCreateWriterMetadata::AddFilesToFileGroup,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) para agregar archivos a Jan.

De forma similar, si un escritor quisiera agregar un destino dirigido a un archivo con una ruta de acceso de "c: ethel" y el nombre "mv.dat" administrado por "Jan" (con la ruta de acceso lógica "writerData Set2"), usaría la instancia de IVssComponent correspondiente a \\ "writerData", pero la información de archivo \\ de "Jan". [](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

## <a name="implicitly-included-components-in-the-restore-set"></a>Componentes incluidos implícitamente en el conjunto de restauración

Los componentes que se incluyeron implícitamente en una copia de seguridad se pueden incluir explícitamente en una restauración si se pueden seleccionar para la restauración. Como se indicó en Working [with Selectability for Restore and Subcomponents](working-with-selectability-for-restore-and-subcomponents.md)( Trabajar con selectibilidad para la restauración y los subcomponentes), estos componentes se agregan al documento Componentes de copia de seguridad mediante el método [**IVssBackupComponents::AddRestoreSubcomponent.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)

Sin embargo, esto no crea una nueva instancia de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ni es el componente accesible directamente a través de la [**interfaz IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)

En su lugar, se debe tener acceso a un componente incluido explícitamente para la restauración, pero incluido implícitamente para la copia de seguridad, a través de una instancia de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente al componente que definió el conjunto de componentes del que era miembro tras la copia de seguridad.

Por ejemplo, para incluir explícitamente para la restauración "Set1", un subcomponente del componente seleccionable para copia de seguridad "writerData", obtendría información al llamar al método [**IVssComponent::GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent) de la instancia de "writerData" de la [**interfaz IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

 

 



