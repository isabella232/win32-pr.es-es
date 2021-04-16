---
description: El elemento compuesto define una composición, un objeto contenedor para las pistas y otras composiciones anidadas.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Elemento compuesto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677077"
---
# <a name="composite-element"></a>Elemento compuesto

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `composite` elemento define una composición, un objeto contenedor para pistas y otras composiciones anidadas.

## <a name="attributes"></a>Atributos

[**Lock**](lock-attribute.md), [**MUTE**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Parent   | `composite`, [ **Grupo**](group-element.md)                                                                             |
| Children | `composite`, [**efecto**](effect-element.md), [**seguimiento**](track-element.md), [**transición**](transition-element.md) |



 

## <a name="remarks"></a>Observaciones

Dentro de un `composite` elemento, la prioridad de las capas anidadas viene determinada implícitamente por el orden en que aparecen dentro del elemento. La primera capa tiene prioridad 0 y las capas siguientes tienen valores de prioridad crecientes.

## <a name="examples"></a>Ejemplos


```XML
<composite> </composite>
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



