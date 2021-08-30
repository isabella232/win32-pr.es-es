---
description: En la tabla Component se enumeran los componentes y tiene las columnas siguientes.
ms.assetid: 069d64e9-106a-42b7-8dea-a44fc0c6e0cd
title: Tabla de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1888628137fcf07cab07d011325ff685809cff68
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474951"
---
# <a name="component-table"></a>Tabla de componentes

En la tabla Component se enumeran los componentes y tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente   | [Identificador](identifier.md) | Y   | No        |
| Componentid | [GUID](guid.md)             | No   | Y        |
| Directorio\_ | [Identificador](identifier.md) | No   | No        |
| Atributos  | [Entero](integer.md)       | No   | No        |
| Condición   | [Condition](condition.md)   | No   | Y        |
| KeyPath     | [Identificador](identifier.md) | No   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Componente
</dt> <dd>

Identifica el registro del componente.

Clave de tabla principal.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>Componentid
</dt> <dd>

GUID de cadena único para este componente, versión e idioma.

Tenga en cuenta que las letras de estos GUID deben estar en mayúsculas. Utilidades como GUIDGEN pueden generar GUID que contengan letras minúsculas. Las letras minúsculas deben cambiarse a mayúsculas para que estos GUID de código de componente sean válidos.

Si esta columna es NULL, el instalador no registra el componente y el instalador no puede quitarlo ni repararlo. Esto puede hacerse intencionadamente si el componente solo es necesario durante la instalación, como una acción personalizada que limpia los archivos temporales o quita un producto antiguo. También puede ser útil al copiar archivos de datos en el equipo de un usuario que no es necesario registrar.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directorio\_
</dt> <dd>

Clave externa de una entrada en la [tabla Directory](directory-table.md). Se trata de un nombre de propiedad cuyo valor contiene la ruta de acceso real, que se puede establecer mediante la acción [AppSearch](appsearch-action.md) o con la configuración predeterminada obtenida de la tabla Directory.

Los desarrolladores deben evitar la creación de componentes que coloquen archivos en una de las carpetas de perfil de usuario. Estos archivos no estarían disponibles para todos los usuarios en situaciones de varios usuarios y podrían hacer que el instalador vea permanentemente el componente como que requiere reparación.

Clave externa para la columna uno de la tabla Directory.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Esta columna contiene una marca de bits que especifica las opciones para la ejecución remota. Agregue el bit indicado al valor total de la columna para incluir una opción.

> [!Note]  
> En el caso de un archivo .msi que se descarga desde una ubicación web, las marcas de atributo no deben establecerse para permitir que un componente se ejecute desde el origen. Se trata de una limitación del instalador Windows y puede devolver un estado de característica de INSTALLSTATE \_ BADCONFIG.

 




