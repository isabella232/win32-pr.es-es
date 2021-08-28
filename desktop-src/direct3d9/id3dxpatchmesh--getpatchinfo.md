---
description: Obtiene los atributos de la revisión.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: Método ID3DXPatchMesh::GetPatchInfo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10b6d327b665b30418478d06d21433614587824eeb481202a9bef202b8727001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847445"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a>Método ID3DXPatchMesh::GetPatchInfo

Obtiene los atributos de la revisión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PatchInfo* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**

Puntero a las estructuras que contienen los atributos de revisión. Para obtener más información sobre los atributos de revisión, [**vea D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 




