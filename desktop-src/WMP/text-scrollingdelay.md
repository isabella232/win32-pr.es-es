---
title: TEXT.scrollingDelay
description: El atributo scrollingDelay especifica o recupera el retraso de tiempo entre los movimientos de desplazamiento.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- TEXT.scrollingDelay Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647e9bbffe723bff0a8079c2776c48db0f23f89306fdb732fed8c62ac420d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117932638"
---
# <a name="textscrollingdelay"></a>TEXT.scrollingDelay

El **atributo scrollingDelay** especifica o recupera el retraso de tiempo entre los movimientos de desplazamiento.

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**int**) que especifica el retraso en milisegundos. Tiene un valor mínimo de 30 y un valor predeterminado de 85. Si se especifica un valor menor que el mínimo, se usa el valor predeterminado.

## <a name="remarks"></a>Comentarios

Si **el desplazamiento** se establece en false, se omite **scrollingDelay.**

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.scrolling**](text-scrolling.md)
</dt> </dl>

 

 





