---
description: La tabla RemoveRegistry contiene la información del Registro que la aplicación debe eliminar del registro del sistema.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: RemoveRegistry Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170dc727eef47ac214f7a7f42af7f487f53ad0b9a0658182420b28eb5224e38d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314885"
---
# <a name="removeregistry-table"></a>RemoveRegistry Table

La tabla RemoveRegistry contiene la información del Registro que la aplicación debe eliminar del registro del sistema.

La tabla RemoveRegistry tiene las siguientes columnas.



| Columna         | Tipo                         | Clave | Nullable |
|----------------|------------------------------|-----|----------|
| RemoveRegistry | [Identificador](identifier.md) | Y   | N        |
| Root           | [Entero](integer.md)       | N   | N        |
| Clave            | [RegPath](regpath.md)       | N   | N        |
| Nombre           | [Formato](formatted.md)   | N   | Y        |
| Componente\_    | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry
</dt> <dd>

Clave de esta tabla.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Raíz
</dt> <dd>

Clave raíz predefinida para el valor del Registro.



| Constante                          | Hexadecimal | Decimal | Clave raíz                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (ninguno)                            | \- 0x001    | -1      | **HKEY \_ El \_ instalador DE** USUARIO ACTUAL establece esta clave mientras se hace una instalación por usuario.<br/>                                                                                                                    |
| (ninguno)                            | -0x001      | -1      | **HKEY \_ El \_ instalador de** MÁQUINA LOCAL establece esta clave al realizar una instalación de todos los usuarios con [**ALLUSERS**](allusers.md) establecido en 1.<br/>                                                                       |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASSES \_ ROOT** El instalador quita el valor del subárbol Clases de **\\ software \\ HKCU** durante las instalaciones en el contexto de instalación por usuario [y por equipo.](installation-context.md)<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **USUARIO ACTUAL DE HKEY \_ \_**                                                                                                                                                                                            |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ LOCAL \_ MACHINE**                                                                                                                                                                                           |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **USUARIOS DE \_ HKEY**                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

Clave localizable para el valor del Registro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Nombre del valor del Registro localizable.

La siguiente cadena de la columna Nombre tiene una importancia especial.



| String | Significado                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| "-"    | La clave se va a eliminar, si está presente, con todos sus valores y subclaves, cuando se instale el componente. |



 

Tenga en cuenta [que la tabla del](registry-table.md) Registro debe usarse para crear o quitar una clave del Registro cuando se quita el componente.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la primera columna de la tabla [Component](component-table.md) que hace referencia al componente que controla la eliminación del valor del Registro.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La información del Registro se elimina del registro del sistema cuando se ha seleccionado el componente correspondiente para instalarse localmente o ejecutarse desde el origen.

Se hace referencia a esta tabla cuando se ejecuta la acción [RemoveRegistryValues.](removeregistryvalues-action.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 




