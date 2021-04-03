---
description: COMTEST es un solicitante de VSS que prueba las operaciones avanzadas de copia de seguridad y restauración.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Herramienta de prueba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7559c304532b337214108435b740595897694f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913386"
---
# <a name="betest-tool"></a>Herramienta de prueba

COMTEST es un solicitante de VSS que prueba las operaciones avanzadas de copia de seguridad y restauración. Esta herramienta se puede usar para probar el uso de una aplicación de características de VSS complejas, como las siguientes:

-   Copia de seguridad incremental y diferencial
-   Opciones de restauración complejas, como la restauración autoritativa
-   Opciones de puesta al día

> [!Note]  
> COMTEST se incluye en el kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores. El SDK de VSS 7,2 incluye una versión de COMTEST que solo se ejecuta en Windows Server 2003. En este tema se describe la versión Windows SDK de COMTEST, no la versión 2003 de Windows Server incluida en el SDK de VSS 7,2. Para obtener información acerca de cómo descargar el Windows SDK y el SDK de VSS 7,2, consulte [servicio de instantáneas de volumen](volume-shadow-copy-service-portal.md).

 

En la instalación de Windows SDK, la herramienta COMTEST se puede encontrar en `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para Windows de 64 bits) y `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para windows de 32 bits).

## <a name="running-the-betest-tool"></a>Ejecutar la herramienta COMTEST

Para ejecutar la herramienta COMTEST desde la línea de comandos, use la siguiente sintaxis:

 *Opciones de línea de comandos de* test

En el ejemplo de uso siguiente se muestra cómo usar la herramienta COMTEST junto con la [herramienta VSS Writer](vss-test-writer-tool.md), que es una VSS Writer.

**Ejemplo de uso de la herramienta de prueba**

