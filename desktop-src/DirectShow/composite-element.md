---
description: El elemento compuesto define una composición, un objeto contenedor para pistas y otras composiciones anidadas.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: elemento composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec9ce7c889829ee227ce31df25d5d17985e877ed107870170f6939aebf14fd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084315"
---
# <a name="composite-element"></a>elemento composite

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

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

 

 



