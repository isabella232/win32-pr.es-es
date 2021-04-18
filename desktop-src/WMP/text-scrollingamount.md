---
title: TEXT. scrollingAmount
description: El atributo scrollingAmount especifica o recupera el número de píxeles que el texto se mueve durante cada movimiento de desplazamiento.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- Media Player de Windows TEXT. scrollingAmount
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680295"
---
# <a name="textscrollingamount"></a>TEXT. scrollingAmount

El atributo **scrollingAmount** especifica o recupera el número de píxeles que el texto se mueve durante cada movimiento de desplazamiento.

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura positivo (**int**) con un valor predeterminado de 6.

## <a name="remarks"></a>Observaciones

Para el desplazamiento suave, **scrollingAmount** debe ser pequeño. Para un dibujo rápido con grandes huecos, el **scrollingAmount** debe ser mayor. Si **scrolling** = "false", **scrollingAmount** se omite.

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

 

 





