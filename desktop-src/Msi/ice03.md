---
description: ICE03 valida los tipos de datos y las claves externas en función de la tabla Validation y las tablas de base de datos \_ del .msi datos.
ms.assetid: e9be1c09-8468-4956-9aa0-12383ade4718
title: ICE03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017c13ee568a0efe4d88c28594fb568a7b4a0736
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074685"
---
# <a name="ice03"></a>ICE03

ICE03 valida los tipos de datos y las claves externas en función de la tabla [ \_ Validation](-validation-table.md) y las tablas de base de datos del .msi datos.

## <a name="result"></a>Resultado

ICE03 publica los siguientes mensajes para los errores de validación.



| Mensaje de error ICE03                                                       | Descripción                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Clave principal duplicada                                                     | Las claves principales de una nueva fila duplican las claves principales de una fila existente. La columna Que acepta valores NULL de la [ \_ tabla Validación](-validation-table.md) muestra las claves principales de la base de datos.                                                                                              |
| No es una columna que acepta valores NULL                                                     | Una columna de tabla que no se especifica como que acepta valores NULL en la columna Acepta valores NULL de la tabla [ \_ Validación](-validation-table.md) contiene una entrada que es Null.                                                                                                                                |
| No es una clave externa válida                                                   | Una columna que es una clave externa en una segunda tabla contiene una entrada que no existe en la clave principal de la segunda tabla.                                                                                                                                                          |
| El valor supera MaxValue                                                    | El valor numérico de una entrada de una tabla de base de datos supera el límite máximo especificado para este campo en la columna MaxValue de la [ \_ tabla Validation](-validation-table.md).                                                                                                           |
| Valor por debajo de MinValue                                                      | El valor numérico de una entrada de una tabla de base de datos es menor que el límite mínimo especificado para este campo en la columna MinValue de la [ \_ tabla Validation](-validation-table.md).                                                                                                      |
| Valor que no es miembro del conjunto                                             | El valor de una entrada de una tabla de base de datos no es miembro del conjunto aceptable de valores especificado para este campo en la columna Set de la [ \_ tabla Validation](-validation-table.md).                                                                                                  |
| Cadena de versión no válida                                                    | Consulte el tipo [de datos](version.md) Versión.                                                                                                                                                                                                                                                 |
| Todas las mayúsculas y minúsculas necesarias                                                   | Consulte el [tipo de datos UpperCase.](uppercase.md)                                                                                                                                                                                                                                             |
| Cadena GUID no válida                                                       | Consulte el tipo [de datos GUID.](guid.md)                                                                                                                                                                                                                                                       |
| Nombre de archivo no válido/uso de caracteres comodín                                      | La base de datos contiene un nombre de archivo no válido o un carácter comodín incorrecto. Vea el [tipo de datos WildCardFilename.](wildcardfilename.md)                                                                                                                                                          |
| Identificador no válido                                                        | Consulte el [tipo de datos](identifier.md) Identificador.                                                                                                                                                                                                                                           |
| Identificador de idioma no válido                                                       | La base de datos contiene un identificador numérico de idioma (LANGID) no válido. Consulte el [tipo de datos Lenguaje.](language.md) Vea [Language Identifier Constants and Strings](../intl/language-identifier-constants-and-strings.md)(Constantes y cadenas de identificador de lenguaje). Por ejemplo, 1033 para Estados Unidos y 0 para el idioma neutro.<br/> |
| Nombre de archivo no válido                                                          | Consulte el tipo [de datos Filename.](filename.md)                                                                                                                                                                                                                                               |
| Ruta de acceso completa no válida                                                         | Consulte los tipos de datos [Path](path.md), [AnyPath](anypath.md)y [Paths.](paths.md)                                                                                                                                                                                                      |
| Cadena condicional no válida                                                    | La base de datos contiene una cadena condicional no válida. Se trata de una cadena de texto que debe evaluarse como TRUE o FALSE según la [sintaxis de la instrucción condicional](conditional-statement-syntax.md). Consulte el [tipo de](condition.md) datos Condición.                                           |
| Cadena de formato no válido                                                     | Consulte el [tipo de datos Con](formatted.md) formato.                                                                                                                                                                                                                                             |
| Cadena de plantilla no válida                                                   | Consulte el tipo [de datos](template.md) Plantilla.                                                                                                                                                                                                                                               |
| Cadena DefaultDir no válida                                                 | Consulte el [tipo de datos DefaultDir.](defaultdir.md)                                                                                                                                                                                                                                           |
| Ruta de acceso del Registro no válida                                                     | Consulte el [tipo de datos RegPath.](regpath.md)                                                                                                                                                                                                                                                 |
| Datos customSource no disponibles                                                     | Consulte el [tipo de datos CustomSource.](customsource.md)                                                                                                                                                                                                                                       |
| Cadena de propiedad no válida                                                   | Consulte el [tipo de datos](property.md) Propiedad.                                                                                                                                                                                                                                               |
| Faltan datos en la \_ tabla de validación o en la base de datos antigua                        | Hay columnas en la base de datos que no aparecen en la columna Columna de la [ \_ tabla Validación](-validation-table.md). La base de \_ datos y la tabla de validación no coinciden                                                                                                           |
| Nombre o sintaxis de gabinetes no válidas                                                   | Consulte el tipo [de datos Archivador.](cabinet.md)                                                                                                                                                                                                                                                 |
| \_Tabla de validación: Cadena de categoría no válida                               | Se trata de un error al crear la tabla \_ Validation. La validación no reconoce la cadena de categoría usada para esta columna concreta en la \_ tabla Validación. Vea [Tipos de datos de columna](column-data-types.md) y especifique una categoría válida.                                           |
| \_Tabla de validación: los datos de la columna KeyTable son incorrectos                  | La columna KeyTable de la \_ tabla Validation hace referencia a una tabla que no existe en la base de datos.                                                                                                                                                                                     |
| \_Tabla de validación: valor de la columna MaxValue < que en la columna MinValue | Se trata de un error al crear la tabla [ \_ de validación](-validation-table.md). Min siempre debe ser menor o igual que Max.                                                                                                                                                              |
| Destino de acceso directo no bueno                                                       | Vea el tipo [de datos Acceso](shortcut.md) directo.                                                                                                                                                                                                                                               |
| Desbordamiento de cadena (mayor que la longitud permitida en la columna)                 | La longitud de la cadena es mayor que el ancho de columna especificado por la definición de columna. Tenga en cuenta que el instalador no limita internamente el ancho de columna al valor especificado. Vea [Formato de definición de columna](column-definition-format.md).                                         |
| Error no definido                                                           | Error desconocido.                                                                                                                                                                                                                                                                            |
| La columna no se puede localizar                                                | Las columnas de clave principal no se pueden localizar.                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 
