---
description: 'Función D3DXPlaneTransformArray (D3dx9math.h): transforma una matriz de planos por una matriz. Los vectores que describen cada plano deben normalizarse.'
ms.assetid: e82e830b-efbb-4bdc-b370-7bfa4326a669
title: Función D3DXPlaneTransformArray (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bdbc845eda69d22f6e7097131f71b074a9b53985
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094133"
---
# <a name="d3dxplanetransformarray-function-d3dx9mathh"></a>Función D3DXPlaneTransformArray (D3dx9math.h)

Transforma una matriz de planos por una matriz. Los vectores que describen cada plano deben normalizarse.

## <a name="syntax"></a>Sintaxis


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _Out_         UINT       OutStride,
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

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntero a la [**estructura D3DXPLANE**](d3dxplane.md) que contiene el plano transformado resultante. Vea Ejemplo.

</dd> <dt>

*OutStride* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

El paso de cada plano transformado.

</dd> <dt>

*pP* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntero a la estructura [**D3DXPLANE de**](d3dxplane.md) entrada, que contiene la matriz de planos que se va a transformar. El vector (a,b,c) que describe el plano debe normalizarse antes de llamar a esta función. Vea Ejemplo.

</dd> <dt>

*PStride* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

El paso de cada plano no transformado.

</dd> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen, que contiene la transpuesta inversa de los valores de transformación.

</dd> <dt>

*n* \[ en\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de planos que se transformarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntero a una [**estructura D3DXPLANE,**](d3dxplane.md) que representa el plano transformado. Este es el mismo valor devuelto en el *parámetro pOut* para que esta función se pueda usar como parámetro para otra función.

## <a name="remarks"></a>Comentarios

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



Un plano se describe mediante ax + by + dw + dw = 0. El primer plano se crea con (a,b,c,d) = (0,1,1,0), que es un plano descrito por y + z = 0. Después del escalado, el nuevo plano contiene (a,b,c,d) = (0, 0,353f, 0,235f, 0), que muestra el nuevo plano descrito por 0,353y + 0,235z = 0.

El parámetro *pM contiene* la transpuesta inversa de la matriz de transformación. Este método requiere la transponer inversa para que el vector normal del plano transformado también se pueda transformar correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneNormalize**](d3dxplanenormalize.md)
</dt> <dt>

[**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)
</dt> <dt>

[**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)
</dt> <dt>

[**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md)
</dt> <dt>

[**D3DXMatrixInverse**](d3dxmatrixinverse.md)
</dt> <dt>

[**D3DXMatrixTranspose**](d3dxmatrixtranspose.md)
</dt> </dl>

 

 
