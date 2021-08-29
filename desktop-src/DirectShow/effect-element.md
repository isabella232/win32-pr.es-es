---
description: El elemento de efecto define un objeto de efecto de audio o vídeo. Un efecto se aplica a una sola secuencia (por ejemplo, una composición, una pista o un origen).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: elemento effect (Gdipluseffects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a780fbab91cd5071efd1135faa680e4707ca1f7327145cc372a5fe8a231a4e8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823665"
---
# <a name="effect-element"></a>elemento effect

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `effect` elemento define un objeto de efecto de audio o vídeo. Un efecto se aplica a una sola secuencia (por ejemplo, una composición, una pista o un origen).

## <a name="attributes"></a>Atributos

[**clsid,**](clsid-attribute.md) [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



| Etiqueta | Value |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| Parent   | [**compuesto,**](composite-element.md) [**grupo,**](group-element.md) [**clip,**](clip-element.md) [**pista**](track-element.md) |
| Children | [**param**](param-element.md)                                                                                                       |



 

## <a name="remarks"></a>Comentarios

El **atributo clsid** especifica el subobjeto que crea el efecto.

## <a name="examples"></a>Ejemplos


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Gdipluseffects.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 




