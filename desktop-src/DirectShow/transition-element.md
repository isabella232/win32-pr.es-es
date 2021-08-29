---
description: El elemento transition define un objeto de transición. Una transición es una transformación de dos entradas que da como resultado una transición de una secuencia (como una compuesta o una pista) a otra.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: elemento transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725c5c6282a35f027cad87fd0b8693dbf4885ce7d4c1d5948abc2caa9014301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951484"
---
# <a name="transition-element"></a>elemento transition

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

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

 

 



