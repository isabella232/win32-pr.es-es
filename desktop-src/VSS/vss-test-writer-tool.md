---
description: El escritor de pruebas es una utilidad que puede usar para probar las aplicaciones de solicitante de VSS.
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: Herramienta de escritura de prueba de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ffdbb513697a701866be5ceeb40168e8c28368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696457"
---
# <a name="vss-test-writer-tool"></a>Herramienta de escritura de prueba de VSS

El escritor de pruebas es una utilidad que puede usar para probar las aplicaciones de solicitante de VSS. Este escritor puede configurarse para realizar casi todas las acciones que puede realizar un VSS Writer. Además, el escritor de pruebas realiza comprobaciones exhaustivas para asegurarse de que el solicitante ha solucionado correctamente estas acciones del escritor.

Cada instancia del escritor se inicializa con un archivo de configuración XML que describe exactamente en qué componentes informará el escritor y cómo se comporta el escritor. El escritor puede configurarse para informar sobre diversos tipos de escenarios, incluidos escenarios más complicados con las interfaces incrementales y diferenciales. El escritor realizará comprobaciones en varios puntos durante el proceso para asegurarse de que el solicitante se comporta de la manera adecuada. Una vez finalizada la restauración, el escritor comprobará que todos los archivos necesarios se han restaurado sin daños. El escritor también puede configurarse para realizar otras operaciones, como errores de eventos específicos.