| Marca de bits | 
|----------|
| <dl><dt><strong>msidbComponentAttributesLocalOnly</strong></dt><dt>0</dt><dt>0x0000</dt></dl> El componente no se puede ejecutar desde el origen. Establezca este bit para todos los componentes que pertenecen a una característica para evitar que la característica se ejecute desde la red o desde el origen. Tenga en cuenta que si una característica no tiene componentes, la característica siempre muestra run-from-source y run-from-my-computer como opciones válidas.<br /> | 
| <dl><dt><strong>msidbComponentAttributesSourceOnly</strong></dt><dt>1</dt><dt>0x0001</dt></dl> El componente solo se puede ejecutar desde el origen. Establezca este bit para todos los componentes que pertenecen a una característica para evitar que la característica se ejecute desde mi equipo. Tenga en cuenta que si una característica no tiene componentes, la característica siempre muestra run-from-source y run-from-my-computer como opciones válidas.<br /> | 
| <dl><dt><strong>msidbComponentAttributesOpciones</strong></dt><dt>2</dt><dt>0x0002</dt></dl> El componente se puede ejecutar localmente o desde el origen.<br /> | 
| <dl><dt><strong>msidbComponentAttributesRegistryKeyPath</strong></dt><dt>4</dt><dt>0x0004</dt></dl> Si se establece este bit, el valor de la columna KeyPath se usa como clave en la <a href="registry-table.md">tabla del Registro</a>. Si el campo Valor del registro correspondiente de la tabla del Registro es NULL, el campo Nombre de ese registro no debe contener "+", "-" o "*". Para obtener más información, vea la descripción del campo Nombre de la <a href="registry-table.md">tabla del Registro</a>.<br /> Se recomienda establecer este bit para las entradas del Registro escritas en el subárbol HKCU. Esto garantiza que el instalador escribe las entradas del Registro HKCU necesarias cuando hay varios usuarios en el mismo equipo.<br /> | 
| <dl><dt><strong>msidbComponentAttributesSharedDllRefCount</strong></dt><dt>8</dt><dt>0x0008</dt></dl> Si se establece este bit, el instalador incrementa el recuento de referencias en el registro DLL compartido del archivo de clave del componente. Si no se establece este bit, el instalador incrementa el recuento de referencias solo si el recuento de referencias ya existe.<br /> | 
| <dl><dt><strong>msidbComponentAttributesPermanent</strong></dt><dt>16</dt><dt>0x0010</dt></dl> Si se establece este bit, el instalador no quita el componente durante una desinstalación. El instalador registra un cliente del sistema adicional para el componente en la Windows del Registro del instalador.<br /> | 
| <dl><dt><strong>msidbComponentAttributesODBCDataSource</strong></dt><dt>32</dt><dt>0x0020</dt></dl> Si se establece este bit, el valor de la columna KeyPath es una clave en la <a href="odbcdatasource-table.md">tabla ODBCDataSource</a>.<br /> | 
| <dl><dt><strong>msidbComponentAttributesTransitive</strong></dt><dt>64</dt><dt>0x0040</dt></dl> Si se establece este bit, el instalador vuelve a evaluar el valor de la instrucción en la columna Condición tras una reinstalación. Si el valor era false anteriormente y ha cambiado a True, el instalador instala el componente. Si el valor era true anteriormente y ha cambiado a False, el instalador quita el componente incluso si el componente tiene otros productos como clientes.<br /> Este bit solo debe establecerse para componentes transitivos. Consulte <a href="using-transitive-components.md">Uso de componentes transitivos.</a><br /> | 
| <dl><dt><strong>msidbComponentAttributesNeverOverwrite</strong></dt><dt>128</dt><dt>0x0080</dt></dl> Si se establece este bit, el instalador no instala ni reinstala el componente si ya existe un archivo de ruta de acceso de clave o una entrada del Registro de ruta de acceso de clave para el componente. La aplicación se registra como un cliente del componente.<br /> Use esta marca solo para los componentes que está registrando la tabla del Registro. No use esta marca para los componentes registrados por las tablas <a href="appid-table.md">AppId</a>, <a href="class-table.md">Class</a>, <a href="extension-table.md">Extension</a>, <a href="progid-table.md">ProgId</a>, <a href="mime-table.md">MIME</a>y <a href="verb-table.md">Verb</a>.<br /> | 
| <dl><dt><strong>msidbComponentAttributes64bit</strong></dt><dt>256</dt><dt>0x0100</dt></dl> Establezca este bit para marcarlo como un componente de 64 bits. Este atributo facilita la instalación de paquetes que incluyen componentes de 32 y 64 bits. Si no se establece este bit, el componente se registra como un componente de 32 bits.<br /> Si se trata de un componente de 64 bits que reemplaza a un componente de 32 bits, establezca este bit y asigne un nuevo GUID en la columna ComponentId.<br /> | 
| <dl><dt><strong>msidbComponentAttributesDisableRegistryReflection</strong></dt><dt>512</dt><dt>0x0200</dt></dl> Establezca este bit para deshabilitar la <a href="/windows/desktop/WinProg64/registry-reflection">reflexión del Registro</a> en todas las claves del Registro nuevas y existentes afectadas por este componente. Si se establece este bit, el Windows llama a <a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey"><strong>RegDisableReflectionKey</strong></a> en cada clave a la que tiene acceso el componente. Este bit está disponible con Windows Installer versión 4.0. Este bit se omite en sistemas de 32 bits. Este bit se omite en las versiones de 64 bits de Windows XP.<br /><blockquote>[!Note]<br />Las aplicaciones de Windows de 32 bits que se ejecutan en el emulador de Windows de 64 bits (WOW64) hacen referencia a una vista diferente del registro que las aplicaciones de 64 bits. La reflexión del Registro copia algunos valores del Registro entre estas dos vistas del Registro.</blockquote><br /><br /> | 
| <dl><dt><strong>msidbComponentAttributesUninstallOnSupersedence</strong></dt><dt>1024</dt><dt>0x0400</dt></dl> Establezca este bit para un componente en un paquete de revisión para evitar dejar componentes huérfanos en el equipo. Si se instala una revisión posterior, marcada con el valor <strong>msidbPatchSequenceSupersedeEarlier</strong> en su tabla <a href="msipatchsequence-table.md">MsiPatchSequence</a> para reemplazar la primera revisión, Windows Installer 4.5 y versiones posteriores pueden anular el registro y desinstalar los componentes marcados con el valor <strong>msidbComponentAttributesUninstallOnSupersedence.</strong> Si el componente no está marcado con este bit, la instalación de una revisión superseding puede dejar un componente no utilizado en el equipo.<br /> Establecer la <strong>propiedad MSIUNINSTALLSUPERSEDEDCOMPONENTS</strong> tiene el mismo efecto que establecer este bit para todos los componentes.<br /><strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4.0</a></strong> y versiones anteriores: no se admite el valor <strong>msidbComponentAttributesUninstallOnSupersedence</strong> y se omite.<br /><br /> | 
| <dl><dt><strong>msidbComponentAttributesShared</strong></dt><dt>2048</dt><dt>0x0800</dt></dl> Si un componente está marcado con este valor de atributo en al menos un paquete instalado en el sistema, el instalador trata el componente como marcado en todos los paquetes. Si se desinstala un paquete que comparte el componente marcado, Windows Installer 4.5 puede seguir compartiendo la versión más alta del componente en el sistema, incluso si el paquete que se está desinstalando instaló la versión más alta. <br /> Si la directiva DisableSharedComponent está establecida en 1, ningún paquete obtiene la funcionalidad de componente compartido habilitada por este bit.<br /><strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4.0</a></strong> y versiones anteriores: el valor <strong>msidbComponentAttributesShared</strong> no se admite y se omite.<br /><br /> | 




 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condición
