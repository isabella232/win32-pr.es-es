---
title: earlydepthstencil
description: Fuerza las pruebas de galería de símbolos de profundidad antes de que se ejecute un sombreador.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed108d4f8e9d8d719d36fc859d5cc01a2317db4756bfbc6b0a548b669d9ca025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986175"
---
# <a name="earlydepthstencil"></a>earlydepthstencil

Fuerza las pruebas de galería de símbolos de profundidad antes de que se ejecute un sombreador.


```
earlydepthstencil   
```



## <a name="remarks"></a>Comentarios

Las pruebas de galería de símbolos de profundidad se realizan normalmente durante el procesamiento de píxeles mediante un sombreador de píxeles. Al forzar las primeras pruebas de galería de símbolos de profundidad, las pruebas se realizan antes de la ejecución del sombreador. el propósito es mejorar el rendimiento por píxel mediante la selección, reducción y evitación del procesamiento innecesario de píxeles.

Una aplicación puede forzar las primeras pruebas de galería de símbolos de profundidad al proporcionar el atributo o el hardware puede ejecutar pruebas tempranas de galería de símbolos de profundidad siempre que no se escriban valores de profundidad y no se realice ninguna operación de acceso desordenado en un sombreador como una optimización.

Este atributo se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos del modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




