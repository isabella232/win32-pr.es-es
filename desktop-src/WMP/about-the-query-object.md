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
# <a name="about-the-query-object"></a>Acerca del objeto de consulta

El objeto de **consulta** representa una consulta compuesta. Cree un nuevo objeto de **consulta** vacío llamando a *mediaCollection*. **createQuery**. Después de crear un objeto de **consulta** , puede llamar a **addCondition** para agregar una condición a la consulta compuesta. Cada llamada subsiguiente a **addCondition** anexa una nueva condición a la consulta existente mediante la lógica y.

Por ejemplo, supongamos que desea crear una consulta que represente todos los medios digitales en los que **WM/Genre** es igual a "Jazz" y el **autor** contiene "Jim". Puede crear una consulta compuesta para representar estas condiciones mediante el siguiente código JScript:


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



Para agregar una condición a una consulta compuesta mediante lógica OR, debe llamar a **query. beginNextGroup**. Este método indica que el grupo de condiciones anterior se ha completado y que la siguiente llamada a **addCondition** representa el inicio de un nuevo grupo de condiciones.

Por ejemplo, para crear una consulta que represente todos los medios digitales en los que **WM/Genre** es igual a "Jazz" y el **autor** contiene "Jim" o **Author** contiene "Dave", podría usar el código de ejemplo siguiente:


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



Para ejecutar la consulta compuesta, llame a **MediaCollection. getPlaylistByQuery**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Query (objeto)**](query-object.md)
</dt> </dl>

 

 




