---
title: TEXT.scrollingAmount
description: El atributo scrollingAmount especifica o recupera el número de píxeles que el texto mueve durante cada movimiento de desplazamiento.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- TEXT.scrollingAmount Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160581"
---
# <a name="textscrollingamount"></a>TEXT.scrollingAmount

El **atributo scrollingAmount** especifica o recupera el número de píxeles que el texto mueve durante cada movimiento de desplazamiento.

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número positivo de lectura **y** escritura (**int**) con un valor predeterminado de 6.

## <a name="remarks"></a>Observaciones

Para un desplazamiento suave, **scrollingAmount** debe ser pequeño. Para un dibujo rápido con espacios grandes, **scrollingAmount** debe ser mayor. Si **se desplaza** ="false", se omite **scrollingAmount.**

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.scrolling**](text-scrolling.md)
</dt> </dl>

 

 





