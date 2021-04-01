---
description: La tabla componente enumera los componentes de y tiene las columnas siguientes.
ms.assetid: 069d64e9-106a-42b7-8dea-a44fc0c6e0cd
title: Tabla de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b721996767fa98209f0e13530f8f1bb1ba8cca07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275762"
---
# <a name="component-table"></a>Tabla de componentes

La tabla componente enumera los componentes de y tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente   | [Identificador](identifier.md) | Y   | N        |
| ComponentId | [GUID](guid.md)             | N   | Y        |
| Directorio\_ | [Identificador](identifier.md) | N   | N        |
| Atributos  | [Entero](integer.md)       | N   | N        |
| Condición   | [Condition](condition.md)   | N   | Y        |
| Rutas     | [Identificador](identifier.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Pone
</dt> <dd>

Identifica el registro del componente.

Clave de la tabla principal.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

GUID de cadena único para este componente, versión e idioma.

Tenga en cuenta que las letras de estos GUID deben estar en mayúsculas. Las utilidades como GUIDGEN pueden generar GUID que contienen letras minúsculas. Las letras minúsculas se deben cambiar a mayúsculas para crear estos GUID de código de componente válidos.

Si esta columna es null, el instalador no registra el componente y el instalador no puede quitar ni reparar el componente. Esto puede hacerse intencionadamente si el componente solo es necesario durante la instalación, por ejemplo, una acción personalizada que limpie los archivos temporales o quite un producto antiguo. También puede ser útil cuando se copian archivos de datos en el equipo de un usuario que no es necesario registrar.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_
</dt> <dd>

Clave externa de una entrada en la [tabla de directorio](directory-table.md). Se trata de un nombre de propiedad cuyo valor contiene la ruta de acceso real, que se puede establecer mediante la [acción AppSearch](appsearch-action.md) o con la configuración predeterminada obtenida de la tabla de directorio.

Los desarrolladores deben evitar la creación de componentes que colocan archivos en una de las carpetas de Perfil de usuario. Estos archivos no estarán disponibles para todos los usuarios en situaciones de varios usuarios y podrían hacer que el instalador ver de forma permanente el componente como un requisito de reparación.

Clave externa para la columna uno de la tabla de directorio.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus
</dt> <dd>

Esta columna contiene una marca de bits que especifica las opciones para la ejecución remota. Agregue el bit indicado al valor total de la columna para incluir una opción.

> [!Note]  
> En el caso de un archivo. msi que se está descargando de una ubicación Web, no se deben establecer marcas de atributo para permitir que un componente se ejecute desde el origen. Se trata de una limitación del Windows Installer y puede devolver el estado de una característica de INSTALLSTATE \_ BADCONFIG.

 



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Marca de bits</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesLocalOnly</strong></dt> <dt>0</dt> <dt>0x0000</dt> </dl> No se puede ejecutar el componente desde el origen. Establezca este bit para todos los componentes que pertenecen a una característica para impedir que la característica se ejecute desde la red o desde el origen de ejecución. Tenga en cuenta que si una característica no tiene componentes, la característica siempre muestra las opciones ejecutar desde el origen y ejecutar desde mi equipo como válidas.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesSourceOnly</strong></dt> <dt>1</dt> <dt>0x0001</dt> </dl> El componente solo se puede ejecutar desde el origen. Establezca este bit para todos los componentes que pertenecen a una característica para impedir que se ejecute la característica desde el equipo. Tenga en cuenta que si una característica no tiene componentes, la característica siempre muestra las opciones ejecutar desde el origen y ejecutar desde mi equipo como válidas.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesOptional</strong></dt> <dt>2</dt> <dt>0x0002</dt> </dl> El componente se puede ejecutar localmente o desde el origen.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesRegistryKeyPath</strong></dt> <dt>4</dt> <dt>0x0004</dt> </dl> Si se establece este bit, el valor de la columna de ruta de clave se utiliza como clave en la <a href="registry-table.md">tabla del registro</a>. Si el campo de valor del registro correspondiente en la tabla del registro es null, el campo de nombre de ese registro no debe contener &quot; + &quot; , &quot; - &quot; o &quot; * &quot; . Para obtener más información, vea la descripción del campo nombre en la <a href="registry-table.md">tabla del registro</a>.<br/> Se recomienda establecer este bit para las entradas del registro escritas en el subárbol HKCU. Esto garantiza que el instalador escriba las entradas del registro HKCU necesarias cuando haya varios usuarios en el mismo equipo.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesSharedDllRefCount</strong></dt> <dt>8</dt> <dt>0x0008</dt> </dl> Si se establece este bit, el instalador incrementa el recuento de referencias en el registro DLL compartido del archivo de clave del componente. Si no se establece este bit, el instalador incrementa el recuento de referencias solo si el recuento de referencias ya existe.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesPermanent</strong></dt> <dt>16</dt> <dt>0x0010</dt> </dl> Si se establece este bit, el instalador no quita el componente durante la desinstalación. El instalador registra un cliente del sistema adicional para el componente en la configuración del registro de Windows Installer.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesODBCDataSource</strong></dt> <dt>32</dt> <dt>0x0020</dt> </dl> Si se establece este bit, el valor de la columna de ruta de clave es una clave en la <a href="odbcdatasource-table.md">tabla ODBCDataSource</a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesTransitive</strong></dt> <dt>64</dt> <dt>0x0040</dt> </dl> Si se establece este bit, el instalador vuelve a evaluar el valor de la instrucción en la columna condición tras una reinstalación. Si el valor era previamente false y ha cambiado a true, el instalador instala el componente. Si el valor era previamente true y ha cambiado a false, el instalador quita el componente aunque el componente tenga otros productos como clientes.<br/> Este bit solo debe establecerse para componentes transitivos. Vea <a href="using-transitive-components.md">uso de componentes transitivos</a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesNeverOverwrite</strong></dt> <dt>128</dt> <dt>0x0080</dt> </dl> Si se establece este bit, el instalador no instala ni vuelve a instalar el componente si ya existe un archivo de ruta de acceso de clave o una entrada del registro de ruta de acceso de clave para el componente. La aplicación se registra como un cliente del componente.<br/> Use esta marca solo para los componentes que se registran en la tabla del registro. No use esta marca para los componentes registrados por las tablas <a href="appid-table.md">AppID</a>, <a href="class-table.md">Class</a>, <a href="extension-table.md">Extension</a>, <a href="progid-table.md">ProgID</a>, <a href="mime-table.md">MIME</a>y <a href="verb-table.md">Verb</a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributes64bit</strong></dt> <dt>256</dt> <dt>0x0100</dt> </dl> Establezca este bit para marcarlo como componente de 64 bits. Este atributo facilita la instalación de paquetes que incluyen componentes de 32 y de 64 bits. Si no se establece este bit, el componente se registra como un componente de 32 bits.<br/> Si se trata de un componente de 64 bits que reemplaza un componente de 32 bits, establezca este bit y asigne un nuevo GUID en la columna ComponentId.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesDisableRegistryReflection</strong></dt> <dt>512</dt> <dt>0x0200</dt> </dl> Establezca este bit para deshabilitar la <a href="/windows/desktop/WinProg64/registry-reflection">reflexión del registro</a> en todas las claves del registro nuevas y existentes afectadas por este componente. Si se establece este bit, el Windows Installer llama a <a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey"><strong>RegDisableReflectionKey</strong></a> en cada clave a la que tiene acceso el componente. Este bit está disponible con Windows Installer versión 4,0. Este bit se omite en los sistemas de 32 bits. Este bit se omite en las versiones de 64 bits de Windows XP.<br/>
<blockquote>
[!Note]<br />
las aplicaciones Windows de 32 bits que se ejecutan en el emulador de Windows de 64 bits (WOW64) hacen referencia a una vista diferente del registro que las aplicaciones de 64 bits. La reflexión del registro copia algunos valores del registro entre estas dos vistas del registro.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesUninstallOnSupersedence</strong></dt> <dt>1024</dt> <dt>0x0400</dt> </dl> Establezca este bit para un componente de un paquete de revisión para evitar que los componentes huérfanos dejen de estar en el equipo. Si se instala una revisión posterior, marcada con el valor <strong>msidbPatchSequenceSupersedeEarlier</strong> en su tabla <a href="msipatchsequence-table.md">MsiPatchSequence</a> para sustituir la primera revisión, Windows Installer 4,5 y versiones posteriores pueden anular el registro y desinstalar los componentes marcados con el valor <strong>msidbComponentAttributesUninstallOnSupersedence</strong> . Si el componente no está marcado con este bit, la instalación de una revisión de sustitución puede dejar detrás de un componente no utilizado en el equipo.<br/> Establecer la propiedad <strong>MSIUNINSTALLSUPERSEDEDCOMPONENTS</strong> tiene el mismo efecto que establecer este bit para todos los componentes.<br/> <strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4,0 y versiones anteriores</a>:</strong> no se admite el valor <strong>msidbComponentAttributesUninstallOnSupersedence</strong> y se omite.<br/> <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesShared</strong></dt> <dt>2048</dt> <dt>0x0800</dt> </dl> Si un componente está marcado con este valor de atributo en al menos un paquete instalado en el sistema, el instalador trata el componente como marcado en todos los paquetes. Si se desinstala un paquete que comparte el componente marcado, Windows Installer 4,5 puede seguir compartiendo la versión más alta del componente en el sistema, incluso si el paquete que se está desinstalando instaló la versión más reciente. <br/> Si la Directiva DisableSharedComponent se establece en 1, ningún paquete obtiene la funcionalidad del componente compartido habilitada por este bit.<br/> <strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4,0 y versiones anteriores</a>:</strong> no se admite el valor <strong>msidbComponentAttributesShared</strong> y se omite.<br/> <br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple
</dt> <dd>

Esta columna contiene una instrucción condicional que puede controlar si un componente está instalado. Si la condición es null o se evalúa como true, el componente está habilitado. Si la condición se evalúa como false, el componente está deshabilitado y no está instalado.

El campo condición habilita o deshabilita un componente solo durante la [acción CostFinalize](costfinalize-action.md). Para habilitar o deshabilitar un componente después de CostFinalize, debe usar una acción personalizada o la [ControlEvent, de acción](doaction-controlevent.md) para llamar a [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea).

Tenga en cuenta que, a menos que se establezca el bit transitivo en la columna Attributes para un componente, el componente permanece habilitado una vez instalado, incluso si la instrucción condicional de la columna condition se evalúa posteriormente como false en una instalación de mantenimiento posterior del producto.

La columna condición de la tabla componente acepta expresiones condicionales que contienen referencias a los Estados instalados de características y componentes. Para obtener información sobre la sintaxis de las instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).

