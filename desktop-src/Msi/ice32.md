---
description: ICE32 valida que las claves y las claves externas del archivo. msi tienen el mismo tamaño y tipos de definición de columna.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667756"
---
# <a name="ice32"></a>ICE32

ICE32 valida que las claves y las claves externas del archivo. msi tienen el mismo tamaño y tipos de definición de columna. Esta acción personalizada de ICE realiza la comparación mediante la [ \_ tabla de validación](-validation-table.md) y usando los tipos de definición devueltos por [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo). Para obtener más información, vea [formato de definición de columna](column-definition-format.md).

## <a name="result"></a>Resultado

ICE32 expone errores si el archivo. msi contiene claves externas a claves de una longitud de columna o un tipo de datos de columna diferentes.

## <a name="example"></a>Ejemplo

ICE32 expone dos errores para el ejemplo mostrado:

-   Hay una clave externa y una clave definidas que difieren en tamaño.
-   Hay una clave externa y una clave definidas que difieren en su tipo de definición.

[ \_ Tabla de validación](-validation-table.md) (parcial)



| Tabla | Columna  | KeyTable | KeyColumn |
|-------|---------|----------|-----------|
| Archivo  | Version | Archivo     | 1         |
| Flap  | Column8 | Flap     | 1         |



 

Definiciones de columna (Partial)



| Tabla | Columna  | Tipo | Size |
|-------|---------|------|------|
| Archivo  | Archivo    | s    | 72   |
| Archivo  | Versión | S    | 32   |
| Flap  | Columna1 | i    | 2    |
| Flap  | Column8 | S    | 32   |



 

La columna versión de la tabla de archivos puede ser una clave externa a otro archivo de la tabla de archivos. Esto ocurre con los archivos complementarios. Sin embargo, la columna versión solo permite una longitud de cadena de 32, mientras que la columna archivo permite una longitud de cadena de 72. Para corregir este error, cambie las longitudes de cadena para que coincidan.

Hay una clave externa y una clave definidas que difieren en sus tipos de definición. Column8 de la tabla flap aparece como una clave externa a Columna1. Column8 es una columna de cadena y Column1 es una columna de tipo entero. Se deben definir los pares de clave externa y de clave para que sus tipos de datos coincidan.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



