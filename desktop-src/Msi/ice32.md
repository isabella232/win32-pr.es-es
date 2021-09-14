---
description: ICE32 valida que las claves y las claves externas del archivo .msi son del mismo tamaño y tipos de definición de columna.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074626"
---
# <a name="ice32"></a>ICE32

ICE32 valida que las claves y las claves externas del archivo .msi son del mismo tamaño y tipos de definición de columna. Esta acción personalizada de ICE realiza la comparación mediante la [ \_ tabla Validation](-validation-table.md) y los tipos de definición devueltos por [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo). Para obtener más información, vea [Formato de definición de columna](column-definition-format.md).

## <a name="result"></a>Resultado

ICE32 publica errores si el archivo .msi contiene claves externas a claves de un tipo de datos de columna o longitud de columna diferente.

## <a name="example"></a>Ejemplo

ICE32 publica dos errores para el ejemplo que se muestra:

-   Hay una clave externa y una clave definidas que difieren en el tamaño.
-   Hay una clave externa y una clave definidas que difieren en su tipo de definición.

[ \_ Tabla de validación](-validation-table.md) (parcial)



| Tabla | Columna  | KeyTable | KeyColumn |
|-------|---------|----------|-----------|
| Archivo  | Version | Archivo     | 1         |
| Aleta  | Column8 | Aleta     | 1         |



 

Definiciones de columna (parcial)



| Tabla | Columna  | Tipo | Size |
|-------|---------|------|------|
| Archivo  | Archivo    | s    | 72   |
| Archivo  | Versión | S    | 32   |
| Aleta  | Columna1 | i    | 2    |
| Aleta  | Column8 | S    | 32   |



 

La columna Version de la tabla File puede ser una clave externa para otro archivo de la tabla File. Esto sucede con archivos complementarios. Sin embargo, la columna Versión solo permite una longitud de cadena 32, mientras que la columna Archivo permite una longitud de cadena de 72. Para corregir este error, cambie las longitudes de cadena para que coincidan.

Hay una clave externa y una clave definidas que difieren en sus tipos de definición. La columna 8 de la tabla de columnas aparece como una clave externa para Column1. Column8 es una columna de cadena y Column1 es una columna entera. Los pares de clave externa y clave deben definirse para que sus tipos de datos coincidan.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



