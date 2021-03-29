---
description: MsiViewGetColumnInfo y la propiedad ColumnInfo del objeto View usan el siguiente formato para describir las definiciones de las columnas de la base de datos.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Formato de definición de columna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277187"
---
# <a name="column-definition-format"></a>Formato de definición de columna

[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) y la [**propiedad ColumnInfo**](view-columninfo.md) del objeto [**View**](view-object.md) usan el siguiente formato para describir las definiciones de las columnas de la base de datos. Cada columna se describe mediante una cadena en el campo registro correspondiente devuelto por la función o la propiedad. La cadena de definición se compone de una sola letra que representa el tipo de datos seguido del ancho de la columna (en caracteres, si es aplicable, bytes de lo contrario). Un ancho de cero designa un ancho sin enlazar (por ejemplo, campos de texto largo y secuencias). Una letra mayúscula indica que se permiten valores NULL en la columna.



| Descriptor de columna | Cadena de definición                 |
|-------------------|-----------------------------------|
| seg?                | Cadena, longitud variable (? = 1-255) |
| S0                | Cadena, longitud variable           |
| i2                | Entero corto                     |
| i4                | Entero largo                      |
| v0                | Secuencia binaria                     |
| i?                | Cadena temporal (? = 0-255)        |
| j?                | Entero temporal (? = 0, 1, 2, 4)     |
| O0                | Objeto temporal                  |



 

Las cadenas usadas para describir columnas tienen la relación siguiente con las cadenas de consulta SQL utilizadas por CREATE y ALTER. Para obtener más información, vea [Sintaxis de SQL](sql-syntax.md).



| Valor devuelto | Sintaxis de SQL                |
|----------------|---------------------------|
| S0             | LONGCHAR                  |
| L0             | LONGCHAR LOCALIZABLE      |
| seg \#           | CHAR ( \# )                  |
| seg \#           | CARÁCTER ( \# )             |
| CG \#           | CHAR ( \# ) traducible      |
| CG \#           | CARÁCTER ( \# ) localizable |
| i2             | SHORT                     |
| i2             | INT                       |
| i2             | INTEGER                   |
| i4             | LONG                      |
| v0             | OBJECT                    |



 

Si la letra no se escribe en mayúsculas, la instrucción SQL debe anexarse con NOT NULL.



| Valor devuelto | Sintaxis de SQL        |
|----------------|-------------------|
| S0             | LONGCHAR NOT NULL |



 

El instalador no limita internamente la longitud de las columnas al valor especificado por el formato de definición de columna. Si los datos introducidos en un campo superan la longitud de columna especificada, el paquete no supera la [validación del paquete](package-validation.md). Para pasar la validación en este caso, se deben cambiar los datos o el esquema de la base de datos. La única forma de cambiar la longitud de la columna de una tabla estándar es exportando la tabla mediante [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editando el archivo. IDT exportado y, a continuación, importando la tabla con [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Los autores no pueden cambiar los tipos de datos de columna, la nulabilidad o los atributos de localización de las columnas de las tablas estándar. Los autores pueden crear tablas personalizadas con columnas que tengan atributos de columna.

Al usar [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) para combinar una base de datos de referencia en una base de datos de destino, los nombres de columna, el número de claves principales y los tipos de datos de columna deben coincidir. **MsiDatabaseMerge** omite los atributos de localización y de longitud de columna. Si una columna de la base de datos de referencia tiene una longitud que es 0 o mayor que la longitud de la columna en la base de datos de destino, **MsiDatabaseMerge** aumenta la longitud de la columna en la base de datos de destino a la longitud de la base de datos de referencia.

Cuando se usa Mergmod.dll versión 2,0, la aplicación de un módulo de combinación a un archivo. msi nunca cambia la longitud de las columnas o los tipos de columna de una tabla de base de datos existente. Sin embargo, la aplicación de un módulo de combinación puede cambiar el esquema de una tabla de base de datos existente si el módulo agrega nuevas columnas a una tabla para la que es válido Agregar columnas. Cuando se usa una versión de Mergemod.dll anterior a la versión 2,0, la aplicación de un módulo de combinación nunca cambia la longitud de las columnas y nunca cambia el esquema de la base de datos de destino.

 

 



