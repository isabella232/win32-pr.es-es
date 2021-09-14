---
description: Bloquee el búfer de vértices.
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: Método ID3DXPatchMesh::LockVertexBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d88d8a1da7ae544c5647fc844cda4966cfee7b10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060534"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a>Método ID3DXPatchMesh::LockVertexBuffer

Bloquee el búfer de vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flags* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de cero o más marcas de bloqueo que describen el tipo de bloqueo que se debe realizar. Para este método, las marcas válidas son:

-   D3DLOCK \_ DISCARD
-   D3DLOCK \_ NO \_ DIRTY \_ UPDATE
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ READONLY
-   D3DLOCK \_ NOOVERWRITE

Para obtener una descripción de las marcas, vea [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

Puntero VOID \* a un búfer de memoria que contiene los datos de vértice devueltos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Normalmente, el búfer de vértices se bloquea, se escribe en y, a continuación, se desbloquea para su lectura.

Las mallas de revisión usan búferes de índice de 16 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
