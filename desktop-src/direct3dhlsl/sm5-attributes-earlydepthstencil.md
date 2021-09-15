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
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573648"
---
# <a name="earlydepthstencil"></a>earlydepthstencil

Fuerza las pruebas de galería de símbolos de profundidad antes de que se ejecute un sombreador.


```
earlydepthstencil   
```



## <a name="remarks"></a>Observaciones

Las pruebas de galería de símbolos de profundidad se realizan normalmente durante el procesamiento de píxeles mediante un sombreador de píxeles. Al forzar las primeras pruebas de galería de símbolos de profundidad, las pruebas se realizan antes de la ejecución del sombreador. el propósito es mejorar el rendimiento por píxel mediante la selección, reducción y evitación de un procesamiento de píxeles innecesario.

Una aplicación puede forzar las primeras pruebas de galería de símbolos de profundidad al proporcionar el atributo o el hardware puede ejecutar pruebas tempranas de galería de símbolos de profundidad siempre que no se escriban valores de profundidad y no se realice ninguna operación de acceso desordenada en un sombreador como una optimización.

Este atributo se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos del modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




