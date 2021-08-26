---
description: La tabla RemoveIniFile contiene la información que una aplicación necesita eliminar de un .ini archivo.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Tabla RemoveIniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6aca38f320a8cb548faf00d284cff4c934e127a44cbaf7ca5b96013fac80d63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074585"
---
# <a name="removeinifile-table"></a>Tabla RemoveIniFile

La tabla RemoveIniFile contiene la información que una aplicación necesita eliminar de un .ini archivo.

La tabla RemoveIniFile tiene las siguientes columnas.



| Columna        | Tipo                         | Clave | Nullable |
|---------------|------------------------------|-----|----------|
| RemoveIniFile | [Identificador](identifier.md) | Y   | N        |
| FileName      | [FileName](text.md)         | N   | N        |
| DirProperty   | [Identificador](identifier.md) | N   | Y        |
| Sección       | [Formato](formatted.md)   | N   | N        |
| Clave           | [Formato](formatted.md)   | N   | N        |
| Valor         | [Formato](formatted.md)   | N   | Y        |
| Acción        | [Entero](integer.md)       | N   | N        |
| Componente\_   | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile
</dt> <dd>

Clave de esta tabla.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nombre
</dt> <dd>

Nombre .ini archivo en el que se va a eliminar la información.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nombre de una propiedad cuyo valor se supone que se resuelve en la ruta de acceso completa a la carpeta del archivo .ini que se va a quitar. La propiedad puede ser el nombre de un directorio de la tabla [Directory](directory-table.md), una propiedad establecida por la tabla [AppSearch](appsearch-table.md)o cualquier otra propiedad que represente una ruta de acceso completa.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sección
</dt> <dd>

Sección archivo .ini localizable.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

Clave de archivo .ini localizable debajo de la sección .

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor localizable que se va a eliminar. El valor es necesario cuando Action es 4.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Acción
</dt> <dd>

Tipo de modificación que se va a realizar.



| Constante                         | Hexadecimal | Decimal | Significado                          |
|----------------------------------|-------------|---------|----------------------------------|
| **msidbIniFileActionRemoveLine** | 0x002       | 2       | Elimina .ini entrada.              |
| **msidbIniFileActionRemoveTag**  | 0x004       | 4       | Elimina una etiqueta de una .ini entrada. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Component](component-table.md) que hace referencia al componente que controla la eliminación del .ini valor.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La .ini archivo se elimina cuando se ha seleccionado el componente correspondiente para instalarse, ya sea localmente o desde el origen.

Se hace referencia a esta tabla cuando se ejecuta la acción [RemoveIniValues.](removeinivalues-action.md)

Si la columna Directory se especifica como null, la ubicación del archivo ini es la ubicación estándar Windows ini, que es el Windows directorio \_ de forma predeterminada.

Al quitar el último valor de una sección, se elimina esa sección. No hay otra manera de eliminar una sección completa que no sea quitar todos sus valores.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



