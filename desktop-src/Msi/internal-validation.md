---
description: Al crear un paquete de instalación, puede utilizar la función MsiViewModify o el método View. Modify para asegurarse de que los datos que especifique son sintácticamente correctos.
ms.assetid: c960e9df-dcd6-44d2-8662-40a1dea81f45
title: Validación interna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3c1a9e6f7b7e35b4d7d91287af64eff7812de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153875"
---
# <a name="internal-validation"></a>Validación interna

Al crear un paquete de instalación, puede utilizar la función [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o el método View. Modify para asegurarse de que los datos que especifique son sintácticamente correctos. Para obtener más información, vea [**Modify Method**](view-modify.md). En el nivel más bajo, la columna de una tabla de base de datos puede almacenar enteros (cortos o largos), cadenas o datos binarios. Sin embargo, un paquete de instalación requiere cadenas o enteros específicos en determinadas tablas. Estas especificaciones se mantienen en la [ \_ tabla de validación](-validation-table.md). Por ejemplo, la columna FileName de la [tabla de archivos](file-table.md) es una columna de cadena, pero almacena específicamente un nombre de archivo. Por lo tanto, no solo debe ser una cadena, sino que también debe seguir los requisitos para asignar nombres a los archivos.

Los distintos valores de enumeración de validación utilizados con la función [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) permiten la validación inmediata en diferentes niveles. La \_ \_ enumeración de campo MSIMODIFY Validate se puede usar para validar campos individuales de un registro. No valida las claves externas. La \_ enumeración Validate de MSIMODIFY valida una fila completa e incluye la validación de clave externa. Si va a insertar una nueva fila en una tabla, use la \_ \_ nueva enumeración MSIMODIFY Validate para comprobar que está agregando datos válidos, así como claves principales únicas. Se produce un error en una inserción si las claves principales no son únicas. Si una llamada a **MsiViewModify** con una de las enumeraciones de validación devuelve un error, puede realizar llamadas repetidas a [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) para diagnosticar el problema. **MsiViewGetError** indica la columna donde se produjo el error, así como el valor de enumeración para ayudar a solucionar el problema. Para obtener más información, vea [**método GetError**](view-geterror.md).

También puede usar la validación interna para asegurarse de que otros autores escriban los datos correctamente en la tabla personalizada. Agregue cada una de las columnas de la tabla personalizada a la \_ tabla de validación con el nombre de la tabla y el nombre de la columna personalizados como clave principal. Proporcione una descripción o propósito de cada columna en la columna Descripción de la \_ tabla de validación. Especifique los requisitos aplicables para cada columna mediante las columnas Nullable, MinValue, MaxValue, KeyTable, KeyColumn, Category y set:

-   Si la columna acepta valores NULL, escriba una ' Y '. Si no es así, escriba una ' N '.
-   Si la columna es una columna de enteros y puede contener un intervalo de enteros, especifique ese intervalo mediante las columnas MinValue y MaxValue.
-   Las columnas de clave externa se identifican mediante las columnas KeyTable y KeyColumn.
-   En el caso de las columnas de cadena, especifique una categoría como nombre de archivo, GUID o identificador. Para obtener más información, vea [tipos de datos de columna](column-data-types.md).
-   Si los datos solo pueden pertenecer a un número específico de valores (string o Integer), use la columna set para enumerar los valores aceptables.

A continuación se muestra una lista de las columnas (además de tabla, columna y descripción) de la \_ tabla de validación que se pueden rellenar si la columna es del tipo especificado. (Tenga en cuenta que no tiene que rellenar todas las columnas).



| Tipo    | Columnas                                                          |
|---------|------------------------------------------------------------------|
| Entero | Nullable, MinValue, MaxValue, KeyTable, KeyColumn, Set           |
| String  | Nullable, KeyTable, KeyColumn, Category, Set, MinValue, MaxValue |
| Binary  | Categoría que acepta valores NULL (la categoría debe ser "binaria")                   |



 

Los entornos de creación pueden usar MSIMODIFY \_ Validate \_ Delete. En esta enumeración se supone que desea eliminar la fila. No se realiza ninguna validación de campo ni de clave externa. En realidad, esta enumeración realiza una validación de clave externa inversa. Comprueba en la \_ tabla de validación las referencias de las columnas KeyTable y KeyColumn de la tabla a la que pertenece la fila "DELETED". Si hay columnas que muestran la tabla que contiene la fila "DELETED" como clave externa potencial, recorre la columna para ver si alguno de los valores hace referencia a los valores de la fila "DELETED". Una devolución de error significa que se interrumpe la integridad relacional de la base de datos mediante la eliminación de la fila.

 

 



