---
description: El elemento linear define el valor de un elemento Param en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el elemento Param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Elemento linear (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678983"
---
# <a name="linear-element"></a>Elemento linear

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El elemento linear define el valor de un elemento [**param**](param-element.md) en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el elemento **param** . El `linear` elemento hace que el parámetro realice una transición fluida de su valor anterior al nuevo valor. Para un salto instantáneo a un nuevo valor, use el elemento [**at**](at-element.md) .

## <a name="attributes"></a>Atributos

[**hora**](time-attribute.md), [ **valor**](value-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



|          |                                |
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
| Encabezado<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 




