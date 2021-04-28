---
description: 'Función D3DXMatrixDecompose (D3dx9math.h): divide una matriz de transformación 3D general en sus componentes escalares, rotacionales y traslacionales.'
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: Función D3DXMatrixDecompose (D3dx9math.h)
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
ms.openlocfilehash: aaaa1059c4ffeafa453694d9c348656c856decaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098193"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a>Función D3DXMatrixDecompose (D3dx9math.h)

Divide una matriz de transformación 3D general en sus componentes escalares, rotacionales y traslacionales.

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

Puntero a la [**salida D3DXVECTOR3**](d3dxvector3.md) que contiene los factores de escalado aplicados a lo largo de los ejes x, y y z.

</dd> <dt>

*pOutRotation* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que describe la rotación.

</dd> <dt>

*pOutTranslation* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero al vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la traducción.

</dd> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una matriz [**D3DXMATRIX de**](d3dxmatrix.md) entrada para descomponer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




