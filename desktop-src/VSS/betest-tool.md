---
description: BETest es un solicitante de VSS que prueba las operaciones avanzadas de copia de seguridad y restauración.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Herramienta BETest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5f37e8bfc224061a8205bf0759cbba4798b0d53227e4f12d89b1e9ddf629d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471155"
---
# <a name="betest-tool"></a>Herramienta BETest

BETest es un solicitante de VSS que prueba las operaciones avanzadas de copia de seguridad y restauración. Esta herramienta se puede usar para probar el uso de características complejas de VSS de una aplicación, como las siguientes:

-   Copia de seguridad incremental y diferencial
-   Opciones de restauración complejas, como la restauración autoritativa
-   Opciones de reversión

> [!Note]  
> BETest se incluye en el Kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores. El SDK de VSS 7.2 incluye una versión de BETest que solo se ejecuta Windows Server 2003. En este tema se describe Windows versión del SDK de BETest, no la versión de Windows Server 2003 incluida en el SDK de VSS 7.2. Para obtener información sobre cómo descargar el SDK Windows y el SDK de VSS 7.2, [consulte Servicio de instantáneas de volumen](volume-shadow-copy-service-portal.md).

 

En la instalación del SDK de Windows, la herramienta BETest se puede encontrar en (para Windows de 64 bits) y (para archivos de `%Program Files(x86)%\Windows Kits\8.1\bin\x64` `%Program Files(x86)%\Windows Kits\8.1\bin\x86` 32 Windows).

## <a name="running-the-betest-tool"></a>Ejecución de la herramienta BETest

Para ejecutar la herramienta BETest desde la línea de comandos, use la sintaxis siguiente:

**BeTest** *command-line-options*

En el ejemplo de uso siguiente se muestra cómo usar la herramienta BETest junto con la herramienta [VSS Test Writer](vss-test-writer-tool.md), que es vss writer.

**Ejemplo de uso de la herramienta BETest**

