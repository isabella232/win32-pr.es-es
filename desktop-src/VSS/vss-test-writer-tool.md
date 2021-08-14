---
description: Test Writer es una utilidad que puede usar para probar las aplicaciones solicitantes de VSS.
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: Herramienta VSS Test Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93f0b81bd5e27db9fdfb70ca52e6f43bbb1e853af87bc12e1d76f01d7966ef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344238"
---
# <a name="vss-test-writer-tool"></a>Herramienta VSS Test Writer

Test Writer es una utilidad que puede usar para probar las aplicaciones solicitantes de VSS. Este sistema de escritura se puede configurar para realizar casi todas las acciones que un escritor de VSS puede realizar. Además, el escritor de pruebas realiza comprobaciones exhaustivas para asegurarse de que el solicitante ha abordado correctamente estas acciones de escritura.

Cada instancia del sistema de escritura se inicializa con un archivo de configuración XML que describe exactamente los componentes sobre los que el escritor va a informar y cómo se comporta el escritor. El sistema de escritura se puede configurar para informar sobre varios tipos de escenarios, incluidos escenarios más complicados mediante las interfaces incremental y diferencial. El escritor realizará comprobaciones en varios puntos durante el proceso para asegurarse de que el solicitante se comporta de forma adecuada. Una vez completada la restauración, el sistema de escritura comprobará que todos los archivos necesarios se han restaurado sin daños. El sistema de escritura también se puede configurar para realizar otras operaciones, como eventos específicos con errores.

