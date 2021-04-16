---
title: TEXT. scrollingDelay
description: El atributo scrollingDelay especifica o recupera el tiempo de retardo entre los movimientos de desplazamiento.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- Media Player de Windows TEXT. scrollingDelay
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680294"
---
# <a name="textscrollingdelay"></a>TEXT. scrollingDelay

El atributo **scrollingDelay** especifica o recupera el tiempo de retardo entre los movimientos de desplazamiento.

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**int**) que especifica el retraso en milisegundos. Tiene un valor mínimo de 30 y un valor predeterminado de 85. Si se especifica un valor menor que el mínimo, se utiliza el valor predeterminado.

## <a name="remarks"></a>Observaciones

Si el **desplazamiento** se establece en false, se omite **scrollingDelay** .

Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXTO. desplazamiento**](text-scrolling.md)
</dt> </dl>

 

 





