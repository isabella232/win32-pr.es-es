---
description: VShadow es una herramienta de línea de comandos que puede usar para crear y administrar instantáneas de volumen.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Herramienta VShadow y ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9043c01d68983d14a0a65f93b993bca3cfe61fcb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477321"
---
# <a name="vshadow-tool-and-sample"></a>Herramienta VShadow y ejemplo

VShadow es una herramienta de línea de comandos que puede usar para crear y administrar instantáneas de volumen.

> [!Note]  
> VShadow se incluye en el Kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores. El SDK de VSS 7.2 incluye una versión de VShadow que solo se ejecuta Windows Server 2003. Para obtener información sobre cómo descargar Windows SDK y el SDK de VSS 7.2, [consulte Servicio de instantáneas de volumen](volume-shadow-copy-service-portal.md).

 

La herramienta VShadow usa opciones de línea de comandos y marcas opcionales para identificar el trabajo que se debe realizar. Cuando se usa sin ninguna opción de línea de comandos, el comando VShadow crea un nuevo conjunto de instantáneas.

Los comandos VShadow realizan las siguientes operaciones:

-   [Crear un conjunto de instantáneas](#creating-a-shadow-copy-set)
-   [Importar un conjunto de instantáneas](#importing-a-shadow-copy-set)
-   [Consulta de propiedades de instantáneas](#querying-shadow-copy-properties)
-   [Eliminación de instantáneas](#deleting-shadow-copies)
-   [Dividir un conjunto de instantáneas](#breaking-a-shadow-copy-set)
-   [Interrumpir un conjunto de instantáneas mediante el método BreakSnapshotSetEx](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [Exponer una instantánea localmente](#exposing-a-shadow-copy-locally)
-   [Exponer una instantánea de forma remota](#exposing-a-shadow-copy-remotely)
-   [Enumerar el estado y los metadatos del escritor](#listing-writer-status-and-metadata)
-   [Realizar operaciones de restauración](#performing-restore-operations)
-   [Revertir a una instantánea anterior](#reverting-to-a-previous-shadow-copy)
-   [Resincronización de LUN](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a>Crear un conjunto de instantáneas

**vshadow** \[ OptionalFlags \] *VolumeList*

Este comando crea un nuevo conjunto de instantáneas.

*VolumeList* es una lista de nombres de volumen. VShadow crea una instantánea para cada volumen de la lista. Opcionalmente, un nombre de volumen se puede terminar con una barra diagonal inversa ( \\ ). Por ejemplo, C: y C: \\ son nombres de volumen válidos. También puede especificar carpetas montadas (por ejemplo, C: DirectoryName) o nombres GUID de \\ volumen (por ejemplo, \\ \\ ? \\ Volume{edbed95e-7e8d-11d8-9d01-505054503030}).

*OptionalFlags es* una máscara de bits de valores de marca opcionales de la tabla siguiente.




| Valor de marca opcional | Descripción | 
|---------------------|-------------|
| <span id="-ad"></span><span id="-AD"></span><strong>-ad</strong><br /> | Esta marca opcional especifica instantáneas de hardware diferenciales. Esta marca y <strong>la marca -ap</strong> son mutuamente excluyentes.<br /><blockquote>[!Note]<br />Esta marca solo se admite en Windows sistemas operativos de servidor.</blockquote><br /> | 
| <span id="-ap"></span><span id="-AP"></span><strong>-ap</strong><br /> | Esta marca opcional especifica instantáneas de hardware plex. Esta marca y <strong>la marca -ad</strong> son mutuamente excluyentes.<br /><blockquote>[!Note]<br />Esta marca solo se admite en Windows sistemas operativos de servidor.</blockquote><br /> | 
| <span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong><strong>-bc=</strong><em>File</em> <strong>.xml</strong><br /> | Esta marca opcional especifica instantáneas no transportables y almacena el documento componentes de copia de seguridad en el archivo especificado. Este archivo se puede usar en una operación de restauración posterior. Esta marca y <strong>la marca -t</strong> son mutuamente excluyentes.<br /><blockquote>[!Note]<br />Esta marca solo se admite en Windows sistemas operativos de servidor.</blockquote><br /> | 
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec= (Comando)</strong><em></em><br /> | Esta marca opcional ejecuta un comando o script después de crear las instantáneas, pero antes de que se cierre la herramienta VShadow. <em>El</em> comando puede especificar un comando de shell ejecutable o un archivo CMD. Si especifica un comando de shell, no se puede especificar ningún parámetro de comando.<br /><blockquote>[!Note]<br />Por motivos de seguridad y para que la implementación sea sencilla, la <strong>marca opcional -exec</strong> no aceptará parámetros que se pasarán al comando o script. Toda la cadena que se pasa a <strong>la marca opcional -exec</strong> se trata como un único archivo CMD o EXE. Para obtener más información sobre esta limitación, vea el código fuente de VShadow.</blockquote><br /> | 
| <span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong><br /> | Esta marca opcional especifica que la operación de instantánea debe completarse solo si se pueden revertir todas las firmas de disco.<br /><blockquote>[!Note]<br />Esta marca solo se admite en Windows sistemas operativos de servidor.</blockquote><br /><strong>Windows Server 2003:</strong> No se admite.<br /> | 
| <span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong><br /> | Esta marca opcional especifica que los LUN de instantáneas se deben enmascarar desde el equipo cuando se divide el conjunto de instantáneas.<br /><blockquote>[!Note]<br />Esta marca solo se admite en Windows sistemas operativos de servidor.</blockquote><br /><strong>Windows Server 2003:</strong> No se admite.<br /> | 
| <span id="-nar"></span><span id="-NAR"></span><strong>-lo</strong><br /> | Esta marca opcional especifica instantáneas sin recuperación automática. Para obtener más información sobre esta opción, vea la documentación de la VSS_VOLSNAP_ATTR_NO_AUTORECOVERY de la <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>enumeración _VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> datos.<br /> | 
| <span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong><br /> | Esta marca opcional especifica que no se deben revertir las firmas de disco.<br /><blockquote>[!Note]<br />Esta marca solo se admite en Windows sistemas operativos de servidor.</blockquote><br /><strong>Windows Server 2003:</strong> No se admite.<br /> | 
| <span id="-nw"></span><span id="-NW"></span><strong>-nw</strong><br /> | Esta marca opcional especifica instantáneas sin que intervendran escritores. Para obtener más información sobre las instantáneas sin participación del escritor, vea <a href="shadow-copy-creation-details.md">Detalles de creación de instantáneas.</a> Esta marca y <strong>las marcas -wi</strong> <strong>y -wx</strong> son mutuamente excluyentes.<br /> | 
| <span id="-p"></span><span id="-P"></span><strong>-p</strong><br /> | Esta marca opcional especifica instantáneas <a href="vssgloss-p.md"><em>persistentes.</em></a><br /><blockquote>[!Note]<br />Esta marca solo se admite en Windows sistemas operativos de servidor.</blockquote><br /> | 
| <span id="-rw"></span><span id="-RW"></span><strong>-rw</strong><br /> | Esta marca opcional especifica que los LUN de instantáneas deben realizarse de lectura y escritura cuando se divide el conjunto de instantáneas.<br /><blockquote>[!Note]<br />Esta marca solo se admite en Windows sistemas operativos de servidor.</blockquote><br /><strong>Windows Server 2003:</strong> No se admite.<br /> | 
| <span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong><br /> | Esta marca opcional especifica instantáneas <a href="vssgloss-c.md"><em>accesibles para el cliente.</em></a><br /><blockquote>[!Note]<br />Esta marca solo se admite en Windows sistemas operativos de servidor.</blockquote><br /> | 
| <span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script=</strong><em>Archivo</em><strong>.cmd</strong><br /> | Esta marca opcional genera un archivo CMD que contiene variables de entorno relacionadas con las instantáneas creadas, como los de instantáneas y los de conjunto de instantáneas.<br /> | 
| <span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t=</strong><em>File</em> <strong>.xml</strong><br /> | Esta marca opcional especifica instantáneas transportables y almacena el documento de componentes de copia de seguridad en el archivo especificado <em> porFile.xml</em> parámetro . Este archivo se puede usar en una operación de importación o restauración posterior. Esta marca y <strong>la marca -bc</strong> son mutuamente excluyentes.<br /><strong>Windows Server 2003, Standard Edition y Windows Server 2003, Web Edition:</strong> No se admiten instantáneas transportables. Todas las ediciones de Windows Server 2003 con Service Pack 1 (SP1) admiten instantáneas transportables.<br /> | 
| <span id="-tr"></span><span id="-TR"></span><strong>-tr</strong><br /> | Esta marca opcional especifica que se debe aplicar la recuperación de TxF durante la creación de instantáneas.<br /><blockquote>[!Note]<br />Esta marca solo se admite en Windows sistemas operativos de servidor.</blockquote><br /> | 
| <span id="-tracing"></span><span id="-TRACING"></span><strong>-tracing</strong><br /> | Esta marca opcional genera una salida detallada que se puede usar para solucionar problemas.<br /> | 
| <span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong><br /> | Esta marca opcional hace que la herramienta VShadow espere la confirmación del usuario antes de salir.<br /> | 
| <span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi=</strong><em>Writer</em><br /> | Esta marca opcional comprueba que el escritor o componente especificado se incluye en la instantánea. <em>Writer</em> puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor. Esta marca y <strong>la marca -nw</strong> son mutuamente excluyentes.<br /> | 
| <span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx=</strong><em>Writer</em><br /> | Esta marca opcional comprueba que el escritor o componente especificado se excluye de la instantánea. <em>Writer</em> puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor. Esta marca y <strong>la marca -nw</strong> son mutuamente excluyentes.<br /> | 




 

## <a name="importing-a-shadow-copy-set"></a>Importar un conjunto de instantáneas

**vshadow** \[ OptionalFlags \] **-i=**_File_ *_.xml_*

La opción de línea de comandos **-i** importa un conjunto de instantáneas transportable.

> [!Note]  
> Esta opción de línea de comandos solo se admite en Windows operativos de servidor.

 

El *File.xml* debe ser un archivo de documento de componentes de copia de seguridad para un conjunto de instantáneas transportable que se creó con la **marca opcional -t** o **-bc.**

Un conjunto de instantáneas es [*una instantánea persistente*](vssgloss-p.md) si se creó con la marca opcional **-p.** Si el conjunto de instantáneas transportable no es persistente, aparece durante un breve período de tiempo mientras se ejecuta el comando de creación de instantáneas y se elimina automáticamente cuando se devuelve el comando. Solo puede importar instantáneas no persistentes durante la creación de instantáneas; para ello, cree el conjunto de instantáneas mediante la marca **opcional -exec** para ejecutar un archivo CMD que llame a VShadow **-i**.

La opción de línea de comandos **-i** no se puede combinar con otras opciones de línea de comandos.

*OptionalFlags es* una máscara de bits de valores de marca opcionales de la tabla siguiente.



| Valor de marca opcional                                                                                                            | Descripción                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_(Comando)_<br/> | Esta marca opcional ejecuta un comando o script después de importar las instantáneas, pero antes de que se cierre la herramienta VShadow. *El* comando puede especificar un comando de shell ejecutable o un archivo CMD. Si especifica un comando de shell, no se puede especificar ningún parámetro de comando.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-tracing**<br/>                                                  | Esta marca opcional genera una salida detallada que se puede usar para solucionar problemas.<br/>                                                                                                                                                                                 |
| <span id="-wait"></span><span id="-WAIT"></span>**-wait**<br/>                                                           | Esta marca opcional hace que la herramienta VShadow espere la confirmación del usuario antes de salir.<br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a>Consulta de propiedades de instantáneas

**vshadow** **-q**

**vshadow** **-qx=**_ShadowCopySetId_

**vshadow** **-s=**_ShadowCopyId_

La opción de línea de comandos **-q** enumera las propiedades de todas las instantáneas del equipo.

La opción de línea de comandos **-qx** enumera las propiedades de todas las instantáneas del conjunto de instantáneas cuyo identificador *especifica ShadowCopySetId.*

La opción de línea de comandos **-s** enumera las propiedades de la instantánea cuyo identificador especifica *ShadowCopyId.*

Estas opciones de línea de comandos usan una combinación de [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) e [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) para obtener las propiedades del conjunto especificado de instantáneas.

Las opciones de línea de comandos **-q**, **-qx** y **-s** son mutuamente excluyentes y no se pueden combinar con otras opciones de línea de comandos.

## <a name="deleting-shadow-copies"></a>Eliminación de instantáneas

**vshadow** **-da**

**vshadow** **-do**

**vshadow** **-dx=**_ShadowCopySetId_

**vshadow** **-ds=**_ShadowCopyId_

El **comando -da** elimina todas las instantáneas del equipo.

> [!Note]  
> La opción de línea de comandos **-da** requiere confirmación del usuario.

 

La opción de línea de comandos **-do** elimina la instantánea más antigua del equipo.

La opción de línea de comandos **-dx** elimina todas las instantáneas del conjunto de instantáneas cuyo identificador *especifica ShadowCopySetId.*

La opción de línea de comandos **-ds** elimina la instantánea cuyo identificador especifica *ShadowCopyId.*

Estas opciones de línea de comandos solo se usan con [*instantáneas persistentes.*](vssgloss-p.md) No es necesario eliminar explícitamente las instantáneas no persistentes, ya que se eliminan automáticamente cuando se cierra el comando de creación de VShadow.

Las opciones de línea de comandos **-da**, **-do**, **-dx** y **-ds** son mutuamente excluyentes y no se pueden combinar con otras opciones de línea de comandos.

## <a name="breaking-a-shadow-copy-set"></a>Dividir un conjunto de instantáneas

**vshadow** **-b=**_ShadowCopySetId_

**vshadow** **-bw=**_ShadowCopySetId_

La opción de línea de comandos **-b=**_ShadowCopySetId_ convierte cada instantánea del conjunto de instantáneas en un volumen independiente de solo lectura.

La opción de línea de comandos **-bw=**_ShadowCopySetId_ convierte cada instantánea del conjunto de instantáneas en un volumen grabable independiente.

> [!Note]  
> Las opciones de línea de comandos **-b** y **-bw** solo se admiten en Windows operativos de servidor.

 

Para obtener información sobre cómo dividir un conjunto de instantáneas, vea [Breaking Shadow Copies](breaking-shadow-copies.md).

Una vez roto el conjunto de instantáneas, el conjunto de instantáneas y las instantáneas individuales ya no existen y no se pueden administrar mediante comandos de VSS.

Un conjunto de instantáneas es persistente si se creó con la **marca opcional -p.** Si el conjunto de instantáneas transportable no es persistente, aparece durante un breve período de tiempo mientras se ejecuta el comando de creación de instantáneas y se elimina automáticamente cuando se devuelve el comando. Puede interrumpir los conjuntos de instantáneas no persistentes solo durante la creación de instantáneas; para ello, cree el conjunto de instantáneas mediante la marca **opcional -exec** para ejecutar un archivo CMD que llame a **vshadow** **-b** o **vshadow** **-bw**.

Las opciones de línea de comandos **-b** y **-bw** son mutuamente excluyentes y no se pueden combinar con otras opciones de línea de comandos.

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a>Interrumpir un conjunto de instantáneas mediante el método BreakSnapshotSetEx

**vshadow** **-bex**

La opción de línea de comandos **-bex** interrumpe un conjunto de instantáneas según las opciones especificadas por las marcas **opcionales -mask**, **-rw**, **-forcerevert** y **-norevert.** Esta opción de línea de comandos es similar a las opciones de línea de comandos **-b** y **-bw.** La opción de línea de comandos **-bex** usa el método [**IVssBackupComponentsEx2::BreakSnapshotSetEx,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) mientras que las opciones de línea de comandos **-b** y **-bw** usan el método [**IVssBackupComponents::BreakSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)

Para obtener información sobre cómo dividir un conjunto de instantáneas, vea [Breaking Shadow Copies](breaking-shadow-copies.md).

> [!Note]  
> La opción de línea de comandos **-bex** solo se admite en Windows operativos de servidor.

 

**vshadow** **-bex** **-mask**

La **marca -mask** especifica que el LUN de instantáneas se enmascarará desde el host. Si se especifica la marca **-mask,** no se pueden especificar las marcas **-rw**, **-forcerevert** y **-norevert.**

**vshadow** **-bex** **-rw**

La **marca -rw** especifica que el LUN de instantáneas se expone al host como un volumen de lectura y escritura.

**vshadow** **-bex** **-forcerevert**

La **marca -forcerevert** especifica que los identificadores de disco de todos los LUN de instantánea se revertirán al de los LUN originales. Sin embargo, si alguno de los LUN originales está presente en el sistema, se producirá un error en la operación y no se revertirá ninguno de los identificadores. Esta marca y **la marca -norevert** son mutuamente excluyentes.

**vshadow** **-bex** **-norevert**

La **marca -norevert** especifica que no se revertirá ninguno de los identificadores de disco LUN de instantáneas. Esta marca y **la marca -forcerevert** son mutuamente excluyentes.

## <a name="exposing-a-shadow-copy-locally"></a>Exponer una instantánea localmente

**vshadow** **-el=**_ShadowCopyId_*_,_*_LocalEmptyDirectory_

 **vshadow** **-el=**_ShadowCopyId_*_,_*_UnusedDriveLetter_

La opción de línea de comandos **-el** asigna una carpeta montada o una letra de unidad a una instantánea persistente. Tenga en cuenta que el contenido del volumen seguirá siendo de solo lectura a menos que llame posteriormente **a vshadow** **-bw** para interrumpir el conjunto de instantáneas.

> [!Note]  
> Las instantáneas no persistentes y [*las*](vssgloss-c.md) instantáneas accesibles para el cliente no se pueden exponer localmente.

 

Por ejemplo, si {edbed95e-7e8d-11d8-9d01-505054503030} es el GUID de una instantánea persistente existente y X: es una letra de unidad no utilizada, el siguiente comando expone la instantánea en X:

**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030}, x:**

En el ejemplo siguiente se muestra cómo exponer la misma instantánea en la carpeta montada C: \\ ShadowCopies \\ June23:

**mkdir c: \\ ShadowCopies \\ June23**

**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},c: \\ ShadowCopies \\ June23**

La opción de línea de comandos **-el** no se puede combinar con otras opciones de línea de comandos.

## <a name="exposing-a-shadow-copy-remotely"></a>Exponer una instantánea de forma remota

**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_

 **vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_

La opción de línea de comandos **-er** asigna un nombre de recurso compartido de solo lectura al directorio raíz (o un subdirectorio) de la instantánea. Tenga en cuenta que el contenido del recurso compartido seguirá siendo de solo lectura a menos que llame posteriormente **a vshadow** **-bw** para interrumpir el conjunto de instantáneas.

> [!Note]  
> [*Las instantáneas accesibles por el*](vssgloss-c.md) cliente no se pueden exponer de forma remota.

 

Por ejemplo, si {edbed95e-7e8d-11d8-9d01-505054503030} es el GUID de una instantánea persistente existente y el recurso compartido 123 es un nombre de recurso compartido sin usar, el siguiente comando expone la instantánea bajo el recurso compartido \_ \_ 123:

**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030}, share \_ 123**

En el ejemplo siguiente se muestra cómo exponer solo un subárbol (denominado "Carpeta1 Carpeta2") de la misma instantánea \\ en el mismo recurso compartido:

**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share \_ 123,Folder1 \\ Folder2**

La opción de línea de comandos **-er** no se puede combinar con otras opciones de línea de comandos.

## <a name="listing-writer-status-and-metadata"></a>Enumerar el estado y los metadatos del escritor

**vshadow** **-ws**

**vshadow** **-wm**

**vshadow** **-wm2**

**vshadow** **-wm3**

La opción de línea de comandos **-ws** enumera los escritores de VSS que se ejecutan actualmente en el equipo y describe su estado. Este comando es el equivalente al comando [vssadmin list writers.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) Hay seis valores de estado posibles: Estable, Con error, Desconocido, Esperando inmovilización, Inmovilizado y Esperando finalización.

La opción de línea de comandos **-wm** muestra un resumen de los metadatos del escritor, incluidos los volúmenes afectados.

La opción de línea de **comandos -wm2** enumera todos los metadatos del escritor.

La opción de línea de comandos **-wm3** enumera todos los metadatos del escritor en formato XML sin formato.

**Windows Vista y Windows Server 2003:** No se admite la opción de línea de comandos **-wm3.**

Puede usar esta información para determinar qué volúmenes incluir en el conjunto de instantáneas de volumen.

> [!Note]  
> Si el estado del escritor es Estable o En espera de finalización, se puede considerar que el escritor está en un estado estable, listo para la siguiente copia de seguridad.

 

Las opciones de línea de comandos **-ws**, **-wm,** **-wm2** y **-wm3** son mutuamente excluyentes y no se pueden combinar con otras opciones de línea de comandos.

## <a name="performing-restore-operations"></a>Realizar operaciones de restauración

**vshadow** \[ OptionalFlags \] **-r=**_File_ *_.xml_*

**vshadow** \[ OptionalFlags \] **-rs=**_File_ *_.xml_*

La opción de línea de comandos **-r** realiza una operación de restauración.

La opción de línea de comandos **-rs** realiza una operación de restauración simulada.

El *File.xml* debe ser un archivo de documento componentes de copia de seguridad para un conjunto de instantáneas que se creó con la **marca opcional -t** o **-bc.**

Las opciones de línea de comandos **-r** y **-rs** son mutuamente excluyentes y no se pueden combinar con otras opciones de línea de comandos.

*OptionalFlags es* una máscara de bits de valores de marca opcionales de la tabla siguiente.



| Valor de marca opcional                                                                                                            | Descripción                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi=**_Writer_<br/>             | Esta marca opcional comprueba que el escritor o componente especificado se incluye en la restauración. *Writer* puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor.<br/>                                                                                    |
| <span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx=**_Writer_<br/>             | Esta marca opcional comprueba que el escritor o componente especificado se excluye de la restauración. *Writer* puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor.<br/>                                                                                  |
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_(Comando)_<br/> | Esta marca opcional ejecuta un comando o script entre los eventos previos a la restauración y posteriores a la restauración que se envían a los escritores. *El* comando puede especificar un comando de shell ejecutable o un archivo CMD. Si especifica un comando de shell, no se puede especificar ningún parámetro de comando.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-tracing**<br/>                                                  | Esta marca opcional genera una salida detallada que se puede usar para solucionar problemas.<br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a>Revertir a una instantánea anterior

**vshadow** **-revert=**_ShadowCopyId_

> [!Note]  
> Esta opción de línea de comandos solo se admite en Windows operativos de servidor.

 

**Windows Server 2008 y Windows Server 2003:** No se admite.

La opción de línea de comandos **-revert** revierte un volumen a la instantánea anterior cuyo identificador especifica *ShadowCopyId.*

La opción de línea de comandos **-revert** no se puede combinar con otras opciones de línea de comandos.

## <a name="resynchronizing-luns"></a>Resincronización de LUN

**vshadow** **-addresync=**_ShadowCopyId_ **-resync=**_BCDFileName_ \[ OptionalResyncFlags\]

**vshadow** **-addresync=**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-resync=**_BCDFileName_ \[ OptionalResyncFlags\]

La opción de línea de comandos **-addresync** especifica los volúmenes que se incluirán en una operación de resincronización de LUN. El *parámetro ShadowCopyId* especifica el identificador de la instantánea. El parámetro *Opcional TargetVolumeDriveLetter* especifica el volumen de destino donde se va a copiar el contenido del volumen de instantáneas.

La opción de línea de comandos **-resync** inicia una operación de resincronización de LUN. Una vez completada la operación, la firma de cada LUN de destino debe ser idéntica a la del LUN del volumen de destino. El *parámetro BCDFileName* especifica el nombre del archivo XML que contiene el documento del componente de copia de seguridad.

> [!Note]  
> Las opciones de línea de comandos **-addresync** **y -resync** solo se admiten en Windows operativos de servidor.

 

**Windows Server 2008 y Windows Server 2003:** No se admite.

*OptionalResyncFlags es* una máscara de bits de valores de marca opcionales de la tabla siguiente.




| Valor de marca opcional | Descripción | 
|---------------------|-------------|
| <span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong><br /> | Esta marca opcional especifica que una vez completada la operación, la firma de cada LUN de destino debe ser idéntica a la del LUN original que se usó para crear la instantánea, no el LUN del volumen de destino.<br /><blockquote>[!Note]<br />La <strong>marca -revertsig</strong> solo se admite en Windows operativos de servidor.</blockquote><br /><strong>Windows Server 2008 y Windows Server 2003:</strong> No se admite.<br /> | 
| <span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong><br /> | Esta marca opcional especifica que el servicio VSS no debe comprobar si hay volúmenes no seleccionados que se sobrescribirían mediante la operación de resincronización de LUN.<br /><blockquote>[!Note]<br />La <strong>marca -novolcheck</strong> solo se admite en Windows operativos de servidor.</blockquote><br /><strong>Windows Server 2008 y Windows Server 2003:</strong> No se admite.<br /> | 




 

 

 
