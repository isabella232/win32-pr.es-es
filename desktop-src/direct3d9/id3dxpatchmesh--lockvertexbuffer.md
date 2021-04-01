---
description: Bloquee el búfer de vértices.
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: 'ID3DXPatchMesh:: LockVertexBuffer (método) (D3DX9Mesh. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914769"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a>ID3DXPatchMesh:: LockVertexBuffer (método)

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

*marcas* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de cero o más marcas de bloqueo que describen el tipo de bloqueo que se va a realizar. Para este método, las marcas válidas son:

-   \_Descartar D3DLOCK
-   \_No se \_ pudo \_ Actualizar D3DLOCK
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ ReadOnly
-   D3DLOCK \_ NOOVERWRITE

Para obtener una descripción de las marcas, vea [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*Puntero void a un búfer de memoria que contiene los datos de vértice devueltos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Normalmente, el búfer de vértices se bloquea, se escribe en él y, a continuación, se desbloquea para leerlo.

Las mallas de revisión utilizan búferes de índice de 16 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
