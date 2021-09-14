---
description: Bloquea el búfer de atributos.
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: Método ID3DXPatchMesh::LockAttributeBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71e50fdc27f3f50b560324c74f5a1609f900772d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060539"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a>Método ID3DXPatchMesh::LockAttributeBuffer

Bloquea el búfer de atributos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LockAttributeBuffer(
  [in]          DWORD flags,
  [out, retval] DWORD **ppData
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

Para obtener una descripción de las marcas, vea [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***

Dirección de un puntero a un búfer que contiene un DWORD para cada cara de la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Normalmente, el búfer de atributos se bloquea, se escribe en y, a continuación, se desbloquea para su lectura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
