---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- Texture3D HLSL
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b5c715f5f2bb7edfaa149cf0da77db5fbca8d47636b6f84fd07071c3b75186e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788325"
---
# <a name="texture3d"></a>Texture3D

Tipo Texture3D ([tal y como existe en Shader Model 4](dx-graphics-hlsl-to-type.md)) más variables de recursos. Este objeto de textura admite los métodos siguientes además de los métodos de Shader Model 4.



| Método                                                                  | Descripción                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture3d-getdimensions.md)             | Obtiene las dimensiones de recursos.                                                              |
| [**Cargar**](texture3d-load.md)                                          | Lee los datos de textura.                                                                        |
| [**Mips. Operador\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) | Obtiene una variable de recurso de solo lectura.                                                        |
| [**Operador\[\]**](sm5-object-texture3d-operatorindex.md)              | Obtiene una variable de recurso de solo lectura.                                                        |
| [**Muestra**](texture3d-sample.md)                                      | Muestrea una textura.                                                                         |
| [**SampleBias**](texture3d-samplebias.md)                              | Muestrea una textura después de aplicar el valor de sesgo al nivel mipmap.                      |
| [**SampleGrad**](texture3d-samplegrad.md)                              | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de la muestra. |
| [**SampleLevel**](texture3d-samplelevel.md)                            | Muestrea una textura en el nivel de mapa mip especificado.                                           |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




