---
description: La tabla IniFile contiene la información. ini que la aplicación necesita para establecer en un archivo. ini.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Tabla IniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082534"
---
# <a name="inifile-table"></a>Tabla IniFile

La tabla IniFile contiene la información. ini que la aplicación necesita para establecer en un archivo. ini.

La tabla IniFile tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| IniFile     | [Identificador](identifier.md) | Y   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| DirProperty | [Identificador](identifier.md) | N   | Y        |
| Sección     | [Formatea](formatted.md)   | N   | N        |
| Clave         | [Formatea](formatted.md)   | N   | N        |
| Value       | [Formatea](formatted.md)   | N   | N        |
| Acción      | [Entero](integer.md)       | N   | N        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile
</dt> <dd>

La clave de esta tabla.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión
</dt> <dd>

Nombre traducible del archivo. ini en el que se va a escribir la información.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nombre de una propiedad que tiene un valor que se resuelve en la ruta de acceso completa de la carpeta que contiene el archivo. ini. La propiedad puede ser el nombre de un directorio en la [tabla del directorio](directory-table.md), una propiedad establecida por la [tabla AppSearch](appsearch-table.md)o cualquier otra propiedad que represente una ruta de acceso completa. Si este campo se deja en blanco, se crea el archivo. ini en la carpeta que tiene la ruta de acceso completa especificada por la propiedad [**WindowsFolder**](windowsfolder.md) .

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Transversal
</dt> <dd>

La sección del archivo. ini localizable.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

La clave del archivo. ini traducible dentro de la sección.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor traducible que se va a escribir.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar
</dt> <dd>

Tipo de modificación que se va a realizar.



| Constante                         | Hexadecimal | Decimal | Modificación                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| **msidbIniFileActionAddLine**    | 0x000       | 0       | Crea o actualiza una entrada. ini.                                                 |
| **msidbIniFileActionCreateLine** | 0x001       | 1       | Crea una entrada. ini solo si la entrada no existe.                   |
| **msidbIniFileActionAddTag**     | 0x003       | 3       | Crea una nueva entrada o anexa un nuevo valor separado por comas a una entrada existente. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa en la primera columna de la [tabla de componentes](component-table.md) que hace referencia al componente que controla la instalación del valor. ini.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La información del archivo. ini se escribe cuando se ha seleccionado el componente correspondiente para instalarlo como local o ejecutar desde el origen.

Se hace referencia a esta tabla cuando se ejecuta la acción [WriteIniValues](writeinivalues-action.md) o la [acción RemoveIniValues](removeinivalues-action.md) .

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

 

 



