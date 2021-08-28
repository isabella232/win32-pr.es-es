---
title: instance
description: Use este atributo para crear una instancia de un sombreador de geometría.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77c19b26107228bb04007d1c2c69ac34b464c7c361966ac9858d9bcdb09b4c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986165"
---
# <a name="instance"></a>instance

Use este atributo para crear una instancia de un sombreador de geometría.


```
instance(X)   
```



## <a name="remarks"></a>Comentarios

X es un índice entero que indica el número de instancias que se ejecutarán para cada elemento dibujado (por ejemplo, para cada triángulo). Al usar este atributo, use [SV \_ GSInstanceID para](sv-gsinstanceid.md) identificar qué instancia de un sombreador de geometría se ejecuta.

Este atributo se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | x        |       |         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos del modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




