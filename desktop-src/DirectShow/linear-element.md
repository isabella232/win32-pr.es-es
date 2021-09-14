---
description: El elemento lineal define el valor de un elemento param en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el elemento param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: linear (Elemento, Camerauicontrol.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063212"
---
# <a name="linear-element"></a>linear (Elemento)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El elemento lineal define el valor de un [**elemento param**](param-element.md) en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el **elemento param.** El `linear` elemento hace que el parámetro realice una transición sin problemas de su valor anterior al nuevo valor. Para un salto instantáneo a un nuevo valor, use el [**elemento at**](at-element.md) .

## <a name="attributes"></a>Atributos

[**time**](time-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



| Etiqueta | Value |
|----------|--------------------------------|
| Parent   | [**param**](param-element.md) |
| Children | None                           |



 

## <a name="examples"></a>Ejemplos


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Camerauicontrol.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 




