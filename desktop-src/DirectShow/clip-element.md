---
description: El clip epecifica un origen multimedia.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: clip (Elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b94ffdbd3d9b49d961cdefdd64de9a212858c5da4859c3beddb77db0ab732d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655519"
---
# <a name="clip-element"></a>clip (Elemento)

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

`clip`epecifica un origen multimedia.

## <a name="attributes"></a>Atributos

[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



| Etiqueta | Value |
|----------|----------------------------------|
| Parent   | [**track**](track-element.md)   |
| Children | [**Efecto**](effect-element.md) |



 

## <a name="remarks"></a>Observaciones

El **atributo clsid** especifica el CLSID de un filtro de origen que se usará como origen. No especifique los atributos **src** **y clsid** dentro del mismo `clip` elemento.

Especifique al menos un atributo de hora de inicio **(start** o **mstart)** y un atributo de tiempo de detenerse **(stop** o **mstop).** Si uno de los atributos de hora de inicio no está especificado, el valor predeterminado es 0 (el principio de la escala de tiempo para **start** o el principio del clip para **mstart).** Si uno de los atributos de tiempo de detenerse no está especificado, DES asume una velocidad de reproducción normal y calcula el tiempo de detenerse no especificado en consecuencia. Si se especifican ambos tiempos de detenerse, la reproducción es más rápida o más lenta de lo normal, si es necesario.

En el ejemplo siguiente, la duración de la escala de tiempo es de siete segundos **(detener** menos **iniciar**). Se supone que la velocidad de reproducción es normal, por lo que el tiempo de detenerse de los medios es predeterminado de 10 segundos (la duración más **mstart).**


```
<clip start="2" stop="9" mstart="3" />
```



En el ejemplo siguiente, el valor predeterminado de la hora de inicio del medio es 0, lo que obliga a que la duración del medio sea de 10 segundos. La duración de la escala de tiempo es de cinco segundos, por lo que el clip se reproduce al doble de la velocidad normal.


```
<clip start="5" stop="10" mstop="10" />  
```



Si el **atributo src** especifica una imagen fija, DES intenta cargar una serie de imágenes fijas para crear una animación. Por ejemplo, si el **atributo src** IMAGE001.BMP, DES busca IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, y así sucesivamente. Suponiendo que existen, se muestran en orden numérico secuencial, a la velocidad especificada por el atributo **framerate.**

## <a name="examples"></a>Ejemplos


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



