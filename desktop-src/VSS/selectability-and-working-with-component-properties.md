---
description: El trabajo con componentes seleccionados implícitamente requiere acceso a los documentos de componentes de copia de seguridad documentos y de metadatos del escritor.
ms.assetid: ede51931-be50-4286-818b-0e6122247bdd
title: Selección y trabajo con propiedades de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d06683bafb02802d84f152f1ceb662eb7491f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156104"
---
# <a name="selectability-and-working-with-component-properties"></a>Selección y trabajo con propiedades de componentes

El trabajo con componentes seleccionados implícitamente requiere acceso a los documentos de componentes de copia de seguridad documentos y de metadatos del escritor.

Hay dos motivos para ello:

-   Los datos de componentes almacenados en el documento componentes de copia de seguridad (representado por la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ) no tienen acceso a la información de conjunto de archivos de componentes: especificación de archivo, ruta de acceso y marca de recursividad. (Vea [trabajar con el documento componentes de copia de seguridad](working-with-the-backup-components-document.md)).
-   Solo los componentes que se [*incluyen explícitamente*](vssgloss-e.md) en el documento componentes de copia de seguridad durante la copia de seguridad tienen su información almacenada directamente en el documento componentes de copia de seguridad. Los solicitantes y escritores deben usar la información disponible a través de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , junto con la información de [*ruta de acceso lógica*](vssgloss-l.md) y los documentos de metadatos del escritor para obtener información sobre y establecer las propiedades de los componentes [*incluidos implícitamente*](vssgloss-i.md) .

El caso "alwriter" descrito en las [acciones lógicas de los componentes](logical-pathing-of-components.md) puede usarse para ilustrar la posibilidad de seleccionar la copia de seguridad.



| Nombre de componente | Ruta de acceso lógica            | Seleccionable para copia de seguridad | Seleccionable para restauración | Incluido explícitamente |
|----------------|-------------------------|-----------------------|------------------------|---------------------|
| Aplicaciones  | ""                      | N                     | N                      | Y                   |
| "ConfigFiles"  | Aplicaciones           | N                     | N                      | Y                   |
| "LicenseInfo"  | ""                      | Y                     | N                      | Y                   |
| "Security"     | ""                      | Y                     | N                      | Y                   |
| UserInfo     | "Security"              | N                     | N                      | N                   |
| Firma | "Security"              | N                     | N                      | N                   |
| "writerData"   | ""                      | Y                     | Y                      | Y                   |
| Set1         | "writerData"            | N                     | Y                      | N                   |
| Bernardo          | "writerData \\ Set1"      | N                     | N                      | N                   |
| Dec          | "writerData \\ Set1"      | N                     | N                      | N                   |
| Set2         | "writerData"            | N                     | Y                      | N                   |
| Bernardo          | "writerData \\ Set2"      | N                     | N                      | N                   |
| Dec          | "writerData \\ Set2"      | N                     | N                      | N                   |
| Misma        | "writerData \\ QueryLogs" | N                     | N                      | N                   |
| Uso        | "writerData"            | Y                     | Y                      | N                   |
| Bernardo          | "uso de writerData \\ "     | N                     | N                      | N                   |
| Dec          | "uso de writerData \\ "     | N                     | N                      | N                   |



 

## <a name="implicitly-included-components-in-the-backup-set"></a>Componentes incluidos implícitamente en el conjunto de copia de seguridad

Al examinar el documento de metadatos del escritor de un escritor (consulte [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) durante la copia de seguridad, un solicitante debe almacenar una lista de todos los componentes, sus rutas de acceso [*lógicas*](vssgloss-l.md)y su información de conjunto de archivos.

Se necesitará información sobre el conjunto de archivos y el archivo excluido para determinar una lista de archivos para cualquier componente incluido (explícita o implícitamente).

En el caso de los componentes de copia de seguridad que no se pueden seleccionar y que no pueden seleccionarse para los antecesores de copia de seguridad y se pueden seleccionar para los componentes de copia de seguridad que no definen un [*conjunto de componentes*](vssgloss-c.md), solo se necesitará un conjunto de archivos y información de archivos excluidos para identificar todos los candidatos del componente para la copia de seguridad, ya que estos componentes

En el caso de los componentes de copia de seguridad, que se pueden incluir explícitamente y que definen un conjunto de componentes, el archivo establece y excluye la información del archivo para el componente de definición y todos los [*subcomponentes*](vssgloss-s.md) deben usarse para seleccionar archivos para copia de seguridad.

Esto significa que los conjuntos de copia de seguridad para los componentes "ejecutables", "ConfigFiles" y "LicenseInfo" solo se pueden encontrar examinando los metadatos del escritor solo para estos componentes mediante sus instancias de la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) .

Sin embargo, si writerData se incluye explícitamente en la copia de seguridad, debe examinar su instancia de la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) y las de "Set1", "Jan" (con la ruta de acceso lógica "writerData \\ Set1"), "Dec" (con la ruta de acceso lógica "writerData \\ Set1"), "Set2", "Jan" (con la ruta de acceso lógica "writerData \\ Set2"), "Dec" (con la ruta de acceso lógica "writerData \\ Set2"), "Query", "Usage", "Jan" (con la ruta de acceso lógica "writerData \\ Usage") y " \\

Para ello, un solicitante tendrá que identificar primero que el componente "writerData" (ruta de acceso lógica "") es seleccionable. A continuación, tendrá que analizar todos los demás componentes administrados por el escritor para determinar si el primer elemento de su ruta de acceso lógica es "writerData". Los componentes que tienen "writerData" como miembros principales de su ruta de acceso lógica se identifican como subcomponentes de "writerData" y se seleccionan implícitamente cuando se seleccionan explícitamente.

