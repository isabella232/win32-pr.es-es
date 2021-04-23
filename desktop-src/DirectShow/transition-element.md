---
description: El elemento transition define un objeto de transición. Una transición es una transformación de dos entradas que da como resultado una transición de una secuencia (como una compuesta o una pista) a otra.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: elemento transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910043"
---
# <a name="transition-element"></a>elemento transition

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `transition` elemento define un objeto de transición. Una transición es una transformación de dos entradas que da como resultado una transición de una secuencia (como una compuesta o una pista) a otra.

## <a name="attributes"></a>Atributos

[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



| Etiqueta | Value |
|----------|------------------------------------------------------------------------|
| Parent   | [**compuesto,**](composite-element.md) [ **pista**](track-element.md) |
| Children | [**param**](param-element.md)                                         |



 

## <a name="remarks"></a>Comentarios

El **atributo clsid** especifica el subobjeto que crea la transición.

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

 

 



