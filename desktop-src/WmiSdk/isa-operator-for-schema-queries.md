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
# <a name="isa-operator-for-schema-queries"></a><span data-ttu-id="c55c6-103">Operador ISA para consultas de esquema</span><span class="sxs-lookup"><span data-stu-id="c55c6-103">ISA Operator for Schema Queries</span></span>

<span data-ttu-id="c55c6-104">El operador ISA es un operador específico de WQL que se puede usar en consultas de datos, eventos y esquemas.</span><span class="sxs-lookup"><span data-stu-id="c55c6-104">The ISA operator is a WQL-specific operator that can be used in data, event, and schema queries.</span></span>

<span data-ttu-id="c55c6-105">Cuando ISA se incluye en la [cláusula WHERE](where-clause.md) de una consulta de esquema, solicita que la consulta se aplique a todas las subclases de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="c55c6-105">When ISA is included in the [WHERE clause](where-clause.md) of an schema query, it requests that the query be applied to all subclasses of the class you specify.</span></span>

<span data-ttu-id="c55c6-106">Por ejemplo, la siguiente instrucción solicita una notificación cada 10 minutos de eventos de modificación de instancia para todas las instancias que son miembros de cualquier clase derivada de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="c55c6-106">For example, the following statement requests notification every 10 minutes of instance modification events for all instances that are members of any class deriving from the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="c55c6-107">La consulta siguiente devuelve la definición de la clase de [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor) y las definiciones de todas sus subclases.</span><span class="sxs-lookup"><span data-stu-id="c55c6-107">The following query returns the definition for the [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor) class and definitions for all of its subclasses.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



<span data-ttu-id="c55c6-108">La clase **meta \_** lo identifica como una consulta de esquema, la propiedad a la que **\_ \_ se** identifica la clase de destino de la consulta y el operador ISA solicita las definiciones de las subclases de la clase de destino.</span><span class="sxs-lookup"><span data-stu-id="c55c6-108">The class **meta\_class** identifies this as a schema query, the property called **\_\_this** identifies the target class of the query, and the ISA operator requests definitions for the subclasses of the target class.</span></span>

 

 
