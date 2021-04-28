---
description: 'Función D3DXFresnelTerm (D3DX10Math.h): calcula el término Fresnel.'
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: Función D3DXFresnelTerm (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9efa557d44451674d2ae4c48a58370e939760a03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113273"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a>Función D3DXFresnelTerm (D3DX10Math.h)

Calcule el término Fresnel.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CosTheta* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

El valor debe estar entre 0 y 1.

</dd> <dt>

*RefracciónIndex* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Índice de reanuración de un material. El valor debe ser mayor que 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Esta función devuelve el término Fresnel para la luz nopolarizada. CosTheta es el coseno del ángulo del incidente.

## <a name="remarks"></a>Comentarios

Para buscar el término Fresnel (F):

Si A es ángulo de incidencia y B es el ángulo de reanguía,


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]

Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



A continuación, al expandir con las identidades trig y simplificar, obtiene lo siguiente:


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
