---
description: Describe los operadores WQL usados en la cláusula WHERE o la instrucción SELECT.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: Operadores WQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a441afb661e4f8d92e21d944462dddd6d7390fd2dbe871512342f7c9251d6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553092"
---
# <a name="wql-operators"></a>Operadores WQL

El Windows lenguaje de consulta de instrumentación de administración de recursos (WQL) admite un conjunto de operadores estándar que se usan en la cláusula [WHERE](where-clause.md) de una instrucción SELECT, como se muestra a continuación.



| Operator       | Descripción              |
|----------------|--------------------------|
| =              | Igual a                 |
| <           | Menor que                |
| >           | Mayor que             |
| <=          | Menor o igual que    |
| >=          | Mayor o igual que |
| != o <> | No es igual a             |



 

Hay algunos operadores específicos de WQL adicionales: IS, IS NOT, ISA y LIKE. Los operadores IS y IS NOT solo son válidos en la cláusula WHERE si la constante es **NULL.** Por ejemplo, las consultas siguientes son válidas:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



Las consultas siguientes muestran usos no válidos de IS y IS NOT:


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



El operador ISA se usa en la cláusula WHERE de las consultas de datos y eventos para probar objetos incrustados para una jerarquía de clases. El operador ISA elimina la necesidad de realizar un seguimiento de las clases recién derivadas al solicitar una jerarquía de clases. Cuando se usa ISA, las subclases recién creadas y existentes de la clase solicitada se incluyen automáticamente en el conjunto de resultados.

Para obtener más información sobre la sintaxis y el uso de este operador, vea los temas siguientes:

-   [Operador ISA para consultas de datos](isa-operator-for-data-queries.md)
-   [Operador ISA para consultas de eventos](isa-operator-for-event-queries.md)
-   [Operador ISA para consultas de esquema](isa-operator-for-schema-queries.md)

El operador LIKE es válido en la cláusula WHERE y se usa para determinar si una cadena de caracteres determinada coincide con un patrón especificado. Por ejemplo, la consulta siguiente devuelve todas las instancias de clases \_ Win32.


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



Para obtener más información sobre la sintaxis y el uso de este operador, vea [Operador LIKE](like-operator.md).

 

 



