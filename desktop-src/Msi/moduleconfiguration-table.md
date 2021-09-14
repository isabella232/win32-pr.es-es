---
description: La tabla ModuleConfiguration identifica los atributos configurables del módulo. Esta tabla no se combina en la base de datos.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: Tabla ModuleConfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa187c10b5d3376a9bec78eb897b4982445ff01f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261167"
---
# <a name="moduleconfiguration-table"></a>Tabla ModuleConfiguration

La tabla ModuleConfiguration identifica los atributos configurables del módulo. Esta tabla no se combina en la base de datos.

La tabla ModuleConfiguration tiene las columnas siguientes.



| Columna       | Tipo                         | Clave | Nullable |
|--------------|------------------------------|-----|----------|
| Nombre         | [Identificador](identifier.md) | Y   | N        |
| Formato       | [Entero](integer.md)       | N   | N        |
| Tipo         | [Texto](text.md)             | N   | Y        |
| ContextData  | [Texto](text.md)             | N   | Y        |
| DefaultValue | [Texto](text.md)             | N   | Y        |
| Atributos   | [Entero](integer.md)       | N   | Y        |
| DisplayName  | [Texto](text.md)             | N   | Y        |
| Descripción  | [Texto](text.md)             | N   | Y        |
| HelpLocation | [Texto](text.md)             | N   | Y        |
| HelpKeyword  | [Texto](text.md)             | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Este campo define el nombre del elemento configurable. Se hace referencia a este nombre en la plantilla de formato de la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

</dd> <dt>

<span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Formato
</dt> <dd>

Esta columna especifica el formato de los datos que se cambian.



| Formato                                       | Value |
|----------------------------------------------|-------|
| [Texto](text-format-types.md)                | 0     |
| [Clave](key-format-types.md)                  | 1     |
| [Entero](integer-format-types.md)          | 2     |
| [Formato de campo de bits](bitfield-format-types.md) | 3     |



 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Esta columna especifica el tipo de los datos que se cambian. Este tipo se usa para proporcionar un contexto para cualquier interfaz de usuario y no se usa en el proceso de combinación. Los valores válidos para esta columna dependen del valor de la columna Formato.

</dd> <dt>

<span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData
</dt> <dd>

Esta columna especifica un contexto semántico para los datos solicitados. El tipo se usa para proporcionar un contexto para cualquier interfaz de usuario y no se usa en el proceso de combinación. Los valores válidos para esta columna dependen de los valores de las columnas Format y Type.

</dd> <dt>

<span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>Defaultvalue
</dt> <dd>

Esta columna especifica un valor predeterminado para el elemento de este registro si la herramienta de combinación rechaza proporcionar un valor. Este valor debe tener el formato, el tipo y el contexto del elemento. Si se trata de un elemento de formato "Key", la clave externa debe ser una clave válida en las tablas del módulo. Null puede ser un valor válido para esta columna en función del elemento. Para los elementos de formato "Clave", este valor está en formato [especial de CMSM.](cmsm-special-format.md) Para todos los demás tipos, el valor se trata literalmente.

Los autores de módulos deben asegurarse de que el módulo sea válido en su estado predeterminado. Esto garantiza que las versiones de Mergemod.dll anteriores a la versión 2.0 puedan seguir utilizando el módulo en su estado predeterminado.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Esta columna es un campo de bits que contiene atributos para este elemento configurable. Null es equivalente a 0. Todos los demás bits de esta columna están reservados para su uso futuro y deben ser 0.



| Nombre                             | Decimal | Hexadecimal | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msmConfigurableOptionKeyNoOrphan | 1       | 0x00000001  | Este atributo solo se aplica a los registros que enumen una clave externa a una tabla de módulos en su campo DefaultValue. La herramienta de combinación omite el atributo para cualquier formato que no sea [Key Format Types](key-format-types.md). Los elementos que no aparecen [en la tabla ModuleSubstitution](modulesubstitution-table.md) se excluyen de la comprobación siguiente. La herramienta de combinación no combina la fila a la que hace referencia la columna DefaultValue en la base de datos de destino si se cumplen las condiciones siguientes después de completar todas las opciones de configuración.<br/> Cada fila de la tabla ModuleConfiguration con el mismo Valor Predeterminado tiene el conjunto msmConfigurationItemsKeyNoOrphan.<br/> Ninguna fila usa DefaultValue porque la herramienta de creación rechazó proporcionar un valor.<br/> La herramienta de combinación combina la fila si se cumple alguna de las condiciones siguientes.<br/> La herramienta de combinación busca cualquier fila que no tenga establecido msmConfigItemsKeyNoOrphan.<br/> Si la herramienta de combinación encuentra alguna fila con DefaultValue porque la herramienta de creación rechazó proporcionar un valor.<br/> |
| msmConfigurableOptionNonNullable | 2       | 0x00000002  | Cuando se establece este atributo, null no es una respuesta válida para este elemento. Este atributo no tiene ningún efecto para [los tipos de formato entero o](integer-format-types.md) los tipos de formato de campo de [bits](bitfield-format-types.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>Displayname
</dt> <dd>

Esta columna proporciona una breve descripción de este elemento que la herramienta de creación puede usar en la interfaz de usuario. Es posible que esta columna no esté localizada. Establezca esta columna en null para que el módulo solicite que la herramienta de creación no exponga esta propiedad en la interfaz de usuario. La herramienta puede pasar por alto el valor de este campo.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Esta columna proporciona una descripción de este elemento que la herramienta de creación puede usar en los elementos de la interfaz de usuario. La transformación de idioma del módulo puede localizar esta cadena. Esta columna puede ser null.

</dd> <dt>

<span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation
</dt> <dd>

Esta columna proporciona el nombre de un archivo de ayuda (sin la extensión .chm) o una lista delimitada por punto y coma de espacios de nombres de ayuda. Esta columna puede ser NULL si no hay ayuda disponible. Esta columna solo puede ser NULL si la columna HelpKeyword es NULL.

</dd> <dt>

<span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword
</dt> <dd>

Esta columna proporciona una palabra clave en el archivo de ayuda o espacio de nombres de la columna HelpLocation. La interpretación de esta palabra clave depende de la columna HelpLocation. Esta columna puede ser null.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los módulos de combinación configurables usan [la tabla ModuleConfiguration.](configurable-merge-modules.md) Mergemod.dll 2.0 o posterior es necesario para crear un módulo de combinación configurable.

Para garantizar la compatibilidad con versiones anteriores de Mergemod.dll, la tabla ModuleConfiguration y la tabla [ModuleSubstitution](modulesubstitution-table.md) deben agregarse a la [tabla ModuleIgnoreTable](moduleignoretable-table.md) de cada módulo.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
[ICE45](ice45.md)  
</dl>

 

 




