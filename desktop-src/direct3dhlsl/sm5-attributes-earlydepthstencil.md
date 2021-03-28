---
title: earlydepthstencil
description: Fuerza la prueba de la galería de símbolos de profundidad antes de que se ejecute un sombreador.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996960"
---
# <a name="earlydepthstencil"></a>earlydepthstencil

Fuerza la prueba de la galería de símbolos de profundidad antes de que se ejecute un sombreador.


```
earlydepthstencil   
```



## <a name="remarks"></a>Observaciones

La prueba de profundidad-estarcido normalmente se realiza durante el procesamiento de píxeles mediante un sombreador de píxeles. Forzar la prueba temprana de la galería de símbolos hace que las pruebas se realicen antes de la ejecución del sombreador; el propósito es mejorar el rendimiento por píxel al reactivar o reducir/evitar el procesamiento de píxeles innecesario.

Una aplicación puede forzar la realización de pruebas tempranas de la galería de símbolos al proporcionar el atributo o el hardware puede ejecutar las pruebas de nivel de estarcido de nivel más rápido, siempre que no se escriban valores de profundidad y no se realicen operaciones de acceso no ordenado en un sombreador como una optimización.

Este atributo es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos del modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