1.  Cree un directorio de prueba denominado C: \\ BETest. Copie los siguientes archivos en este directorio:
    -   betest.exe
    -   vswriter.exe
    -   [BetestSample.xml](#sample-xml-configuration-file-betestsamplexml)
    -   [VswriterSample.xml](#sample-xml-configuration-file-vswritersamplexml)
2.  Cree un directorio denominado C: \\ TestPath. Coloque algunos archivos de datos de prueba en este directorio.
3.  Cree un directorio denominado C: \\ BackupDestination. Deje este directorio vacío.
4.  Abra dos ventanas de comandos con privilegios elevados y establezca el directorio de trabajo de cada una en C: \\ BETest.
5.  En la primera ventana de comandos, inicie la herramienta [VSS Test Writer](vss-test-writer-tool.md) como se muestra a continuación:

    **vswriter.exe VswriterSample.xml**

    El vswriterSample.xml archivo configura la herramienta VSS Test Writer (vswriter) para notificar el contenido del directorio c: TestPath como preparación para una operación de copia \\ de seguridad. Tenga en cuenta que la herramienta VSS Test Writer no producirá resultados hasta que detecte la actividad de un solicitante como BETest. Para detener la herramienta VSS Test Writer, presione CTRL+C.

6.  En la segunda ventana de comandos, use la herramienta BETest para realizar una operación de copia de seguridad de la siguiente manera:

    **betest.exe /B /S backup.xml /D C: \\ BackupDestination /X BetestSample.xml**

    BETest realizará una copia de seguridad de los archivos desde el directorio C: \\ TestPath al directorio C: \\ BackupDestination. Guardará el documento del componente de copia de seguridad en C: \\ BETest \\backup.xml.

7.  Si la operación de copia de seguridad se realiza correctamente, elimine el contenido del directorio C: TestPath y use la herramienta BETest para realizar una operación de restauración como \\ se muestra a continuación:

    **betest.exe /R /S backup.xml /D C: \\ BackupDestination /X BetestSample.xml**

## <a name="betest-tool-command-line-options"></a>BETest Tool Command-Line Options

La herramienta BETest usa las siguientes opciones de línea de comandos para identificar el trabajo que se va a realizar.

<dl> <dt>

<span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**
</dt> <dd>

Realiza una operación de restauración autoritativa para Active Directory o Active Directory modo de aplicación.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_B"></span><span id="_b"></span>**/b**
</dt> <dd>

Realiza una operación de copia de seguridad, pero no realiza una restauración.

</dd> <dt>

<span id="_BC"></span><span id="_bc"></span>**/BC**
</dt> <dd>

Realiza solo la operación de copia de seguridad completa.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *Filename*
</dt> <dd>

> [!Note]  
> Esta opción de línea de comandos solo se proporciona por compatibilidad con versiones anteriores. En **su lugar,** se debe usar la opción de línea de comandos /X.

 

Selecciona los componentes de los que se va a realizar una copia de seguridad o se restaurarán en función del contenido del archivo de configuración especificado por *Filename*. Este archivo solo debe contener caracteres ANSI en el intervalo de 0 a 127 y no debe tener más de 1 MB. Cada línea del archivo debe usar el formato siguiente:

*WriterId* : *ComponentName*;

Donde *WriterId* es el identificador de escritor y *ComponentName* es el nombre de uno de los componentes del escritor. El identificador de escritor y los nombres de componente deben estar entre comillas y deben haber espacios antes y después de los dos puntos (:). Si se especifican dos o más componentes, deben estar separados por comas. Por ejemplo:

"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";

</dd> <dt>

<span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D Ruta de** *acceso*
</dt> <dd>

Guarde los archivos de copia de seguridad en o restáurelos desde el directorio de copia de seguridad especificado por *Path*.

</dd> <dt>

<span id="_NBC"></span><span id="_nbc"></span>**/NB**
</dt> <dd>

Omite la operación de copia de seguridad completa.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_O"></span><span id="_o"></span>**/o**
</dt> <dd>

Especifica que la copia de seguridad incluye un estado del sistema de arranque.

</dd> <dt>

<span id="_P"></span><span id="_p"></span>**/p**
</dt> <dd>

Crea una instantánea persistente.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Nombre de archivo** *anterior*
</dt> <dd>

Si el tipo de copia de seguridad especificado en la opción de línea de comandos **/T** es INCREMENTAL o DIFFERENTIAL, establezca el documento de copia de seguridad en el archivo especificado por *Filename* para la copia de seguridad completa o incremental anterior.

**Windows Server 2003 y Windows XP:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_R"></span><span id="_r"></span>**/r**
</dt> <dd>

Realiza la restauración, pero no realiza la copia de seguridad. Debe usarse junto con la opción de línea de comandos **/S.**

</dd> <dt>

<span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**
</dt> <dd>

Crea una instantánea que se puede usar para la reversión de aplicaciones.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Filename*
</dt> <dd>

En el caso de la copia de seguridad, guarda el documento de copia de seguridad en el archivo especificado por *Nombre de archivo*. Solo en caso de restauración, carga el documento de copia de seguridad desde este archivo.

</dd> <dt>

<span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**
</dt> <dd>

Crea una instantánea de volumen, pero no realiza copias de seguridad ni restauraciones.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**
</dt> <dd>

Detiene BETest cuando se encuentra el primer error de escritor.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*
</dt> <dd>

Especifica el tipo de copia de seguridad. *BackupType* puede ser FULL, LOG, COPY, INCREMENTAL o DIFFERENTIAL. Para obtener más información sobre los tipos de copia de seguridad, [**vea VSS \_ BACKUP \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).

</dd> <dt>

<span id="_V"></span><span id="_v"></span>**/v**
</dt> <dd>

Genera una salida detallada que se puede usar para solucionar problemas.

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> <dt>

<span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** Nombre de *archivo*
</dt> <dd>

Selecciona los componentes de los que se va a realizar una copia de seguridad o se restaurarán en función del contenido del archivo de configuración XML especificado por *Filename*. Este archivo solo debe contener caracteres ANSI en el intervalo de 0 a 127. El formato del archivo XML se define mediante el esquema en el BETest.xml archivo. Para obtener un archivo de configuración de ejemplo, consulte BetestSample.xml. Ambos archivos están en el directorio vsstools.

> [!Note]  
> Puede ver el archivo BETest.xml en Internet Explorer. Antes de abrir este archivo, asegúrese de que el archivo xdr-schema.xsl está en el mismo directorio que BETest.xml. El archivo xdr-schema.xsl contiene instrucciones de representación que hacen que BETest.xml archivo sea más legible.

 

**Windows Server 2003:** No se admite esta opción de línea de comandos.

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a>Archivo de configuración XML de ejemplo: BetestSample.xml

El siguiente archivo de configuración de ejemplo, BetestSample.xml, se puede encontrar en el directorio Vsstools.

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

En este ejemplo de un archivo de configuración simple se selecciona un componente del que se va a realizar una copia de seguridad o restaurar.

## <a name="sample-xml-configuration-file-vswritersamplexml"></a>Archivo de configuración XML de ejemplo: VswriterSample.xml

El siguiente archivo de configuración de ejemplo, VswriterSample.xml, se puede encontrar en el directorio Vsstools.

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

El elemento raíz de este archivo de configuración se denomina TestWriter. Todos los demás elementos se organizan en el elemento TestWriter.

El primer atributo asociado a TestWriter es el atributo usage. Este atributo especifica el tipo de uso notificado a través [**del método IVssExgvWriterMetadata::GetIdentity.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) Uno de los valores posibles para este atributo es USER \_ DATA.

El segundo atributo es el atributo deleteFiles. Este atributo se describe en [Configuring Writer Attributes](vss-test-writer-tool.md).

El primer elemento secundario del elemento raíz es un elemento RestoreMethod. Este elemento especifica lo siguiente:

-   El método de restauración (en este caso, RESTORE \_ IF \_ SE PUEDE \_ \_ REEMPLAZAR)
-   Si el escritor requiere eventos de restauración (en este caso, siempre)
-   Si se requiere un reinicio después de restaurar el sistema de escritura (en este caso, no)

Opcionalmente, este elemento puede especificar una asignación de ubicación alternativa. (En este caso, no se especifica ninguna ubicación alternativa). Para obtener más información, vea [Especificar asignaciones de ubicación alternativas.](vss-test-writer-tool.md)

El segundo elemento secundario es un elemento Component. Este elemento hace que el escritor agregue un componente a sus metadatos. Un elemento Component contiene atributos para describir el componente y los elementos secundarios para describir el contenido del componente, como el siguiente:

-   componentType para indicar si se trata de un grupo de archivos o una base de datos (en este caso, un grupo de archivos)
-   logicalPath para la ruta de acceso lógica del componente (en este caso, no se especifica ninguno)
-   componentName para el nombre del componente (en este caso, "TestFiles")
-   seleccionable para indicar el estado seleccionable para copia de seguridad

El elemento Component también tiene un elemento secundario denominado ComponentFile para agregar una especificación de archivo a este componente. (Un elemento Component puede tener un número arbitrario de elementos ComponentFile que se pueden especificar para cada componente). Este elemento ComponentFile tiene los siguientes atributos:

-   path="c: \\ TestPath"
-   filespec=" \* "
-   recursive="no"

 

 



