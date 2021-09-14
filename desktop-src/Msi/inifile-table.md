---
description: La tabla IniFile contiene la .ini que la aplicación debe establecer en un .ini archivo.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Tabla IniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171821"
---
# <a name="inifile-table"></a>Tabla IniFile

La tabla IniFile contiene la .ini que la aplicación debe establecer en un .ini archivo.

La tabla IniFile tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| IniFile     | [Identificador](identifier.md) | Y   | No        |
| FileName    | [FileName](text.md)         | No   | No        |
| DirProperty | [Identificador](identifier.md) | No   | Y        |
| Sección     | [Formato](formatted.md)   | No   | No        |
| Clave         | [Formato](formatted.md)   | No   | No        |
| Value       | [Formato](formatted.md)   | No   | No        |
| Acción      | [Entero](integer.md)       | No   | No        |
| Componente\_ | [Identificador](identifier.md) | No   | No        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile
</dt> <dd>

Clave de esta tabla.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nombre
</dt> <dd>

Nombre localizable del archivo .ini en el que se va a escribir la información.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nombre de una propiedad que tiene un valor que se resuelve en la ruta de acceso completa de la carpeta que contiene .ini archivo. La propiedad puede ser el nombre de un directorio de la tabla [Directory](directory-table.md), una propiedad establecida por la tabla [AppSearch](appsearch-table.md)o cualquier otra propiedad que represente una ruta de acceso completa. Si este campo se deja en blanco, el archivo .ini se crea en la carpeta que tiene la ruta de acceso completa especificada por la [**propiedad WindowsFolder.**](windowsfolder.md)

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sección
</dt> <dd>

Sección archivo .ini localizable.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

Clave de archivo .ini localizable dentro de la sección .

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor localizable que se va a escribir.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Acción
</dt> <dd>

Tipo de modificación que se va a realizar.



| Constante                         | Hexadecimal | Decimal | Modificación                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| **msidbIniFileActionAddLine**    | 0x000       | 0       | Crea o actualiza una .ini entrada.                                                 |
| **msidbIniFileActionCreateLine** | 0x001       | 1       | Crea una .ini solo si la entrada aún no existe.                   |
| **msidbIniFileActionAddTag**     | 0x003       | 3       | Crea una nueva entrada o anexa un nuevo valor separado por comas a una entrada existente. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Component](component-table.md) que hace referencia al componente que controla la instalación del .ini valor.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La .ini de archivos se escribe cuando se ha seleccionado el componente correspondiente para instalarse como local o ejecutarse desde el origen.

Se hace referencia a esta tabla cuando se [ejecuta la acción WriteIniValues](writeinivalues-action.md) o [la acción RemoveIniValues.](removeinivalues-action.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
</dl>

 

 



