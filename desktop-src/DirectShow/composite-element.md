---
description: El elemento compuesto define una composición, un objeto contenedor para pistas y otras composiciones anidadas.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: elemento composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5eff3e0c16040f837e4c8a792ebac3124d723d1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908843"
---
# <a name="composite-element"></a>elemento composite

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `composite` elemento define una composición, un objeto contenedor para pistas y otras composiciones anidadas.

## <a name="attributes"></a>Atributos

[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



| Etiqueta | Value |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Parent   | `composite`, [ **group**](group-element.md)                                                                             |
| Children | `composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md) |



 

## <a name="remarks"></a>Comentarios

Dentro de un elemento, la prioridad de las capas anidadas viene determinada implícitamente por `composite` el orden en que aparecen dentro del elemento. La primera capa tiene prioridad 0 y las capas posteriores tienen valores de prioridad crecientes.

## <a name="examples"></a>Ejemplos


```XML
<composite> </composite>
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