</dt> <dd>

Esta columna contiene una instrucción condicional que puede controlar si un componente está instalado. Si la condición es NULL o se evalúa como true, el componente está habilitado. Si la condición se evalúa como False, el componente está deshabilitado y no está instalado.

El campo Condición habilita o deshabilita un componente solo durante la [acción CostFinalize](costfinalize-action.md). Para habilitar o deshabilitar un componente después de CostFinalize, debe usar una acción personalizada o [doAction ControlEvent](doaction-controlevent.md) para llamar a [**MsiSetComponentState.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)

Tenga en cuenta que, a menos que el bit transitivo de la columna Atributos esté establecido para un componente, el componente permanece habilitado una vez instalado, aunque la instrucción condicional de la columna Condición se evalúe posteriormente como False en una instalación de mantenimiento posterior del producto.

La columna Condición de la tabla Componente acepta expresiones condicionales que contienen referencias a los estados instalados de características y componentes. Para obtener información sobre la sintaxis de las instrucciones condicionales, vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

</dd> <dt>

<span id="KeyPath"></span><span id="keypath"></span><span id="KEYPATH"></span>KeyPath
</dt> <dd>

Este valor apunta a un archivo o carpeta que pertenece al componente que el instalador usa para detectar el componente. Dos componentes no pueden compartir el mismo valor de ruta de acceso de clave. El valor de esta columna también es la ruta de acceso devuelta por [**la función MsiGetComponentPath.**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)

