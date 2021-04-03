---
title: Acerca del objeto de consulta
description: Acerca del objeto de consulta
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Media Player de Windows, objeto de consulta
- Modelo de objetos de Windows Media Player, objeto de consulta
- modelo de objetos, Query (objeto)
- Control ActiveX de Windows Media Player, objeto de consulta
- Control ActiveX, Query (objeto)
- Control ActiveX móvil de Windows Media Player, objeto de consulta
- Windows Media Player Mobile, objeto de consulta
- Query (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a26f60c38e053b91c7e56f5cbd7ccaf2ba0fe2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776327"
---
# <a name="about-the-query-object"></a><span data-ttu-id="dd739-111">Acerca del objeto de consulta</span><span class="sxs-lookup"><span data-stu-id="dd739-111">About the Query Object</span></span>

<span data-ttu-id="dd739-112">El objeto de **consulta** representa una consulta compuesta.</span><span class="sxs-lookup"><span data-stu-id="dd739-112">The **Query** object represents a compound query.</span></span> <span data-ttu-id="dd739-113">Cree un nuevo objeto de **consulta** vacío llamando a *mediaCollection*. **createQuery**.</span><span class="sxs-lookup"><span data-stu-id="dd739-113">You create a new, empty **Query** object by calling *mediaCollection*.**createQuery**.</span></span> <span data-ttu-id="dd739-114">Después de crear un objeto de **consulta** , puede llamar a **addCondition** para agregar una condición a la consulta compuesta.</span><span class="sxs-lookup"><span data-stu-id="dd739-114">After you have created a **Query** object, you can call **addCondition** to add a condition to the compound query.</span></span> <span data-ttu-id="dd739-115">Cada llamada subsiguiente a **addCondition** anexa una nueva condición a la consulta existente mediante la lógica y.</span><span class="sxs-lookup"><span data-stu-id="dd739-115">Each subsequent call to **addCondition** appends a new condition to the existing query using AND logic.</span></span>

<span data-ttu-id="dd739-116">Por ejemplo, supongamos que desea crear una consulta que represente todos los medios digitales en los que **WM/Genre** es igual a "Jazz" y el **autor** contiene "Jim".</span><span class="sxs-lookup"><span data-stu-id="dd739-116">For example, suppose you want to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim".</span></span> <span data-ttu-id="dd739-117">Puede crear una consulta compuesta para representar estas condiciones mediante el siguiente código JScript:</span><span class="sxs-lookup"><span data-stu-id="dd739-117">You could create a compound query to represent these conditions by using the following JScript code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



<span data-ttu-id="dd739-118">Para agregar una condición a una consulta compuesta mediante lógica OR, debe llamar a **query. beginNextGroup**.</span><span class="sxs-lookup"><span data-stu-id="dd739-118">To add a condition to a compound query using OR logic, you must call **Query.beginNextGroup**.</span></span> <span data-ttu-id="dd739-119">Este método indica que el grupo de condiciones anterior se ha completado y que la siguiente llamada a **addCondition** representa el inicio de un nuevo grupo de condiciones.</span><span class="sxs-lookup"><span data-stu-id="dd739-119">This method signals that the previous condition group is completed and that the next call to **addCondition** represents the start of a new condition group.</span></span>

<span data-ttu-id="dd739-120">Por ejemplo, para crear una consulta que represente todos los medios digitales en los que **WM/Genre** es igual a "Jazz" y el **autor** contiene "Jim" o **Author** contiene "Dave", podría usar el código de ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="dd739-120">For example, to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim" or **Author** contains "Dave", you could use the following example code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");

// Start the next condition group. This group will be
// combined with the previous group using a logical OR operation.
Query.beginNextGroup();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Dave");
```



<span data-ttu-id="dd739-121">Para ejecutar la consulta compuesta, llame a **MediaCollection. getPlaylistByQuery**.</span><span class="sxs-lookup"><span data-stu-id="dd739-121">To execute your compound query, call **MediaCollection.getPlaylistByQuery**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd739-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd739-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd739-123">**MediaCollection.getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="dd739-123">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="dd739-124">**Modelo de objetos del reproductor para lenguajes de scripting**</span><span class="sxs-lookup"><span data-stu-id="dd739-124">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="dd739-125">**Query (objeto)**</span><span class="sxs-lookup"><span data-stu-id="dd739-125">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 




