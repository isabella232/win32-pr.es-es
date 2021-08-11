---
description: 'A continuación se muestra la sintaxis básica de la instrucción SELECT para una consulta local:'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Instrucción SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df8cc5f4b6bab673d20c981e44386d3fdbd651b5a2753d8c965ee55023a6562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227200"
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



Los especificadores de columna deben ser columnas de nombre de propiedad válidas, separadas por comas. Los nombres de columna válidos son descripciones de propiedades registradas o se definen mediante el esquema del sistema de propiedades del shell. Solo puede seleccionar las columnas marcadas como recuperables en el esquema del sistema de propiedades. Si usa mayúsculas y minúsculas mixtas para identificar propiedades que no son propiedades definidas por el sistema, debe incluir el especificador de columna entre comillas dobles. Los nombres de propiedad definidos por el sistema incluyen todas las propiedades que comienzan por "System" (por ejemplo, System.Contact.FirstName) y no requieren comillas.

> [!Note]  
> También puede incluir nombres de propiedad definidos por el sistema entre comillas dobles para mejorar la legibilidad. Esto no afecta a la compatibilidad.

 

Cuando la consulta devuelve un documento que no tiene la columna solicitada, el valor de esa columna para el documento es **NULL.**

Debe proporcionar al menos un nombre de columna en una instrucción SELECT. En la Lenguaje de consulta estructurado (SQL), puede usar el asterisco ( ) para especificar que se van a devolver todas las columnas \* de una tabla. Sin embargo, no se aplica ningún conjunto definido y fijo de propiedades a todos los documentos. Por este motivo, no SQL asterisco en el <columns> especificador de la instrucción SELECT.

## <a name="getting-the-top-n-results"></a>Obtención de los n primeros resultados

Puede especificar un número máximo de resultados para devolver mediante la sintaxis TOP:


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a>Tipos de datos de columna de conversión

En ocasiones, es posible que tenga que convertir los datos de cadena extraídos de los documentos como otro tipo de datos para que se pueda realizar una comparación adecuada. Para obtener más información, consulte [Conversión del tipo de datos de una columna](-search-sql-castingdatacolumntype.md).

## <a name="examples"></a>Ejemplos

Los ejemplos siguientes devuelven el nombre y la dirección URL de los documentos correspondientes.


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Convertir el tipo de datos de una columna](-search-sql-castingdatacolumntype.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 



