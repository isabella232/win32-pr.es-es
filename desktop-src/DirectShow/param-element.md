---
description: El elemento param especifica el valor de una propiedad en una transición, un efecto u otro subobjeto.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: elemento param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a10f902e85066f6cea14023e8cff9250126add0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909043"
---
# <a name="param-element"></a>elemento param

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `param` elemento especifica el valor de una propiedad en una transición, un efecto u otro subobjeto.

## <a name="attributes"></a>Atributos

[**name**](name-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



| Etiqueta | Value |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md) |
| Children | [**en**](at-element.md), [ **lineal**](linear-element.md)                                               |



 

## <a name="remarks"></a>Comentarios

El **atributo** value especifica el valor de la propiedad al principio de la transición o efecto. Use el **elemento en** o **lineal** para especificar valores cambiantes. Si el **elemento param** no contiene elementos **en** o **lineales,** el valor permanece constante durante la duración del efecto o la transición.

> [!Note]  
> Un **elemento param** dentro de un **elemento clip** no puede contener elementos **en** o **lineales.**

 

Muchas transiciones admiten una propiedad **Progress** estándar que oscila entre 0 y 1,0, lo que indica qué porcentaje de la transición se refleja en la salida. En **Progreso** = 0,0, la transición está al principio de su secuencia (completamente la primera imagen de vídeo). En **Progreso** = 0,5, la transición se completa a la mitad. (Por ejemplo, en un borrado, en **Progreso** = 0,5, el límite de transición está en el centro de la imagen) En **Progreso** = 1.0, la transición se completa (completamente la segunda imagen). De forma predeterminada, las transiciones van desde **Progreso** = 0,0 al principio de la transición a **Progreso** = 1,0 al final.

Otras propiedades suelen ser específicas de una transición o efecto determinados. Por ejemplo, la transición de borrado admite una **propiedad GradientSize** que controla el ancho del área de transición.

Para ejecutar una transición hacia atrás, establezca la propiedad **Progress** en 1.0 al principio de la transición y use el elemento **lineal** para cambiar el valor a 0.0, como se muestra en el ejemplo siguiente:


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a>Ejemplos


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



