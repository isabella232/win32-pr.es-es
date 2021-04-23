---
description: El elemento effect define un objeto de efecto de audio o vídeo. Un efecto se aplica a una sola secuencia (por ejemplo, una composición, una pista o un origen).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: elemento effect (Gdipluseffects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908663"
---
# <a name="effect-element"></a>elemento effect

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 




