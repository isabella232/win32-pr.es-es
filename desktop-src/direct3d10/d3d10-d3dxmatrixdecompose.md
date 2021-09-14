---
description: 'Función D3DXMatrixDecompose (D3DX10Math.h): divide una matriz de transformación 3D general en sus componentes escalares, rotacionales y traslacionales.'
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: Función D3DXMatrixDecompose (D3DX10Math.h)
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
ms.openlocfilehash: cc87de99d72283c20f25b15ea8d0e5864e2550d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965115"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a>Función D3DXMatrixDecompose (D3DX10Math.h)

Divide una matriz de transformación 3D general en sus componentes escalares, rotacionales y traslacionales.

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

*pOutScale* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a la salida [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que contiene los factores de escalado aplicados a lo largo de los ejes x, y y z.

</dd> <dt>

*pOutRotation* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que describe la rotación.

</dd> <dt>

*pOutTranslation* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero al vector D3DXVECTOR3 que describe la traducción.

</dd> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a una matriz [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) entrada para descomponer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
