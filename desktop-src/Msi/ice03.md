---
description: ICE03 valida los tipos de datos y las claves externas en función de la \_ tabla de validación y las tablas de base de datos del archivo. msi.
ms.assetid: e9be1c09-8468-4956-9aa0-12383ade4718
title: ICE03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017c13ee568a0efe4d88c28594fb568a7b4a0736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277553"
---
# <a name="ice03"></a>ICE03

ICE03 valida los tipos de datos y las claves externas en función de la [ \_ tabla de validación](-validation-table.md) y las tablas de base de datos del archivo. msi.

## <a name="result"></a>Resultado

ICE03 publica los siguientes mensajes para los errores de validación.



| Mensaje de error de ICE03                                                       | Descripción                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Clave principal duplicada                                                     | Las claves principales de una nueva fila duplican las claves principales de una fila existente. La columna que admite valores NULL de la [ \_ tabla de validación](-validation-table.md) muestra las claves principales de la base de datos.                                                                                              |
| No es una columna que admite valores NULL                                                     | Una columna de tabla que no se especifica como que acepta valores NULL en la columna que admite valores NULL de la [ \_ tabla de validación](-validation-table.md) contiene una entrada que es NULL.                                                                                                                                |
| No es una clave externa válida                                                   | Una columna que es una clave externa en una segunda tabla contiene una entrada que no existe en la clave principal de la segunda tabla.                                                                                                                                                          |
| El valor supera MaxValue                                                    | El valor numérico de una entrada de una tabla de base de datos supera el límite máximo especificado para este campo en la columna MaxValue de la [ \_ tabla de validación](-validation-table.md).                                                                                                           |
| Valor bajo MinValue                                                      | El valor numérico de una entrada de una tabla de base de datos es menor que el límite mínimo especificado para este campo en la columna MinValue de la [ \_ tabla de validación](-validation-table.md).                                                                                                      |
| El valor no es un miembro del conjunto.                                             | El valor de una entrada de una tabla de base de datos no es un miembro del conjunto de valores aceptable especificado para este campo en la columna set de la [ \_ tabla de validación](-validation-table.md).                                                                                                  |
| Cadena de versión no válida                                                    | Vea el tipo de datos [version](version.md) .                                                                                                                                                                                                                                                 |
| Todo en mayúsculas necesario                                                   | Vea el tipo de datos en [mayúsculas](uppercase.md) .                                                                                                                                                                                                                                             |
| Cadena de GUID no válida                                                       | Vea el tipo de datos [GUID](guid.md) .                                                                                                                                                                                                                                                       |
| Nombre de archivo no válido/uso de caracteres comodín                                      | La base de datos contiene un nombre de archivo no válido o un carácter comodín incorrecto. Vea el tipo de datos [WildCardFilename](wildcardfilename.md) .                                                                                                                                                          |
| Identificador no válido                                                        | Vea el tipo de datos [Identifier](identifier.md) .                                                                                                                                                                                                                                           |
| Identificador de idioma no válido                                                       | La base de datos contiene un identificador de idioma numérico (LANGID) no válido. Vea el tipo de datos [Language](language.md) . Vea [constantes y cadenas de identificador de idioma](../intl/language-identifier-constants-and-strings.md). Por ejemplo, 1033 para los Estados Unidos y 0 para idiomas neutros.<br/> |
| Nombre de archivo no válido                                                          | Vea el tipo de datos [filename](filename.md) .                                                                                                                                                                                                                                               |
| Ruta de acceso completa no válida                                                         | Vea los tipos de datos [path](path.md), [AnyPath](anypath.md)y [paths](paths.md) .                                                                                                                                                                                                      |
| Cadena condicional incorrecta                                                    | La base de datos contiene una cadena condicional no válida. Se trata de una cadena de texto que debe evaluarse como TRUE o FALSE según la sintaxis de la [instrucción condicional](conditional-statement-syntax.md). Vea el tipo de datos [Condition](condition.md) .                                           |
| Cadena de formato no válida                                                     | Vea el tipo de datos [con formato](formatted.md) .                                                                                                                                                                                                                                             |
| Cadena de plantilla no válida                                                   | Vea el tipo de datos de la [plantilla](template.md) .                                                                                                                                                                                                                                               |
| Cadena de DefaultDir no válida                                                 | Vea el tipo de datos [DefaultDir](defaultdir.md) .                                                                                                                                                                                                                                           |
| Ruta de acceso del registro no válida                                                     | Vea el tipo de datos [RegPath](regpath.md) .                                                                                                                                                                                                                                                 |
| Datos de CustomSource no válidos                                                     | Vea el tipo de datos [CustomSource](customsource.md) .                                                                                                                                                                                                                                       |
| Cadena de propiedad no válida                                                   | Vea el tipo de datos de la [propiedad](property.md) .                                                                                                                                                                                                                                               |
| Faltan datos en la tabla de validación o en la base de datos \_ anterior                        | Hay columnas en la base de datos que no aparecen en la columna columna de la [ \_ tabla de validación](-validation-table.md). La base de datos y la \_ tabla de validación no coinciden                                                                                                           |
| Sintaxis/nombre de archivo. cab incorrecto                                                   | Vea el tipo de datos del [archivo. cab](cabinet.md) .                                                                                                                                                                                                                                                 |
| \_Tabla de validación: cadena de categoría no válida                               | Se trata de un error al crear la \_ tabla de validación. La validación no reconoce la cadena de categoría utilizada para esta columna en particular en la \_ tabla de validación. Vea [tipos de datos de columna](column-data-types.md) y especifique una categoría válida.                                           |
| \_Tabla de validación: los datos de la columna KeyTable son incorrectos                  | La columna KeyTable de la \_ tabla de validación hace referencia a una tabla que no existe en la base de datos.                                                                                                                                                                                     |
| \_Tabla de validación: valor en la columna MaxValue < que en la columna MinValue | Se trata de un error al crear la [ \_ tabla de validación](-validation-table.md). Min debe ser siempre menor o igual que Max.                                                                                                                                                              |
| Destino de acceso directo incorrecto                                                       | Vea el tipo de datos de [acceso directo](shortcut.md) .                                                                                                                                                                                                                                               |
| Desbordamiento de cadena (mayor que la longitud permitida en la columna)                 | La longitud de la cadena es mayor que el ancho de columna especificado por la definición de la columna. Tenga en cuenta que el instalador no limita internamente el ancho de columna al valor especificado. Vea [formato de definición de columna](column-definition-format.md).                                         |
| Error no definido                                                           | Error desconocido.                                                                                                                                                                                                                                                                            |
| No se puede localizar la columna                                                | No se pueden localizar las columnas de clave principal.                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 
