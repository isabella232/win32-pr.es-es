---
description: El elemento Group define un grupo, el objeto de nivel superior en una escala de tiempo.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Elemento Group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b8146586d93a53093a68bb1abc08e85c52f14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997992"
---
# <a name="group-element"></a>Elemento Group

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El elemento **Group** define un grupo, el objeto de nivel superior en una escala de tiempo.

## <a name="attributes"></a>Atributos

[**bitdepth**](bitdepth-attribute.md), [**almacenamiento en búfer**](buffering-attribute.md), [**velocidad de fotogramas**](framerate-attribute.md), [**alto**](height-attribute.md), [**bloqueo**](lock-attribute.md), [**silencio**](mute-attribute.md), [**nombre**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**Samplingrate**](samplingrate-attribute.md), [**tipo**](type-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**nombre de usuario**](username-attribute.md), [**ancho**](width-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**marco**](timeline-element.md)                                                                     |
| Children | [**compuesto**](composite-element.md), [**efecto**](effect-element.md), [**seguimiento**](track-element.md) |



 

## <a name="remarks"></a>Observaciones

Dentro de un `group` elemento, la prioridad de las capas anidadas viene determinada implícitamente por el orden en que aparecen dentro del elemento. La primera capa tiene prioridad 0 y las capas siguientes tienen valores de prioridad crecientes.

## <a name="examples"></a>Ejemplos


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