</dd> <dt>

<span id="KeyPath"></span><span id="keypath"></span><span id="KEYPATH"></span>Rutas
</dt> <dd>

Este valor apunta a un archivo o carpeta que pertenece al componente que el instalador usa para detectar el componente. Dos componentes no pueden compartir el mismo valor de ruta de acceso de clave. El valor de esta columna también es la ruta de acceso devuelta por la función [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .

Si el valor no es null, la ruta de acceso de la ruta de acceso es una clave principal en las tablas [Registry](registry-table.md), [ODBCDataSource](odbcdatasource-table.md)o [File](file-table.md) , dependiendo del valor del atributo. Si la ruta de acceso de la clave es null, la carpeta de la columna de directorio \_ se usa como la ruta de acceso de la clave.

Dado que las carpetas creadas por el instalador se eliminan cuando están vacías, debe crear una entrada en la [tabla CreateFolder](createfolder-table.md) para instalar un componente que se compone de una carpeta vacía.

Tenga en cuenta que si un componente de Windows Installer contiene un archivo o una clave del registro que está protegida por [protección de recursos de Windows](/windows/desktop/Wfp/windows-resource-protection-portal) (WRP) o un archivo protegido por protección de archivos de Windows (WFP), este recurso debe usarse como la ruta de acceso clave del componente. En este caso, Windows Installer no instala, actualiza o quita el componente. No debe incluir ningún recurso protegido en un paquete de instalación. En su lugar, debe usar los [mecanismos de sustitución de recursos admitidos](/windows/desktop/Wfp/supported-file-replacement-mechanisms) para protección de recursos de Windows. Para obtener más información, vea [usar Windows Installer y protección de recursos de Windows](windows-resource-protection-on-windows-vista.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener una explicación de la relación entre los componentes y las características, consulte [tabla de características](feature-table.md).

El instalador realiza un seguimiento de los archivos dll compartidos independientemente del recuento de referencias de DLL compartidas en el registro. Si existe un recuento de referencias para un archivo DLL compartido en el registro, el instalador siempre incrementa el recuento cuando está instalando el archivo y lo reduce cuando se está desinstalando. Si no se establece **msidbComponentAttributesSharedDllRefCount**, y el recuento de referencias aún no existe, el instalador no creará uno. Tenga en cuenta que el recuento de referencias de SharedDLLs en el registro se incrementa para los archivos instalados en la carpeta del sistema.

Si no se establece **msidbComponentAttributesSharedDllRefCount** , otra aplicación puede quitar el componente aunque siga siendo necesario. Para ver cómo podría suceder esto, considere el siguiente escenario:

-   Una aplicación que usa el instalador instala un componente compartido.
-   No se ha establecido el bit **msidbComponentAttributesSharedDllRefCount** y no hay ningún recuento de referencias. Por lo tanto, el instalador no comienza un recuento de referencias.
-   Se instala una aplicación heredada que comparte este componente y no usa el instalador.
-   La aplicación heredada crea e incrementa un recuento de referencias para el componente compartido.
-   Se desinstalará la aplicación heredada.
-   El recuento de referencias del componente compartido se reduce a cero y se quita el componente.
-   La aplicación que usa el instalador ya no tiene acceso al componente.

Para evitar este comportamiento, establezca **msidbComponentAttributesSharedDllRefCount**.

Tenga en cuenta que los componentes de servicios del sistema no se deben especificar como ejecutar desde el origen sin diseñarse específicamente para ese uso. Consulte la [tabla ServiceInstall](serviceinstall-table.md) para obtener más detalles.

Tenga en cuenta que los atributos que habilitan la instalación desde código fuente no deben establecerse nunca para los componentes que contienen bibliotecas de vínculos dinámicos que van a la carpeta del sistema. La razón es que si el estado de la instalación del componente se establece en ejecutar desde código fuente siguiendo una característica o se establece en la interfaz de usuario, se producirá un error en las llamadas subsiguientes a **LoadLibrary** en el archivo dll.

Vea también [control de los Estados de selección de características](controlling-feature-selection-states.md).

## <a name="validation"></a>Validación

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE08](ice08.md)  
[ICE09](ice09.md)  
[ICE18](ice18.md)  
[ICE19](ice19.md)  
[ICE21](ice21.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE38](ice38.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE54](ice54.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE76](ice76.md)  
[ICE79](ice79.md)  
[ICE80](ice80.md)  
[ICE83](ice83.md)  
[ICE86](ice86.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE92](ice92.md)  
[ICE97](ice97.md)  
</dl>

