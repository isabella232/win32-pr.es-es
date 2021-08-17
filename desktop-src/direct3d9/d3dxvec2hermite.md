---
description: 'Función D3DXVec2Hermite (D3dx9math.h): realiza una interpolación spline hermite con los vectores 2D especificados.'
ms.assetid: 30eb9490-bc01-4449-adfb-1c552e8ad3e7
title: Función D3DXVec2Hermite (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 052174ba85370c62dc8a4618b44880f1e750801a78cf61963d863a9057c10568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804065"
---
# <a name="d3dxvec2hermite-function-d3dx9mathh"></a>Función D3DXVec2Hermite (D3dx9math.h)

Realiza una interpolación spline de Hermite, utilizando los vectores 2D especificados.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR2* D3DXVec2Hermite(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pT1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntero a la [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen, un vector de posición.

</dd> <dt>

*pT1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen, un vector tangente.

</dd> <dt>

*pV2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen, un vector de posición.

</dd> <dt>

*pT2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen, un vector tangente.

</dd> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de ponderación. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntero a una [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la interpolación spline de Hermite.

## <a name="remarks"></a>Comentarios

La **función D3DXVec2Hermite** interpola de (positionA, tangentA) a (positionB, tangentB) mediante la interpolación spline de Hermite.

La interpolación spline es una generalización de la spline de facilidad de entrada y de salida. La rampa es una función de preguntas y respuestas con las siguientes propiedades.

Q(s) = Asntes + Bsmientos + Cs + D (y, por lo tanto, Q's) = 3Azos + 2B + C)

a) Q(0) = v1, por lo que Q'(0) = t1

b) Q(1) = v2, por lo que Q'(1) = t2

v1 es el contenido de pV1, v2 en el contenido de pV2, t1 es el contenido de pT1 y t2 es el contenido de pT2.

Estas propiedades se usan para resolver A, B, C, D.

``` syntax
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t-1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```

Conecte las soluciones para A, B, C y D para generar preguntas y respuestas.

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

El resultado es:

Q(s) = (2v1 - 2v2 + t2 + t1)sntes + (3v2 - 3v1 - 2t1 - t2)sntes + t1 + v1

Que se puede reorganizar como:

Q(s) = (2sntes - 3s): + 1)v1 + (-2sntes + 3sntes)v2 + (sntes - 2s): + s)t1 + (sntes - s): t2

Las curvas spline hermite son útiles para controlar la animación porque la curva recorre todos los puntos de control. Además, dado que la posición y la tangente se especifican explícitamente en los extremos de cada segmento, es fácil crear una curva continua C2 siempre que se asegúrese de que la posición inicial y la tangente coinciden con los valores finales del último segmento.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la **función D3DXVec2Hermite** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
