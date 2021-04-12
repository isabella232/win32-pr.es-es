---
description: Calcula un cuadro de límite orientado al eje de coordenadas.
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: Función D3DXComputeBoundingBox (D3DX9Mesh. h)
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
ms.openlocfilehash: df0376428153cfc02e499c9e26226cce81154023
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280361"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a>Función D3DXComputeBoundingBox (D3DX9Mesh. h)

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

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

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

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que describe la esquina inferior izquierda devuelta del cuadro de límite. Vea la sección Comentarios.

</dd> <dt>

*pMax* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que describe la esquina superior derecha devuelta del cuadro de límite. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
