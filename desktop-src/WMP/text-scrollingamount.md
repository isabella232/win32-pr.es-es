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
ms.openlocfilehash: 2a8d5b703c02c2d3049f98a934980f1dbf8b1c5beceaca4d97158ea68c13db9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466965"
---
# <a name="textscrollingamount"></a>TEXT.scrollingAmount

El **atributo scrollingAmount** especifica o recupera el número de píxeles que el texto mueve durante cada movimiento de desplazamiento.

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número positivo de lectura y **escritura** (**int**) con un valor predeterminado de 6.

## <a name="remarks"></a>Comentarios

Para un desplazamiento suave, **scrollingAmount** debe ser pequeño. Para dibujar rápidamente con espacios grandes, **scrollingAmount** debe ser mayor. Si **se desplaza** ="false", se omite **scrollingAmount.**

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.scrolling**](text-scrolling.md)
</dt> </dl>

 

 





