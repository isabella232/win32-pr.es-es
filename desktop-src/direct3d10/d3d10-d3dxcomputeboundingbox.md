---
description: Calcula un cuadro de límite orientado al eje de coordenadas.
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: Función D3DXComputeBoundingBox (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9a93eb4a10f6c2b2fd7eda82afcc21158138a1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708015"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a>Función D3DXComputeBoundingBox (D3DX10math. h)

Calcula un cuadro de límite orientado al eje de coordenadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFirstPosition* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a la primera posición.

</dd> <dt>

*NumVertices* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices.

</dd> <dt>

*dwStride* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Recuento o número de bytes entre los vértices.

</dd> <dt>

*pMin* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que describe la esquina inferior izquierda devuelta del cuadro de límite.

</dd> <dt>

*pMax* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que describe la esquina superior derecha devuelta del cuadro de límite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
