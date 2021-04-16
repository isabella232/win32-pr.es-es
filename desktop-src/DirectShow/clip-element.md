---
description: El clip epecifies un origen multimedia.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Elemento clip
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe975113f370b13e50ba695d6fb3388a43c3a74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494500"
---
# <a name="clip-element"></a>Elemento clip

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

`clip`Epecifies un origen de medios.

## <a name="attributes"></a>Atributos

[**CLSID**](clsid-attribute.md), [**velocidad de fotogramas**](framerate-attribute.md), [**bloqueo**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**silenciar**](mute-attribute.md), [**src**](src-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**Stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



|          |                                  |
|----------|----------------------------------|
| Parent   | [**track**](track-element.md)   |
| Children | [**realizado**](effect-element.md) |



 

## <a name="remarks"></a>Observaciones

El atributo **CLSID** especifica el CLSID de un filtro de origen que se va a utilizar como origen. No especifique los atributos **src** y **CLSID** en el mismo `clip` elemento.

Especifique al menos un atributo de tiempo de inicio (**Start** o **mstart**) y un atributo de tiempo de parada (**Stop** o **mstop**). Si no se especifica uno de los atributos de hora de inicio, el valor predeterminado es 0 (el principio de la escala de tiempo para el **Inicio** o el principio del clip para **mstart**). Si no se especifica uno de los atributos de tiempo de parada, DES supone una velocidad de reproducción normal y calcula la hora de detención no especificada en consecuencia. Si se especifican ambas horas de detención, la reproducción es más rápida o más lenta que la normal, si es necesario.

En el ejemplo siguiente, la duración de la escala de tiempo es de siete segundos (**detener** menos **Inicio**). Se presupone la velocidad de reproducción normal, por lo que el tiempo de detención del medio predeterminado es de 10 segundos (la duración más **mstart**).


```
<clip start="2" stop="9" mstart="3" />
```



En el ejemplo siguiente, el valor predeterminado de la hora de inicio del medio es 0, lo que obliga a que la duración del medio sea de 10 segundos. La duración de la escala de tiempo es de cinco segundos, por lo que el clip vuelve a reproducirse dos veces la tarifa normal.


```
<clip start="5" stop="10" mstop="10" />  
```



Si el atributo **src** especifica una imagen fija, des intenta cargar una serie de imágenes fijas para crear una animación. Por ejemplo, si el atributo **src** es IMAGE001.BMP, DES busca IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, etc. Suponiendo que existen, se muestran en orden numérico secuencial, a la velocidad especificada por el atributo de **velocidad de fotogramas** .

## <a name="examples"></a>Ejemplos


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



