---
description: 'Función D3DXCreateSkinInfo: crea un objeto de malla de máscara vacío mediante un declarador.'
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: Función D3DXCreateSkinInfo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d1539e0bf7a552fdb44bb1c2f323af387797a660d4e1bade312000652fb5bbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676145"
---
# <a name="d3dxcreateskininfo-function"></a>Función D3DXCreateSkinInfo

Crea un objeto de malla de máscara vacío mediante un declarador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumVertices* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices para la malla de máscara.

</dd> <dt>

*pDeclaration* \[ En\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matriz [**de elementos D3DVERTEXELEMENT9,**](d3dvertexelement9.md) que describe el formato de vértice de la malla devuelta.

</dd> <dt>

*NumBones* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de tejidos para la malla de máscara.

</dd> <dt>

*ppSkinInfo* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Dirección de un puntero a una [**interfaz ID3DXSkinInfo,**](id3dxskininfo.md) que representa el objeto de malla de máscara creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Use [**SetIonalInfluence para**](id3dxskininfo--setboneinfluence.md) rellenar el objeto de malla de máscara vacío devuelto por este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**SetIonalInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
