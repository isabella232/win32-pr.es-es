---
description: Transforma una matriz de planos en una matriz. Los vectores que describen cada plano se deben normalizar.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: Función D3DXPlaneTransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 128b9c8c73db81faa877295e993504a7a510cd4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083764"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a>Función D3DXPlaneTransformArray (D3DX10Math. h)

Transforma una matriz de planos en una matriz. Los vectores que describen cada plano se deben normalizar.

## <a name="syntax"></a>Sintaxis


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntero a la estructura [**D3DXPLANE**](d3d10-d3dxplane.md) que contiene el plano transformado resultante. Vea el ejemplo.

</dd> <dt>

Retrasos  \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Paso de cada plano transformado.

</dd> <dt>

*PP* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Puntero a la estructura D3DXPLANE de entrada, que contiene la matriz de los planos que se van a transformar. El vector (a, b, c) que describe el plano debe normalizarse antes de que se llame a esta función. Vea el ejemplo.

</dd> <dt>

*PStride* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Paso de cada plano no transformado.

</dd> <dt>

*p. m* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen, que contiene la transposición inversa de los valores de transformación.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de planos que se van a transformar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntero a una estructura D3DXPLANE que representa el plano transformado. Este es el mismo valor que se devuelve en el parámetro pOut para que esta función se pueda usar como parámetro de otra función.

## <a name="remarks"></a>Observaciones

En este ejemplo se transforma un plano aplicando una escala no uniforme.


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



AX + por + cz + DW = 0 describe un plano. El primer plano se crea con (a, b, c, d) = (0, 1, 1, 0), que es un plano descrito por y + z = 0. Después del escalado, el nuevo plano contiene (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), que muestra el nuevo plano que se va a describir mediante 0.353 y + 0.235 z = 0.

El parámetro pM contiene la transposición inversa de la matriz de transformación. Este método requiere la TRANSPOSE inversa para que el vector normal del plano transformado también se pueda transformar correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
