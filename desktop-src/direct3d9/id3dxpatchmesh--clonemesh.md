---
description: Crea una nueva malla de revisión con la declaración de vértice especificada.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'ID3DXPatchMesh:: CloneMesh (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362464"
---
# <a name="id3dxpatchmeshclonemesh-method"></a>ID3DXPatchMesh:: CloneMesh (método)

Crea una nueva malla de revisión con la declaración de vértice especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Opciones* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas [**D3DXMESH**](./d3dxmesh.md) que especifican las opciones de creación de la malla.

</dd> <dt>

*pDecl* \[ de\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que especifican el formato de vértice de los vértices de la malla de salida.

</dd> <dt>

*pmesh* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Dirección de un puntero a una interfaz [**ID3DXPatchMesh**](id3dxpatchmesh.md) que representa la malla clonada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

**CloneMesh** convierte el búfer de vértices en la nueva declaración de vértices. Las entradas en la declaración de vértices que son nuevas en la malla original se establecen en 0. Si la malla actual tiene adyacencias, la nueva malla también tendrá adyacencias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
