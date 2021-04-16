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
# <a name="wql-operators"></a><span data-ttu-id="c2d0c-103">Operadores WQL</span><span class="sxs-lookup"><span data-stu-id="c2d0c-103">WQL Operators</span></span>

<span data-ttu-id="c2d0c-104">El lenguaje de consulta de Instrumental de administración de Windows (WQL) admite un conjunto de operadores estándar que se utilizan en la [cláusula WHERE](where-clause.md) de una instrucción SELECT, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="c2d0c-104">The Windows Management Instrumentation Query Language (WQL) supports a set of standard operators that are used in the [WHERE clause](where-clause.md) of a SELECT statement, as follows.</span></span>



| <span data-ttu-id="c2d0c-105">Operator</span><span class="sxs-lookup"><span data-stu-id="c2d0c-105">Operator</span></span>       | <span data-ttu-id="c2d0c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2d0c-106">Description</span></span>              |
|----------------|--------------------------|
| =              | <span data-ttu-id="c2d0c-107">Igual a</span><span class="sxs-lookup"><span data-stu-id="c2d0c-107">Equal to</span></span>                 |
| <           | <span data-ttu-id="c2d0c-108">Menor que</span><span class="sxs-lookup"><span data-stu-id="c2d0c-108">Less than</span></span>                |
| >           | <span data-ttu-id="c2d0c-109">Mayor que</span><span class="sxs-lookup"><span data-stu-id="c2d0c-109">Greater than</span></span>             |
| <=          | <span data-ttu-id="c2d0c-110">Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="c2d0c-110">Less than or equal to</span></span>    |
| >=          | <span data-ttu-id="c2d0c-111">Mayor o igual que</span><span class="sxs-lookup"><span data-stu-id="c2d0c-111">Greater than or equal to</span></span> |
| <span data-ttu-id="c2d0c-112">! = o <></span><span class="sxs-lookup"><span data-stu-id="c2d0c-112">!= or <></span></span> | <span data-ttu-id="c2d0c-113">No es igual a</span><span class="sxs-lookup"><span data-stu-id="c2d0c-113">Not equal to</span></span>             |



 

<span data-ttu-id="c2d0c-114">Hay algunos operadores adicionales específicos de WQL: es, no es, ISA y LIKE.</span><span class="sxs-lookup"><span data-stu-id="c2d0c-114">There are a few additional WQL-specific operators: IS, IS NOT, ISA, and LIKE.</span></span> <span data-ttu-id="c2d0c-115">Los operadores IS y IS NOT son válidos en la cláusula WHERE solo si la constante es **null**.</span><span class="sxs-lookup"><span data-stu-id="c2d0c-115">The IS and IS NOT operators are valid in the WHERE clause only if the constant is **NULL**.</span></span> <span data-ttu-id="c2d0c-116">Por ejemplo, las siguientes consultas son válidas:</span><span class="sxs-lookup"><span data-stu-id="c2d0c-116">For example, the following queries are valid:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



<span data-ttu-id="c2d0c-117">Las siguientes consultas muestran usos no válidos de IS y no es:</span><span class="sxs-lookup"><span data-stu-id="c2d0c-117">The following queries show invalid uses of IS and IS NOT:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



<span data-ttu-id="c2d0c-118">El operador ISA se usa en la cláusula WHERE de las consultas de datos y eventos para probar los objetos incrustados de una jerarquía de clases.</span><span class="sxs-lookup"><span data-stu-id="c2d0c-118">The ISA operator is used in the WHERE clause of data and event queries to test embedded objects for a class hierarchy.</span></span> <span data-ttu-id="c2d0c-119">El operador ISA elimina la necesidad de realizar un seguimiento de las clases derivadas recién al solicitar una jerarquía de clases.</span><span class="sxs-lookup"><span data-stu-id="c2d0c-119">The ISA operator eliminates the need for keeping track of newly derived classes when requesting a hierarchy of classes.</span></span> <span data-ttu-id="c2d0c-120">Al utilizar ISA, las subclases recién creadas y existentes de la clase solicitada se incluyen automáticamente en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c2d0c-120">When you use ISA, newly created and existing subclasses of the requested class are automatically included in the result set.</span></span>

<span data-ttu-id="c2d0c-121">Para obtener más información sobre la sintaxis y el uso de este operador, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="c2d0c-121">For more information about the syntax and use of this operator, see the following topics:</span></span>

-   [<span data-ttu-id="c2d0c-122">Operador ISA para consultas de datos</span><span class="sxs-lookup"><span data-stu-id="c2d0c-122">ISA Operator for Data Queries</span></span>](isa-operator-for-data-queries.md)
-   [<span data-ttu-id="c2d0c-123">Operador ISA para consultas de eventos</span><span class="sxs-lookup"><span data-stu-id="c2d0c-123">ISA Operator for Event Queries</span></span>](isa-operator-for-event-queries.md)
-   [<span data-ttu-id="c2d0c-124">Operador ISA para consultas de esquema</span><span class="sxs-lookup"><span data-stu-id="c2d0c-124">ISA Operator for Schema Queries</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="c2d0c-125">El operador LIKE es válido en la cláusula WHERE y se utiliza para determinar si una cadena de caracteres determinada coincide con un patrón especificado.</span><span class="sxs-lookup"><span data-stu-id="c2d0c-125">The LIKE operator is valid in the WHERE clause and is used to determine whether a given character string matches a specified pattern.</span></span> <span data-ttu-id="c2d0c-126">Por ejemplo, la consulta siguiente devuelve todas las instancias de \_ clases Win32.</span><span class="sxs-lookup"><span data-stu-id="c2d0c-126">For example, the following query returns all instances of Win32\_ classes.</span></span>


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



<span data-ttu-id="c2d0c-127">Para obtener más información sobre la sintaxis y el uso de este operador, vea [like (operador](like-operator.md)).</span><span class="sxs-lookup"><span data-stu-id="c2d0c-127">For more information about the syntax and use of this operator, see [LIKE Operator](like-operator.md).</span></span>

 

 



