---
description: El elemento group define un grupo, el objeto de nivel superior en una escala de tiempo.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: elemento group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31502cef89c8383e935f409d76b9e31ca53a2da1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246446"
---
# <a name="group-element"></a>group (Elemento)

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El **elemento group** define un grupo, el objeto de nivel superior en una escala de tiempo.

## <a name="attributes"></a>Atributos

[**bitdepth,**](bitdepth-attribute.md) [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



| Etiqueta | Value |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**línea de tiempo**](timeline-element.md)                                                                     |
| Children | [**compuesto**](composite-element.md), [**efecto**](effect-element.md), [**pista**](track-element.md) |



 

## <a name="remarks"></a>Observaciones

Dentro de `group` un elemento, la prioridad de las capas anidadas se determina implícitamente por el orden en que aparecen dentro del elemento. La primera capa tiene prioridad 0 y las capas posteriores tienen valores de prioridad crecientes.

## <a name="examples"></a>Ejemplos


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



