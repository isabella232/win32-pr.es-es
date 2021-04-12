---
description: Calcular el término Fresnel.
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: Función D3DXFresnelTerm (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed6c6dd19dd6b7b70c5eeb08051f9799756b0782
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362568"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a>Función D3DXFresnelTerm (D3dx9math. h)

Calcular el término Fresnel.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CosTheta* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

El valor debe estar entre 0 y 1.

</dd> <dt>

*RefractionIndex* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Índice de refracción de un material. El valor debe ser mayor que 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Esta función devuelve el término Fresnel para una luz no polarizada. CosTheta es el coseno del ángulo del incidente.

## <a name="remarks"></a>Observaciones

Para encontrar el término Fresnel (F):

Si un es el ángulo de incidencia y B es el ángulo de la refracción, entonces


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



A continuación, la expansión con las identidades trigonométricas y la simplificación, obtiene:


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
