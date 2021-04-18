---
description: Divide una matriz de transformación 3D general en sus componentes escalares, de rotación y de conversión.
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: Función D3DXMatrixDecompose (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92f120f1c3637216d77a5298b5de219f5605d571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698344"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a>Función D3DXMatrixDecompose (D3dx9math. h)

Divide una matriz de transformación 3D general en sus componentes escalares, de rotación y de conversión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOutScale* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero al [**D3DXVECTOR3**](d3dxvector3.md) de salida que contiene los factores de escala que se aplican a lo largo de los ejes x, y y z.

</dd> <dt>

*pOutRotation* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que describe la rotación.

</dd> <dt>

*pOutTranslation* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero al vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la traducción.

</dd> <dt>

*p. m* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una matriz de entrada [**D3DXMATRIX**](d3dxmatrix.md) para descomponer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




