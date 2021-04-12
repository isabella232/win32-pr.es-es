---
description: Transforma un plano mediante una matriz. La matriz de entrada es la transposición inversa de la transformación real.
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: Función D3DXPlaneTransform (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b3c3390d84cd0d9c876afac6243ab90ca515e11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362718"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a>Función D3DXPlaneTransform (D3DX10Math. h)

Transforma un plano mediante una matriz. La matriz de entrada es la transposición inversa de la transformación real.

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

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntero al [**D3DXPLANE**](d3d10-d3dxplane.md) que contiene el plano transformado resultante. Vea el ejemplo.

</dd> <dt>

*PP* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Puntero a la estructura D3DXPLANE de entrada, que contiene el plano que se va a transformar. El vector (a, b, c) que describe el plano debe normalizarse antes de que se llame a esta función. Vea el ejemplo.

</dd> <dt>

*p. m* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen, que contiene los valores de la transformación. Esta matriz debe contener la transposición inversa de los valores de transformación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntero a una estructura D3DXPLANE que representa el plano transformado. Este es el mismo valor que se devuelve en el parámetro pOut para que esta función se pueda usar como parámetro de otra función.

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

 

 
