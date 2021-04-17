---
description: El elemento Transition define un objeto Transition. Una transición es una transformación de dos entradas que da como resultado una transición de un flujo (como un compuesto o un seguimiento) a otra.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Elemento Transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b7663785c641252609366c8bfd6044582829e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667642"
---
# <a name="transition-element"></a>Elemento Transition

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `transition` elemento define un objeto de transición. Una transición es una transformación de dos entradas que da como resultado una transición de un flujo (como un compuesto o un seguimiento) a otra.

## <a name="attributes"></a>Atributos

[**CLSID**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**MUTE**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



|          |                                                                        |
|----------|------------------------------------------------------------------------|
| Parent   | [**compuesto**](composite-element.md), [ **seguimiento**](track-element.md) |
| Children | [**param**](param-element.md)                                         |



 

## <a name="remarks"></a>Observaciones

El atributo **CLSID** especifica el subobjeto que crea la transición.

## <a name="examples"></a>Ejemplos


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



