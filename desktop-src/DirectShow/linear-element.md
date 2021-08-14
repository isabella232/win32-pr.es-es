---
description: El elemento lineal define el valor de un elemento param en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el elemento param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: linear (Elemento, Camerauicontrol.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34bff0ef1ef4c9c95752f986aabeddd24b40cc695a8a0f292b1072dfdc1d3d28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397149"
---
# <a name="linear-element"></a>linear (Elemento)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El elemento lineal define el valor de un elemento [**param**](param-element.md) en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el **elemento param.** El `linear` elemento hace que el parámetro realice una transición sin problemas de su valor anterior al nuevo valor. Para un salto instantáneo a un nuevo valor, use el [**elemento at**](at-element.md) .

## <a name="attributes"></a>Atributos

[**time**](time-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



| Etiqueta | Valor |
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

 

 




