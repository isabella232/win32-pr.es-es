---
description: 'Función D3DXComputeBoundingBox (D3DX9Mesh.h): calcula un rectángulo de selección orientado al eje de coordenadas.'
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: Función D3DXComputeBoundingBox (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03eb722e68b58ec48a3bf607ab72d67004ad30a0c765b19c1b84ae29577c773b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299957"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a>Función D3DXComputeBoundingBox (D3DX9Mesh.h)

Calcula un rectángulo de selección orientado al eje de coordenadas.

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

*pFirstPosition* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a la primera posición.

</dd> <dt>

*NumVertices* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices.

</dd> <dt>

*dwStride* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Recuento o número de bytes entre vértices.

</dd> <dt>

*pMin* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que describe la esquina inferior izquierda devuelta del cuadro de límite. Vea la sección Comentarios.

</dd> <dt>

*pMax* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que describe la esquina superior derecha devuelta del cuadro de límite. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
