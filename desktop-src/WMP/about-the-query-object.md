---
title: Acerca del objeto de consulta
description: Acerca del objeto de consulta
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Reproductor de Windows Media,Objeto Query
- Reproductor de Windows Media modelo de objetos, objeto Query
- object model,Query object
- Reproductor de Windows Media ActiveX control, objeto Query
- ActiveX control, objeto Query
- Reproductor de Windows Media Control de ActiveX móvil,objeto Query
- Reproductor de Windows Media Mobile,Query (objeto)
- Query (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d649263f981d02e106466c6e0fcada99c316054d4bf6e0acc0faca641c75dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470405"
---
# <a name="about-the-query-object"></a>Acerca del objeto de consulta

El **objeto Query** representa una consulta compuesta. Para crear un nuevo objeto **Query** vacío, llame *a mediaCollection*. **createQuery**. Después de crear un **objeto Query,** puede llamar a **addCondition** para agregar una condición a la consulta compuesta. Cada llamada subsiguiente **a addCondition** anexa una nueva condición a la consulta existente mediante la lógica AND.

Por ejemplo, supongamos que quiere crear una consulta que represente todos los medios digitales donde **WM/Genre** sea igual a "Jazz" y **Author** contenga "Jim". Puede crear una consulta compuesta para representar estas condiciones mediante el código JScript siguiente:


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



Para agregar una condición a una consulta compuesta mediante la lógica OR, debe llamar a **Query.beginNextGroup**. Este método indica que se ha completado el grupo de condiciones anterior y que la siguiente llamada a **addCondition** representa el inicio de un nuevo grupo de condiciones.

Por ejemplo, para crear una consulta que represente todos los medios digitales donde **WM/Genre** es igual a "Jazz" y **Author** contiene "Jim" o **Author** contiene "Dave", puede usar el código de ejemplo siguiente:


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



Para ejecutar la consulta compuesta, llame **a MediaCollection.getPlaylistByQuery**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Objeto Query**](query-object.md)
</dt> </dl>

 

 




