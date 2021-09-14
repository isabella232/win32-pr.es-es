---
description: La tabla Registro contiene la información del Registro que la aplicación debe establecer en el registro del sistema.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Tabla del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069682"
---
# <a name="registry-table"></a>Tabla del Registro

La tabla Registro contiene la información del Registro que la aplicación debe establecer en el registro del sistema.

La tabla Registry tiene las siguientes columnas.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Registro    | [Identificador](identifier.md) | Y   | N        |
| Root        | [Entero](integer.md)       | N   | N        |
| Clave         | [RegPath](regpath.md)       | N   | N        |
| Nombre        | [Formato](formatted.md)   | N   | Y        |
| Value       | [Formato](formatted.md)   | N   | Y        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registro
</dt> <dd>

Clave principal usada para identificar un registro.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Raíz
</dt> <dd>

Clave raíz predefinida para el valor del Registro. Escriba un valor de -1 en este campo para que la clave raíz dependa del tipo de instalación. Escriba uno de los otros valores de la tabla siguiente para forzar que el valor del Registro se escriba en una clave raíz determinada.



| Constante                          | Hexadecimal | Decimal | Clave raíz                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (ninguno)                            | \- 0x001    | -1      | Si se trata de una instalación por usuario, el valor del Registro se escribe en **HKEY \_ CURRENT \_ USER**. Si se trata de una instalación por equipo, el valor del Registro se escribe en **HKEY \_ LOCAL \_ MACHINE**. Tenga en cuenta que se especifica una instalación por equipo estableciendo la [**propiedad ALLUSERS**](allusers.md) en 1.<br/>                |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASSES \_ ROOT** El instalador escribe o quita el valor del subárbol Clases de **\\ software \\ HKCU** durante la instalación en el contexto de instalación [por usuario](installation-context.md).<br/> El instalador escribe o quita el valor del subárbol Clases de **\\ software \\ HKLM** durante las instalaciones por máquina.<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **USUARIO ACTUAL DE HKEY \_ \_**                                                                                                                                                                                                                                                                                                                      |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ LOCAL \_ MACHINE**                                                                                                                                                                                                                                                                                                                     |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **USUARIOS DE \_ HKEY**                                                                                                                                                                                                                                                                                                                              |



 

Tenga en cuenta que se recomienda que las entradas del Registro escritas en el subárbol **HKCU** hacen referencia a un componente con el bit RegistryKeyPath establecido en la columna Atributos de la [tabla Component](component-table.md). Esto garantiza que el instalador escribe las entradas del Registro necesarias cuando hay varios usuarios en el mismo equipo.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

Clave localizable para el valor del Registro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Esta columna contiene el nombre del valor del Registro (localizable). Si es Null, los datos especificados en la columna Valor se escriben en la clave del Registro predeterminada.

Si la columna Valor es Null, las cadenas que se muestran en la tabla siguiente de la columna Nombre tienen una importancia especial.



| String | Significado                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | La clave se creará, si no está presente, cuando se instale el componente.                                                                                                                            |
| \-     | La clave se eliminará, si está presente, con todos sus valores y subclaves, cuando se desinstale el componente.                                                                                     |
| \*     | La clave se creará, si no está presente, cuando se instale el componente. Además, la clave se eliminará, si está presente, con todos sus valores y subclaves, cuando se desinstale el componente. |



 

Tenga en cuenta que la tabla [RemoveRegistry](removeregistry-table.md) debe usarse si se va a eliminar una clave del Registro instalada, con sus valores y subclaves, cuando se instala el componente.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Esta columna es el valor localizable del Registro. El campo tiene [el formato](formatted.md). Si el valor está asociado a uno de los prefijos siguientes (es decir, valor ), el valor se interpreta como se \# % describe en la tabla. Tenga en cuenta que cada prefijo comienza con un signo de número ( \# ). Si el valor comienza con dos o más signos numéricos consecutivos ( ), el primero se omite y el valor se \# interpreta y se almacena como una \# cadena.



| Prefijo | Significado                                                                        |
|--------|--------------------------------------------------------------------------------|
| \#X    | El valor se interpreta y almacena como un valor hexadecimal (REG \_ BINARY).      |
| \#%    | El valor se interpreta y almacena como una cadena expandible (REG \_ EXPAND \_ SZ). |
| \#     | El valor se interpreta y almacena como un entero (REG \_ DWORD).                |



 

-   Si el valor contiene la tilde de secuencia , el valor se interpreta como una lista de cadenas delimitada por null \[ ~ \] (REG \_ MULTI \_ SZ). Por ejemplo, para especificar una lista que contenga las tres cadenas a, b y c, use "a \[ ~ \] b \[ ~ \] c".
-   La secuencia \[ ~ \] dentro del valor separa las cadenas individuales y se interpreta y almacena como un carácter NULL.
-   Si precede a la lista de cadenas, las cadenas se anexarán a las cadenas de valor \[ ~ \] del Registro existentes. Si ya se produce una cadena anexa en el valor del Registro, se quita la aparición original de la cadena.
-   Si sigue al final de la lista de \[ cadenas, las cadenas se anteponen a cualquier cadena de valor ~ \] del Registro existente. Si ya se produce una cadena de anteponer en el valor del Registro, se quita la repetición original de la cadena.
-   Si está al principio y al final o al principio ni al final de la lista de cadenas, las cadenas reemplazarán las cadenas de valor \[ ~ \] del Registro existentes.
-   De lo contrario, el valor se interpreta y se almacena como una cadena (REG \_ SZ).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Component](component-table.md) que hace referencia al componente que controla la instalación del valor del Registro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las [acciones WriteRegistryValues](writeregistryvalues-action.md) y [RemoveRegistryValues](removeregistryvalues-action.md) de las tablas de secuencia [*procesan*](s-gly.md) la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

La información del Registro se escribe en el registro del sistema cuando se ha seleccionado el componente correspondiente para instalarse localmente o ejecutarse desde el origen.

Tenga en cuenta que el instalador quita una clave del Registro después de quitar el último valor o subclave bajo la clave. Para evitar que se quite una clave del Registro vacía al desinstalar, escriba un valor ficticio en la clave que necesita conservar y escriba + en la columna Nombre. Si está en la columna Nombre, la clave se elimina, con todos sus valores y \* subclaves, cuando se quita el componente.

Se puede usar una acción personalizada para agregar filas a la tabla del Registro durante una transacción de instalación, desinstalación o reparación. Estas filas no se conservan en la tabla del Registro y la información solo está disponible durante la transacción actual. Por lo tanto, la acción personalizada debe ejecutarse en todas las transacciones de instalación, desinstalación o reparación que requieran la información de estas filas adicionales. La acción personalizada debe ir antes de [las acciones RemoveRegistryValues](removeregistryvalues-action.md) y [WriteRegistryValues](writeregistryvalues-action.md) de la secuencia de acciones.

Para obtener información sobre cómo proteger una clave del Registro, vea [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) y [LockPermissions Table](lockpermissions-table.md).

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

 

 