Si el valor no es NULL, KeyPath es una clave principal en las tablas [Registry](registry-table.md), [ODBCDataSource](odbcdatasource-table.md)o [File](file-table.md) en función del valor attribute. Si KeyPath es NULL, la carpeta de la columna \_ Directory se usa como ruta de acceso de la clave.

Dado que las carpetas creadas por el instalador se eliminan cuando están vacías, debe crear una entrada en la [tabla CreateFolder](createfolder-table.md) para instalar un componente que consta de una carpeta vacía.

Tenga en cuenta que si un componente del instalador de Windows contiene un archivo o una clave del Registro que está protegido por [Windows Resource Protection](/windows/desktop/Wfp/windows-resource-protection-portal) (WRP) o un archivo protegido por Windows File Protection (WFP), este recurso debe usarse como KeyPath para el componente. En este caso, Windows instalador no instala, actualiza ni quita el componente. No debe incluir ningún recurso protegido en un paquete de instalación. En su lugar, debe usar los [mecanismos de reemplazo de recursos admitidos](/windows/desktop/Wfp/supported-file-replacement-mechanisms) para Windows Resource Protection. Para obtener más información, vea [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para obtener una explicación de la relación entre componentes y características, vea [Tabla de características](feature-table.md).

El instalador realiza un seguimiento de los archivos DLL compartidos independientemente del recuento de referencias dll compartidas en el Registro. Si existe un recuento de referencias para un archivo DLL compartido en el Registro, el instalador siempre incrementa el recuento cuando instala el archivo y lo disminuye cuando se desinstala. Si **msidbComponentAttributesSharedDllRefCount** no está establecido y el recuento de referencias aún no existe, el instalador no creará uno. Tenga en cuenta que el recuento de referencias de SharedDLLs en el Registro se incrementa para los archivos instalados en la carpeta System.

Si **msidbComponentAttributesSharedDllRefCount** no está establecido, otra aplicación puede quitar el componente incluso si sigue siendo necesario. Para ver cómo podría ocurrir esto, considere el siguiente escenario:

-   Una aplicación que usa el instalador instala un componente compartido.
-   El **bit msidbComponentAttributesSharedDllRefCount** no está establecido y no hay ningún recuento de referencias. Por lo tanto, el instalador no inicia un recuento de referencias.
-   Se instala una aplicación heredada que comparte este componente y no usa el instalador.
-   La aplicación heredada crea e incrementa un recuento de referencias para el componente compartido.
-   La aplicación heredada se desinstala.
-   El recuento de referencias del componente compartido se disminuye a cero y se quita el componente.
-   La aplicación que usa el instalador ya no tiene acceso al componente.

Para evitar este comportamiento, establezca **msidbComponentAttributesSharedDllRefCount**.

Tenga en cuenta que los componentes de servicios del sistema no deben especificarse como de ejecución desde el origen sin estar diseñados específicamente para ese uso. Consulte la [tabla ServiceInstall para](serviceinstall-table.md) obtener más detalles.

Tenga en cuenta que los atributos que habilitan la instalación desde el origen nunca deben establecerse para los componentes que contienen bibliotecas de vínculos dinámicos que van a la carpeta del sistema. El motivo es que, si el estado de instalación del componente se establece en run-from-source siguiendo una característica o estando establecido en la interfaz de usuario, se producirá un error en las llamadas posteriores a **LoadLibrary** en el archivo DLL.

Vea también Controlar [los estados de selección de características](controlling-feature-selection-states.md).

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

