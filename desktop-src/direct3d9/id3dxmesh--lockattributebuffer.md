---
description: Bloquea el búfer de malla que contiene los datos de atributo de la malla y devuelve un puntero a él.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'ID3DXMesh:: LockAttributeBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 901cb98a9d75d08b6412d6fdca841d403064354b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698208"
---
# <a name="id3dxmeshlockattributebuffer-method"></a>ID3DXMesh:: LockAttributeBuffer (método)

Bloquea el búfer de malla que contiene los datos de atributo de la malla y devuelve un puntero a él.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de cero o más marcas de bloqueo que describen el tipo de bloqueo que se va a realizar. Para este método, las marcas válidas son:

-   \_Descartar D3DLOCK
-   \_No se \_ pudo \_ Actualizar D3DLOCK
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ ReadOnly

Para obtener una descripción de las marcas, vea [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***

Dirección de un puntero a un búfer que contiene un valor DWORD para cada una de las caras de la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Si se ha llamado a [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) , la malla también tendrá una tabla de atributos a la que se puede tener acceso mediante el método [**ID3DXBaseMesh:: GetAttributeTable**](id3dxbasemesh--getattributetable.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[**ID3DXMesh::SetAttributeTable**](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