1.  Cree un directorio de prueba denominado C: \\ COMTEST. Copie los siguientes archivos en este directorio:
    -   betest.exe
    -   vswriter.exe
    -   [BetestSample.xml](#sample-xml-configuration-file-betestsamplexml)
    -   [VswriterSample.xml](#sample-xml-configuration-file-vswritersamplexml)
2.  Cree un directorio denominado C: \\ TestPath. Coloque algunos archivos de datos de prueba en este directorio.
3.  Cree un directorio denominado C: \\ BackupDestination. Deje este directorio vacío.
4.  Abra dos ventanas de comandos con privilegios elevados y establezca el directorio de trabajo de cada en C: \\ compruébelo.
5.  En la primera ventana de comandos, inicie la [herramienta VSS test Writer](vss-test-writer-tool.md) de la manera siguiente:

    **vswriter.exe VswriterSample.xml**

    En el archivo vswriterSample.xml se configura la herramienta VSS Writer (vswriter) para notificar el contenido del directorio c: \\ TestPath como preparación para una operación de copia de seguridad. Tenga en cuenta que la herramienta de escritura de prueba de VSS no producirá ningún resultado hasta que detecte actividad de un solicitante como COMTEST. Para detener la herramienta VSS Writer, presione CTRL + C.

6.  En la segunda ventana de comandos, use la herramienta COMTEST para realizar una operación de copia de seguridad como se indica a continuación:

    **betest.exe/B/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**

    COMTEST hará una copia de seguridad de los archivos del \\ directorio c: TestPath en el \\ directorio c: BackupDestination Se guardará el documento del componente de copia de seguridad en C: \\ Compruébelo \\backup.xml.

7.  Si la operación de copia de seguridad se realiza correctamente, elimine el contenido del directorio C: \\ TestPath y use la herramienta COMTEST para realizar una operación de restauración de la siguiente manera:

    **betest.exe/R/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**

## <a name="betest-tool-command-line-options"></a>Opciones de Command-Line de herramientas de prueba

La herramienta COMTEST usa las siguientes opciones de línea de comandos para identificar el trabajo que se va a realizar.

<dl> <dt>

<span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**
</dt> <dd>

Realiza una operación de restauración autoritativa para Active Directory o Active Directory Application Mode.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_B"></span><span id="_b"></span>**B**
</dt> <dd>

Realiza una operación de copia de seguridad, pero no realiza una restauración.

</dd> <dt>

<span id="_BC"></span><span id="_bc"></span>**/BC**
</dt> <dd>

Solo realiza la operación de copia de seguridad completa.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *nombreDeArchivo*
</dt> <dd>

> [!Note]  
> Esta opción de línea de comandos solo se proporciona para la compatibilidad con versiones anteriores. En su lugar, se debe utilizar la opción de línea de comandos **/x** .

 

Selecciona los componentes de los que se va a realizar una copia de seguridad o que se van a restaurar según el contenido del archivo de configuración especificado por *filename*. Este archivo debe contener solo caracteres ANSI en el intervalo comprendido entre 0 y 127, y no debe tener más de 1 MB. Cada línea del archivo debe tener el formato siguiente:

*WriterId* : *ComponentName*;

Donde *WriterId* es el identificador del escritor y *ComponentName* es el nombre de uno de los componentes del escritor. El identificador del escritor y los nombres de los componentes deben estar entre comillas y debe haber espacios delante y detrás del signo de dos puntos (:). Si se especifican dos o más componentes, deben separarse con comas. Por ejemplo:

"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";

</dd> <dt>

<span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** ( *ruta* )
</dt> <dd>

Guarde los archivos de copia de seguridad en o los restaure desde el directorio de copia de seguridad especificado por *path*.

</dd> <dt>

<span id="_NBC"></span><span id="_nbc"></span>**/NBC**
</dt> <dd>

Omite la operación de copia de seguridad completa.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_O"></span><span id="_o"></span>**/O**
</dt> <dd>

Especifica que la copia de seguridad incluye un estado del sistema de arranque.

</dd> <dt>

<span id="_P"></span><span id="_p"></span>**/P**
</dt> <dd>

Crea una instantánea persistente.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span> *Nombre de archivo* /pre
</dt> <dd>

Si el tipo de copia de seguridad especificado en la opción de línea de comandos **/t** es incremental o diferencial, establezca el documento de copia de seguridad en el archivo especificado por *filename* para la copia de seguridad completa o incremental anterior.

**Windows Server 2003 y Windows XP:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_R"></span><span id="_r"></span>**/R**
</dt> <dd>

Realiza la restauración pero no realiza la copia de seguridad. Se debe usar junto con la opción de línea de comandos **/s** .

</dd> <dt>

<span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**
</dt> <dd>

Crea una instantánea que se puede utilizar para la reversión de la aplicación.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *nombreDeArchivo*
</dt> <dd>

En el caso de la copia de seguridad, guarda el documento de copia de seguridad en el archivo especificado por *filename*. En el caso de la restauración, carga el documento de copia de seguridad desde este archivo.

</dd> <dt>

<span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**
</dt> <dd>

Crea una instantánea de volumen pero no realiza copias de seguridad ni restauración.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**
</dt> <dd>

Detiene la prueba cuando se encuentra el primer error de escritura.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *copia*
</dt> <dd>

Especifica el tipo de copia de seguridad. *Copia* puede ser completo, registro, copia, incremental o diferencial. Para obtener más información sobre los tipos de copia de seguridad, vea [**\_ \_ tipo de copia de seguridad de VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).

</dd> <dt>

<span id="_V"></span><span id="_v"></span>**/V**
</dt> <dd>

Genera una salida detallada que se puede usar para solucionar problemas.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *nombreDeArchivo*
</dt> <dd>

Selecciona los componentes de los que se va a realizar una copia de seguridad o que se van a restaurar según el contenido del archivo de configuración XML especificado por *filename*. Este archivo solo debe contener caracteres ANSI en el intervalo comprendido entre 0 y 127. El formato del archivo XML lo define el esquema en el archivo de BETest.xml. Para obtener un archivo de configuración de ejemplo, vea BetestSample.xml. Ambos archivos se encuentran en el directorio vsstools

> [!Note]  
> Puede ver el archivo de BETest.xml en Internet Explorer. Antes de abrir este archivo, asegúrese de que el archivo XDR-Schema. xsl está en el mismo directorio que BETest.xml. El archivo XDR-Schema. xsl contiene instrucciones de representación que hacen que el archivo BETest.xml sea más legible.

 

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a>Archivo de configuración XML de ejemplo: BetestSample.xml

El siguiente archivo de configuración de ejemplo, BetestSample.xml, se puede encontrar en el directorio Vsstools

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

En este ejemplo de un archivo de configuración simple se selecciona un componente del que se va a realizar la copia de seguridad o la restauración.

## <a name="sample-xml-configuration-file-vswritersamplexml"></a>Archivo de configuración XML de ejemplo: VswriterSample.xml

El siguiente archivo de configuración de ejemplo, VswriterSample.xml, se puede encontrar en el directorio Vsstools

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

El elemento raíz de este archivo de configuración se denomina TestWriter. Todos los demás elementos se organizan bajo el elemento TestWriter.

El primer atributo asociado a TestWriter es el atributo Usage. Este atributo especifica el tipo de uso indicado a través del método [**IVssExamineWriterMetadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) . Uno de los valores posibles para este atributo son los \_ datos de usuario.

El segundo atributo es el atributo deleteFiles. Este atributo se describe en [configuración de los atributos del escritor](vss-test-writer-tool.md).

El primer elemento secundario del elemento raíz es un elemento RestoreMethod. Este elemento especifica lo siguiente:

-   El método restore (en este caso, RESTOre \_ If \_ \_ se puede \_ reemplazar)
-   Si el escritor requiere eventos de restauración (en este caso, siempre)
-   Si es necesario un reinicio después de restaurar el escritor (en este caso, no)

Este elemento puede especificar opcionalmente una asignación de ubicación alternativa. (En este caso, no se especifica ninguna ubicación alternativa). Para obtener más información, vea [especificar asignaciones de ubicaciones alternativas](vss-test-writer-tool.md).

El segundo elemento secundario es un elemento de componente. Este elemento hace que el escritor agregue un componente a sus metadatos. Un elemento Component contiene atributos para describir el componente y los elementos secundarios para describir el contenido del componente, como el siguiente:

-   componentType para indicar si se trata de un grupo de archivos o de una base de datos (en este caso, un grupo de archivos)
-   logicalPath para la ruta de acceso lógica del componente (en este caso, no se especifica ninguno)
-   componentName para el nombre del componente (en este caso, "prueba")
-   Selectable para indicar el estado Selectable-for-Backup

El elemento componente también tiene un elemento secundario denominado ComponentFile para agregar una especificación de archivo a este componente. (Un elemento de componente puede tener un número arbitrario de elementos ComponentFile que se pueden especificar para cada componente). Este elemento ComponentFile tiene los siguientes atributos:

-   Ruta de acceso = "c: \\ TestPath"
-   filespec = " \* "
-   Recursive = "no"

 

 



