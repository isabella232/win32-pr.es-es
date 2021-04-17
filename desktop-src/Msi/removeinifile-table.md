---
description: La tabla RemoveIniFile contiene la información que debe eliminar una aplicación de un archivo. ini.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Tabla RemoveIniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669801"
---
# <a name="removeinifile-table"></a>Tabla RemoveIniFile

La tabla RemoveIniFile contiene la información que debe eliminar una aplicación de un archivo. ini.

La tabla RemoveIniFile tiene las columnas siguientes.



| Columna        | Tipo                         | Clave | Nullable |
|---------------|------------------------------|-----|----------|
| RemoveIniFile | [Identificador](identifier.md) | Y   | N        |
| FileName      | [FileName](text.md)         | N   | N        |
| DirProperty   | [Identificador](identifier.md) | N   | Y        |
| Sección       | [Formatea](formatted.md)   | N   | N        |
| Clave           | [Formatea](formatted.md)   | N   | N        |
| Value         | [Formatea](formatted.md)   | N   | Y        |
| Acción        | [Entero](integer.md)       | N   | N        |
| Componente\_   | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile
</dt> <dd>

La clave de esta tabla.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión
</dt> <dd>

Nombre del archivo. ini en el que se va a eliminar la información.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nombre de una propiedad cuyo valor se supone que se va a resolver como la ruta de acceso completa a la carpeta del archivo. ini que se va a quitar. La propiedad puede ser el nombre de un directorio en la [tabla del directorio](directory-table.md), una propiedad establecida por la [tabla AppSearch](appsearch-table.md)o cualquier otra propiedad que represente una ruta de acceso completa.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Transversal
</dt> <dd>

La sección del archivo. ini localizable.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

La clave del archivo. ini traducible debajo de la sección.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor traducible que se va a eliminar. El valor es necesario cuando la acción es 4.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar
</dt> <dd>

Tipo de modificación que se va a realizar.



| Constante                         | Hexadecimal | Decimal | Significado                          |
|----------------------------------|-------------|---------|----------------------------------|
| **msidbIniFileActionRemoveLine** | 0x002       | 2       | Elimina la entrada. ini.              |
| **msidbIniFileActionRemoveTag**  | 0x004       | 4       | Elimina una etiqueta de una entrada. ini. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa en la primera columna de la [tabla de componentes](component-table.md) que hace referencia al componente que controla la eliminación del valor. ini.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La información del archivo. ini se elimina cuando se selecciona la instalación del componente correspondiente, ya sea de forma local o se ejecuta desde el origen.

Se hace referencia a esta tabla cuando se ejecuta la [acción RemoveIniValues](removeinivalues-action.md) .

Si la columna de directorio \_ se especifica como null, la ubicación del archivo ini es la ubicación estándar de Windows ini, que es el directorio de Windows de forma predeterminada.

Al quitar el último valor de una sección, se elimina esa sección. No hay ninguna otra manera de eliminar una sección completa que no sea la eliminación de todos sus valores.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



