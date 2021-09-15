---
description: 'Función D3DXComputeBoundingSphere (D3DX9Mesh.h): calcula una esfera de límite para la malla.'
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: Función D3DXComputeBoundingSphere (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dbfccb13dfe15b06de98ddba114cdc62c5f4ec05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569345"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a>Función D3DXComputeBoundingSphere (D3DX9Mesh.h)

Calcula una esfera de límite para la malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
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

Número de bytes entre vectores de posición. Use [**GetNumBytesPerVertex,**](id3dxbasemesh--getnumbytespervertex.md) [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)o [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) para obtener el paso de vértice.

</dd> <dt>

*pCenter* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

[**Estructura D3DXVECTOR3,**](d3dxvector3.md) que define el centro de coordenadas de la esfera de límite devuelta.

</dd> <dt>

*pRadius* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Radio de la esfera de límite devuelta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
