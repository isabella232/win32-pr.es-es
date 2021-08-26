---
description: MsiViewGetColumnInfo y la propiedad ColumnInfo del objeto View usan el formato siguiente para describir las definiciones de columna de base de datos.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Formato de definición de columna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f0fcad09d0c87b766022602b152c09f466b4d6cddc87467b89ff02793240b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077935"
---
# <a name="column-definition-format"></a>Formato de definición de columna

[**MsiViewGetColumnInfo y**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) la [**propiedad ColumnInfo**](view-columninfo.md) del objeto [**View**](view-object.md) usan el formato siguiente para describir las definiciones de columna de base de datos. Cada columna se describe mediante una cadena en el campo de registro correspondiente devuelto por la función o propiedad . La cadena de definición consta de una sola letra que representa el tipo de datos seguido del ancho de la columna (en caracteres si procede, bytes en caso contrario). Un ancho de cero designa un ancho sin enlazar (por ejemplo, flujos y campos de texto largos). Una letra mayúscula indica que se permiten valores NULL en la columna.



| Descriptor de columna | Cadena de definición                 |
|-------------------|-----------------------------------|
| s?                | Cadena, longitud variable (?=1-255) |
| s0                | Cadena, longitud variable           |
| i2                | Entero corto                     |
| i4                | Entero largo                      |
| v0                | Secuencia binaria                     |
| ¿G?                | Cadena temporal (?=0-255)        |
| ¿J?                | Entero temporal (?=0,1,2,4)     |
| O0                | Objeto temporal                  |



 

Las cadenas usadas para describir columnas tienen la siguiente relación con las cadenas de consulta SQL cadenas de consulta usadas por CREATE y ALTER. Para obtener más información, [vea sintaxis SQL .](sql-syntax.md)



| Valor devuelto | Sintaxis de SQL                |
|----------------|---------------------------|
| s0             | LONGCHAR                  |
| l0             | LONGCHAR LOCALIZABLE      |
| s \#           | CHAR( \# )                  |
| s \#           | CHARACTER( \# )             |
| L \#           | CHAR( \# ) LOCALIZABLE      |
| L \#           | CHARACTER( \# ) LOCALIZABLE |
| i2             | SHORT                     |
| i2             | INT                       |
| i2             | INTEGER                   |
| i4             | LONG                      |
| v0             | OBJECT                    |



 

Si la letra no está en mayúsculas, la instrucción SQL debe anexarse con NOT NULL.



| Valor devuelto | Sintaxis de SQL        |
|----------------|-------------------|
| s0             | LONGCHAR NOT NULL |



 

El instalador no limita internamente la longitud de las columnas al valor especificado por el formato de definición de columna. Si los datos especificados en un campo superan la longitud de columna especificada, el paquete no puede pasar la [validación del paquete](package-validation.md). Para pasar la validación en este caso, se deben cambiar los datos o el esquema de la base de datos. El único medio para cambiar la longitud de columna de una tabla estándar es exportar la tabla mediante [**MsiDatabaseExport,**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)editar el archivo .idt exportado y, a continuación, importar la tabla mediante [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Los autores no pueden cambiar los tipos de datos de columna, la nulabilidad ni los atributos de localización de ninguna columna de las tablas estándar. Los autores pueden crear tablas personalizadas con columnas que tengan atributos de columna.

Cuando se [**usa MsiDatabaseMerge para**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) combinar una base de datos de referencia en una base de datos de destino, los nombres de columna, el número de claves principales y los tipos de datos de columna deben coincidir. **MsiDatabaseMerge omite** los atributos de localización y longitud de columna. Si una columna de la base de datos de referencia tiene una longitud de 0 o mayor que la longitud de esa columna en la base de datos de destino, **MsiDatabaseMerge** aumenta la longitud de columna de la base de datos de destino a la longitud de la base de datos de referencia.

Cuando se Mergmod.dll versión 2.0, la aplicación de un módulo de combinación a un archivo .msi nunca cambia la longitud de las columnas o los tipos de columna de una tabla de base de datos existente. Sin embargo, la aplicación de un módulo de combinación puede cambiar el esquema de una tabla de base de datos existente si el módulo agrega nuevas columnas a una tabla para la que es válido agregar columnas. Cuando se usa una Mergemod.dll anterior a la versión 2.0, la aplicación de un módulo de combinación nunca cambia la longitud de las columnas y nunca cambia el esquema de la base de datos de destino.

 

 



