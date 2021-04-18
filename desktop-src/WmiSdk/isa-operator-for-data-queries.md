---
description: Use el operador ISA en la cláusula WHERE de una consulta de datos para solicitar objetos incrustados en una jerarquía de clases.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Operador ISA para consultas de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4c063c99f50a57c8b22a5bbe7040aa3fe96ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687989"
---
# <a name="isa-operator-for-data-queries"></a><span data-ttu-id="9fba6-103">Operador ISA para consultas de datos</span><span class="sxs-lookup"><span data-stu-id="9fba6-103">ISA Operator for Data Queries</span></span>

<span data-ttu-id="9fba6-104">Use el operador ISA en la cláusula WHERE de una consulta de datos para solicitar objetos incrustados en una jerarquía de clases.</span><span class="sxs-lookup"><span data-stu-id="9fba6-104">Use the ISA operator in the WHERE clause of a data query to request embedded objects in a class hierarchy.</span></span>

<span data-ttu-id="9fba6-105">En el ejemplo siguiente se muestra la sintaxis para solicitar objetos incrustados en una jerarquía de clases.</span><span class="sxs-lookup"><span data-stu-id="9fba6-105">The following example shows the syntax to request embedded objects in a class hierarchy.</span></span>


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



<span data-ttu-id="9fba6-106">El resultado incluye instancias de **clase** con objetos incrustados que se derivan de **ParentClass** en la propiedad **EmbeddedProp** .</span><span class="sxs-lookup"><span data-stu-id="9fba6-106">The result includes instances of **Class** having embedded objects that are derived from **ParentClass** in the **EmbeddedProp** property.</span></span> <span data-ttu-id="9fba6-107">No todas las instancias del objeto de **clase** se derivan de **ParentClass**, pero el resultado devuelve los objetos incrustados que se derivan de **ParentClass**.</span><span class="sxs-lookup"><span data-stu-id="9fba6-107">Not every instance of the **Class** object is derived from **ParentClass**, but the result returns the embedded objects that are derived from **ParentClass**.</span></span>

<span data-ttu-id="9fba6-108">Por ejemplo, en la siguiente consulta, **ClassA** incluye la propiedad **EmbeddedObj** débilmente tipada.</span><span class="sxs-lookup"><span data-stu-id="9fba6-108">For example, in the following query, **ClassA** includes the weakly typed **EmbeddedObj** property.</span></span> <span data-ttu-id="9fba6-109">La clase **ClassA** tiene diez instancias.</span><span class="sxs-lookup"><span data-stu-id="9fba6-109">The **ClassA** class has ten instances.</span></span> <span data-ttu-id="9fba6-110">Cinco de esas instancias tienen objetos incrustados con un tipo derivado de **ClassZ**.</span><span class="sxs-lookup"><span data-stu-id="9fba6-110">Five of those instances have embedded objects with a type derived from **ClassZ**.</span></span> <span data-ttu-id="9fba6-111">Los otros cinco tienen objetos incrustados de otros tipos.</span><span class="sxs-lookup"><span data-stu-id="9fba6-111">The other five have embedded objects of other types.</span></span>

<span data-ttu-id="9fba6-112">En el ejemplo siguiente se muestra la consulta que devuelve las cinco instancias, que incluyen los objetos que se derivan de **ClassZ**.</span><span class="sxs-lookup"><span data-stu-id="9fba6-112">The following example shows the query that returns the five instances, which include the objects that are derived from **ClassZ**.</span></span>


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



