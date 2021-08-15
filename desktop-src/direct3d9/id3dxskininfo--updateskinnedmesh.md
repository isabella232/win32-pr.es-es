---
description: Aplica el desnasado de software a los vértices de destino en función de las matrices actuales.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: Método ID3DXSkinInfo::UpdateSkinnedMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22b36e1836570a10647f5b737a68afa1e65a4dce80fe9d49061a3eee8a799651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729457"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a>Método ID3DXSkinInfo::UpdateSkinnedMesh

Aplica el desnasado de software a los vértices de destino en función de las matrices actuales.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTransforms* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matriz de transformación de transformaciones de transformaciones.

</dd> <dt>

*pIonalInvTransposeTransforms* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Transponer inversamente la matriz de transformación de los tejidos.

</dd> <dt>

*pVerticesSrc* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al búfer que contiene los vértices de origen.

</dd> <dt>

*pVerticesDst* \[ En\]
</dt> <dd>

Tipo: **[ **PVOID**](../winprog/windows-data-types.md)**

Puntero al búfer que contiene los vértices de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Cuando se usa para la máscara de vértices con dos elementos de posición, este método desasocia el segundo elemento de posición con el inverso del pórtico en lugar del propio pórtico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
