---
description: El elemento Param especifica el valor de una propiedad en una transición, un efecto u otro subobjeto.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Elemento Param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb1d007a7f3e2dcffaa7b9163c76be604fed7a9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906737"
---
# <a name="param-element"></a>Elemento Param

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `param` elemento especifica el valor de una propiedad en una transición, efecto u otro subobjeto.

## <a name="attributes"></a>Atributos

[**nombre**](name-attribute.md), [ **valor**](value-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**clip**](clip-element.md), [**efecto**](effect-element.md), [**transición**](transition-element.md) |
| Children | [**en**](at-element.md), [ **lineal**](linear-element.md)                                               |



 

## <a name="remarks"></a>Observaciones

El atributo **Value** especifica el valor de la propiedad al inicio de la transición o efecto. Use el elemento **at** o **linear** para especificar los valores que se van a cambiar. Si el elemento **param** no contiene elementos **en** o **lineales** , el valor permanece constante a lo largo de la duración del efecto o de la transición.

> [!Note]  
> Un elemento **param** dentro de un elemento **clip** no **puede contener elementos** in o **linear** .

 

Muchas transiciones admiten una propiedad de **progreso** estándar que va de 0 a 1,0, que indica el porcentaje de la transición que se refleja en la salida. En **curso** = 0,0, la transición está al principio de su secuencia (completamente la primera imagen de vídeo). En **curso** = 0,5, la transición está completada a la mitad. (Por ejemplo, en un borrado, en **curso** = 0,5 el límite de la transición está en el centro de la imagen) En **curso** = 1,0, la transición se completa (por completo la segunda imagen). De forma predeterminada, las transiciones pasan de **Progress** = 0,0 al inicio de la transición a **Progress** = 1,0 al final.

Otras propiedades suelen ser específicas de una transición o efecto determinado. Por ejemplo, la transición de borrado admite una propiedad **GradientSize** que controla el ancho del área de transición.

Para ejecutar una transición hacia atrás, establezca la propiedad **Progress** en 1,0 al inicio de la transición y use el elemento **linear** para cambiar el valor a 0,0, tal como se muestra en el ejemplo siguiente:


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

 

 



