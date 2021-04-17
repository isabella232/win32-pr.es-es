---
description: 'A continuación se muestra la sintaxis básica de la instrucción SELECT para una consulta local:'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Instrucción SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05832dab0184870a626fa4bce502d908c9b05f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705475"
---
# <a name="select-statement"></a>Instrucción SELECT

A continuación se muestra la sintaxis básica de la instrucción SELECT para una consulta local:


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



A continuación se muestra la parte de la columna de la sintaxis de la instrucción SELECT:


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



Los especificadores de columna deben ser columnas de nombre de propiedad válidos, separados por comas. Los nombres de columna válidos son descripciones de propiedades registradas o se definen mediante el esquema del sistema de propiedades del shell. Puede seleccionar solo las columnas que están marcadas como recuperables en el esquema del sistema de propiedades. Si usa una combinación de mayúsculas y minúsculas mixta para identificar propiedades que no son propiedades definidas por el sistema, debe incluir el especificador de columna entre comillas dobles. Los nombres de propiedad definidos por el sistema incluyen todas las propiedades que comienzan por "System" (por ejemplo, System. contact. FirstName) y no requieren comillas.

> [!Note]  
> También puede escribir los nombres de propiedad definidos por el sistema entre comillas dobles para mejorar la legibilidad. Esto no afecta a la compatibilidad.

 

Cuando la consulta devuelve un documento que no tiene la columna solicitada, el valor de esa columna para el documento es **null**.

Debe proporcionar al menos un nombre de columna en una instrucción SELECT. En la consulta Lenguaje de consulta estructurado (SQL), se le permite usar el asterisco ( \* ) para especificar que se devuelvan todas las columnas de una tabla. Sin embargo, ningún conjunto de propiedades definido y fijo se aplica a todos los documentos. Por esta razón, no se permite el asterisco SQL en el <columns> especificador de la instrucción SELECT.

## <a name="getting-the-top-n-results"></a>Obtener los n resultados principales

Puede especificar un número máximo de resultados que se van a devolver mediante la sintaxis superior:


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a>Convertir tipos de datos de columna

En ocasiones, puede que necesite convertir los datos de cadena extraídos de los documentos como otro tipo de datos para que se pueda realizar una comparación adecuada. Para obtener más información, consulte [conversión del tipo de datos de una columna](-search-sql-castingdatacolumntype.md).

## <a name="examples"></a>Ejemplos

Los ejemplos siguientes devuelven el nombre y la dirección URL de los documentos coincidentes.


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Conversión del tipo de datos de una columna](-search-sql-castingdatacolumntype.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 