De hecho, es necesario realizar un examen similar para determinar que ningún componente tiene "LicenseInfo" como miembro principal de su ruta de acceso lógica y, por lo tanto, "LicenseInfo" no tiene subcomponentes.

Debido a la complejidad de este mecanismo en VSS, muchos escritores de solicitudes pueden resultarle útil para crear sus propias estructuras para almacenar información de componentes y conjuntos de copia de seguridad tanto para componentes agregados de forma explícita como implícita.

## <a name="properties-of-implicitly-included-components"></a>Propiedades de los componentes incluidos implícitamente

Durante las operaciones de restauración y copia de seguridad, las instancias de las interfaces [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) y [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) se usan para recuperar información acerca de los componentes y para establecer o cambiar las propiedades de los componentes. Sin embargo, solo los componentes incluidos explícitamente tendrán instancias de la interfaz **IVssComponent** o serán accesibles para la interfaz **IVssBackupComponents** .

Algunas propiedades son conjuntos de componentes en el ámbito. Entre estas propiedades se incluyen las siguientes:

-   Estado de copia de seguridad y restauración: <dl>

[**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)  
    [**IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)  
    [**IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)  
    [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)  
    </dl>
-   Opciones de copia de seguridad y restauración: <dl>

[**IVssBackupComponents:: SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions)  
    [**IVssComponent::GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)  
    [**IVssBackupComponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)  
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

Por lo tanto, se usa la instancia de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) del miembro que define un conjunto de componentes o se usa el nombre, el tipo y la ruta de acceso lógica del miembro que lo define con un método [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) para establecer o recuperar las propiedades de todos los miembros del conjunto de componentes.

Por esta razón, los conjuntos de componentes se tratan como unidades. Por ejemplo, una copia de seguridad de un conjunto de componentes solo se realiza correctamente si la copia de seguridad de todos los conjuntos de archivos de todos sus componentes se realiza correctamente.

En el ejemplo anterior, suponga que un archivo del componente "Jan" (con la ruta de acceso lógica "writerData \\ Set2") es un miembro del conjunto de componentes definido por "writerData". Si no se pudo realizar una copia de seguridad de uno de los archivos de "Jan", un solicitante usaría la información de "writerData" (su nombre "writerData", su ruta de acceso "" y su tipo de componente) como argumentos al establecer [**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) con **false** para indicar el error del conjunto de componentes.

Del mismo modo, el estado devuelto por [**IVssComponent:: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) para la instancia de "writerData" de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) se aplica no solo a "writerData" sino también a todos sus subcomponentes.

Además, si un escritor decidió cambiar el destino de restauración mediante [**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) de la instancia de "writerData" de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent), que cambiaría el destino de restauración de todos los conjuntos de archivos de todos los subcomponentes de "writerData".

Las siguientes propiedades no se aplican a todo el componente, sino a determinados archivos o conjuntos de archivos:

-   Asignaciones de ubicación alternativas: <dl>

[**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)  
    [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)  
    [**IVssComponent::GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)  
    </dl>
-   Archivos diferenciados: <dl>

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

[**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)  
    [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)  
    [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)  
    </dl>

Cuando un solicitante tiene acceso a estas características para un subcomponente mediante la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , usa la información de componente para el componente de definición del conjunto de componentes, pero la información del archivo o del conjunto de archivos para el subcomponente.

Del mismo modo, si la propiedad es accesible a través de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , se usa la instancia correspondiente al subcomponente que lo define, pero los argumentos del archivo o del conjunto de archivos se toman del subcomponente.

Por ejemplo, supongamos que el subcomponente "Jan" (con la ruta de acceso lógica "writerData \\ Set2") tenía un archivo establecido con una ruta de acceso "c: \\ Fred", una especificación de archivo de " \* . dat" y una marca recursiva de **true** puede tener que restaurarse en una ubicación alternativa.

Si este fuera el caso, un solicitante llamaría a [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping), usando la información de "writerData" (tipo de componente, un nombre de componente de "writeData" y una ruta de acceso lógica de "") junto con la información del conjunto de archivos "Jan" (ruta de acceso "c: \\ Fred", especificación de archivo " \* . 

Tenga en cuenta que, en este caso, la información del conjunto de archivos debe coincidir exactamente con la información de conjunto de archivos usada por [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) para agregar archivos a Jan.

Del mismo modo, si un escritor deseara agregar un destino dirigido a un archivo con una ruta de acceso "c: \\ Ethel" y el nombre "Lucy. dat" administrados por "ene" (con la ruta de acceso lógica "writerData \\ Set2"), usaría la instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente a "writerData", pero la información del archivo "Jan".

## <a name="implicitly-included-components-in-the-restore-set"></a>Componentes incluidos implícitamente en el conjunto de restauración

Los componentes que se incluyeron implícitamente en una copia de seguridad pueden incluirse explícitamente en una restauración si son seleccionables para la restauración. Como se indicó en [trabajar con la selección para restaurar y subcomponentes](working-with-selectability-for-restore-and-subcomponents.md), dichos componentes se agregan al documento de componentes de copia de seguridad mediante el método [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) .

Sin embargo, esto no crea una nueva instancia de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , ni tampoco es el componente accesible directamente a través de la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .

En su lugar, se debe tener acceso a un componente incluido explícitamente para la restauración, pero que se incluye implícitamente para la copia de seguridad, a través de una instancia de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que corresponde al componente que definió el conjunto de componentes del que era miembro tras la copia de seguridad.

Por ejemplo, para incluir explícitamente for restore "Set1", un subcomponente de Selectable para el componente de copia de seguridad "writerData", obtenería información sobre él llamando al método [**IVssComponent:: GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent) de la instancia de "writerData" de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

 

 



