---
description: Divide una matriz de transformación 3D general en sus componentes escalares, de rotación y de conversión.
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: Función D3DXMatrixDecompose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 507c8f177db0f71b3d333a8343e4166e649f424a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280471"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a>Función D3DXMatrixDecompose (D3DX10Math. h)

Divide una matriz de transformación 3D general en sus componentes escalares, de rotación y de conversión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOutScale* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) de salida que contiene los factores de escala que se aplican a lo largo de los ejes x, y y z.

</dd> <dt>

*pOutRotation* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que describe la rotación.

</dd> <dt>

*pOutTranslation* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero al vector D3DXVECTOR3 que describe la traducción.

</dd> <dt>

*p. m* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a una matriz de entrada [**D3DXMATRIX**](d3d10-d3dxmatrix.md) para descomponer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
