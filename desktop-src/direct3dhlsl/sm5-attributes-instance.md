---
title: instance
description: Use este atributo para instanciar un sombreador de geometría.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077113"
---
# <a name="instance"></a>instance

Use este atributo para instanciar un sombreador de geometría.


```
instance(X)   
```



## <a name="remarks"></a>Observaciones

X es un índice entero que indica el número de instancias que se van a ejecutar para cada elemento dibujado (por ejemplo, para cada triángulo). Al utilizar este atributo, use [VP \_ GSInstanceID](sv-gsinstanceid.md) para identificar qué instancia de un sombreador de geometría se está ejecutando.

Este atributo es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | x        |       |         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos del modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




