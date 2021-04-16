---
description: VShadow es una herramienta de línea de comandos que puede usar para crear y administrar instantáneas de volumen.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Herramienta y ejemplo de VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497524"
---
# <a name="vshadow-tool-and-sample"></a>Herramienta y ejemplo de VShadow

VShadow es una herramienta de línea de comandos que puede usar para crear y administrar instantáneas de volumen.

> [!Note]  
> VShadow se incluye en el kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores. El SDK de VSS 7,2 incluye una versión de VShadow que solo se ejecuta en Windows Server 2003. Para obtener información acerca de cómo descargar el Windows SDK y el SDK de VSS 7,2, consulte [servicio de instantáneas de volumen](volume-shadow-copy-service-portal.md).

 

La herramienta VShadow utiliza opciones de la línea de comandos y marcas opcionales para identificar el trabajo que se va a realizar. Cuando se usa sin ninguna opción de línea de comandos, el comando VShadow crea un nuevo conjunto de instantáneas.

Los comandos de VShadow realizan las operaciones siguientes:

-   [Crear un conjunto de instantáneas](#creating-a-shadow-copy-set)
-   [Importar un conjunto de instantáneas](#importing-a-shadow-copy-set)
-   [Consultar propiedades de instantáneas](#querying-shadow-copy-properties)
-   [Eliminar instantáneas](#deleting-shadow-copies)
-   [Dividir un conjunto de instantáneas](#breaking-a-shadow-copy-set)
-   [Dividir un conjunto de instantáneas mediante el método BreakSnapshotSetEx](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [Exponer una instantánea localmente](#exposing-a-shadow-copy-locally)
-   [Exponer una instantánea de forma remota](#exposing-a-shadow-copy-remotely)
-   [Enumerar el estado y los metadatos del escritor](#listing-writer-status-and-metadata)
-   [Realización de operaciones de restauración](#performing-restore-operations)
-   [Revertir a una instantánea anterior](#reverting-to-a-previous-shadow-copy)
-   [Volver a sincronizar LUN](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a>Crear un conjunto de instantáneas

**vshadow** \[ OptionalFlags \] *VolumeList*

Este comando crea un nuevo conjunto de instantáneas.

*VolumeList* es una lista de nombres de volumen. VShadow crea una instantánea para cada volumen de la lista. Opcionalmente, un nombre de volumen puede terminar con una barra diagonal inversa ( \\ ). Por ejemplo, C: y C: \\ son nombres de volumen válidos. También puede especificar las carpetas montadas (por ejemplo, C: \\ directoryname) o los nombres de GUID de volumen (por ejemplo, \\ \\ ? \\ Volumen {edbed95e-7e8d-11d8-9d01-505054503030}).

*OptionalFlags* es una máscara de máscara de valores de marca opcionales de la tabla siguiente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor opcional de marca</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong><br/></td>
<td>Esta marca opcional especifica las instantáneas de hardware diferenciales. Esta marca y la marca <strong>-AP</strong> son mutuamente excluyentes.<br/>
<blockquote>
[!Note]<br />
Esta marca solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-ap"></span><span id="-AP"></span><strong>-AP</strong><br/></td>
<td>Esta marca opcional especifica las instantáneas de hardware de Plex. Esta marca y la marca <strong>-ad</strong> son mutuamente excluyentes.<br/>
<blockquote>
[!Note]<br />
Esta marca solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-BC =</strong><em>File</em><strong>. XML</strong><br/></td>
<td>Esta marca opcional especifica las instantáneas no transportables y almacena el documento de componentes de copia de seguridad en el archivo especificado. Este archivo se puede usar en una operación de restauración posterior. Esta marca y la marca <strong>-t</strong> son mutuamente excluyentes.<br/>
<blockquote>
[!Note]<br />
Esta marca solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec =</strong><em>comando</em><br/></td>
<td>Esta marca opcional ejecuta un comando o script después de crear las instantáneas, pero antes de que se cierre la herramienta VShadow. El <em>comando</em> puede especificar un comando de Shell ejecutable o un archivo CMD. Si especifica un comando de Shell, no se puede especificar ningún parámetro de comando.<br/>
<blockquote>
[!Note]<br />
Por motivos de seguridad y para simplificar la implementación, la marca opcional <strong>-exec</strong> no aceptará los parámetros que se van a pasar al comando o script. La cadena completa pasada a la marca opcional <strong>-exec</strong> se trata como un único archivo CMD o exe. Para obtener más información sobre esta limitación, vea el código fuente de VShadow.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong><br/></td>
<td>Esta marca opcional Especifica que la operación de instantáneas se debe completar solo si se pueden revertir todas las firmas de disco.<br/>
<blockquote>
[!Note]<br />
Esta marca solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> No compatible.<br/></td>
</tr>
<tr class="even">
<td><span id="-mask"></span><span id="-MASK"></span><strong>-máscara</strong><br/></td>
<td>Esta marca opcional Especifica que los LUN de instantáneas deben enmascararse del equipo cuando se interrumpe el conjunto de instantáneas.<br/>
<blockquote>
[!Note]<br />
Esta marca solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> No compatible.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nar"></span><span id="-NAR"></span><strong>-Nar</strong><br/></td>
<td>Esta marca opcional especifica instantáneas sin recuperación automática. Para obtener más información acerca de esta opción, consulte la documentación de la VSS_VOLSNAP_ATTR_NO_AUTORECOVERY marca de la enumeración <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong><br/></td>
<td>Esta marca opcional Especifica que las firmas de disco no se deben revertir.<br/>
<blockquote>
[!Note]<br />
Esta marca solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> No compatible.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nw"></span><span id="-NW"></span><strong>-NW</strong><br/></td>
<td>Esta marca opcional especifica instantáneas sin necesidad de escritores. Para obtener más información sobre las instantáneas sin participación del escritor, consulte los <a href="shadow-copy-creation-details.md">detalles de creación de instantáneas</a>. Esta marca y las marcas <strong>-Wi</strong> y <strong>-WX</strong> son mutuamente excluyentes.<br/></td>
</tr>
<tr class="even">
<td><span id="-p"></span><span id="-P"></span><strong>-p</strong><br/></td>
<td>Esta marca opcional especifica <a href="vssgloss-p.md"><em>instantáneas persistentes</em></a>.<br/>
<blockquote>
[!Note]<br />
Esta marca solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-rw"></span><span id="-RW"></span><strong>-RW</strong><br/></td>
<td>Esta marca opcional Especifica que los LUN de instantánea deben ser de lectura y escritura cuando se interrumpa el conjunto de instantáneas.<br/>
<blockquote>
[!Note]<br />
Esta marca solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> No compatible.<br/></td>
</tr>
<tr class="even">
<td><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong><br/></td>
<td>Esta marca opcional especifica <a href="vssgloss-c.md"><em>instantáneas accesibles para el cliente</em></a>.<br/>
<blockquote>
[!Note]<br />
Esta marca solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script =</strong><em>archivo</em><strong>. cmd</strong><br/></td>
<td>Esta marca opcional genera un archivo CMD que contiene variables de entorno relacionadas con las instantáneas creadas, como identificadores de instantáneas e identificadores de conjuntos de instantáneas.<br/></td>
</tr>
<tr class="even">
<td><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>File</em><strong>. XML</strong><br/></td>
<td>Esta marca opcional especifica las instantáneas transportables y almacena el documento de componentes de copia de seguridad en el archivo especificado por el parámetro <em>File.xml</em> . Este archivo se puede usar en una operación de importación o restauración posterior. Esta marca y la marca <strong>-BC</strong> se excluyen mutuamente.<br/> <strong>Windows server 2003, Standard Edition y Windows server 2003, Web Edition:</strong> No se admiten las instantáneas transportables. Todas las ediciones de Windows Server 2003 con Service Pack 1 (SP1) admiten instantáneas transportables.<br/></td>
</tr>
<tr class="odd">
<td><span id="-tr"></span><span id="-TR"></span><strong>-TR</strong><br/></td>
<td>Esta marca opcional Especifica que la recuperación de TxF debe aplicarse durante la creación de la instantánea.<br/>
<blockquote>
[!Note]<br />
Esta marca solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-tracing"></span><span id="-TRACING"></span><strong>-seguimiento</strong><br/></td>
<td>Esta marca opcional genera una salida detallada que se puede usar para solucionar problemas.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wait"></span><span id="-WAIT"></span><strong>-Wait</strong><br/></td>
<td>Esta marca opcional hace que la herramienta VShadow espere la confirmación del usuario antes de salir.<br/></td>
</tr>
<tr class="even">
<td><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-Wi =</strong><em>redactor</em><br/></td>
<td>Esta marca opcional comprueba que el escritor o componente especificado se incluye en la instantánea. El <em>escritor</em> puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor. Esta marca y la marca <strong>-NW</strong> son mutuamente excluyentes.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-WX =</strong><em>redactor</em><br/></td>
<td>Esta marca opcional comprueba que el escritor o componente especificado está excluido de la instantánea. El <em>escritor</em> puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor. Esta marca y la marca <strong>-NW</strong> son mutuamente excluyentes.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a>Importar un conjunto de instantáneas

**vshadow** \[ OptionalFlags \] **-i =**_archivo_*_. XML_*

La opción de línea de comandos **-i** importa un conjunto de instantáneas transportables.

> [!Note]  
> Esta opción de línea de comandos solo se admite en sistemas operativos Windows Server.

 

El archivo de *File.xml* debe ser un archivo de documento de componentes de copia de seguridad para un conjunto de instantáneas transportables creado con la marca opcional **-t** o **-BC** .

Un conjunto de instantáneas es una [*instantánea persistente*](vssgloss-p.md) si se creó con la marca opcional **-p** . Si el conjunto de instantáneas transportables es no persistente, aparece durante un breve período de tiempo mientras se ejecuta el comando de creación de instantáneas y se elimina automáticamente cuando el comando vuelve. Puede importar instantáneas no persistentes solo durante la creación de instantáneas mediante la creación del conjunto de instantáneas mediante la marca opcional **-exec** para ejecutar un archivo CMD que llama a VShadow **-i**.

La opción de línea de comandos **-i** no se puede combinar con otras opciones de la línea de comandos.

*OptionalFlags* es una máscara de máscara de valores de marca opcionales de la tabla siguiente.



| Valor opcional de marca                                                                                                            | Descripción                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_comando_<br/> | Esta marca opcional ejecuta un comando o script después de la importación de las instantáneas, pero antes de que se cierre la herramienta VShadow. El *comando* puede especificar un comando de Shell ejecutable o un archivo CMD. Si especifica un comando de Shell, no se puede especificar ningún parámetro de comando.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-seguimiento**<br/>                                                  | Esta marca opcional genera una salida detallada que se puede usar para solucionar problemas.<br/>                                                                                                                                                                                 |
| <span id="-wait"></span><span id="-WAIT"></span>**-Wait**<br/>                                                           | Esta marca opcional hace que la herramienta VShadow espere la confirmación del usuario antes de salir.<br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a>Consultar propiedades de instantáneas

**vshadow** **-q**

**vshadow** **-QX =**_ShadowCopySetId_

**vshadow** **-s =**_ShadowCopyId_

La opción de línea de comandos **-q** muestra las propiedades de todas las instantáneas del equipo.

La opción de línea de comandos **-QX** muestra las propiedades de todas las instantáneas del conjunto de instantáneas cuyo identificador se especifica mediante *ShadowCopySetId*.

La opción de línea de comandos **-s** muestra las propiedades de la instantánea cuyo identificador se especifica mediante *ShadowCopyId*.

Estas opciones de línea de comandos usan una combinación de [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) y [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) para obtener las propiedades del conjunto de instantáneas especificado.

Las opciones de línea de comandos **-q**, **-QX** y **-s** se excluyen mutuamente y no se pueden combinar con otras opciones de la línea de comandos.

## <a name="deleting-shadow-copies"></a>Eliminar instantáneas

**vshadow** **-da**

**vshadow** **-do**

**vshadow** **-DX =**_ShadowCopySetId_

**vshadow** **-DS =**_ShadowCopyId_

El comando **-da** elimina todas las instantáneas del equipo.

> [!Note]  
> La opción de línea de comandos **-da** requiere la confirmación del usuario.

 

La opción **de línea de comandos-do** elimina la instantánea más antigua del equipo.

La opción de línea de comandos **-DX** elimina todas las instantáneas del conjunto de instantáneas cuyo identificador se especifica mediante *ShadowCopySetId*.

La opción de línea de comandos **-DS** elimina la instantánea cuyo identificador se especifica mediante *ShadowCopyId*.

Estas opciones de línea de comandos solo se usan con [*instantáneas persistentes*](vssgloss-p.md) . No es necesario eliminar de forma explícita las instantáneas no persistentes, ya que se eliminan automáticamente cuando se cierra el comando de creación de VShadow.

Las opciones de línea de comandos **-da**, **-do**, **-DX** y **-DS** se excluyen mutuamente y no se pueden combinar con otras opciones de la línea de comandos.

## <a name="breaking-a-shadow-copy-set"></a>Dividir un conjunto de instantáneas

**vshadow** **-b =**_ShadowCopySetId_

**vshadow** **-BW =**_ShadowCopySetId_

La opción de línea de comandos **-b =**_ShadowCopySetId_ convierte cada instantánea del conjunto de instantáneas en un volumen independiente de solo lectura.

La opción de línea de comandos **-BW =**_ShadowCopySetId_ convierte cada instantánea del conjunto de instantáneas en un volumen grabable independiente.

> [!Note]  
> Las opciones de línea de comandos **-b** y **-BW** solo se admiten en sistemas operativos Windows Server.

 

Para obtener información acerca de cómo dividir un conjunto de instantáneas, consulte [romper instantáneas](breaking-shadow-copies.md).

Una vez interrumpido el conjunto de instantáneas, el conjunto de instantáneas y las instantáneas individuales ya no existen y no se pueden administrar mediante comandos de VSS.

Un conjunto de instantáneas es persistente si se creó con la marca opcional **-p** . Si el conjunto de instantáneas transportables es no persistente, aparece durante un breve período de tiempo mientras se ejecuta el comando de creación de instantáneas y se elimina automáticamente cuando el comando vuelve. Puede romper los conjuntos de instantáneas no persistentes solo durante la creación de instantáneas mediante la creación del conjunto de instantáneas mediante la marca opcional **-exec** para ejecutar un archivo CMD que llama a **vshadow** **-b** o **vshadow** **-BW**.

Las opciones de línea de comandos **-b** y **-BW** se excluyen mutuamente y no se pueden combinar con otras opciones de la línea de comandos.

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a>Dividir un conjunto de instantáneas mediante el método BreakSnapshotSetEx

**vshadow** **-BEX**

La opción de línea de comandos **-BEX** divide un conjunto de instantáneas según las opciones especificadas por las marcas opcionales **-Mask**, **-RW**, **-forcerevert** y **-norevert** . Esta opción de línea de comandos es similar a las opciones de línea de comandos **-b** y **-BW** . La opción de línea de comandos **-BEX** usa el método [**IVssBackupComponentsEx2:: BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) , mientras que las opciones de línea de comandos **-b** y **-BW** usan el método [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .

Para obtener información acerca de cómo dividir un conjunto de instantáneas, consulte [romper instantáneas](breaking-shadow-copies.md).

> [!Note]  
> La opción de línea de comandos **-BEX** solo se admite en sistemas operativos Windows Server.

 

**vshadow** **-BEX** **-Mask**

La marca **-Mask** especifica que el LUN de instantáneas se enmascarará desde el host. Si se especifica la marca **-Mask** , no se pueden especificar las marcas **-RW**, **-forcerevert** y **-norevert** .

**vshadow** **-BEX** **-RW**

La marca **-RW** especifica que el LUN de instantáneas se expondrá al host como un volumen de lectura/escritura.

**vshadow** **-BEX** **-forcerevert**

La marca **-forcerevert** especifica que los identificadores de disco de todos los LUN de instantánea se revertirán a los de los LUN originales. Sin embargo, si alguno de los LUN originales está presente en el sistema, se producirá un error en la operación y no se revertirá ninguno de los identificadores. Esta marca y la marca **-norevert** son mutuamente excluyentes.

**vshadow** **-BEX** **-norevert**

La marca **-norevert** especifica que no se revertirá ninguno de los identificadores de disco LUN de instantánea. Esta marca y la marca **-forcerevert** son mutuamente excluyentes.

## <a name="exposing-a-shadow-copy-locally"></a>Exponer una instantánea localmente

**vshadow** **-el =**_ShadowCopyId_*_,_*_LocalEmptyDirectory_

 **vshadow** **-el =**_ShadowCopyId_*_,_*_UnusedDriveLetter_

La opción de línea de comandos **-** el asigna una carpeta montada o una letra de unidad a una instantánea persistente. Tenga en cuenta que el contenido del volumen seguirá siendo de solo lectura, a menos que llame a **vshadow** **-BW** posteriormente para interrumpir el conjunto de instantáneas.

> [!Note]  
> Las instantáneas no persistentes y las [*instantáneas accesibles para el cliente*](vssgloss-c.md) no se pueden exponer localmente.

 

Por ejemplo, si {edbed95e-7e8d-11d8-9d01-505054503030} es el GUID de una instantánea persistente existente y X: es una letra de unidad no utilizada, el siguiente comando expone la instantánea en X:

**vshadow** **-el = {edbed95e-7e8d-11d8-9d01-505054503030}, x:**

En el ejemplo siguiente se muestra cómo exponer la misma instantánea en la carpeta montada C: \\ ShadowCopies \\ June23:

**mkdir c: \\ ShadowCopies \\ June23**

**vshadow** **-el = {edbed95e-7e8d-11d8-9d01-505054503030}, c: \\ ShadowCopies \\ June23**

La opción de línea de comandos **-** el no puede combinarse con otras opciones de la línea de comandos.

## <a name="exposing-a-shadow-copy-remotely"></a>Exponer una instantánea de forma remota

**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_

 **vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_

La opción de línea de comandos **-er** asigna un nombre de recurso compartido de solo lectura al directorio raíz (o un subdirectorio) de la instantánea. Tenga en cuenta que el contenido del recurso compartido seguirá siendo de solo lectura, a menos que llame posteriormente a **vshadow** **-BW** para interrumpir el conjunto de instantáneas.

> [!Note]  
> Las [*instantáneas accesibles para el cliente*](vssgloss-c.md) no se pueden exponer de forma remota.

 

Por ejemplo, si {edbed95e-7e8d-11d8-9d01-505054503030} es el GUID de una instantánea persistente existente y el recurso compartido \_ 123 es un nombre de recurso compartido sin usar, el siguiente comando expone la instantánea en share \_ 123:

**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}, recurso compartido \_ 123**

En el ejemplo siguiente se muestra cómo exponer solo un subárbol (denominado "Folder1 \\ Carpeta2") de la misma instantánea en el mismo recurso compartido:

**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}, recurso compartido \_ 123, carpeta1 \\ Carpeta2**

La opción de línea de comandos **-er** no se puede combinar con otras opciones de la línea de comandos.

## <a name="listing-writer-status-and-metadata"></a>Enumerar el estado y los metadatos del escritor

**vshadow** **-WS**

**vshadow** **-WM**

**vshadow** **-wm2**

**vshadow** **-wm3**

La opción de línea de comandos **-WS** enumera los escritores de VSS que se están ejecutando actualmente en el equipo y describe su estado. Este comando es el equivalente del comando [vssadmin List Writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) . Hay seis valores de estado posibles: estable, con errores, desconocido, en espera de inmovilización, congelada y en espera de finalización.

La opción de línea de comandos **-WM** muestra un resumen de los metadatos del escritor, incluidos los volúmenes afectados.

La opción de línea de comandos **-wm2** enumera todos los metadatos del escritor.

La opción de línea de comandos **-wm3** enumera todos los metadatos del escritor en formato XML sin formato.

**Windows Vista y Windows Server 2003:** No se admite la opción de línea de comandos **-wm3** .

Puede usar esta información para determinar qué volúmenes se van a incluir en el conjunto de instantáneas de volumen.

> [!Note]  
> Si el estado del escritor es estable o está esperando a la finalización, se puede considerar que el escritor está en un estado estable, listo para la siguiente copia de seguridad.

 

Las opciones **de línea de comandos-WS**, **-WM**, **-wm2** y **-wm3** se excluyen mutuamente y no se pueden combinar con otras opciones de la línea de comandos.

## <a name="performing-restore-operations"></a>Realización de operaciones de restauración

**vshadow** \[ OptionalFlags \] **-r =**_archivo_*_. XML_*

**vshadow** \[ OptionalFlags \] **-RS =**_archivo_*_. XML_*

La opción de línea de comandos **-r** realiza una operación de restauración.

La opción de línea de comandos **-RS** realiza una operación de restauración simulada.

El archivo de *File.xml* debe ser un archivo de documento de componentes de copia de seguridad para un conjunto de instantáneas creado con la marca opcional **-t** o **-BC** .

Las opciones de línea de comandos **-r** y **-RS** se excluyen mutuamente y no se pueden combinar con otras opciones de la línea de comandos.

*OptionalFlags* es una máscara de máscara de valores de marca opcionales de la tabla siguiente.



| Valor opcional de marca                                                                                                            | Descripción                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-Wi =**_redactor_<br/>             | Esta marca opcional comprueba que el escritor o componente especificado está incluido en la restauración. El *escritor* puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor.<br/>                                                                                    |
| <span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-WX =**_redactor_<br/>             | Esta marca opcional comprueba que el escritor o componente especificado se excluya de la restauración. El *escritor* puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor.<br/>                                                                                  |
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_comando_<br/> | Esta marca opcional ejecuta un comando o un script entre los eventos previos y posteriores a la restauración que se envían a los escritores. El *comando* puede especificar un comando de Shell ejecutable o un archivo CMD. Si especifica un comando de Shell, no se puede especificar ningún parámetro de comando.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-seguimiento**<br/>                                                  | Esta marca opcional genera una salida detallada que se puede usar para solucionar problemas.<br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a>Revertir a una instantánea anterior

**vshadow** **-Revert =**_ShadowCopyId_

> [!Note]  
> Esta opción de línea de comandos solo se admite en sistemas operativos Windows Server.

 

**Windows server 2008 y Windows server 2003:** No compatible.

La opción de línea de comandos **-Revert** revierte un volumen a la instantánea anterior cuyo identificador se especifica mediante *ShadowCopyId*.

La opción de línea de comandos **-Revert** no se puede combinar con otras opciones de la línea de comandos.

## <a name="resynchronizing-luns"></a>Volver a sincronizar LUN

**vshadow** **-addresync =**_ShadowCopyId_ **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]

**vshadow** **-addresync =**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]

La opción de línea de comandos **-addresync** especifica los volúmenes que se van a incluir en una operación de resincronización de LUN. El parámetro *ShadowCopyId* especifica el identificador de la instantánea. El parámetro opcional *TargetVolumeDriveLetter* especifica el volumen de destino en el que se copiará el contenido del volumen de instantáneas.

La opción de línea de comandos **-Resync** inicia una operación de resincronización de LUN. Una vez completada la operación, la firma de cada LUN de destino debe ser idéntica a la del LUN de volumen de destino. El parámetro *BCDFileName* especifica el nombre del archivo XML que contiene el documento del componente de copia de seguridad.

> [!Note]  
> Las opciones de línea de comandos **-addresync** y **-Resync** solo se admiten en sistemas operativos Windows Server.

 

**Windows server 2008 y Windows server 2003:** No compatible.

*OptionalResyncFlags* es una máscara de máscara de valores de marca opcionales de la tabla siguiente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor opcional de marca</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong><br/></td>
<td>Esta marca opcional Especifica que, una vez completada la operación, la firma de cada LUN de destino debe ser idéntica a la del LUN original que se usó para crear la instantánea, no el LUN de volumen de destino.<br/>
<blockquote>
[!Note]<br />
La marca <strong>-revertsig</strong> solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/> <strong>Windows server 2008 y Windows server 2003:</strong> No compatible.<br/></td>
</tr>
<tr class="even">
<td><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong><br/></td>
<td>Esta marca opcional Especifica que el servicio VSS no debe comprobar si hay volúmenes no seleccionados que se sobrescribirán con la operación de resincronización de LUN.<br/>
<blockquote>
[!Note]<br />
La marca <strong>-novolcheck</strong> solo se admite en sistemas operativos Windows Server.
</blockquote>
<br/> <strong>Windows server 2008 y Windows server 2003:</strong> No compatible.<br/></td>
</tr>
</tbody>
</table>



 

 

 
