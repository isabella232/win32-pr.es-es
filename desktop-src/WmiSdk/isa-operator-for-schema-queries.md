---
description: El operador ISA es un operador específico de WQL que se puede usar en consultas de datos, eventos y esquemas.
ms.assetid: 0520470c-ebfc-4c45-8a1f-47fd66bf8414
ms.tgt_platform: multiple
title: Operador ISA para consultas de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb50146e4bd1219712c84bc1acec7fc7d50146b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687986"
---
# <a name="isa-operator-for-schema-queries"></a>Operador ISA para consultas de esquema

El operador ISA es un operador específico de WQL que se puede usar en consultas de datos, eventos y esquemas.

Cuando ISA se incluye en la [cláusula WHERE](where-clause.md) de una consulta de esquema, solicita que la consulta se aplique a todas las subclases de la clase especificada.

Por ejemplo, la siguiente instrucción solicita una notificación cada 10 minutos de eventos de modificación de instancia para todas las instancias que son miembros de cualquier clase derivada de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



La consulta siguiente devuelve la definición de la clase de [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor) y las definiciones de todas sus subclases.


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



La clase **meta \_** lo identifica como una consulta de esquema, la propiedad a la que **\_ \_ se** identifica la clase de destino de la consulta y el operador ISA solicita las definiciones de las subclases de la clase de destino.

 

 
