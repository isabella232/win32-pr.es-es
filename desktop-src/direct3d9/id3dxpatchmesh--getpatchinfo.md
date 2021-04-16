---
description: Obtiene los atributos de la revisión.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'ID3DXPatchMesh:: GetPatchInfo (método) (D3DX9Mesh. h)'
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
ms.openlocfilehash: 70308857aa66551ed371dbe511acb6bd2d211bfb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670247"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a>ID3DXPatchMesh:: GetPatchInfo (método)

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

Puntero a las estructuras que contienen los atributos patch. Para obtener más información sobre los atributos de revisión, vea [**D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 