> [!Note]  
> Esta herramienta se incluye en el kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores. Puede descargar la Windows SDK desde [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

En la instalación de Windows SDK, la herramienta VssSampleProvider se puede encontrar en `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para Windows de 64 bits) y `%Program Files(x86)%\Windows Kits\8.1\bin\x86` .

## <a name="running-the-test-writer-tool"></a>Ejecutar la herramienta de escritura de prueba

Para iniciar el escritor de pruebas, escriba lo siguiente en el símbolo del sistema:

**vswriter.exe** *config-file*

donde *config-file* es la ruta de acceso a un archivo de configuración que especifica el comportamiento de este escritor.

Para detener el escritor de pruebas, presione CTRL + C.

Se pueden ejecutar varias instancias del escritor de pruebas al mismo tiempo. Sin embargo, cada instancia del escritor informará del mismo ID. de clase del escritor (aunque es un identificador de instancia de escritor diferente), por lo que las rutas de acceso lógicas y los nombres de componente deben ser únicos en todas las instancias en ejecución simultáneas del escritor.

Para asegurarse de que el escritor puede comprobar correctamente que el solicitante ha respetado las especificaciones de exclusión de archivos, todos los archivos de los que se realizó una copia de seguridad deberían eliminarse del volumen original antes de intentar restaurarlos. Se recomienda que se almacene una plantilla de cada escenario del escritor, por lo que el escenario se puede volver a crear fácilmente.

## <a name="using-a-configuration-file"></a>Uso de un archivo de configuración

El siguiente archivo de configuración de ejemplo, vswriter \_config.xml, se puede encontrar en `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` en plataformas x86 y `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` en plataformas x64.

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

El elemento raíz de este archivo de configuración se denomina TestWriter. Todos los demás elementos se organizan bajo el elemento TestWriter.

Uno de los atributos asociados a TestWriter es el atributo Usage. Este atributo especifica el tipo de uso indicado a través de [**IVssExamineWriterMetadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity). Uno de los valores posibles para este atributo son los \_ datos de usuario.

El primer elemento secundario del elemento raíz siempre debe ser un elemento RestoreMethod. Este elemento especifica lo siguiente:

-   El método restore (en este caso, RESTOre \_ If \_ \_ se puede \_ reemplazar)
-   Si el escritor requiere eventos de restauración (en este caso, siempre)
-   Si es necesario un reinicio después de restaurar el escritor (en este caso, no)

Este elemento puede especificar opcionalmente una asignación de ubicación alternativa. (En este caso, no se especifica ninguna ubicación alternativa).

El segundo elemento secundario es un elemento ExcludeFile. Este elemento hace que el escritor excluya un archivo o un conjunto de archivos de la copia de seguridad.

El tercer elemento secundario es un elemento de componente. Este elemento hace que el escritor agregue un componente a sus metadatos. Un elemento Component contiene atributos para describir el componente y los elementos secundarios para describir el contenido del componente, como el siguiente:

-   componentType para indicar si se trata de un grupo de archivos o una base de datos
-   logicalPath para la ruta de acceso lógica del componente
-   componentName para el nombre del componente
-   Selectable para indicar el estado Selectable-for-Backup

El elemento componente también tiene un elemento secundario denominado ComponentFile para agregar una especificación de archivo a este componente. (Un elemento de componente puede tener un número arbitrario de elementos ComponentFile que se pueden especificar para cada componente). Este elemento ComponentFile tiene los siguientes atributos:

-   Ruta de acceso = "c: \\ writerData \\ myFilesHere"
-   filespec = " \* "
-   Recursive = "no"

Aunque el escritor de pruebas comprueba el comportamiento del solicitante, no comprueba que el archivo de configuración Mantenga siempre la semántica documentada para un escritor. Hay muchas operaciones que un escritor con buen comportamiento no debe hacer (por ejemplo, notificar el mismo archivo en varios componentes) y depende del autor del archivo de configuración XML para mantener estas semánticas.

## <a name="configuring-writer-attributes"></a>Configuración de atributos del escritor

El elemento raíz TestWriter contiene atributos que determinan distintos comportamientos del escritor. Algunos de los comportamientos que se pueden modificar son los siguientes:



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
<td><span id="verbosity"></span><span id="VERBOSITY"></span>detalle<br/></td>
<td>El escritor imprime el estado en la consola a medida que recibe eventos y los procesa. El nivel de detalle mostrado se especifica mediante el atributo de detalle. Hay tres niveles de detalle entre los que elegir:<br/> <dl> <dt><span id="low"></span><span id="LOW"></span>habilita</dt> <dd> Solo se imprimirán los errores del escritor o el comportamiento incorrecto del solicitante.<br/> </dd> <dt><span id="medium"></span><span id="MEDIUM"></span>medio</dt> <dd> Todo lo que se encuentra en el nivel de detalle bajo se imprime además de información de estado adicional, como cuando se reciben los eventos. Es el nivel predeterminado.<br/> </dd> <dt><span id="high"></span><span id="HIGH"></span>calidad</dt> <dd> Se indica información de estado detallada sobre el funcionamiento del escritor.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>deleteFiles<br/></td>
<td>Para realizar una comprobación adicional, establezca este atributo en &quot; sí &quot; para que el escritor elimine todos sus archivos inmediatamente después de crear la instantánea de volumen. A continuación, el solicitante debe copiar los archivos de la instantánea, ya que ya no existen en el volumen original. <br/>
<blockquote>
[!Note]<br />
En el caso de los escritores de asignación, los archivos se eliminan de la ubicación original después de la asignación, pero antes de que se cree la instantánea. Una vez creada la instantánea, los archivos se eliminan del directorio de la.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletePartialFiles<br/></td>
<td>Para eliminar archivos parciales, establezca este atributo en &quot; sí &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deleteDifferencedFiles<br/></td>
<td>Para eliminar archivos diferenciados, establezca este atributo en &quot; sí &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkIncludes<br/></td>
<td>Establezca este atributo en &quot; sí &quot; para que el escritor Compruebe que todos los archivos de los que se ha realizado una copia de seguridad se han restaurado en una ubicación adecuada y que el archivo no está dañado. Los archivos parciales y los archivos diferenciados también se administran correctamente.<br/></td>
</tr>
<tr class="even">
<td><span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>checkExcludes<br/></td>
<td>Establezca este atributo en &quot; sí &quot; para que el escritor Compruebe que los archivos que coinciden con una especificación de archivo en la lista de exclusión no se restauran. Para que funcione correctamente, los directorios de restauración se deben vaciar antes de la restauración.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="specifying-alternate-location-mappings"></a>Especificar asignaciones de ubicación alternativas

Una asignación de ubicación alternativa especifica una ubicación en la que restaurar si el método de restauración es VSS \_ WRE \_ restore \_ en una \_ \_ ubicación alternativa o si se produce un error en la restauración normal de un componente. Un escritor puede informar de las asignaciones de ubicación alternativas al solicitante mediante el método [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) . Puede Agregar asignaciones de ubicación alternativas al archivo de configuración del escritor de pruebas agregando subelementos AlternateLocationMapping al elemento RestoreMethod.

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

Este ejemplo especifica que el solicitante debe intentar primero restaurar todos los archivos que coincidan con c: \\ files \\ \* . txt en el directorio c: \\ files. Si uno de estos archivos no se puede reemplazar, el solicitante debe restaurar todos los archivos al directorio c: \\ altfiles en su lugar. El solicitante debe guardar esta asignación de ubicación alternativa mediante el método [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) . Si el escritor de pruebas está configurado para comprobar si los archivos se han restaurado, también comprobará si el solicitante ha llamado a **AddAlternativeLocationMapping**.

## <a name="specifying-files-to-be-excluded"></a>Especificar los archivos que se van a excluir

Cada escritor puede especificar una lista de especificaciones de archivo que especifican los archivos que el solicitante debe excluir de la copia de seguridad. Puede agregar estas especificaciones de archivo al archivo de configuración del escritor de pruebas agregando subelementos ExcludeFile al elemento raíz TestWriter.

Este es un ejemplo de un subelemento ExcludeFile que excluye todos los archivos del directorio C: \\ files que coinciden con C: \\ temp \* . \* .

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a>Realizar copias de seguridad de los escritores de

Muchos escritores actúan como "redactores". Un redactor de asignaciones crea archivos intermedios, o "genera archivos", basándose en un conjunto original de archivos, y coloca los archivos de asignación en una ubicación alternativa en el momento de la copia de seguridad. El escritor usa el método [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) para notificar al solicitante que debe hacer copia de seguridad de estos archivos desde la ubicación alternativa. Sin embargo, estos archivos se deben restaurar en la ubicación activa de los archivos originales. El escritor de pruebas se puede configurar para que actúe como un escritor de la forma de una especificación de archivo determinada.

El siguiente elemento ComponentFile contiene un atributo alternatePath:

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

En este ejemplo se configura el escritor de pruebas para copiar todos los archivos que coincidan con c: \\ files \\ \* . txt en el directorio c: \\ files alsign \\ inmediatamente antes de que se cree la instantánea de volumen. El solicitante debe hacer una copia de seguridad de los archivos del \\ directorio c: files alliberar \\ . Si el escritor de pruebas está configurado para eliminar archivos, elimina los archivos originales antes de crear la instantánea, por lo que no aparecen en el directorio c: \\ files del volumen de instantáneas. En este caso, los archivos de c: \\ los archivos \\ se eliminan después de crear la instantánea, por lo que se les debe hacer una copia de seguridad desde el directorio c: \\ files \\ en el volumen de instantáneas.

## <a name="reporting-component-dependencies"></a>Dependencias de componentes de informes

Los escritores pueden especificar una dependencia entre un componente local y un componente que existe en otro escritor. Estas dependencias se envían al solicitante mediante [**IVssWMComponent:: GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). El escritor de pruebas puede configurarse para notificar estas dependencias mediante la adición de uno o varios subelementos de dependencia al elemento de componente.

El siguiente elemento de componente contiene un subelemento de dependencia:

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

La dependencia se especifica como atributos del elemento de dependencia. writerId es el identificador de clase del escritor que contiene el destino de la dependencia, logicalPath es la ruta de acceso lógica al componente en ese escritor y componentName es el nombre del componente. En este caso, si el solicitante realiza una copia de seguridad de "WriterComponent" en el escritor actual, también debe hacer una copia de seguridad del componente "ComponentPath \\ Writer2Component" en el escritor de destino.

> [!Note]  
> El escritor de pruebas no realiza ninguna comprobación para asegurarse de que se respetan las dependencias.

 

## <a name="failing-events"></a>Eventos con error

El escritor de pruebas se puede configurar para que se produzca un error en cualquiera de los eventos normales que recibe un escritor. Estos eventos son los siguientes:



| Evento                                                                                                                                    | Descripción                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>Identificar<br/>                                     | Se recibe como respuesta a una llamada a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) . Un error aquí hará que no se notifique al escritor.<br/>                                                                 |
| <span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup<br/>     | Se recibe como respuesta al solicitante que llama a [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).<br/>                                                                                                                 |
| <span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>PrepareForSnapsot<br/> | Se recibe cuando el solicitante llama a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), pero antes de crear la instantánea.<br/>                                                                                              |
| <span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>Inmovilice<br/>                                             | Se recibe inmediatamente después de [*PrepareForSnapshot*](vssgloss-p.md), pero aún antes de que se cree la instantánea.<br/>                                                                                                      |
| <span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>Moviliza<br/>                                                     | Se recibe una vez finalizada la creación de la instantánea.<br/>                                                                                                                                                                                                     |
| <span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>Instantánea<br/>                     | Recibido después de que se complete la reanudación, pero antes de que se complete [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) .<br/>                                                                                                                   |
| <span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>Aborta<br/>                                                 | Se recibe si transcurre demasiado tiempo entre [*Freeze*](vssgloss-f.md) e [*reanudación*](vssgloss-t.md) o si el solicitante llama a [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).<br/> |
| <span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete<br/>             | Se recibe cuando se cierra el solicitante. Los errores aquí nunca se inscribirán.<br/>                                                                                                                                                                                 |
| <span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>Prerestauración<br/>                             | Se recibe cuando el solicitante llama a [**IVssBackupComponents::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)volver a restaurar.<br/>                                                                                                                                           |
| <span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>Postrestore<br/>                         | Se recibe cuando el solicitante llama a [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).<br/>                                                                                                                                         |



 

Estos errores se configuran agregando uno o más subelementos FailEvent al elemento raíz TestWriter. Hay dos clases de errores que se pueden establecer: reintentos y no reintentables. Los errores con posibilidad de reintento son errores que pueden desaparecer si se vuelve a intentar todo el proceso de copia de seguridad, aunque es improbable que los errores no reintentables desaparezcan. El tipo de error para el evento se elige en función del atributo de reintento.

A continuación se muestra un ejemplo de un error básico no reintentable:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="no" />
```

En este ejemplo se producirá un error en el escritor durante el evento [*Freeze*](vssgloss-f.md) . [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) informará de que el error del escritor es de VSS \_ E \_ WRITERERROR no \_ reintentable.

A continuación se muestra un ejemplo de un error de reintento básico:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="yes"
               numFailures="2"/>
```

En este ejemplo se producirá un error en el escritor las dos primeras veces que recibe un evento [*Freeze*](vssgloss-f.md) . Después de las dos primeras veces, el escritor siempre se realizará correctamente. El error del escritor informado a través de [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) será un código de error de reintento aleatorio.

## <a name="declaring-supported-backup-types"></a>Declarar tipos de copia de seguridad admitidos

Los escritores comunican qué tipos de copia de seguridad se admiten a través de la llamada a [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)del solicitante. El elemento raíz TestWriter contiene atributos para cada tipo de copia de seguridad para indicar la compatibilidad. Estos atributos son supportsCopy, supportsDifferential, supportsIncremental y supportsLog. Para indicar la compatibilidad con un tipo de copia de seguridad determinado, establezca el atributo correspondiente en "sí".

Si el solicitante establece el tipo de copia de seguridad en un tipo de copia de seguridad que no es compatible con el escritor, el escritor notará este hecho durante [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), pero de otro modo funcionará correctamente.

## <a name="indicating-the-file-backup-type"></a>Que indica el tipo de copia de seguridad de archivos

El método [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) devuelve una máscara de archivos al solicitante que indica cómo se debe realizar la copia de seguridad de un archivo. Esto indicará si un archivo es necesario o no durante determinados tipos de copia de seguridad y si se requiere una instantánea durante determinados tipos de copia de seguridad. Los tipos de copia de seguridad de esta máscara de caracteres se explican con mayor longitud en el [rol solicitante de documentos en la copia de seguridad de almacenes complejos](requestor-role-in-backing-up-complex-stores.md).

En el escritor de pruebas, los elementos de esta máscara de máscara se especifican mediante el establecimiento de atributos en cada elemento ComponentFile. Los atributos fullBackupRequired, diffBackupRequired, incBackupRequired y logBackupRequired especifican Cuándo es necesario hacer una copia de seguridad de un archivo. Los atributos fullSnapshotRequired, diffSnapshotRequired, incSnapshotRequired y logSnapshotRequired especifican Cuándo se debe realizar una copia de seguridad de un archivo desde una instantánea de un volumen (y nunca desde el volumen original). El valor predeterminado para todos estos valores es "sí", lo que indica que siempre se debe hacer una copia de seguridad de un archivo y se debe realizar una copia de seguridad de una instantánea de un volumen.

## <a name="adding-partial-files"></a>Agregar archivos parciales

Durante el procesamiento de [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), un escritor tiene la oportunidad de agregar archivos parciales a cada componente. Estos archivos parciales se muestran mediante [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). El escritor de pruebas se puede configurar para agregar archivos parciales mediante la especificación de subelementos PartialFile en un elemento componente.

A continuación se muestra un ejemplo de un elemento de componente que tiene dos subelementos PartialFile:

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

Solo se deben especificar de esta manera los archivos parciales que coincidan parcialmente con un ComponentFile existente (como en el primer archivo parcial del ejemplo) o nuevos archivos parciales que estén en el mismo volumen que un ComponentFile existente (como en el segundo archivo parcial). Para este componente, el solicitante debe realizar una copia de seguridad completa de todos los archivos que coincidan con c: \\ files \\ \* . txt, excepto partial.txt. Después, el solicitante debe hacer una copia de seguridad de los intervalos especificados (donde un intervalo es un desplazamiento seguido de una longitud) para los archivos c: \\ files \\partial.txt y c: \\ files2 \\partial.txt.

Si el escritor está configurado para comprobar las restauraciones de archivos, solo se comprobarán los intervalos de copia de seguridad del archivo parcial en el momento de la restauración. Las modificaciones realizadas en otras partes del archivo pasarán desapercibidas. Si se establece el atributo deletePartialFiles del elemento raíz TestWriter, los archivos parciales se eliminan del volumen original inmediatamente después de crear la instantánea.

## <a name="adding-differenced-files"></a>Agregar archivos diferenciados

Durante el procesamiento de [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), un escritor puede Agregar archivos diferenciados a cada componente. Estos archivos diferenciados se muestran mediante [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). El escritor de pruebas se puede configurar para agregar archivos diferenciados mediante la especificación de subelementos DifferencedFile en un elemento componente.

A continuación se muestra un ejemplo de un elemento de componente que tiene dos subelementos DifferencedFile:

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

A diferencia de los archivos parciales, los archivos diferenciados nunca deben coincidir parcialmente con una especificación ComponentFile. La especificación de archivo en un elemento DifferencedFile debe coincidir exactamente con un ComponentFile (como en el primer archivo diferenciado en el ejemplo) o no debe coincidir en absoluto, sino en un volumen al que se hace referencia en un ComponentFile (como en el segundo archivo diferenciado). Los valores de fecha y hora deben ser relativos a la zona horaria local, pero se convertirán a GMT antes de que se notifique al solicitante. En el ejemplo, solo se realizarán copias de seguridad de los archivos que coincidan con c: \\ files \\ \* . txt o c: \\ files2 \\ \* . txt que se han modificado desde 1/22/2003:12:44:17.

Si el escritor de pruebas está configurado para comprobar las restauraciones de archivos, solo se comprobará la restauración de los archivos modificados. Si se establece el atributo deleteDifferencedFiles del elemento raíz TestWriter, los archivos diferenciados se eliminan del volumen original inmediatamente después de crear la instantánea.

## <a name="new-targets"></a>Nuevos destinos

Algunos escritores permiten al solicitante informarles de que se ha elegido una nueva ubicación para restaurar determinados archivos en. El escritor indica que admite este modo como parte de la máscara de la máscara devuelta por [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). De forma predeterminada, el escritor de pruebas siempre admite nuevos destinos. Esta compatibilidad se puede deshabilitar si se establece el atributo supportsNewTarget del elemento raíz TestWriter en "no".

Si un escritor admite nuevos destinos, el solicitante puede informar al escritor de nuevos destinos llamando a [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget). El escritor comprobará entonces la nueva ubicación de destino para comprobar la restauración en lugar de la ubicación original.

## <a name="more-information"></a>Más información

El escritor de pruebas admite más opciones de configuración que no se describen aquí. El esquema completo de todas las capacidades de configuración del escritor de pruebas se especifica en swriter.xml `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` (para Windows de 64 bits) y `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` (para windows de 32 bits). Este archivo contiene un esquema XML que describe completamente todos los elementos y atributos que componen un archivo de configuración. Cada elemento y cada atributo de este archivo se comentan con una descripción que documenta el uso del atributo o del elemento.

 

 




