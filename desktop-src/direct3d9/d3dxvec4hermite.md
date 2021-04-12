---
description: Realiza una interpolación de spline Hermite, usando los vectores 4D especificados.
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: Función D3DXVec4Hermite (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85cf60150606a37c2e68ebf72bd4a3772d346660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280357"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a>Función D3DXVec4Hermite (D3dx9math. h)

Realiza una interpolación de spline Hermite, usando los vectores 4D especificados.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR4* D3DXVec4Hermite(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pT1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) de origen, un vector de posición.

</dd> <dt>

*PT1* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) de origen, un vector tangente.

</dd> <dt>

*pV2* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) de origen, un vector de posición.

</dd> <dt>

*PT2* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) de origen, un vector tangente.

</dd> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de ponderación. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la interpolación de la spline de Hermite.

## <a name="remarks"></a>Observaciones

La función **D3DXVec4Hermite** se interpola desde (positiona, tangenta) hasta (PositionB, tangentB) mediante la interpolación de spline de Hermite.

La interpolación spline es una generalización de la spline de fácil entrada y de fácil salida. La rampa es una función de Q (s) con las siguientes propiedades.

Q (s) = como ³ + BS ² + CS + D (y, por lo tanto, Q ' (s) = 3As ² + 2Bs + C)

a) Q (0) = V1, so Q ' (0) = T1

b) Q (1) = V2, so Q ' (1) = T2

V1 es el contenido de pV1, V2 en el contenido de pV2, T1 es el contenido de pT1 y T2 es el contenido de pT2.

Estas propiedades se usan para resolver para A, B, C, D.

Conecte las soluciones para A, B, C y D para generar Q (s).

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

El resultado es:

Q (s) = (2V1-2v2 + T2 + T1) s ³ + (3v2-3V1-2T1-T2) s ² + T1s + v1

Que se puede reorganizar como:

Q (s) = (2S ³-3S ² + 1) V1 + (-2S ³ + 3S ²) v2 + (s ³-2s ² + s) T1 + (s ³-s ²) T2

Las curvas spline de Hermite son útiles para controlar la animación, ya que la curva se ejecuta a través de todos los puntos de control. Además, dado que la posición y la tangente se especifican explícitamente en los extremos de cada segmento, es fácil crear una curva continua C2 siempre que se asegure de que la posición inicial y la tangente coinciden con los valores finales del último segmento.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut. De esta manera, la función **D3DXVec4Hermite** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
