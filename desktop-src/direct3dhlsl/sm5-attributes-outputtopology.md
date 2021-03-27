---
title: outputtopology
description: Define el tipo primitivo de salida para del teselador.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103994833"
---
# <a name="outputtopology"></a>outputtopology

Define el tipo primitivo de salida para del teselador.


```
outputtopology(X)      
```



## <a name="remarks"></a>Observaciones

X debe ser [**punto**](dx-graphics-hlsl-geometry-shader.md), **línea**, **triángulo \_ CW** o **triángulo \_ CCW** y debe incluirse entre comillas. Estas son las opciones válidas para este atributo:


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



Este atributo es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos del modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




