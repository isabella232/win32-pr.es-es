---
description: 'Función D3DXPlaneTransform (D3dx9math.h): transforma un plano mediante una matriz. La matriz de entrada es la transpuesta inversa de la transformación real.'
ms.assetid: 3581b397-cbd8-4aed-80dd-1841f331a367
title: Función D3DXPlaneTransform (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c4376319d8ac2d49c480110d5119af5a3cefc9fe491f4997efdc15e30bf50db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986465"
---
# <a name="d3dxplanetransform-function-d3dx9mathh"></a>Función D3DXPlaneTransform (D3dx9math.h)

Transforma un plano mediante una matriz. La matriz de entrada es la transpuesta inversa de la transformación real.

## <a name="syntax"></a>Sintaxis


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntero a la [**estructura D3DXPLANE**](d3dxplane.md) que contiene el plano transformado resultante. Vea el ejemplo.

</dd> <dt>

*pP* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntero a la estructura [**D3DXPLANE de**](d3dxplane.md) entrada, que contiene el plano que se transformará. El vector (a,b,c) que describe el plano debe normalizarse antes de llamar a esta función. Vea el ejemplo.

</dd> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen, que contiene los valores de transformación. Esta matriz debe contener la transpuesta inversa de los valores de transformación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntero a una [**estructura D3DXPLANE,**](d3dxplane.md) que representa el plano transformado. Este es el mismo valor devuelto en el parámetro pOut para que esta función se pueda usar como parámetro para otra función.

## <a name="remarks"></a>Observaciones

### <a name="examples"></a>Ejemplos

En este ejemplo se transforma un plano aplicando una escala no uniforme.


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



Un plano se describe mediante ax + by + dw + dw = 0. El primer plano se crea con (a,b,c,d) = (0,1,1,0), que es un plano descrito por y + z = 0. Después del escalado, el nuevo plano contiene (a,b,c,d) = (0, 0,353f, 0,235f, 0), que muestra el nuevo plano descrito por 0,353y + 0,235z = 0.

El parámetro pM contiene la transpuesta inversa de la matriz de transformación. Este método requiere la transpuesta inversa para que el vector normal del plano transformado también se pueda transformar correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

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

 

 




