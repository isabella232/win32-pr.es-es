---
description: 'Método ID3DXBaseMesh::GetVertexBuffer: recupera el búfer de vértices asociado a la malla.'
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: Método ID3DXBaseMesh::GetVertexBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9533188e3e2effe1759b58f70c9f033cc491844c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115373"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a>Método ID3DXBaseMesh::GetVertexBuffer

Recupera el búfer de vértices asociado a la malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppVB* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***

Dirección de un puntero a una [**interfaz IDirect3DVertexBuffer9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) que representa el objeto de búfer de vértice asociado a la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
