---
description: Describe los operadores WQL utilizados en la cláusula WHERE o en la instrucción SELECT.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: Operadores WQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5cc37d03884a3609abf3f76d2c78ba22b3c9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716189"
---
# <a name="wql-operators"></a>Operadores WQL

El lenguaje de consulta de Instrumental de administración de Windows (WQL) admite un conjunto de operadores estándar que se utilizan en la [cláusula WHERE](where-clause.md) de una instrucción SELECT, como se indica a continuación.



| Operator       | Descripción              |
|----------------|--------------------------|
| =              | Igual a                 |
| <           | Menor que                |
| >           | Mayor que             |
| <=          | Menor o igual que    |
| >=          | Mayor o igual que |
| ! = o <> | No es igual a             |



 

Hay algunos operadores adicionales específicos de WQL: es, no es, ISA y LIKE. Los operadores IS y IS NOT son válidos en la cláusula WHERE solo si la constante es **null**. Por ejemplo, las siguientes consultas son válidas:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



Las siguientes consultas muestran usos no válidos de IS y no es:


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



El operador ISA se usa en la cláusula WHERE de las consultas de datos y eventos para probar los objetos incrustados de una jerarquía de clases. El operador ISA elimina la necesidad de realizar un seguimiento de las clases derivadas recién al solicitar una jerarquía de clases. Al utilizar ISA, las subclases recién creadas y existentes de la clase solicitada se incluyen automáticamente en el conjunto de resultados.

Para obtener más información sobre la sintaxis y el uso de este operador, vea los temas siguientes:

-   [Operador ISA para consultas de datos](isa-operator-for-data-queries.md)
-   [Operador ISA para consultas de eventos](isa-operator-for-event-queries.md)
-   [Operador ISA para consultas de esquema](isa-operator-for-schema-queries.md)

El operador LIKE es válido en la cláusula WHERE y se utiliza para determinar si una cadena de caracteres determinada coincide con un patrón especificado. Por ejemplo, la consulta siguiente devuelve todas las instancias de \_ clases Win32.


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



Para obtener más información sobre la sintaxis y el uso de este operador, vea [like (operador](like-operator.md)).

 

 



