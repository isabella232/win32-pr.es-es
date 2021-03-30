---
description: La tabla del registro contiene la información del registro que la aplicación necesita para establecer en el registro del sistema.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Tabla del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001870"
---
# <a name="registry-table"></a>Tabla del registro

La tabla del registro contiene la información del registro que la aplicación necesita para establecer en el registro del sistema.

La tabla del registro tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Registro    | [Identificador](identifier.md) | Y   | N        |
| Root        | [Entero](integer.md)       | N   | N        |
| Clave         | [RegPath](regpath.md)       | N   | N        |
| Nombre        | [Formatea](formatted.md)   | N   | Y        |
| Value       | [Formatea](formatted.md)   | N   | Y        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Del registro
</dt> <dd>

Clave principal que se usa para identificar un registro de registro.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Raíces
</dt> <dd>

Clave raíz predefinida para el valor del registro. Escriba un valor de-1 en este campo para que la clave raíz dependa del tipo de instalación. Escriba uno de los otros valores de la tabla siguiente para forzar que el valor del registro se escriba en una clave raíz determinada.



| Constante                          | Hexadecimal | Decimal | Clave raíz                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (ninguno)                            | \- 0x001    | -1      | Si se trata de una instalación por usuario, el valor del registro se escribe en **HKEY \_ Current \_ User**. Si se trata de una instalación por equipo, el valor del registro se escribe en **HKEY \_ local \_ Machine**. Tenga en cuenta que una instalación por equipo se especifica estableciendo la propiedad [**AllUsers**](allusers.md) en 1.<br/>                |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASES \_ raíz** el instalador escribe o quita el valor de la **\\ clase HKCU Software \\ classes** durante la instalación en el [contexto de instalación](installation-context.md)por usuario.<br/> El instalador escribe o quita el valor del subárbol **HKLM \\ software \\ classes** durante las instalaciones por máquina.<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ Current \_ User**                                                                                                                                                                                                                                                                                                                      |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ local \_ Machine**                                                                                                                                                                                                                                                                                                                     |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **\_usuarios HKEY**                                                                                                                                                                                                                                                                                                                              |



 

Tenga en cuenta que se recomienda que las entradas del registro escritas en el subárbol **HKCU** hagan referencia a un componente que tenga establecido el bit RegistryKeyPath en la columna Attributes de la [tabla de componentes](component-table.md). Esto garantiza que el instalador escriba las entradas del registro necesarias cuando haya varios usuarios en el mismo equipo.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

La clave localizable para el valor del registro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Esta columna contiene el nombre del valor del registro (localizable). Si es null, los datos especificados en la columna valor se escriben en la clave del registro predeterminada.

Si la columna valor es null, las cadenas que se muestran en la tabla siguiente en la columna nombre tienen una importancia especial.



| String | Significado                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | La clave se creará, si no está presente, cuando se instale el componente.                                                                                                                            |
| \-     | La clave se eliminará, si está presente, con todos sus valores y subclaves, cuando se desinstale el componente.                                                                                     |
| \*     | La clave se creará, si no está presente, cuando se instale el componente. Además, la clave se eliminará, si está presente, con todos sus valores y subclaves, cuando se desinstale el componente. |



 

Tenga en cuenta que se debe usar la [tabla RemoveRegistry](removeregistry-table.md) si se va a eliminar una clave del registro instalada, con sus valores y subclaves, cuando se instale el componente.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Esta columna es el valor del registro localizable. El campo tiene [formato](formatted.md). Si el valor se adjunta a uno de los siguientes prefijos (es decir, \# % *Value*), el valor se interpreta como se describe en la tabla. Tenga en cuenta que cada prefijo comienza con un signo de número ( \# ). Si el valor comienza con dos o más signos de número consecutivos ( \# ), el primero \# se omite y el valor se interpreta y se almacena como una cadena.



| Prefijo | Significado                                                                        |
|--------|--------------------------------------------------------------------------------|
| \#x1    | El valor se interpreta y se almacena como un valor hexadecimal (REG \_ binario).      |
| \#%    | El valor se interpreta y se almacena como una cadena expansible (REG \_ Expand \_ SZ). |
| \#     | El valor se interpreta y se almacena como un entero (REG \_ DWORD).                |



 

-   Si el valor contiene la tilde de la secuencia \[ ~ \] , el valor se interpreta como una lista de cadenas delimitada por null (REG \_ multi \_ SZ). Por ejemplo, para especificar una lista que contenga las tres cadenas a, b y c, use "a \[ ~ \] b \[ ~ \] c".
-   La secuencia \[ ~ \] dentro del valor separa las cadenas individuales y se interpreta y se almacena como un carácter nulo.
-   Si \[ ~ \] precede a la lista de cadenas, las cadenas se anexarán a cualquier cadena de valor del registro existente. Si ya hay una cadena anexada en el valor del registro, se quita la repetición original de la cadena.
-   Si \[ ~ \] después del final de la lista de cadenas, las cadenas se anteponen a cualquier cadena de valor del registro existente. Si ya hay una cadena anteponeda en el valor del registro, se quita la repetición original de la cadena.
-   Si \[ ~ \] se encuentra al principio y al final, o al principio o al final de la lista de cadenas, las cadenas van a reemplazar cualquier cadena de valor del registro existente.
-   De lo contrario, el valor se interpreta y se almacena como una cadena (REG \_ SZ).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa en la primera columna de la [tabla de componentes](component-table.md) que hace referencia al componente que controla la instalación del valor del registro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las acciones [WriteRegistryValues](writeregistryvalues-action.md) y [RemoveRegistryValues](removeregistryvalues-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla. Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).

La información del registro se escribe en el registro del sistema cuando se ha seleccionado el componente correspondiente para que se instale localmente o se ejecute desde el origen.

Tenga en cuenta que el instalador quita una clave del registro después de quitar el último valor o subclave de la clave. Para evitar que se quite una clave del Registro vacía al desinstalar, escriba un valor ficticio en la clave que necesita mantener y escriba + en la columna nombre. Si \* está en la columna nombre, la clave se elimina, con todos sus valores y subclaves, cuando se quita el componente.

Se puede utilizar una acción personalizada para agregar filas a la tabla del registro durante una operación de instalación, desinstalación o reparación. Estas filas no se conservan en la tabla del registro y la información solo está disponible durante la transacción actual. Por lo tanto, la acción personalizada se debe ejecutar en todas las transacciones de instalación, desinstalación o reparación que requieran la información de estas filas adicionales. La acción personalizada debe ser anterior a las acciones [RemoveRegistryValues](removeregistryvalues-action.md) y [WriteRegistryValues](writeregistryvalues-action.md) en la secuencia de acción.

Para obtener información sobre cómo proteger una clave del registro, vea la [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md) y la [tabla LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE49](ice49.md)  
[ICE53](ice53.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE70](ice70.md)  
[ICE80](ice80.md)  
</dl>

 

 