> [!Note]  
> Esta herramienta se incluye en el Kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores. Puede descargar el SDK Windows desde [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

En la Windows DEL SDK, la herramienta VssSampleProvider se puede encontrar en (para archivos de `%Program Files(x86)%\Windows Kits\8.1\bin\x64` 64 Windows) y `%Program Files(x86)%\Windows Kits\8.1\bin\x86` .

## <a name="running-the-test-writer-tool"></a>Ejecución de la herramienta de escritura de pruebas

Para iniciar el escritor de pruebas, escriba lo siguiente en el símbolo del sistema:

**vswriter.exe** *config-file*

donde *config-file* es la ruta de acceso a un archivo de configuración que especifica el comportamiento de este escritor.

Para detener el escritor de pruebas, presione CTRL+C.

Se pueden ejecutar varias instancias del escritor de pruebas al mismo tiempo. Sin embargo, cada instancia del escritor informará del mismo identificador de clase de escritor (aunque sea un identificador de instancia de escritor diferente), por lo que las rutas de acceso lógicas y los nombres de componente deben ser únicos en todas las instancias que se ejecutan simultáneamente del escritor.

Para asegurarse de que el escritor puede comprobar correctamente que el solicitante ha respetado las especificaciones de archivo de exclusión, todos los archivos de los que se ha hecho una copia de seguridad deben eliminarse del volumen original antes de intentar restaurarlos. Se recomienda almacenar una plantilla de cada escenario de escritor, para que el escenario se pueda volver a crear fácilmente.

## <a name="using-a-configuration-file"></a>Uso de un archivo de configuración

El siguiente archivo de configuración de ejemplo, vswriterconfig.xml, se puede encontrar en en plataformas \_ `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` x86 y `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` en plataformas x64.

``` syntax
<TestWriter usage="USER_DATA">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED"
                   writerRestore="always"
                   rebootRequired="no" />

    <ExcludeFile path="c:\writerData\notTheseFiles" 
                 filespec="excludeThisFile.txt" 
                 recursive="no"/>

    <Component componentType="filegroup"
               componentName="TestFiles">
        <ComponentFile path="c:\writerData\myFilesHere" 
                       filespec="*"
                       recursive="no" />
    </Component>

</TestWriter>
```

El elemento raíz de este archivo de configuración se denomina TestWriter. Todos los demás elementos se organizan en el elemento TestWriter.

Uno de los atributos asociados a TestWriter es el atributo de uso. Este atributo especifica el tipo de uso notificado a través [**de IVssExgvWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity). Uno de los valores posibles para este atributo es USER \_ DATA.

El primer elemento secundario del elemento raíz siempre debe ser un elemento RestoreMethod. Este elemento especifica lo siguiente:

-   Método de restauración (en este caso, RESTORE \_ IF \_ CAN BE \_ \_ REPLACED)
-   Si el escritor requiere eventos de restauración (en este caso, siempre)
-   Si se requiere un reinicio después de restaurar el sistema de escritura (en este caso, no)

Opcionalmente, este elemento puede especificar una asignación de ubicación alternativa. (En este caso, no se especifica ninguna ubicación alternativa).

El segundo elemento secundario es un elemento ExcludeFile. Este elemento hace que el escritor excluya un archivo o un conjunto de archivos de la copia de seguridad.

El tercer elemento secundario es un elemento Component. Este elemento hace que el escritor agregue un componente a sus metadatos. Un elemento Component contiene atributos para describir el componente y los elementos secundarios para describir el contenido del componente, como los siguientes:

-   componentType para indicar si se trata de un grupo de archivos o una base de datos
-   logicalPath para la ruta de acceso lógica del componente
-   componentName para el nombre del componente
-   seleccionable para indicar el estado seleccionable para copia de seguridad

El elemento Component también tiene un elemento secundario denominado ComponentFile para agregar una especificación de archivo a este componente. (Un elemento Component puede tener un número arbitrario de elementos ComponentFile que se pueden especificar para cada componente). Este elemento ComponentFile tiene los siguientes atributos:

-   path="c: \\ writerData \\ myFilesHere"
-   filespec=" \* "
-   recursive="no"

Aunque el escritor de pruebas comprueba el comportamiento del solicitante, no comprueba que el archivo de configuración mantenga siempre la semántica documentada para un escritor. Hay muchas operaciones que un escritor bien comportado no debe realizar (por ejemplo, notificar el mismo archivo en varios componentes) y es el autor del archivo de configuración XML el que debe mantener esta semántica.

## <a name="configuring-writer-attributes"></a>Configuración de atributos de escritor

El elemento raíz TestWriter contiene atributos que determinan varios comportamientos del escritor. Algunos de los comportamientos que se pueden modificar son los siguientes:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="verbosity"></span><span id="VERBOSITY"></span>nivel de detalle<br/></td>
<td>El escritor imprime el estado en la consola a medida que recibe eventos y los procesa. El nivel de detalle mostrado se especifica mediante el atributo verbosity. Hay tres niveles de detalle entre los que elegir:<br/> <dl> <dt><span id="low"></span><span id="LOW"></span>Bajo</dt> <dd> Solo se imprimirán los errores en el sistema de escritura o el comportamiento incorrecto del solicitante.<br/> </dd> <dt><span id="medium"></span><span id="MEDIUM"></span>Medio</dt> <dd> Todo en el nivel de detalle bajo se imprime además de información de estado adicional, como cuando se reciben eventos. Es el nivel predeterminado.<br/> </dd> <dt><span id="high"></span><span id="HIGH"></span>Alto</dt> <dd> Se notifica información de estado detallada sobre el funcionamiento del sistema de escritura.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>deleteFiles<br/></td>
<td>Para realizar una comprobación adicional, establezca este atributo en sí para que el escritor elimine todos sus archivos inmediatamente después de crear la &quot; &quot; instantánea de volumen. A continuación, el solicitante debe copiar los archivos de la instantánea, ya que ya no existen en el volumen original. <br/>
<blockquote>
[!Note]<br />
En el caso de los escritores de escritores de escritores, los archivos se eliminan de la ubicación original después de la cópiela, pero antes de que se cree la instantánea. Una vez creada la instantánea, los archivos se eliminan del directorio de la instantánea.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletePartialFiles<br/></td>
<td>Para eliminar archivos parciales, establezca este atributo en &quot; &quot; sí.<br/></td>
</tr>
<tr class="even">
<td><span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deleteDifferencedFiles<br/></td>
<td>Para eliminar archivos diferenciados, establezca este atributo en &quot; &quot; sí.<br/></td>
</tr>
<tr class="odd">
<td><span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkIncludes<br/></td>
<td>Establezca este atributo en sí para que el escritor compruebe que todos los archivos de los que se ha realizado una copia de seguridad se han restaurado en una ubicación adecuada y que el archivo no se ha &quot; &quot; dañado. Los archivos parciales y los archivos diferenciados también se controlan correctamente.<br/></td>
</tr>
<tr class="even">
<td><span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>checkExcludes<br/></td>
<td>Establezca este atributo en sí para que el escritor compruebe que los archivos que coinciden con una especificación de archivo de la lista de exclusión &quot; &quot; no se restauran. Para que funcione correctamente, los directorios de restauración deben vaciarse antes de la restauración.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="specifying-alternate-location-mappings"></a>Especificar asignaciones de ubicación alternativas

Una asignación de ubicación alternativa especifica una ubicación a la que restaurar si el método de restauración es VSS WRE RESTORE TO ALTERNATE LOCATION o si se produce un error en la restauración \_ \_ normal de un \_ \_ \_ componente. Un escritor puede notificar sus asignaciones de ubicación alternativas al solicitante mediante el método [**IVssExgvWriterMetadata::GetAlternateLocationMapping.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) Puede agregar asignaciones de ubicación alternativas al archivo de configuración del escritor de pruebas agregando subelementos AlternateLocationMapping al elemento RestoreMethod.

El siguiente elemento RestoreMethod contiene un subelemento AlternateLocationMapping.

``` syntax
<RestoreMethod method="RESTORE_IF_CAN_REPLACE"
              writerRestore="always"
              rebootRequired="no">
    <AlternateLocationMapping path="c:\files"
                              filespec="*.txt"
                              recursive="no"
                              alternatePath="c:\altfiles"/>
</RestoreMethod>
```

En este ejemplo se especifica que el solicitante debe intentar primero restaurar todos los archivos que coinciden con c:.txt al directorio \\ \\ \* de archivos \\ c:. Si no se puede reemplazar uno de estos archivos, el solicitante debe restaurar todos los archivos en el directorio c: \\ altfiles en su lugar. El solicitante debe guardar esta asignación de ubicación alternativa mediante el método [**IVssBackupComponents::AddAlternativeLocationMapping.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) Si el escritor de pruebas está configurado para comprobar si se han restaurado los archivos, también comprobará si el solicitante ha llamado a **AddAlternativeLocationMapping**.

## <a name="specifying-files-to-be-excluded"></a>Especificar los archivos que se excluirán

Cada escritor puede especificar una lista de especificaciones de archivo que especifican los archivos para que el solicitante los excluya de la copia de seguridad. Puede agregar estas especificaciones de archivo al archivo de configuración del escritor de pruebas agregando subelementos ExcludeFile al elemento raíz TestWriter.

Este es un ejemplo de un subelemento ExcludeFile que excluye todos los archivos del directorio C: \\ files que coinciden con C: temp \\ \* \* .

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a>Copia de seguridad de escritores de escritores de escritores

Muchos escritores actúan como "escritores de escritores de escritores". Un escritor de escritores de escritores crea archivos intermedios, o "archivos de almacenamiento", basados en un conjunto original de archivos, y coloca los archivos en una ubicación alternativa en el momento de la copia de seguridad. El escritor usa el [**método IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) para notificar al solicitante que debe hacer una copia de seguridad de estos archivos desde la ubicación alternativa. Sin embargo, estos archivos deben restaurarse en la ubicación activa de los archivos originales. El escritor de pruebas se puede configurar para que actúe como escritor de escritores de escritura para una especificación de archivo determinada.

El siguiente elemento ComponentFile contiene un atributo alternatePath:

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

En este ejemplo se configura el escritor de pruebas para copiar todos los archivos que coinciden con c:.txt en el directorio c: files directory inmediatamente antes de crear la instantánea \\ \\ \* \\ de \\ volumen. El solicitante debe hacer una copia de seguridad de los archivos desde el directorio c: \\ \\ files directory. Si el escritor de pruebas está configurado para eliminar archivos, elimina los archivos originales antes de crear la instantánea, por lo que no aparecen en el directorio de archivos c: del volumen de \\ instantáneas. En este caso, los archivos de c: files se eliminan después de crear la instantánea, por lo que se debe hacer una copia de seguridad de ellos desde el directorio c: files del volumen de \\ \\ \\ \\ instantáneas.

## <a name="reporting-component-dependencies"></a>Dependencias de componentes de informes

Los escritores pueden especificar una dependencia entre un componente local y un componente que existe en otro escritor. Estas dependencias se notifican al solicitante mediante [**IVssWMComponent::GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). Test Writer se puede configurar para notificar estas dependencias agregando uno o varios subelementos Dependency al elemento Component.

El siguiente elemento Component contiene un subelemento Dependency:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
         <Dependency writerId="<GUID of target writer>"
                     logicalPath="ComponentPath"
                     componentName="Writer2Component" />
    </Component>
```

La dependencia se especifica como atributos del elemento Dependency. writerId es el identificador de clase del escritor que contiene el destino de la dependencia, logicalPath es la ruta de acceso lógica al componente en ese escritor y componentName es el nombre del componente. En este caso, si el solicitante hace una copia de seguridad de "WriterComponent" en el sistema de escritura actual, también debe hacer una copia de seguridad del componente "ComponentPath Writer2Component" en el escritor \\ de destino.

> [!Note]  
> Test Writer no realiza ninguna comprobación para asegurarse de que se respetan las dependencias.

 

## <a name="failing-events"></a>Eventos con errores

El escritor de pruebas se puede configurar para producir un error en cualquiera de los eventos normales que recibe un escritor. Estos eventos son los siguientes:



| Evento                                                                                                                                    | Descripción                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>Identificar<br/>                                     | Se recibe como respuesta a una [**llamada a IVssBackupComponents::GatherWriterMetadata.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) Un error aquí hará que no se notimente el escritor.<br/>                                                                 |
| <span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup<br/>     | Se recibe como respuesta al solicitante que llama a [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).<br/>                                                                                                                 |
| <span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>PrepareForSnapsot<br/> | Se recibe cuando el solicitante llama a [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), pero antes de crear la instantánea.<br/>                                                                                              |
| <span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>Congelar<br/>                                             | Se recibe inmediatamente después [*de PrepareForSnapshot,*](vssgloss-p.md)pero todavía antes de que se cree la instantánea.<br/>                                                                                                      |
| <span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>Deshielo<br/>                                                     | Se recibe una vez finalizada la creación de la instantánea.<br/>                                                                                                                                                                                                     |
| <span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>PostSnapshot<br/>                     | Se recibe una vez completado Thaw, pero antes de [**que finalice IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)<br/>                                                                                                                   |
| <span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>Aborta<br/>                                                 | Se recibe si transcurre demasiado tiempo entre [*Freeze*](vssgloss-f.md) y [*Thaw*](vssgloss-t.md) o si el solicitante llama a [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).<br/> |
| <span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete<br/>             | Se recibe cuando se cierra el solicitante. Los errores aquí nunca se notifican.<br/>                                                                                                                                                                                 |
| <span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>PreRestore<br/>                             | Se recibe cuando el solicitante llama [**a IVssBackupComponents::P reStore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).<br/>                                                                                                                                           |
| <span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>PostRestore<br/>                         | Se recibe cuando el solicitante llama [**a IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).<br/>                                                                                                                                         |



 

Estos errores se configuran agregando uno o varios subelementos FailEvent al elemento raíz TestWriter. Hay dos clases de errores que se pueden establecer: reintentar y no reintentar. Los errores reintentables son errores que pueden desaparecer si se vuelve a intentar todo el proceso de copia de seguridad, mientras que es poco probable que los errores que no se pueden reintentar desaparezcan. El tipo de error para el evento se elige en función del atributo que se puede reintentar.

Este es un ejemplo de un error básico que no se puede reintentar:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="no" />
```

Este ejemplo provocará un error en el escritor durante el [*evento Freeze.*](vssgloss-f.md) [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) informa del error del sistema de escritura como VSS \_ E \_ WRITERERROR \_ NONRETRYABLE.

Este es un ejemplo de un error básico que se puede reintentar:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="yes"
               numFailures="2"/>
```

Este ejemplo hará que el sistema de escritura no se pueda escribir las dos primeras veces que recibe un [*evento Freeze.*](vssgloss-f.md) Después de las dos primeras veces, el escritor siempre se realizará correctamente. El error del escritor notificado [**a través de GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) será un código de error que se puede reintentar aleatoriamente.

## <a name="declaring-supported-backup-types"></a>Declarar tipos de copia de seguridad admitidos

Los escritores comunican qué tipos de copia de seguridad se admiten a través de la [**llamada de IVssExgvWriterMetadata::GetBackupSchema del**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)solicitante. El elemento raíz TestWriter contiene atributos para cada tipo de copia de seguridad para indicar la compatibilidad. Estos atributos son supportsCopy, supportsDifferential, supportsIncremental y supportsLog. Para indicar la compatibilidad con un tipo de copia de seguridad determinado, establezca el atributo correspondiente en "sí".

Si el solicitante establece el tipo de copia de seguridad en un tipo de copia de seguridad que no es compatible con el escritor, el escritor tendrá en cuenta este hecho durante [**PrepareForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)pero de lo contrario funcionará correctamente.

## <a name="indicating-the-file-backup-type"></a>Indica el tipo de copia de seguridad de archivos

El [**método IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) devuelve una máscara de bits al solicitante que indica cómo se debe hacer una copia de seguridad de un archivo. Esto indicará si un archivo es necesario o no durante determinados tipos de copia de seguridad, así como si se requiere una instantánea durante determinados tipos de copia de seguridad. Los tipos de copia de seguridad de esta máscara de bits se explican con mayor longitud en el documento Rol del solicitante en Copia de [seguridad de almacenes complejos](requestor-role-in-backing-up-complex-stores.md).

En Test Writer, los elementos de esta máscara de bits se especifican estableciendo atributos en cada elemento ComponentFile. Los atributos fullBackupRequired, diffBackupRequired, incBackupRequired y logBackupRequired especifican cuándo es necesario realizar una copia de seguridad de un archivo. Los atributos fullSnapshotRequired, diffSnapshotRequired, incSnapshotRequired y logSnapshotRequired especifican cuándo se debe hacer una copia de seguridad de un archivo desde una instantánea de un volumen (y nunca desde el volumen original). El valor predeterminado de todos estos valores es "yes", lo que indica que siempre se debe hacer una copia de seguridad de un archivo y se debe hacer una copia de seguridad desde una instantánea de un volumen.

## <a name="adding-partial-files"></a>Agregar archivos parciales

Durante el procesamiento de [**DoSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)un escritor tiene la oportunidad de agregar archivos parciales a cada componente. Estos archivos parciales se notifican [**mediante IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). Test Writer se puede configurar para agregar archivos parciales especificando subelementos PartialFile en un elemento Component.

Este es un ejemplo de un elemento Component que tiene dos subelementos PartialFile:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <PartialFile path="c:\files"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
        <PartialFile path="c:\files2"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
    </Component>
```

Solo se deben especificar de esta manera los archivos parciales que coincidan parcialmente con un ComponentFile existente (como en el primer archivo parcial del ejemplo) o los nuevos archivos parciales que se encuentran en el mismo volumen que un ComponentFile existente (como en el segundo archivo parcial). Para este componente, el solicitante debe hacer una copia de seguridad completa de todos los archivos que coincidan con c: \\.txt \\ \* excepto partial.txt. A continuación, el solicitante debe hacer una copia de seguridad de los intervalos especificados (donde un intervalo es un desplazamiento seguido de una longitud) para los archivos c: filespartial.txt y \\ \\ c: \\ files2 \\partial.txt.

Si el sistema de escritura está configurado para comprobar las restauraciones de archivos, solo se comprobarán los intervalos de copia de seguridad del archivo parcial en el momento de la restauración. Las modificaciones en otras partes del archivo pasarán desapercibidas. Si se establece el atributo deletePartialFiles del elemento raíz TestWriter, los archivos parciales se eliminan del volumen original inmediatamente después de crear la instantánea.

## <a name="adding-differenced-files"></a>Agregar archivos diferenciados

Durante el procesamiento de [**DoSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)un escritor puede agregar archivos diferenciados a cada componente. Estos archivos diferenciados se notifican [**mediante IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). Test Writer se puede configurar para agregar archivos diferenciados especificando subelementos DifferencedFile en un elemento Component.

Este es un ejemplo de un elemento Component que tiene dos subelementos DifferencedFile:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <DifferencedFile path="c:\files"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
        <DifferencedFile path="c:\files2"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
    </Component>
```

A diferencia de los archivos parciales, los archivos diferenciados nunca deben coincidir parcialmente con una especificación ComponentFile. La especificación de archivo de un elemento DifferencedFile debe coincidir exactamente con un ComponentFile (como en el primer archivo diferenciado del ejemplo) o no debe coincidir en absoluto, pero debe estar en un volumen al que se hace referencia en un ComponentFile (como en el segundo archivo diferenciado). Los valores de fecha y hora deben ser relativos a la zona horaria local, pero se convertirán a GMT antes de que se notifican al solicitante. En el ejemplo, solo se hará una copia de seguridad de los archivos que coinciden con c:.txt o c: files2.txt que se han modificado desde \\ \\ \* \\ el \\ \* 22/1/2003:12:44:17.

Si el escritor de pruebas está configurado para comprobar las restauraciones de archivos, solo se comprobará la restauración de los archivos modificados. Si se establece el atributo deleteDifferencedFiles del elemento raíz TestWriter, los archivos diferenciados se eliminan del volumen original inmediatamente después de crear la instantánea.

## <a name="new-targets"></a>Nuevos destinos

Determinados escritores permiten al solicitante informarles de que se ha elegido una nueva ubicación en la que restaurar determinados archivos. El sistema de escritura indica que admite este modo como parte de la máscara de bits devuelta por [**IVssExgvWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). De forma predeterminada, Test Writer siempre admite nuevos destinos. Esta compatibilidad se puede deshabilitar estableciendo el atributo supportsNewTarget del elemento raíz TestWriter en "no".

Si un sistema de escritura admite nuevos destinos, el solicitante puede informar al escritor de nuevos destinos mediante una llamada a [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget). A continuación, el escritor comprobará la nueva ubicación de destino para comprobar la restauración en lugar de la ubicación original.

## <a name="more-information"></a>Más información

Test Writer admite más opciones de configuración que no se describen aquí. El esquema completo de todas las funcionalidades de configuración del sistema de escritura de pruebas se especifica en swriter.xml en (para el Windows de 64 bits) y (para las Windows `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` de 32 bits). Este archivo contiene un esquema XML que describe por completo todos los elementos y atributos que forma un archivo de configuración. Cada elemento y cada atributo de este archivo se comentan con una descripción que documenta el uso de ese elemento o atributo.

 

 




