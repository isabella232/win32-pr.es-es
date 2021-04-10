---
description: La función DATEADD realiza los cálculos de fecha y hora de las propiedades coincidentes que tienen tipos de fecha. Utilice la función DATEADD para obtener fechas y horas en un período de tiempo especificado antes de la presente.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: Función DATEADD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153962"
---
# <a name="dateadd-function"></a>Función DATEADD

La función DATEADD realiza los cálculos de fecha y hora de las propiedades coincidentes que tienen tipos de fecha. Utilice la función DATEADD para obtener fechas y horas en un período de tiempo especificado antes de la presente.

## <a name="syntax"></a>Sintaxis


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a>Argumentos

*DateTimeUnits*

Especifica las unidades del parámetro de *fecha* y hora: año, trimestre, mes, semana, día, hora, minuto o segundo. Este valor distingue entre mayúsculas y minúsculas y no se necesitan comillas alrededor del parámetro.

*OffsetValue*

Especifica el desplazamiento de tiempo, en las unidades especificadas por el parámetro *DateTimeUnits* . **OffsetValue** debe ser un entero negativo. No se admiten valores positivos.

*DateTime*

Especifica una marca de tiempo de la que se va a calcular el desplazamiento. No puede ser un literal de fecha. Debe ser GETGMTDATE o el resultado de otra función DATEADD.

## <a name="remarks"></a>Observaciones

La función DATEADD solo se puede usar en comparaciones de valores literales y solo en el lado derecho del operador de comparación.

La función GETGMTDATE devuelve la fecha y hora actuales en la hora del meridiano de Greenwich (GMT). Recuerde que este valor puede no ser el mismo que el de la hora local del equipo.

No use el operador de comparación es igual a (=) porque la representación de tiempo interna puede producir errores de redondeo que producen resultados de coincidencia inesperados.

Puede usar varias funciones DATEADD para combinar unidades de desplazamiento.

### <a name="examples"></a>Ejemplos

La cláusula WHERE de ejemplo siguiente coincide con los documentos que se modificaron en los últimos cinco días:


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



En el ejemplo siguiente, la cláusula WHERE coincide con los documentos que se modificaron en los últimos dos días y cuatro horas:


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Comparación de valores literales](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Comparaciones de varios valores (matriz)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



