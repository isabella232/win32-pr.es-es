---
description: El elemento at define el valor de un elemento Param en un momento determinado, en relación con el inicio de la transición o efecto que contiene el parámetro.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Elemento at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb539331519fb23b6b8aa45b374457229f807a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806596"
---
# <a name="at-element"></a>Elemento at

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `at` elemento define el valor de un elemento [**param**](param-element.md) en un momento determinado, en relación con el inicio de la transición o efecto que contiene el parámetro. El `at` elemento hace que el parámetro salte repentinamente al nuevo valor en el momento dado. Para una progresión fluida a un nuevo valor, use el elemento [**lineal**](linear-element.md) .

## <a name="attributes"></a>Atributos

[**hora**](time-attribute.md), [ **valor**](value-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



|          |                                |
|----------|--------------------------------|
| Parent   | [**param**](param-element.md) |
| Children | None                           |



 

## <a name="examples"></a>Ejemplos


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



